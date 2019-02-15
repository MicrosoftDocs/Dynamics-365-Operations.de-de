---
title: Verteilte Auftragsverwaltung (DOM)
description: In diesem Thema wird die Funktion der verteilten Auftragsverwaltung (Distributed Order Management, DOM) in Microsoft Dynamics 365 for Retail beschrieben.
author: josaw1
manager: AnnBe
ms.date: 11/15/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8f1b07243ec2d42e47073d8d90f00ea563020d82
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "302333"
---
# <a name="distributed-order-management-dom"></a>Verteilte Auftragsverwaltung (DOM)

[!include [banner](includes/banner.md)]

In dem neuen Paradigma für Einzelhandelsvorgänge bemühen sich Einzelhändler, personalisiertes Customer Engagement, Omnichannel-Erfahrungen und nahtlose Interaktionen bereitzustellen. Da so viele Auswahlmöglichkeiten zur Verfügung stehen, kaufen die Verbraucher bei dem Einzelhändler, bei dem sie die besten Erfahrungen machen. In vielen Fällen sind Preise und Produkte nicht mehr der wichtigste Aspekt für die Kundenentscheidung.

Einzelhändler müssen über alle Kanäle einen Echtzeitüberblick über ihren Bestand haben, um die Customer Experience zu verbessern. Mit einer einzigen, umfassenden Ansicht des gesamten Lagerbestands können Auftragserfüllung, Zuteilung und Verteilung optimiert werden. Aus diesem Grund werden die Annahme und Implementierung einer verteilten Auftragsverwaltung (DOM) für Einzelhändler immer wichtiger.

In einem komplexen Netzwerk von Systemen und Prozessen optimiert DOM die Auftragserfüllung. Sie basiert auf einer einzigen, globalen Ansicht der Lagerbestände in der gesamten Organisation, sodass Bestellungen intelligent verwaltet und genau und konstengünstiger abgewickelt werden. Dank der besseren Effizienz in der Lieferkette von Einzelhändlern, können diese die Erwartungen ihrer Kunden mithilfe der DOM besser erfüllen.

Die folgende Abbildung zeigt den Lebenszyklus eines Auftrags in einem System für die verteilte Auftragsverwaltung.

![Lebenszyklus eines Auftrags im DOM-Kontext](./media/flow.png "Lebenszyklus eines Auftrags im DOM-Kontext")

## <a name="set-up-dom"></a>DOM einrichten

1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
2. Erweitern Sie auf der Registerkarte **Konfigurationschlüssel** den Knoten **Einzelhandel**, aktivieren Sie anschließend das Kontrollkästchen **Verteilte Auftragsverwaltung**.
3. Gehen Sie zu **Einzelhandel \> Verteilte Auftragsverwaltung \> Einrichten \> DOM-Parameter**.
4. Legen Sie auf der Registerkarte **Allgemein** die folgenden Werte fest:

    - **Verteilte Auftragsverwaltung aktivieren** – Setzen Sie diese Option auf **Ja**.
    - **Verwenden von Bing Maps für DOM bestätigen** – Setzen Sie diese Option auf **Ja**.

        > [!NOTE]
        > Sie können diese Option nur dann auf **Ja** setzen, wenn die Option **Bing Maps aktivieren** auf der Registerkarte **Bing Maps** der Seite **Freigegebene Einzelhandelsparameter** (**Einzelhandel \> Zentralverwaltungseinrichtung \> Parameter \> Freigegebene Einzelhandelsparameter**) ebenfalls auf **Ja** gesetzt ist und wenn im Feld **Bing Maps-Schlüssel** ein gültiger Schlüssel eingegeben wurde.

    - **Einbehaltungsdauer in Tagen** – Geben Sie an, wie lange von DOM-Abläufen erzeugte Erfüllungspläne im System behalten werden sollen. Der Stapelverarbeitungsjob **Einrichten des Löschenauftrag für DOM-Erfüllungsdaten** löscht alle Erfüllungspläne, die älter sind, als die Anzahl der hier angegebenen Tage.
    - **Ablehnungszeitraum (in Tagen)** – Geben Sie an, wie viel Zeit vergehen soll, bis eine abgelehnte Auftragsposition dem gleichen Standort zugewiesen werden kann.

5. Legen Sie auf der Registerkarte **Solver** die folgenden Werte fest:

    - **Max. Versuche zur automatischen Erfüllung** – Geben Sie an, wie häufig die DOM-Modul versuchen soll, eine Auftragsposition an einen Standort zu vermitteln. Wenn die DOM-Modul eine Auftragsposition nicht nach der angegebenen Anzahl der Versuche einem Standort vermitteln kann, wird die Auftragsposition als Ausnahme markiert. In zukünftigen Abläufen wird die Position dann solange übersprungen, bis der Status manuell zurückgesetzt wird.
    - **Regionsradius für lokales Geschäft** – Geben Sie einen Wert ein. In diesem Feld können Sie festlegen, wie Standorte gruppiert und in Bezug auf die Entfernung als gleichwertig betrachtet werden. Wenn Sie beispielsweise **100** eingeben, wird jedes Geschäft oder Verteilzentrum innerhalb eines 100-Meilen-Radius der Erfüllungsadresse in Bezug auf die Entfernung als gleichwertig betrachtet.
    - **Solver-Typ** – Wählen Sie einen Werttyp aus. Für Retail sind zwei Solver-Typen freigegeben: **Produktions-Solver** und **Vereinfachter Solver**. Für alle Maschinen, auf denen DOM ausgeführt wird (d. h., alle Server, die zur DOMBatch-Gruppe gehören), muss **Produktions-Solver** ausgewählt werden. Der Produktions-Solver erfordert den Lizenzschlüssel, der standardmäßig in Produktionsumgebungen lizenziert und festgestellt wird. Für Nicht-Produktionsumgebungen muss dieser Lizenzschlüssel manuell angegeben werden. Um den Lizenzschlüssel manuellen bereitzustellen, führen Sie die folgenden Schritte aus:

        1. Öffnen Sie in Microsoft Dynamics Lifecycle Services die Bibliothek der freigegebenen Anlage, wählen Sie **Modell** als Anlagentyp aus, und laden Sie die Datei **DOM-Lizenz** herunter.
        2. Starten Sie den Microsoft Internetinformationsdienste (IIS)-Manager, klicken Sie mit der rechten Maustaste auf **AOSService-Website**, und wählen Sie anschließend **Entdecken** aus. Ein Windows Explorer-Fenster wird bei **\<AOS-Dienst-Stamm\>\\webroot** geöffnet. Notieren Sie den Pfad zu \<AOS-Dienst-Stamm\>, da Sie ihn im nächsten Schritt verwenden werden.
        3. Kopieren Sie die Konfigurationsdatei im Verzeichnis **\<AOS-Dienst-Stamm\>\\PackagesLocalDirectory\\DOM\\bin**.
        4. Gehen Sie zum Client "Retail Zentralverwaltung", und öffnen Sie die Seite **DOM-Parameter**. Wählen Sie auf der Registerkarte **Solver** im Feld **Solver-Typ** die Option **Produktions-Solver** aus, und bestätigen Sie, ob keine Fehlermeldungen angezeigt werden.

        > [!NOTE]
        > Der Vereinfachte Solver wird bereitgestellt, damit Einzelhändler die DOM-Funktion ausprobieren können, ohne eine spezielle Lizenz bereitzustellen. Organisationen können den vereinfachten Solver nicht in Produktionsumgebungen verwenden.
        >
        > Obwohl der vereinfachte Solver die gleiche Gruppe von Funktionen bereitstellt wie der Produktions-Solver, bestehen Einschränkungen hinsichtlich der Leistung (die Anzahl von Aufträgen und Auftragspositionen, die in einem Ablauf behandelt werden können) und der Konvergenz der Ergebnisse (möglicherweise liefert ein Auftragsstapel in einigen Szenarien nicht das beste Ergebnis).
     
6. Gehen Sie zurück zu **Einzelhandel \> Verteilte Auftragsverwaltung \> Einrichten \> DOM-Parameter**.
7. Weisen Sie auf der Registerkarte **Nummernkreise** anschließend den verschiedenen DOM-Entitäten die erforderlichen Nummernkreise zu.

    > [!NOTE]
    > Bevor die Nummernkreise zugeordnet werden können, müssen Sie die Entitäten auf der Seite **Nummernkreise** (**Organisationsverwaltung \> Nummernkreise \> Nummernkreise**) definieren.

8. Die DOM-Funktion unterstützt die Definition verschiedener Arten von DOM-Regeln, und Organisationen können abhängig von ihren Geschäftsanforderungen mehrere Regeln konfigurieren. DOM-Regeln können für eine Gruppe von Standorten oder einzelne Standorte sowie für eine bestimmte Produktkategorie, ein Produkt oder eine Variante definiert werden. Um die Gruppierung der Lagerplätze zu erstellen die für die DOM-Regeln verwendet werden müssen, führen Sie die folgenden Schritte aus:

    1. Gehen Sie zu **Einzelhandel \> Kanaleinstellungen \> Erfüllungsgruppen**.
    2. Geben Sie unter **Neu** einen neuen Namen und eine Beschreibung für die neue Gruppe ein.
    3. Wählen Sie **Speichern**.
    4. Wählen Sie **Position hinzufügen**, um einem einzelnen Standort zur Gruppe hinzuzufügen. Aktivieren Sie **Positionen hinzufügen**, um mehrere Lagerplätze hinzuzufügen.

9. Um Regeln definieren, gehen Sie zu **Einzelhandel \> Verteilte Auftragsverwaltung \> Einstellungen \> Verwalten von Regeln**. Die folgenden DOM-Regeln werden derzeit unterstützt:

    - **Mindestlagerbestandsregel** – Durch diesen Regeltyp können Organisationen für andere Zwecke als die Auftragserfüllung "Umzäunungen" für eine bestimmte Menge eines Produkts festlegen. Beispielsweise können Organisationen wünschen, dass DOM nicht den gesamten Bestand berücksichtigt, der in einem Geschäft zur Auftragserfüllung verfügbar ist. Stattdessen müssen Sie einen Lagerbestand für die Laufkundschaft reservieren. Wenn dieser Regeltyp verwendet wird, können Sie beispielsweise den Mindestlagerbestand definieren, der für eine Produktgruppe, ein Einzelprodukt oder eine Produktvariante pro Standort oder Standortgruppe behalten werden soll.
    - **Prioritätsregel für Erfüllungsstandort** – Durch diesen Regeltyp können Organisationen eine Hierarchie der Standorte definieren, um eine Priorität festzulegen, nach der das OM-Modul versucht, Erfüllungsstandorte für bestimmte Produkte zu finden. Der gültige Prioritätsbereich ist 1 bis 10, wobei 1 die höchste Priorität und 10 die niedrigste Priorität hat. Standorte, die höhere Priorität aufweisen, werden vor Standorten berücksichtigt, die niedrigere Priorität haben. Wenn die Regel als uneingeschränkte Einschränkungsregel definiert wird, werden Aufträge nur an Standorte vermittelt, für die Prioritäten definiert wurden.
    - **Partielle Auftragsregel** – Mit dieser Regel können Organisationen definieren, ob ein Auftrag oder Auftragspositionen ein Auftrag teilweise werden kann bzw. können. Folgende Parameter sind verfügbar:

        - **Partielle Aufträge erfüllen?** – Ist die Option auf **Ja** festgelegt, kann DOM nur ein Teil der Menge in einer Auftragsposition erfüllen. Diese teilweise Erfüllung wird erreicht, indem die Auftragsposition aufgeteilt wird.
        - **Partielle Positionen erfüllen?** – Ist die Option auf **Ja** festgelegt, kann DOM nur eine Teilmenge in einer Auftragsposition erfüllen. Diese teilweise Erfüllung wird erreicht, indem die Auftragsposition aufgeteilt wird.
        - **Erfüllen von Auftrag nur von einem einzelnen Standort** – Wenn die Option auf **Ja** gesetzt ist, stellt DOM sicher, das alle Positionen eines Auftrags von einem einzigen Standort aus erfüllt werden.

        In der folgenden Tabelle ist aufgeführt, wie sich DOM verhält, wenn eine Kombination dieser Parameter definiert ist.

        |      | Partielle Aufträge erfüllen | Partielle Positionen erfüllen | Auftrag nur von einem Standort aus erfüllen | Beschreibung |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Ja                    | Ja                   | Ja                                  | Einige Positionen des Auftrags können erfüllt werden, und einzelne Positionen können teilweise erfüllt werden, aber alle Positionen müssen vom selben Standort in einer DOM-Instanz ausgeführt werden. (Diese Kombination wird derzeit nicht unterstützt.) |
        | 2    | Ja                    | Nein                    | Ja                                  | Einige Positionen des Auftrags können erfüllt werden, aber einzelne Positionen können nicht teilweise erfüllt werden, und alle erfüllten Positionen müssen vom selben Standort in einer DOM-Instanz ausgeführt werden. (Diese Kombination wird derzeit nicht unterstützt.) |
        | 3    | Ja                    | Ja                   | Nein                                   | Einige Positionen des Auftrags können erfüllt werden, einzelne Positionen können teilweise erfüllt werden, und alle Positionen können von mehreren Standorten in einer DOM-Instanz erfüllt werden werden. |
        | 4\*  | Nein                     | Nicht zutreffend        | Nein                                   | Alle Auftragspositionen müssen erfüllt werden, einzelne Positionen können nicht teilweise erfüllt werden, und jede Auftragsposition kann von einem anderen Standort erfüllt wurden. |
        | 5\*  | Nein                     | Nicht zutreffend        | Ja                                  | Alle Auftragspositionen müssen erfüllt werden, einzelne Positionen können nicht teilweise erfüllt werden, und alle Auftragspositionen können nur von einem einzigen Standort ausgeliefert wurden. |
        | 6\*  | Nein                     | Nicht zutreffend        | Nein                                   | Diese Kombination funktioniert wie Kombination 4, da **Partielle Positionen erfüllen** nicht auf **Ja** gesetzt sein kann, wenn **Partielle Aufträge erfüllen** auf **Nein** festgelegt ist. |
        | 7\*  | Nein                     | Nicht zutreffend        | Ja                                  | Diese Kombination funktioniert wie Kombination 5, da **Partielle Positionen erfüllen** nicht auf **Ja** gesetzt sein kann, wenn **Partielle Aufträge erfüllen** auf **Nein** festgelegt ist. |
        | 8    | Ja                    | Nein                    | Nein                                   | Einige Positionen des Auftrags können erfüllt werden, aber einzelne Positionen können nicht teilweise erfüllt werden, und die verschiedenen Auftragspositionen können von mehreren Standorten in einer DOM-Instanz erfüllt werden werden. |
        | 9\*  | Nein                     | Nicht zutreffend        | Ja                                  | Alle Auftragspositionen müssen erfüllt werden, und alle Auftragspositionen dürfen nur von einem einzelnen Standort aus erfüllt werden. |

        \* Wenn **Partielle Aufträge erfüllen** auf **Nein** festgelegt wird, wird **Partielle Positionen erfüllen** immer mit **Nein** berücksichtigt, unabhängig davon, wie dieses Feld tatsächlich festgelegt ist.

    - **Regel für Erfüllungsstandort offline** – Mit dieser Regel können Organisationen einen Standort oder eine Standortgruppe für DOM als offline oder als nicht verfügbar angeben, damit dort keine Aufträge zur Erfüllung zugewiesen werden können.
    - **Regel für maximale Ablehnung** – Mit dieser Regel können Organisationen einen Schwellenwert für Ablehnungen definieren. Wenn der Schwellenwert erreicht wird, markiert der DOM-Prozessor einen Auftrag oder eine Auftragsposition als Ausnahme und schließt ihn oder sie durch Entfernen von späterer Bearbeitung aus.

        Wenn Auftragspositionen einem Standort zugewiesen sind, kann der Standort eine zugewiesene Auftragsposition ablehnen, da er aus bestimmten Gründen möglicherweise nicht in der Lage ist, die Position zu erfüllen. Abgelehnte Positionen werden als Ausnahme markiert und wieder in den Pool für die weitere Verarbeitung bei der nächsten Ausführung gestellt. Bei der nächsten Ausführung versucht DOM, die abgelehnte Position einem anderen Standort zuzuweisen. Der neue Standort kann die zugewiesene Auftragsposition auch ablehnen. Dieser Zyklus von Zuweisung und Ablehnung kann wiederholt ausgeführt werden. Wenn die Anzahl der Ablehnungen den definierten Schwellenwert erreicht, markiert DOM die Auftragsposition als permanente Ausnahme und wählt die Position nicht erneut für eine Zuweisung aus. DOM berücksichtigt die Auftragsposition nur dann wieder für eine erneute Zuweisung, wenn ein Benutzer den Status der Auftragsposition manuell zurücksetzt.

    - **Regel für maximale Entfernung** – Mit dieser Regel können Organisationen die maximale Entfernung definieren, in der sich ein Standort oder eine Standortgruppe befinden kann, um den Auftrag zu erfüllen. Wenn Regeln für maximal überlappende Entfernungen für einen Standort definiert werden, wendet DOM die niedrigste maximale Entfernung an, die für diesen Standort definiert ist.
    - **Regel für maximale Auftragsanzahl** – Mit dieser Regel können Organisationen die maximale Anzahl von Aufträgen definieren, die ein Standort oder eine Standortgruppe an einem Kalendertags bearbeiten kann. Wird die maximale Anzahl von Aufträgen einem Standort für einen einzigen Tag zugewiesen, weist DOM diesem Standort für den Rest des Kalendertags keine weiteren Aufträge zu.

    Nachfolgend sind einige der allgemeinen Attribute aufgeführt, die für alle vorhergehenden Regeltypen definiert werden können:

    - **Startdatum** und **Enddatum** – Für jede Regel kann mit diesen Feldern ein Gültigkeitsdatum festgelegt werden.
    - **Deaktiviert** – Nur Regeln, die in diesem Feld den Wert **Nein** haben, werden in einer DOM-Ausführung berücksichtigt.
    - **Unbedingte Einschränkung** – Eine Regel kann als unbedingte oder nicht unbedingte Einschränkung definiert werden. Jede DOM-Ausführung durchläuft zwei Iterationen. In der ersten Iteration wird jede Regel als unbedingte Einschränkungsregel behandelt, unabhängig von der Einstellung dieses Feldes. Das bedeutet, dass jede Regel angewendet wird. Die einzige Ausnahme ist die Regel **Standortpriorität**. In der zweiten Iteration werden die Regeln entfernt, die nicht als unbedingte Einschränkungsregeln definiert wurden, und der Auftrag oder die Auftragspositionen, die bei Anwendung aller Regeln keinen Standorten zugewiesen wurden, werden nun Standorten zugewiesen.

10. Erfüllungsprofile werden verwendet, um eine Regelsammlung, juristische Personen, Auftragsursprünge und Lieferarten zu gruppieren. Jede DOM-Ausführung gilt für ein bestimmtes Erfüllungsprofil. Auf diese Weise können Organisationen eine Gruppe von Regeln für mehrere juristische Personen für Aufträge definieren und ausführen, die bestimmte Auftragsursprünge und -Lieferarten haben. Wenn ein anderer Regelsatz für andere Auftragsursprünge oder Lieferarten ausgeführt werden muss, können die Erfüllungsprofile entsprechend definiert werden. Gehen Sie zum Einrichten von Erfüllungsprofilen folgendermaßen vor:  

    1. Gehen Sie zurück zu **Einzelhandel \> Verteilte Auftragsverwaltung \> Einrichten \> Erfüllungsprofile**.
    2. Wählen Sie **Neu** aus.
    3. Geben Sie in den Feldern **Profil** und **Beschreibung** Werte ein.
    4. Aktivieren Sie die Option **Ergebnis automatisch übernehmen**. Wenn Sie diese Option auf **Ja** setzen, werden die Ergebnisse der DOM-Ausführung für das Profil automatisch in die Auftragspositionen übernommen. Wenn Sie diese auf **Nein** setzen, können die Ergebnisse nur im Erfüllungsplan angezeigt werden können. Sie werden nicht in die Auftragspositionen übernommen.
    5. Wenn das DOM-Profil für Aufträge durchgeführt werden soll, die jeden Auftragsursprung haben, legen sogar Aufträge, in denen der Auftragsursprung nicht definiert ist, die Option **Aufträge mit leerem Auftragsursprung verarbeiten** auf **Ja** fest. Um das Profil nur für einige Auftragsursprünge auszuführen, können Sie sie auf der Seite **Auftragsursprünge** festlegen. Dies wird später erläutert.
    6. Aktivieren Sie auf dem Inforegister **Juristische Personen** die Option **Hinzufügen**, und wählen Sie dann eine juristische Person aus.
    7. Aktivieren Sie auf dem Inforegister **Regeln** die Option **Hinzufügen**, und wählen Sie dann die Regel aus, die mit dem Profil verknüpft werden soll.
    8. Wiederholen Sie die obigen zwei Schritte, bis dem Profil alle erforderlichen Regeln zugeordnet sind.
    9. Wählen Sie **Speichern**.
    10. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Einstellungen**, und wählen Sie **Lieferarten** aus.
    11. Wählen Sie auf der Seite **Lieferarten** die Option **Neu** aus.
    12. Wählen Sie im Feld **Unternehmen** aus, die juristische Person aus. Die Liste der Unternehmen wird auf die juristischen Personen beschränkt, die Sie zuvor hinzugefügt haben.
    13. Im Feld **Lieferart** wählen Sie die Lieferart aus, die diesem Profil zugeordnet werden soll. Eine Lieferart kann nicht mehreren aktiven Profilen zugeordnet werden.
    14. Wiederholen Sie die obigen beiden Schritte, bis dem Profil alle erforderlichen Lieferarten zugeordnet sind.
    15. Schließen Sie die Seite **Lieferarten**.
    16. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Einstellungen**, und wählen Sie **Auftragsursprünge** aus.
    17. Wählen Sie auf der Seite **Auftragsursprünge** die Option **Neu** aus.
    18. Wählen Sie im Feld **Unternehmen** aus, die juristische Person aus. Die Liste der Unternehmen wird auf die juristischen Personen beschränkt, die Sie zuvor hinzugefügt haben.
    19. Wählen Sie im Feld **Auftragsursprung** den Auftragsursprung aus, der diesem Profil zugeordnet werden soll. Ein Auftragsursprung kann nicht mehreren aktiven Profilen zugeordnet werden.
    20. Wiederholen Sie die obigen beiden Schritte, bis dem Profil alle erforderlichen Auftragsursprünge zugeordnet sind.
    21. Schließen Sie die Seite **Auftragsursprünge**.
    22. Legen Sie die Option **Profil aktivieren** auf **Ja** fest. Wenn in den Einstellungen ein Fehler vorhanden ist, erhalten Sie eine Warnmeldung.

## <a name="dom-processing"></a>DOM-Verarbeitung

DOM wird nur in einen Stapelverarbeitungsauftrag ausgeführt. Um der Stapelverarbeitungsauftrag für DOM-Ausführungen zu konfigurieren, führen Sie die folgenden Schritte aus.

1. **Einzelhandel \> Verteilte Auftragsverwaltung \> Stapelverarbeitung \> DOM-Verarbeitung für einen Auftrag einrichten**.
1. Wählen Sie im Inforegister **Parameter** im Feld **Erfüllungsprofil** ein Profil aus, für das DOM ausgeführt werden muss.
1. Wählen Sie im Inforegister **Im Hintergrund ausführen** im Feld **Stapelverarbeitungsgruppe** eine konfigurierte Stapelverarbeitungsgruppe aus.
1. Geben Sie im Feld **Aufgabenbeschreibung** einen Namen für den Stapelverarbeitungsauftrag ein.
1. Wählen Sie **Wiederholung** aus, und definieren Sie die Wiederholung des Stapelverarbeitungsauftrags.
1. Wählen Sie **OK**.

Zum Zeitpunkt des Verarbeitung berücksichtigt DOM die Reihenfolge und die Auftragspositionen, die im Folgenden beschrieben sind:

- Auftragspositionen, die die Kriterien für Auftragsursprünge, Lieferarten und juristische Person gemäß dem DOM-Profil erfüllen und die auch alle folgenden Kriterien erfüllen:

    - Sie werden von den Einzelhandelskanälen erstellt.
    - Sie wurden nie durch DOM vermittelt.
    - Sie wurden zuvor durch DOM vermittelt, sind aber als Ausnahmen markiert und liegen unter halb des maximalen Schwellenwertes für Versuche.
    - Die Lieferart lautet nicht Abholung oder elektronischen Lieferung.
    - Sie sind nicht zur Lieferung markiert.
    - Sie wurden nicht manuell ausgeschlossen.

- Aufträge sind nicht gesperrt

Nach der Anwendung der Regeln, der Bestandseinschränkungen und der Optimierung wählt DOM den Standort aus, der der Lieferadresse des Kunden Debitors am nächsten ist.

![Auftragskriterien](./media/ordercriteria.png "Auftragskriterien")

## <a name="results-of-dom-runs"></a>Ergebnisse von DOM-Ausführungen

Wenn das Erfüllungsprofil auf **Automatisch übernehmen** festgelegt ist, werden die Ergebnisse des Durchlaufs automatisch in die Auftragspositionen übernommen, und der Erfüllungsplan kann separat angezeigt werden. Ist das Erfüllungsprofil nicht auf **Automatisch übernehmen** festgelegt, können nur die Ergebnisse des Durchlaufs nur in der Erfüllungsplanansicht angezeigt werden. 

Um alle erzeugten Erfüllungspläne anzuzeigen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zurück zu **Einzelhandel \> Verteilte Auftragsverwaltung \> Verteilte Auftragsverwaltung**.
2. Wählen Sie Arbeitsbereich **Verteilte Auftragsverwaltung** die Kachel **Erfüllungspläne** aus.
3. Wählen Sie die ID des relevanten Auftragserfüllungsplans aus, um den Erfüllungsplan anzuzeigen.

    Der Abschnitt mit den Bestelldetails im Erfüllungsplan zeigt die Originalauftragspositionen an, die Teil des Durchlaufs waren. Neben den Standardfeldern für die Auftragspositionen enthält der Abschnitt mit den Bestelldetails auch die folgenden drei DOM-spezifischen Felder:

    - **Erfüllungstyp** – Dieses Feld gibt an, ob die Auftragsposition vollständig, teilweise oder gar nicht an einen Standort vermittelt wurde.
    - **Teilen** – Dieses Feld gibt an, ob die Auftragsposition auf verschiedene Standorte aufgeteilt und an diese vermittelt wurde.
    - **Anzahl Erfüllungsstandorte** – Dieses Feld gibt an, wie viele Erfüllungspositionen für eine Auftragsposition erstellt wurden (basierend auf der Anzahl der Standorte, an die die ursprüngliche Auftragsposition vermittelt wurde).

    Der Abschnitt mit den Auftragserfüllungsdetails zeigt die Zuteilung der Originalauftragspositionen zu den verschiedenen Standorten sowie die jeweiligen Mengen an.

## <a name="order-line-actions-and-statuses"></a>Auftragspositionsaktivitäten und Statusangaben

Im Folgenden werden die Einstellungen für die Auftragsposition beschrieben. Gehen Sie zu **Einzelhandel \> Kunden \> Alle Aufträge**, um die Auftragsposition zu öffnen.
- Ist der Option **Aus DOM-Verarbeitung ausschließen** auf der Registerkarte **Allgemein** der Auftragsposition auf **Ja** gesetzt, wird der Auftrag oder die Auftragsposition aus der DOM-Verarbeitung ausgeschlossen.
- Im Feld **DOM-Status** auf der Registerkarte **Allgemein** der Auftragsposition kann einer der folgenden Werte festgelegt werden:

    - **Kein** – Die Auftragsposition wurde nie vermittelt.
    - **Vollständig** – Die Auftragsposition wurde erfolgreich vermittelt und einem Standort zugewiesen.
    - **Ausnahme** – Die Auftragsposition wurde vermittelt, kann aber keinem Standort zugewiesen werden. Ausnahmen haben mehrerer Untertypen, die vom DOM-Arbeitsbereich aus angezeigt werden können:

        - **Keine Menge verfügbar** – Es ist kein verfügbarer Lagerbestand verfügbar, mit dem der Auftrag Standorten zugewiesen werden kann.
        - **Maximale Ablehnungen** – Die Auftragsposition hat den maximalen Schwellenwert für Ablehnungen erreicht.
        - **Datenänderungskonflikt** – Die Auftragsposition wurde seit der Vermittlung des Auftrags geändert. Daher kann der Erfüllungsplan nicht in den Auftrag übernommen werden.
        - **Auftragspositionsspezifische Ausnahme** – Es gibt mehrere Ausnahmen in der Auftragsposition.

- DOM kann während der Auftragserfassung im interaktiven Modus ausgeführt werden. Wenn Sie eine Auftragsposition eingeben, können Sie nach der Eingabe des Produkts und der Menge die Option **Position aktualisieren** und dann unter **DOM** die Option **Erfüllungsstandort vorschlagen** auswählen. Dann wird eine auf den DOM-Regeln basierende Liste der Standorte angezeigt, die die Menge in der Auftragsposition erfüllen können. Die Liste ist nach Entfernung sortiert. Wählen Sie einen Standort aus, um den entsprechenden Standort und das Lage in der Auftragsposition festzulegen. Damit diese Funktionen greifen, muss ein aktives Erfüllungsprofil vorhanden sein, dass mit dem Auftragsursprung und der Lieferart in der Auftragsposition übereinstimmt.
- Um die DOM-Ausführungsprotokolle für eine Auftragsposition anzuzeigen, wählen Sie **Auftragsposition** und dann unter **DOM** die Option **DOM-Protokolle anzeigen** aus. In den DOM-Protokolle werden alle Ereignisse und Protokolle angezeigt, die von der DOM-Ausführung generiert wurden. Anhand der Protokolle erkennen Sie einfach, warum der Auftragsposition ein bestimmter Standort zugewiesen wurde und welche Regeln und Einschränkungen zur Zuweisung gehören. Auf der Registerkarte **Verwalten** sind die DOM-Protokolle auch im Auftragskopf verfügbar.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Ausführen eines Bereinigungsauftrags für DOM-Erfüllungspläne

Während die DOM-Verarbeitung ausgeführt wird, werden Erfüllungspläne erstellt. Im Laufe der Zeit verfügt das System über verschiedene Erfüllungspläne. Um die Anzahl der Erfüllungspläne im System zu verwalten, können Sie einen Stapelverarbeitungsauftrag konfigurieren, der ältere Erfüllungspläne basierend auf dem Wert **Einbehaltungszeitraum in Tagen** löscht.

1. Gehen Sie zu **Einzelhandel \> Verteilte Auftragsverwaltung \> Stapelverarbeitung \> Einrichten des Löschenauftrags für DOM-Erfüllungsdaten**. 
1. Wählen Sie im Feld **Stapelverarbeitungsgruppe** eine konfigurierte Stapelverarbeitungsgruppe aus.
1. Wählen Sie **Wiederholung** aus, und definieren Sie die Wiederholung des Stapelverarbeitungsauftrags.
1. Wählen Sie **OK**.

## <a name="more-information"></a>Weitere Informationen

Nachfolgend sind einige Hinweise aufgeführt, die Sie bei der Verwendung der DOM-Funktion berücksichtigen sollten:

- Momentan berücksichtigt DOM nur Aufträge, die von den Einzelhandelskanälen erstellt werden. Aufträge werden als Einzelhandelsaufträge angegeben, wenn die Option **Einzelhandelsauftrag** auf **Ja** festgelegt ist.
- Microsoft hat DOM nicht mit den erweiterten Funktionen für die Lagerortverwaltung getestet. Kunden und Partner müssen mit Sorgfalt festlegen, ob DOM mit den erweiterten Funktionen und Prozessen für die Lagerortverwaltung kompatibel ist, die für sie relevant sind.
- DOM ist nur in der Cloudversion von Retail verfügbar. Es wird nicht für Vor-Ort-Bereitstellungen unterstützt.
