---
title: Zugriffsrechte für Kostenobjekt-Controller
description: Dieser Artikel bietet Informationen über Zugriffsrechte für Kostenobjekt-Controller.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c40be758c5e5d1d1fb025630ed8321ae46251892
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903188"
---
# <a name="access-rights-for-cost-object-controllers"></a>Zugriffsrechte für Kostenobjekt-Controller

[!include [banner](../includes/banner.md)]

Der Arbeitsbereich **Kostensteuerung** ist ein zentraler Punkt, in dem Manager die Leistung der Kostenobjekte anzeigen können. In diesem Arbeitsbereich können Manager Kostenrechnungsdaten nutzen, auch wenn sie keine Kostenbuchhalter sind. Aus Sicherheitsgründen solle Managern ermöglicht werden, nur die Kostenrechnungsdaten anzuzeigen, die den bestimmten Kostenobjekten zugeordnet sind, für die sie zuständig sind.

Es gibt vier eindeutige Rollen in der Kostenrechnung.

| Rollenname               | Lizenz      |
|-------------------------|--------------|
| Kostenrechnungs-Manager | Aktivität     |
| Kostenbuchhalter         | Operations   |
| Sachbearbeiter Kostenbuchhaltung   | Abläufe   |
| Kostenobjekt-Controller  | Teammitglieder |

In diesem Artikel wird erläutert, wie Managern die Rolle **Kostenobjekt-Controller** zugewiesen wird.

Wenn einem Manager die Rolle **Kostenobjekt-Controller** zugewiesen wird, kann der Manager die folgenden Aufgaben ausführen:

- Zugriff auf den Arbeitsbereich **Kostensteuerung** (im Client).

    - Detailinformationen zu den und Ansichtszugriff auf die Seiten, die die Drillthrough-Erfahrung unterstützen.

- Zugriff auf den Arbeitsbereich **Kostensteuerung** (im der Mobilanwendung).

> [!NOTE]
> Die Rolle **Kostenobjekt-Controller** steuert nicht, auf welche Kostenobjekte der Benutzer zugreifen und Daten dazu anzeigen kann. Sicherheit auf Positionsebene wird über Dimensionshierarchien und die Zugriffslistenhierarchie bereitgestellt.

## <a name="grant-access-rights"></a>Zugriffsrechte gewähren
Das folgende Beispiel zeigt, wie eine Dimensionshierarchie aussehen kann.

**Dimensionshierarchiedetails**

| Dimensionshierarchiename | Dimensionen    | Dimensionshierarchie-Typname      | Zugriffslistenhierarchie |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Kostenstellen | Dimensionsklassifizierungshierarchie | **Ja**               |

Sie können das Inforegister **Benutzer** im Hierarchie-Designer verwenden, um mindestens eine Benutzerkennungen auf jedem Knoten einzufügen.

|             Knoten                 | Benutzer            | Von-Dimensionsmitglied     |   Bis-Dimensionsmitglied   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| Organisation                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Verwaltung                 | April            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finanzen   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Produktion            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpackung | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montage  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Kostenbuchhalter sollten der höchsten Ebene der Hierarchie zugewiesen werden, damit sie alle Einträge in der Kostenrechnung anzeigen können.

Bevor die Zugriffslistenhierarchie und deren Sicherheitseinstellungen angewendet werden können, muss die Option **Anzeigezugriff für Kostenobjektdimensionsmitglieder zulassen** auf **Ja** in der Registerkarte **Allgemein** der Seite **Kostenrechnungsparameter** (**Kostenrechnung** > **Einstellungen** > **Parameter**) festgelegt werden.

Die Einstellungen für die Zugriffslistenhierarchie werden verwendet, um die Daten zu steuern, die in den folgenden Bereichen angezeigt werden:

- Arbeitsbereich **Kostensteuerung** (im Client)

    - Daten auf den Seiten, die für den Drillthrough verwendet werden

- Arbeitsbereich **Kostensteuerung** (in der Mobilanwendung):

    - Salden in Karten

- Microsoft Power BI:

    - Daten, die in Power BI-Visualisierungen angezeigt werden
    - Power BI-Datenvisualisierungen, die im Client von Dynamics 365 Finance eingebettet werden

> [!IMPORTANT]
> - Bevor sich die Zugriffslistenhierarchie auf Daten in Power BI auswirken kann, müssen die Zugriffslistenhierarchie und Sicherheit auf Zeilenebene in Power BI zugeordnet werden. Weitere Informationen finden Sie unter [Sicherheit für das Kostenrechnungs-Inhaltspack einrichten](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - In diesem Artikel werden die Voraussetzungen behandelt, die erfüllt sein müssen, bevor Sie den Arbeitsbereich **Kostensteuerung** verwenden können.

Zusätzliche Ressourcen

- [Kostensteuerungs-Arbeitsbereich](cost-control-workspace.md)
- [Dimensionshierarchie](dimension-hierarchy.md)
- [Sicherheit für Kostensteuerungs-Inhaltspack einrichten](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
