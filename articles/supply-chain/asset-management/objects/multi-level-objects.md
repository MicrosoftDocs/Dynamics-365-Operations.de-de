---
title: Anlagen auf mehreren Ebenen
description: In diesem Thema wird erläutert, wie Anlagen auf mehreren Ebenen erstellt und gelöscht werden.
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
ms.openlocfilehash: 5c2a4052f9beca554932d7f2547288e02358b603
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571506"
---
# <a name="multi-level-assets"></a><span data-ttu-id="67f7f-103">Anlagen auf mehreren Ebenen</span><span class="sxs-lookup"><span data-stu-id="67f7f-103">Multi-level assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="67f7f-104">In diesem Thema wird erläutert, wie Anlagen auf mehreren Ebenen erstellt und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="67f7f-104">This topic explains how to create and delete multi-level assets.</span></span> <span data-ttu-id="67f7f-105">Sie können Anlagen und zugehörige untergeordnete Anlagen in einer hierarchischen Baumstruktur erstellen.</span><span class="sxs-lookup"><span data-stu-id="67f7f-105">You can create assets and related sub-assets in a hierarchical tree structure.</span></span> <span data-ttu-id="67f7f-106">Auf diese Weise können Sie Beziehungen und Abhängigkeiten zwischen den Anlagen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="67f7f-106">In this way, you can show relations and dependencies among assets.</span></span> <span data-ttu-id="67f7f-107">Wartungsaufträge können auf allen Ebenen der Anlagenstruktur in Beziehung gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="67f7f-107">Maintenance jobs can be related to all levels of the tree structure.</span></span> <span data-ttu-id="67f7f-108">Statistiken können für eine einzelne Ebene oder als Summe aller Ebenen mit untergeordneten Anlagen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="67f7f-108">Statistics can also be created for an individual level or as a sum of all sub-asset levels.</span></span>

<span data-ttu-id="67f7f-109">Auf der Listenseite **Alle Anlagen** (**Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**) listet die Spalte **Anlagen** die Anlagen in hierarchischer Reihenfolge auf.</span><span class="sxs-lookup"><span data-stu-id="67f7f-109">On the **All Assets** list page (**Asset management** \> **Common** \> **Assets** \> **All assets**), the **Asset** column lists assets in hierarchical order.</span></span> <span data-ttu-id="67f7f-110">Die Spalte **Übergeordnet** zeigt die zugehörige übergeordnete Anlage an.</span><span class="sxs-lookup"><span data-stu-id="67f7f-110">The **Parent** column shows the related parent.</span></span> <span data-ttu-id="67f7f-111">Darüber hinaus zeigt, wenn Anlagen und untergeordnete Anlagen erstellt wurden, der **Anlagenstruktur** im Bereich **Zugehörige Informationen** die Anlagen in einer Baumstruktur.</span><span class="sxs-lookup"><span data-stu-id="67f7f-111">Additionally, if assets and sub-assets have already been created, the **Asset tree** section in the **Related information** pane shows the assets in a tree structure.</span></span>

<span data-ttu-id="67f7f-112">Informationen zum Erstellen von Anlagen finden Sie unter [Anlage erstellen](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="67f7f-112">For information about how to create an asset, see [Create an asset](../objects/create-an-object.md).</span></span> <span data-ttu-id="67f7f-113">Um eine untergeordnete Anlage zu erstellen, wählen Sie die übergeordnete Anlage im Feld **Übergeordnet** im Inforegister **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-113">To create a sub-asset, select the parent asset in the **Parent** field on the **General** FastTab.</span></span>

## <a name="copy-an-asset-or-asset-structure"></a><span data-ttu-id="67f7f-114">Anlage oder Anlagenstruktur kopieren</span><span class="sxs-lookup"><span data-stu-id="67f7f-114">Copy an asset or asset structure</span></span>

<span data-ttu-id="67f7f-115">Wenn Ihr Unternehmen mehrere ähnliche Anlagenstrukturen hat, können Sie die Funktion zum Kopieren in Asset Management verwenden, um sie schnell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67f7f-115">If your company has several similar asset structures, you can use the Copy function in Asset Management to quickly create them.</span></span>

1. <span data-ttu-id="67f7f-116">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="67f7f-116">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="67f7f-117">Wählen Sie auf der Listenseite **Alle Anlagen** die zu kopierende Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-117">On the **All assets** list page, select the asset to copy.</span></span> <span data-ttu-id="67f7f-118">Wenn Sie beispielsweise die gesamte Anlagenstruktur einschließlich der untergeordneten Anlagen kopieren möchten, wählen Sie eine übergeordnete Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-118">For example, if you want to copy the whole asset structure, including sub-assets, select a parent asset.</span></span>
3. <span data-ttu-id="67f7f-119">Wählen Sie **Anlage kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-119">Select **Copy asset**.</span></span> <span data-ttu-id="67f7f-120">Im Abschnitt **Kopieren von** wird das Feld **Anlage** auf die Anlage festgelegt, die Sie auf der Listenseite ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="67f7f-120">In the **Copy from** section, the **Asset** field is set to the asset that you selected on the list page.</span></span>
4. <span data-ttu-id="67f7f-121">Geben Sie im Abschnitt **Kopieren nach** im Feld **Anlage** den Namen der neuen Anlage ein.</span><span class="sxs-lookup"><span data-stu-id="67f7f-121">In the **Copy to** section, in the **Asset** field, enter the name of the new asset.</span></span>
5. <span data-ttu-id="67f7f-122">Wenn die Anlage, die Sie erstellen, Teil einer vorhandenen Anlagenstruktur sein soll, wählen Sie im Abschnitt **Übergeordnete Anlage** im Feld **Anlage** die Kennung der einer übergeordneten Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-122">If the asset that you're creating should be part of an existing asset structure, in the **Parent asset** section, in the **Asset** field, select a parent ID.</span></span>
6. <span data-ttu-id="67f7f-123">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="67f7f-123">Select **OK**.</span></span> <span data-ttu-id="67f7f-124">Die neue Anlagenstruktur wird auf der Listenseite **Alle Anlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67f7f-124">The new asset structure is shown on the **All assets** list page.</span></span> <span data-ttu-id="67f7f-125">Alle Anlagenattribute, Wartungspläne und Wartungsdurchgänge, die der kopierten Anlage zugeordnet sind, werden in die neue Anlage oder Anlagenstruktur übertragen.</span><span class="sxs-lookup"><span data-stu-id="67f7f-125">All asset attributes, maintenance plans, and maintenance rounds that are related to the asset that you copied are transferred to the new asset or asset structure.</span></span>

<span data-ttu-id="67f7f-126">Wenn Sie eine Anlagenstruktur kopieren, haben die untergeordneten Anlagen in der neuen Struktur den gleichen Namen wie die kopierten untergeordneten Anlagen.</span><span class="sxs-lookup"><span data-stu-id="67f7f-126">When you copy an asset structure, the sub-assets in the new structure have the same name as the sub-assets that you copied.</span></span> <span data-ttu-id="67f7f-127">Nach dem Kopieren können Sie den Namen und andere Einstellungen für eine Anlage einfach ändern.</span><span class="sxs-lookup"><span data-stu-id="67f7f-127">After the copy procedure is completed, you can easily change the name and other settings for an asset.</span></span> <span data-ttu-id="67f7f-128">Wählen Sie die Anlage auf der Listenseite **Alle Anlagen** aus, und wählen Sie dann die Schaltfläche **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-128">Select the asset on the **All assets** list page, and then select the **Edit** button.</span></span>

> [!NOTE]
> <span data-ttu-id="67f7f-129">Wenn Sie eine Anlage oder eine Anlagenstruktur kopieren, wird der Lebenszyklusstatus der neuen Anlagen auf den Status zurückgesetzt, den Sie als anfänglichen Lebenszyklusstatus für Anlagen definiert haben.</span><span class="sxs-lookup"><span data-stu-id="67f7f-129">When you copy an asset or asset structure, the lifecycle state of the new assets is reset to whatever state you defined as the initial lifecycle state for assets.</span></span> <span data-ttu-id="67f7f-130">Der funktionale Standort wird auf den standardmäßigen funktionalen Standort zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="67f7f-130">The functional location is reset to the default functional location.</span></span>

## <a name="delete-an-asset-or-asset-structure"></a><span data-ttu-id="67f7f-131">Anlage oder Anlagenstruktur löschen</span><span class="sxs-lookup"><span data-stu-id="67f7f-131">Delete an asset or asset structure</span></span>

<span data-ttu-id="67f7f-132">Wenn eine Anlage über untergeordnete Anlagen verfügt, können Sie die Anlage nur dann löschen, wenn keine Wartungsanfragen, Arbeitsaufträge, Fehlererfassungen oder Bedingungsbewertungen für die Anlagen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="67f7f-132">If an asset has related sub-assets, you can delete it only if no maintenance requests, work order jobs, fault registrations, or condition assessments are registered on any of the assets.</span></span>

1. <span data-ttu-id="67f7f-133">Wählen Sie auf der Listenseite **Alle Anlagen** die zu löschende Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="67f7f-133">On the **All assets** list page, select the asset to delete.</span></span>
2. <span data-ttu-id="67f7f-134">Wählen Sei **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="67f7f-134">Select **Delete**.</span></span>

> [!NOTE]
> <span data-ttu-id="67f7f-135">Wenn Sie eine Anlage nicht auf diese Weise löschen können, können Sie auch einen Anlagenlebenszyklusstatus für diesen Zweck einrichten.</span><span class="sxs-lookup"><span data-stu-id="67f7f-135">If you can't delete an asset by using this procedure, another way to handle deletion is to set up an asset lifecycle state for this purpose.</span></span> <span data-ttu-id="67f7f-136">Sie können beispielsweise einen Lebenszyklusstatus **Verschrottet** oder **Gelöscht** auf der Seite **Anlagenlebenszyklusstatus** einrichten.</span><span class="sxs-lookup"><span data-stu-id="67f7f-136">For example, you can set up a **Scrapped** or **Deleted** lifecycle state on the **Asset lifecycle states** page.</span></span>
