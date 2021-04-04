---
title: Nach Zuordnung einer neuen Website werden Produkte und Kategorien nicht im Commerce-Website-Generator angezeigt
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Zuordnen einer neuen Website nicht im Commerce-Website-Generator angezeigt werden.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46ad73256e5acf6d42772fc4af154a8d74206bbb
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585344"
---
# <a name="products-and-categories-dont-appear-in-commerce-site-builder-after-a-new-site-is-mapped"></a><span data-ttu-id="f64f6-103">Nach Zuordnung einer neuen Website werden Produkte und Kategorien nicht im Commerce-Website-Generator angezeigt</span><span class="sxs-lookup"><span data-stu-id="f64f6-103">Products and categories don't appear in Commerce site builder after a new site is mapped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f64f6-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Zuordnen einer neuen Website nicht im Commerce-Website-Generator angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f64f6-104">This topic provides troubleshooting guidance that can help when products and categories don't appear in Commerce site builder after a new site is mapped.</span></span>

## <a name="description"></a><span data-ttu-id="f64f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f64f6-105">Description</span></span>

<span data-ttu-id="f64f6-106">Produkte und Kategorien werden nicht im Commerce-Website-Generator angezeigt, nachdem eine neue Website zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f64f6-106">Products and categories don't appear in Commerce site builder after a new site is mapped.</span></span>

## <a name="resolution"></a><span data-ttu-id="f64f6-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="f64f6-107">Resolution</span></span>

### <a name="add-products-to-channel-categories-in-commerce-headquarters"></a><span data-ttu-id="f64f6-108">Kanalkategorien Produkte in der Commerce-Zentralverwaltung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f64f6-108">Add products to channel categories in Commerce headquarters</span></span>

<span data-ttu-id="f64f6-109">Befolgen Sie diese Schritte, um Kanalkategorien Produkte in der Commerce-Zentralverwaltung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f64f6-109">To add products to channel categories in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f64f6-110">Wählen Sie **Retail and Commerce \> Kanaleinstellung \> Kanalkategorien und Produktattribute**.</span><span class="sxs-lookup"><span data-stu-id="f64f6-110">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="f64f6-111">Wählen Sie in der linken Navigation die Kategorie aus, die auf der E-Commerce-Website angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f64f6-111">In the left navigation, select the category that should appear on the e-commerce site.</span></span>
1. <span data-ttu-id="f64f6-112">Wählen Sie im Inforegister **Produkte** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="f64f6-112">On the **Products** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="f64f6-113">Wählen Sie im Abschnitt **Verfügbare Produkte** die Produkte aus, die angezeigt werden sollen. Wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="f64f6-113">In the **Available Products** section, select the products that should appear, and then select **Add**.</span></span>
1. <span data-ttu-id="f64f6-114">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="f64f6-114">Select **OK**.</span></span>
1. <span data-ttu-id="f64f6-115">Wählen Sie im Aktionsbereich die Option **Kanalupdates veröffentlichen** aus, sobald die Produkte im Inforegister **Produkte** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f64f6-115">After the products appear on the **Products** FastTab, select **Publish channel updates** on the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f64f6-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f64f6-116">Additional resources</span></span>

[<span data-ttu-id="f64f6-117">Einen Kanal zur Verwendung einer Kanalnavigationshierarchie konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f64f6-117">Configure a channel to use a channel navigation hierarchy</span></span>](../configure-channel-hierarchy.md)
