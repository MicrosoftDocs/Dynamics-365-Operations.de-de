---
title: Leasingbücher einrichten
description: In diesem Thema werden die Informationen beschrieben, die in Leasingbüchern verwaltet werden. Leasingbücher enthalten die Rechnungslegungsgrundsätze, die bestimmen, wie ein Mietvertrag im System bilanziert wird.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443773"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="89a15-104">Leasingbücher einrichten</span><span class="sxs-lookup"><span data-stu-id="89a15-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89a15-105">Leasingbücher enthalten die Rechnungslegungsgrundsätze, die bestimmen, wie ein Mietvertrag im System bilanziert wird.</span><span class="sxs-lookup"><span data-stu-id="89a15-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="89a15-106">Neben der Bilanzierung auf Cash-Basis unterstützt Anlagenleasing die folgenden Standards:</span><span class="sxs-lookup"><span data-stu-id="89a15-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="89a15-107">Allgemein anerkannte Rechnungslegungsgrundsätze in den USA (US-GAAP)</span><span class="sxs-lookup"><span data-stu-id="89a15-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="89a15-108">Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="89a15-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="89a15-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="89a15-109">ASC 840</span></span>
- <span data-ttu-id="89a15-110">Internationaler Financial Reporting-Standard 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="89a15-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="89a15-111">International Buchführungsstandard 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="89a15-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="89a15-112">Gehen Sie folgendermaßen vor, um einen Mietvertrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="89a15-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="89a15-113">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasingbücher**.</span><span class="sxs-lookup"><span data-stu-id="89a15-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="89a15-114">Wählen Sie **Neu** aus, um ein Buch hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="89a15-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="89a15-115">Stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="89a15-115">Set the following fields.</span></span>

    | <span data-ttu-id="89a15-116">Name</span><span class="sxs-lookup"><span data-stu-id="89a15-116">Name</span></span>                                     | <span data-ttu-id="89a15-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89a15-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="89a15-118">Buchungsebene</span><span class="sxs-lookup"><span data-stu-id="89a15-118">Posting layer</span></span>                            | <span data-ttu-id="89a15-119">Wählen Sie die zu verwendende Buchungsebene aus.</span><span class="sxs-lookup"><span data-stu-id="89a15-119">Select the posting layer to use.</span></span> <span data-ttu-id="89a15-120">Jedes Buch, das einem Mietvertrag beigefügt ist, wird für eine bestimmte Buchungsebene eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="89a15-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="89a15-121">Jede Buchungsebene hat unterschiedliche Buchungszwecke.</span><span class="sxs-lookup"><span data-stu-id="89a15-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="89a15-122">Mietvertragstyp</span><span class="sxs-lookup"><span data-stu-id="89a15-122">Lease type</span></span>                               | <span data-ttu-id="89a15-123">Wählen Sie aus, ob der Mietvertrag automatisch klassifiziert werden soll oder ob es als Finanzierungsleasing oder Ausrüstungs-Leasingvertrag vordefiniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="89a15-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="89a15-124">Buchhaltungsframework</span><span class="sxs-lookup"><span data-stu-id="89a15-124">Accounting framework</span></span>                     | <span data-ttu-id="89a15-125">Wählen Sie das Framework aus dass dem Buch zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="89a15-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="89a15-126">Einrichten von Mietdauer/Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="89a15-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="89a15-127">Das System klassifiziert den Mietvertrag als ein Finanzierungsleasing, wenn die Mietvertragsgart auf **Automatisch** eingestellt ist und das Verhältnis der Mietdauer zur Nutzungsdauer der Anlage größer oder gleich dem im Feld eingegebenen Prozentsatz ist.</span><span class="sxs-lookup"><span data-stu-id="89a15-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="89a15-128">Einrichtung von Barwert/Anlagenzeitwert</span><span class="sxs-lookup"><span data-stu-id="89a15-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="89a15-129">Geben Sie eine ganze Zahl ein, um den Schwellenwert zu definieren, der den Mietvertragstyp bestimmt.</span><span class="sxs-lookup"><span data-stu-id="89a15-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="89a15-130">Wenn der Barwert zukünftiger Mindestmietzahlungen höher ist als der benutzerdefinierte Wert aus der Buchkonfiguration, und wenn die Mietvertragsklassifizierung des Buches auf „Automatisch“ eingestellt ist, klassifiziert das System den Mietvertrag als Finanzierungsleasing.</span><span class="sxs-lookup"><span data-stu-id="89a15-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="89a15-131">Kurzfristiger Schwellenwert</span><span class="sxs-lookup"><span data-stu-id="89a15-131">Short-term threshold</span></span>                     | <span data-ttu-id="89a15-132">Geben Sie die Anzahl der Monate ein, die als Schwellenwert für kurzfristige Mietverträge verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89a15-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="89a15-133">Wenn die Laufzeit des Mietvertrags kleiner oder gleich der Anzahl der Monate ist, die Sie hier eingeben, klassifiziert das System den Mietvertrag als kurzfristigen Mietvertrag, und die Behandlung der zurückgestellten Miete wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="89a15-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="89a15-134">Schwellenwert für geringen Wert</span><span class="sxs-lookup"><span data-stu-id="89a15-134">Low value threshold</span></span>                      | <span data-ttu-id="89a15-135">Geben Sie einen Betrag ein, der als Schwellenwert für Leasingobjekte mit geringem Wert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89a15-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="89a15-136">Wenn der Zeitwert der Anlage kleiner oder gleich des hier eingegebenen Werts ist, klassifiziert das System den Mietvertrag als Leasingobjekt von geringem Wert, und die Behandlung der zurückgestellten Miete wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="89a15-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="89a15-137">An Kreditor bezahlen</span><span class="sxs-lookup"><span data-stu-id="89a15-137">Pay to vendor</span></span>                            | <span data-ttu-id="89a15-138">Setzen Sie diese Option auf **Ja**, damit Mietzahlungen als Rechnung auf das in jedem Mietvertrag angegebene Kreditorenkonto gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="89a15-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="89a15-139">Wenn eine Mietzahlung gebucht wird, wird das Kreditorenkonto gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="89a15-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="89a15-140">Wenn diese Option auf **Nein** gesetzt ist, wird stattdessen das Konto gutgeschrieben, das für die **Mietzahlung**-Buchungsart auf der **Leasingbuchungsparameter**-Seite angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="89a15-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
