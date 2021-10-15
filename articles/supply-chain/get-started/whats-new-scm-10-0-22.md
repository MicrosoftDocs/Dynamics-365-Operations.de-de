---
title: Vorschau auf Dynamics 365 Supply Chain Management 10..22 (November 2021)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Supply Chain Management 10.0.22 entweder neu oder geändert sind.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3f5166338aebe784fe7f95372a437d4ed660de77
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579711"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Vorschau auf Dynamics 365 Supply Chain Management 10..22 (November 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema werden die Funktionen aufgeführt, die in der Microsoft Dynamics 365 Supply Chain Management Vorschauversion 10.0.22 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.995 und ist wie folgt verfügbar:

- **Vorschauversion:** September 2021
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** Oktober 2021
- **Allgemeine Verfügbarkeit von Release (automatisches Update):** November 2021

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Die Spalte *Funktion* bietet Links zum [Release-Plan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features), wo Sie die offiziellen Release-Termine für jede Funktion sehen können. Die Spalte *Weitere Informationen* enthält weitere Informationen und/oder Links zur zugehörigen Dokumentation. Informationen zum Aktivieren einer Funktion finden Sie in der Spalte *Aktiviert von*. Weitere Informationen zur Funkions-Verwaltung finden Sie unter [Funktions-Verwaltung Übersicht](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Möglicherweise aktualisieren wir dieses Thema, um Funktionen einzubeziehen, die es in den Build geschafft haben, nachdem dieses Thema ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von   |
|---|---|---|---|
| Planung | [Planungsoptimierungsunterstützung für die fähigkeitsbasierte Ressourcenzuweisung](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planung mit Ressourcenauswahl basierend auf der Funktion](../master-planning/planning-optimization/capability-based-scheduling.md) | Funktionsverwaltung (*Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung*) |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben). Wenn Sie eine dieser Funktionen verwenden möchten, müssen Sie sie explizit aktivieren unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktionsbereich | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Kostenverwaltung | Erstellen Sie zugehörige Belege für Neubewertungen der Standardkostenrundung | <p>Wenn eine Bestandsfinanzbuchung (z. B. eine Kundenauftragsrechnung oder eine Bestandsbuchung) vorgenommen wird, veranlasst diese Funktion das System, einen separaten Beleg für alle zugehörigen Standardkostenrundungs-Neubewertungen zu erstellen und diesen als zugehörigen Beleg an den Finanzbuchungsbeleg anzuhängen.</p><p>Ohne diese Funktion zeichnet das System die Neubewertungen der Standardkostenrundung auf derselben Belegbuchung auf. Dieses Verhalten kann manchmal zu widersprüchlichen Datumsangaben führen, da die Neubewertungen das Sitzungs- oder Systemdatum verwenden, während Finanzbuchungen das Buchungsdatum verwenden.</p> |
| Verteilte Hybridtopologie | *(Es ist keine Funktionsverwaltung erforderlich.)* | <p>Diese Version erweitert die Ladungsplanungsfunktionen der Lagerverwaltungs-Workload für Cloud- und Edge-Skalierungs-Einheiten.</p><p>Weitere Informationen finden Sie unter [Arbeitsauslastungen in der Lagerortverwaltung für Cloud- und Edge-Skalierungseinheiten](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Verwaltung für technische Änderung | Variantengenerierung für technische Produkte | <p>Mit dieser Funktion können Sie basierend auf Farbe, Größe, Stil oder Konfigurationsabmessungen mehrere Varianten für ein technisches Produkt generieren.</p><p>Weitere Informationen finden Sie unter [Generieren Sie Varianten für Engineering-Produkte](../engineering-change-management/engineering-variants.md).</p> |
| Lager- und Lagerortverwaltung | Integration der Bestandssichtbarkeit mit Reservierungsversatz | <p>Diese Funktion kann erst aktiviert werden, nachdem die *Integration der Inventarsichtbarkeit* Funktion aktiviert ist. Es bietet Funktionen zum Ausgleichen von Reservierungen, die in der Inventarsichtbarkeit vorgenommen werden.</p><p>Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](../inventory/inventory-visibility-reservations.md).</p> |
| Vertrieb und Marketing | Begrenzen Sie die Anzahl der Verkaufsaufträge, die für die Buchung ausgewählt werden können | <p>Diese Funktion ist automatisch aktiviert. Sie fügt eine Einstellung namens **Max. Anzahl von Verkaufsaufträgen für die Buchung** auf der Seite **Parameter für Debitoren** hinzu. Mit diesem Feld können Sie die maximale Anzahl von Verkaufsaufträgen festlegen, die beim Buchen von Bestätigungen, Kommissionierlisten, Lieferscheinen und Rechnungen auf der Seite mit den Verkaufsaufträgen ausgewählt werden können. Der Standardwert ist *100*.</p><p>Diese Funktion trägt dazu bei, die Leistung der Seite mit den Aufträgen zu verbessern, wenn eine erhebliche Anzahl von Verkaufsaufträgen ausgewählt ist. Sie hat keinen Einfluss auf die Anzahl der Verkaufsaufträge, die von einer periodischen Aufgabe verarbeitet werden können.</p> |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfethemen kürzlich hinzugefügt oder erheblich aktualisiert. Diese Themen beziehen sich nicht unbedingt auf die neuen Funktionen, die für diese Version hinzugefügt wurden, wie im vorherigen Abschnitt aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Themen |
|---|---|
| Verwaltung für technische Änderung | [Überblick über das Änderungsmanagement](../engineering-change-management/product-engineering-overview.md) listet jetzt alle zugehörigen, optionalen Funktionen auf, die in der Funktionsverwaltung verfügbar sind |
| Produktprogrammplanung | [Einrichtung der Bedarfsplanung](../master-planning/demand-forecasting-setup.md) |
| Produktprogrammplanung | [Nettobedarf und Informationen zum Bedarfsverursacher in der Planungsoptimierung](../master-planning/planning-optimization/net-requirements.md) |
| Lagerortverwaltung | [Freigabe ins Lager](../warehousing/release-to-warehouse-process.md) bietet einen detaillierten Überblick über den vollständigen Freigabeprozess im Lager |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdate für Finance and Operations Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.22 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattformupdates für Version 10.0.22 von Finance and Operations-Apps (November 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.22 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) an.

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
