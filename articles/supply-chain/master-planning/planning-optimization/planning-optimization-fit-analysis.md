---
title: Planungsoptimierung Fit-Analyse
description: In diesem Thema wird erläutert, wie Sie Ihr aktuelles Setup und Ihre Daten mit den Möglichkeiten der Planungsoptimierungsfunktionalität verifizieren können.
author: ChristianRytt
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 60f63a49222b3d0f13850b0f39764c6c848aba15
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049435"
---
# <a name="planning-optimization-fit-analysis"></a>Passanalyse zu Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Sie sollten das Ergebnis der Passanalyse der Planungsoptimierung als Teil des Migrationsprozesses analysieren. Beachten Sie, dass der Umfang der Planungsoptimierung nicht der aktuellen integrierten Produktprogrammplanungsfunktion entspricht. Wir empfehlen Ihnen, mit Ihrem Partner zusammenzuarbeiten und die Dokumentation zu lesen, um sich auf die Migration vorzubereiten. 

Mithilfe der Passanalyse für die Planungsoptimierung können Sie feststellen, wo sich das Ergebnis zwischen der integrierten Produktprogrammplanung-Engine und der Planungsoptimierung unterscheiden kann. Diese Analyse basiert auf Ihrem aktuellen Setup und Ihren Daten. 

Um das Ergebnis der Planungsoptimierungs-Passanalyse anzuzeigen, gehen Sie zu **Produktprogrammplanung** \> **Einstellungen** \> **Planungsoptimierungs-Passanalyse** und wählen dann **Analyse ausführen** aus. Wenn die Analyse Inkonsistenzen feststellt, werden diese auf der gleichen Seite aufgelistet. (Die Analyse kann einige Minuten dauern.)

> [!NOTE]
> Wenn Inkonsistenzen festgestellt werden, können Sie die Planungsoptimierung trotzdem nutzen. Die Ergebnisse der Fit-Analyse zeigen nur, an welchen Stellen der Planungsservice Ihr aktuelles Setup nicht berücksichtigt. Input

## <a name="analysis-results-example-1"></a>Analyseergebnisse: Beispiel 1

- **Funktion:** Produktion
- **Problem:** Artikel mit einer Stücklistenstufe größer als Null: 56
- **Erklärung:** Die Fit-Analyse ergab 56 Artikel, die eine Stückliste für die Produktion eingerichtet haben. Da die aktuelle Version der Planungsoptimierung die Produktion nicht unterstützt, erzeugt die Planungsoptimierung Planbestellungen anstelle von Planfertigungsaufträgen. Es wird auch eine Warnung angezeigt, die die betroffenen Elemente auflistet.

## <a name="analysis-results-example-2"></a>Analyseergebnisse: Beispiel 2

- **Funktion:** Aktionen
- **Problem:** Deckungsgruppen mit aktivierter Aktionsberechnung: 6
- **Erklärung:** Die Fit-Analyse ergab sechs Deckungsgruppen, in denen die Aktionsberechnung eingeschaltet ist. Da die aktuelle Version der Planungsoptimierung keine Aktionen unterstützt, werden bei der Masterplanung keine Aktionen generiert.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Übersicht möglicher Ergebnisse aus der Fit-Analyse

Die folgende Tabelle zeigt die verschiedenen Ergebnisse, die nach einer Anpassungsanalyse angezeigt werden können. Nummernzeichen (_\#_) werden durch eine Zahl ersetzt, die die Anzahl der Datensätze angibt, bei denen das Problem aufgetreten ist. Unterstützte Funktionen oder Funktionen in der Vorschau sind ab Version 10.0.9 verfügbar (es sei denn, in der Spalte „Erwartete Verfügbarkeit“ ist eine höhere Versionsnummer aufgeführt).

| Funktion | Gelistetes Problem | Erläuterung | Erwartete Verfügbarkeit |
| --- | --- | --- | --- |
| Aktionen | Dispositionssteuerungsgruppen mit aktivierter Aktivitätenberechnung: _\#_ | Diese Funktion steht noch aus. Derzeit werden während der Masterplanung keine Aktionen generiert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. Der Hauptzweck von Aktionen besteht darin, Änderungen an bestehenden Aufträgen vorzuschlagen. Bewerten Sie, ob Aktionen im Rahmen Ihrer Geschäftsprozesse aktiv angewendet werden oder ob die Verzögerungsinformationen bezüglich der Bestellungen ausreichend sind. | Oktober 2021 - April 2022 |
| Basiskalender | Kalender, die den Basiskalender verwenden: _\#_ | Diese Funktion steht noch aus. Derzeit wird der Basiskalender ignoriert, wenn die Planungsoptimierung aktiviert ist. Prüfen Sie, ob der Basiskalender für Ihre Geschäftsprozesse benötigt wird oder ob eine direkte Einrichtung in Kalendern ausreicht. | April – Oktober 2021 | 
| Chargendispositionscodes | Nicht kompensierbare Chargendispositionsmaster: _\#_ | Diese Funktion steht noch aus. Derzeit werden Chargen-Dispositionscodes ignoriert, wenn die Planungsoptimierung aktiviert ist. | Oktober 2021 - April 2022 |
| Verfügbarkeitszusage (CTP) | Standardauftragseinstellungen mit Lieferdatumskontrolle, die auf CTP eingestellt ist: _\#_ | Diese Funktion steht noch aus. Derzeit wird CTP ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Oktober 2021 - April 2022 |
| Statischen in dynamischen Plan kopieren | "Statischen in dynamischen Plan kopieren" ist in den Produktprogrammplanungsparametern aktiviert. | Die Planungsoptimierung kopiert den statischen Plan unabhängig von dieser Einstellung nicht in den dynamischen Plan. Im Allgemeinen ist dieses Konzept aufgrund der Geschwindigkeit und vollständigen Regeneration, die die Planungsoptimierung bietet, weniger relevant. Wenn zwei oder mehr Pläne verwendet werden, sollte für jeden Plan eine Masterplanung ausgelöst werden. | Oktober 2021 - April 2022 |
| Umwandeln | Dispositionssteuerungsgruppen mit automatisch festgelegtem Sofortanlagezeitraum: _\#_ | In Version 10.0.7 und höher wird das Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion _Automatische Umwandlung zur Planungsoptimierung_ wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Festigung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Festlegung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Festigungszeitraum einbezogen werden muss. | Unterstützt |
| Umwandeln | Artikeldeckungsdatensätze mit automatisch festgelegter Umwandlung: _\#_ | In Version 10.0.7 und höher wird das automatische Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion _Automatische Umwandlung zur Planungsoptimierung_ wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Festigung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Festlegung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Festigungszeitraum einbezogen werden muss. | Unterstützt |
| Umwandeln | Produktprogrammpläne mit automatisch festgelegter Umwandlung: _\#_ | In Version 10.0.7 und höher wird das automatische Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion _Automatische Umwandlung zur Planungsoptimierung_ wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Festigung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Festlegung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Festigungszeitraum einbezogen werden muss. | Unterstützt |
| FitAnalysisPlanningItems | Planungselemente: _\#_ | Diese Funktion steht noch aus. Derzeit werden Planungselemente wie normale Elemente behandelt, wenn die Planungsoptimierung aktiviert ist. | Oktober 2021 - April 2022 |
| Planung | Abdeckungsgruppen mit „Intercompany-Bestellungen einschließen“ aktiviert: _\#_ | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Intercompany-Planung](Intercompany-planning.md) | Unterstützt |
| Planung | Abdeckungsgruppen mit der Einstellung „Planungswert verringern um“ auf einen anderen Wert als „Aufträge“ festgelegt: _\#_ | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Produktprogrammplanung mit Bedarfsprognosen](demand-forecast.md) | Unterstützt |
| Planung | Planzahlenmodelle mit Untermodellen: _\#_ |  Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Produktprogrammplanung mit Bedarfsprognosen](demand-forecast.md) | Unterstützt |
| Planung | Masterpläne mit aktivierter Option „Beschaffungsplanung einbeziehen“: _\#_ | Diese Funktion steht noch aus. Derzeit Beschaffungsplanungen nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. | Oktober 2021 - April 2022 |
| Nichtplanungszeitraum | Dispositionssteuerungsgruppen mit gesperrtem festgelegtem Sofortanlagezeitraum: _\#_ | Der Sperrzeitraum wird nicht oft verwendet, und es ist derzeit nicht geplant, ihn für die Planungsoptimierung aufzunehmen. Derzeit wird der eingerichtete Sperrzeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | N/V |
| Nichtplanungszeitraum | Artikeldeckungsdatensätze mit gesperrtem festgelegtem Sofortanlagezeitraum: _\#_ | Der Sperrzeitraum wird nicht oft verwendet, und es ist derzeit nicht geplant, ihn für die Planungsoptimierung aufzunehmen. Derzeit wird der eingerichtete Sperrzeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | N/V |
| Nichtplanungszeitraum | Produktprogrammpläne mit gesperrtem festgelegtem Sofortanlagezeitraum: _\#_ | Der Sperrzeitraum wird nicht oft verwendet, und es ist derzeit nicht geplant, ihn für die Planungsoptimierung aufzunehmen. Derzeit wird der eingerichtete Sperrzeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | N/V |
| Intercompany | Produktprogrammpläne einschließlich geplanten Downstream-Bedarfs: _\#_ | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Intercompany-Planung](Intercompany-planning.md) | Unterstützt |
| Kanban | Artikeldeckungsdatensätze mit geplantem Auftragstyp "Kanban": _\#_ | Diese Funktion steht noch aus. Derzeit wird die auf Kanban eingestellte Artikelabdeckung ignoriert, wenn die Planungsoptimierung aktiviert ist. Die geplante Kanban-Auftragsart erstellt während der Masterplanung eine Warnung, und geplante Bestellungen werden erstellt, um den entsprechenden Bedarf zu decken. | Oktober 2021 - April 2022 |
| Kanban | Artikel mit Standardauftragstyp „Kanban“: _\#_ | Derzeit wird die auf Kanban eingestellte Standardauftragsart ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Kanban-Standardauftragsart erstellt während der Masterplanung eine Warnung, und geplante Bestellungen werden erstellt, um den entsprechenden Bedarf zu decken. | Oktober 2021 - April 2022 |
| Produktlebenszyklus-Status | Produktlebenszyklus-Status nicht aktiv für die Planung: _\#_ | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Ausschließen von Produkten, die bestimmte Status im Produktlebenszyklus haben](product-lifecycle-state.md) | Unterstützt |
| Produktion | Stücklistenpositionen mit Rundung oder mehreren Konfigurationen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Rundungen und mehrere Setups in Stücklistenzeilen ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. | April – Oktober 2021 |
| Produktion | Stücklisten-/Formelpositionen mit Formelmessung: _\#_ | Diese Funktion steht noch aus. Derzeit wird Formelmessung in Stücklisten- und Formelzeilen ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. | 2021. Oktober |
| Produktion | Stücklisten-/Formelpositionen mit Artikelersetzung (Plangruppen): _\#_ | Diese Funktion steht noch aus. Derzeit wird Artikelersetzung (Plangruppen) ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. | 2021. Oktober |
| Produktion | Stücklisten-/Formelpositionen mit negativer Menge: _\#_ | Diese Funktion steht noch aus. Stücklisten-/Formelpositionen mit negativer Menge werden mit einer Menge von 0 (null) eingeschlossen, und eine Warnung wird ausgegeben, wenn die Planungsoptimierung aktiviert ist. Aktualisieren Sie die Stammdaten, um Warnungen zu vermeiden. | 2021. Oktober |
| Produktion | Stücklisten-/Formelpositionen mit Ressourcenverbrauch: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten-/Formelpositionen mit Ressourcenverbrauch ignoriert, wenn die Planungsoptimierung aktiviert ist. Wenn diese Funktion unterstützt wird, wird der Materialbedarf auf das Produktionsstartdatum festgelegt. Bis diese Funktion unterstützt wird, werden keine Anforderungen für Materialien generiert, die mit einem Ressourcenverbrauchsflag gekennzeichnet sind. | April – Oktober 2021 |
| Produktion | Stücklisten-/Formelpositionen mit Schrittverbrauch: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten-/Formelpositionen mit Schrittverbrauch ignoriert, wenn die Planungsoptimierung aktiviert ist. | 2021. Oktober |
| Produktion | Stücklisten mit konstantem Ausschuss oder variablem Ausschuss definiert: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten mit konstantem Ausschuss oder variablem Ausschuss ignoriert, wenn die Planungsoptimierung aktiviert ist. | Oktober 2021 - April 2022 |
| Produktion | Stücklisten mit Fremdarbeit: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten mit Fremdarbeit ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Oktober 2021 - April 2022 |
| Produktion | Stücklisten ohne Standort: _\#_ | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Produktionsplanung](production-planning.md) | Unterstützt |
| Produktion | Bedarf mit bestimmten definierten Stücklisten- oder Arbeitsplananforderungen: _\#_ | Diese Funktion steht noch aus. Derzeit werden die spezifischen Stücklisten- oder Routenanforderungen, die im Bedarf definiert sind (z. B. eine Unterstückliste oder Unterroute in einem Kundenauftrag), ignoriert, wenn die Planungsoptimierung aktiviert ist. Unabhängig von dieser Einstellung wird die Standardstückliste oder -Route verwendet. | Oktober 2021 - April 2022 |
| Produktion | Formelversionen mit Kuppel-/Nebenprodukten: _\#_ | Diese Funktion steht noch aus. Derzeit werden Kuppel-/Nebenprodukten, die der Formelversion zugeordnet sind, ignoriert, wenn die Planungsoptimierung aktiviert ist. | 2021. Oktober |
| Produktion | Formelversionen mit Ertrag: _\#_ | Diese Funktion steht noch aus. Derzeit wird Ertrag, der der Formelversion zugeordnet ist, ignoriert, wenn die Planungsoptimierung aktiviert ist. | Oktober 2021 - April 2022 |
| Produktion | Pläne einschließlich Abfolge: _\#_ | Diese Funktion steht noch aus. Derzeit werden Abfolgen ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Oktober 2021 - April 2022 |
| Produktion | Freigegebene, noch nicht gestartete Produktionsaufträge, deren Beginn vor heute geplant ist: _\#_ | Diese Funktion steht noch aus. Wenn sich ein Fertigungsauftrag verzögert, wird die Masterplanung derzeit davon ausgehen, dass er heute abgeschlossen wird. Dies ist für freigegebene Fertigungsaufträge relevant, bei denen ein Liefertermin in der Vergangenheit liegt, dieser jedoch noch nicht abgeschlossen wurde. | Oktober 2021 - April 2022 |
| Produktion | Mit begrenzter Kapazität eingeplante Ressourcen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Ressourcen mit begrenzter Kapazität ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Planung erfolgt basierend auf der Standardvorlaufzeit des Produkts. | Unendlich: Juni 2021, begrenzt: Oktober 2021 |
| Produktion | In Planung verwendete Arbeitspläne: _\#_ | Diese Funktion steht noch aus. Derzeit werden Arbeitspläne ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Standardvorlaufzeit des Produkts wird verwendet. | 2021. Juli |
| Produktion | Verkaufspositionsreservierung mit Stücklistenauflösung: _\#_ | Verkaufspositionsreservierung, die Auflösung verwendet, wird nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. | 2021. Oktober |
| Produktion | Planung mit Auflösung von Produktionsaufträgen: _\#_ | Terminplanung, die Auflösung von Produktionsaufträgen verwendet, wird nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Produktionsaufträge können individuell geplant werden. | 2021. Oktober |
| Angebotsanforderungen | Produktprogrammpläne mit aktivierten Angebotsanforderungen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Angebotsanfragen (RFQs) nicht als Bedarf betrachtet, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. | Oktober 2021 - April 2022 |
| Anforderungen | Produktprogrammpläne mit aktivierten Anforderungen: _\#_ | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Bestellanforderungen](purchase-requisitions.md) | Unterstützt |
| Sicherheitszuschläge | Dispositionssteuerungsgruppen mit Sicherheitszuschlag: _\#_ | Diese Funktion wird jetzt teilweise unterstützt. Weitere Informationen finden Sie unter [Sicherheitszuschläge](safety-margins.md) | Sicherheitszuschlag für Warenzugang: Unterstützt. Sicherheitszuschlag für Wiederbestellung und Warenabgang: April - Oktober 2021 |
| Sicherheitszuschläge | Produktprogrammpläne mit Sicherheitszuschlag: _\#_ | Diese Funktion wird jetzt teilweise unterstützt. Weitere Informationen finden Sie unter [Sicherheitszuschläge](safety-margins.md) | Sicherheitszuschlag für Warenzugang: Unterstützt. Sicherheitszuschlag für Wiederbestellung und Warenabgang: April - Oktober 2021 |
| Sicherheitslagerbestandserfüllung | Artikelabdeckungsaufzeichnungen mit Einstellung „Mindestbestand auffüllen“, die sich von „Heutiges Datum + Beschaffungszeit“ unterscheiden: _\#_ | Planungsoptimierung verwendet immer *Heutiges Datum + Beschaffungszeit*. Diese Änderung wird vorgenommen, um sich auf eine vereinfachte Planungskonfiguration in der Zukunft vorzubereiten und ein umsetzbares Ergebnis zu erzielen. Wenn die Beschaffungszeit für den Sicherheitsbestand nicht enthalten ist, werden Planaufträge, die für den aktuell niedrigen Lagerbestand erstellt werden, aufgrund der Vorlaufzeit immer verzögert. Dieses Verhalten kann zu erheblichen Störungen und unerwünschten Planaufträgen führen. Die beste Vorgehensweise besteht darin, die Einstellung so zu ändern, dass *Heutiges Datum + Beschaffungszeit* verwendet wird. Aktualisieren Sie die Stammdaten, um Warnungen zu vermeiden. | N/V |
| Verkaufsangebote | Produktprogrammpläne mit aktivierten Verkaufsangeboten: _\#_ | Diese Funktion steht noch aus. Derzeit werden Angebote ignoriert, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. | Oktober 2021 - April 2022 |
| Haltbarkeitsdatum | Produktprogrammpläne mit aktiviertem Haltbarkeitsdatum: _\#_ | Diese Funktion steht noch aus. Derzeit wird das Haltbarkeitsdatum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | 2021. Oktober |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Planungsoptimierung](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
