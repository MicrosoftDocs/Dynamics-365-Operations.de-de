---
title: Erstellen von Serviceobjektbeziehungen
description: In diesem Thema wird beschrieben, wie Serviceobjektbeziehungen für eine Servicevereinbarung und einen Serviceauftrag erstellt werden.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 352d3b790da340102b7dbe116d9deeb2f3cbfc4e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428892"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="f1540-103">Erstellen von Serviceobjektbeziehungen</span><span class="sxs-lookup"><span data-stu-id="f1540-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f1540-104">In diesem Thema wird beschrieben, wie Serviceobjektbeziehungen für eine Servicevereinbarung und einen Serviceauftrag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f1540-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="f1540-105">Durch Erstellen einer Serviceobjektbeziehung wird das Serviceobjekt einer Servicevereinbarung oder einem Serviceauftrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f1540-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="f1540-106">Wenn ein Debitor einen Service für einen Artikel anfordert, der ein Serviceobjekt ist, können Sie das Serviceobjekt aus der Liste der Serviceobjektbeziehungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="f1540-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="f1540-107">Erstellen einer Serviceobjektbeziehung für einen Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="f1540-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="f1540-108">Gehen Sie folgendermaßen vor, um eine Serviceobjektbeziehung für einen Servicevertrag zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f1540-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="f1540-109">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="f1540-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="f1540-110">Wählen Sie in der Liste **Serviceverträge** eine vorhandene Servicevereinbarung aus, oder klicken Sie auf **Neu**, um einen neuen Servicevertrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1540-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="f1540-111">Klicken Sie im **Serviceverträge**-Formular im **Aktivitätsbereich** auf der Registerkarte **Servicevereinbarung** in der Gruppe **Referenzen** auf **Serviceobjekte**.</span><span class="sxs-lookup"><span data-stu-id="f1540-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="f1540-112">Klicken Sie im Formular **Serviceobjekte** auf **Neu**, und wählen Sie anschließend ein Serviceobjekt für diese Servicevereinbarung aus.</span><span class="sxs-lookup"><span data-stu-id="f1540-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="f1540-113">Klicken Sie auf **Funktionen**, um dem Servicevertrag eine Stückliste zuzuweisen, und wählen Sie dann **Vorlagenstücklisten anfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="f1540-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="f1540-114">Wählen Sie im Formular **Vorlagenstückliste auswählen** im Feld **Vorlagenstückliste** eine Vorlagenstückliste aus.</span><span class="sxs-lookup"><span data-stu-id="f1540-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="f1540-115">Erstellen einer Serviceobjektbeziehung für einen Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="f1540-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="f1540-116">Gehen Sie folgendermaßen vor, um eine Serviceobjektbeziehung für einen Serviceauftrag zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f1540-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="f1540-117">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="f1540-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f1540-118">Wählen Sie in der Liste **Serviceaufträge** einen vorhandenen Serviceauftrag aus, oder erstellen Sie einen neuen.</span><span class="sxs-lookup"><span data-stu-id="f1540-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="f1540-119">Klicken Sie im **Serviceaufträge**-Formular im **Aktivitätsbereich** auf der Registerkarte **Serviceaufträge** in der Gruppe **Referenzen** auf **Serviceobjekte**.</span><span class="sxs-lookup"><span data-stu-id="f1540-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="f1540-120">Klicken Sie im Formular **Serviceobjekte** auf **Neu**, und wählen Sie anschließend ein Serviceobjekt für diese Serviceaufträge aus.</span><span class="sxs-lookup"><span data-stu-id="f1540-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="f1540-121">Klicken Sie auf **Funktionen**, um dem Servicevertrag eine Stückliste zuzuweisen, und wählen Sie dann **Vorlagenstücklisten anfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="f1540-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="f1540-122">Wählen Sie im Formular **Vorlagenstückliste auswählen** im Feld **Vorlagenstückliste** eine Vorlagenstückliste aus.</span><span class="sxs-lookup"><span data-stu-id="f1540-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="f1540-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1540-123">See also</span></span>

[<span data-ttu-id="f1540-124">Serviceobjekte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="f1540-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="f1540-125">Serviceobjektbeziehungen</span><span class="sxs-lookup"><span data-stu-id="f1540-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="f1540-126">Vorlagenstücklisten</span><span class="sxs-lookup"><span data-stu-id="f1540-126">Template BOMs</span></span>](template-boms.md)

  


