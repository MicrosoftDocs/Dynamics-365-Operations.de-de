---
title: Cashflowplanung
description: Dieses Thema bietet einen Überblick über den Cashflow-Planungsprozess. Es wird auch erklärt, wie Cashflow-Planung in andere Module im System integriert wird.
author: panolte
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4979a57c966f25dba62a944a4e44086e5f6aed28
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712536"
---
# <a name="cash-flow-forecasting"></a>Cashflowplanung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mit den Tools für die Cashflow-Planung können Sie kommenden Cashflow- und Währungsbedarf analysieren, damit Sie eine Vorkalkulation des künftigen Bargeldbedarfs des Unternehmens durchführen können. Um eine zuverlässige Cashflow-Planung zu erhalten, müssen Sie folgende Aufgaben vollständig ausführen:

- Ermitteln Sie alle Liquiditätskonten, und erstellen Sie eine entsprechende Liste. Liquiditätskonten sind die Unternehmenskonten für Bargeld oder bargeldähnliche Zahlungsmittel.
- Konfigurieren Sie das Verhalten der Buchungsplanungen, die die Liquiditätskonten des Unternehmens betreffen.

Nachdem Sie diese Aufgaben abgeschlossen haben, können Sie Planungen des Cashflow- und des bevorstehenden Währungsbedarfs berechnen und analysieren.

## <a name="cash-flow-forecasting-integration"></a>Cashflow-Planungsintegration

Cashflow-Planung kann in die Module "Hauptbuch", "Kreditoren", "Debitoren", "Budetierung" und "Lagerverwaltung" integriert werden. Der Planungsvorgang verwendet Buchungsinformationen, die in das System eingegeben werden, und der Berechnungsvorgang plant die erwarteten Bargeldauswirkungen jeder Buchung. Die folgenden Buchungsarten werden berücksichtigt, wenn der Cashflow berechnet wird:

- **Aufträge** – Aufträge, die noch nicht fakturiert wurden und die zu physischen oder wertmäßigen Umsätzen führen.
- **Freitextrechnungen** – Noch nicht gebuchte Freitextrechnungen, die zu finanziellen Verkäufen führen. 
- **Bestellungen** – Bestellungen, die noch nicht fakturiert wurden und die zu physischen oder wertmäßigen Umsätzen führen.
- **Debitoren** – Offene Debitorenbuchungen (Rechnungen, die noch nicht bezahlt wurden).
- **Kreditoren** – Offene Kreditorenbuchungen (Rechnungen, die noch nicht bezahlt wurden).
- **Sachkontobuchungen** – Buchungen, bei denen angegeben ist, dass künftig eine Buchung erfolgt.
- **Budgeterfassungseinträge** – Budgeterfassungseinträge, die für die Cashflow-Planung ausgewählt wurden.
- **Bedarfsplanung** – Bestandsplanungsmodellpositionen, die für die Cashflow-Planung ausgewählt wurden.
- **Beschaffungssplanung** – Bestandsplanungsmodellpositionen, die für die Cashflow-Planung ausgewählt wurden.
- **Externe Datenquelle** – Externe Daten, die mithilfe von Tabellenkalkulationsvorlagen in die Cashflow-Prognosen eingegeben oder importiert werden.
- **Projektplanungen** – Projektverwaltungs- und -verrechnungsplanungen unter Verwendung des Planungsmodells.
- **Cashflow-Zahlungen an die Umsatzsteuerbehörde** – Voraussichtliche Zahlungsbeträge und Zeitpunkte der Umsatzsteuerbehörde, die zu finanziellen Zahlungen führen. Aktivieren Sie die Funktion Cashflow-Zahlungen an die Umsatzsteuerbehörde.

## <a name="configuration"></a>Variante

Um den Cashflow-Planungsprozess zu konfigurieren, können Sie die Seite **Cashflow-Planungseinstellung** verwenden. Geben Sie auf dieser Seite die zu verfolgenden Liquiditätskonten und das Standardplanungsverhalten für jeden Bereich an.

### <a name="general-ledger"></a>Hauptbuch

Sie müssen zunächst die Liquiditätskonten definieren, die Sie durch die Cashflow-Planung nachverfolgen möchten. Normalerweise sind diese Liquiditätskonten Hauptkonten, die den Bankkonten zugeordnet sind, die Bargeld empfangen und auszahlen. Wählen Sie auf der Seite **Cashflow-Planungssetup** auf der Registerkarte **Hauptbuch** die Hauptkonten aus, die in die Planung einbezogen werden sollen. Wenn ein Bankkonto dem Hauptkonto auf der Seite **Bankkonto** zugeordnet wurde, wird dies im Feld **Bankkonto** angezeigt.

Sie können eine abhängige Cashflow-Planung für ein Hauptkonto mit Buchungen einrichten, die sich direkt auf die Buchungen eines anderen Hauptkontos beziehen. Jede Position, die Sie im Abschnitt **In den abhängigen Konten** hinzufügen, erstellt eine Cashflow-Planung in einem abhängigen Hauptkonto. Dieser Betrag ist ein Anteil des Cashflow-Betrags vom primären Hauptkonto, das Sie ausgewählt haben.

Legen Sie zuerst das Feld **Hauptkonto** auf das primäre Hauptkonto fest, in dem anfängliche Buchungen zu erwarten sind. Legen Sie das Feld **Abhängiges Hauptkonto** auf das Konto fest, das von der ersten Buchung im primären Hauptkonto beeinflusst wird. Legen Sie angemessene Werte für weitere Felder der Position fest. Sie können die Werte im Feld **Prozent** ändern, um die Auswirkung des primären Hauptkontos auf das abhängige Hauptkonto widerzuspiegeln. Für eine Umsatz- oder Einkaufsplanung muss ein Wert für **Zahlungsbedingungen** ausgewählt werden, der stellvertretend für den Großteil der Debitoren oder Kreditoren ist. Legen Sie das Feld **Buchungstyp** auf den erwarteten Buchungstyp fest, der der Cashflow-Planung zugeordnet ist.

### <a name="accounts-payable"></a>Kreditorenkonten

Sie können die Planung für Einkäufe berechnen, indem Sie die Optionen auf der Registerkarte **Kreditoren** der Seite **Cashflow-Planungssetup** verwenden. Bevor Sie Cashflow-Planung für Kreditoren konfigurieren können, müssen Sie die Zahlungsbedingungen, Kreditorengruppen und Kreditoren-Buchungsprofile konfigurieren.

Im Abschnitt **Standardwerte für Einkaufsplanung** können Sie die Standardeinkaufsverhalten für die Cashflow-Planung auswählen. Drei Felder bestimmen die Zeit der Bargeldauswirkung: **Zeit zwischen Lieferdatum und Rechnungsdatum**, **Zahlungsbedingungen** und **Zeit zwischen Rechnungsfälligkeitsdatum und Zahlungsdatum**. Die Planung verwendet die Standardeinstellung für das Feld **Zahlungsbedingungen** nur, wenn ein Wert nicht in der Buchung angegeben ist. Verwenden Sie Zahlungsbedingungen, um die typische Anzahl von Tagen für jeden Teil des Vorgangs zu beschreiben.

Das Feld **Liquiditätskonten für Zahlungen** gibt das Liquiditätskonto an, das am häufigsten für Zahlungen verwendet wird. Verwenden Sie das Feld **Prozentsatz des Betrags, der der Cashflowplanung zuzuordnen ist**, um anzugeben, ob ein Prozentsatz der Beträge bei der Planung verwendet werden soll. Lassen Sie dieses Feld leer, wenn die vollständigen Buchungsbeträge bei der Planung verwendet werden.

Sie können die standardmäßige Einstellung für das Feld **Zeit zwischen Rechnungsfälligkeitsdatum und Zahlungsdatum** für vorhandene Kreditorengruppen überschreiben. Die Planung verwendet den Standardwert aus dem **Standardwerte für Einkaufsplanung**-Abschnitt, es sei denn, dass ein anderer Wert für die Kreditorengruppe angegeben ist, die dem Kreditor der Buchung zugeordnet ist. Um den Standardwert zu überschrieben, wählen Sie eine Kreditorengruppe aus, und legen dann den neuen Wert für das Feld **Einkaufszeit** fest.

Sie können die standardmäßige Einstellung für das Feld **Liquiditätskonto** für bestimmte Kreditorenbuchungsprofile überschreiben. Die Planung verwendet den Standardwert aus dem **Standardwerte für Einkaufsplanung**-Abschnitt, es sei denn, dass ein anderes Liquiditätskonto für das Buchungsprofil angegeben ist, das dem Kreditor der Buchung zugeordnet ist. Um den Standardwert zu überschrieben, wählen Sie ein Buchungsprofil aus, und geben Sie anschließend das Liquiditätskonto an, das voraussichtlich betroffen ist.

### <a name="accounts-receivable"></a>Debitoren

Sie können die Planung für Verkäufe berechnen, indem Sie die Optionen auf der Registerkarte **Debitoren** der Seite **Cashflow-Planungssetup** verwenden. Bevor Sie Cashflow-Planung für Debitoren konfigurieren können, müssen Sie die Zahlungsbedingungen, Kundengruppen und Kunden-Buchungsprofile konfigurieren.

Im Abschnitt **Standardwerte für Verkaufsplanung** können Sie Standardverkaufsverhalten für die Cashflow-Planung auswählen. Drei Felder bestimmen die Zeit der Bargeldauswirkung: **Zeit zwischen Lieferdatum und Rechnungsdatum**, **Zahlungsbedingungen** und **Zeit zwischen Rechnungsfälligkeitsdatum und Zahlungsdatum**. Die Planung verwendet die Standardeinstellung für das Feld **Zahlungsbedingungen** nur, wenn ein Wert nicht in der Buchung angegeben ist. Verwenden Sie Zahlungsbedingungen, um die typische Anzahl von Tagen für jeden Teil des Vorgangs zu beschreiben. 

Das Feld **Liquiditätskonten für Zahlungen** gibt das Liquiditätskonto an, das am häufigsten für Zahlungen verwendet wird. Verwenden Sie das Feld **Prozentsatz des Betrags, der der Cashflowplanung zuzuordnen ist**, um anzugeben, ob ein Prozentsatz der Beträge bei der Planung verwendet werden soll. Lassen Sie dieses Feld leer, wenn die vollständigen Buchungsbeträge bei der Planung verwendet werden.

Sie können die standardmäßige Einstellung für das Feld **Zeit zwischen Rechnungsfälligkeitsdatum und Zahlungsdatum** für vorhandene Kundengruppen überschreiben. Die Planung verwendet den Standardwert aus dem **Standardwerte für Verkaufsplanung**-Abschnitt, es sei denn, dass ein anderer Wert für die Kundengruppe angegeben ist, die dem Kunden der Buchung zugeordnet ist. Um den Standardwert zu überschrieben, wählen Sie eine Kundengruppe aus, und legen dann den neuen Wert für das Feld **Verkaufszeit** fest.

Sie können die standardmäßige Einstellung für das Feld **Liquiditätskonto** für bestimmte Kundenbuchungsprofile überschreiben. Die Planung verwendet den Standardwert aus dem **Standardwerte für Verkaufsplanung**-Abschnitt, es sei denn, dass ein anderes Liquiditätskonto für das Buchungsprofil angegeben ist, das dem Kunden der Buchung zugeordnet ist. Um den Standardwert zu überschrieben, wählen Sie ein Buchungsprofil aus, und legen Sie anschließend das Liquiditätskonto an, das voraussichtlich betroffen ist.

### <a name="budgeting"></a>Budgetierung

Budgets, die aus den Budgetmodellen erstelllt werden, können in Cashflowplanungen einbezogen werden. Wählen Sie auf der Registerkarte **Budgetierung** der Seite **Cashflowplanungseinstellung** die Budgetmodelle aus, die in die Planung einbezogen werden sollen. Standardmäßig werden neue Budgetregistereinträge in der Planungen einbezogen, nachdem das Budgetmodell für Cashflowplanung aktiviert wurde.

Budgetregistereinträge können durch Personalisierung individuell in die Cashflow-Prognose einbezogen werden. Wenn Sie der Seite **Budgetregistereintrag** die Spalte „In Cashflow-Prognosen einbeziehen“ hinzufügen, überschreibt das System die Einstellungen auf der Seit **Cashflow-Planungssetup**, um einen individuellen Budgetregistereintrag in die Prognose aufzunehmen.


### <a name="inventory-management"></a>Lagerverwaltung

Bestandslieferungs- und Bedarfsplanung kann in die Cashflowplanung einbezogen werden. Auf der Registerkarte **Bestandverwaltung** der Seite **Cashflow-Planungssetup** wählen Sie das Planungsmodell aus, das in die Caschflow-Planung einbezogen werden sollen. Das Einbeziehen in der Cashflow-Planung kann für einzelne Lieferungs- und Bedarfsplanungspositionen überschrieben werden.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Einrichten von Dimensionen für die Cashflow-Planung
Auf der neuen Registerkarte auf der Seite  **Einrichtung der Cashflow-Planung**  können Sie steuern, welche Finanzdimensionen für die Filterung im Arbeitsbereich  **Cashflow-Planung**  verwendet werden sollen. Diese Registerkarte wird nur angezeigt, wenn die Cashflow-Planungsfunktion aktiviert ist.

Wählen Sie auf der Registerkarte **Dimensionen** aus der Liste der zur Filterung verwendeten Dimensionen aus und verschieben Sie sie mit den Pfeiltasten in die rechte Spalte. Zum Filtern von Cashflow-Planungsdaten können nur zwei Dimensionen ausgewählt werden. 

### <a name="setting-up-external-source"></a>Externe Quelle einrichten
Externe Daten können in die Cashflowplanung eingegeben oder importiert werden, wenn Finance Insights konfiguriert wurde. Bevor externe Daten eingegeben oder importiert werden, müssen externe Quellen eingerichtet werden. Richten Sie auf der Registerkarte **Externe Quelle** externe Cashflow-Kategorien ein. Eine Kategorie kann **ausgehend** oder **eingehend** sein. **Liquidität** sollte als Buchungsart gewählt werden. Wählen Sie im Raster **Einstellungen juristische Person** wählen Sie die juristischen Personen und die entsprechenden Hauptkonten aus, für die die externen Cashflow-Kategorien gelten.

Weitere Informationen finden Sie unter [Externe Daten in Cashflowplanungen](../../finance/finance-insights/external-data-in-cash-flow.md). 

### <a name="project-management-and-accounting"></a>Projektverwaltung und -buchhaltung

In Version 10.0.17 ermöglicht eine neue Funktion die Integration in die Projektverwaltung und -verrechnung sowie in die Cashflow-Planung. In dem **Funktionsverwaltung**-Arbeitsbereich schalten Sie die **Cashflow-Projektplanung**-Funktion zur Einbeziehung der prognostizierten Kosten und Einnahmen in die Cashflow-Planung ein. Auf der Registerkarte **Projektverwaltung und -verrechnung** der Seite **Cashflow-Planungssetup** wählen Sie die Projekttypen und Transaktionstypen aus, die in die Cashflow-Planung aufgenommen werden sollen. Wählen Sie dann das Projektplanungsmodell aus. Ein Submodell vom Reduktionstyp funktioniert am besten. Die Liquiditätskonten, die in der Debitorenkonfiguration eingegeben wurden, werden als Standardliquiditätskonten verwendet. Daher müssen Sie beim Einrichten der Cashflow-Planung keine Standard-Liquiditätskonten eingeben. Es kann auch ein Budgetmodell verwendet werden, es kann jedoch nur ein Typ auf der Seite **Cashflow-Planungssetup** für Projektverwaltung und -verrechnung ausgewählt werden. Ein Planungsmodell bietet die größte Flexibilität, wenn Projektverwaltung und -verrechnung oder Project Operations verwendet werden.

Nachdem die Funktion zur Cashflow-Projektplanung aktiviert wurde, kann die Cashflow-Planung für jedes Projekt auf der Seite **Alle Projekte** angezeigt werden. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Plan** in der Gruppe **Planung** die Option **Cashflow-Planung** aus. In den **Bargeldübersicht**-Arbeitsbereichen (siehe den Abschnitt [Berichterstattung](#reporting) weiter unten in diesem Thema) zeigt der Projektplanungs-Transaktionstyp die Zuflüsse (Projektplanungseinnahmen) und die Abflüsse (Projektplanungskosten) an. Die Beträge können nur einbezogen werden, wenn das **Projektphase**-Feld in den **Bargeldübersicht**-Arbeitsbereichen auf **In Bearbeitung** eingestellt ist.

Projekttransaktionen werden weiterhin auf verschiedene Weise in die Cashflow-Planungen einbezogen, unabhängig davon, ob die **Cashflow-Projektplanung**-Funktion aktiviert ist. Gebuchte Projektrechnungen werden in der Planung als Teil der offenen Debitorenbuchungen einbezogen. Durch das Projekt initiierte Aufträge und Bestellungen sind bei der Kapazitätsplanung für offene Aufträge enthalten, nachdem diese in das System eingegeben wurden. Projektplanung kann auch in ein Sachkontobudgetmodell übertragen werden. Dieses Sachkontobudgetmodell ist dann in der Cashflow-Planung als Teil der Budgetregistereinträge enthalten. Wenn Sie die Funktion **Cashflow-Projektplanung** eingeschaltet haben, übertragen Sie keine Projektplanungen in ein Sachkontobudgetmodell, da diese Aktion dazu führt, dass die Projektplanungen zweimal gezählt werden.

### <a name="sales-tax-authority-payments"></a>Mehrwertsteuerzahlungen an autoritative Stelle 

Die Funktion Cashflow-Mehrwertsteuerzahlungen an die Behörde prognostiziert die Auswirkungen von Mehrwertsteuerzahlungen auf den Cashflow. Es verwendet unbezahlte Umsatzsteuertransaktionen, Steuerabrechnungszeiträume und die Zahlungsfrist des Steuerzeitraums, um das Datum und die Höhe von Cashflow-Zahlungen vorherzusagen. 

### <a name="calculation"></a>Berechnung

Bevor Sie Cashflowplanungsanalyse anzeigen können, muss der Cashflow-Berechnungsprozess ausgeführt werden. Der Berechnungsprozess projiziert die künftigen Bargeldauswirkungen von Buchungen, die eingegeben wurden.

Berechnen Sie die Cashflowplanung, indem Sie die Seite **Cashflowplanungen berechnen** verwenden. Sie können entweder die gesamte Cashflowplanung oder eine sich erhöhende Cashflowplanung berechnen. 

- Um alle Cashflow-Planungsbuchungen zu löschen und neu zu berechnen, legen Sie das Feld **Berechnungsmethode für Cashflowplanungen** auf **Summe** fest. Es wird empfohlen, diesen Ansatz zu verwenden, wenn Sie die Cashflowplanung schon längere Zeit nicht mehr aktualisiert haben. 
- Um die vorhandenen Cashflowinformationen nur für neue Buchungen zu aktualisieren, legen Sie das Feld **Berechnungsmethode für Cashflowplanungen** auf **Neu** fest. Die Seite wird das Datum anzeigen, an dem die Cashflowberechnung zuletzt ausgeführt wurde.

Sie können auch die Stapelverarbeitung für die Cashflowplanung verwenden. Zur Sicherstellung, dass Ihre Planungsanalyse regelmäßig aktualisiert wird, richten Sie eine sich wiederholende Stapelverarbeitung für die Cashflowplanungsberechnung ein.

In Version 10.0.13 wurde eine Erweiterung des Berechnungsprozesses veröffentlicht, die das Framework für die Prozessautomatisierung verwendet, um die Cashflowberechnung zu planen. Dies wird mit der Funktion **Automatisierung der Cashflowplanung** im Arbeitsbereich **Funktionsverwaltung** aktiviert. Wählen Sie nach der Aktivierung den Link **Automatisierung der Cashflowplanung**, um die neue Automatisierungsseite aufzurufen, auf der Sie den Cashflowberechnungsprozess planen können. Um einen neuen Zeitplan für die Cashflowplanung zu erstellen, gehen Sie auf **Neue Prozessautomatisierung erstellen** und dann auf **Automatisierung der Cashflowplanung** im Drop-down-Menü **Zeitplantyp**. Sie müssen für jedes Unternehmen, für das Sie die Cashflowplanungsdaten aktualisieren, einen Zeitplan festlegen.  Auf dieser Seite wird auch angezeigt, welche Automatisierungsaufträge für die Cashflowplanung ausstehen und wann der letzte Auftrag abgeschlossen wurde.  

> [!NOTE] 
> Wenn bereits vorhandene Stapelverarbeitungsaufträge für Cashflowplanungen geplant sind, wird eine Fehlermeldung angezeigt, und Sie können diese Funktion nicht aktivieren. Bestehende Stapelverarbeitungsaufträge müssen gelöscht werden, bevor Sie diese Funktion aktivieren können. 

Weitere Informationen finden Sie unter [Prozessautomatisierung](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Bericht

Nachdem die Cashflowplanung berechnet wurde, müssen Sie die entsprechenden Entitätsinformationen für analytische Berichterstellung aktualisieren. Auf der Seite **Entitätsspeicher** wählen Sie die Messung **LedgerCovLiquidityMeasurement-Aggregat** aus und klicken dann auf **Aktualisieren**.

Es gibt zwei Arbeitsbereiche, die Cashflowplanungsdaten enthalten. Ein Arbeitsbereich enthält Daten für alle Unternehmen, und ein anderer Arbeitsbereich nur Daten für das aktuelle Unternehmen.

Zugriff auf den Arbeitsbereich für alle Unternehmen wird über die Aufgabe **Cashflow-Arbeitsbereich für alle Unternehmen anzeigen** gesteuert. Standardmäßig ist der Arbeitsbereich **Bargeldüberblick – alle Unternehmen** für folgende Rollen verfügbar:

- Leitender Geschäftsführer
- Leiter Finanzabteilung
- Financial Controller

Zugriff auf den Arbeitsbereich für das aktuelle Unternehmen wird über die Arbeitsbereichsaufgabe **Cashflow-Arbeitsbereich für das aktuelle Unternehmen anzeigen** gesteuert. Standardmäßig ist der Arbeitsbereich **Bargeldüberblick – aktuelles Unternehmen** für folgende Rollen verfügbar:

- Sachbearbeiter Buchhaltung
- Leiter Buchhaltung
- Supervisor Buchhaltung
- Leiter Kreditorenkonten
- Leiter Debitorenkonten

Der Arbeitsbereich **Bargeldüberblick – alle Unternehmen** zeigt die Cashflowplanungsanalyse in der Systemwährung an. Die Systemwährung und der Systemwechselkurstyp, die zur Analyse verwendet werden, werden auf der Seite **Systemparameter** definiert. Der Arbeitsbereich zeigt einen Überblick der Cashflowplanung und Bankkontosalden für alle Unternehmen an. Ein Diagramm aus Barzu- und -ausflüssen bietet eine Übersicht der künftigen Geldbewegungen und Salden in der Systemwährung, zusammen mit detaillierten Informationen zu den Planungsbuchungen. Sie können auch die folgenden Währungssalden sehen.

Der Arbeitsbereich **Bargeldüberblick – aktuelles Unternehmen** zeigt Cashflowplanungsanalysen in der definierten Buchhaltungswährung des Unternehmens. Die Buchhaltungswährung, die zur Analyse verwendet wird, wird auf der Seite **Sachkonto** definiert. Der Arbeitsbereich zeigt einen Überblick der Cashflowplanung und Bankkontosalden für das aktuelle Unternehmen an. Ein Diagramm aus Barzu- und -ausflüssen bietet eine Übersicht der künftigen Geldbewegungen und Salden in der Buchhaltungswährung, zusammen mit detaillierten Informationen zu den Planungsbuchungen. Sie können auch die folgenden Währungssalden sehen.

Weitere Informationen zur Cashflowplanungsanalyse finden Sie unter [Power BI-Inhalt – Bargeldübersicht](Cash-Overview-Power-BI-content.md).

Darüber hinaus können Sie Cashflowplanungsdaten für bestimmte Konten, Aufträge und Artikel auf den folgenden Seiten anzeigen:

- **Zwischenbilanz**: Wählen Sie **Cashflow-Planungen** aus, um die künftigen Cashflows für das ausgewählte Hauptkonto anzuzeigen.
- **Alle Aufträge**: Auf der Registerkarte **Rechnung** wählen Sie **Cashflow-Planungen** aus, um die geplante Bargeldauswirkung des ausgewählten Auftrags anzuzeigen.
- **Alle Bestellungen**: Auf der Registerkarte **Rechnung** wählen Sie **Cashflow-Planungen** aus, um die geplante Bargeldauswirkung der ausgewählten Bestellung anzuzeigen.
- **Beschaffungsplanung**: Wählen Sie **Cashflow-Planungen** aus, um die künftigen Cashflows anzuzeigen, die der ausgewählten Artikelbeschaffungsplanung zugeordnet werden.
- **Bedarfsplanung**: Wählen Sie **Cashflow-Planungen** aus, um die künftigen Cashflows anzuzeigen, die der ausgewählten Artikelbedarfsplanung zugeordnet werden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
