---
title: Einen Kanal zu einer Organisationshierarchie hinzufügen
description: In diesem Artikel wird beschrieben, wie ein Kanal zu einer Organisationshierarchie in Microsoft Dynamics 365 Commerce hinzugefügt wird.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8de9242b9d272158dff9c486006a1684f073935e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876585"
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