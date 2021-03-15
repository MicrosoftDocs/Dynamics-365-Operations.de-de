---
title: Eine Kanalnavigationshierarchie erstellen
description: In diesem Thema wird beschrieben, wie eine Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce erstellt wird.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89e24496d35ea0a02bd985f76d7579e1914d9290
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972981"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Eine Kanalnavigationshierarchie erstellen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Kanalnavigationshierarchie in Microsoft Dynamics 365 Commerce erstellt wird.

## <a name="overview"></a>Übersicht

Eine Kanalnavigationshierarchie dient zur Gruppierung und Organisierung von Produkten in Kategorien, sodass die Produkte online oder an einer Verkaufsstelle (POS) durchsucht werden können.

## <a name="create-a-channel-navigation-hierarchy"></a>Eine Kanalnavigationshierarchie erstellen

Um eine Kanalnavigationshierarchie zu erstellen, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Kanalnavigationskategorien**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Kästchen **Name** einen Namen ein.
1. Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.
1. Wählen Sie **Erstellen** aus.
1. Wählen Sie im Aktionsbereich **Neuer Kategorieknoten**, um einen Stammknoten zu erstellen.
1. Geben Sie im Kästchen **Name** einen Namen ein.
1. Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.
1. Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Die folgende Abbildung zeigt einen beispielhaften Stammknoten.

![Beispiel für einen Stammknoten](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Navigationskategorieknoten erstellen

Gehen Sie folgendermaßen vor, um zusätzliche Navigationskategorieknoten zu erstellen, um die Produktkategorien auf dem Kanal darzustellen.

1. Wählen Sie im Navigationsbereich den übergeordneten Knoten aus, dem Sie eine Kategorie hinzufügen möchten.
1. Klicken Sie im Aktivitätsbereich auf **Neuer Kategorieknoten**.
1. Geben Sie im Kästchen **Name** einen Namen ein.
1. Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.
1. Geben Sie in das Feld **Anzeigename** einen Anzeigename ein.
1. Geben Sie im Feld **Anzeigereihenfolge** eine Anzeigereihenfolge ein (optional).
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel einer vollständigen Kanalnavigationshierarchie.

![Beispiel einer Kanalhierarchie](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Produkte zu Kategorieknoten hinzufügen

Gehen Sie folgendermaßen vor, um Produkte zu Kategorieknoten hinzuzufügen.

1. Wählen Sie einen Kategorieknoten aus.
1. Wählen Sie unter **Produkte** die Option **Hinzufügen** aus.
1. Suchen Sie die neuen Produkte, die Sie hinzufügen möchten, anhand der Produktnummer oder des Produktnamens und wählen Sie dann **OK** aus.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

> [!NOTE]
> Das Hinzufügen von Produkten zu einem Knoten in der Kanalnavigationshierarchie reicht nicht aus, damit die Produkte in einem ausgewählten Kanal angezeigt werden. Die Produkte müssen auch zu einem Produkt sortiert werden.

Das folgende Bild zeigt einen Beispielknoten mit hinzugefügten Produkten.

![Produkte zu einem Kategorieknoten hinzufügt](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Produktattributgruppen zu Kategorieknoten hinzufügen

> [!NOTE]
> Attributgruppen müssen erstellt werden, bevor Sie sie einem Knoten in der Kanalnavigationshierarchie hinzufügen können.

Befolgen Sie diese Schritte, um ein Produkt einer Attributgruppe zu einem Kategorieknoten hinzuzufügen.

1. Wählen Sie einen Kategorieknoten aus.
1. Wählen Sie unter **Produktattributgruppe** die Option **Hinzufügen**.
1. Suchen Sie die Attributgruppen, die Sie hinzufügen möchten, und wählen Sie dann **OK**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt einen Beispielknoten mit hinzugefügten Produktattributgruppen.

![Produktattributgruppen auf einem Knoten](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Sortimente einrichten](set-up-assortments.md)

[Attribute und Attributgruppen verwalten](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]