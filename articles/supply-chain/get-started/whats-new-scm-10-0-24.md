---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.24 (Februar 2022)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Supply Chain Management 10.0.24 entweder neu oder geändert sind.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d7dd3bbb0d1aa701757ad7fa525aba04fe9419c9
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986302"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.24 (Februar 2022)

[!include [banner](../includes/banner.md)]

Dieses Thema listet Funktionen auf, die in Microsoft Dynamics 365 Supply Chain Management-Version 10.0.24 entweder neu sind oder geändert wurden. Diese Version hat die Build-Nummer 10.0.1084 und ist wie folgt verfügbar:

- **Vorschau des Release:** Dezember 2021
- **Allgemeine Verfügbarkeit des Releases (Selbst-Update):** Januar 2022
- **Allgemeine Verfügbarkeit des Releases (Auto-Update):** Februar 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Thema, um Funktionen einzubeziehen, die es in den Build geschafft haben, nachdem dieses Thema ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Verteilte Hybridtopologie | [Verbesserte Arbeitsauslastungen für Lagerausführung auf Skalierungseinheiten](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Workloads in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](../cloud-edge/cloud-edge-workload-warehousing.md) | Standardmäßig aktiviert. |
| Planung | [Planungsoptimierungsunterstützung für Sicherheitszuschlag für Wiederbestellung und Warenabgang](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Sicherheitszuschläge](../master-planning/planning-optimization/safety-margins.md) | Standardmäßig aktiviert. |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Produktionssteuerung | Bedarfsbasierte Materialverfügbarkeitsprüfung für Produktionsaufträge | Diese Funktion ermöglicht ein schnelleres Öffnen der Seite **Freigeben von Produktionsaufträgen**, die über den Arbeitsbereich **Produktionsbodenverwaltung** verfügbar ist. Ohne diese Funktion prüft das System beim Öffnen der Seite automatisch, ob für alle aufgelisteten Fertigungsaufträge Materialien verfügbar sind, was bei einer großen Auftragsmenge viel Zeit in Anspruch nehmen kann. Wenn diese Funktion aktiviert ist, stellt das System stattdessen eine Symbolleistenschaltfläche bereit, mit der Sie die Materialprüfung nur für ausgewählte Aufträge und bei Bedarf starten können. |
| Produktionssteuerung | (Vorschau) Materialverbrauch in der Produktionsausführungsoberfläche (nicht WMS) registrieren | Diese Funktion ermöglicht es Arbeitern, die Produktionsausführungsoberfläche zu verwenden, um Materialverbrauch, Chargennummern und Seriennummern zu registrieren. Diese Funktion unterstützt nur Artikel, die nicht für die Verwendung von erweiterten Lagerort-Prozessen (WMS) aktiviert sind. Die Unterstützung für WMS-fähige Elemente ist für eine zukünftige Version geplant.<p>Einige Hersteller, insbesondere in der Prozessindustrie, müssen den Materialverbrauch pro Charge oder Produktionsauftrag explizit erfassen. Mitarbeiter können beispielsweise eine Waage verwenden, um die Menge des bei der Arbeit verbrauchten Materials zu wiegen. Um eine vollständige Rückverfolgbarkeit des Materials zu gewährleisten, müssen diese Organisationen auch registrieren, welche Chargennummern bei der Herstellung jedes Produkts verbraucht wurden. |
| Produktionssteuerung | Fertigmeldung bei Arbeitsauslastung der Lagerortverwaltung für die Cloud- und Edge-Skalierungseinheit | Mit dieser Funktion können Mitarbeiter die mobile Warehouse Management-App verwenden, um einen Produktions‑ oder Batchauftrag als abgeschlossen zu melden, wenn die App für eine Arbeitsauslastung der Lagerortverwaltung auf einer Cloud‑ oder Edge-Skalierungseinheit ausgeführt wird. Weitere Informationen finden Sie unter [Fertig melden und auf einer Skalierungseinheit einlagern](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Produktionssteuerung | Produktionsauftrag starten bei Arbeitsauslastung der Lagerortverwaltung für die Cloud- und Edge-Skalierungseinheit | Mit dieser Funktion können Mitarbeiter die mobile Warehouse Management-App verwenden, um einen Produktions‑ oder Batchauftrag zu starten, wenn die App für eine Arbeitsauslastung der Lagerortverwaltung auf einer Cloud‑ oder Edge-Skalierungseinheit ausgeführt wird. |
| Lagerortverwaltung | Neue Workbenchseiten zur Ladungsplanung | Aktiviert die zwei neuen Ladungsplanungs-Workbenchseiten: **Workbench für eingehende Ladungsplanung** und **Workbench für ausgehende Ladungsplanung**. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfethemen kürzlich hinzugefügt oder erheblich aktualisiert. Diese Themen beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Themen |
|---|---|
| Kostenverwaltung | [Lagerwertberichte](../cost-management/inventory-value-report-storage.md) |
| Kostenverwaltung | [Beispiele und Logik für Lagerwertberichte](../cost-management/inventory-value-report-examples.md) |
| Produktprogrammplanung | [In der Planungsoptimierung verwendete Datums- und Zeitparameter](../master-planning/planning-optimization/date-time-used.md) |
| Produktprogrammplanung | [Einrichtung der Bedarfsplanung](../master-planning/demand-forecasting-setup.md) |
| Produktprogrammplanung | [Sicherheitsbestandserfassung verwenden, um die Mindestdeckung für Artikel zu aktualisieren](../master-planning/safety-stock-journal.md) |
| Produktionssteuerung | [Produktionsausführungsoberfläche anpassen](../production-control/production-floor-execution-customize.md) |
| Produktionssteuerung | [Stil der Produktionsausführungsoberflächenschnittstelle](../production-control/production-floor-execution-styles.md) |
| Vertrieb und Marketing | [Verbesserungen an der Leistung der Verkaufshistorienbereinigung](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Lagerortverwaltung | [Benutzerkonten für mobile Geräte](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Supply Chain Management 10.0.24 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattformupdates für Version 10.0.24 von Apps für Finanzen und Betrieb (November 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.24 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f) an.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2021wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Das Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
