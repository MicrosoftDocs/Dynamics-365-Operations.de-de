---
title: Neuerungen und Änderungen in Dynamics 365 Supply Chain Management 10.0.28 (August 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.28 neu oder geändert wurden.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7e17127ff6ef6c52034b8aa5e0c8404772363ca9
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186518"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10028-august-2022"></a>Neuerungen und Änderungen in Dynamics 365 Supply Chain Management 10.0.28 (August 2022)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.28 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1264 und ist im folgenden Zeitplan verfügbar:

- **Vorschau auf die Veröffentlichung:** Mai 2022
- **Allgemeine Verfügbarkeit der Freigabe (Selbst-Update):** Juli 2022
- **Allgemeine Verfügbarkeit der Version (Auto-Update):** Juli 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Bestand und Logistik | [Entitäten zur Integration von Gesamttransportkosten für Speditionen Dritter](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Gesamttransportkosten Entitäten Übersicht](../landed-cost/landed-cost-entities-overview.md) | Standardmäßig aktiviert |
| Planung | [Bedarfsgesteuerte Materialbedarfsplanung (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | [Bedarfsgesteuerte Planung im Überblick](../master-planning/planning-optimization/ddmrp-overview.md) | Funktionsverwaltung:<br>*(Vorschauversion) DDMRP für Planungsoptimierung* |
| Planung | [Unterstützung der Planungsoptimierung für Verfügbarkeitszusagen (CTP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capable-to-promise-ctp) | Demnächst | Funktionsverwaltung:<br>*(Vorschauversion) Verfügbarkeitszusage für die Planungsoptimierung* |
| Planung | [Unterstützung der Planungsoptimierung für die Haltbarkeitsdauer](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Demnächst | Standardmäßig aktiviert |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Lager- und Lagerortverwaltung | Aktivieren Sie den Intercompany Lagerbestand, um nur Lagerbestände ungleich Null anzuzeigen. | Mit dieser Funktion können Sie festlegen, ob Artikel mit einem Lagerbestand von Null in die Intercompany-Bestandsliste aufgenommen werden sollen. Sie können diese Option über die Einstellung **Artikel mit einem Lagerbestand von Null in der Intercompany-Bestandsliste nicht anzeigen** steuern, die diese Funktion auf der Seite **Parameter der Bestands- und Lagerverwaltung** festlegt. |
| Lager- und Lagerortverwaltung | (Indien) Bei Verrechnungspreisregeln wird der Lagerplatz ignoriert, wenn „Von Lagerortcode“ auf „Alle“ festgelegt ist. | <p>Diese Funktion gilt nur für indische Lokalisierungen. Es macht das Festlegen von Transferpreisen für Artikel in Umlagerungen intuitiver.</p><p>Sie legen die Verrechnungspreise fest, indem Sie jeden Artikel mit Verrechnungspreisregeln konfigurieren. Eine Möglichkeit, diese Konfiguration vorzunehmen, besteht darin, eine Regelzeile einzufügen, in der das Feld **Aus Lagercode** auf *Alle* festgelegt ist. Diese Einstellung gibt an, dass der in der Zeile festgelegte Verrechnungspreis unabhängig von dem Lager gelten soll, aus dem der Artikel kommissioniert wird. Wenn diese Funktion aktiviert ist, ignorieren Verrechnungspreisregeln, bei denen das Feld **Aus Lagercode** auf *Alle* festgelegt ist, die Einstellung **Ort**. Daher gilt die Regel unabhängig von dem Ort, der auf dem Umlagerungsauftrag angegeben ist. Dieses Verhalten ist wahrscheinlich das, was erwartet wird, da der Ort in der Hierarchie der Dimensionen unterhalb des Lagers liegt.</p><p>Ohne diese Funktion wendet das System Regeln dieser Art nur an, wenn der Ort auf dem Umlagerungsauftrag genau mit dem Ort übereinstimmt, der für die Regel festgelegt ist. (Wenn für die Regel ein leerer Ort festgelegt ist, wendet das System die Regel nur auf Umlagerungsaufträge an, die ebenfalls einen leeren Wert für den Ort haben.)</p> |
| Lager- und Lagerortverwaltung | Daten im Lagerbestandbericht bereinigen | Mit dieser Funktion können Sie die Daten bereinigen, die zum Erstellen von *Bestandsberichten für Lagerbestände* verwendet werden. |
| Produktionssteuerung | Projektaktivitäten für Servicevertrags- und Serviceauftragszeilen zuweisen | Diese Funktion fügt den Zeilen von Servicevereinbarungen und Serviceaufträgen ein Feld mit der Bezeichnung **Projektaktivität** hinzu, so dass Sie eine Projektaktivität für diese Zeilen festlegen können. Die Funktion hilft Ihnen, Blockierungsfehler zu vermeiden, wenn Sie Erfassungen von Service-Management-Projekten buchen, die das Festlegen einer Projektaktivität erfordern.  |
| Lagerortverwaltung | Dienst zur manuellen Auswahl von Umlagerungszeilen für Admins oder ähnliche vertrauenswürdige Benutzer | Mit dieser Funktion können Administratoren manuell Transaktionen im Bestand kommissionieren, die mit Transferzeilen in Verbindung stehen. Zu diesen Zeilen gehören auch Zeilen, die bereits an das Lager freigegeben wurden. Administratoren sollten diese Kommissionierung nur in Ausnahmefällen vornehmen, z.B. wenn sich das System in einem beschädigten Zustand befindet. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Diese Artikel stehen nicht unbedingt im Zusammenhang mit den neuen Funktionen, die für diese Version hinzugefügt wurden, wie in den vorherigen Abschnitten aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Kostenverwaltung | [Fester Zugangspreis](../cost-management/fixed-receipt-price.md) |
| Kostenverwaltung | [Häufig gestellte Fragen zur Nachkalkulation von Beständen](../cost-management/inventory-costing-faq.md) |
| Kostenverwaltung | [Buchhaltungsregel „Auf Belastungskonto buchen“](../cost-management/post-to-charge-account-accounting-principle.md) |
| Lagerverwaltung | [Lagerbuchungsdetails](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattform-Updates für Finanz- und Betriebs-Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.28 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.28 der Finanz- und Betriebs-Apps (Juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.28 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) an.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan](/dynamics365-release-plan/2022wave1/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

