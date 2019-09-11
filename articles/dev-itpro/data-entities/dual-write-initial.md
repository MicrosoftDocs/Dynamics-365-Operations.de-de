---
title: Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations und Common Data Service
description: In diesem Thema wird die Synchronisierungsreihenfolge angegeben, die Sie beim Erstellen der anfänglichen Daten befolgen müssen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873127"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="5e60f-103">Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations und Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5e60f-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="5e60f-104">Bevor Sie die Datenintegration verwenden, müssen Sie die anfänglichen Daten erstellen, die für Debitoren, Kreditoren und Kontakte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5e60f-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="5e60f-105">Angenommen, Sie möchten einen neuen **Kreditorengruppe**-Artikel erstellen und seinen **Zahlungsbedingungen**-Wert auf **Net30** festlegen.</span><span class="sxs-lookup"><span data-stu-id="5e60f-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="5e60f-106">In diesem Fall müssen Sie, bevor Sie versuchen, den **Kreditorengruppe**-Artikel zu erstellen, überprüfen, ob **Net30** in Microsoft Dynamics 365 for Finance and Operations und Common Data Service vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5e60f-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="5e60f-107">(Bald wird eine Funktion für eine Dualschreibplattform namens Initial Sync von Microsoft veröffentlicht. Diese führt eine einmalige Datensynchronisierung zwischen Finance and Operations und Common Data Service im Rahmen der dualen Schreibeinrichtung durch.)</span><span class="sxs-lookup"><span data-stu-id="5e60f-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="5e60f-108">Microsoft veröffentlicht eine Dualschreibzuordnung für alle Referenzdaten einschließlich **Zahlungsbedingungen**.</span><span class="sxs-lookup"><span data-stu-id="5e60f-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="5e60f-109">Wenn Sie die anfänglichen Daten bereits in einem System haben, kann ein kleiner Updatevorgang in einem Datensatz einen Dualschreibvorgang in diesem Datensatz auslösen.</span><span class="sxs-lookup"><span data-stu-id="5e60f-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="5e60f-110">Sie müssen die folgende Prioritätsreihenfolge beachten und sicherstellen, dass die anfänglichen Daten sowohl in Finance and Operations als auch in Common Data Service verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5e60f-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="5e60f-111">Lieferant</span><span class="sxs-lookup"><span data-stu-id="5e60f-111">Vendor</span></span>

<span data-ttu-id="5e60f-112">Hier die Reihenfolge der Ausführung für die **Kreditor**-Entität:</span><span class="sxs-lookup"><span data-stu-id="5e60f-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="5e60f-113">Kreditorengruppe</span><span class="sxs-lookup"><span data-stu-id="5e60f-113">Vendor group</span></span>

    1. <span data-ttu-id="5e60f-114">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="5e60f-114">Terms of payment</span></span>

        1. <span data-ttu-id="5e60f-115">Zahlungstag und -positionen</span><span class="sxs-lookup"><span data-stu-id="5e60f-115">Payment day and lines</span></span>
        2. <span data-ttu-id="5e60f-116">Zahlungszeitplan</span><span class="sxs-lookup"><span data-stu-id="5e60f-116">Payment schedule</span></span>

2. <span data-ttu-id="5e60f-117">Kreditorzahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="5e60f-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="5e60f-118">Debitor (Organisation)</span><span class="sxs-lookup"><span data-stu-id="5e60f-118">Customer (Organization)</span></span>

<span data-ttu-id="5e60f-119">Hier die Reihenfolge der Ausführung für die **Debitor**-Entität:</span><span class="sxs-lookup"><span data-stu-id="5e60f-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="5e60f-120">Debitorengruppe</span><span class="sxs-lookup"><span data-stu-id="5e60f-120">Customer group</span></span>

    1. <span data-ttu-id="5e60f-121">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="5e60f-121">Terms of payment</span></span>

        1. <span data-ttu-id="5e60f-122">Zahlungstag und -positionen</span><span class="sxs-lookup"><span data-stu-id="5e60f-122">Payment day and lines</span></span>
        2. <span data-ttu-id="5e60f-123">Zahlung</span><span class="sxs-lookup"><span data-stu-id="5e60f-123">Payment</span></span> 

2. <span data-ttu-id="5e60f-124">Zahlungsmethode für Debitoren</span><span class="sxs-lookup"><span data-stu-id="5e60f-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="5e60f-125">Kontakt (Person)</span><span class="sxs-lookup"><span data-stu-id="5e60f-125">Contact (Person)</span></span>

<span data-ttu-id="5e60f-126">Hier die Reihenfolge der Ausführung für die **Kontakt**-Entität:</span><span class="sxs-lookup"><span data-stu-id="5e60f-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="5e60f-127">Debitor</span><span class="sxs-lookup"><span data-stu-id="5e60f-127">Customer</span></span>
2. <span data-ttu-id="5e60f-128">Lieferant</span><span class="sxs-lookup"><span data-stu-id="5e60f-128">Vendor</span></span>
