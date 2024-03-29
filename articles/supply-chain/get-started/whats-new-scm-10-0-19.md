---
title: Was ist neu oder geändert in Dynamics 365 Supply Chain Management Version 10.0.19 (Juni 2021)
description: Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Supply Chain Management 10.0.19 sind.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de9d20ba7ffc0bc5201ccafc2157a13983923249
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9125021"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Was ist neu oder geändert in Dynamics 365 Supply Chain Management Version 10.0.19 (Juni 2021)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.19 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.837 und ist wie folgt verfügbar:

- **Vorschau auf die Veröffentlichung:** April 2021
- **Allgemeine Verfügbarkeit der Freigabe (Selbst-Update):** Juni 2021
- **Allgemeine Verfügbarkeit der Version (Auto-Update):** Juni 2021

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation.

Die meisten dieser Funktionen müssen aktiviert werden mithilfe von [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), bevor Sie sie verwenden können.

| Funktionsbereich | Funktion | Weitere Informationen |
|---|---|---|
| Bestand&nbsp;und&nbsp;Logistik | [Die vom Kreditor übermittelte Bankverbindung genehmigen und speichern](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Kontoinformationen von Kreditoren pflegen](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Bestand und Logistik | [Optimierung beim Export von Datenentitäten der Kontaktperson](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Wenn diese Funktion aktiviert ist, werden zugehörige Aufträge (oder Positionen) nicht aufgrund von Änderungen an referenzierten Daten im nächsten inkrementellen Export berücksichtigt. Wenn diese Funktion deaktiviert ist, werden zugehörige Aufträge (oder Positionen) nicht aufgrund von Änderungen an referenzierten Daten im nächsten inkrementellen Export berücksichtigt. |
| Bestand und Logistik | [Erweiterungen der Funktionalitäten für die Lagerort-Ausführung mit Scale-Units](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Nachrichtenverarbeitungsmeldungen](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Lagerregulierung des Lagerorts](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Workloads in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Bestand und Logistik | [Nachschlagefeld für die Felder Belegeinleitung und Belegabschluss auf der Angebotsseite](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Diese Funktion fügt das Nachschlagefeld für die Felder **Belegeinleitung** und **Belegabschluss** auf der Seite **Verkaufsangebot** hinzu.<br><br>Diese Funktion ist standardmäßig aktiviert. |
| Bestand und Logistik | [Lagerort-Ausführung mit Edge Scale-Einheiten auf Ihrer angepassten Hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Skalierte Einheiten auf angepasster Hardware mit LBD bereitstellen](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Fertigung | [Fertigungsausführung mit Scale-Einheiten auf Ihrer angepassten Hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Skalierte Einheiten auf angepasster Hardware mit LBD bereitstellen](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planung | Abfragebasierte geplanter Auftrag umwandeln | [Fest geplante Aufträge](../master-planning/planning-optimization/planned-order-firming.md) |
| Produktinformationsverwaltung | [Verbesserungen an der Seite mit Variantenvorschlägen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Vordefinierte Produktvarianten erstellen](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet eine schrittweise Verbesserung einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben). Wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktion&nbsp;Name&nbsp;in Funktion&nbsp;Verwaltung | Mehr erfahren |
|---|---|---|
| Vertrieb und Marketing | Leistungsverbesserungen bei der Bereinigung des Verkaufsverlaufs | Die Bereinigung des Verkaufsverlaufs kann lange dauern, wenn sie in Umgebungen mit einem hohen Volumen an Verkaufsaktualisierungen nur selten ausgeführt wird. Um die Dauer zu verringern und die Zuverlässigkeit zu verbessern, teilt diese Funktion die Bereinigung in Stapel auf, die für eine begrenzte Dauer ausgeführt werden. Wenn möglich werden Datenbankfunktionen genutzt, um das Sperren zu minimieren und das Verbinden von Transaktionstabellen während der Bereinigung zu vermeiden. Weitere Informationen finden Sie unter [Datenbereinigung der Verkaufshistorie planen](../sales-marketing/sales-update-history-cleanup-performance-improvements.md). |
| Vertrieb und Marketing | Angefordertes Wareneingangsdatum mit bestätigtem Datum bei Intercompany-Aufträgen aktualisieren | Mit dieser Funktion können Sie steuern, was mit den Feldwerten für Verkaufs- und Kaufdatum geschieht, wenn Sie die konzerninterne Direktlieferung verwenden. Sie können wählen, ob das System die angeforderten Daten aktualisiert oder die Aktualisierung überspringt. Wenn Sie die Aktualisierung überspringen, entsprechen die angeforderten Daten den Anforderungen des Kunden. Wenn Sie die Aktualisierung aktivieren, stellen die angeforderten Daten (bei Verwendung der Lieferterminsteuerung) zunächst nur das dar, was der Kunde angefordert hat. Kontrolle des Liefertermins, falls abweichend von *Keiner* wird außer Kraft setzen, was ursprünglich angefordert wurde. Sie können diese Option mit der neuen Option **Aktualisieren Sie das angeforderte Empfangsdatum mit dem bestätigten Datum** in den Einstellungen des konzerninternen Anbieters oder Kunden einstellen.<br><br>Wenn die Funktion deaktiviert ist, überschreibt das System das angeforderte Empfangsdatum für ursprüngliche Kundenaufträge basierend auf der Regel zur Kontrolle des Lieferdatums. Das angeforderte Versanddatum bleibt jedoch unverändert. |
| Lagerortverwaltung | Mengen bei Freigabe an Lager auf nächste Verkaufseinheit abrunden | Diese Funktion fügt eine Option hinzu, mit der die Bestellmengen bei der Freigabe an das Lager eingeschränkt werden können. Wenn diese Option aktiviert ist, werden Bestellmengen auf die nächste ganze Verkaufseinheit abgerundet, und Bestellungen, die Mengen für weniger als eine Verkaufseinheit enthalten, werden zur Freigabe abgelehnt. |
| Lagerortverwaltung | Organisationsweite Zyklusmethode „Arbeitserstellung planen“ | Bei Aktivierung dieser Funktion wird die Wellenmethode *Arbeitserstellung planen* so konfiguriert, dass sie für alle juristischen Personen parallel ausgeführt wird. Einige zusätzliche Einstellungen sind ebenfalls betroffen. Alle Details finden Sie unter [Planen der Arbeitserstellung während der Welle](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Sie beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt, aber sie können Ihnen helfen, mehr aus den vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Verwaltung für technische Änderung | [Fragen zur Verwaltung für technische Änderungen](../engineering-change-management/change-management-faq.md) |
| Beschaffung | [Kategorie-Anforderungen von Anbietern](../procurement/category-requests-from-vendors.md) |
| Produktinformationsverwaltung | [Maßeinheit verwalten](../pim/tasks/manage-unit-measure.md)<br><br>[Berechnungen für Produktkonfigurationsmodelle](../pim/config-model-calculations.md) |
| Produktionssteuerung | [Vereinheitlichte Nummernkreise für Einzelvorgangskennungen](../production-control/unified-job-ids.md) |
| Transportverwaltung | [LTL-Klassen](../transportation/ltl-class.md)<br><br>[NMFC-Codes](../transportation/nmfc-codes.md) |
| Lagerortverwaltung, Wellenerstellung und -verarbeitung | [Zykluserstellung und -verarbeitung](../warehousing/wave-processing.md)<br><br>[Lagerparameter für Wellenverarbeitung](../warehousing/wave-warehouse-parameters.md)<br><br>[Wellenvorlagen](../warehousing/wave-templates.md)<br><br>[Wellenzuteilung](../warehousing/wave-allocation-method.md)<br><br>[Arbeitserstellung während Welle planen](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Containerisierung](../warehousing/wave-containerization.md)<br><br>[Wellenausführungsbenachrichtigungen](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattform-Updates für Finanz- und Betriebs-Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.19 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.19 der Finanz- und Betriebs-Apps (Juni 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.19 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415) an.

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

