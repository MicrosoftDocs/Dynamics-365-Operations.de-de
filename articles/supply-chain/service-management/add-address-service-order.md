---
title: Hinzufügen einer Adresse zu einem Serviceauftrag
description: In diesem Thema wird beschrieben, wie eine Debitorenadresse zu einem Serviceauftrag hinzugefügt wird.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41497eacae8bcc0e57df8062f7f318a39c2b4909
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428886"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="22f91-103">Hinzufügen einer Adresse zu einem Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="22f91-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="22f91-104">In diesem Thema wird beschrieben, wie eine Debitorenadresse zu einem Serviceauftrag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="22f91-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="22f91-105">Beim Erstellen eines Serviceauftrags werden die Adressinformationen aus dem Projekt übertragen, dem der Serviceauftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="22f91-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="22f91-106">Allerdings können Sie einen alternativen Speicherort von Adressen auswählen, die bereits in Microsoft Dynamics AX für Debitoren, Kreditoren, Standorte, Lagerorte, Serviceaufträge und Projekte eingegeben sind.</span><span class="sxs-lookup"><span data-stu-id="22f91-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="22f91-107">Zudem können Sie eine neue Adresse erstellen.</span><span class="sxs-lookup"><span data-stu-id="22f91-107">You can also create a new address.</span></span> <span data-ttu-id="22f91-108">Standardmäßig wird die neue Adresse in das Projekt übertragen.</span><span class="sxs-lookup"><span data-stu-id="22f91-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="22f91-109">Allerdings können Sie angeben, dass die neue Adresse für diese Instanz des Services relevant ist.</span><span class="sxs-lookup"><span data-stu-id="22f91-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="22f91-110">Die neue Adresse wird dann nicht in das Projekt übertragen.</span><span class="sxs-lookup"><span data-stu-id="22f91-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="22f91-111">Erstellen einer Debitorenadresse für einen Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="22f91-111">Create a customer address for a service order</span></span>

<span data-ttu-id="22f91-112">Um einem Serviceauftrag eine Adresse hinzuzufügen, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="22f91-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="22f91-113">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="22f91-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="22f91-114">Öffnen Sie den Serviceauftrag, für den eine Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="22f91-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="22f91-115">Klicken Sie im **Aktivitätsbereich** auf **Bearbeiten**, und klicken Sie anschließend auf **Kopfzeilenansicht**.</span><span class="sxs-lookup"><span data-stu-id="22f91-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="22f91-116">Klicken Sie auf dem Inforegister **Adresse** auf **Adresse hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="22f91-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="22f91-117">Geben Sie im Formular **Neue Adresse** einen eindeutigen Namen für die Adresse ein, und füllen Sie die verbleibenden Felder aus.</span><span class="sxs-lookup"><span data-stu-id="22f91-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="22f91-118">Wenn Sie denselben Namen als vorhandene Adresse eingeben, überschreiben die Informationen, die Sie in die verbleibenden Felder eingeben, die Informationen für die vorhandene Adresse.</span><span class="sxs-lookup"><span data-stu-id="22f91-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="22f91-119">Klicken Sie auf **OK**, um die neue Adresse in Ihren Serviceauftrag zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="22f91-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="22f91-120">Angeben einer alternativen Adresse für einen Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="22f91-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="22f91-121">Um einem Serviceauftrag eine alternative Adresse hinzuzufügen, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="22f91-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="22f91-122">Klicken auf **Serviceverwaltung** \> **Gemeinsam** \> **Serviceaufträge** \> **Serviceaufträge**.</span><span class="sxs-lookup"><span data-stu-id="22f91-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="22f91-123">Öffnen Sie den Serviceauftrag, für den eine alternative Adresse erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="22f91-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="22f91-124">Klicken Sie im **Aktivitätsbereich** auf **Bearbeiten**, und klicken Sie anschließend auf **Kopfzeilenansicht**.</span><span class="sxs-lookup"><span data-stu-id="22f91-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="22f91-125">Klicken Sie auf dem Inforegister **Adresse** auf **Weitere Adresse**.</span><span class="sxs-lookup"><span data-stu-id="22f91-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="22f91-126">In der **Adressauswahl** Formular auf das Feld **Datensatztyp**, wählen Sie **Serviceaufträge** aus.</span><span class="sxs-lookup"><span data-stu-id="22f91-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="22f91-127">Wählen Sie eine Adresse aus, und klicken Sie auf **OK**, um sie in Ihren Serviceauftrag zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="22f91-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


