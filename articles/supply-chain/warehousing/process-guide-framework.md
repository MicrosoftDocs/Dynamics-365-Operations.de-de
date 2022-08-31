---
title: Framework zur Prozessanleitung
description: Dieser Artikel enthält Informationen zum Prozessleitfaden-Framework für Entwickler, die unsere mobilen Lagerprozesse in X++ erweitern.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e88f32e0347a808d03615cf85e50b1592d691670
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860434"
---
# <a name="process-guide-framework"></a>Framework zur Prozessanleitung

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zum Prozessleitfaden-Framework für Entwickler, die die mobilen Lagerprozesse in X++ erweitern. Durch die Aufteilung der Prozesse in kleine Schritte sind die mobilen Prozesse am Lagerort erweiterbar. Die Geschäftslogik und das Erstellen der Benutzeroberfläche jedes Schritts wurden in einzelne Klassen extrahiert, was eine Erweiterbarkeit ermöglicht.

## <a name="overview-of-the-existing-design"></a>Überblick über das bestehende Design

Die mobilen Ausführungsabläufe im Lagerort werden über einen einzigen benutzerdefinierten Service-Endpunkt bereitgestellt. Die Anfrage kommt von der mobilen App in Form einer XML-Zeichenfolge, die die Metadaten der in der mobilen App präsentierten Benutzeroberfläche sowie die vom Benutzer eingegebenen Werte enthält.

Wenn die Anforderung empfangen wird, besteht der erste Schritt darin, dieses XML zu deserialisieren. Die **WHSMobileAppServiceXMLTranslator**-Klasse konvertiert das XML in einen Container, der sowohl die Steuerungsinformationen als auch Sitzungsinformationen enthält.

Anschließend wird aus den Informationen im Container abgeleitet, an welchem Lagerortprozess der Benutzer gerade arbeitet oder welchen er gerade starten wird (dargestellt durch die **WHSWorkExecuteMode**-Enumeration) und instanziieren dementsprechend eine abgeleitete Klasse von **WHSWorkExecuteDisplay**. Die **displayform()**-Methode wird aufgerufen, die dann Folgendes tut:

-   Sie verarbeitet die Daten des Benutzers (an die **WHSRFControlData**-Klasse delegiert, aber einige Prozesse implementieren eine bestimmte Logik, indem sie die **processControl()**-Methode außer Kraft setzen).

-   Führt Geschäftslogik aus.

-   Erhöht den Schritt.

-   Erstellt den Container, der die neue Benutzeroberfläche darstellt (normalerweise in einer **build…()**-Methode).

Der Container wird dann an den Übersetzer zurückgegeben, der dann das XML serialisiert und als Antwort an das mobile Gerät zurücksendet.

Das folgende Sequenzdiagramm zeigt eine Übersicht über den Ausführungs-Flow. Beachten Sie, dass das Diagramm eher eine schematische Übersicht und keine 1:1-Darstellung des tatsächlichen Codes ist.

![Schematischer Überblick über den Prozess.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Grund für den Neuentwurf

Der obige Entwurf bietet einen sehr einfachen Rahmen für die Erstellung von Prozessen, die in mobilen Flows verwendet werden. Wie jedoch oben ersichtlich ist, übernehmen die **displayform()**-Methoden mehrere Aufgaben. Es delegiert sie zwar an andere Methoden und Klassen, aber in Ermangelung konkreter Klassenverantwortlichkeiten erfolgt dies auf inkonsistente Weise über Klassen hinweg. Da die Zahl der unterstützten Szenarien organisch wächst, können einige dieser Klassen außerdem recht komplex werden. Um die Sache interessanter zu machen, werden einige dieser Klassen/Methoden überschrieben und in mehreren Modi wiederverwendet. Das Ergebnis sind extrem lange Methoden mit hoher zyklomatischer Komplexität. Diese haben in der Vergangenheit zu Wartungsproblemen geführt. Das Beheben von Fehlern in diesen Methoden war riskant und regressionsanfällig.
Zum Beispiel wird die **processWorkLine()**-Methode in der **WhsWorkExecuteDisplay**-Klasse von mehreren Prozessen referenziert (im Grunde überall dort, wo eine Arbeitsausführung durchgeführt wird).

Um Erweiterbarkeit dafür zu erreichen, besteht eine der Optionen darin, die **displayForm**-Methoden in kleinere Methoden umzuwandeln und Erweiterbarkeitspunkte einzuführen. Aufgrund der Szenariomatrix wäre es jedoch für Partner eine Herausforderung, Erweiterungen zu schreiben und gegen Regressionen zu validieren. Darüber hinaus würde der Code aufgrund des oben erwähnten Mangels an einer strukturierten Verantwortungsverteilung im Laufe der Zeit auf unvorhersehbare Weise wachsen, was eine Herausforderung beim Aufbau von Qualitätserweiterungen darstellt.

Damit ist die Neugestaltung die nachhaltige Option, mit dem Ziel klar definierte Klassen mit eigenständigen Zuständigkeiten zu erhalten. Eine Klasse sollte eine Zuständigkeit, einen Grund zum Wechseln und einen Grund zur Erweiterung haben.

## <a name="design-overview"></a>Designübersicht

Im neu gestalteten Rahmen dreht sich die Kernstrategie um zwei Prinzipien: den Ausführungs-Flow in einzelne Komponenten mit klar definierten Verantwortlichkeiten zu unterteilen und in jeder der Komponenten klar definierte Erweiterungspunkte zu haben.

Der Name für das neue Framework lautet „ProcessGuide“. Dies liegt daran, dass das Ziel dieser Klassen darin besteht, einen Benutzer durch einen Geschäftsprozess zu führen (im Gegensatz zum Rich Client, bei dem es sich um eine formularbasierte Erfahrung handelt, bei der der Benutzer mehr Flexibilität bei der Interaktion mit den Daten oder in der Reihenfolge seiner Aufgabenausführung hat).

> [!NOTE]
> Ein bemerkenswertes Detail ist das bewusste Weglassen des „WHS“-Präfixes. Während die mobilen Prozesse ursprünglich für die Lagerhaltung eingeführt wurden, haben sie später Grenzen überschritten, um verschiedene Prozesse bei der Produktions- und Lagerverwaltung zu unterstützen. Infolgedessen wurde die Lagerortreferenz im Namen des Frameworks ausgeschlossen.

Um die Komponenten zu identifizieren, ist der erste Schritt ein Blick auf den Produktionsstartprozess (**WhsWorkExecuteDisplayProdStart**-Klasse). Dies ist ein Schema des Prozesses.

![Bild des schematischen Prozesses.](media/production-start-process-schematic.png)

Betrachtet man die Ablaufsteuerung, sind die folgenden Komponenten erforderlich:

-   Ein Controller, der den gesamten Geschäftsprozess durchläuft.
-   Ein Schritt, der für die Ausführung eines Schritts im Prozess verantwortlich ist.
-   Ein Datenprozessor zum Verarbeiten der Daten in einem Schritt.
-   Ein Seitenersteller, der für das Erstellen der Benutzeroberfläche für einen Schritt verantwortlich ist.
-   Ein Navigationsagent, der für den Schrittübergang verantwortlich ist.
-   Eine Klasse, die für die Ausführung des Geschäftsprozesses verantwortlich ist.

Wenn Sie im obigen Prozessablaufdiagramm mit Schritt 1 beginnen und mit der Verarbeitung der Daten aus dem vorherigen Schritt beginnen und dann mit dem Erstellen einer Benutzeroberfläche enden, werden die Daten im nächsten Schritt weiter verarbeitet. Dies führt zu einer engen Kopplung zwischen aufeinanderfolgenden Schritten. Als Ergebnis würde unser neues allgemeines Schema wie folgt aussehen:

![Bild eines allgemeinen schematischen Prozesses.](media/high-level-schematic.png)

Im Folgenden sind die wichtigsten Komponenten des neu gestalteten Prozesses aufgeführt:

-   **ProcessGuideController** – Diese Klasse orchestriert die Gesamtausführung des Geschäftsprozesses. Es definiert die Werke, die den Schritt instanziieren, und den Navigationsagenten, die später die Prozessausführung bilden, sowie die Bereinigungslogik zum Abbruch oder Verlassen des Prozesses.

-   **ProcessGuideStep** – Diese Klasse repräsentiert einen einzelnen Schritt im Geschäftsprozess. Diese Klasse enthält eine Definition der Werke, die einen Seitenersteller, Aktionen und Datenprozessoren instanziieren, und ist dafür verantwortlich, diese in der richtigen Reihenfolge aufzurufen.

-   **ProcessGuideNavigationAgent** – Diese Klasse ist für die Navigation zwischen den Schritten verantwortlich. Wenn ein Schritt abgeschlossen ist, ist der Navigationsagent für die Definition des nächsten Schritts verantwortlich und übergibt alle Parameter, die der vorherige Schritt möglicherweise an den Nächsten kommunizieren muss.

-   **ProcessGuidePageBuilder** – Diese Klasse ist für die Instanziierung der Benutzeroberfläche verantwortlich.

-   **ProcessGuideAction** – Diese Klasse stellt eine Aktion dar, die dem Benutzer als Schaltfläche angezeigt wird.

-   **ProcessGuideDataProcessor** – Diese Klasse ist für die Verarbeitung der vom Benutzer eingegebenen Daten in einem Feld verantwortlich.

## <a name="execution-flow"></a>Ausführungsablauf

Der Startpunkt des Ausführungsablaufs bleibt unverändert. Die Anfrage kommt also immer noch über dieselben Endpunkte an, gefolgt von der XML-Deserialisierung in den Container. Dieser Container wird dann an **getNextFormState()** übergeben.

Es sind drei wichtige Klassen zu beachten:

-  **ProcessGuideSessionState** – Diese enthält die Informationen zum Sitzungsstatus – Modus, Durchgang, Controller und ausgeführter Schritt usw.

-  **ProcessGuidePage** – Diese enthält eine stark typisierte Darstellung der Metadaten der Benutzeroberfläche.

-  **ProcessGuideRequest** – Diese enthält die beiden oben genannten Klassen als Mitglieder und ist eine stark typisierte Darstellung der vom mobilen Gerät empfangenen Anfrage.

Diese Klassen werden unter Verwendung der Containerinformationen (sowohl Zustands- als auch vom Benutzer eingegebene Steuerdaten) erstellt. Dies bietet eine typsichere Möglichkeit, auf die Werte zuzugreifen und sie zu bearbeiten. Verglichen mit dem wiederholten Zugriff auf den Container während des Prozesses bringt dies Vorteile sowohl hinsichtlich der Lesbarkeit als auch der Leistung.

Die Sitzungsstatusinformationen werden verwendet, um die richtige **ProcessGuideController**-Klasse zu instanziieren. Einmal instanziiert wird die **createResponse()**-Methode in der **ProcessGuideController**-Klasse aufgerufen. Diese Methode ist der Einstiegspunkt in die Prozessleitlogik und kommt nach der Ausführung mit der Antwort zurück (in der **ProcessGuideResponse**-Klasse dargestellt). Die Antwort wird dann zurück in den Container konvertiert und an die Legacy-Logik übergeben, die sie dann in XML serialisiert und die Antwort an das mobile Gerät zurücksendet.

Als Nächstes muss der Controller den nächsten auszuführenden Schritt finden. Wenn dies der Beginn eines neuen Prozesses ist, ruft der Controller **initialStep()** auf, um den ersten Schritt des Prozesses zu abzurufen. Danach würde er die **execute()**-Methode in **ProcessGuideStep** anrufen. Diese Methode würde dann eine **ProcessGuidePageBuilder**-Klasse instanziieren und **buildPage()** anrufen. Dieses Element würde mit einem **ProcessGuidePage**-Objekt zurückkehren, das eine virtuelle Darstellung der Benutzeroberfläche ist, die dem Benutzer präsentiert werden soll. Der Schritt würde dann das Ergebnis an den Controller zurücksenden, der dann den aktuellen Sitzungsstatus speichert und dann das Ergebnis an **getNextFormState()** in Form der **ProcessGuideResponse**-Klasse zurückgibt. Danach wird die Antwort zurück in den Container konvertiert und anschließend in XML serialisiert, und die Antwort wird an das mobile Gerät zurückgesendet.

Das folgende Sequenzdiagramm erläutert diese Ablaufsteuerung. Beachten Sie, dass dies die gebräuchlichste Ablaufsteuerung ist (zur Erklärung des Designs vereinfacht).

![Vereinfachte Ablaufsteuerung.](media/control-flow.png)

Wenn der Benutzer eine Aktion auf dem mobilen Gerät ausführt, indem er auf eine Schaltfläche klickt (oder einen Wert scannt – was normalerweise die Standardaktion auslöst) – kommt die Anfrage bei der **createResponse()**-Methode in der **ProcessGuideController**-Klasse über den gleichen Weg an. Diesmal weiß der Controller jedoch anhand der Sitzungsstatusinformationen, in welchem Schritt sich der Benutzer befindet. Dementsprechend instanziiert er die entsprechende **ProcessGuideStep**-Klasse und ruft die execute-Methode auf. Die **ProcessGuideStep** liest wiederum den vom Benutzer aufgerufenen Aktionsnamen und instanziiert dann die entsprechende **ProcessGuideAction**-Klasse und ruft **execute()** auf.

Die **ProcessGuideAction**-Klasse ist für die Ausführung der spezifischen Aktion zuständig. Es gibt jedoch zwei bemerkenswerte Ausnahmen.

Die erste ist die **ProcessGuideOKAction**-Klasse. Diese Aktion impliziert, dass der Benutzer den Vorgang bestätigen und fortfahren möchte. Dementsprechend führt diese Methode tatsächlich einen Callback an die ProcessGuideStep-Klasse aus, was bedeutet, dass der Schritt **processData()** in **ProcessGuideDataProcessor** aufruft. Dieser verarbeitet die vom Benutzer eingegebenen Daten, aktualisiert dann den Status des Schritts und sendet das Ergebnis an den Controller zurück. Abhängig vom Prozessorergebnis ruft der Schritt den Seitenersteller auf, um die entsprechende Benutzeroberfläche zu erstellen, oder setzt den Status des Schritts auf „Abgeschlossen“. Dies wird in der oberen Hälfte des nachfolgenden Sequenzdiagramms widergespiegelt.

Die andere Ausnahme ist die Stornierungsaktion, die in den **ProcessGuideCancelResetProcessAction**- und **ProcessGuideCancelExitProcessAction**-Klassen implementiert wird. Diese Aktionen stellen die Absicht dar, den Prozess abzubrechen und entweder zum Start des Prozesses zurückzukehren oder den Prozess vollständig zu beenden. Ähnlich wie die **OK**-Aktion führen diese Aktionen auch einen Rückruf zum Schritt aus, der die Absicht an das **ProcessGuideController**-Element signalisiert. Der Controller führt dann die erforderliche Bereinigung der Zustandsvariablen durch und verschiebt das Steuerelement entweder zum Anfangsschritt des Prozesses oder beendet den Prozess insgesamt.

Nachdem der Schritt abgeschlossen ist, wenn der Status des Schritts auf **Abgeschlossen** gesetzt ist, dann instanziiert der Controller das **ProcessGuideNavigationAgent**-Element, das den Namen des nächsten Schritts zurückgibt. Der Controller instanziiert dann diesen Schritt und ruft die **execute()**-Methode auf – und der Kreislauf geht weiter. Am häufigsten ruft der neue Schritt das entsprechende **ProcessGuidePageBuilder**-Element auf, um die Benutzeroberfläche für den nächsten Bildschirm zu erstellen, der dem Benutzer präsentiert und dann zurückgesendet wird. Dieser Flow wird in der oberen Hälfte des nachfolgenden Sequenzdiagramms dargestellt.

![Sequenzdiagramm.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Aufbau eines neuen Prozesses mit dem ProcessGuide-Framework

Die Ablaufsteuerung lässt sich am besten anhand eines in der Anwendung vorhandenen Beispiels – dem Production Start-Prozess – erklären.

## <a name="overview-of-the-production-start-process"></a>Überblick über den Produktionsstartprozesses

Beginnen wir damit, den Prozessablauf zu verstehen. Im ersten Schritt wird der Benutzer nach der Produktionsauftrag-ID gefragt.

![Aufforderung nach Produktions-ID.](media/production-id-prompt.png)

Wenn der Benutzer die Produktionsauftrags-ID eingibt, wird die Auftragsnummer validiert. Einige der ausgeführten Validierungen basieren darauf, ob sich die Bestellung am selben Lagerort befindet, bei dem der Benutzer angemeldet ist, sowie auf dem Status der Bestellung. Wenn die Validierung fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt. Wenn die Validierung erfolgreich ist, werden dem Benutzer Details zum Produktionsauftrag und zum Artikel angezeigt.

Der Benutzer kann entweder abbrechen, um zum Anfang des Prozesses zurückzukehren, oder auf **OK** klicken, um zu bestätigen. Im letzteren Fall wird der Produktionsauftrag auf den **Gestartet**-Status gesetzt, die entsprechenden Erfassungen werden gebucht, das Steuerelement kehr zum ersten Schritt zurück und dem Benutzer wird die Meldung „Arbeit abgeschlossen“ angezeigt.


## <a name="creating-the-controller"></a>Erstellen des Controllers

Der erste Schritt bei der Erstellung des Geschäftsprozesses besteht darin, die controller-Klasse zu erstellen, die aus der abstrakten **ProcessGuideController**-Klasse erweitert wird, die das Standardverhalten eines Controllers implementiert. Der neue Klassenname ist **ProdProcessGuideProductionStartController** und ist mit dem **WHSWorkExecuteMode**-Wert von **StartProdOrder** dekoriert. Die gleiche auf **SysExtension** basierte Instanziierung, die in den **WHSWorkExecuteDisplay**-Klassen verwendet werden, die bei der Instanziierung des Controllers helfen, wenn der Benutzer ein Menüelement für diesen Modus ausführt.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Das Namensmuster der Klasse ist **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Dies ist das Muster, das für die controller-Klassen und zur Erweiterung auf andere Klassen verwendet wird.


## <a name="building-the-first-step"></a>Den ersten Schritt erstellen

Um den ersten Schritt zu definieren, erstellen Sie als Nächstes die **ProdProcessGuidePromptProductionIdStep**-Klasse, die sich aus **ProcessGuideStep** erweitert.

Die Instanziierung der Klasse wird an eine Schritt-Factory delegiert, die von der **ProcessGuideController**-Basisklasse aufgerufen wird. Die Standardimplementierung der Factory instanziiert den Schritt basierend auf dem Namen. Daher müssen Sie zur Instanziierung von **ProdProcessGuidePromptProductionIdStep** als ersten Schritt im Controller zwei Dinge tun:

-   Dekorieren Sie die **ProdProcessGuidePromptProductionIdStep**-Klasse mit einem **ProcessGuideStepName**-Attribut.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Implementieren Sie in der controller-Klasse die abstrakte Methode **initialStepName()**, um den Schrittnamen zurückzugeben.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Der Wert im **ProcessGuideStepName**-Attribut muss, wie oben gezeigt, nicht genau mit dem Klassennamen übereinstimmen. Die Implementierung ermöglicht jedoch Einheitlichkeit und Typsicherheit bei Querverweisen bei der Verwendung der Klasse. Es wird empfohlen, diese Namenskonvention zu verwenden.
>
> Die auf **ProcessGuideStepName** basierte Instanziierung des Schrittes ist in der **ProcessGuideStepDefaultFactory**-Klasse implementiert. In dem seltenen Fall, dass Sie eine andere Strategie für die Instanziierung des Schritts wünschen, müssen Sie Folgendes tun:
> -   Erstellen Sie eine neue Factory-Klasse, die von **ProcessGuidStepAbstractFactory** erbt.
> -   Erstellen Sie optional eine neue Parameterklasse, die die **ProcessGuideIStepCreationParameters**-Schnittstelle implementiert, die die Parameter enthält, die die Fabrik benötigen würde.
> -   Überschreiben Sie in Ihrer controller-Klasse die **stepFactory()**- und **stepCreationParameters()**-Methoden, um die obige Factory und die Parameter zurückzugeben.

Der nächste Schritt besteht darin, die Funktionalität der **ProdProcessGuidePromptProductionIdStep**-Klasse zu implementieren. Sie müssen die Logik zum Erstellen der Benutzeroberfläche, zum Verarbeiten der vom Benutzer eingegebenen Daten und zum Bestimmen, wann der Schritt abgeschlossen ist, implementieren.

### <a name="building-the-user-interface-for-the-first-step"></a>Erstellen der Benutzeroberfläche für den ersten Schritt

Die Benutzeroberfläche wird mit einer Klasse erstellt, die von der abstrakte **ProcessGuidePageBuilder**-Klasse erbt. Benennen Sie für diesen Schritt die Klasse, um darzustellen, was sie tut – **ProdProcessGuidePromptProductionIdPageBuilder**.

Der Instanzierungsmechanismus der Klasse ähnelt dem, mit dem der Schritt vom Controller instanziiert wurde. 

-   Dekorieren Sie die **ProdProcessGuidePromptProductionIdPageBuilder**-Klasse mit einem **ProcessGuidePageBuilderName**-Attribut.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Implementieren Sie in der **ProdProcessGuidePromptProductionIdStep**-Klasse die abstrakte Methode **pageBuilderName()**, um diesen Namen zurückzugeben.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Ähnlich wie bei der Schritt-Factory ist auch für die Seitenersteller-Factory ein abstraktes Factory-Muster implementiert. In dem seltenen Fall, dass Sie eine andere Strategie für die Instanziierung des Seitenerstellers wünschen, können Sie Folgendes tun:
> - Erstellen Sie eine neue Factory-Klasse, die von **ProcessGuidePageBuilderAbstractFactory** erbt.
> - Erstellen Sie optional eine neue Parameterklasse, die die **ProcessGuideIPageBuilderCreationParameters**-Schnittstelle implementiert, die die Parameter enthält, die die Fabrik benötigen würde.
> - Überschreiben Sie in Ihrer step-Klasse die **pageBuilderFactory()**- und **pageBuilderCreationParameters()**-Methoden, um die obige Factory und die Parameter zurückzugeben.

Um die Benutzeroberfläche zu implementieren, benötigen Sie eine Seite mit einem Textfeld zur Eingabe der Produktionsauftrags-ID sowie einer **OK**-Schaltfläche und einer **Abbrechen**-Schaltfläche. Die **Abbrechen**-Schaltfläche sollte den Vorgang beenden.

Um dies zu implementieren, müssen Sie zwei Methoden in der **ProdProcessGuidePromptProductionIdPageBuilder**-Klasse implementieren:

-   Verwenden Sie die **addDataControls()**-Methode, um das Textfeld hinzuzufügen.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Verwenden Sie die **addActionControls()**-Methode zum Hinzufügen der **OK**- und **Abbrechen**-Schaltflächen.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Dadurch werden die Datensteuerelemente hinzugefügt, gefolgt von den Schaltflächen. Wenn Sie jedoch einen Bildschirm mit eingestreuten Datensteuerelementen und Schaltflächen erstellen möchten, können Sie stattdessen für Flexibilität die **addControls()**-Methode außer Kraft setzen.

Ein weiteres zu berücksichtigendes Szenario ist die Neuaufbau der Seite im Falle von Validierungsfehlern, beispielsweise wenn der Benutzer eine falsche Produktionsauftrags-ID eingibt. Die **ProcessGuidePageBuilder**-Basisklasse implementiert das Standardverhalten, das die Benutzeroberfläche neu erstellt, den gescannten Wert löscht und die Fehlerkontrolle mit der Fehlermeldung hinzufügt. Da dies das Standardverhalten ist, das Sie verwenden möchten, müssen Sie keinen Code für die Fehlerbehandlung hinzufügen.

> [!TIP]
> Wenn Sie benutzerdefiniertes UI-Verhalten für Fehlersituationen implementieren möchten, können Sie eine oder mehrere der Methoden **rebuildFromRequestPage()**, **isErrorState()** und **reuseRequestPageOnError()** außer Kraft setzen.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Verarbeitung der vom Benutzer eingegebenen Daten im ersten Schritt

Die Verarbeitung der Daten erfolgt in der **ProcessGuideDataProcessorDefault**-Klasse, die wiederum die Legacy-Klasse **WhsRfControlData** aufruft. An diesem Standardverhalten sind keine Änderungen erforderlich, und **WhsRfControlData** hat bereits eine Logik zur Validierung des **ProdId**-Feld, sodass Sie keine Logik für die Handhabung schreiben müssen. Falls Erweiterungen für die Validierungslogik erforderlich sind, ziehen Sie die Verwendung der auf **WhsControl** basierten Erweiterungsmechanismus in Betracht.

### <a name="determine-if-the-first-step-is-complete"></a>Feststellen, ob der erste Schritt abgeschlossen ist

Wenn die Validierung erfolgreich ist, ist es an der Zeit, den Schritt als abgeschlossen zu markieren. Dies geschieht in der Basisklasse, Sie müssen jedoch die Bedingung implementieren, um den Schrittabschluss zu bestimmen. Dies erledigt die folgende außer Kraft gesetzte Methode.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Schritt 2: Bestelldetails anzeigen und bestätigen

Im zweiten Schritt wird dem Benutzer ein Bildschirm mit Details zur Bestellung angezeigt. Der Benutzer kann entweder auf die **OK**-Schaltfläche klicken, um den Start des Produktionsauftrags zu bestätigen, oder auf **Abbrechen**, um zum Anfang des Prozesses zurückzukehren. Nennen Sie für dieses Beispiel den Schritt **ProdProcessGuideConfirmProductionOrderStep** und die Seitenersteller-Klasse **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Die ProdProcessGuideConfirmProductionOrderStep-Klasse sieht wie folgt aus.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Da der Benutzer hier keine Werte eingibt, müssen Sie die **isComplete()**-Methode außer Kraft setzen. Der Schritt ist abgeschlossen, wenn der Benutzer auf **OK** klickt.

Die Seitenersteller-Klasse überschreibt die **addDataControls()**-Methode, um drei Etiketts hinzuzufügen. Das erste Etikett zeigt die Produktionsauftrags-ID, das zweite enthält Artikelinformationen (wie Artikel-ID, Abmessungen oder Beschreibung) und das dritte enthält die Menge und Maßeinheit.

**addActionControls()** wird dann überschrieben, um 2 Schaltflächen hinzuzufügen – die **OK**-Schaltfläche, und die **Abbrechen**-Schaltfläche, um den Vorgang abzubrechen und zum Anfang des Vorgangs zurückzukehren.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Sie finden denselben Quellcode für die X++-Methoden in diesem Artikel mithilfe des Anwendungs-Explorers. Filtern Sie nach dem Klassennamen, klicken Sie dann mit der rechten Maustaste auf den Klassennamen und wählen Sie **Code anzeigen**.

### <a name="step-3-start-the-production-order"></a>Schritt 3: Den Produktionsauftrag starten

Im dritten Schritt wird die Geschäftslogik zum Starten des Produktionsauftrags ausgeführt. Dieser Schritt unterscheidet sich etwas von den vorherigen Schritten, da dieser Schritt keine Benutzeroberfläche hat. Dieser Schritt wird im Hintergrund ausgeführt, wenn der Benutzer im vorherigen Schritt auf **OK** klickt.

Die abstrakte **ProcessGuideStepWithoutPrompt**-Klasse implementiert das Standardverhalten für solche Schritte. Der aktuelle Schritt sollte daher die **ProcessGuideStepWithoutPrompt**-Klasse erweitern und die **doExecute()**-Methode außer Kraft setzen.

Das folgende Codebeispiel zeigt die Klasse und die **doExecute()**-Methodenimplementierung. Die Methode ruft einfach die Auftrags-ID und die Benutzer-ID aus dem Sitzungsstatus ab und ruft die Methode auf, um diesen Produktionsauftrag zu starten.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Im Falle einer Ausnahme stellt die Ausnahmebehandlungslogik des Frameworks sicher, dass der Prozess auf den vorherigen Schritt zurückgesetzt wird.

> [!NOTE]
> Der Aufruf von **addProcessCompletionMessage()** fügt den Navigationsparametern die Meldung „Arbeit abgeschlossen“ hinzu. Im nächsten Schritt (vorausgesetzt, er verfügt über eine Benutzeroberfläche) wird diese Meldung angezeigt. Die Basisklassen behandeln diese Logik, und es muss kein spezieller Code zu den Prozessklassen hinzugefügt werden, um dieses Verhalten zu erreichen.


### <a name="building-the-navigation-through-the-steps"></a>Aufbau der Navigation durch die Schritte

Die **ProcessGuideController**-Basisklasse instanziiert die **ProcessGuideNavigationAgentDefault**-Klasse, die auf einer vordefinierten Navigationsroute basiert, die eine einfache Karte mit Quell- und Zielschritten ist. Für das Produktionsstartszenario würde diese Implementierung ausreichen, da es keine bedingte Verzweigung gibt. Daher müssen Sie nur die **initializeNavigationRoute()**-Methode zum Definieren der Navigationsroute außer Kraft setzen.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Es gibt Prozesse, bei denen es zu einer bedingten Verzweigung kommt (basierend auf Benutzeraktionen oder anderen Bedingungen). Solche Prozesse müssen Folgendes tun:

-   Bestimmte Navigationsagenten implementieren, die von der **ProcessGuideNavigationAgent**-Klasse geerbt wurden.

-   Die spezifische Navigationsagent-Factory implementieren, die von der **ProcessGuideNavigationAgentAbstractFactory**-Klasse geerbt wurde, die Logik enthält, um den richtigen Navigationsagent basierend auf dem aktuellen Schritt, dem Sitzungsstatus, der Benutzeraktion oder einer anderen Logik zu instanziieren.

-   Optional **navigationAgentCreationParameters()** in der Controller-Klasse überschreiben, um geeignete Parameter zu übergeben.

-   **navigationAgentFactory()** im Controller überschreiben, um die oben erstellte Navigationsagent-Factory zu instanziieren.

### <a name="action-classes"></a>Aktionsklassen

Aktionsklassen stellen Benutzeraktionen dar, daher verwendet dieses Beispiel die **OK**-Aktion, um zu zeigen, wie die Aktionen erstellt werden.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Die Klasse muss 2 abstrakte Methoden implementieren:

-   **label()**, die das in einem mit dieser Aktion verknüpften Schaltflächensteuerelement anzuzeigende Etikett zurückgibt.

-   **doExecute()**, das die Aktion ausführt. Wie bereits erwähnt, führt die **OK**-Schaltfläche lediglich einen Rückruf zum Schritt aus. Andere Aktionen können hier jedoch eine komplexere Logik haben.

Die Aktionen werden mit **SysExtension**-Framework auf der Grundlage des **ProcessGuideActionName**-Attributs instanziiert. Ähnlich wie bei der Instanziierung von Seitenerstellern implementiert die Schrittklasse die Standardaktions-Factory, und es ist möglich, diese zu überschreiben. Der Seitenersteller fügt ein Schaltflächen-Steuerelement wie dieses hinzu.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Dabei fordert er den Schritt auf, eine Aktionsklasse für den übergebenen Namen zu erstellen, und verknüpft diese Aktion mit der Schaltfläche.

### <a name="summary"></a>Übersicht

Um alles zusammenzufassen, was in diesem Artikel erklärt wurde, finden Sie hier eine umfassende Zusammenfassung des für den Prozess erforderlichen Codes:

1.  **ProdProcessGuideProductionStartController**

    1.  **initialStepName()** überschreiben, um den Namen des ersten Schrittes anzugeben.
    2.  **initializeNavigationRoute()** überschreiben, um die Navigationskarte zu erstellen.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  **isComplete()** überschreiben, um anzugeben, wann der Schritt als abgeschlossen gilt.
    2.  **pageBuilderName()** überschreiben, um den zu verwendenden Seitenersteller anzugeben.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  **addDataControls()** überschreiben, um das **Produkt-ID**-Textfeld hinzuzufügen.
    2.  **addActionControls()** überschreiben, um die **OK**- und **Abbrechen**-Schaltflächen hinzuzufügen.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  **pageBuilderName()** überschreiben, um den zu verwendenden Seitenersteller anzugeben.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  **addDataControls()** überschreiben, um die Auftrags-, Artikel- und Mengeninformationsetiketten hinzuzufügen.

    2.  **addActionControls()** überschreiben, um die **OK**- und **Abbrechen**-Schaltflächen hinzuzufügen.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Die **generateItemInfoForProdId()**-Methode, die zum Generieren der Artikelinformationsetiketten verwendet wird, ist von diesem Artikel ausgeschlossen. Diese Methode fragt einige Tabellen ab, um Artikel-ID, Beschreibung und Abmessungen abzurufen. Wenn Sie ein besseres Verständnis von **generateItemInfoForProdId()** erhalten möchten, schauen Sie sich den Quellcode an.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  **doExecute()** überschreiben, um den Produktionsstartprozess durchzuführen und die Prozessabschlussmeldung hinzuzufügen.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Beachten Sie, dass viele der gängigen Muster (Neugenerierung der Benutzeroberfläche bei Fehler, Einstellung der Meldung zum Abschluss des Prozesses, **OK**- und **Abbrechen**-Verhalten) in das Framework verschoben wurden – wodurch der Anwendungsentwickler davor bewahrt werden, Boilerplate-Code zu schreiben, der sowohl fehleranfällig ist als auch das Risiko eines inkonsistenten Verhaltens über Prozesse hinweg birgt. Wo das Szenario jedoch vom gemeinsamen Pfad abweichen muss, hat der Anwendungsentwickler die Möglichkeit, geeignete Methoden zu überschreiben – aber dann ist dies eine bewusste Abweichung, die sowohl explizit als auch nachvollziehbar ist.


### <a name="extending-a-business-process"></a>Erweitern eines Geschäftsablaufs

Bisher wurde in diesem Artikel hervorgehoben, wie ein neuer Prozess mithilfe der **ProcessGuide**-Frameworks verwendet wird. In diesem letzten Abschnitt finden Sie einige Beispiele, wie dieser Geschäftsprozess erweitert werden kann.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Einen Schritt in einem Flow hinzufügen (mit ProcessGuideNavigationAgentDefault)

Wo erweitert wird:

-   Untergeordnetes Element der **ProcessGuideController**-Klasse für den Prozess.

Wie erweitert wird:

-   Erweitern Sie die **initializeNavigationRoute()**-Methode in der Controller-Klasse, und rufen Sie in der **ProcessGuideNavigationRoute**-Klasse **addFollowingStep()** auf.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Einen Schritt in einem Flow hinzufügen (mit benutzerdefiniertem Navigationsagent)

Wo erweitert wird:

-   Untergeordnetes Element von **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Wie erweitert wird:

-   Erstellen Sie eine neue untergeordnete Klasse von **ProcessGuideNavigationAgent**, die den gewünschten Schrittnamen zurückgibt.

-   Erstellen Sie eine neue Klasse, die von **ProcessGuideNavigationAgentFactory** abgeleitet ist, die bedingt den oben erstellten Navigationsagenten zurückgibt.

-   Erweitern Sie die **navigationAgentFactory()**-Methode in der Controller-Klasse, um die oben erstellte Navigationsagent-Factory zurückzugeben.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Hinzufügen eines neuen Steuerelements in der Benutzeroberfläche eines vorhandenen Schritts 

Wo erweitert wird:

-   Untergeordnetes Element von **ProdProcessGuidePageBuilder** für den Schritt.

Wie erweitert wird:

-   Erweitern Sie die **addDataControls()**-Methode, und fügen Sie das zusätzliche Steuerelement hinzu.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Komplette Überarbeitung der Benutzeroberfläche in einem bestehenden Schritt

Wo erweitert wird:

-   Untergeordnetes Element von **ProdProcessGuideStep**.

Wie erweitert wird:

-   Erstellen Sie eine neue untergeordnete Klasse der **ProdProcessGuidePageBuilder**-Klasse, und implementieren Sie die gewünschte Benutzeroberfläche.

-   Erweitern Sie die **pageBuildeName()**-Methode in der Schrittklasse, um das **ProcessGuidePageBuilderNameAttribute**-Element für die oben erstellte Klasse zurückzugeben.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Logik ändern, wenn ein Schritt als abgeschlossen gilt

Wo erweitert wird:

-   Untergeordnetes Element von **ProdProcessGuideStep**.

Wie erweitert wird:

-   Erweitern Sie die **isComplete()**-Methode, um die zusätzliche Logik zu erstellen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]