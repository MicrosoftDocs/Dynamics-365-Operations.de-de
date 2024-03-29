---
title: Finanzanalyse
description: Finanzanalyse nutzt Microsoft Power BI, um Finanzleistungskennzahlen (KPIs), Diagramme und Finanzaufstellungen zusammenzuführen.
author: kweekley
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 21d7d045c812c54d6776394ad9a0b025b55df8e1
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109111"
---
# <a name="financial-analysis"></a>Finanzanalyse

[!include [banner](../includes/banner.md)]

**Finanzanalyse** nutzt Microsoft Power BI, um Finanzleistungskennzahlen (KPIs), Diagramme und Finanzaufstellungen zusammenzuführen. Power BI wird in der Anwendung eingebettet. Der Fokus von **Finanzanalyse** liegt auf der analytischen Berichterstellung. Personen in einer gesamten Organisation können anzeigen, erforschen, verstehen und handeln. 

**Finanzanalyse** kombiniert Daten aus dem Hauptbuch und von untergeordneten Sachkonten, um ein vollständigeres Bild der finanziellen Lage einer Organisation zu vermitteln.

> [!NOTE]
> Dieses Dokument verwendet die folgende Power BI-Terminologie:
> 
> - **Bericht** – Eine einzelne .pbix-Datei, in der die visuellen Elemente auf allen Registerkarten gespeichert werden.
> - **Seite** – Eine Registerkarte in einer einzelnen .pbix-Datei. Jeder Seite kann ein oder mehrere visuelle Elemente enthalten.
> - **Visual** – Eine einzelne Datenquelle, wie eine Karte, KPI, Diagramm, Graph, Matrix oder Finanzaufstellung. Eine Seite, die eine Finanzaufstellung als ein visuelles Element hat, kann keine anderen visuellen Elemente haben wegen der Größe der Daten, über die berichtet wird.

Der **Arbeitsbereich für die Finanzanalyse** konzentriert sich darauf, dass Sie die Daten in bestehenden Berichten anzeigen und filtern können. Sie können dem Arbeitsbereich **Finanzanalyse** neue Visualisierungen hinzufügen. Der Arbeitsbereich **Finanzanalyse** ist sowohl für die aktuelle Firma als auch für alle Firmen verfügbar, um Daten für alle juristischen Entitäten anzuzeigen, unabhängig von den juristischen Entitäten, auf die die Rolle Zugriff hat.

- [Hinzufügen oder Bearbeiten von Power BI-Visualisierungen auf Ihrem Dashboard](/powerapps/user/add-powerbi-dashboards)

## <a name="dynamics-365-finance-setup"></a>Einrichtung von Dynamics 365 Finance
**Hauptbuch**

Der Hauptkontotyp und die Hauptkontokategorien werden verwendet, um entsprechende Standardhauptkonten in der Finanzaufstellung **Bilanz** und den verschiedenen Finanzaufstellungen **Gewinn- & Verlustrechnung** in **Finanzanalyse** einzugeben.

Auf der Seite **Hauptkonten** müssen Sie Ihr Hauptkonto festlegen, sodass einer der folgenden Typen ihm zugewiesen wird:

- Umsatz
- Expense
- Anlagen
- Passivposten
- Eigenkapital

Weisen Sie Ihren Hauptkonten keinen anderen Hauptkontotyp zu, wie **Bilanz** oder **Gewinn und Verlust**. Die Berichterstellung kann nicht den Typ des Hauptkontos bestimmen, wenn andere Hauptkontotypen zugewiesen sind, weil sie nicht ausreichend differenziert sind. Der Typ des Hauptkontos muss bestimmt werden, damit Passivposten und Umsatzerlös als positive Beträge in Finanzberichten angezeigt werden.

Um in Finanzaufstellungen angezeigt zu werden und in verschiedene andere visuelle Elemente einbezogen zu werden, wie beispielsweise KPIs, muss jedem Hauptkonto eine Hauptkontokategorie zugewiesen werden. Die Hauptkontokategorien sind verbessert worden, sodass sie einen Anzeigereihenfolge enthalten. Die Anzeigereihenfolge wird speziell für Finanzaufstellungen in **Finanzanalyse** verwendet. Nachdem Sie eine neue Hauptkontokategorie bearbeiten oder hinzufügen, können Sie den Wert **Anzeigereihenfolge** ändern, um die Reihenfolge zu definieren, in der die Hauptkontokategorien in einer Finanzaufstellung angezeigt werden sollen. Wenn Sie die Anzeigereihenfolge für viele Hauptkontokategorien ändern müssen, können Sie die Funktion „In Excel öffnen” verwenden, um die Änderungen schnell zurück in der Anwendung zu bearbeiten und zu veröffentlichen.

## <a name="entity-store"></a>Entitätsspeicher
Die Daten für **Finanzanalyse** werden aus dem Entitätsspeicher entnommen (**Systemverwaltung** \> **Einrichtung** \> **Entitätsspeicher**). Wenn Sie den Arbeitsbereich **CFO-Überblick** oder **Finanzanalyse** öffnen und die folgende Warnmeldung in den visuellen Elementen angezeigt wird, müssen Sie die Entitäten aktualisieren.

![Warnung.](./media/Cantdisplay.png)

Sie müssen die folgenden Entitäten aktualisieren, um sich Daten im Arbeitsbereich **Finanzanalyse** anzeigen zu lassen:

- Finanzberichterstattungs-Buchungsdaten – Version 3 
- Kredit und Inkasso V2
- LedgerCovLiquidityMeasurement
- Einkaufscube
- Verkaufscube

Sie können definieren, dass eine sich wiederholende Charge regelmäßig die Daten in den Entitäten aktualisiert. Da jede Entität während einer Aktualisierung vollständig neu erstellt wird, wählen Sie die Zeit und die Häufigkeit von Entitätsaktualisierungen mit Bedacht aus. Die primäre Entität, die für die Finanzaufstellungen verwendet wird, ist die Entität FinancialReportingTransactionData. Daher entscheiden Sie sich möglicherweise, die Entität häufiger zu aktualisieren.

## <a name="security"></a>Sicherheit
Aktuell können die Daten in eingebetteten Power BI-Berichten nicht auf juristische Personen beschränkt werden, auf die der Benutzer Zugriff hat. Daher werden die eingebetteten Power BI-Berichte durch Berechtigungen in den Sicherheitseinstellungen gesteuert. Die Berechtigungen, die definiert werden, lassen Zugriff auf Daten entweder für alle juristischen Personen oder nur das aktive Unternehmen zu. In der folgenden Tabelle werden die Berechtigungen angezeigt, die vorhanden sind und die Rollen, denen sie zugewiesen sind. Die Berechtigungen können von verschiedenen Rollen entfernt oder ihnen zugewiesen werden, basierend auf den Anforderungen Ihrer Organisation.

| Abgabe                                    | Rollen | Beschreibung |
|-----------------------------------------|-------|------------|
| Finanzanalyse des derzeitigen Unternehmens anzeigen | <ul><li>Sachbearbeiter Buchhaltung</li><li>Leiter Buchhaltung</li><li>Supervisor Buchhaltung</li><li>Wirtschaftsprüfer</li><li>Budget-Manager</li><li>Leitender Geschäftsführer</li><li>Leiter Finanzabteilung</li><li>Financial Controller</li></ul> | Diese Berechtigungen bieten Zugriff auf Finanzanalyse. Standardmäßig wird das aktive Unternehmen als Filter verwendet. Sie können nicht andere juristische Personen hinzufügen. |
| Finanzanalyse aller Unternehmen anzeigen   | In Microsoft Dynamics 365 Finance, Enterprise Edition 7.3, ist diese Aufgabe keiner Rolle zugewiesen. In der nächsten Version werden diese Berechtigungen der Rolle „Leiter Finanzabteilung” zugewiesen werden. | Diese Berechtigungen bieten Zugriff auf das Menüelement für den Arbeitsbereich CFO-Überblick. Standardmäßig wird das aktive Unternehmen als Filter verwendet. Sie können jedoch alle juristischen Personen hinzufügen, unabhängig davon, ob der Benutzer Zugriff auf die anderen juristischen Personen hat. |


## <a name="financial-reporting-vs-financial-analysis"></a>Finanzberichterstellung vs. Finanzanalyse
Obwohl **Finanzanalyse** Finanzaufstellungen enthält, ist es kein Ersatz für die Finanzberichterstellung in der Anwendung. Die Standardfinanzaufstellungen in **Finanzanalyse** sind im Umfang begrenzt und umfassen nicht alle Typen von Finanzaufstellungen. Finanzberichterstattung ist immer noch das primäre Tool zum Entwerfen, Erstellen und Generieren von gesetzlich vorgeschriebenen Finanzaufstellungen.

Das folgende Vergleichsdiagramm hilft, die zwei Optionen zu unterscheiden:


| Funktion                                                   | Financial Reporting                                               | Finanzanalyse |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Standardberichte bearbeiten**                                 | Ja                                                               | Nein |
| **Neue Berichte erstellen**                                   | Ja                                                               | Nein |
| **Berichte drucken**                                        | Ja                                                               | Nein |
| **Nach Excel exportieren**                                      | Ja                                                               | Begrenzte Exportrohdaten in Excel, kein formatierter Bericht |
| **Berichterstellungshierarchie unterstützen/Organisationshierarchie**   | Ja                                                               | Nein |
| **Bericht zu Daten von untergeordneten Sachkonten**                             | Ja, beschränkt auf nur einen Kreditor, Debitor                              | Ja, Kreditor, Debitor, Kreditoren-/Debitorengruppen, Kreditoren-/Debitorenadressen, usw. |
| **Berichtswährung**                                   | Ja, Buchhaltungswährung und in Berichtswährung übersetzen       | Nein, nur Buchhaltungswährung |
| **Sicherheit**                                             | Ja, erfüllt Financ-Berichterstellungsstruktur-Sicherheit | Eingeschränkte Ansicht Berichte für alle Unternehmen (unabhängig von der Finanzen und Betrieb Sicherheit) oder nur für aktive Firmen |
| **Unterschiedlichen Kontenplan und Geschäftsjahre unterstützen** | Ja                                                               | Nein |
| **Bericht zu externen Daten**                              | Nein                                                                | Nein |
| **Konsolidierungen unterstützen**                               | Ja                                                               | Begrenzter Möglichkeitenbericht zu mehreren Unternehmen, aber nur Verwendung der Buchhaltungswährung |

Folgende Finanzaufstellungen sind verfügbar:

- Zwischenbilanz
- Bilanz
- Gewinn- und Verlustrechnung nach Region
- Gewinn- und Verlustrechnung Istwert vs. Budget
- Gewinn- und Verlustrechnung mit Abweichungen
- Gewinn- und Verlustrechnung mit zwölfmonatigem Trend
- Dreijähriger Trend der Ausgaben
- Ausgaben nach Lieferant
- Umsatz nach Debitoren

## <a name="edit-visuals"></a>Bearbeiten visueller Elemente
In den vorherigen Versionen von **Finanzanalyse** konnten keine visuellen Elemente bearbeitet werden. In künftigen Versionen können Benutzer, die über die entsprechende Sicherheit verfügen, neue visuelle Elemente erstellen, vorhandene visuelle Elemente kopieren und visuelle Elemente bearbeiten. Obwohl die .pbix-Dateien, die die Berichte enthalten, als Ressourcen verfügbar sind, wird davon abgeraten, dass Sie die Standardberichte bearbeiten. Zusätzliche Änderungen werden am Datenmodell, Standardberichten und benutzerdefinierten visuellen Elementen zur Finanzaufstellung, die zum Erstellen der Finanzaufstellungen verwendet werden, vorgenommen. Um sich daher neue Funktionen und Änderungen am Datenmodell in der nächsten Version zunutze zu machen, müssen Sie sämtliche Änderungen erneut vornehmen, die Sie in Standardberichten mithilfe von Microsoft Power BI Desktop vorgenommen haben.

## <a name="filtering"></a>Filtern
Benutzer können den Bericht filtern, indem sie den Bereich **Filter** links verwenden. Dieser Bereich ist der gleiche Bereich, der über Power BI Desktop verfügbar ist. Es gibt verschiedene Ebenen der Filterung, von denen einige möglicherweise nicht verfügbar sind, abhängig davon, was Sie auf einer Seite (Registerkarte) ausgewählt haben oder ob Sie die Drillthroughfunktionen verwenden:

- **Filter auf Berichtsebene** – Diese Filter werden auf alle visuellen Elemente auf allen Seiten (Registerkarten) angewendet.
- **Filter auf Seitenebene** – Diese Filter werden auf alle visuellen Elemente auf der aktiven Registerkarte angewendet. Diese Filter werden zusätzlich zu den Filtern auf Berichtsebene angewendet.
- **Filter auf der visuellen Ebene** – Diese Filter werden nur auf das ausgewählte visuelle Element angewendet. Diese Filter werden zusätzlich zu den Filtern auf Seitenebene angewendet.
- **Drillthroughfilter** – Durch diesen Filter wird aus einem visuellen „Quell”-Element gefiltert, das auf das aktuelle visuelle Element angewendet wird, wenn Sie ein Drillthrough vom visuellen Quellelement bis zum aktuellen visuellen Element durchführen.

![Filteroptionen.](./media/filter.png)

Um einen bestimmte Filterwert zu entfernen, wählen Sie das daneben angezeigte Radierersymbol aus. Entfernen Sie keinen Filter, indem Sie das X auswählen. Wenn Sie das X auswählen, wird das Feld, in dem Sie derzeit Filtern, als Filteroption entfernt. Wenn Sie aus Versehen ein Feld aus einem Filter entfernen, schließen Sie den Arbeitsbereich und öffnen Sie ihn dann erneut. Die Standardfiltereinstellungen werden erneut angewendet.

Standardmäßig wenn Sie erstmals Arbeitsbereiche öffnen, wird die aktive juristische Person als der Filter auf Berichtsebene verwendet. Je nach ihrer Sicherheit können Benutzer in der Lage sein, andere juristische Personen hinzufügen oder die standardmäßige juristische Person ändern, zu die im Filter ausgewählt ist.

Der Filter **Steuerkalender** ist erforderlich, damit der korrekte Kalender für das visuelle Element verwendet wird. Standardmäßig wird der Filter auf Berichtsebene auf den Steuerkalender der aktiven juristischen Person festgelegt. Wenn Sie den Filter auf einen Steuerkalender ändern, der ein anderes Start- oder Enddatum aufweist, werden die Anfangssalden nicht einbezogen. Daher wird Ihre Finanzaufstellung **Bilanz** nicht die korrekten Salden anzeigen. Wenn Sie einen zusätzlichen Steuerkalender im Filter auswählen, haben Sie einen zusätzlichen Satz Spalten. Jeder zusätzliche Satz von Spalten zeigt die Beträge für einen anderen Steuerkalender an.

Der Filter **Buchungsebene** ist auch erforderlich. Standardmäßig wird der Filter auf „Aktuell” festgelegt. Sie können zusätzliche Buchungsebenen im Filter auswählen, um die aggregierten Beträge anzuzeigen.

Filter sind auch für die Felder **Datum** und **Geschäftsjahr** verfügbar. In der Regel werden diese Filter auf der Seitenebene angewendet. Standardmäßig verwendet der Filter **Datum** ein relationales Datum, das Sie ändern können. Sie können auch den relationalen Datumsfilter entfernen und den Filter **Geschäftsjahr** stattdessen verwenden.

## <a name="currency"></a>Währung

Alle visuellen Elemente, die aus Hauptbuchdaten berichten, zeigen Beträge in der Buchhaltungswährung an. Wenn Sie daher auf Basis der juristischen Person filtern, müssen Sie Acht geben, dass Sie nur juristische Personen einbeziehen, die dieselbe Buchhaltungswährung haben. Andernfalls aggregieren Sie Daten in unterschiedlichen Währungen.

Alle visuellen Elemente, die zu Daten aus untergeordneten Sachkonten berichten, wie beispielsweise **Cashflowplanung** und **Top 10** visuelle Elemente, zeigen Beträge in der Systemwährung an. Die Systemwährung und der Systemwechselkurs-Typ werden auf der Seite **Systemparameter** definiert.

Das visuelle Element **Saldo nach Bankkonto** verwendet Beträge in der Währung der Bankkonten.

## <a name="dimensions"></a>Dimensionen

Die Standardfinanzaufstellungen enthalten keine Finanzdimensionen, aber sind nur auf das Hauptkonto fokussiert. Unterstützung für Finanzdimensionen wird in künftigen Versionen verfügbar sein, wenn die Berichte bearbeitbar werden. Organisationen sind dann in der Lage, nach Finanzdimensionswerten zu filtern.

Einige Finanzaufstellungen enthalten Dimensionen, die auf Transaktionen untergeordneter Sachkonten beruhen. Das Ziel der neuen Finanzaufstellungen ist es, das Filtern nach Dimensionen zuzulassen, die nicht als Finanzdimensionen eingerichtet sind. Der standardmäßige Bericht „Ausgaben nach Lieferant” kann beispielsweise über das Hauptkonto hinaus nach unten erweitert werden, sodass Sie die Salden aufgeteilt nach Lieferant sehen können. Der Lieferant ist nicht als Finanzdimension eingerichtet. Stattdessen kehrt das System zur ursprünglichen Transaktion des untergeordneten Sachkontos zurück, um den Lieferanten zu finden.

Folgende Dimensionen werden in den Standardberichten verwendet. Keine dieser Dimensionen sind Finanzdimensionen.

- Lieferant
- Kreditorengruppe
- Kunde
- Debitorengruppe
- Land/Region
- Bundesland
- Stadt

> [!IMPORTANT] 
> Wenn Sie Transaktionen für mehrere Lieferanten oder Debitoren in einem einzelnen Beleg zusammenfassen, indem Sie die Finanzerfassungen verwenden, werden die Daten nicht korrekt sein. Der Berichterstellungsprozess kann nicht ermitteln, welcher Kreditor oder Debitor einem spezifischen Sachkonto in einem Journaleintrag zugeordnet ist, da diese Informationen nirgends verwaltet werden. Daher wird davon abgeraten, dass Sie mehrere Lieferanten, Kunden, Anlagen oder Projekte in einem einzelnen Beleg eingeben.

## <a name="drill-on-data"></a>Drillvorgang für Daten

Verschiedene Ebenen von Drillvorgängen sind über Power BI verfügbar. Jede Ebene hat einen anderen Namen und andere Funktionen. Sie können auch Drillvorgänge für Zeilen und Spalten vornehmen. In diesem Abschnitt werden die verschiedenen Optionen behandelt, indem die Finanzaufstellung **Zwischenbilanz** als Beispiel verwendet wird und gezeigt wird, wie Sie Drillvorgänge für Zeilen durchführen können. Die gleiche Funktionalität ist für Spalten vorhanden. Sie müssen einfach die Einstellung **Drillvorgang für** ändern.

In der folgenden Abbildung ist die Aufstellung **Zwischenbilanz** auf die oberste Ebene der Zeilenhierarchie reduziert, nämlich dem Hauptkontotyp.

![Aufstellung „Zwischenbilanz“.](./media/trial-balance.png)

Um die nächste Ebene der Hierarchie anzuzeigen, nämlich die Hauptkontokategorien, können Sie das Feld **Drillvorgang für** auf **Zeilen** festlegen und dann die Schaltfläche **Erweitern** auswählen (die dritte Schaltfläche nach dem Feld „Drillvorgang für”). Jetzt sehen Sie alle Hauptkontokategorien erweitert. Aktuell können Sie mit Power BI nicht ausschließlich eine Zeile oder Spalte erweitern, aber immer noch alle anderen Zeilen oder Spalten sehen.

![Drilldown der Zwischenbilanz für Reihen ausführen.](./media/trial-balance2.png)

Um die Hauptkonten für alle Zeilen zu erweitern, können Sie erneut die Schaltfläche **Erweitern** verwenden. Um allerdings einen Drilldown zu den Hauptkonten für nur eine Zeile durchzuführen, wählen Sie zuerst die Schaltfläche **Detailinformationen anzeigen** aus (der einzelne nach unten gerichtete Pfeil auf der rechten Seite des Fensters), und wählen Sie dann die Zeile aus, zu der der Drilldown ausgeführt werden soll. Die folgende Abbildung zeigt die Ergebnisse, wenn die Zeile **Verkäufe** ausgewählt ist, nachdem die Schaltfläche **Detailinformationen anzeigen** ausgewählt ist.

![Schaltfläche zum Erweitern der Zwischenbilanz.](./media/trial-balance3.png)

Nachdem Sie ein Drilldown auf eine einzelne Zeile ausführen, werden mehrere Klicks benötigt, um zur vollständigen Zwischenbilanz zurückzukehren. Die Schaltfläche **Drillup** (die erste Schaltfläche nach dem Feld **Drillvorgang für**) führt nur einen Drillup im Kontext der Kategorie **Verkäufe** durch, wie in der folgenden Abbildung gezeigt.

![Schaltfläche zum Drillup für Zwischenbilanz.](./media/trial-balance4.png)

Sie können weiterhin die Schaltfläche **Drillup** verwenden, um zur obersten Zusammenfassungsebene für die Zeilen zurückzukehren.

Power BI hat auch eine Schaltfläche, mit der Sie zur nächsten Ebene in der Hierarchie wechseln können (die zweite Schaltfläche nach dem Feld **Drillvorgang für**). Die Auswirkung dieser Schaltfläche unterscheidet sich von der Auswirkung der Schaltfläche **Erweitern** (die dritte Schaltfläche nach dem Feld **Drillvorgang für**), die verwendet wird, um die Hierarchie zu erweitern. Wenn Sie die Hierarchie erweitern wird die Hierarchie im Bericht verwaltet. Wie beispielsweise zuvor gezeigt wurde, wenn Sie den Hauptkontotyp erweitern, sehen Sie immer noch den Hauptkontotyp im Bericht. Wenn Sie jedoch zur nächsten Ebene in der Hierarchie wechseln, zeigt der Bericht nicht mehr das übergeordnete Element in der Hierarchie an, wie in der folgenden Abbildung dargestellt.

![Schaltfläche für Drillvorgang zurück für Zwischenbilanz.](./media/trial-balance5.png)

Um die Transaktionsdetails hinter den zusammengefassten Salden anzuzeigen, können Sie einige Beträge auswählen, um einen Drillvorgang zu Financial and Operations auszuführen.

Die Drillvorgang zurück von den Finanzaufstellungen führt Sie zum „Buchhaltungsquellen-Explorer” (ASE), nicht zu den Belegtransaktionen. Der ASE zeigt nicht nur die Buchhaltungseinträge im Hauptbuch. Stattdessen zeigt er die Details der Transaktion des untergeordneten Sachkontos. Daher erhalten Sie viel mehr Details über die ursprüngliche Transaktion und Sie können diese für die Analyse verwenden. Sie können beispielsweise sehen, wer der Lieferant oder Kunde war, was der Kunde kaufte oder der Lieferant verkaufte und sogar welches Projekt in der Transaktion war.

Die nachfolgenden Filter aus den Finanzaufstellungen werden an den ASE gesendet, sodass der ASE die Transaktionen anzeigt, die aggregiert werden:

Erforderliche Felder zum Filtern:

- Juristische Person
- Steuerkalender
- Jahr
- Hauptkontokennung

Optionale Felder zum Filtern:

- Quartal
- Monat
- Periode

Wenn Sie bei einer Zeile nicht weit genug nach unten erweitern, funktioniert der Drilldownvorgang nicht. Wenn Sie beispiel nur bis zur Hauptkontokategorie nach unten erweitern, können Sie keinen Drilldown in den ASE zum Saldo durchführen, da das Hauptkonto ein Pflichtfeld für das Filtern im ASE ist.

Wenn Sie in eine Zeile zu weit nach unten erweitern, werden die zusätzlichen Filter in den Finanzaufstellungen nicht an den ASE übermittelt. Daher sehen Sie möglicherweise eine Differenz bei Ihren Zahlen. Wenn Sie beispielsweise herunter zum Land oder Region in den Zeilen der Finanzaufstellung „Gewinn- und Verlustrechnung nach Region” erweitern, wird das Land oder die Region nicht als Filter im ASE einbezogen.

> [!NOTE]
> Sie können in den Finanzaufstellungszeilen oder -spalten einen Drilldown weiter nach unten durchführen, als der ASE aktuell für die Filterung unterstützt. Daher stimmt in manchen Situationen die Summe detaillierter Transaktionen im ASE nicht mit dem Saldo überein, zu dem Sie einen Drillvorgang zurück durchführen. Diese Funktionalität wird in Zukunft weiter verbessert werden.

## <a name="hierarchies"></a>Hierarchien

Von den Standardfinanzaufstellungen werden zwei Hierarchien verwendet, um bei den Daten einen Drillvorgang durchzuführen oder sie zu erweitern. Eine Hierarchie ist für die Zeilen und die andere Hierarchie ist für die Spalten. Beide Hierarchien sind im Entwurf der Finanzaufstellung vordefiniert. Für die meisten Finanzaufstellungen ist die Zeilenhierarchie **Hauptkontotyp** \> **Hauptkontokategorien** \> **Hauptkonto**. Einige Berichte besitzen jedoch zusätzliche Felder, wie Land und Region. Die zusätzlichen Knoten der Hierarchie basieren auf Daten des untergeordneten Sachkontos für jede Transaktion.

Für die Spalten ist die Hierarchie auf die juristischen Personen und die Finanzzeiträume fokussiert. Für die meisten Finanzaufstellungen ist die Spaltenhierarchie **Juristische Person** \> **Steuerkalender** \> **Geschäftsjahr** \> **Quartal** \> **Periode**.

Momentan unterstützen die Finanzaufstellungen nicht die Organisationshierarchien, mit denen Sie Daten aggregieren können.

## <a name="data-limitations"></a>Datenbegrenzungen
Die visuellen Elemente der Finanzaufstellungen haben eine Begrenzung bei der Zahl der Zeilen, die angezeigt werden können. Aktuell ist die Begrenzung auf 30.000 festgelegt. Wenn Sie diese Begrenzung überschreiten, hat das visuelle Element ein Warnsymbol, um Sie über diese Situation zu benachrichtigen.

![Datenbegrenzungen.](./media/data-limit.png)

Wenn das Maximum überschritten wird, sind die Summen, die in der Finanzaufstellung angezeigt werden, nicht korrekt, da nicht alle Zeilen in das visuelle Element geladen wurden.

### <a name="empty-rows"></a>Leere Zeilen
Power BI bietet keine Option, leere Zeilen auszublenden und anzuzeigen. Wenn eine Zeile keine Daten enthält, wird die Zeile im visuellen Element nicht angezeigt.


## <a name="additional-resources-for-power-bi"></a>Zusätzliche Ressourcen für Power BI

Die Informationen in den folgenden Ressourcen sind nicht erforderlich, um die eingebetteten Berichte für den Arbeitsbereich **Finanzanalyse** in einer Produktionsumgebung zu aktivieren. Stattdessen sind sie für Entwicklerfelder hilfreich und wenn Sie Ihre eigenen Power BI-Berichte einbetten möchten.

- [Zugriff auf analytische Arbeitsbereiche und Berichte in einer Umgebungen mit einem Feld](/archive/blogs/dynamicsaxbi/accessing-analytical-workspaces-on-1box-environment)

- [Analysen zu Arbeitsbereichen mit Power BI Embedded hinzufügen](/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

