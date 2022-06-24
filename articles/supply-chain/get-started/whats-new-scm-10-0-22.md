---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.22. (November 2021)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.22 neu oder geändert wurden.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 53f1670454ef505e61e96b16990d913473b46bf4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849502"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.22. (November 2021)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.22 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.995 und ist wie folgt verfügbar:

- **Vorschauversion:** September 2021
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** Oktober 2021
- **Allgemeine Verfügbarkeit von Release (automatisches Update):** November 2021

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation. Informationen zum Aktivieren einer Funktion finden Sie in der Spalte *Aktiviert von*. Weitere Informationen zur Funkions-Verwaltung finden Sie unter [Funktions-Verwaltung Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Möglicherweise aktualisieren wir diesen Artikel, um Funktionen einzubeziehen, die es in den Build geschafft haben, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von   |
|---|---|---|---|
| Planung | [Planungsoptimierungsunterstützung für die fähigkeitsbasierte Ressourcenzuweisung](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planung mit Ressourcenauswahl basierend auf der Funktion](../master-planning/planning-optimization/capability-based-scheduling.md) | Funktionsverwaltung (*Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben). Wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Verteilte Hybridtopologie | *(Es ist keine Funktionsverwaltung erforderlich.)* | <p>Diese Version erweitert die Ladungsplanungsfunktionen der Lagerverwaltungs-Workload für Cloud- und Edge-Skalierungs-Einheiten.</p><p>Weitere Informationen finden Sie unter [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Verwaltung für technische Änderung | Variantengenerierung für technische Produkte | <p>Mit dieser Funktion können Sie basierend auf Farbe, Größe, Stil oder Konfigurationsabmessungen mehrere Varianten für ein technisches Produkt generieren.</p><p>Weitere Informationen finden Sie unter [Generieren Sie Varianten für Engineering-Produkte](../engineering-change-management/engineering-variants.md).</p> |
| Lager- und Lagerortverwaltung | Integration der Bestandssichtbarkeit mit Reservierungsversatz | <p>Diese Funktion kann erst aktiviert werden, nachdem die *Integration der Inventarsichtbarkeit* Funktion aktiviert ist. Es bietet Funktionen zum Ausgleichen von Reservierungen, die in der Inventarsichtbarkeit vorgenommen werden.</p><p>Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](../inventory/inventory-visibility-reservations.md).</p> |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Diese Artikel beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Verwaltung für technische Änderung | [Überblick über das Änderungsmanagement](../engineering-change-management/product-engineering-overview.md) listet jetzt alle zugehörigen, optionalen Funktionen auf, die in der Funktionsverwaltung verfügbar sind |
| Produktprogrammplanung | [Einrichtung der Bedarfsplanung](../master-planning/demand-forecasting-setup.md) |
| Produktprogrammplanung | [Nettobedarf und Informationen zum Bedarfsverursacher in der Planungsoptimierung](../master-planning/planning-optimization/net-requirements.md) |
| Lagerortverwaltung | [Freigabe ins Lager](../warehousing/release-to-warehouse-process.md) bietet einen detaillierten Überblick über den vollständigen Freigabeprozess im Lager |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Supply Chain Management 10.0.22 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattformupdates für Version 10.0.22 von Apps für Finanzen und Betrieb (November 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.22 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) an.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2021 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2021wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
