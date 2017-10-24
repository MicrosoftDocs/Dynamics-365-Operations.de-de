---
title: "Wählen Sie ein Produktkonfigurationsmodell aus."
description: "Die Notwendigkeit, Produkte zu konfigurieren, um bestimmte Anforderungen zu erfüllen, wird eher die Regel anstatt die Ausnahme, sowohl in B2B- als auch in den B2C-Beziehungen."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c0d3cd5a969dfa7e851abe434c5d8d9dafe8eb55
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="build-a-product-configuration-model"></a>Wählen Sie ein Produktkonfigurationsmodell aus.

[!include[banner](../includes/banner.md)]


Die Notwendigkeit, Produkte zu konfigurieren, um bestimmte Anforderungen zu erfüllen, wird eher die Regel anstatt die Ausnahme, sowohl in B2B- als auch in den B2C-Beziehungen.

Ein Hersteller, der Konfigurieren-zum Auftrag-Szenarien unterstützt, hat die Gelegenheit, auf Kundenbedürfnisse sorgfältiger zu achten. Darüber hinaus kann er, indem er Halbfertigwaren in Form von allgemeinen Komponenten anstelle von Fertigprodukten lagert, das Kapital reduzieren, das am Bestand gebunden ist.  

Ein erfolgreicher Umstieg von der Fertigung-zu-Bestand-Einstellung zur Konfigurieren-zum Auftrag-Einstellung erfordert eine sorgfältige Analyse der Produktstrukturen, Kennung der Produktfamilien und Komponentisierung. Um die Anzahl von Teilen zu reduzieren und die Zahl von Waren im Prozess zu minimieren, ist es sehr wichtig dass Sie die Produktschnittstellen verstehen und dass Sie für Wiederverwendungsmöglichkeit entwerfen.  

Es gibt mehrere Produktkonfigurationsmodellierungsprinzipien, wie die regelbasierte, dimensionsbasierte und einschränkungsbasierte Modellstruktur. Untersuchungen zeigen, dass die einschränkungsbasierte Methode die Anzahl von Codezeilen in den Modellen um ungefähr 50 Prozent verringern kann, wenn mit anderen Modellierungsprinzipien verglichen wird. Daher kann diese Methode die Gesamtkosten (TCO) reduzieren. Wenn Sie von einem regelbasierten Modell, das auf X++-Code basiert, zu einem einschränkungsbasierten Modell übergehen, benötigen Sie keine Entwicklerlizenz mehr, um Produktmodelle zu verwalten.

## <a name="product-configuration"></a>Produktkonfiguration
Die Industrialisierungsperiode hat zu großen Leistungen beim Erzeugen hochwertiger und funktionsreicher Produkte zu erschwinglichen Preise geführt. Die Kostendegression hat es für die meisten Personen in der industrialisierten Welt möglich gemacht, Autos, Fernseher, Haushaltswaren und andere Waren zu kaufen, die die meisten als einen erforderlichen Teil unseres Alltagslebens erachten.  

Da viele Produkte zu einer Ware geworden sind, ist eine Anforderung, sie zu unterscheiden, aufgetreten. Die primäre Antwort von Herstellern zu dieser Herausforderung ist, Varianten jedes Produkts zu erstellen, damit Kunden mehr Alternativen haben. Diese Strategie hat zu erhöhten Planungsherausforderungen und auch zu einer Erhöhung der Bestandskosten und der nicht verkauften Produkte, die veralten, geführt.  

Durch die Annahme einer Konfigurieren-zum Auftrag-Philosophie haben Hersteller die Gelegenheit, Kundennachfragen für einmalige Produkte zu erfüllen und dabei veraltete Lagerartikel zu reduzieren oder zu eliminieren. Wenn eine Fertigung-zu-Bestand-Philosophie zu einer Konfigurieren-zum Auftrag-Philosophie übergeht, ist eine primäre Herausforderung, dass erforderliche kurze Lieferzeiten mit niedrigen Lagerbestände ausgeglichen werden müssen.  

Der Schlüssel zum Erfolg hier ist, die Produktpalette sorgfältig zu analysieren, und nach Mustern in Produktfunktionen und -prozessen zu suchen. Die Zielsetzung besteht darin, generische Komponenten zu erkennen, die von denselben Ausrüstung erstellt und in allen Varianten verwendet werden können.  

Der neue Produktkonfigurationsfunktionsumfang umfasst eine Benutzeroberfläche (UI), die einen visuellen Überblick der Produktkonfigurationsmodellstruktur enthält, und auch eine deklarative Einschränkungssyntax, die nicht kompiliert werden muss. Daher können Unternehmen, die eine Konfigurationsmethode unterstützen möchten, leichter anfangen. Wie die folgenden Abschnitte erklären, benötigt ein Produktdesigner nicht mehr den Support eines Entwicklers, um ein Produktkonfigurationsmodell zu erstellen, zu testen und für die Verkaufsorganisation freizugeben.

## <a name="building-a-product-configuration-model"></a>Ein Produktkonfigurationsmodell erstellen
Es gibt mehrere Arten, die ein Benutzer wählen kann, um ein Produktkonfigurationsmodell zu erstellen. Eine Option ist, einem sequenziellen Ablauf zu folgen, indem zunächst alle Referenzdaten, wie Produktmaster, eindeutig identifizierbare Produkte und betriebliche Ressourcen erstellt werden, und sie dann als Komponenten, Stücklisten (BOM)- Positionen, Arbeitsplan-Arbeitsgänge und andere Elemente des Produktkonfigurationsmodells eingeschlossen werden. Alternativ können Sie einen schrittweiseren Ansatz auswählen, indem Sie zuerst das Modell erstellen und dann ggf. später Referenzdaten hinzufügen.

### <a name="components"></a>Komponenten

Ein Produktkonfigurationsmodell besteht aus einer oder mehreren Komponenten, die durch Unterkomponentenbeziehungen verbunden sind. Komponenten werden einmal definiert und können dann viele Male in mindestens einem Produktkonfigurationsmodell verwendet werden. Die Komponenten sind die wichtigsten Bausteine eines Produktkonfigurationsmodells, und fast alle Informationen zum Modell werden zu diesen zugeordnet.

### <a name="attributes"></a>Attribute

Jede Komponente enthält eines oder mehrere Attribute, die dessen Eigenschaften identifizieren. Die Attribute sind das, was Benutzer beim Konfigurationsprozess auswählen. Attribute steuern Interkomponenten- und Intrakomponentenbeziehungen durch die Einbeziehung in den Einschränkungen oder in Berechnungen. Durch Bedingungen, die für die Stücklistenpositionen angewendet werden, können die Attribute verwendet werden, um zu ermitteln, aus welchen physischen Teilen das konfigurierte Produkt bestehen wird. Außerdem kann ein Attribut die Eigenschaft einer Stücklistenposition durch einen Zuordnungsmechanismus steuern. Ähnliche Funktionen sind für Arbeitsplan-Arbeitsgänge hinsichtlich Einbeziehung und Eigenschafteneinstellungen vorhanden.

### <a name="expression-constraints"></a>Ausdruckseinschränkungen

Die Verwendung eines einschränkungsbasierten Produktkonfigurationsmodell bedeutet, dass einige Einschränkungen bestehen, wenn der Benutzer Werte für die verschiedenen Attribute auswählt. Solche Einschränkungen können als Ausdruckseinschränkungen implementiert werden, indem die OML (Optimization Modeling Language) verwendet wird. Alternativ kann eine Einschränkung in Form einer Tabelleneinschränkung implementiert werden.

### <a name="table-constraints"></a>Tabelleneinschränkungen

Tabelleneinschränkungen können als benutzerdefinierte oder als systemdefinierte Einschränkung vorliegen.  

Eine benutzerdefinierte Tabelleneinschränkung wird vom Benutzer erstellt. Der Benutzer wählt eine Kombination von Attributtypen aus, um die Spalten der Tabelle darzustellen und gibt dann Werte aus den Domänen der ausgewählten Attributtypen ein, um die Zeilen in der Tabelleneinschränkung zu bilden.  

Eine systemdefinierte Tabelleneinschränkung wird definiert, indem ausgewählt wird, welche Microsoft Dynamics 365 for Finance and Operations-Tabelle als Referenz verwendet wird, und indem dann Felder aus dieser Tabelle festgelegt werden, um die Spalten in der Einschränkung zu bilden. Die Zeilen der Tabelleneinschränkung sind die Zeilen der Finance and Operations-Tabelle, die bei der Konfiguration vorhanden sind.  

Eine Tabelleneinschränkung wird in einem Produktkonfigurationsmodell einbezogen, indem die Tabelleneinschränkungsdefinition verwiesen und die betreffenden Attribute im Modell zu den Spalten in der Tabelleneinschränkung zuordnet werden.

### <a name="calculations"></a>Berechnungen

Berechnungen stellen einen Mechanismus für die Ausführung von arithmetischen Operationen in einem Konfigurationsmodell dar. So kann eine Berechnung die Dauer eines bestimmten Rohmaterial-Artikels oder die Bearbeitungszeit für einen Polierarbeitsgang bestimmen. Berechnungen sind obligatorisch und legen den Wert für ein Zielattribut fest, nachdem alle Attributwerte, die im Berechnungsausdruck enthalten sind, verfügbar sind.

### <a name="subcomponents"></a>Unterkomponenten

Unterkomponenten spiegeln die Knoten in der Produktkonfigurationsmodellstruktur wider. Für jede Unterkomponentenbeziehung muss eine Referenz für einen Produktmaster angegeben werden, bei dem die Technologie für Variantenkonfiguration auf die einschränkungsbasierte Konfiguration festgelegt ist.

### <a name="user-requirements"></a>Benutzeranforderungen

Eine Benutzeranforderung hat alle Elemente einer Unterkomponente. Der einzige Unterschied ist, dass eine Benutzeranforderung an keinen Produktmaster gebunden wird. Die praktische Auswirkungen dieser Differenz ist, dass alle Stücklistenpositionen oder Arbeitsplan-Arbeitsgänge, die im Rahmen einer Benutzeranforderung definiert werden, in die übergeordnete Teilstücklistenstruktur oder -arbeitsplan reduziert werden. Dieses Verhalten ähnelt dem Verhalten einer Phantomstückliste.

### <a name="bom-lines"></a>Stücklistenpositionen

Stücklistenpositionen werden eingeschlossen, um die Fertigungsstückliste für jede Komponente zu identifizieren. Eine Stücklistenposition muss einen Artikel verweisen, und alle Artikel-Eigenschaften können auf einen festen Wert festgelegt oder einem Attribut zugeordnet werden.

### <a name="route-operations"></a>Arbeitsplanarbeitsgänge

Arbeitsplan-Arbeitsgänge werden eingeschlossen, um den Fertigungsarbeitsplan zu identifizieren. Ein Arbeitsplan-Arbeitsgang muss einen definierten Arbeitsgang verweisen, und alle Arbeitsgangseigenschaften können auf einen festen Wert festgelegt werden. Alle Eigenschaften außer Ressourcenanforderungen können einem Attribut anstelle eines Werts zugeordnet werden.

## <a name="validating-and-testing-a-product-configuration-model"></a>Ein Produktkonfigurationsmodell validieren und testen
Die Prüfung eines Produktkonfigurationsmodells kann auf mehreren Ebenen im Modell auftreten und daher unterschiedliche Bereiche enthalten. Die niedrigste Ebene ist für eine einzelne Ausdruckseinschränkung. In diesem Fall wird die Prüfung in der Regel vom Produktdesigner ausgeführt, um zu überprüfen, ob die Syntax eines Ausdrucks korrekt ist.  

Entsprechend können eine Bedingung für eine Stücklistenposition oder ein Arbeitsplan-Arbeitsgang isoliert geprüft werden.  

Eine Prüfung kann für eine benutzerdefinierte Tabelleneinschränkungsdefinition auch ausgeführt werden. In diesem Fall kann der Benutzer überprüfen, ob die Werte, die für jedes Feld eingegeben werden, innerhalb der Domäne der entsprechenden Attributtypen sind.  

Schließlich kann die Prüfung für ein vollständiges Produktkonfigurationsmodell durchgeführt werden, um zu überprüfen, ob die vollständige Syntax korrekt ist und alle Benennungs- und Modellierungskonventionen berücksichtigt wurden.

### <a name="testing"></a>Testen

Ein Modell testen ist gleich, wie wenn man eine tatsächliche Konfigurationssitzung startet. Der Benutzer kann durch die Konfigurationsseiten durchgehen und überprüfen, ob die vorbildliche Struktur den Konfigurationsvorgang unterstützt. Der Benutzer kann überprüfen, ob die Attributwerte korrekt sind und die Attributbeschreibungen den Benutzer führen, um die richtigen Werte auszuwählen. Schließlich, nachdem eine Testsitzung abgeschlossen wurde, versucht das System, die Stückliste und den Arbeitsplan zu erstellen, der den ausgewählten Attributwerten entspricht und eine Fehlermeldung anzeigt, wenn ein Fehler auftritt.

### <a name="the-configuration-page"></a>Die Konfigurationsseite

Um zwischen Komponenten zu navigieren, klicken Sie auf **Weiter** oder auf eine Komponente in der Produktkonfigurationsmodellstruktur, um den Fokus Sie dafür festzulegen.

## <a name="finalizing-a-model-for-configuration"></a>Fertigstellen eines Modells für die Konfiguration
Wenn ein Produktkonfigurationsmodell bereit ist, in Konfigurieren-zum Auftrag-Szenarien verwendet zu werden, muss eine Version erstellt werden. Jedoch gibt es mehrere Optionen, die die Modellierungserfahrung verbessern können.

### <a name="user-interface"></a>Benutzeroberfläche

Die Konfigurationsbenutzeroberfläche kann geändert werden, indem Attributgruppen in mindestens einer Unterkomponente eingeführt werden. Eine solche Gruppierung kann die Beziehungen zwischen bestimmten Attributen markieren und den Konfigurationsbenutzer unterstützen, den Bereich des Produkts zu kennzeichnen, der derzeit Fokus ist.

### <a name="templates"></a>Vorlagen

Eine oder mehrere Konfigurationsvorlagen können erstellt werden, um den Konfigurationsprozess zu beschleunigen. Alternativ können Vorlagen erstellt werden, um bestimmte Attributkombinationen zu fördern, z. B. wenn eine Verkaufskampagne auf eine bestimmte Reihe von Produktfunktionen fokussiert ist.

### <a name="translations"></a>Übersetzungen

Wenn das Produkt in verschiedenen Ländern/Regionen verkauft wird, können Übersetzungen für den gesamten Text erstellt werden, der in der Konfigurationsbenutzeroberfläche angezeigt wird. Dieser Text umfasst nicht nur Namens- und Textfelder, sondern auch Attributtextwerte.

### <a name="versions"></a>Versionen

Der letzte und der wichtigste Schritt im Abschlussprozess ist, eine Version für das Produktkonfigurationsmodell zu erstellen. Die Version stellt die Beziehung zwischen dem Produktmaster, der für die Konfiguration in einem Auftrag oder einer Angebotsposition ausgewählt werden kann, und dem Produktkonfigurationsmodell dar. Eine Version muss genehmigt und aktiviert werden, bevor sie in einer Konfigurationssitzung verwendet werden kann.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Erweitern eines Produktkonfigurationsmodells durch das API
Eine dedizierte Anwendungsprogrammierschnittstelle (API) wurde implementiert, sodass Partner und andere, die eine Entwicklerlizenz haben, den Funktionsumfang eines Produktkonfigurationsmodells erweitern können. Das Hauptziel war, einen Mechanismus einzurichten, mit dem Partner und Debitoren, die den vorhandenen Produktgenerator verwenden, den Code, der in den Produktgeneratormodellen eingebettet ist, in die API migrieren können. Auf diese Weise können sie ihre Modelle vom Produktgenerator in eine Produktkonfiguration migrieren. Allerdings können neue Partner und Kunden auch von der Verwendung der API zum Erweitern neuer Produktkonfigurationsmodelle profitieren.

### <a name="pcadaptor-class"></a>PCAdaptor-Klasse

Das API ist so implementiert, dass sie einen Satz **PCAdaptor**-Klassen verwendet, die die Datenstruktur der Produktkonfigurationsmodelle verfügbar machen. Eine Instanz der **PCAdaptor Klasse**  muss für jedes Modell erstellt werden, das als Kreditor erfasst wird. Nachdem eine Konfigurationssitzung abgeschlossen ist, sucht das System nach einer Instanz dieser Klasse und führt diese aus, wenn es sie gefunden hat.  

Das folgende Flussdiagramm veranschaulicht den Prozess.  

[![Flussidagramm](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Produktkonfiguration für das API-Flussdiagramm

## <a name="product-configuration"></a>Produktkonfiguration
Die Produktkonfiguration kann von den folgenden Stellen ausgeführt werden:

-   Auftragsposition
-   Verkaufsangebotsposition
-   Bestellposition
-   Produktionsauftragsposition
-   Artikelbedarfsposition (Projekt)

Der Zweck der Konfiguration ist, eine unterschiedliche Variante des Produkts zu erstellen, das der Bedingung des Debitors entspricht. Eine eindeutige Variantenkennung wird für jede neue Konfiguration erstellt. Diese Kennung aktiviert Nachverfolgung durch das Lager.

### <a name="multiple-sites-and-intercompany"></a>Mehrere Standorte und Intercompany

Wenn eine Variante an einem Standort erfolgt oder auch an einem Unternehmen, das von der Site oder dem Unternehmen der Produktion abweicht, werden die Stückliste und der Arbeitsplan für die Lieferantensite im Lieferunternehmen erstellt und dort eingelagert. Die Produktvariante wird in allen Unternehmen freigegeben, die an der Lieferkette teilnehmen.




