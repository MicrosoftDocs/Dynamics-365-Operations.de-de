---
title: Neuerungen und Änderungen in Dynamics 365 Supply Chain Management 10.0.20 (August 2021)
description: Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Supply Chain Management 10.0.20 sind.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d99a7a7d0261ba0afd19efbb237dff329527723d
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219153"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Neuerungen und Änderungen in Dynamics 365 Supply Chain Management 10.0.20 (August 2021)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.20 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.886 und ist wie folgt verfügbar:

- **Vorschau auf die Veröffentlichung:** Mai 2021
- **Allgemeine Verfügbarkeit der Freigabe (Selbst-Update):** Juli 2021
- **Allgemeine Verfügbarkeit der Version (Auto-Update):** August 2021

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation.

Die meisten dieser Funktionen müssen aktiviert werden mithilfe von [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), bevor Sie sie verwenden können.

| Funktionsbereich | Funktion | Weitere Informationen |
|---|---|---|
| Bestand&nbsp;und&nbsp;Logistik | [Auftragsdetails – Leistungsverbesserung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Durch diese Funktion reagiert die Benutzeroberfläche beim Öffnen von Kundenaufträgen schneller, insbesondere bei Aufträgen mit vielen Zeilen. |
| Fertigung | [Rufen Sie Prozessautomatisierungsabläufe auf, um Qualitätsaufträge zu erstellen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Rufen Sie Prozessautomatisierungsabläufe auf, um Qualitätsaufträge zu erstellen](../production-control/process-automation-quality-orders.md ) |
| Fertigung | [Verbessere Steuerelementformate für Benutzeroberflächen für Produktionsausführung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Produktionsausführungsoberfläche konfigurieren](../production-control/production-floor-execution-configure.md) |
| Planung | [Endloskapazitätsplanung zur Planungsoptimierung](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Zeitplanung mit unbegrenzter Kapazität](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Produktinformationsverwaltung | [Änderungen in Formeln und deren Bestandteile verwalten](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Verwalten Sie Änderungen in Formeln und deren Substanzen](../engineering-change-management/manage-formula-changes.md) |
| Produktinformationsverwaltung | [Produktbereitschaftsprüfungen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Produktbereitschaft](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet eine schrittweise Verbesserung einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben). Wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktion&nbsp;Name&nbsp;in Funktion&nbsp;Verwaltung | Mehr erfahren |
|---|---|---|
| Produktprogrammplanung | Parallele Autorisierung der angepassten Bedarfsplanung | Diese Funktion ermöglicht die parallele Autorisierung der angepassten Bedarfsprognose aus der Seite **Angepasste Nachfrageprognose**. Mit dieser Funktion soll die Leistung gesteigert werden, wenn eine große Anzahl von Prognosen genehmigt wird. Bei der Autorisierung kann der Benutzer die **Anzahl der Themen** im Autorisierungsdialog angeben. |
| Produktprogrammplanung | Chargenfähige Umwandlung und Konsolidierung für geplante Sammel- und Verpackungschargenaufträge | Mit dieser Funktion können Sie Batchaufträge verwenden, um geplante Sammel- und Verpackungsaufträge zu konsolidieren. |
| Produktionssteuerung | Generische Arbeitspläne kopieren | Diese Funktion erweitert die Funktion zum Kopieren von Routen, sodass Benutzer Routen kopieren können, die nicht objektspezifisch sind. Es ermöglicht dem System, alle relevanten Informationen (wie Standort, Routengruppe, Ressourcenanforderungen und verschiedene Zeiten) zu aktualisieren, nachdem die Funktion zum Kopieren von Routen zum Überschreiben einer Route verwendet wurde, die noch keinem Element zugewiesen ist. |
| Produktionssteuerung | Zugehörige Ressourcenanforderungen bei Änderung eines Arbeitsplanvorgangs aktualisieren | Mit dieser Funktion kann das System die zugehörigen Ressourcenanforderungen aktualisieren, nachdem ein Benutzer den Vorgang eines vorhandenen Arbeitsplanschritts geändert hat. |
| Produktinformationsverwaltung | Die Stückliste meldet eine Vorverarbeitung, um Zeitüberschreitungen zu vermeiden | Diese Funktion bewirkt, dass der Stücklistenbericht vorverarbeitet wird. Dadurch werden Zeitüberschreitungsprobleme vermieden, wenn der Bericht eine große Datenlast aufweist. |
| Beschaffung | Zurücksetzen beschaffungsbezogener Workflows aktivieren | Mit dieser Vorschaufunktion können Sie die folgenden Workflows auf den Entwurfsstatus zurücksetzen: Bestellung, Lieferantenwechsel und Bestellanforderungen. |
| Transportverwaltung | Erstellung einer Erfassung vom Typ „Kreditorenrechnung“ beim Verwerfen eines Frachtbriefs aktivieren | Wenn diese Funktion aktiviert ist, wird ein entsprechendes Lieferantenrechnungsjournal nur aus Abstimmungsgründen erstellt, wenn Sie die Option Kreditorenzahler verwenden. Andernfalls wird immer das Rechnungsjournal erstellt. |
| Lagerortverwaltung | Für Wiederbeschaffungsaufträge ausgewählte Vorlagen überprüfen | Mit dieser Funktion können Sie sicherstellen, dass Benutzer beim Einrichten eines Wiederbeschaffungsauftrags gültige Wiederbeschaffungsvorgänge auswählen. Es verhindert, dass Benutzer einen Wiederbeschaffungs-Einzelvorgang ohne Vorlage erstellen und Vorlagen vom Typ *Wellenbedarf* ausführen. Dies führt zu keiner Wiederbeschaffungsarbeit und kann lange dauern. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Sie beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt, aber sie können Ihnen helfen, mehr aus den vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Verwaltung für technische Änderung | [Zustände und Transaktionen im Produktlebenszyklus](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Lagerverwaltung | [Add-In Bestandstransparenz](../inventory/inventory-visibility.md)<br><br>[Überblick über die Qualitäts- und Qualitätsmangelverwaltung](../inventory/quality-management-processes.md) (plus alle verwandten Artikel der Qualitätsverwaltung) |
| Beschaffung | [Herstellerzertifizierung pflegen](../../finance/public-sector/manage-vendor-certification.md) |
| Produktionssteuerung | [Stil der Produktionsausführungsoberflächenschnittstelle](../production-control/production-floor-execution-styles.md) |
| Lagerortverwaltung | [Weisen Sie der mobilen Warehouse Management-App Schrittsymbole und -titel zu](../warehousing/step-icons-titles.md)<br><br>[Aufgeschobene Verarbeitung von manuellen Bestandsbewegungen](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattform-Updates für Finanz- und Betriebs-Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.20 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.20 der Finanz- und Betriebs-Apps (Juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.20 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) an. 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 Veröffentlichungsplan Welle 1

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Testen Sie [Dynamics 365: 2021 Release Welle 1 Plan](/dynamics365-release-plan/2021wave1/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

