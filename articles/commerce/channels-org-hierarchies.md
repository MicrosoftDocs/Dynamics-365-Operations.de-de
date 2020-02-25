---
title: Organisationshierarchien einrichten
description: In diesem Thema wird beschrieben, wie Organisationshierarchien in Microsoft Dynamics 365 Commerce eingerichtet werden.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6c19542089526c1e17fb1133d52cf042f244fb80
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002334"
---
# <a name="set-up-organization-hierarchies"></a>Organisationshierarchien einrichten


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Organisationshierarchien in Microsoft Dynamics 365 Commerce eingerichtet werden.

## <a name="overview"></a>Übersicht

Bevor Sie Kanäle erstellen, müssen Sie sicherstellen, dass Ihre Organisationshierarchien eingerichtet wurden.

Organisationshierarchien können verwendet werden, um unterschiedliche Perspektiven des Unternehmens anzuzeigen und entsprechende Berichte zu erstellen. So können Sie z. B. eine Hierarchie für Steuererklärungen sowie für rechtlich relevante oder für gesetzlich vorgeschriebene Berichte einrichten. Anschließend können Sie eine weitere Hierarchie einrichten, um anhand von Finanzdaten Berichte zu erstellen, die zwar gesetzlich nicht erforderlich sind, aber zur internen Berichterstattung dienen.

Bevor Sie eine Organisationshierarchie erstellen, müssen Sie Organisationen erstellen. Weitere Informationen finden Sie unter [Juristische Personen erstellen](channels-legal-entities.md) oder [Organisationseinheiten erstellen](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Weitere Informationen finden Sie unter folgenden Themen.
- [Organisationen und Organisationshierarchien – Übersicht](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies)
- [Ihre Organisationshierarchie planen](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy?toc=/dynamics365/commerce/toc.json)
- [Erstellen einer Organisationshierarchie](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Erstellen einer Organisationshierarchie

Führen Sie die folgenden Schritte aus, um eine Organisationshierarchie zu erstellen.

1. Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Organisationshierarchien**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Name** einen Wert ein.
1. Wählen Sie im Abschnitt **Zweck** die Option **Zweck zuweisen**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie einen Zweck aus, der Ihrer Organisationshierarchie zugewiesen werden soll.
1. Wählen Sie im Abschnitt **Zugewiesene Hierarchien** die Option **Hinzufügen**.
1. Markieren Sie in der Liste die ausgewählte Zeile. Suchen Sie die Hierarchie, die Sie soeben erstellt haben.
1. Wählen Sie **OK**.

Die folgende Abbildung zeigt eine beispielhafte Organisationshierarchie, die für eine fiktive Gruppe von „Adventure Works”-Läden erstellt wurde.

![Beispiel einer Organisationshierarchie](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Hinzufügen von Organisationen zu einer Hierarchie

Gehen Sie folgendermaßen vor, um Organisationen zu einer Hierarchie hinzuzufügen.

1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie Ihre Hierarchie aus.
1. Wählen Sie im Aktionsbereich **Anzeigen** aus.
1. Fügen Sie Organisationen nach Bedarf hinzu.
1. Um eine Organisation hinzuzufügen, wählen Sie **Bearbeiten**und dann **Einfügen** aus. Wenn Sie mit den Änderungen fertig sind, können Sie einen Entwurf speichern und die Änderungen veröffentlichen.

Die folgende Abbildung zeigt eine juristische Person, die im Hierarchie-Stammverzeichnis hinzugefügt wurde. Für die Kanäle „Mall“, „Outlet“, „Online“ und „Callcenter“ wurden vier Kostenstellen hinzugefügt. Anschließend können jeweils verschiedene Einzelhandels-, Callcenter- und Online-Kanäle hinzugefügt werden.

![Beispiel eines Hierarchiedesigners](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planen Ihrer Organisationshierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Erstellen juristischer Personen](channels-legal-entities.md)

[Erstellen von Organisationseinheiten](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanalübersicht](channels-overview.md)

[Voraussetzungen der Kanaleinrichtung](channels-prerequisites.md)
