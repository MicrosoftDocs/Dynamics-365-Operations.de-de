---
title: Anlagenhersteller und -modelle
description: In diesem Thema wird erläutert, wie Anlagenhersteller und zugehörige Modelle in Asset Management eingerichtet werden.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b77605070387871335c480e25cbe23af1155d6e8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812167"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="5f514-103">Anlagenhersteller und -modelle</span><span class="sxs-lookup"><span data-stu-id="5f514-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5f514-104">In diesem Thema wird erläutert, wie Anlagenhersteller und zugehörige Modelle in Asset Management eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="5f514-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="5f514-105">Modelle können Anlagentypen zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="5f514-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="5f514-106">Produktmodellbeziehungen einrichten</span><span class="sxs-lookup"><span data-stu-id="5f514-106">Set up product-model relations</span></span>

1. <span data-ttu-id="5f514-107">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Hersteller und Modell** aus.</span><span class="sxs-lookup"><span data-stu-id="5f514-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="5f514-108">Wählen Sie **Neu** aus, um ein neues Produkt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f514-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="5f514-109">Geben Sie im Feld **Hersteller** den Namen des Anlagenherstellers ein.</span><span class="sxs-lookup"><span data-stu-id="5f514-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="5f514-110">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="5f514-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5f514-111">Wählen Sie auf dem Inforegister **Modelle** die Option **Hinzufügen** aus, um ein Anlagenmodell zu erstellen, das dem Anlagenhersteller zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f514-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="5f514-112">Geben Sie im Feld **Modell** einen Namen für das Anlagenmodell ein.</span><span class="sxs-lookup"><span data-stu-id="5f514-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="5f514-113">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="5f514-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="5f514-114">Wählen Sie im Feld **Anlagentyp** den Anlagentyp aus, dem das Herstellermodell zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f514-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f514-115">Sie können Zuordnungen für Anlagentypen, -hersteller und -modelle auch in der Suche **Anlagentypen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="5f514-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="5f514-116">Weitere Informationen finden Sie unter [Anlagentypen](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5f514-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="5f514-117">Auf dem Inforegister **Details** wird im Feld **Modelle** die Anzahl der Anlagenmodelle angezeigt, die für den ausgewählten Anlagenhersteller eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="5f514-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="5f514-118">Das Feld **Anlagen** zeigt die Anzahl der Anlagen, die den ausgewählten Hersteller verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f514-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="5f514-119">Das Feld **Anlagen** zeigt die Anzahl der Objekte, die das Herstellermodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f514-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="5f514-120">Für einen Anlagentyp können keine Anlagenherstellermodell-Zuordnungen vorliegen, er kann einem Anlagenherstellermodell zugeordnet sein, oder er kann mehreren Anlagenherstellermodellen zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="5f514-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="5f514-121">Wenn ein Anlagentyp mindestens einem Herstellermodell zugeordnet ist, können nur die Kombinationen, die in der Suche **Herstellermodell** eingerichtet sind, auf den Asset Management-Seiten ausgewählt werden, für die eine Kombination aus Anlagentyp, -hersteller und -modell eingerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f514-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="5f514-122">Zu diesen Seiten gehören **Alle Anlagen**, **Anlagenservicelevel**, **Einzelvorgangstypstandards** und **Wartungsbudgetpositionen**.</span><span class="sxs-lookup"><span data-stu-id="5f514-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="5f514-123">Wenn einige Anlagentypen keinem Herstellermodell zugeordnet sind, werden auf den Seiten nur diese Anlagentypen und Herstellermodelle angezeigt, die ebenfalls keinen Anlagentypen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5f514-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="5f514-124">Wählen Sie einen Hersteller und ein Modell für ein Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="5f514-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="5f514-125">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="5f514-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="5f514-126">Wählen Sie in der Spalte **Anlage** den Link für die Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="5f514-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="5f514-127">Die Seite **Details** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5f514-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="5f514-128">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5f514-128">Select **Edit**.</span></span>
4. <span data-ttu-id="5f514-129">Wählen Sie auf dem Inforegister **Allgemein** Werte in den Feldern **Hersteller** und **Modell** aus.</span><span class="sxs-lookup"><span data-stu-id="5f514-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
