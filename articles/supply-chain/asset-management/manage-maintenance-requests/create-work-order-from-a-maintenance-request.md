---
title: Arbeitsaufträge aus Wartungsanfragen erstellen
description: In diesem Thema wird erläutert, wie Sie einen Wartungsauftrag aus einer Wartungsanfrage in der Anlagenverwaltung erstellen.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5bf147104909302173c32b8376f16c66784110cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253326"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="47c77-103">Arbeitsaufträge aus Wartungsanfragen erstellen</span><span class="sxs-lookup"><span data-stu-id="47c77-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="47c77-104">Nachdem Sie Wartungsanforderungen erstellt haben, können Sie sie ohne Weiteres in Arbeitsaufträge umwandeln.</span><span class="sxs-lookup"><span data-stu-id="47c77-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="47c77-105">In diesem Thema wird die schnellste Methode beschrieben, um mit Wartungsanfragen zu arbeiten, mehrere Wartungsanfragen gleichzeitig zu aktualisieren und dann einen Arbeitsauftrag für mehrere Wartungsanfragen zugleich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47c77-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="47c77-106">Auf der Seite **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte** können Sie auch mit jeweils einer Wartungsanfrage arbeiten und eine Wartungsanfrage in einen Arbeitsauftrag umwandeln.</span><span class="sxs-lookup"><span data-stu-id="47c77-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="47c77-107">Jede Wartungsanfrage kann sich nur auf einen Arbeitsauftrag beziehen.</span><span class="sxs-lookup"><span data-stu-id="47c77-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="47c77-108">Allerdings können mehrere Wartungsanfragen in einen Arbeitsauftrag aufgenommen werden, selbst wenn die Wartungsanfragen über verschiedene Anlagen verfügen.</span><span class="sxs-lookup"><span data-stu-id="47c77-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="47c77-109">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Wartungsanfragen** \> **Alle Wartungsanfragen**.</span><span class="sxs-lookup"><span data-stu-id="47c77-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="47c77-110">Bevor Sie einen Arbeitsauftrag aus Wartungsanfragen erstellen können, müssen Sie mindestens einen Wartungsauftragstyp für die Wartungsanfragen sowie eine Wartungsauftragstypvariante und eine Facharbeit auswählen, wenn diese Informationen relevant sind.</span><span class="sxs-lookup"><span data-stu-id="47c77-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="47c77-111">In der Rasteransicht können Sie Informationen für eine Wartungsanfrage leicht aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="47c77-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="47c77-112">Wenn Sie bereit sind, einen Arbeitsauftrag zu erstellen, wählen Sie die Wartungsanfragen aus, die darin enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="47c77-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="47c77-113">Wenn Sie mehrere Wartungsanfragen auswählen, um diese in einen Arbeitsauftrag umzuwandeln, müssen die Felder **Anlage** und **Wartungsauftragstyp** gefüllt werden, bevor Sie den Arbeitsauftrag erstellen können.</span><span class="sxs-lookup"><span data-stu-id="47c77-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="47c77-114">Wenn Sie eine Wartungsanfrage auswählen, um diese in einen Arbeitsauftrag umzuwandeln, muss nur das Feld **Anlage** festgelegt werden, bevor Sie den Arbeitsauftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="47c77-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="47c77-115">Wenn Sie jedoch den Arbeitsauftrag erstellen, können Sie einen Wartungsauftragstyp (sowie eine zugehörige Wartungsauftragstypvariante und eine Facharbeit, wenn diese Informationen relevant sind) im Dialogfeld **Arbeitsauftrag erstellen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="47c77-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="47c77-116">Wählen Sie **Arbeitsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="47c77-116">Select **Work order**.</span></span>
5. <span data-ttu-id="47c77-117">Legen Sie im Dialogfeld **Arbeitsauftrag erstellen** die Felder fest, und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="47c77-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="47c77-118">In einer Meldungsleiste werden Sie ggf. darüber informiert, dass ein neuer Arbeitsauftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="47c77-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="47c77-119">Wenn Sie einen Arbeitsauftrag erstellen, der auf einer Wartungsanfrage basiert und die Anlage, die sich auf die Wartungsanfrage bezieht, in einer Garantievereinbarung enthalten ist, werden Sie außerdem in einer Meldungsleiste über die Garantievereinbarung informiert.</span><span class="sxs-lookup"><span data-stu-id="47c77-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="47c77-120">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Arbeitsaufträge** \> **Alle Arbeitsaufträge** aus, und öffnen Sie den neuen Arbeitsauftrag.</span><span class="sxs-lookup"><span data-stu-id="47c77-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Neuen Arbeitsauftrag öffnen](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]