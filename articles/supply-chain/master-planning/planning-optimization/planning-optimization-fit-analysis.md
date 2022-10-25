---
title: Passanalyse zur Planungsoptimierung
description: In diesem Artikel wird erläutert, wie Sie Ihr aktuelles Setup und Ihre Daten mit den Möglichkeiten der Planungsoptimierungsfunktionalität verifizieren können.
author: t-benebo
ms.date: 08/11/2022
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 15ec53c1f13b3017fb6e829bd1c8e99fbb938ce3
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689993"
---
# <a name="planning-optimization-fit-analysis"></a>Passanalyse zu Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Sie sollten das Ergebnis der Passanalyse der Planungsoptimierung als Teil des Migrationsprozesses analysieren. Beachten Sie, dass der Umfang der Planungsoptimierung nicht der aktuellen integrierten Produktprogrammplanungsfunktion entspricht. Wir empfehlen Ihnen, mit Ihrem Partner zusammenzuarbeiten und die Dokumentation zu lesen, um sich auf die Migration vorzubereiten. 

Mithilfe der Passanalyse für die Planungsoptimierung können Sie feststellen, wo sich das Ergebnis zwischen der integrierten Produktprogrammplanung-Engine und der Planungsoptimierung unterscheiden kann. Diese Analyse basiert auf Ihrem aktuellen Setup und Ihren Daten. 

Um das Ergebnis der Planungsoptimierungs-Passanalyse anzuzeigen, gehen Sie zu **Produktprogrammplanung** \> **Einstellungen** \> **Planungsoptimierungs-Passanalyse** und wählen dann **Analyse ausführen** aus. Wenn die Analyse Inkonsistenzen feststellt, werden diese auf der gleichen Seite aufgelistet. (Die Analyse kann einige Minuten dauern.)

> [!NOTE]
>
> - Einige Inkonsistenzen können von der Fit-Analyse der Planungsoptimierung nicht erkannt werden. Weitere Informationen finden Sie unter [Unterschiede zwischen klassischer Produktprogrammplanung und Planungsoptimierung](planning-optimization-differences-with-built-in.md).
>
> - Wenn Inkonsistenzen festgestellt werden, können Sie die Planungsoptimierung trotzdem nutzen. Die Ergebnisse der Fit-Analyse zeigen nur, an welchen Stellen der Planungsservice Ihr aktuelles Setup nicht berücksichtigt. Input

## <a name="analysis-results-example-1"></a>Analyseergebnisse: Beispiel 1

- **Funktion:** Produktion
- **Problem:** Artikel mit einer Stücklistenstufe größer als Null: 56
- **Erklärung:** Die Fit-Analyse ergab 56 Artikel, die eine Stückliste für die Produktion eingerichtet haben. Da die aktuelle Version der Planungsoptimierung die Produktion nicht unterstützt, erzeugt die Planungsoptimierung Planbestellungen anstelle von Planfertigungsaufträgen. Es wird auch eine Warnung angezeigt, die die betroffenen Elemente auflistet.

## <a name="analysis-results-example-2"></a>Analyseergebnisse: Beispiel 2

- **Funktion:** Aktionen
- **Problem:** Deckungsgruppen mit aktivierter Aktionsberechnung: 6
- **Erklärung:** Die Fit-Analyse ergab sechs Deckungsgruppen, in denen die Aktionsberechnung eingeschaltet ist. Da die aktuelle Version der Planungsoptimierung keine Aktionen unterstützt, werden bei der Masterplanung keine Aktionen generiert.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Übersicht möglicher Ergebnisse aus der Fit-Analyse

Die folgende Tabelle zeigt die verschiedenen Ergebnisse, die nach einer Anpassungsanalyse angezeigt werden können. Nummernzeichen (*\#*) werden durch eine Zahl ersetzt, die die Anzahl der Datensätze angibt, bei denen das Problem aufgetreten ist.

> [!IMPORTANT]
> Für Funktionen, die noch nicht unterstützt werden, enthält die folgende Tabelle voraussichtliche Verfügbarkeitsinformationen, die auf Grundlage unserer aktuellen Roadmap geschätzt werden. Diese Schätzungen können ohne Vorankündigung geändert werden.

| Funktion | Gelistetes Problem | Erläuterung | Erwartete Verfügbarkeit |
| --- | --- | --- | --- |
| Aktionen | Dispositionssteuerungsgruppen mit aktivierter Aktionsberechnung: *\#* | Diese Funktion wird jetzt unterstützt. | Unterstützt |
| Basiskalender | Kalender, die den Basiskalender verwenden: *\#* | Diese Funktion wird jetzt unterstützt. | Unterstützt | 
| Chargendispositionscodes | Nicht kompensierbare Chargendispositionsmaster: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Chargendispositionscodes verwenden, um Chargen als verfügbar oder nicht verfügbar zu markieren](../../inventory/batch-disposition-codes.md) | Unterstützt |
| Verfügbarkeitszusage (CTP) | Standardauftragseinstellungen mit Lieferdatumskontrolle, die auf CTP eingestellt ist: *\#* | In Supply Chain Management 10.0.28 und neuer stellt ein Prozess namens *CTP für Planungsoptimierung* bestätigte Versand- und Empfangsdaten zur Verfügung, nachdem der dynamische Plan ausgeführt wurde. Bei älteren Versionen von Supply Chain Management wird die veraltete CTP-Einstellung ignoriert, wenn die Planungsoptimierung aktiviert ist. | Unterstützt |
| Statischen in dynamischen Plan kopieren | "Statischen in dynamischen Plan kopieren" ist in den Produktprogrammplanungsparametern aktiviert. | Die Planungsoptimierung kopiert den statischen Plan unabhängig von dieser Einstellung nicht in den dynamischen Plan. Im Allgemeinen ist dieses Konzept aufgrund der Geschwindigkeit und vollständigen Regeneration, die die Planungsoptimierung bietet, weniger relevant. Wenn zwei oder mehr Pläne verwendet werden, sollte für jeden Plan eine Masterplanung ausgelöst werden. | Nicht zutreffend |
| Umwandeln | Dispositionssteuerungsgruppen mit automatisch umgewandeltem Umwandlungszeitraum: *\#* | In Version 10.0.7 und höher wird das Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion *Automatische Umwandlung zur Planungsoptimierung* wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Umwandlung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Umwandlung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Umwandlungszeitraum einbezogen werden muss. | Unterstützt |
| Umwandeln | Artikeldeckungsdatensätze mit automatisch festgelegter Umwandlung: *\#* | In Version 10.0.7 und höher wird das automatische Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion *Automatische Umwandlung zur Planungsoptimierung* wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Umwandlung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Umwandlung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Umwandlungszeitraum einbezogen werden muss. | Unterstützt |
| Umwandeln | Produktprogrammpläne mit automatisch festgelegter Umwandlung: *\#* | In Version 10.0.7 und höher wird das automatische Umwandeln nach Abschluss der Masterplanung als separater Umwandlungs-Batch-Job unterstützt (vorausgesetzt, die Funktion *Automatische Umwandlung zur Planungsoptimierung* wurde in der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert). Beachten Sie, dass die automatische Umwandlung für die Planungsoptimierung auf dem Bestelldatum (Startdatum) und nicht auf dem Anforderungsdatum (Enddatum) basiert. Dieses Verhalten stellt sicher, dass die Umwandlung von Planaufträgen rechtzeitig erfolgt, ohne dass die Vorlaufzeit in den Umwandlungszeitraum einbezogen werden muss. | Unterstützt |
| FitAnalysisPlanningItems | Planungselemente: *\#* | Diese Funktion steht noch aus. Derzeit werden Planungselemente wie normale Elemente behandelt, wenn die Planungsoptimierung aktiviert ist. | Veröffentlichungszyklus 2, 2022 oder später |
| Planung | Abdeckungsgruppen mit „Intercompany-Bestellungen einschließen“ aktiviert: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Intercompany-Planung](Intercompany-planning.md) | Unterstützt |
| Planung | Abdeckungsgruppen mit der Einstellung „Planungswert verringern um“ auf einen anderen Wert als „Aufträge“ festgelegt: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Produktprogrammplanung mit Bedarfsprognosen](demand-forecast.md) | Unterstützt |
| Planung | Planungszahlenmodelle mit Untermodellen: *\#* |  Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Produktprogrammplanung mit Bedarfsprognosen](demand-forecast.md) | Unterstützt |
| Planung | Masterpläne mit aktivierter Option „Beschaffungsplanung einbeziehen“: *\#* | Diese Funktion steht noch aus. Derzeit Beschaffungsplanungen nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. | Veröffentlichungszyklus 2, 2022 oder später |
| Nichtplanungszeitraum | Dispositionssteuerungsgruppen mit gesperrtem festgelegtem Nichtplanungszeitraum: *\#* | Diese Funktion steht noch aus. Derzeit wird der eingerichtete Nichtplanungszeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Nichtplanungszeitraum | Artikeldeckungsdatensätze mit gesperrtem festgelegtem Nichtplanungszeitraum: *\#* | Diese Funktion steht noch aus. Derzeit wird der eingerichtete Nichtplanungszeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Nichtplanungszeitraum | Produktprogrammpläne mit gesperrtem festgelegtem Nichtplanungszeitraum: *\#* | Diese Funktion steht noch aus. Derzeit wird der eingerichtete Nichtplanungszeitraum ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Intercompany | Produktprogrammpläne einschließlich geplanten Downstream-Bedarfs: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Intercompany-Planung](Intercompany-planning.md) | Unterstützt |
| Kanban | Artikeldeckungsdatensätze mit geplantem Auftragstyp "Kanban": *\#* | Diese Funktion steht noch aus. Derzeit wird die auf Kanban eingestellte Artikelabdeckung ignoriert, wenn die Planungsoptimierung aktiviert ist. Die geplante Kanban-Auftragsart erstellt während der Masterplanung eine Warnung, und geplante Bestellungen werden erstellt, um den entsprechenden Bedarf zu decken. | Zukünftiger Zyklus |
| Kanban | Artikel mit Standardauftragstyp „Kanban“: *\#* | Derzeit wird die auf Kanban eingestellte Standardauftragsart ignoriert, wenn die Planungsoptimierung aktiviert ist. Die Kanban-Standardauftragsart erstellt während der Masterplanung eine Warnung, und geplante Bestellungen werden erstellt, um den entsprechenden Bedarf zu decken. | Zukünftiger Zyklus |
| Produktlebenszyklus-Status | Produktlebenszyklus-Status nicht aktiv für die Planung: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Ausschließen von Produkten, die bestimmte Produktlebenszyklus-Status haben](product-lifecycle-state.md) | Unterstützt |
| Produktion | Stücklistenpositionen mit Rundung oder mehreren Konfigurationen: *\#* | Diese Funktion steht noch aus. Derzeit werden Rundungen und mehrere Setups in Stücklistenzeilen ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. | Zukünftiger Zyklus|
| Produktion | Stücklisten-/Formelpositionen mit Formelmessung: *\#* | Diese Funktion steht noch aus. Derzeit wird Formelmessung in Stücklisten- und Formelzeilen ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Stücklisten-/Formelpositionen mit Artikelersetzung (Plangruppen): *\#* | Diese Funktion steht noch aus. Derzeit wird Artikelersetzung (Plangruppen) ignoriert, wenn die Planungsoptimierung aktiviert ist, unabhängig von dieser Einstellung. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Stücklisten-/Formelpositionen mit negativer Menge: *\#* | Diese Funktion steht noch aus. Stücklisten-/Formelpositionen mit negativer Menge werden mit einer Menge von 0 (null) eingeschlossen, und eine Warnung wird ausgegeben, wenn die Planungsoptimierung aktiviert ist. Aktualisieren Sie die Stammdaten, um Warnungen zu vermeiden. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Stücklisten-/Formelpositionen mit Ressourcenverbrauch: *\#* | Diese Funktion steht noch aus. Derzeit werden Stücklisten-/Formelpositionen mit Ressourcenverbrauch ignoriert, wenn die Planungsoptimierung aktiviert ist. Wenn diese Funktion unterstützt wird, wird der Materialbedarf auf das Produktionsstartdatum festgelegt. Bis diese Funktion unterstützt wird, werden keine Anforderungen für Materialien generiert, die mit einem Ressourcenverbrauchsflag gekennzeichnet sind. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Stücklisten-/Formelpositionen mit Schrittverbrauch: *\#* | Diese Funktion steht noch aus. Derzeit werden Stücklisten-/Formelpositionen mit Schrittverbrauch ignoriert, wenn die Planungsoptimierung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Stücklisten mit konstantem Ausschuss oder variablem Ausschuss definiert: *\#* | Diese Funktion steht noch aus. Derzeit werden Stücklisten mit konstantem Ausschuss oder variablem Ausschuss ignoriert, wenn die Planungsoptimierung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Stücklisten mit Fremdarbeit: *\#* | Diese Funktion wird jetzt unterstützt. | Unterstützt |
| Produktion | Stücklisten ohne Standort: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Produktionsplanung](production-planning.md) | Unterstützt |
| Produktion | Bedarf mit bestimmten definierten Stücklisten- oder Arbeitsplananforderungen: *\#* | Diese Funktion steht noch aus. Derzeit werden die spezifischen Stücklisten- oder Routenanforderungen, die im Bedarf definiert sind (z. B. eine Unterstückliste oder Unterroute in einem Kundenauftrag), ignoriert, wenn die Planungsoptimierung aktiviert ist. Unabhängig von dieser Einstellung wird die Standardstückliste oder -Route verwendet. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Formelversionen mit Kuppel-/Nebenprodukten: *\#* | Diese Funktion steht noch aus. Derzeit werden Kuppel-/Nebenprodukten, die der Formelversion zugeordnet sind, ignoriert, wenn die Planungsoptimierung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Formelversionen mit Ertrag: *\#* | Diese Funktion steht noch aus. Derzeit wird Ertrag, der der Formelversion zugeordnet ist, ignoriert, wenn die Planungsoptimierung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Pläne einschließlich Abfolge: *\#* | Diese Funktion steht noch aus. Derzeit werden Abfolgen ignoriert, wenn die Planungsoptimierung unabhängig von dieser Einstellung aktiviert ist. | Veröffentlichungszyklus 2, 2022 |
| Produktion | Freigegebene, noch nicht gestartete Produktionsaufträge, deren Beginn vor heute geplant ist: *\#* | Diese Funktion steht noch aus. Wenn sich ein Produktionsauftrag verzögert, wird die Masterplanung derzeit davon ausgehen, dass er heute abgeschlossen wird. Dies ist für freigegebene Produktionsaufträge relevant, bei denen ein Liefertermin in der Vergangenheit liegt, dieser jedoch noch nicht abgeschlossen wurde. | Zukünftiger Zyklus |
| Produktion | Mit begrenzter Kapazität eingeplante Ressourcen: *\#* | Diese Funktion wird jetzt unterstützt.| Unterstützt |
| Produktion | In Planung verwendete Arbeitspläne: *\#* | Diese Funktion wird unterstützt. | Unterstützt |
| Produktion | Verkaufspositionsreservierung mit Stücklistenauflösung: *\#* | Verkaufspositionsreservierung, die Auflösung verwendet, wird nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. | Zukünftiger Zyklus |
| Produktion | Planung mit Auflösung von Produktionsaufträgen: *\#* | Terminplanung, die Auflösung von Produktionsaufträgen verwendet, wird nicht unterstützt, wenn die Planungsoptimierung aktiviert ist. Produktionsaufträge können individuell geplant werden. | Zukünftiger Zyklus |
| Angebotsanforderungen | Produktprogrammpläne mit aktivierten Angebotsanforderungen: *\#* | Diese Funktion steht noch aus. Derzeit werden Angebotsanforderungen (RFQs) nicht als Bedarf betrachtet, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. | Veröffentlichungszyklus 2, 2022 |
| Anforderungen | Produktprogrammpläne mit aktivierten Anforderungen: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Bestellanforderungen](purchase-requisitions.md) | Unterstützt |
| Sicherheitszuschläge | Dispositionssteuerungsgruppen mit Sicherheitszuschlag: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Sicherheitszuschläge](safety-margins.md) | Unterstützt |
| Sicherheitszuschläge | Produktprogrammpläne mit Sicherheitszuschlag: *\#* | Diese Funktion wird jetzt unterstützt. Weitere Informationen finden Sie unter [Sicherheitszuschläge](safety-margins.md) |  Unterstützt |
| Sicherheitslagerbestandserfüllung | Artikelabdeckungsaufzeichnungen mit Einstellung „Mindestbestand auffüllen“, die sich von „Heutiges Datum + Beschaffungszeit“ unterscheiden: *\#* | Planungsoptimierung verwendet immer *Heutiges Datum + Beschaffungszeit*. Diese Änderung wird vorgenommen, um sich auf eine vereinfachte Planungskonfiguration in der Zukunft vorzubereiten und ein umsetzbares Ergebnis zu erzielen. Wenn die Beschaffungszeit für den Sicherheitsbestand nicht enthalten ist, werden Planaufträge, die für den aktuell niedrigen Lagerbestand erstellt werden, aufgrund der Vorlaufzeit immer verzögert. Dieses Verhalten kann zu erheblichen Störungen und unerwünschten Planaufträgen führen. Die beste Vorgehensweise besteht darin, die Einstellung so zu ändern, dass *Heutiges Datum + Beschaffungszeit* verwendet wird. Aktualisieren Sie die Stammdaten, um Warnungen zu vermeiden. | N/V |
| Verkaufsangebote | Produktprogrammpläne mit aktivierten Verkaufsangeboten: *\#* | Diese Funktion steht noch aus. Derzeit werden Angebote ignoriert, wenn die Planungsoptimierung aktiviert ist. Sie werden unabhängig von dieser Einstellung ignoriert. | Veröffentlichungszyklus 2, 2022 oder später |
| Haltbarkeitsdatum | Produktprogrammpläne mit aktiviertem Haltbarkeitsdatum: *\#* | Diese Funktion steht noch aus. | Veröffentlichungszyklus 2, 2022 |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht zur Planungsoptimierung](planning-optimization-overview.md)

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Unterschiede zwischen der klassischen Masterplanplanung und der Planungsoptimierung](planning-optimization-differences-with-built-in.md)

[In der Planungsoptimierung nicht verwendete Parameter](not-used-parameters.md)

[Planhistorie und Planungsprotokolle einsehen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
