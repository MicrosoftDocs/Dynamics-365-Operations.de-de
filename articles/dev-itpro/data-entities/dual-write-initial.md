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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797297"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="a0c43-103">Ausführungsreihenfolge der Erstsynchronisierung für Finance and Operations und Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a0c43-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="a0c43-104">Bevor Sie die Datenintegration verwenden, müssen Sie die anfänglichen Daten erstellen, die für Debitoren, Kreditoren und Kontakte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a0c43-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="a0c43-105">Wenn Sie beispielsweise ein neues Element **Kreditorengruppe** erstellen und seine **Zahlungsbedingungen** als **Net30** festlegen möchten, müssen Sie vor dem Erstellen der **Kreditorengruppe** sicherstellen, dass **Net30** sowohl in Finance and Operations als auch in Common Data Service vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a0c43-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="a0c43-106">(Bald wird eine Funktion für eine Dualschreibplattform namens **Initial Sync** veröffentlicht. Diese führt eine einmalige Datensynchronisierung zwischen Finance and Operations und Common Data Service im Rahmen der dualen Schreibeinrichtung durch.)</span><span class="sxs-lookup"><span data-stu-id="a0c43-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="a0c43-107">Tipps: Wir veröffentlichen eine Dualschreibzuordnung für alle Referenzdaten einschließlich **Zahlungsbedingungen**.</span><span class="sxs-lookup"><span data-stu-id="a0c43-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="a0c43-108">Wenn Sie die anfänglichen Daten bereits in einem System haben, kann ein kleiner Updatevorgang in einem Datensatz einen Dualschreibvorgang in diesem Datensatz auslösen.</span><span class="sxs-lookup"><span data-stu-id="a0c43-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="a0c43-109">Sie müssen die folgende Prioritätsreihenfolge beachten und sicherstellen, dass die anfänglichen Daten sowohl in Finance and Operations als auch in Common Data Service verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a0c43-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="a0c43-110">Lieferant</span><span class="sxs-lookup"><span data-stu-id="a0c43-110">Vendor</span></span>

<span data-ttu-id="a0c43-111">Die Ausführungsreihenfolge für Kreditor ist:</span><span class="sxs-lookup"><span data-stu-id="a0c43-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="a0c43-112">Debitor (Organisation)</span><span class="sxs-lookup"><span data-stu-id="a0c43-112">Customer (Organization)</span></span>

<span data-ttu-id="a0c43-113">Die Ausführungsreihenfolge für Debitor ist:</span><span class="sxs-lookup"><span data-stu-id="a0c43-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="a0c43-114">Kontakt (Person)</span><span class="sxs-lookup"><span data-stu-id="a0c43-114">Contact (Person)</span></span>

<span data-ttu-id="a0c43-115">Die Ausführungsreihenfolge für Kontakt ist:</span><span class="sxs-lookup"><span data-stu-id="a0c43-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
