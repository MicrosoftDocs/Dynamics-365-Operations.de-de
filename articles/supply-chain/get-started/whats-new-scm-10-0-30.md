---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.30. (November 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.30 neu oder geändert wurden.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2983c113487934fd0751efcef9129e1f28d8dce8
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714797"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.30. (November 2022)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.30 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1362 und ist im folgenden Zeitplan verfügbar:

- **Vorschauversion:** September 2022
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** Oktober 2022
- **Allgemeine Verfügbarkeit von Release (automatisches Update):** November 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von   |
|---|---|---|---|
| Fertigung | [Überwachen Sie Geräte mit Sensor Data Intelligence](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligence-Startseite](../sensor-data-intelligence/sdi-home-page.md) | Funktionsverwaltung:<br>*(Vorschau) Sensor Data Intelligence* |
| Lagerortverwaltung | [Umleitungen auf mehreren Ebenen für die mobile Warehouse Management-App](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [Umleitungen für Schritte in den Menüpunkten des Mobilgeräts konfigurieren](../warehousing/warehouse-app-detours.md) | Funktionsverwaltung:<br>*Umleitungen auf mehreren Ebenen für die mobile Warehouse Management-App* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Produktionssteuerung | Verfügbare Informationen in Fertigungsaufträgen zur Freigabeseite | Fügt eine Spalte für die verfügbare Lagerbestandsmenge für den Einzelposten im Abschnitt „Positionen“ auf der **Fertigungsaufträge zur Freigabe**-Seite hinzu. |
| Transportverwaltung | Zugehörigen Routensegmenten Lieferungen zuweisen | Mit dieser Funktion kann das System die Frachtkosten der Sendungen genauer aufteilen, auch für Ladungen mit mehreren Sendungen, die entlang einer einzigen Route an verschiedene Zielsegmente geliefert werden. Sie ordnet jede Sendung anhand der Zieladressen von Sendung und Segment dem am besten geeigneten Routensegment zu. Die Funktion berechnet dann die Frachtkosten jeder Sendung als Anteil der Gesamtfrachtkosten der Ladung, basierend auf dem relativen Gewicht, Volumen, der Menge und der zurückgelegten Entfernung der Sendung. Diese Funktion gilt nur für Sendungen, die mit dem Modul Transportation Management (TMS) verwaltet werden. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Supply Chain Management 10.0.30 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattformupdates für Version 10.0.30 von Apps für Finanzen und Betrieb (November 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates der Version 10.0.30 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) an.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2022wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
