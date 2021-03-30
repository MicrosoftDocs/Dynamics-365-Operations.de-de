---
title: Eine Leasinggruppe erstellen
description: In diesem Thema wird erläutert, wie Sie Leasinggruppen einrichten. Leasinggruppen sind erforderlich, um neue Mietverträge zu erstellen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8ad226e87776615d9c19a239e0fb90b648d9c49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210456"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="ca024-104">Eine Leasinggruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="ca024-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca024-105">In diesem Thema wird erläutert, wie Sie Leasinggruppen einrichten.</span><span class="sxs-lookup"><span data-stu-id="ca024-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="ca024-106">Leasinggruppen sind erforderlich, um neue Mietverträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca024-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="ca024-107">Leasingbücher sind jeder Leasinggruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ca024-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="ca024-108">Leasingbücher bestimmen die Standardbücher, die für jeden Mietvertrag erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ca024-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="ca024-109">Sie können einer Leasinggruppe auf der Seite **Leasingbuchungsparameter** bestimmte Konten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ca024-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="ca024-110">Erstellen Sie ein Leasingbuch und fügen Sie eine Leasinggruppe hinzu</span><span class="sxs-lookup"><span data-stu-id="ca024-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="ca024-111">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasinggruppen**.</span><span class="sxs-lookup"><span data-stu-id="ca024-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="ca024-112">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Leasinggruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca024-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="ca024-113">Dem Raster wird eine Zeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca024-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="ca024-114">Geben Sie in der neuen Zeile im **Leasinggruppe** Feld einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ca024-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="ca024-115">Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ca024-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="ca024-116">Die Informationen, die Sie gerade eingegeben haben, werden dem **Leasinggruppe**-Feld auf der Seite **Mietvertrag hinzufügen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca024-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="ca024-117">Ein Buch mit einer Leasinggruppe verknüpfen</span><span class="sxs-lookup"><span data-stu-id="ca024-117">Associate a book with a lease group</span></span>

<span data-ttu-id="ca024-118">Nachdem Sie Leasinggruppen erstellt haben, können Sie jeder Gruppe Bücher zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ca024-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="ca024-119">Wenn Sie einen Mietvertrag erstellen und es einer Leasinggruppe zuweisen, erstellt das System eine Reihe von Zeitplänen für jedes Buch, das dieser Leasinggruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ca024-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="ca024-120">Bücher müssen eingerichtet werden, bevor sie einer Leasinggruppe zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="ca024-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="ca024-121">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasinggruppe**.</span><span class="sxs-lookup"><span data-stu-id="ca024-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="ca024-122">Wählen Sie eine Leasinggruppe aus und wählen Sie dann **Bücher**.</span><span class="sxs-lookup"><span data-stu-id="ca024-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="ca024-123">Wählen Sie **Neu** und dann im Feld **Buchart** das Buch aus, das der Leasinggruppe zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca024-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="ca024-124">Sie können einer Leasinggruppe mehrere Bücher zuweisen, wenn ein Mietvertrag auf unterschiedliche Weise bilanziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ca024-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]