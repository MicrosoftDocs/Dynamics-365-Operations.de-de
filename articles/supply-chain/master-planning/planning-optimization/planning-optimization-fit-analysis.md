---
title: Planungsoptimierung Fit-Analyse
description: In diesem Thema wird erläutert, wie Sie Ihr aktuelles Setup und Ihre Daten mit den Möglichkeiten der Planungsoptimierungsfunktionalität verifizieren können.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9bf19604d246988e05b91c8a41b1f57b523d2192
ms.sourcegitcommit: 73ae66c9464bcc9ddc1efbf4e76abb2758862fe6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346652"
---
# <a name="planning-optimization-fit-analysis"></a>Planungsoptimierung Fit-Analyse

[!include [banner](../../includes/banner.md)]

Um zu sehen, wie kompatibel Ihr aktuelles Setup und Ihre Daten mit der Funktionalität der Planungsoptimierung sind, gehen Sie zu **Masterplanung** \> **Setup** \> **Planungsoptimierung Fit-Analyse**, und wählen Sie dann **Laufanalyse**. Wenn die Analyse Inkonsistenzen feststellt, werden diese auf der gleichen Seite aufgelistet. (Die Analyse kann einige Minuten dauern.)

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

Die folgende Tabelle zeigt die verschiedenen Ergebnisse, die nach einer Anpassungsanalyse angezeigt werden können. Nummernzeichen (_\#_) werden durch eine Zahl ersetzt, die die Anzahl der Datensätze angibt, bei denen das Problem aufgetreten ist.

| Funktion | Gelistetes Problem | Erläuterung |
| --- | --- | --- |
| Aktivitäten | Dispositionssteuerungsgruppen mit aktivierter Aktivitätenberechnung: _\#_ | Diese Funktion steht noch aus. Derzeit werden während der Masterplanung keine Aktionen generiert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. Der Hauptzweck von Aktionen besteht darin, Änderungen an bestehenden Aufträgen vorzuschlagen. |
| Basiskalender | Kalender, die den Basiskalender verwenden: _\#_ | Diese Funktion steht noch aus. Derzeit wird der Basiskalender ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Chargendispositionscodes | Nicht kompensierbare Chargendispositionsmaster: _\#_ | Diese Funktion steht noch aus. Derzeit werden Chargen-Dispositionscodes ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Verfügbarkeitszusage (CTP) | Standardauftragseinstellungen mit Lieferdatumskontrolle, die auf CTP eingestellt ist: _\#_ | Diese Funktion steht noch aus. Derzeit wird CTP ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |
| Statischen in dynamischen Plan kopieren | "Statischen in dynamischen Plan kopieren" ist in den Produktprogrammplanungsparametern aktiviert. | Die Planungsoptimierung kopiert den statischen Plan unabhängig von dieser Einstellung nicht in den dynamischen Plan. Im Allgemeinen ist dieses Konzept aufgrund der Geschwindigkeit und vollständigen Regeneration, die die Planungsoptimierung bietet, weniger relevant. Wenn zwei oder mehr Pläne verwendet werden, sollte für jeden Plan eine Masterplanung ausgelöst werden. |
| Umwandeln | Dispositionssteuerungsgruppen mit automatisch festgelegtem Sofortanlagezeitraum: _\#_ | In Version 10.0.7 und höher wird das Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion _Automatische Umwandlung zur Planungsoptimierung_ wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Festigung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Festlegung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Festigungszeitraum einbezogen werden muss. |
| Umwandeln | Artikeldeckungsdatensätze mit automatisch festgelegter Umwandlung: _\#_ | In Version 10.0.7 und höher wird das automatische Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion _Automatische Umwandlung zur Planungsoptimierung_ wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Festigung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Festlegung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Festigungszeitraum einbezogen werden muss. |
| Umwandeln | Produktprogrammpläne mit automatisch festgelegter Umwandlung: _\#_ | In Version 10.0.7 und höher wird das automatische Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion _Automatische Umwandlung zur Planungsoptimierung_ wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Festigung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Festlegung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Festigungszeitraum einbezogen werden muss. |
| FitAnalysisPlanningItems | Planungselemente: _\#_ | Diese Funktion steht noch aus. Derzeit werden Planungselemente wie normale Elemente behandelt, wenn die Planungsoptimierung aktiviert ist. |
| Planung | Abdeckungsgruppen mit „Intercompany-Bestellungen einschließen“ aktiviert: _\#_ | Diese Funktion steht noch aus. Derzeit enthält die Masterplanung keine nachgelagerten Planungsanforderungen, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. Beachten Sie, dass freigegebene/feste Bestellungen weiterhin mit der regulären Intercompany-Funktionalität funktionieren und die meisten Szenarien abdecken. |
| Planung | Abdeckungsgruppen mit der Einstellung „Planungswert verringern um“ auf einen anderen Wert als „Aufträge“ festgelegt: _\#_ | Standardmäßig verwendet die Planungsoptimierung unabhängig von dieser Einstellung „Planungswert verringern um“ für Bestellungen. |
| Planung | Planzahlenmodelle mit Untermodellen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Prognosen, die Untermodelle verwenden, nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. |
| Planung | Masterpläne mit aktivierter Option „Beschaffungsplanung einbeziehen“: _\#_ | Diese Funktion steht noch aus. Derzeit Beschaffungsplanungen nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. |
| Nichtplanungszeitraum | Dispositionssteuerungsgruppen mit gesperrtem festgelegtem Sofortanlagezeitraum: _\#_ | Der Sperrzeitraum wird nicht oft verwendet, und es ist derzeit nicht geplant, ihn für die Planungsoptimierung aufzunehmen. Derzeit wird der eingerichtete Sperrzeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |
| Nichtplanungszeitraum | Artikeldeckungsdatensätze mit gesperrtem festgelegtem Sofortanlagezeitraum: _\#_ | Der Sperrzeitraum wird nicht oft verwendet, und es ist derzeit nicht geplant, ihn für die Planungsoptimierung aufzunehmen. Derzeit wird der eingerichtete Sperrzeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |
| Nichtplanungszeitraum | Produktprogrammpläne mit gesperrtem festgelegtem Sofortanlagezeitraum: _\#_ | Der Sperrzeitraum wird nicht oft verwendet, und es ist derzeit nicht geplant, ihn für die Planungsoptimierung aufzunehmen. Derzeit wird der eingerichtete Sperrzeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |
| Intercompany | Produktprogrammpläne einschließlich geplanten Downstream-Bedarfs: _\#_ | Diese Funktion steht noch aus. Derzeit enthält die Masterplanung keine nachgelagerten Planungsanforderungen, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. Beachten Sie, dass freigegebene/feste Bestellungen weiterhin mit der normalen Intercompany-Funktionalität funktionieren und die meisten Szenarien abdecken. |
| Kanban | Artikeldeckungsdatensätze mit geplantem Auftragstyp "Kanban": _\#_ | Diese Funktion steht noch aus. Derzeit wird die auf Kanban eingestellte Artikelabdeckung ignoriert, wenn die Planungsoptimierung aktiviert ist. Die geplante Kanban-Auftragsart erstellt während der Masterplanung eine Warnung, und geplante Bestellungen werden erstellt, um den entsprechenden Bedarf zu decken. |
| Kanban | Artikel mit Standardauftragstyp „Kanban“: _\#_ | Derzeit wird die auf Kanban eingestellte Standardauftragsart ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Kanban-Standardauftragsart erstellt während der Masterplanung eine Warnung, und geplante Bestellungen werden erstellt, um den entsprechenden Bedarf zu decken. |
| Produktlebenszyklus-Status   | Produktlebenszyklus-Status nicht aktiv für die Planung: _\#_ | Dies ist eine ausstehende Funktion. Derzeit wird der Produktlebenszyklusstatus bei aktivierter Planungsoptimierung ignoriert. Sie können den Produktfilter auf Planebene anpassen, um zu vermeiden, dass Produkte einbezogen werden, bei denen der Status des Produktlebenszyklus für die Planung deaktiviert ist. |
| Produktion | Stücklistenpositionen mit Rundung oder mehreren Konfigurationen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Rundungen und mehrere Setups in Stücklistenzeilen ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. |
| Produktion | Stücklisten-/Formelpositionen mit Formelmessung: _\#_ | Diese Funktion steht noch aus. Derzeit wird Formelmessung in Stücklisten- und Formelzeilen ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. |
| Produktion | Stücklisten-/Formelpositionen mit Artikelersetzung (Plangruppen): _\#_ | Diese Funktion steht noch aus. Derzeit wird Artikelersetzung (Plangruppen) ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. |
| Produktion | Stücklisten-/Formelpositionen mit negativer Menge: _\#_ | Diese Funktion steht noch aus. Stücklisten-/Formelpositionen mit negativer Menge werden mit einer Menge von 0 (null) eingeschlossen, und eine Warnung wird ausgegeben, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Stücklisten-/Formelpositionen mit Ressourcenverbrauch: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten-/Formelpositionen mit Ressourcenverbrauch ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Stücklisten-/Formelpositionen mit Schrittverbrauch: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten-/Formelpositionen mit Schrittverbrauch ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Stücklisten mit konstantem Ausschuss oder variablem Ausschuss definiert: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten mit konstantem Ausschuss oder variablem Ausschuss ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Stücklisten mit Fremdarbeit: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten mit Fremdarbeit ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |
| Produktion | Stücklisten ohne Standort: _\#_ | Diese Funktion steht noch aus. Derzeit werden Stücklisten ohne Standort ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Bedarf mit bestimmten definierten Stücklisten- oder Arbeitsplananforderungen: _\#_ | Diese Funktion steht noch aus. Derzeit werden die spezifischen Stücklisten- oder Routenanforderungen, die im Bedarf definiert sind (z. B. eine Unterstückliste oder Unterroute in einem Kundenauftrag), ignoriert, wenn die Planungsoptimierung aktiviert ist. Unabhängig von dieser Einstellung wird die Standardstückliste oder -Route verwendet. |
| Produktion | Formelversionen mit Kuppel-/Nebenprodukten: _\#_ | Diese Funktion steht noch aus. Derzeit werden Kuppel-/Nebenprodukten, die der Formelversion zugeordnet sind, ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Formelversionen mit Ertrag: _\#_ | Diese Funktion steht noch aus. Derzeit wird Ertrag, der der Formelversion zugeordnet ist, ignoriert, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Pläne einschließlich Abfolge: _\#_ | Diese Funktion steht noch aus. Derzeit werden Abfolgen ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |
| Produktion | Freigegebene, noch nicht gestartete Produktionsaufträge, deren Beginn vor heute geplant ist: _\#_ | Diese Funktion steht noch aus. |
| Produktion | Mit begrenzter Kapazität eingeplante Ressourcen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Ressourcen mit begrenzter Kapazität ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Planung erfolgt basierend auf der Standardvorlaufzeit des Produkts. |
| Produktion | In Planung verwendete Arbeitspläne: _\#_ | Diese Funktion steht noch aus. Derzeit werden Arbeitspläne ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Standardvorlaufzeit des Produkts wird verwendet. |
| Produktion | Verkaufspositionsreservierung mit Stücklistenauflösung: _\#_ | Verkaufspositionsreservierung, die Auflösung verwendet, wird nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. |
| Produktion | Planung mit Auflösung von Produktionsaufträgen: _\#_ | Terminplanung, die Auflösung von Produktionsaufträgen verwendet, wird nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Produktionsaufträge können individuell geplant werden. |
| Angebotsanforderungen | Produktprogrammpläne mit aktivierten Angebotsanforderungen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Angebotsanfragen (RFQs) nicht als Bedarf betrachtet, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. |
| Anforderungen | Produktprogrammpläne mit aktivierten Anforderungen: _\#_ | Diese Funktion steht noch aus. Derzeit werden Anforderungen ignoriert, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. |
| Sicherheitszuschläge | Dispositionssteuerungsgruppen mit Sicherheitszuschlag: _\#_ | Diese Funktion steht noch aus. Derzeit wird der Sicherheitszuschlag ignoriert, wenn die Planungsoptimierung aktiviert ist. Um dieses Verhalten auszugleichen, können Sie die Vorlaufzeit so erhöhen, dass sie den Sicherheitszuschlag enthält. |
| Sicherheitszuschläge | Produktprogrammpläne mit Sicherheitszuschlag: _\#_ | Diese Funktion steht noch aus. Derzeit wird Sicherheitszuschlag ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. Um dieses Verhalten auszugleichen, können Sie die Vorlaufzeit so erhöhen, dass sie den Sicherheitszuschlag enthält. |
| Sicherheitslagerbestandserfüllung | Artikelabdeckungsaufzeichnungen mit Einstellung „Mindestbestand auffüllen“, die sich von „Heutiges Datum + Beschaffungszeit“ unterscheiden: _\#_ | Planungsoptimierung verwendet immer *Heutiges Datum + Beschaffungszeit*. Diese Änderung wird vorgenommen, um sich auf eine vereinfachte Planungskonfiguration in der Zukunft vorzubereiten und ein umsetzbares Ergebnis zu erzielen. Wenn die Beschaffungszeit für den Sicherheitsbestand nicht enthalten ist, werden Planaufträge, die für den aktuell niedrigen Lagerbestand erstellt werden, aufgrund der Vorlaufzeit immer verzögert. Dieses Verhalten kann zu erheblichen Störungen und unerwünschten Planaufträgen führen. Die beste Vorgehensweise besteht darin, die Einstellung so zu ändern, dass *Heutiges Datum + Beschaffungszeit* verwendet wird. |
| Verkaufsangebote | Produktprogrammpläne mit aktivierten Verkaufsangeboten: _\#_ | Diese Funktion steht noch aus. Derzeit werden Angebote ignoriert, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. |
| Haltbarkeitsdatum | Produktprogrammpläne mit aktiviertem Haltbarkeitsdatum: _\#_ | Diese Funktion steht noch aus. Derzeit wird das Haltbarkeitsdatum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Planungsoptimierung](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)
