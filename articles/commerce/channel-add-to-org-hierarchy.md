---
title: Einen Kanal zu einer Organisationshierarchie hinzufügen
description: In diesem Artikel wird beschrieben, wie ein Kanal zu einer Organisationshierarchie in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 9def2d7c3cf17ecd9b74ce41f56bc3220a754597
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278596"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a>Einen Kanal zu einer Organisationshierarchie hinzufügen


[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie ein Kanal zu einer Organisationshierarchie in Microsoft Dynamics 365 Commerce hinzugefügt wird.

## <a name="overview"></a>Übersicht

Kanäle müssen einer oder mehreren Organisationshierarchien zugeordnet sein. Bevor Sie Kanäle erstellen, müssen Sie bestätigen, dass Ihre Organisationshierarchien eingerichtet wurden.  

Siehe [Organisationshierarchien](channels-org-hierarchies.md) für weitere Informationen zum Erstellen von Organisationshierarchien.

## <a name="select-a-hierarchy"></a>Wählen Sie eine Hierarchie aus

Gehen Sie folgendermaßen vor, um eine Hierarchie auszuwählen.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Organisationshierarchien**.
1. Wählen Sie aus der Liste die Organisationshierarchie aus, der Sie den Kanal hinzufügen möchten.
1. Wählen Sie im Aktionsbereich **Ansicht** aus, um die Hierarchiedetails anzuzeigen.

Das folgende Bild zeigt Details zur Organisationshierarchie für die ausgewählte Hierarchie.

![Details zur Organisationshierarchie für die ausgewählte Hierarchie.](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a>Einen Kanal zu einem Hierarchieknoten hinzufügen

Gehen Sie folgendermaßen vor, um einen Kanal zu einem Hierarchieknoten hinzuzufügen.

1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie den Hierarchieknoten aus, zu dem der Kanal hinzugefügt werden soll, und klicken Sie dann auf **Einfügen** in der Dropdown-Liste, und wählen Sie **Retail Channel** aus. 
1. Wählen Sie den Kanal aus, den Sie hinzufügen möchten, und wählen Sie dann die Schaltfläche **OK**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Wählen Sie im Aktionsbereich **Veröffentlichen** aus und geben Sie ein **Datum des Inkrafttretens** in der Vergangenheit an, um diese Aktion sofort in Kraft treten zu lassen.

Das folgende Bild zeigt, wie Sie einen Kanal auswählen, um ihn einem Hierarchieknoten hinzuzufügen.

![Einen Kanal auswählen, um ihn einem Hierarchieknoten hinzuzufügen.](media/channel-add-to-org-hierarchy-2.png)

Das folgende Bild zeigt eine Hierarchie mit verschiedenen hinzugefügten Kanälen.

![Eine Hierarchie mit verschiedenen hinzugefügten Kanälen.](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Kanäle](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)

[Organisationen und Organisationshierarchien – Übersicht](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Planen Ihrer Organisationshierarchie](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisationshierarchien](channels-org-hierarchies.md)

[Einen Retail Channel einrichten](channel-setup-retail.md)
    
[Einen Onlinekanal einrichten](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
