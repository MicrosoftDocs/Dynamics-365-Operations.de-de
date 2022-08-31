---
title: Bestandsprognosen
description: In diesem Artikel werden die Angebots- und Nachfrageprognosefunktionen beschrieben, mit denen Bestandsprognosen in Microsoft Dynamics 365 Supply Chain Management erstellt werden können.
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 10e3b6ad079dbcbc3cce429a4d9d838e584b9c54
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844524"
---
# <a name="inventory-forecasts"></a>Bestandsprognosen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Bestandsprognosen anzeigen und erstellen. Sie können Angebots- und Nachfrageprognosepositionen für Artikel, Artikelgruppen, Artikelzuordnungsschlüssel, Debitorenkonten, Debitorengruppen, Kreditorenkonten und Kreditorengruppen erstellen und anzeigen.

Für jede Prognosezeile können Sie das verwendete Prognosemodell auswählen. Anschließend können Sie den Artikel oder die Artikelgruppe sowie die Menge oder den Transaktionsbetrag angeben. Sie können auch einen Zeitplan für die Zuweisung der geplanten Menge einrichten.

Die Angebots- und Nachfrageprognosezeilen erzeugen eine Bestandsprognose für dieselbe Kombination eines Artikels und eines Modells. Diese Bestandsprognose stellt ein Gleichgewicht zwischen Angebot und Nachfrage dar, die für denselben Artikel eingegeben wurden. Er kann nicht bearbeitet werden. Die Bestandsprognose hilft dem Lagerverwaltungsteam, erwartete Änderungen des Lagerbestands eines Artikels während des kommenden prognostizierten Zeitraums zu überprüfen.

Wenn Sie Ihre Nachfrage und/oder Vorrat eingegeben haben, können Sie einen Bedarfsplanungslauf durchführen, um den Bruttobedarf an Material und Kapazität zu berechnen und um Bestellvorschläge zu erstellen.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Prognosezeilen anzeigen und manuell eingeben

Verwenden Sie dieses Verfahren, um manuell neue Planungspositionen für Produkte zu erstellen.

Es gibt auch andere Möglichkeiten, Prognosezeilen zu erstellen:

- [Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md).
- [Verlaufsdaten für Bedarfsplanungen importieren](import-historical-data.md).
- [Generieren einer Prognose mit dem Microsoft Azure Machine Learning-Webdienst](demand-forecasting-setup.md).
- [Importieren von Bedarfs- oder Beschaffungsplanungzeilen mithilfe des Datenmanagement-Frameworks (Datenentitäten ForecastDemandForecastEntryStaging und ForecastSupplyForecastEntryStaging)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

Wie die Tabelle in Schritt 1 zeigt, gibt es verschiedene Möglichkeiten, auf die verwendeten Seiten zuzugreifen.

1. Öffnen Sie je nach Art der Entität, für die Sie eine Prognose erstellen möchten, und der Art der Prognose, die Sie erstellen möchten, eine Beschaffungs-, Bedarfs- oder Bestandsplanungsseite, wie in der folgenden Tabelle beschrieben.

    | Entität | Anweisungen |
    |---|---|
    | Freigegebene Produkte | <ol><li>Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</li><li>Wählen Sie das Produkt aus, für das Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich auf der Registerkarte **Planen** in der Gruppe **Prognose** die Option **Bedarfsplanung**, **Beschaffungsplanung**, oder **Bestandsplanung**, abhängig von der Art der Prognose, mit der Sie arbeiten möchten.</li></ol> |
    | Freigegebene Produktvarianten | <ol><li>Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produktvarianten**.</li><li>Wählen Sie die Variante aus, für das Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich auf der Registerkarte **Planen** in der Gruppe **Prognose** die Option **Bedarfsplanung**, **Beschaffungsplanung**, oder **Bestandsplanung**, abhängig von der Art der Prognose, mit der Sie arbeiten möchten.</li></ol> |
    | Artikelgruppen | <ol><li>Gehen Sie zu **Lagerverwaltung \> Einstellungen \> Bestand \> Artikelgruppen**.</li><li>Wählen Sie die Artikelgruppe aus, für die Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich **Planung \> Bedarf**, **Planung \> Beschaffung**, oder **Planung \> Bestandsplanung**, abhängig von der Art der Prognose, mit der Sie arbeiten möchten.</li></ol> |
    | Artikelzuteilungsschlüssel | <ol><li>Wechseln Sie zu **Lagerverwaltung \> Einstellungen \> Planung**.</li><li>Wählen Sie den Artikelzuteilungsschlüssel aus, für die Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich **Bedarfsplanung** aus.</li></ol> |
    | Kunden | <ol><li>Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Debitoren**.</li><li>Wählen Sie den Debitor aus, für das Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich **Bedarfsplanung definieren** aus.</li></ol> |
    | Debitorengruppen | <ol><li>Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Debitorengruppen**.</li><li>Wählen Sie die Debitorengruppe aus, für die Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich **Bedarfsplanung definieren** aus.</li></ol> |
    | Lieferanten | <ol><li>Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Kreditoren**.</li><li>Wählen Sie den Kreditor aus, für den Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich **Eingabe** aus, um die Seite **Beschaffungsplanung** zu öffnen.</li></ol> |
    | Kreditorengruppen | <ol><li>Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Kreditorengruppen**.</li><li>Wählen Sie die Kreditorengruppe aus, für die Sie eine Prognose erstellen möchten.</li><li>Wählen Sie im Aktivitätsbereich **Eingabe** aus, um die Seite **Beschaffungsplanung** zu öffnen.</li></ol> | 
    | Alle Positionen | <ul><li>Gehen Sie zu **Masterplanung \> Planung \> Bedarfsplanungszeilen** oder **Masterplanung \> Planung \> Beschaffungsplanungszeilen**, abhängig von der Art der Prognose, mit der Sie arbeiten möchten.</li></ul> |

    Je nach Auswahl wird die Seite **Beschaffungsplanung** oder **Bedarfsplanung** angezeigt. Es zeigt alle vorhandenen Prognosezeilen für den Datensatz an, den Sie vor dem Öffnen der Seite ausgewählt haben.

1. Wählen Sie im Aktionsbereich **Neu**, um dem Raster im oberen Teil der Seite eine Planungsposition hinzuzufügen.
1. Auf der neuen Position im Feld **Modell** wählen Sie im Feld das zu verwendende Planungsmodell aus. Geben Sie dann nach Bedarf weitere Details ein, z. B. Artikel, Artikelgruppe, Debitoren- oder Kreditorenkonto oder -gruppe, Artikelmenge oder Gesamttransaktionsbetrag. Ausführliche Informationen zu den Feldern, die auf den Seiten **Beschaffungsplanung** und **Bedarfsplanung** verfügbar sind, finden Sie in den späteren Abschnitten dieses Artikels.
1. Um die Prognose über den Zeitraum zu verteilen, wählen Sie auf der Registerkarte **Überblick** die Option **Planung zuordnen** auf der Symbolleiste.
1. Prüfen Sie im Raster **Zuteilung** den Zeithorizont sowie die Zeitintervalle einzurichten, die verwendet werden, um die Planungsmengen zu verteilen.

## <a name="supply-forecast-lines"></a>Beschaffungsplanungspositionen

Mit der Beschaffungsplanung können Sie einen Plan für zu kaufende Artikel erstellen. Es teilt Einkaufs- und Beschaffungsmitarbeitern mit, was sie bestellen sollen.

Sie können eine Beschaffungsplanung nach Artikel, Artikelgruppe, Artikelzuordnungsschlüssel, Lieferant und Lieferantengruppe eingeben. Informationen zu allen Möglichkeiten zum Öffnen der Seite **Beschaffungsplanung** für verschiedene Entitäten und Datensätze finden Sie im Abschnitt [Planungspositionen anzeigen und manuell eingeben](#manual-entry) weiter oben in diesem Artikel.

Der obere Teil der Seite **Beschaffungsplanung** enthält ein Raster mit Beschaffungsplanungspositionen und eine Reihe von Registerkarten, die Sie verwenden können, um weitere Informationen zu einer ausgewählten Planungspositionen anzuzeigen und festzulegen. Der untere Teil der Seite bietet ein Raster **Zuteilung**.

In den folgenden Unterabschnitten werden alle Felder beschrieben, die auf jeder Registerkarte verfügbar sind, sowie alle Befehle, die im Aktivitätsbereich der Seite und in der Symbolleiste auf der Registerkarte **Überblick** verfügbar sind.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Aktionsbereichbefehle auf der Seite „Beschaffungsplanung“

Die folgende Tabelle beschreibt die Befehle, die im Aktivitätsbereich der Seite **Beschaffungsplanung** verfügbar sind.

| Befehl | Beschreibung |
|---|---|
| Speichern | Speichern Sie Ihre aktuellen Einstellungen. |
| Bearbeiten | Aktivieren Sie die Einstellungen auf der zu bearbeitenden Seite. |
| Neue | Fügen Sie eine Planungsposition im oberen Teil des Rasters hinzu. |
| Löschen | Entfernen Sie die ausgewählte Planungsposition aus dem oberen Raster. |
| Planungssalden | Zeigen Sie Planungssalden an, die für die Modell-ID der ausgewählten Position für das aktuelle Geschäftsjahr berechnet wurden. Die Salden werden nach Periode (Monat) aufgeteilt. |
| Cashflow-Planungen | Zeigen Sie prognostizierte Transaktionen an, die dem Hauptbuch zugeordnet wurden. Weitere Informationen unter [Cashflowprognosen](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Bestand \> Dimensionen anzeigen | Wählen Sie die Bestandsdimensionen aus, die im Raster auf der Registerkarte **Überblick** angezeigt werden sollen. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Symbolleistenbefehle auf der Registerkarte „Übersicht“ der Seite Angebotsprognose

Die folgende Tabelle beschreibt die Befehle, die in der Symbolleiste auf der Registerkarte **Übersicht** der Seite **Beschaffungsplanung** verfügbar sind.

| Befehl | Beschreibung |
|---|---|
| Planung zuordnen | Wenn Sie eine Verrechnungsmethode verwenden, generieren Sie die einzelnen Einteilungen für den Prognosetransaktion. Die Menge der Position wird dann nach Datum (entsprechend den ausgewählten Zeitintervallen), Menge und Betrag für den gesamten Zeithorizont verteilt. (Siehe den Abschnitt [Planung zuordnen](#allocate-forecast) weiter unten in diesem Artikel.) |
| Sammelaktualisierung | Öffnen Sie die Seite **Planungsbuchungen bearbeiten**. (Siehe den Abschnitt [Planungsbuchungen im Bulk aktualisieren](#bulk-update) weiter unten in diesem Artikel.) |
| Planzahlenergebnis | Öffnen Sie eine Ansicht der Seite **Bestandsplanung**, die nach der ausgewählten Artikel-/Modellkombination gefiltert wird. (Siehe den Abschnitt [Bestandsplanunf](#inventory-forecast) weiter unten in diesem Artikel.) |
| Artikelbedarf erstellen | Öffnen Sie ein Dialogfeld, in dem Sie Artikelbedarfe und Kundenauftrags- oder Artikelerfassungszeilen für projektbezogene Planungsbuchungen erstellen können. Obwohl dieser Befehl sowohl für Beschaffungsplanung als auch für Bedarfsplanung verfügbar ist, kann er nicht für die Seite **Beschaffungsplanung** verwendet werden. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Symbolleistenbefehle auf der Registerkarte „Übersicht“ der Seite „Beschaffungsplanung“

Die folgende Tabelle beschreibt die Felder auf der Registerkarte **Übersicht** der Seite **Beschaffungsplanung**.

| Feld | Beschreibung |
|---|---|
| **Modell** | Das Planungsmodell, dem die Buchung zugewiesen ist. |
| **Datum** | Das Startdatum der Buchung. |
| **Kreditorenkonto** | Das der Buchung zugeordnete Kreditorenkonto. |
| **Kreditorengruppe** | Die der Buchung zugeordnete Kreditorengruppe. |
| **Artikelnummer** | Die Kennung des Artikels. |
| **Artikelgruppe** | Die Artikelgruppe, der die Buchung zugeordnet ist. |
| **Artikelzuteilungsschlüssel** | Der Artikelverteilungsschlüssel, der der Planung zugeordnet ist. |
| **Artikelgewichtsmenge** | Die prognostizierte Menge in der angegebenen Artikelgewichteinheit. |
| **Artikelgewichtseinheit** | Die Artikelgewichteinheit ist die Einheit, in der der Artikel eingekauft wird. Der Wert wird automatisch aus der Artikeleinrichtung abgerufen. |
| **Menge** | Die geplante Menge in der angegebenen Bestelleinheit. |
| **Einheit** | Die Einheit, in der der Artikel bestellt wird. Der Wert wird automatisch aus der Artikeleinrichtung abgerufen. Sie können es jedoch ändern, wenn Einheitenumrechnungen eingerichtet sind. |
| **Betrag** | Der Bruttobetrag abzüglich Rabatten, mit dem die Planungsbuchung zur Planung beiträgt. |
| **Währung** | Die für die Planungsbuchung verwendete Währung. Die Standardwährung wird automatisch eingegeben, aber der Benutzer kann eine andere Währung auswählen. |
| (Andere Dimensionen) | Zusätzliche Dimensionen können als Spalten im Raster angezeigt werden. Wählen Sie **Dimensionen anzeigen** im Aktivitätsbereich, um die zusätzlichen Dimensionen auszuwählen, die angezeigt werden sollen. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Die Registerkarte „Allgemein“ der Seite „Beschaffungsplanung“

Die Registerkarte **Allgemein** zeigt weitere Informationen über die aktuell ausgewählte Position auf der Registerkarte **Übersicht** an. Einige dieser Informationen werden aus der Registerkarte **Übersicht** wiederholt. In der folgenden Tabelle werden die Felder beschrieben, die für die Registerkarte **Allgemeines** einzigartig sind.

| Feld | Beschreibung |
|---|---|
| Bericht | Setzen Sie diese Option auf *Ja*, wenn die Buchung im Bericht enthalten sein soll. |
| Kommentare | Geben Sie alle Kommentare zur Planungsbuchung ein. |
| Aktiv | Aktivieren Sie dieses Kontrollkästchen, wenn die Buchung im Budgetbericht enthalten sein soll. |
| In Cashflowplanungen einbeziehen | Aktivieren Sie dieses Kontrollkästchen, um die Planungsbuchung dem Hauptbuch zuzuweisen. Die Einstellung dieses Kontrollkästchens kann zum Melden von Transaktionen nicht geändert werden. |
| Mehrwertsteuergruppe | Die Steuergruppe, die zur Angabe von Steuern für die Planungsbuchung verwendet wird. |
| Artikel-Mehrwertsteuergruppe | Die Artikelsteuergruppe, die zur Angabe von Steuern für die Planungsbuchung verwendet wird. |
| Methode | <p>Wählen Sie die Methode aus, die verwendet wird, um die Planungsbuchung zuzuordnen:</p><ul><li>**Keine** – Es findet keine Zuweisung statt.</li><li>**Zeitraum** – Für jede Periode die gleiche Menge prognostizieren. Wenn Sie diesen Wert auswählen, geben Sie eine Menge im Feld **Pro** Feld und eine Zeiteinheit im Feld **Einheit** ein.</li><li>**Schlüssel** – Die Planungsmenge wird entsprechend dem Planzahlenverteilungsschlüssel zugeordnet, den Sie im Feld **Periodenschlüssel** angegeben haben. Sie können diese Methode verwenden, wenn saisonale Schwankungen berücksichtigt werden sollen.</li></ol>|
| Pro | <p>Geben Sie die Anzahl von Zeitintervallen ein, um die die Planung in die Zukunft reicht. Dieses Feld ist nur verfügbar, wenn im Feld *Zeitraumtyp* **Methode** ausgewählt wird.</p><p>Wenn Sie zum Beispiel *Period* im Feld **Methode** auswählen, geben Sie im Feld *Pro* **1** ein und wählen Sie *Monate* im Feld **Einheit** aus. Geben Sie im Feld **Ende** ein Enddatum an, das ein Jahr in die Zukunft reicht. In diesem Fall wird für jeden Monat des kommenden Jahrs basierend auf den Artikel- und Mengenangaben in der Kopfzeile eine Planungsposition erstellt.</p> |
| Einheit | Wählen Sie die Einheit des Zeitintervalls: *Tage*, *Monate*, oder *Jahre*. Zuteilung entspricht dann der Anzahl von Tagen, Monaten oder Jahren, die Sie im Feld **Pro** festgelegt haben.|
| Periodenschlüssel | Den Planzahlenverteilungsschlüssel anzeigen. |
| Beenden | Geben Sie das Enddatum an, wenn Sie die Felder **Pro** und **Einheit** verwenden. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Die Registerkarte „Artikel“ der Seite „Beschaffungsplanung“

Die Registerkarte **Artikel** zeigt weitere Informationen über die Zeile anzuzeigen, die gerade auf der Registerkarte **Übersicht** ausgewählt ist.

Das Raster oben auf der Registerkarte **Artikel** wiederholt die Elementinformationen, die auch auf der Registerkarte **Übersicht** angezeigt werden. Darüber hinaus enthält es das Feld **Preis je Einheit**, das den Kaufpreis für die Anzahl der Einheiten anzeigt, die im Feld **Einheit** angegeben sind. Der Preis je Einheit wird automatisch aus der Artikeleinrichtung abgerufen, kann jedoch geändert werden.

Die Felder unterhalb des Rasters enthalten weitere Artikeldetails. Einige dieser Informationen werden aus der Registerkarte **Übersicht** wiederholt. In der folgenden Tabelle werden die Felder beschrieben, die für die Registerkarte **Artikel** einzigartig sind.

| Feld | Beschreibung |
|---|---|
| Preiseinheit | Die Anzahl von Einheiten an, auf die sich der Einkaufspreis bezieht. Der Wert wird automatisch aus der Artikeltabelle abgerufen, kann jedoch geändert werden. |
| Belastungen für Einkäufe | Die festen Zuschläge für den Einkaufspreis. Verkaufsbelastungen sind unabhängig von der Menge. |
| Rabattprozentsatz | Der Rabatt als Prozentsatz. |
| Rabattbetrag | Als Betrag pro Verkaufseinheit ausgedrückter Rabatt. |
| Bruttobetrag | Der Betrag, wenn keine Rabatte gewährt werden. |
| Menge | Die Buchungsmenge, ausgedrückt in der Lagereinheit des Artikels. |
| Unterstückliste | Die Stücklistennummer einer bestimmten untergeordneten Stückliste. |
| Teilstrecke | Die Arbeitsplannummer eines bestimmten untergeordneten Arbeitsplans. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Die Registerkarte „Finanzdimensionen“ der Seite „Beschaffungsplanung“

Die Registerkarte **Finanzdimensionen** zeigt alle Finanzdimensionswerte für die Zeile an, die derzeit auf der Registerkarte **Übersicht** ausgewählt sind.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Die Registerkarte „Bestandsdimensionen“ der Seite „Beschaffungsplanung“

Die Registerkarte **Bestandsdimensionen** zeigt alle Bestandsdimensionswerte für die Zeile an, die derzeit auf der Registerkarte **Übersicht** ausgewählt sind.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Das Zuteilungsraster auf der Seite „Beschaffungsplanung“

Wenn Sie einen Artikelzuordnungsschlüssel verwenden oder eine Artikelprognose für eine oder mehrere zukünftige Perioden eingegeben haben, können Sie die Prognose zuordnen, indem Sie **Planung zuordnen** in der Symbolleiste auf der Registerkarte **Übersicht** auswählen. Die Menge wird dann so verteilt, wie es durch die Positionen im Raster **Zuteilung** angezeigt wird.

## <a name="demand-forecast-lines"></a>Bedarfsplanungspositionen

Mit der Bedarfsplanung können Sie Bedarf für einen Debitoren erfassen oder generieren. Es hilft Vertriebs- und Marketingsachbearbeitern, Masterplanungssachbearbeiter über den erwarteten Bedarf im kommenden Planungszeitraum zu informieren.

Sie können eine Bedarfsplanung nach Artikel, Artikelgruppe, Artikelzuordnungsschlüssel, Debitor und Deboitorengruppe eingeben. Informationen zu allen Möglichkeiten zum Öffnen der Seite **Bedarfsplanung** für verschiedene Entitäten und Datensätze finden Sie im Abschnitt [Planungspositionen anzeigen und manuell eingeben](#manual-entry) weiter oben in diesem Artikel.

Der obere Teil der Seite **Bedarfsplanung** enthält ein Raster mit Bedarfsplanungspositionen und eine Reihe von Registerkarten, die Sie verwenden können, um weitere Informationen zu einer ausgewählten Planungspositionen anzuzeigen und festzulegen. Der untere Teil der Seite bietet ein Raster **Zuteilung**.

In den folgenden Unterabschnitten werden alle Felder beschrieben, die auf jeder Registerkarte verfügbar sind, sowie alle Befehle, die im Aktivitätsbereich der Seite und in der Symbolleiste auf der Registerkarte **Überblick** verfügbar sind.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Aktionsbereichbefehle auf der Seite „Bedarfsplanung“

Die folgende Tabelle beschreibt die Befehle, die im Aktivitätsbereich der Seite **Bedarfsplanung** verfügbar sind.

| Befehl | Beschreibung |
|---|---|
| Speichern | Speichern Sie Ihre aktuellen Einstellungen. |
| Bearbeiten | Aktivieren Sie die Einstellungen auf der zu bearbeitenden Seite. |
| Neue | Fügen Sie eine Planungsposition im oberen Teil des Rasters hinzu. |
| Löschen | Entfernen Sie die ausgewählte Planungsposition aus dem oberen Raster. |
| Planungssalden | Zeigen Sie Planungssalden an, die für die Modell-ID der ausgewählten Position für das aktuelle Geschäftsjahr berechnet wurden. Die Salden werden nach Periode (Monat) aufgeteilt. |
| Cashflow-Planung | Zeigen Sie prognostizierte Transaktionen an, die dem Hauptbuch zugeordnet werden muss. Weitere Informationen unter [Cashflowprognosen](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Dimensionen anzeigen | Wählen Sie die Produkt-, Lager- und Rücckverfolgungsdimensionen aus, die im Raster auf der Registerkarte **Übersicht** angezeigt werden sollen. |
| Hauptbuch - Vorschau | Zeigt die Hauptbucheinträge für die ausgewählte Buchung an. |
| Angebotspositionen übertragen | Hiermit können Sie Angebotspositionen in das ausgewählte Projekt übertragen. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Symbolleistenbefehle auf der Registerkarte „Übersicht“ der Seite Bedarfsplanung

Die folgende Tabelle beschreibt die Befehle, die in der Symbolleiste auf der Registerkarte **Übersicht** der Seite **Bedarfsplanung** verfügbar sind.

| Befehl | Beschreibung |
|---|---|
| Planung zuordnen | Wenn Sie eine Verrechnungsmethode verwenden, generieren Sie die einzelnen Einteilungen für den Prognosetransaktion. Die Menge der Position wird dann nach Datum (entsprechend den ausgewählten Zeitintervallen), Menge und Betrag für den gesamten Zeithorizont verteilt. (Siehe den Abschnitt [Planung zuordnen](#allocate-forecast) weiter unten in diesem Artikel.)|
| Sammelaktualisierung | Öffnen Sie die Seite **Planungsbuchungen bearbeiten**. (Siehe den Abschnitt [Planungsbuchungen im Bulk aktualisieren](#bulk-update) weiter unten in diesem Artikel.) |
| Planzahlenergebnis | Öffnen Sie eine Ansicht der Seite **Bestandsplanung**, die nach der ausgewählten Artikel-/Modellkombination gefiltert wird. (Siehe den Abschnitt [Bestandsplanunf](#inventory-forecast) weiter unten in diesem Artikel.) |
| Artikelbedarf erstellen | Öffnen Sie ein Dialogfeld, in dem Sie Artikelbedarfe und Kundenauftrags- oder Artikelerfassungszeilen für projektbezogene Planungsbuchungen erstellen können. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Symbolleistenbefehle auf der Registerkarte „Übersicht“ der Seite „Bedarfsplanung“

Die folgende Tabelle beschreibt die Felder auf der Registerkarte **Übersicht** der Seite **Bedarfsplanung**.

| Feld | Beschreibung |
|---|---|
| **Name der Aufgaben** | Der Name der Stapelverarbeitungsaufgabe, die zum Erstellen der Planungsposition verwendet wurde. |
| **Modell** | Das Planungsmodell, dem die Buchung zugewiesen ist. |
| **Datum** | Das Startdatum der Buchung. |
| **Debitorenkonto** | Das der Buchung zugeordnete Debitorenkonto. |
| **Debitorengruppe** | Die der Buchung zugeordnete Debitorengruppe. |
| **Artikelnummer** | Die Kennung des Artikels. |
| **Produktname** | Die Beschreibung des Artikels. |
| **Artikelzuteilungsschlüssel** | Der Artikelverteilungsschlüssel, der während der Planzahlenzuweisung verwendet wird. |
| **Verkaufsmenge** | Die Buchungsmenge in der angegebenen Verkaufseinheit. |
| **Einheit** | Die Einheit, in der der Artikel verkauft wird. |
| **Betrag** | Der Bruttobetrag abzüglich Rabatten, mit dem die Planungsbuchung zur Planung beiträgt. |
| **Verkaufspreis** | Der Verkaufspreis für die Anzahl der Einheiten, die im Feld **Preiseinheit** angegeben sind. Die Werte werden aus der Artikeleinrichtung abgerufen, können jedoch geändert werden. |
| **Verkaufswährung** | Die für die Planungsbuchung verwendete Währung. Die Standardwährung wird automatisch eingegeben, aber der Benutzer kann eine andere Währung auswählen. |
| **Artikelgewichtsmenge** | Die prognostizierte Menge in der angegebenen Artikelgewichteinheit. |
| **Artikelgewichtseinheit** | Die Artikelgewichteinheit ist die Einheit, in der der Artikel verkauft wird. Der Wert wird automatisch aus der Artikeleinrichtung abgerufen. |
| (Andere Dimensionen) | Zusätzliche Produkt-, Lager- und Rückverfolgungsimensionen können als Spalten im Raster angezeigt werden. Wählen Sie **Dimensionen anzeigen** im Aktivitätsbereich, um die zusätzlichen Dimensionen auszuwählen, die angezeigt werden sollen. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Die Registerkarte „Allgemein“ der Seite „Bedarfsplanung“

Die Registerkarte **Allgemein** zeigt weitere Informationen über die aktuell ausgewählte Position auf der Registerkarte **Übersicht** an. Einige dieser Informationen werden aus der Registerkarte **Übersicht** wiederholt. In der folgenden Tabelle werden die Felder beschrieben, die für die Registerkarte **Allgemeines** einzigartig sind.

| Feld | Beschreibung |
|---|---|
| Sequenzzahl der Bedarfsplanung | Die eindeutige Nummer der Bedarfsplanungsposition. Diese Nummer wird generiert, indem der Nummernkreis verwendet wird, der für Bedarfsplanung auf der Seite **Masterplanungsparameter** ausgewählt ist. |
| Artikelgruppe | Die Artikelgruppe, der die Buchung zugeordnet ist. |
| Bericht | Setzen Sie diese Option auf *Ja*, wenn die Buchung im Bericht enthalten sein soll. |
| Kommentare | Geben Sie alle Kommentare zur Planungsbuchung ein. |
| Aktiv | Aktivieren Sie dieses Kontrollkästchen, wenn die Buchung im Budgetbericht enthalten sein soll. Die Einstellung dieses Kontrollkästchens kann zum Melden von Transaktionen nicht geändert werden. |
| In Cashflowplanungen einbeziehen | Aktivieren Sie dieses Kontrollkästchen, um die Planungsbuchung dem Hauptbuch zuzuweisen. Die Einstellung dieses Kontrollkästchens kann zum Melden von Transaktionen nicht geändert werden. Weitere Informationen unter [Cashflowprognosen](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Mehrwertsteuergruppe | Die Steuergruppe, die zur Angabe von Steuern für die Planungsbuchung verwendet wird. |
| Artikel-Mehrwertsteuergruppe | Die Artikelsteuergruppe, die zur Angabe von Steuern für die Planungsbuchung verwendet wird. |
| Methode | <p>Wählen Sie die Methode aus, die verwendet wird, um die Planungsbuchung zuzuordnen:</p><ul><li>**Keine** – Es findet keine Zuweisung statt.</li><li>**Zeitraum** – Für jede Periode die gleiche Menge prognostizieren. Wenn Sie diesen Wert auswählen, geben Sie eine Menge im Feld **Pro** Feld und eine Zeiteinheit im Feld **Einheit** ein.</li><li>**Schlüssel** – Die Planungsmenge wird entsprechend dem Planzahlenverteilungsschlüssel zugeordnet, den Sie im Feld **Periodenschlüssel** angegeben haben. Sie können diese Methode verwenden, wenn saisonale Schwankungen berücksichtigt werden sollen.</li><ul>|
| Pro | <p>Geben Sie die Anzahl von Zeitintervallen ein, um die die Planung in die Zukunft reicht. Dieses Feld ist nur verfügbar, wenn im Feld *Zeitraumtyp* **Methode** ausgewählt wird.</p><p>Wenn Sie zum Beispiel *Period* im Feld **Methode** auswählen, geben Sie im Feld *Pro* **1** ein und wählen Sie *Monate* im Feld **Einheit** aus. Geben Sie im Feld **Ende** ein Enddatum an, das ein Jahr in die Zukunft reicht. In diesem Fall wird für jeden Monat des kommenden Jahrs basierend auf den Artikel- und Mengenangaben in der Kopfzeile eine Planungsposition erstellt. |
| Einheit | Wählen Sie die Einheit des Zeitintervalls: *Tage*, *Monate*, oder *Jahre*. Zuteilung entspricht dann der Anzahl von Tagen, Monaten oder Jahren, die Sie im Feld **Pro** festgelegt haben.|
| Periodenschlüssel | Geben Sie den Periodenzuordnungsschlüssel an, der für die Zuordnung der Planung verwendet wird. Weitere Informationen finden Sie unter [Zuteilung von Budgetplanungsdaten](../../finance/budgeting/budget-planning-data-allocation.md). |
| Beenden | Geben Sie das Enddatum an, wenn Sie die Felder **Pro** und **Einheit** verwenden. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Die Registerkarte „Artikel“ der Seite „Bedarfsplanung“

Die Registerkarte **Artikel** zeigt weitere Artikelnformationen über die aktuell ausgewählte Position auf der Registerkarte **Übersicht** an. Einige dieser Informationen werden aus der Registerkarte **Übersicht** wiederholt. In der folgenden Tabelle werden die Felder beschrieben, die für die Registerkarte **Artikel** einzigartig sind.

| Feld | Beschreibung |
|---|---|
| Preiseinheit | Die Anzahl der Verkaufseinheiten, für die der Verkaufspreis zutrifft. Der Wert wird automatisch aus der Artikeltabelle abgerufen, kann jedoch geändert werden. |
| Verkauf – Belastungen | Die festen Zuschläge für den Verkaufspreis. Verkaufsbelastungen sind unabhängig von der Menge. |
| Einstandspreis | Die Kosten für die aktuelle Planungsbuchung pro Lagereinheit. Der Wert wird aus der Artikeltabelle abgerufen, können jedoch geändert werden. |
| Rabattprozentsatz | Der Rabatt als Prozentsatz. |
| Rabattbetrag | Als Betrag pro Verkaufseinheit ausgedrückter Rabatt. |
| Bruttobetrag | Der Betrag, wenn keine Rabatte gewährt werden. |
| Lagermenge | Die Buchungsmenge, ausgedrückt in der Lagereinheit des Artikels. |
| Bestimmte Stückliste verwenden | Die Stücklistennummer einer bestimmten Stückliste. |
| Bestimmten Arbeitsplan verwenden | Die Arbeitsplannummer eines bestimmten untergeordneten Arbeitsplans. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Die Registerkarte „Projekt“ der Seite „Bedarfsplanung“

Die Registerkarte **Projekt** zeigt weitere Projektinformationen über die aktuell ausgewählte Position auf der Registerkarte **Übersicht** an. Einige dieser Informationen werden aus den Registerkarten **Übersicht**, **Allgemein**, oder **Artikel** wiederholt. In der folgenden Tabelle werden die Felder beschrieben, die für die Registerkarte **Projekt** einzigartig sind.

| Feld | Beschreibung |
|---|---|
| Projektdatum | Das Datum der Bedarfsplanungsbuchung. |
| Projektkennung | Der von der aktuellen Buchung zugewiesene Bezeichner des Projekts. |
| Finanzierungsquelle | Die der Beschaffungsplanung zugeordnete Finanzierungsquelle. |
| Aktivitätsnummer | Die der Bedarfsplanungsbuchung zugeordnete Finanzierungsquelle. |
| Kategorie | Die Kostenkategorie der aktuellen Buchung. |
| Abrechnungscode | Der Status, dem die Buchung zugeordnet ist. |
| Transaktions-ID | Die Systemkennung für die Bedarfsplanungsbuchung. |
| Betrag der Kosten | Der Betrag der Bedarfsplanungsbuchung. |
| Preis je Einheit | Der Preis pro Einheit. |
| Geändert von | Die Kennung der Arbeitskraft, die die ausgewählte Buchung zuletzt geändert hat. |
| Rechnungsdatum | Geben Sie das erwartete Rechnungsdatum ein. |
| Löschungsdatum | Hier können Sie das Änderungsdatum anzeigen oder ändern. Bei Erstellung der Planung wird das Löschungsdatum auf das Enddatum des Projekts festgelegt. Wenn für das Projekt kein Enddatum festgelegt wurde, wird das Projektdatum verwendet. Dieses Feld bezieht sich auf Festpreis- und Investitionsprojekte. |
| Kostenzahlungsdatum | Geben Sie das voraussichtliche Datum für die Bezahlung der Bestellung ein. |
| Verkaufszahlungsdatum | Geben Sie das voraussichtliche Datum für die Bezahlung des Verkaufs ein. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Die Registerkarte „Finanzdimensionen“ der Seite „Bedarfsplanung“

Die Registerkarte **Finanzdimensionen** zeigt alle Finanzdimensionswerte für die Zeile an, die derzeit auf der Registerkarte **Übersicht** ausgewählt sind.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Die Registerkarte „Bestandsdimensionen“ der Seite „Bedarfsplanung“

Die Registerkarte **Bestandsdimensionen** zeigt alle Bestandsdimensionswerte für die Zeile an, die derzeit auf der Registerkarte **Übersicht** ausgewählt sind.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Das Zuteilungsraster auf der Seite „Bedarfsplanung“

Wenn Sie einen Artikelzuordnungsschlüssel verwenden oder eine Artikelprognose für eine oder mehrere zukünftige Perioden eingegeben haben, können Sie die Prognose zuordnen, indem Sie **Planung zuordnen** in der Symbolleiste auf der Registerkarte **Übersicht** auswählen. Die Menge wird dann so verteilt, wie es durch die Positionen im Raster **Zuteilung** angezeigt wird. (Siehe den Abschnitt [Planung zuordnen](#allocate-forecast) weiter unten in diesem Artikel.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Planzahlenergebnis

Die Seiten der Beschaffungs- und Bedarfsplanung haben eine Schaltfläche **Bestandsplanung**, die eine Ansicht der Seite **Bestandsplanung** Seite öffnet, die nach derselben Artikel-/Modellkombination gefiltert wird. Die Bestandsprognose stellt ein Gleichgewicht zwischen Angebot und Nachfrage dar, die für denselben Artikel eingegeben wurden. Er kann nicht bearbeitet werden. Die Bestandsprognose hilft dem Lagerverwaltungsteam, erwartete Änderungen des Lagerbestands eines Artikels während des kommenden prognostizierten Zeitraums zu überprüfen.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Der Aktionsbereich auf der Seite „Bestandsplanung“

Die folgende Tabelle beschreibt die Befehle, die im Aktivitätsbereich der Seite **Bestandsplanung** verfügbar sind.

| Vorgang | Beschreibung |
|---|---|
| Beschaffungsplanung | Öffnen Sie eine Ansicht der Seite **Beschaffungsplanung**, die nach derselben Artikel-/Modell-/Datumskombination gefiltert wird. |
| Bedarfsplanung | Öffnen Sie eine Ansicht der Seite **Bedarfsplanung**, die nach derselben Artikel-/Modell-/Datumskombination gefiltert wird. |
| Bestand \> Dimensionen anzeigen | Wählen Sie die Produkt-, Lager- und Rücckverfolgungsdimensionen aus, die im Raster **Übersicht** angezeigt werden sollen. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Das Raster auf der Seite „Bestandsplanung“

Die folgende Tabelle beschreibt die Felder im Raster auf der Seite **Bestandsplanung**.

| Feld | Beschreibung |
|---|---|
| **Modell** | Das Planungsmodell, dem die Buchung zugewiesen ist. |
| **Artikelnummer** | Die Kennung des Artikels. |
| **Budgetdatum** | Das Datum der Planungsbuchung. |
| **Planungstyp** | Die Quelle der Transaktion (*Bedarfsplanung* oder *Beschaffungsplanung*). |
| **Artikelgewichtsmenge** | Die prognostizierte Menge in der Artikelgewichteinheit. |
| **Menge** | Die geplante Menge in der Lagereinheit. |
| **Artikelgewicht kumuliert** | Die kumulierte Planungsmenge in der Artikelgewichteinheit, wenn mehrere Planungspositionen für denselben Artikel kumuliert wurden. |
| **Unterstückliste** | Die Stücklistennummer einer bestimmten untergeordneten Stückliste. |
| **Teilstrecke** | Die Arbeitsplannummer eines bestimmten untergeordneten Arbeitsplans. |
| (Andere Dimensionen) | Zusätzliche Dimensionen können als Spalten im Raster angezeigt werden. Wählen Sie im Aktivitätsbereich **Bestand \> Dimensionen anzeigen**, um die zusätzlichen Dimensionen auszuwählen, die angezeigt werden sollen. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Planung zuordnen

Die folgende Prozedur dient zum Verarbeiten ausgewählter Buchungspositionen. Wenn Sie eine Planung zuordnen, wird die Menge wie durch die Positionen im Raster **Zuteilung** angegeben verteilt.

1. Öffnen Sie je nach Art der Entität, für die Sie eine Planung erstellen möchten, und der Art der Planung, die Sie erstellen möchten, eine Beschaffungs- oder Bedarfsplanungsseite, wie unter [Planungspositionen anzeigen und manuell eingeben](#manual-entry) beschrieben.
1. Wählen Sie auf der Seite „Beschaffungs- oder Bedarfsplanungspositionen“ eine Planungsposition aus. Wählen Sie dann auf der Registerkarte **Übersicht** auf der Symbolleiste **Planung zuordnen** aus.
1. Legen Sie im Dialogfeld **Planung zuordnen** die Felder fest, die in der folgenden Tabelle beschrieben werden. (Der Wert, den Sie im Feld **Methode** auswählen, legt die anderen verfügbaren Felder fest.)

    | Feld | Beschreibung |
    |---|---|
    | Methode | <p>Wählen Sie die Methode aus, die verwendet wird, um die Planungsbuchung zuzuordnen:</p><ul><li>**Keine** – Es findet keine Zuweisung statt.</li><li>**Zeitraum** – Für jede Periode die gleiche Menge prognostizieren. Wenn Sie diesen Wert auswählen, geben Sie eine Menge im Feld **Pro** Feld und eine Zeiteinheit im Feld **Einheit** ein.</li><li>**Schlüssel** – Die Planungsmenge wird entsprechend dem Planzahlenverteilungsschlüssel zugeordnet, den Sie im Feld **Periodenschlüssel** angegeben haben. Sie können diese Methode verwenden, wenn saisonale Schwankungen berücksichtigt werden sollen.</li><ul>|
    | Pro | <p>Geben Sie die Anzahl von Zeitintervallen ein, um die die Planung in die Zukunft reicht. Dieses Feld ist nur verfügbar, wenn im Feld *Zeitraumtyp* **Methode** ausgewählt wird.</p><p>Wenn Sie zum Beispiel *Period* im Feld **Methode** auswählen, geben Sie im Feld *Pro* **1** ein und wählen Sie *Monate* im Feld **Einheit** aus. Geben Sie dann im Feld **Ende** ein Enddatum an, das ein Jahr in die Zukunft reicht. In diesem Fall wird für jeden Monat des kommenden Jahrs basierend auf den Artikel- und Mengenangaben in der Kopfzeile eine Planungsposition erstellt. |
    | Einheit | Wählen Sie die Einheit des Zeitintervalls: *Tage*, *Monate*, oder *Jahre*. Zuteilung entspricht dann der Anzahl von Tagen, Monaten oder Jahren, die Sie im Feld **Pro** festgelegt haben.|
    | Periodenschlüssel | Geben Sie den Periodenzuordnungsschlüssel an, der für die Zuordnung der Planung verwendet wird. Weitere Informationen finden Sie unter [Zuteilung von Budgetplanungsdaten](../../finance/budgeting/budget-planning-data-allocation.md). |
    | Beenden | Geben Sie das Enddatum an, das für Ihre Einstellungen in den Feldern **Pro** und **Einheit** gilt. |

1. Wählen Sie **OK** aus, um Ihre Einstellungen zu bestätigen.
1. Sie können die Ergebnisse auf der Registerkarte **Zuteilung** für die gleiche Position überprüfen.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Planungsbuchungen im Bulk aktualisieren

Dieses Verfahren dient zum Verarbeiten vorhandener Buchungspositionen. Planungsbuchungspositionen können kopiert, geändert und gelöscht werden.

1. Wählen Sie auf der Seite „Beschaffungs- oder Bedarfsplanungspositionen“ **Bulk-Update**.
1. Klicken Sie im Dialogfeld auf **Filter**.
1. Wählen Sie auf der Registerkarte **Bereich** die Kriterien für die Quellplanungsdaten aus, die kopiert, geändert oder gelöscht werden sollen. Zu den Daten zählen möglicherweise das Planzahlenmodell, Artikelnummer und Debitorenkonto.
1. Wählen Sie **OK**, um Ihre Auswahl zu bestätigen.

    Nachdem die Daten ausgewählt wurden, können Sie das Dialogfeld **Planungsbuchungen bearbeiten** verwenden, um festzulegen, wie Sie es kopieren, bearbeiten oder löschen möchten.

    > [!NOTE]
    > Der Filterschritt ist Voraussetzung für die Verwendung der Funktion **Bulk-Bearbeitung**. Wenn Sie es überspringen, wählt das Programm **alle** Planungspositionen aus und aktualisiert sie. Daher können Sie unbeabsichtigt eine Duplizierung oder Entfernung von Buchungen verursachen.

1. Im Abschnitt **Verwaltung** können Sie auswählen, ob Sie die ausgewählten Planungsbuchungen kopieren, aktualisieren oder löschen möchten.
1. Verwenden Sie den Abschnitt **Änderungen im Feld** zum Ändern der Parameter für die Planung. Aktivieren Sie das Kontrollkästchen des gewünschten Parameters, und treffen Sie anschließend in den zur Verfügung stehenden Optionen eine Auswahl. Wählen Sie beispielsweise das Kontrollkästchen **Modell**, und wählen Sie dann eine Planungsmodellnummer aus. Vorhandene Planungspositionen werden in das ausgewählte Planzahlenmodell kopiert.
1. Verwenden Sie den Abschnitt **Änderung der Periode**, um das Start- und Enddatum der Planung nach vorne oder hinten zu verschieben. Aktivieren Sie das entsprechende Kontrollkästchen, und definieren Sie mithilfe der Mengen- und Periodenfelder das Verschieben der Planungsdatumswerte. Sie können eine negative Menge eingeben, um das Startdatum nach vorne zu verschieben (d. h. früher zu machen).

    Um beispielsweise das geplante Startdatum der Buchung um sechs Monate zu verschieben, aktivieren Sie das Kontrollkästchen aus, geben Sie *6* als Menge ein und wählen Sie *Monate* als die Periode aus.

1. Verwenden Sie den Bereich **Korrektes Feld** zum Aktualisieren der eigentlichen Planungsdaten. Wählen Sie im Feld **Feld** das zu ändernde Kriterium aus. Geben Sie im Feld **Faktor** einen Multiplikator für das ausgewählte Kriterium ein, oder geben Sie eine Additions- oder Subtraktionskonstante ein. Wählen Sie zum Beispiel *Menge* als Kriterium und geben Sie einen Faktor von *1,5* ein, um die Artikelmenge mit 1,5 zu multiplizieren. Geben Sie alternativ eine Konstante *-25* ein, um die Artikelmenge um 25 Einheiten zu verringern.
1. Verwenden Sie den Abschnitt **Finanzdimensionen**, um die Finanzdimensionen von Planungspositionen zu aktualisieren. Wählen Sie die Finanzdimensionen aus, die Sie ändern möchten, und geben Sie dann einen Wert ein, der auf die ausgewählten Dimensionen angewendet werden soll.
1. Wählen Sie **OK**, um Ihre Änderungen zu übernehmen.

## <a name="use-forecasts-with-master-planning"></a>Prognosen mit der Produktprogrammplanung verwenden

Nachdem Sie Ihre Bedarfsprognose und/oder Vorratsprognose eingegeben haben, können Sie die Prognosen während der Masterplanung einbeziehen, um den erwarteten Bedarf und/oder Vorrat in Ihrem Masterplanungslauf zu berücksichtigen. Wenn Prognosen in die Produktprogrammplanung einbezogen werden, werden die Bruttobedarfe für Materialien und Kapazitäten berechnet und geplanter Aufträge generiert.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Festlegen eines Masterplans zur Einbeziehung einer Bestandsprognose

Um einen Masterplan so festzulegen, dass er eine Bestandsprognose enthält, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie einen bestehenden Plan aus, oder erstellen Sie einen neuen Plan.
1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Prognosemodell** - Wählen Sie das zu verwendende Prognosemodell. Dieses Modell wird berücksichtigt, wenn ein Versorgungsvorschlag für den aktuellen Masterplan erstellt wird.
    - **Bestandsprognose einbeziehen** – Legen Sie diese Option auf *Ja* fest, um die Bestandsprognose in den aktuellen Masterplan einzubeziehen. Wenn Sie sie auf *Nein* festlegen, werden Transaktionen der Versorgungsprognose nicht in den Masterplan aufgenommen.
    - **Bedarfsprognose einbeziehen** - Legen Sie diese Option auf *Ja* fest, um die Bedarfsplanung in den aktuellen Masterplan einzubeziehen. Wenn Sie sie auf *Nein* festlegen, werden die Transaktionen der Bedarfsplanung nicht in den Masterplan aufgenommen.
    - **Methode zur Reduzierung des Prognosebedarfs** - Wählen Sie die Methode, die zur Reduzierung des Prognosebedarfs verwendet werden soll. Weitere Informationen finden Sie unter [Schlüssel für Prognosereduzierung](planning-optimization/demand-forecast.md#reduction-keys).

1. Auf dem Inforegister **Zeiträume in Tagen** können Sie die folgenden Felder festlegen, um den Zeitraum festzulegen, in dem die Planung berücksichtigt wird:

    - **Prognoseplan** - Legen Sie diese Option auf *Ja* fest, um den Prognoseplan-Zeitzaun, der von den einzelnen Deckungsgruppen ausgeht, außer Kraft zu setzen. Legen Sie sie auf *Nein* fest, um die Werte aus den einzelnen Coverage-Gruppen für den aktuellen Masterplan zu verwenden.
    - **Prognosezeitraum** - Wenn Sie die Option **Prognoseplan** auf *Ja* festlegen, geben Sie die Anzahl der Tage (ab dem heutigen Datum) an, für die die Bedarfsplanung gelten soll.

    > [!IMPORTANT]
    > Die Option **Prognoseplan** wird bei der Planungsoptimierung noch nicht unterstützt.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Einen Masterplan ausführen, der eine Bestandsprognose enthält

Führen Sie die folgenden Schritte aus, um einen Masterplan auszuführen, der eine Bestandsprognose enthält.

1. Gehen Sie zu **Produktprogrammplanung \> Arbeitsbereiche \> Masterplanung**.
1. Geben Sie im Feld **Stammplan** den Masterplan ein oder wählen Sie ihn aus, den Sie im vorherigen Verfahren festgelegt haben.
1. Wählen Sie auf der Kachel **Stammplanung** die Option **Ausführen**.
1. Legen Sie in der Dialogbox **Produktprogrammplanung** die Option **Verarbeitungszeit verfolgen** auf *Ja* fest.
1. Geben Sie im Feld **Anzahl von Threads** eine Zahl ein.
1. Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.
1. Ein Standard-Dialogfeld für den Abfrage-Editor wird angezeigt. Markieren Sie auf der Registerkarte **Bereich** die Zeile, in der das Feld **Feld** auf *Elementnummer* festgelegt ist.
1. Wählen Sie im Feld **Kriterium** die Elementnummer aus, die in den Plan aufgenommen werden soll.
1. Wählen Sie **OK** aus.

Um die berechneten Anforderungen anzuzeigen, öffnen Sie die Seite **Bruttobedarf**. Beispiel: Wählen Sie auf der Seite **Freigegebene Produkte** im Aktionsbereich auf der Registerkarte **Plan** in der Gruppe **Bedarf** die Option **Bruttobedarf**.

Um die erzeugten Planaufträge anzuzeigen, gehen Sie zu **Masterplanung \> Allgemein \> Geplante Aufträge**, und wählen Sie den entsprechenden Prognoseplan aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Bedarfsplanung – Übersicht](introduction-demand-forecasting.md)
- [Einrichten einer Bedarfsplanung](demand-forecasting-setup.md)
- [Eine statistische Grundplanung generieren](generate-statistical-baseline-forecast.md)
- [Manuelle Anpassungen an der Grundplanung](manual-adjustments-baseline-forecast.md)
- [Produktprogrammplanung mit Bedarfsprognosen](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]