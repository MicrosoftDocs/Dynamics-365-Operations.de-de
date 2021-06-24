---
title: Ein Format zur Konsolidierung importieren
description: Dieses Thema beinhaltet detaillierte Informationen zum Importformat, das beim Konsolidieren von Finanzdaten mehrerer juristischer Personen verwendet wird.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 714c34dfcd109a442a4ecd741409dea5c4aade20
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216805"
---
# <a name="import-format-for-consolidation"></a>Ein Format zur Konsolidierung importieren

[!include [banner](../includes/banner.md)]

Dieses Thema beinhaltet detaillierte Informationen zum Importformat, das beim Konsolidieren von Finanzdaten mehrerer juristischer Personen verwendet wird. Das Importformat muss als Textdatei (.txt) gespeichert werden.

## <a name="import-format"></a>Importformat

In der folgenden Tabelle ist das Importformat aufgeführt, das Sie verwenden sollten, wenn Sie während eines Imports eine Konsolidierung durchführen.

| Datensatztabelle | Formate | Notizen |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Die Datensatztabelle</li><li>Die Hauptkonto-ID der Quelle</li><li>Die Hauptkontoposition</li><li>Der Hauptkontotyp</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Die Hauptkonto-ID</li><li>Das Buchungsdatum</li><li>Der Finanzzeitraumtyp (**0** = Eröffnung, **1** = Betrieb und **2** = Abschluss)</li><li>Die Buchungswährung</li><li>Belastung oder Gutschrift (**0** = Belastung und **1** = Gutschrift)</li><li>Die Buchungsebene</li><li>Buchungsbeträge</li><li>Leistung</li><li>Die lokale RecID (mehrdeutiger, eindeutiger int64-Wert für die Buchung)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Die Eintragsnummer (Budget-Kopfzeilen-Buchungsnummer)</li><li>Das Standard-Datum der Budget-Kopfzeile</li><li>Die Budgetmodell-ID</li><li>Budgettyp (**1** – Ursprüngliches Budget, **2** – Transfer, **3** – Revision, **4** – Belastung, **5** – Vorbelastung, **6** – Vortragsbudget, **7** – Projekt, **8** – Anlagevermögen, **9** – Bedarfsplanung, **10** – Beschaffungsplanung, **11** – Umlagen, **12** – Vorläufiges Budget.)</li><li>Das Datum der Position</li><li>Die Hauptkonto-ID für die Position</li><li>Der Währungscode für die Position</li><li>Der Betrag für die Position in der Buchungswährung</li><li>Der ganzzahlige Aufzählungswert für den Budgettyp für die Position (Ausgaben oder Umsatzerlös)</li></ul> |
| 4            | DEMF | RecordCompany ist die juristische Person der Quelle. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Hauptkontokennung</li><li>Transaktionsdatum</li><li>Der Finanzzeitraumtyp (0 Eröffnung, 1 Betrieb und 2 Abschluss)</li><li>Buchungswährung</li><li>Belastung oder Gutschrift (0 für Belastung und 1 für Gutschrift)</li><li>Buchungsebene</li><li>Transaktionsbetrag</li><li>Leistung</li><li>Lokale RecID (mehrdeutiger, eindeutiger int64-Wert für die Buchung)</li></ul>  |
| 6            | BusinessUnit, 1 Abteilung, 2 | Die Finanzdimensionsattribute, die in der Segmentreihenfolge definiert sind.<p>Sie können die Seite **Exportieren** nutzen, um zu überprüfen, wie die Attribute definiert sind.</p> |
| 7            | 002,1,658 | <ul><li>Der Finanzdimensionswert</li><li>Die Finanzdimension als Index, der in RecordDimensions bereitgestellt wird</li><li>Eine mehrdeutige, eindeutige Datensatz-ID, die der eindeutigen Datensatz-ID von RecordTrans oder RecordTrans2 zugeordnet ist</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensionswerte, die der Buchung aus RecordBudget zugeordnet sind</li><li>Die Finanzdimension als Index, der in RecordDimensions bereitgestellt wird</li><li>Eine mehrdeutige Positionsdatensatz-ID, die an der Reihenfolge der Buchungspositionen in der Datei ausgerichtet ist</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
