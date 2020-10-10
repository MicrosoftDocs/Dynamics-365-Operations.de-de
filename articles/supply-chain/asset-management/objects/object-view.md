---
title: Anlagenansicht
description: In diesem Thema wird die Anlagenansicht in Asset Management beschrieben.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc4cd9ada9c1f64b434cd657eb5f5654c1328ef4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888761"
---
# <a name="asset-view"></a><span data-ttu-id="27937-103">Anlagenansicht</span><span class="sxs-lookup"><span data-stu-id="27937-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="27937-104">In diesem Thema wird die Anlagenansicht in Asset Management beschrieben.</span><span class="sxs-lookup"><span data-stu-id="27937-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="27937-105">Die Seite **Anlagenansicht** enthält aktive Anlagen und funktionale Standorte in einer Baumstruktur.</span><span class="sxs-lookup"><span data-stu-id="27937-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="27937-106">Auf diese Weise erhalten Sie eine schnelle Übersicht über die Anlagenbeziehungen zu funktionalen Standorten.</span><span class="sxs-lookup"><span data-stu-id="27937-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="27937-107">Zudem können Sie detaillierte Informationen über funktionale Standorte, Anlagen und die zugehörigen Stücklisten (BOMs) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="27937-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="27937-108">Darüber hinaus erhalten Sie einen schnellen Überblick über die aktiven Wartungsanfragen und Arbeitsaufträge, die einer Anlage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="27937-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="27937-109">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Anlagenansicht**.</span><span class="sxs-lookup"><span data-stu-id="27937-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="27937-110">Um die Ansicht auf der Seite zu ändern, wählen Sie einen neuen Wert im Feld **Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="27937-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="27937-111">Die Standardansicht, die angezeigt wird, wenn Sie die Seite **Anlagenansicht** öffnen, hängt von dem Wert ab, der im Feld **Ansicht** auf der Registerkarte **Anlagen** der Seite **Anlagenverwaltungsparameter** aktiviert ist (**Anlagenverwaltung** \> **Einstellungen** \> **Anlagenverwaltungsparameter**).</span><span class="sxs-lookup"><span data-stu-id="27937-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="27937-112">Rechts auf der Seite zeigen Inforegister Details der ausgewählten Ansicht an.</span><span class="sxs-lookup"><span data-stu-id="27937-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="27937-113">Die Breadcrumb-Spur, die über der Strukturansicht angezeigt wird, zeigt die aktuelle Auswahl in der Strukturansicht an.</span><span class="sxs-lookup"><span data-stu-id="27937-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="27937-114">Diese Breadcrumb-Spur verwendet das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="27937-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="27937-115">Kennung des funktionalen Standorts/Kennung des funktionalen Standorts (falls es mehr als einen funktionalen Standort gibt) \> Anlagenkennung/Anlagenkennung (falls es mehr als eine Anlage gibt) – Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="27937-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="27937-116">Wenn Sie eine Anlage in der Baumstruktur ausgewählt haben, können Sie **Aktive Anfragen** oder **Aktive Arbeitsaufträge** auswählen, um die Wartungsanfragen oder die Arbeitsaufträge anzuzeigen, die der Anlage zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="27937-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="27937-117">Sie können auch **Öffnen** \> **Funktionaler Standort**, **Anlage** oder **Anlagenstückliste** auswählen, um die zugehörige Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="27937-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="27937-118">Die Option **Funktionale Standorte der Anlage**, die Sie im Feld **Ansicht** auswählen können, ist ebenfalls bei jeder Anlagensuche verfügbar, in der Sie eine Anlage auswählen können.</span><span class="sxs-lookup"><span data-stu-id="27937-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="27937-119">Die Strukturansicht wird auf einer Registerkarte **Anlagenansicht** angezeigt, auf der Sie beispielsweise [eine Anlage erstellen](../objects/create-an-object.md), eine Wartungsanfrage erstellen oder einen Arbeitsauftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="27937-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
