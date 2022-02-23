---
title: Lohn auf Basis von Erfassungen
description: In diesem Thema wird erläutert, wie Lohn auf der Grundlage der Erfassungen von Arbeitskräften berechnet wird.
author: johanhoffmann
manager: tfehr
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 98ca6f7713b2f605a49a97d391fb8485bea78c4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966379"
---
# <a name="pay-based-on-registrations"></a>Lohn auf Basis von Erfassungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird im Detail erläutert, wie Lohn auf der Grundlage der Erfassungen von Arbeitskräften berechnet wird. Zudem enthält es Beispiele, die zeigen, wie die verschiedenen Kombinationen von Einrichtungsoptionen angezeigt werden, die für die Berechnung des Ergebnisses verfügbar sind. Nachfolgend sind einige der Bereiche, die erfasst sind:

- Gleitzeit
- Überstunden
- Pausen
- Wechselcodes
- Lohnelemente
- Lohnvereinbarungen
- Zeit- und Anwesenheitsberechnungsparameter
- Abwesenheit

## <a name="the-use-of-flex-time"></a>Die Verwendung von Gleitzeit

Perioden der Gleitzeit werden in den Zeitprofilen eingerichtet, die in "Zeit und Anwesenheit" verwendet werden. Es gibt zwei Gleitzeitprofiltypen: **Gleitzeit+** und **Gleitzeit-**. Wenn eine Arbeitskraft Zeit in einer „Gleitzeit+”-Periode erfasst, wird das Gleitzeitsaldo der Arbeitskraft um die Stunden erhöht, die gearbeitet wurden. Die Arbeitskraft erhält keine Vergütung für die Stunden, die während der „Gleitzeit+”-Periode gearbeitet wurden. Allerdings kann die Arbeitskraft während der Flexperioden frei machen und dies mit den Stunden von seinem Gleitzeitsaldo ausgleichen. Deshalb wird Freizeit während der Gleitzeitperioden vom System als Abwesenheit betrachtet.

## <a name="scenarios-based-on-flex-periods"></a>Szenarien auf Grundlage von Gleitzeitperioden

Die beiden Szenarien, die folgen, basieren auf einem Gleitzeitprofil, das einem Arbeitstag entspricht. Bei beiden Szenarien wird entsprechend der Gleitzeitperiode Lohn berechnet, in der die Arbeitskraft ein- und ausstempelt.

### <a name="flex-profile-for-one-workday"></a>Gleitzeitprofil für einen Arbeitstag

| Profiltyp  | Start    | Beenden      | Tag     |
|---------------|----------|----------|---------|
| Überstunden     | 00:00 (vormittags) | 06:00 (vormittags) | Montag  |
| Gleitzeit+         | 06:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Einstempeln      | 07:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Standardzeit | 07:00 (vormittags) | 02:30 (nachmittags) | Montag  |
| Gleitzeit-         | 02:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Ausstempeln     | 03:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Überstunden     | 03:30 (nachmittags) | 06:00 (vormittags) | Dienstag |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Szenario 1: Eine Arbeitskraft erfasst das Einstempeln während einer „Gleitzeit+”-Periode und das Ausstempeln während einer „Gleitzeit-”-Periode

Die Erfassungen der Arbeitskraft für den Tag sehen so aus.

| Journalerfassungstyp | Start    | Beenden      |
|---------------------------|----------|----------|
| Einstempeln                  | 06:30 (vormittags) | 06:30 (vormittags) |
| Produktionseinzelvorgang            | 06:30 (vormittags) | 02:45 (nachmittags) |
| Ausstempeln                 | 02:45 (nachmittags) | 02:45 (nachmittags) |

Die Erfassungen der Arbeitskraft für den Tag werden berechnet und auf der Seite **Genehmigen** zum Lohn übertragen (**Zeit und Anwesenheit** &gt; **Überprüfen und genehmigen** &gt; **Genehmigen**). Nachdem die Erfassungen berechnet wurden, kann das Ergebnis der Berechnung auf der Registerkarte **Zeiten** angezeigt werden. 

Um dieses Szenario zu verstehen, sehen Sie sich die folgenden Felder an.

| Gleitzeit+ | Gleitzeit- | Zeit | Entlohnte Zeit |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8.25 | 8.50     |

#### <a name="calculation-of-flex"></a>Flex + berechnen

Entsprechend dem Gleitzeitprofil ist die Zeitspanne zwischen 06:00 bis 07:00 eine Flex+-Periode. Wenn die Arbeitskraft daher um 06:30 Uhr einstempelt, erhält er 0,5 Stunden. Diese Zeitmenge wird dem Gleitzeitkonto der Arbeitskraft hinzugefügt.

#### <a name="calculation-of-flex-"></a>Flex - berechnen

Entsprechend dem Gleitzeitprofil beginnt die Flexperiode um 02:30 Uhr und um.03:30 Uhr. Wenn daher die Arbeitskraft um 14:45 Uhr ausstempelt, werden die 45 Minuten (0,75 Stunden), die in der „Gleitzeit-”-Periode liegen als Lohnzeit erfasst, und dieselbe Zeitmenge wird vom Gleitzeitkonto der Arbeitskraft abgezogen. Die 45 Minuten sind in der entlohnten Zeit enthalten, da der Arbeitskraft Lohn für die restlichen 45 Minuten in der „Gleitzeit-”-Periode gewährt wird. Wenn die Arbeitskraft während der Flexperiode abwesend ist, werden die 45 Minuten aus dem Gleitzeitkonto abgezogen werden.

#### <a name="calculation-of-time"></a>Berechnung der Zeit

Zeit wird als die Zeit zwischen dem Ein- und Ausstempeln berechnet, das heißt 06:30 Uhr bis 14:45 Uhr, was 8,25 Stunden entspricht.

#### <a name="calculation-of-pay-time"></a>Berechnung der bezahlten Zeit

Die entlohnte Zeit ist die Zeitspanne, für die einer Arbeitskraft Lohn gewährt wird. In diesem Szenario ist die Arbeitskraft während 8,25 Stunden am Arbeitsplatz (**Zeit**). Allerdings wird **Entlohnte Zeit** als 8.50 Stunden berechnet, da der Arbeitskraft Lohn für die Flexperiode gewährt wird, nachdem diese ausstempelte. Die entlohnte Zeit entspricht den Arbeitsstunden des geplanter Arbeit, da Flex+-Zeit dem Gleitzeitkonto der Arbeitskraft hinzugefügt wird, nicht der entlohnten Zeit. Die Abwesenheitszeit während der „Gleitzeit-”-Periode wird zum Entlohnungszeitpunkt vergütet und vom Gleitzeitkonto der Arbeitskraft abgezogen.

| Zeit              | Registrierungstyp | Bezahlte Zeit «(Stunden)      |
|-------------------|-------------------|-----------------------|
| 06:30 Uhr - 07:00 Uhr | Gleitzeit+             | 0                     |
| 07:00 – 14:45 Uhr | Standardzeit     | 7.75                  |
| 14:45 – 15:30 Uhr | Gleitzeit-             | 0.75 (Abwesenheitsperiode) |
|                   | Summe             | 8.50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Szenario 2: Eine Arbeitskraft arbeitet während der gesamten „Gleitzeit-”-Periode und leistet auch Überstunden

Die Erfassungen der Arbeitskraft für den Tag sehen so aus.

| Journalerfassungstyp | Start    | Beenden      |
|---------------------------|----------|----------|
| Einstempeln                  | 06:30 (vormittags) | 06:30 (vormittags) |
| Produktionseinzelvorgang            | 06:30 (vormittags) | 05:00 (nachmittags) |
| Ausstempeln                 | 05:00 (nachmittags) | 05:00 (nachmittags) |

Nachdem Sie die Journal-Erfassungen der Seite auf **Genehmigen** berechnet haben, können Sie die Berechnungsauswirkung auf den **Zeiten** anzeigen. Um dieses Szenarios zu veranschaulichen, gehen Sie zu folgenden Felder.

| Gleitzeit+ | Gleitzeit- | Zeit  | Entlohnte Zeit | Entlohnte Überstundenzeit |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 1.50         |

#### <a name="calculation-of-flex"></a>Flex + berechnen

Entsprechend dem Gleitzeitprofil ist die Zeitspanne zwischen 06:00 bis 07:00 eine Flex+-Periode. Wenn daher die Arbeitskraft um 06:30 Uhr einstempelt, verdient sie 0,5 Stunden „Gleitzeit+”-Zeit in ihrem Gleitzeitsaldo.

#### <a name="calculation-of-flex-"></a>Flex - berechnen

Weil die Arbeitskraft während der Flexperiode arbeitet, wird die Flexperioade nicht berechnet. "Gleitzeit-" wird nur berechnet, wenn die Arbeitskraft während der Flexperiode abwesend ist. Klicken Sie in einer Zahlungsperspektive, wenn die Arbeitskraft während der Flexperiode arbeitet, wird ihr der Lohnsatz gewährt, der für Standardzeit definiert wird. Wenn die Arbeitskraft während der Flexperiode abwesend ist, werdebn die 45 Minuten aus dem Gleitzeitkonto abgezogen werden.

#### <a name="calculation-of-time"></a>Berechnung der Zeit

Zeit wird als die Zeit zwischen dem Einstempeln um 06:30 Uhr und dem Ausstempeln um 17:00 Uhr, oder 15,5 Stunden, berechnet.

#### <a name="calculation-of-pay-time"></a>Berechnung der bezahlten Zeit

In diesem Szenario ist die Arbeitskraft während 10,50 Stunden am Arbeitsplatz (**Zeit**). Allerdings wird **Entlohnte Zeit** als 10.00 Stunden berechnet, da die Arbeitskraft kein Lohn für die Flex+-Periode erhält.

#### <a name="calculation-of-pay-overtime"></a>Berechnung der Überstunden

| Zeit               | Registrierungstyp | Bezahlte Zeit «(Stunden) |
|--------------------|-------------------|------------------|
| 06:30 Uhr - 07:00 Uhr  | Gleitzeit+             | 0                |
| 07:00 – 14:30 Uhr  | Standardzeit     | 7.50             |
| 14:30 – 15:30 Uhr  | Gleitzeit-             | 1,00             |
| 15:30 – 17:00 Uhr | Überstunden          | 1.50             |
|                    | Summe             | 10.00            |

### <a name="generation-of-pay-items"></a>Generierung von Lohnaufstellungen

Erfassungen von Arbeitskräften für den Tag können von der Seite **Approve** übertragen werden. Wenn die Erfassungen übertragen werden, werden folgende Lohnelemente generiert. Lohnelemente ermöglichen eine Aufschlüsselung der entlohnten Standardzeit, Überstunden, entlohnte Pausenzeit, usw.

Um die Liste der Lohnartikel zu öffnen, wählen Sie **Zeit und Anwesenheit** &gt; **Prüfen und Genehmigen** &gt; **Genehmigen** aus. Wählen Sie dann **Abfrage** &gt; **Übertragene Erfassungen** aus.

Die Lohnelemente sind die Grundlage für den Lohn einer Arbeitskraft. Sie können eine Datei generieren, die die Informationen aus den Lohnartikeln enthält, und diese Datei in ein Lohnabrechnungssystem übertragen.

Im Rahmen der Übertragung werden Uhrzeit und Kosten aus der Produktion als auch Projektaktivitäten zu der Projekterfassung übertragen, um die Zeit- und Kostenausgabe abzulegen. Die übertragenen Erfassungen sind die Grundlage für Zeit und Einstandspreis pro Stunde für Produktionsaufträge und Projekte. Sie können die übertragenen Erfassungen öffnen, indem Sie das Menü **Abfrage** auf die Seite **Genehmigen** verwenden.

Beispiel für Szenario 2 werden folgende Lohnelement generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz  | Gesamtkosten |
|---------------|----------|-----------|-------|------------|
| Standardzeit | 1201     | 10.0      | 10    | 100        |
| Überstunden      | 1301     | 1.50      | 5     | 7.50       |
|               |          |           | Summe | 107.50     |

Das Lohnelement für Standardzeit hat eine Lohneinheit von 10 Stunden, die die Standardzeit, die „Gleitzeit-”-Zeit sowie Überstunden abdeckt. Standardzeit, „Gleitzeit-”-Zeit und Überstunden werden in einem Lohnelement zusammengeführt, da alle Typen als Standardzeit berechnet werden, basierend auf der Standardeinstellung eines Parameters auf der Seite **Berechnungsparameter** (**Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Berechnungsparameter**). Die Überstunden werden zuzüglich zur Standardzeit berechnet, indem ein zusätzlicher Satz von 5 verwendet wird.

Wenn Sie klar unterscheiden möchten zwischen Standardzeit und Überstunden, sodass die Lohneinheiten für die Lohn nur die Ausgabe der tatsächlichen Zeit für Standardzeit und Überstunden betreffen, müssen die Lohneinheiten für Standardzeit als 8,50 berechnet werden, und die Lohneinheiten für Überstunden müssen als 1,50 berechnet werden.

Um das System so zu konfigurieren, das deutlich zwischen Standardzeit und Überstunden unterschieden wird, müssen Sie Überstunden von der Standardzeit ausschließen. Sie müssen auch die Einstellungen der Lohnart für Überstunden ändern, sodass der Lohnsatz für Überstunden alle Zahlungen für die Stunden abdeckt, die für Überstunden aufgewendet wurden.

### <a name="exclude-overtime-from-the-standard-time"></a>Ausschließen von Überstunden aus der Standardzeit

Wählen Sie auf der Seite **Berechnungsparameter** **Überstunden** als Profil-Spezifikationstyp aus, und legen Sie die Option **Entlohnte Zeit** auf **Nein** fest, wie hier angezeigt.

| Erfassungs-Spezifikation | Profilspezifikationstyp | Herstellkostenkalkulation   |     | Entlohnt         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Arbeitszeit       | Überstunden                   | Standardzeit | Ja | Entlohnte Zeit     | Nr.  |
|                    |                            | Entlohnte Zeit      | Ja | Entlohnte Überstundenzeit | Ja |

Nachdem Sie die Berechnungsparameter anpassen, werden folgende Lohnelement generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz  | Gesamtkosten |
|---------------|----------|-----------|-------|------------|
| Standardzeit | 1201     | 8.50      | 10    | 85.0       |
| Überstunden      | 1301     | 1.50      | 15    | 22.50      |
|               |          |           | Summe | 107.50     |

> [!NOTE]
> Die Berechnungsparameter haben eine empfohlene Standardeinstellung. Im Allgemeinen sollten Sie vorsichtig sein, wenn Sie in diese Parameter ändern. Um die empfohlenen Standardeinstellungen wiederherzustellen, wählen Sie auf der Seite **Berechnungsparameter** die Option **Werte wiederherstellen** aus.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Ermöglichen Sie Abweichungen von den Standardlohnprofilen

Auf der Seite **Profile** (**Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Zeitprofile** &gt; **Profile**), können Sie die Profiltypen, einrichten Wechselcodes und Pausen enthalten.

### <a name="switch-codes"></a>Wechselcodes

Sie können Wechselcodes verwenden, um es Arbeitskräfte zu ermöglichen, von ihrem Profiltyp abzuweichen, indem ein anderer Profiltyp geändert wird. So können Sie beispielsweise eine Arbeitskraft zur Änderung von Flex+-Zeit nach Überstunden ermöglichen. Eine Arbeitskraft kann ein Wechselcode für die Erfassung hinzufügen, oder Sie können die Aufgabe des Hinzufügens eines Wechselcodes dem Genehmiger der Erfassungen zuweisen.

Bevor ein Wechselcode verwendet werden kann, müssen Sie diesen als Artikeltyp für indirekte Aktivität bezeichnen. Sie müssen dann den Wechselcode dem Zeitprofil für die Periode hinzufügen, in der Sie eine Änderung des Profiltyps zulassen möchten. So führen Sie die folgenden Schritte aus, um den Wechselcode zu erstellen, der die Flex+-Periode von 06:00 auf 07:00 auf Überstunden ändert.

1. Erstellen Sie einen Wechselcode, mit der Bezeichnung **OTBCI (Flexzeit zu Überstunden vor dem Einstempeln konvertieren )**. Wählen Sie **Zeit und Anwesenheit** &gt; **Verwalten indirekter Aktivitäten** &gt; **Indirekte Aktivitäten** aus.
2. In der Spalte **Wechselcode** fügen Sie OTBCI der Flex+-Position im Zeitprofil hinzu.
3. In der Spalte **Sekundär** fügen Sie den Profiltyp **Überstunden** hinzu.

Berücksichtigen Sie folgendes Flex-Profil für den Arbeitstag.

| Profiltyp  | Start    | Beenden      | Tag     |
|---------------|----------|----------|---------|
| Überstunden     | 00:00 (vormittags) | 06:00 (vormittags) | Montag  |
| Gleitzeit+         | 06:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Einstempeln      | 07:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Standardzeit | 07:00 (vormittags) | 02:30 (nachmittags) | Montag  |
| Gleitzeit-         | 02:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Ausstempeln     | 03:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Überstunden     | 03:30 (nachmittags) | 06:00 (vormittags) | Dienstag |

Hier sind Erfassungen der Arbeitskraft an diesem Tag.

| Journalerfassungstyp | Start    | Beenden      |
|---------------------------|----------|----------|
| Einstempeln                  | 06:30 (vormittags) | 06:30 (vormittags) |
| Produktionseinzelvorgang            | 06:30 (vormittags) | 02:45 (nachmittags) |
| Ausstempeln                 | 05:00 (nachmittags) | 05:00 (nachmittags) |

Die folgenden Lohnelemente werden nach der Übertragung generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz  | Gesamtkosten |
|---------------|----------|-----------|-------|------------|
| Standardzeit | 1201     | 8.50      | 10    | 85.0       |
| Überstunden      | 1305     | 1.50      | 15    | 22.50      |
|               |          |           | Summe | 107.50     |

Auf der Seite **Genehmigen** können Sie die Übertragung rückgängig machen und dann **Wechselcode** verwenden, um den **OTBCI** Wechselcode zu übernehmen. Wenn Sie die Erfassungen ein zweites Mal übertragen, werden die folgenden Lohnelemente generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz  | Gesamtkosten |
|---------------|----------|-----------|-------|------------|
| Standardzeit | 1201     | 8.50      | 10    | 80.0       |
| Überstunden      | 1305     | 2.00      | 15    | 30.0       |
|               |          |           | Summe | 107.50     |

> [!NOTE]
> Wenn Sie den Wechselcode anwenden, erhöhen sich die Überstunden um 0,5 Stunden, von 1,50 zu 2,00. Die 0,5 Stunden ist die Konvertierung der „Gleitzeit+”-Zeit, die erfasst wurde, von 6:30 Uhr bis 7:00 Uhr, in Überstunden.

### <a name="breaks"></a>Pausen

Pausen von der Arbeit wirken sich auf die Berechnung des Lohns der Arbeitskraft aus. Erfasste Pausen sind als Typ einer indirekte Aktivität definiert. Sie können entweder als **Entlohnt** definiert werden, damit die Pause dem Lohn der Arbeitskraft hinzugefügt werden kann, oder als **Nicht entlohnt**, um zu verhindern, dass die Pause zum Lohn der Arbeitskraft hinzugefügt wird. Eine Pause kann auch als **Geplant** oder **Geplant** festgelegt werden.

#### <a name="planned-breaks"></a>Geplante Pausen

Wenn ein Unternehmen feste Pausen hat, wie eine feste Pause für das Mittagessen, kann die Pause im Zeitprofil konfiguriert werden. In diesem Fall muss die Arbeitskraft die Pause in den Einzelvorgangslistenseiten nicht erfassen. Stattdessen wird der Pause für automatisch, wenn die Erfassungen der Arbeitskraft berechnet auf der Seite **Genehmigen** werden.

#### <a name="registered-breaks"></a>Erfasste Pausen

Wenn ein Unternehmen nicht geplanten Pause verwendet, können Arbeitskräfte Im Verlauf des Tages eingelegte Pausen erfassen. Erfasste Pausen können beispielsweise verwendet werden, wenn eine Arbeitskraft nach einem Gleitzeitprofil ohne definierte Ein- und Ausstempeluhrzeiten arbeitet. Erfasste Pausen sind ein Typ indirekter Aktivität. Die Arbeitskraft erfasst die Pause auf der Terminalseite **Einzelvorgangsliste** oder auf der Geräteseite **Einzelvorgangsliste**. Auf diesen beiden Seiten kann der Benutzer den Typ der Pause in einer Liste mit vordefinierten Pausenaktivitäten auswählen.

#### <a name="paid-and-unpaid-breaks"></a>Entlohnte und unbezahlte Pausen

Pausenaktivitäten können als **Bezahlt** oder **Unbezahlt** eingerichtet werden. Eine bezahlte Pause ist in der Berechnung der entlohnten Zeit enthalten, und das System verwendet den Zahlungstyp, der in der Lohnvereinbarung für den Erfassungstyp **Pause** definiert ist.

### <a name="example-of-a-planned-break"></a>Beispiel einer geplanten Pause

Berücksichtigen Sie das folgende Zeitprofil, das eine nicht bezahlte Mittagspause enthält.

| Profiltyp  | Start    | Beenden      | Tag     |
|---------------|----------|----------|---------|
| Überstunden     | 00:00 (vormittags) | 06:00 (vormittags) | Montag  |
| Gleitzeit+         | 06:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Einstempeln      | 07:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Standardzeit | 07:00 (vormittags) | 12:00 (nachmittags) | Montag  |
| Pause         | 12:00 (nachmittags) | 12:30 (nachmittags) | Montag  |
| Standardzeit | 12:30 (nachmittags) | 02:30 (nachmittags) | Montag  |
| Gleitzeit-         | 02:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Ausstempeln     | 03:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Überstunden     | 03:30 (nachmittags) | 06:00 (vormittags) | Dienstag |

Hier sind Erfassungen der Arbeitskraft an diesem Tag.

| Journalerfassungstyp | Start    | Beenden      |
|---------------------------|----------|----------|
| Einstempeln                  | 06:30 (vormittags) | 06:30 (vormittags) |
| Produktionseinzelvorgang            | 06:30 (vormittags) | 02:45 (nachmittags) |
| Ausstempeln                 | 05:00 (nachmittags) | 05:00 (nachmittags) |

Nachdem Sie die Journal-Erfassungen der Seite auf **Genehmigen** berechnet haben, können Sie die Berechnungsauswirkung auf den **Zeiten** anzeigen. Um dieses Szenarios zu veranschaulichen, gehen Sie zu folgenden Felder.

| Gleitzeit+ | Gleitzeit- | Zeit  | Entlohnte Zeit | Nicht entlohnte Pausenzeit | Entlohnte Überstundenzeit |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9.50     | 0.5                 | 1.50         |

> [!NOTE] 
> Das System berechnet 0,5 Stunden nicht entlohnter Pausen, und diese Zeit ist nicht Teil der entlohnten Zeit.

### <a name="example-of-a-registered-break"></a>Beispiel einer erfassten Pause

Berücksichtigen Sie das folgende Zeitprofil, das nicht geplanten Pausen enthält.

| Profiltyp  | Start    | Beenden      | Tag     |
|---------------|----------|----------|---------|
| Überstunden     | 00:00 (vormittags) | 06:00 (vormittags) | Montag  |
| Gleitzeit+         | 06:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Einstempeln      | 07:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Standardzeit | 07:00 (vormittags) | 02:30 (nachmittags) | Montag  |
| Gleitzeit-         | 02:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Ausstempeln     | 03:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Überstunden     | 03:30 (nachmittags) | 06:00 (vormittags) | Dienstag |

Hier sind Erfassungen der Arbeitskraft an diesem Tag.

| Journalerfassungstyp | Start    | Beenden      |
|---------------------------|----------|----------|
| Einstempeln                  | 06:30 (vormittags) | 06:30 (vormittags) |
| Produktionseinzelvorgang            | 06:30 (vormittags) | 05:00 (nachmittags) |
| Pause                     | 12:03 (nachmittags) | 12:32 (nachmittags) |
| Ausstempeln                 | 05:00 (nachmittags) | 05:00 (nachmittags) |

Wenn die Erfassungen berechnet werden, wird die Zeit für die Aktivitäten berechnet.

| Journalerfassungstyp | Start    | Beenden      | Zeit  |
|---------------------------|----------|----------|-------|
| Einstempeln                  | 06:30 (vormittags) | 06:30 (vormittags) |       |
| Produktionseinzelvorgang            | 06:30 (vormittags) | 05:00 (nachmittags) | 10.00 |
| Pause                     | 12:03 (nachmittags) | 12:32 (nachmittags) | 0,50  |
| Ausstempeln                 | 05:00 (nachmittags) | 05:00 (nachmittags) |       |

> [!NOTE]
> Die Zeit für die Pause läuft parallel zur Zeit für die Aktivität (in diesem Beispiel ein Produktionseinzelvorgang). Dieses Verhalten wird immer für Pausenaktivitäten verwendet. Wenn die Erfassungen berechnet werden, wird die Pausenzeit von der Aktivitätszeit subtrahiert. In diesem Fall hat der Produktions-Einzelvorgang eine Dauer von 10.50 Stunden, und die Zeit wird als 10 berechnet, da 0.5 Stunden Pausenzeit von der Aktivitätszeit subtrahiert werden.

Nachdem Sie die Journal-Erfassungen der Seite auf **Genehmigen** berechnet haben, können Sie die Berechnungsauswirkung auf den **Zeiten** anzeigen. Um dieses Szenarios zu veranschaulichen, gehen Sie zu folgenden Felder.

| Gleitzeit+ | Gleitzeit- | Zeit  | Entlohnte Zeit | Nicht entlohnte Pausenzeit | Entlohnte Überstundenzeit |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9.50     | 0.5                 | 1.50         |

Wenn die geplante Pause anstelle von unbezahlten bezahlt wurde, würde das Berechnungsergebnis folgendermaßen aussehen.

| Gleitzeit+ | Gleitzeit- | Zeit  | Entlohnte Zeit | Entlohnte Pausenzeit | Entlohnte Überstundenzeit |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 0.5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Lohnelemente und Pausen bezahlte

Wenn Sie Erfassungen auf der Seite **Genehmigen** übertragen, werden Lohnelemente generiert. Eine separater Zahlungsartikel wird für bezahlte Pausen generiert.

Der Lohnsatz für eine entlohnte Pause wird durch die Lohnart bestimmt, die in den Lohnvereinbarungen für die Pause eingerichtet ist. Anstatt eine Lohnart zu verwenden, können Sie den Einstandspreis pro Stunde für die Pause für ein definiertes Datumsintervall einrichten.

Berücksichtigen Sie das folgende Zeitprofil.

| Profiltyp  | Start    | Beenden      | Tag     |
|---------------|----------|----------|---------|
| Überstunden     | 00:00 (vormittags) | 06:00 (vormittags) | Montag  |
| Gleitzeit+         | 06:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Einstempeln      | 07:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Standardzeit | 07:00 (vormittags) | 02:30 (nachmittags) | Montag  |
| Gleitzeit-         | 02:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Ausstempeln     | 03:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Überstunden     | 03:30 (nachmittags) | 06:00 (vormittags) | Dienstag |

Hier sind Erfassungen der Arbeitskraft an diesem Tag.

| Journalerfassungstyp | Start    | Beenden      | Zeit |
|---------------------------|----------|----------|------|
| Einstempeln                  | 07:00 (vormittags) | 07:00 (vormittags) |      |
| Produktionseinzelvorgang            | 07:00 (vormittags) | 03:00 (nachmittags) | 7.5  |
| Pause (bezahlt)              | 12:00 (nachmittags) | 12:30 (nachmittags) | 0.5  |
| Ausstempeln                 | 03:00 (nachmittags) | 03:00 (nachmittags) |      |

Bei diesem Beispiel wird die Lohnart für Standardzeit auf **1201** festgelegt, und ein Lohnsatz von **10** wird in Lohnvereinbarung eingerichtet. Die entlohnte Pause hat eine Lohnart von **1301** sowie einen Lohnsatz von **8**. Wenn die Erfassungen übertragen werden, werden folgende Lohnelemente generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 7.50      | 10   |
| Gleitzeit-         | 1201     | 0,50      | 10   |
| Pause (bezahlt)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Wie die Kosten von Pausen zu Projekten und Produktionsaufträge zugewiesen sind

Die Kosten pro Stunde für Projektaktivitäten und Produktionseinzelvorgänge können so eingerichtet werden, dass sie entweder durch die in „Zeit und Anwesenheit” berechneten Lohnsätze oder durch die für die Aktivitäten definierten Kostenkategorien bestimmt werden.

Um die Kostenkategorie einzurichten, wählen Sie **Produktionssteuerung** &gt; **Einstellungen** &gt; **Fertigungssteuerung** &gt; **Produktionsauftragsstandards** aus, und legen Sie das Feld **Kostenkategorie** entweder auf **Ja** oder **Nein** fest.

- **Nein** – Die Kosten werden auf Basis der Lohnsätze berechnet, die für Aufwandsprojekte Anwesenheitserfassungs-Typen definiert werden.
- **Ja** – Die Kosten werden basierend auf Kostenkategorien und Projektaktivitäten für die Produktion berechnet.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Kostenberechnung auf Grundlage von Lohnsätzen, die in "Zeit und Anwesenheit" berechnet werden

Das folgende Beispiel zeigt, wie die Kosten pro Stunde berechnet werden, wenn die Kosten eingerichtet werden, damit sie auf Grundlage von Lohnsätzen berechnet werden.

Der Satz für Kosten pro Stunde, der für Produktionsaufträge und Projekte verwendet wird, wird während des Übertragungsprozesses berechnet. Um den Stundensatz pro Aktivität anzuzeigen, öffnen Sie die Seite **Genehmigen** in „Zeit und Anwesenheit”, und wählen Sie anschließend **Abfrage** &gt; **Übertragene Erfassungen** aus. Sie können den Stundenkostensatz pro Erfassung auf der Registerkarte **Einstandspreise** finden.

Führen Sie die folgenden Erfassungen aus, die das gleiche Zeitprofil verwenden wi im vorherigen Beispiel werden.

| Journalerfassungstyp | Start    | Beenden      | Zeit |
|---------------------------|----------|----------|------|
| Einstempeln                  | 07:00 (vormittags) | 07:00 (vormittags) |      |
| Prozess (Auftrag: 4711)     | 07:00 (vormittags) | 11:00 (vormittags) | 4    |
| Prozess (Auftrag: 4712)     | 11:00 (vormittags) | 03:00 (nachmittags) | 3.50 |
| Pause (bezahlt)              | 12:00 (nachmittags) | 12:30 (nachmittags) | 0,50 |
| Ausstempeln                 | 03:00 (nachmittags) | 03:00 (nachmittags) |      |

Wenn die Erfassungen übertragen werden, werden folgende Lohnelemente generiert.

| Registrierungstyp     | Zeit | Einstandspreis pro Stunde |
|-----------------------|------|---------------------|
| Einstempeln              | 0,00 | 0,00                |
| Prozess (Auftrag: 4711) | 4,00 | 10.00               |
| Prozess (Auftrag: 4712) | 3.50 | 11.14               |
| Pause (bezahlt)          | 0,50 | 0,00                |
| Ausstempeln             | 0,00 | 0,00                |

Die Berechnung des Einstandspreises pro Stunde für die entlohnte Pause hängt von einer Einstellung für die direkten Lohnkosten ab. Wählen Sie **Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Zeit- und Anwesenheitsparameter** aus. Auf der Registerkarte **Einstandspreis** unter **Direkte Lohnkosten**, im Feld **Standardzeit**, können Sie **Ja**, **Nein** oder **Umlage** auswählen.

- **Ja** – Dieser Wert wird für das vorstehende Beispiel verwendet. Die Kosten werden der Produktion oder der Projektaktivität zugewiesen, die parallel mit der entlohnten Pausenaktivität ausgeführt wird. Im Beispiel ist diese Aktivität der Produktions-Einzelvorgang für Auftrag 4712. Wie Sie sehen können, ist der Einstandspreis pro Stunde für die entlohnte Pause 0 (Null), und er ist dem Einzelvorgang zugewiesen, der parallel mit der Pause ausgeführt wird.

    Die entlohnte Pause hat eine Dauer von 0,5 Stunden, und der Lohnsatz ist 8. Somit sind die Gesamtkosten für die entlohnte Pause 4. Die Gesamtkosten werden dann dem 3,5 -Stunden-Bearbeitungseinzelvorgang zugeordnet. Daher trägt die entlohnte Pause 1,14 pro Stunde an Kosten (bei 4 ÷ 3,5 = 1,14) bei.

- **Zuteilung** – Die bezahlte Pause wird gleichmässig auf die Einzelvorgänge aufgeteilt, die während des Tages erfasst werden. Wenn dieser Wert zum vorstehende Beispiel verwendet wird, werden die folgenden übertragenen Erfassungen generiert.

    | Registrierungstyp     | Zeit | Einstandspreis pro Stunde |
    |-----------------------|------|---------------------|
    | Einstempeln              | 0,00 | 0,00                |
    | Prozess (Auftrag: 4711) | 4,00 | 10.53               |
    | Prozess (Auftrag: 4712) | 3.50 | 10.53               |
    | Pause (bezahlt)          | 0,50 | 0,00                |
    | Ausstempeln             | 0,00 | 0,00                |

    Die gesamten Bearbeitungszeit für die beiden Produktionseinzelvorgänge beträgt 7,5 Stunden, und die Gesamtkosten der entlohnten Pause betragen 4. Daher werden die Kosten der Pause als 0,53 (= 4 ÷ 7,5) berechnet.

- **Nein** – Die Kosten für die bezahlte Pause erhöhen nicht die Stundenkosten der Prozessaktivitäten.

    | Registrierungstyp     | Zeit | Einstandspreis pro Stunde |
    |-----------------------|------|---------------------|
    | Einstempeln              | 0,00 | 0,00                |
    | Prozess (Auftrag: 4711) | 4,00 | 10.00               |
    | Prozess (Auftrag: 4712) | 3.50 | 10.00               |
    | Pause (bezahlt)          | 0,50 | 0,00                |
    | Ausstempeln             | 0,00 | 0,00                |

## <a name="absence"></a>Abwesenheit

Ein Abwesenheitscode wird verwendet, um die Periode der Abwesenheit einer Arbeitskraft zu erfassen. Wie Pausen und Wechselcodes ist ein Abwesenheitscode eine Art von indirekter Aktivität. Absenzzeit kann entweder geplant oder angemeldet sein, Abwesenheit kann entweder gültig oder ungültig sein. Beispiele der gültigen Abwesenheit kann ein Arzttermin oder ein Gerichtstermin sein. Ungültige Abwesenheit ist, wenn die Abwesenheit keinen triftigen Grund enthält, z.B. wenn eine Arbeitskraft zu spät zur Arbeit kommt. Normalerweise verursacht eine zulässige Abwesenheit keinen Abzug vom Lohn einer Arbeitskraft, wohingegen eine unzulässige Abwesenheit einen Abzug verursacht.

### <a name="planned-absence"></a>Geplante Abwesenheit

Sie können geplante Abwesenheit für Arbeitskräfte auf der Seite **Geplante Abwesenheit erstellen** erstellen (**Zeit und Anwesenheit** &gt; **Geplante Abwesenheit erstellen**). Dort wird die geplante Abwesenheit als Abwesenheitseinzelvorgang für ein angegebenes Datum und Zeitintervall erfasst.

Der Einzelvorgang basiert auf einer Abfrage. Daher können Sie eine geplante Abwesenheit für mehrere Arbeitskräfte erstellen, wie beispielsweise Arbeitskräfte, die zur selben Berechnungsgruppe gehören. Wenn die geplante Abwesenheit für einzelne Arbeitskräfte ist, kann die Erfassung von der Seite **Anwesenheit** oder auf der Seite **Zeiterfassung für Arbeitskräfte** eingegeben werden.

- Um eine Abwesenheitserfassung von der Seite **Anwesenheit** einzugeben, wählen Sie **Zeit und Anwesenheit** &gt; **Abfragen und Berichte** &gt; **Anwesenheit** &gt; **Anwesenheit** aus, und wählen Sie dann **Abwesenheitserfassung** aus.
- Um eine Abwesenheitserfassung von der Seite *<strong><em>Zeiterfassung für Arbeitskräfte</em></strong>* einzugeben, wählen Sie <strong>Zeit und Anwesenheit</strong> &gt; <strong>Setup</strong> &gt; <strong>Zeiterfassung für Arbeitskräfte</strong> aus, und wählen Sie dann auf der Registerkarte <strong>Zeit</strong> unter <strong>Zeitzuweisung</strong> die Option <strong>Abwesenheitserfassungen</strong> aus.

Sie können den Bericht **Geplante Abwesenheitszeiten** verwenden, um eine Übersicht über geplante Abwesenheiten für Arbeitskräfte anzuzeigen. Um diesen Bericht zu öffnen, wählen Sie **Zeit und Anwesenheit** &gt; **Abfragen und Berichte** &gt; **Abwesenheitsberichte** &gt; **Geplante Abwesenheitszeiten** aus.

### <a name="registered-absence"></a>Erfasste Abwesenheit

Im Allgemeinen werden Arbeitskräfte als anwesend betrachtet, wenn sie nicht für einen beliebigen Zeitraum zwischen der geplanten Ein- und Ausstempeluhrzeit bei der Arbeit sind. Wenn Arbeitskräfte später als geplant einstempeln oder wenn sie früher als geplant ausstempeln, werden sie gefragt, einen Abwesenheitscode auszuwählen, um den Grund für die Abwesenheit anzugeben. Ein Abwesenheitscode kann so eingerichtet werden, dass er für die Erfassung gültig ist. Nur gültige Codes sind umgehend in der Liste verfügbar.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Szenarien auf Grundlage unterschiedlicher Kombinationen von Arbeitsstundenerfassungen

In den folgenden Szenarios werden die Lohnelemente und -einträge zur Genehmigung an, die für Arbeitskräfte auf Grundlage ihrer Erfassungen generiert werden. Diese Szenarien basieren auf den folgenden Zeitprofilen.

| Profiltyp  | Start    | Beenden      | Tag     |
|---------------|----------|----------|---------|
| Überstunden     | 00:00 (vormittags) | 06:00 (vormittags) | Montag  |
| Gleitzeit+         | 06:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Einstempeln      | 07:00 (vormittags) | 07:00 (vormittags) | Montag  |
| Standardzeit | 07:00 (vormittags) | 02:30 (nachmittags) | Montag  |
| Gleitzeit-         | 02:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Ausstempeln     | 03:30 (nachmittags) | 03:30 (nachmittags) | Montag  |
| Überstunden     | 03:30 (nachmittags) | 06:00 (vormittags) | Dienstag |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Szenario 1: Die Arbeitskraft stempelt später als geplant ein

Die Arbeitskraft stempelt um 08:30 Uhr ein. Da die geplante Einstempelzeit 07:00 ist, ist er 1,50 Stunde zu spät zur Arbeit. Da die 1,50 Stunden als Abwesenheitzeit berücksichtigt wird, ist die Arbeitskraft aufgefordert, einen Abwesenheitscode auswählen. Die Arbeitskraft verlässt die Arbeit um 15:30 Uhr, was die geplante Ausstempeluhrzeit ist. Wenn die Erfassungen der Arbeitskraft berechnet und genehmigt werden, wird die Abwesenheitserfassung zusammen mit dem Abwesenheitscode, den die Arbeitskraft beim Einstempeln auswählte, für die Zeit zwischen 07:00 Uhr bis 08:30 Uhr angezeigt.

Im Zeitprofil können Sie den Anmeldetyp **Einstempeln** konfigurieren, damit eine Toleranz vorhanden ist, wenn Arbeitskräfte zu spät zur Arbeit sind. Wenn Sie eine Toleranz von 5 einrichten, erhält die Arbeitskraft für einen Abwesenheitscode, wenn er später als 07:05 einstempelt.

Da die Arbeitskraft in diesem Fall keinen triftigen Grund für das Zuspätkommen zur Arbeit hat, wählt er einen Abwesenheitscode aus, der für unzulässige Abwesenheit definiert wird. Ein Abwesenheitscode wird für ungültige Abwesenheit anwendbar, wenn die Einstellung für Überstundenabzug für die Abwesenheitsgruppe aktiviert ist, zum der Abwesenheitscode gehört. Um die Einstellung festzulegen, wählen Sie **Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Gruppen** &gt; **Abwesenheitsgruppen** aus, und aktivieren Sie dann das Kontrollkästchen **Überstunden abziehen**.

So werden Erfassungen der Arbeitskraft für den Tag auf der Seite **Genehmigen** bei Berechnung angezeigt werden.

| Journalerfassungstyp         | Start    | Beenden      | Zeit |
|-----------------------------------|----------|----------|------|
| Abwesenheit (Inicht erlaubt - zu spät zur Arbeit) | 07:00 (vormittags) | 08:30 (vormittags) | 1.5  |
| Einstempeln                          | 08:30 (vormittags) | 08:30 (vormittags) |      |
| Produktionseinzelvorgang                    | 07:30 (vormittags) | 03:30 (nachmittags) | 7.0  |
| Ausstempeln                         | 03:30 (nachmittags) | 03:30 (nachmittags) |      |

Das hier ist das sich ergebende Lohnelemente, nachdem die Erfassungen übertragen werden.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 7:00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Szenario 2: Die Arbeitskraft stempelt vor der geplanten Ausstempeluhrzeit für eine Standardzeitperiode aus

Die Arbeitskraft stempelt um 07:00 Uhr ein und stempelt früher, um 13:00 Uhr aus. Da 01:00 Uhr vor dem geplanten Ausstempeln um 03:30 Uhr liegt und 01:00 eine Standard-Zeitperiode ist, wird die Arbeitskraft aufgefordert, einen Abwesenheitscode auszuwählen. Die Arbeitskraft wählt einen Abwesenheitscode für einen Arzttermin aus, der als zulässige Abwesenheit definiert ist. Der Lohnsatz für eine zulässige Abwesenheit wird in den Lohnvereinbarungen für den Erfassungstyp **Abwesenheit** definiert (**Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Lohn** &gt; **Lohnvereinbarungen**).

So werden Erfassungen der Arbeitskraft für den Tag auf der Seite **Genehmigen** bei Berechnung angezeigt werden.

| Journalerfassungstyp              | Start    | Beenden      | Zeit |
|----------------------------------------|----------|----------|------|
| Einstempeln                               | 07:00 (vormittags) | 07:00 (vormittags) |      |
| Produktionseinzelvorgang                         | 07:00 (vormittags) | 13:00 (nachmittags) | 4.0  |
| Ausstempeln                              | 13:00 (nachmittags) | 13:00 (nachmittags) |      |
| Abwesenheit (gültig – Arzttermin) | 13:00 (nachmittags) | 03:30 (nachmittags) | 3.5  |

Das hier ist das sich ergebende Lohnelemente, nachdem die Erfassungen übertragen werden.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 7.50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Szenario 3: Die Arbeitskraft stempelt vor der geplanten Ausstempeluhrzeit wähend einer „Gleitzeit-”-Periode aus

Die Arbeitskraft stempelt um 07:00 Uhr ein und stempelt um 14:15 Uhr aus, was in der geplanten „Gleitzeit-”-Periode liegt. Die Zeit zwischen der tatsächlichen Ausstempeluhrzeit und der geplanten Ausstempeluhrzeit wird nicht als Abwesenheit betrachtet, und die Arbeitskraft wird nicht dazu aufgefordert, einen Abwesenheitscode auszuwählen. Der Betrag wird dem Gleitzeitkonto der Arbeitskraft abgezogen, und die Arbeitskraft wird während dem verbleibenden Teil der „Gleitzeit-”-Periode von 14:15 Uhr bis 15:30 Uhr entlohnt.

So werden Erfassungen der Arbeitskraft für den Tag auf der Seite **Genehmigen** bei Berechnung angezeigt werden.

| Journalerfassungstyp | Start    | Beenden      | Zeit |
|---------------------------|----------|----------|------|
| Einstempeln                  | 07:00 (vormittags) | 07:00 (vormittags) |      |
| Produktionseinzelvorgang            | 07:00 (vormittags) | 14:15 (nachmittags) | 7.25 |
| Ausstempeln                 | 14:15 (nachmittags) | 14:15 (nachmittags) |      |

Das hier ist das sich ergebende Lohnelemente, nachdem die Erfassungen übertragen werden.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 8.50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Szenario 4: Die Arbeitskraft stempelt verspätet ein und stempelt nach der geplanten Ausstempeluhrzeit während einer Überstundenperiode aus

Die Arbeitskraft stempelt verspätet um 09:30 Uhr ein, und um dann seine verspätete Anwesenheit auszugleichen, macht er Überstunden und stempelt um 17:00 Uhr aus. Da die Arbeitskraft verspätet kam und die Zeit durch länger Arbeiten ausgeglichen hat, will das Unternehmen dem Mitarbeiter keine Überstunden vergüten, die er zwischen der geplanten Ausstempelzeit zwischen 03:30 Uhr und seinem Ausstempeln um 05:00 Uhr gearbeitet hat, obwohl diese Periode als Überstunden im Zeitprofil definiert wird.

Um dieses Szenarios zu behandeln, kann der Abwesenheitscode so festgelegt werden, dass Überstunden um sämtliche Stunden unzulässiger Abwesenheit reduziert werden, die bei der Arbeitskraft am gleichen Tag vorliegen. Wählen Sie **Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Gruppen** &gt; **Abwesenheitsgruppen** aus, und aktivieren Sie das Kontrollkästchen **Überstunden abziehen**, um Überstunden von Stunden unzulässiger Abwesenheit abzuziehen.

So werden Erfassungen der Arbeitskraft für den Tag auf der Seite **Genehmigen** bei Berechnung angezeigt werden.

| Journalerfassungstyp         | Start    | Beenden      | Zeit |
|-----------------------------------|----------|----------|------|
| Abwesenheit (Inicht erlaubt - zu spät zur Arbeit) | 07:00 (vormittags) | 09:30 (vormittags) | 1.5  |
| Einstempeln                          | 09:30 (vormittags) | 09:30 (vormittags) |      |
| Produktionseinzelvorgang                    | 09:30 (vormittags) | 05:00 (nachmittags) | 7.5  |
| Ausstempeln                         | 05:30 (nachmittags) | 05:30 (nachmittags) |      |

Wenn das Kontrollkästchen **Überstundenzeit abziehen** für den ausgewählten Abwesenheitscode ausgewählt ist, werden die Stunden abgezogen für die die Arbeitskraft illegal abwesend war. Wenn die Erfassungen übertragen werden, werden folgende Lohnelemente generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 9:00      | 10   |
| Überstunden      | 1301     | 0.5       | 15   |

Hier ziehen die 1,5 Stunden der unzulässigen Abwesenheit von 07:00 bis 09:30 bis die 2 Überstunden von 03:30 Uhr bis 05:30 Uhr ab. Das Ergebnis der Erfassung beträgt 1,5 Stunden Standardzeit und 0,5 Stunden Überstunden.

Durch Kontrast, wenn das Kontrollkästchen **Überstundenzeit abziehen** für den ausgewählten Abwesenheitscode deaktiviert ist, wird der Arbeitskraft Überstundenzuschlag gewährt, auch wenn er zu spät war oder eine ungültige Abwesenheit aufweist. Wenn die Erfassungen übertragen werden, werden folgende Lohnelemente generiert.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 7.50      | 10   |
| Überstunden      | 1301     | 2.0       | 15   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Szenario 5: Die Arbeitskraft stempelt vor der geplanten Ausstempeluhrzeit aus und kann die Abwesenheitsperiode in eine „Gleitzeit-”-Periode konvertieren

Das folgende Beispiel zeigt, wie das Gleitzeitkonto einer Arbeitskraft reduziert werden kann, indem die Abwesenheitsperiode in eine „Gleitzeit-”-Periode konvertiert wird.

Die Arbeitskraft stempelt um 07:00 Uhr ein und stempelt um 01:00 Uhr aus. Sie hat eine Vereinbarung mit ihrem Vorgesetzten getroffen, dass sie nach Hause ins Wochenende gehen kann, wenn sie diese Stunden von ihrem Gleitzeitkonto abzieht. Wenn die Arbeitskraft um 13:00 Uhr ausstempelt, wird Sie dazu aufgefordert, einen Abwesenheitscode auszuwählen, da die Periode der Abwesenheit für den Rest des Arbeitstags, der betroffen ist, sich nicht in einer geplanten „Gleitzeit-”-Periode befindet. Um den verbleibenden Teil des Arbeitstags in eine „Gleitzeit-”-Periode zu konvertieren, kann die Arbeitskraft einen Abwesenheitscode auswählen, der eingerichtet ist, um ihr Gleitzeitkonto zu reduzieren.

Um den Saldo flexibler Stunden für Arbeitskräfte zu reduzieren, die an einem Arbeitstag Abwesenheit erfassen, wählen Sie **Zeit und Anwesenheit** &gt; **Einstellungen** &gt; **Gruppen** &gt; **Abwesenheitsgruppen** aus, und aktivieren Sie das Kontrollkästchen **Reduziert Gleitzeit**.

So werden Erfassungen der Arbeitskraft für den Tag auf der Seite **Genehmigen** vor Berechnung angezeigt werden.

| Journalerfassungstyp | Start    | Beenden      | Zeit |
|---------------------------|----------|----------|------|
| Einstempeln                  | 07:00 (vormittags) | 07:00 (vormittags) |      |
| Produktionseinzelvorgang            | 07:00 (vormittags) | 13:00 (nachmittags) | 6.0  |
| Ausstempeln                 | 13:00 (nachmittags) | 13:00 (nachmittags) |      |

Wenn die Arbeitskraft einen Abwesenheitscode für unzulässige Abwesenheit auswählt, sehen Sie hier, wie die sich ergebende Lohnelemente sich um die Erfassung kümmern.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 6,00      | 10   |

Wenn die Arbeitskraft einen Abwesenheitscode für gültige Abwesenheit auswählen und der Abwesenheitscode eingerichtet wird, um diesen zu reduzieren Gleitzeitkonto, zeigen wir hier, wie die resultierenden Lohnelemente auf die Erfassungen übertragen werden.

| Gehaltstyp     | Lohnart | Lohneinheiten | Satz |
|---------------|----------|-----------|------|
| Standardzeit | 1201     | 8.50      | 10   |

In diesem Fall wird der Gleitzeitsaldo der Arbeitskraft durch die tatsächlichen Stunden zwischen der geplanten Zeit und Ausstempeluhrzeit der Ausstempeluhrzeit verringert (das heißt, die 2,5 Stunden von 01:00 bis 03:30 Uhr).

> [!NOTE]
> Es wird nicht empfohlen, dass Sie sowohl das Kontrollkästchen **Gleitzeit abziehen** als auch das Kontrollkästchen **Überstunden abziehen** für einen Abwesenheitscode aktivieren, da durch diese Einstellungen die unzulässigen Stunden von den Überstunden der Arbeitskraft abgezogen werden und gleichzeitig das Gleitzeitkonto der Arbeitskraft verringert wird.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Szenario 6: Es gibt keine geplante Abwesenheit für den Tag und keine Arbeitskraftanwesenheit für den Tag

Wenn die Arbeitskraft nicht zur Arbeit kommt an einen Arbeitstag und keine geplante Abwesenheit für die Arbeitskraft an diesem Tag vorhanden sind, wird ein Standardabwesenheitscode für die Berechnung der Erfassungen der Arbeitskraft verwendet. Um Standardabwesenheitscodes zu definieren, wählen Sie **Zeit und Anwesenheit** &gt; **Zeit- und Anwesenheitsparameter** aus. Sie können dann einen Abwesenheitscode in den folgenden Feldern auswählen:

- Automatisches Einfügen von Gleitzeit-
- Automatisches Einfügen von Abwesenheit

Wenn die täglichen Erfassungen für eine Arbeitskraft berechnet werden, die für Gleitzeiten aktiviert ist, wird der Abwesenheitscode, der im Feld **Automatische Einfügung von Gleitzeit-** angegeben ist, als Standardabwesenheitscode verwendet. Wenn die Arbeitskraft nicht für Gleitzeiten aktiviert ist, wird der Abwesenheitscode, der im Feld **Automatische Einfügungsabwesenheit** angegeben ist, verwendet. Wenn ein Unternehmen einer Kombination von Arbeitskräften hat, die für Gleitzeiten und Arbeitskräfte aktiviert werden, die nicht für Gleitzeiten aktiviert sind, müssen beide Parameter eingerichtet werden.
