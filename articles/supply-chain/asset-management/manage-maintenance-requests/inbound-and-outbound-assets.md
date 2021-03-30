---
title: Ein- und ausgehende Anlagen
description: In diesem Thema wird erläutert, wie Sie ein- und ausgehende Anlagen in Asset Management erfassen.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c77aa0dc10844fbe07afa0b8d2a6f3578a246ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253346"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="f7306-103">Ein- und ausgehende Anlagen</span><span class="sxs-lookup"><span data-stu-id="f7306-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f7306-104">Wenn Ihr Unternehmen Reparatur- oder Wartungsarbeiten für Anlagen ausführt, die von anderen Standorten oder Kunden entgegen genommen werden, kann Asset Management sowohl eingehende Anlagen nachverfolgen, die auf dem Weg zu Ihrem Unternehmen sind, als auch ausgehenden Anlagen, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7306-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="f7306-105">Wenn Sie Lebenszyklusstatus für ein- und ausgehende Anlagen zum Verwalten von Anlagen verwenden möchten, die empfangen und zurückgegeben werden, müssen Sie Lebenszyklusstatus für Wartungsanforderungen und Lebenszyklusmodelle einrichten, die diese Aktivitäten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f7306-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="f7306-106">Weitere Informationen finden Sie unter [Wartungsanforderungen](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="f7306-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="f7306-107">Die Einrichtung von Asset Management bestimmt, ob Sie mit ein- und ausgehenden Anlagen arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f7306-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="f7306-108">Erfassen von Anlagen als eingehend</span><span class="sxs-lookup"><span data-stu-id="f7306-108">Register assets as inbound</span></span>

1. <span data-ttu-id="f7306-109">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Wartungsanfragen** \> **Aktive Wartungsanfragen**.</span><span class="sxs-lookup"><span data-stu-id="f7306-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="f7306-110">Wählen Sie die Wartungsanfrage aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="f7306-111">Wählen Sie **Wartungsanforderungsstatus aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="f7306-112">Wählen Sie **Eingehend** aus (oder einen anderen Lebenszyklusstatus, den Sie für eingehende Anlagen erstellt haben), und wählen Sie anschließend **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7306-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Erfassen von Anlagen als eingehend](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="f7306-114">Erfassen von eingehenden Anlagen als empfangen</span><span class="sxs-lookup"><span data-stu-id="f7306-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="f7306-115">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Ein-/ausgehend** \> **Eingehende Anlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="f7306-116">Wählen Sie die Anlage oder die Wartungsanfrage aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="f7306-117">Wählen Sie **Anlagen entgegennehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="f7306-118">Geben Sie im Feld **Eingegangen** das Datum und die Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f7306-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="f7306-119">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-119">Then select **OK**.</span></span> <span data-ttu-id="f7306-120">Der Datensatz wird von der Listenseite **Eingehende Anlagen** entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7306-120">The record is removed from the **Inbound assets** list page.</span></span>

![Erfassen von eingehenden Anlagen als empfangen](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="f7306-122">Erfassen von Anlagen als ausgehend</span><span class="sxs-lookup"><span data-stu-id="f7306-122">Register assets as outbound</span></span>

<span data-ttu-id="f7306-123">Wenn Sie den Wartungs- oder Reparaturauftrag erledigt haben, können Sie die Anlage als zurückgegeben erfassen.</span><span class="sxs-lookup"><span data-stu-id="f7306-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="f7306-124">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Wartungsanfragen** \> **Aktive Wartungsanfragen**.</span><span class="sxs-lookup"><span data-stu-id="f7306-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="f7306-125">Wählen Sie die Wartungsanfrage aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="f7306-126">Wählen Sie **Wartungsanforderungsstatus aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="f7306-127">Wählen Sie **Ausgehend** aus (oder einen anderen Lebenszyklusstatus, den Sie für ausgehende Anlagen erstellt haben), und wählen Sie anschließend **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7306-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="f7306-128">Erfassen von ausgehenden Anlagen als geliefert</span><span class="sxs-lookup"><span data-stu-id="f7306-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="f7306-129">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Ein-/ausgehend** \> **Ausgehende Anlagen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="f7306-130">Wählen Sie die Anlage oder die Wartungsanfrage aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="f7306-131">Wählen Sie **Anlagen liefern** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="f7306-132">Geben Sie im Feld **Geliefert** das Datum und die Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="f7306-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="f7306-133">Wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f7306-133">Then select **OK**.</span></span> <span data-ttu-id="f7306-134">Der Datensatz wird von der Listenseite **Ausgehende Anlagen** entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7306-134">The record is removed from the **Outbound assets** list page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]