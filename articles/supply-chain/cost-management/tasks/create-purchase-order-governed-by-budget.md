---
title: Eine durch das Budget gesteuerte Bestellung erstellen
description: Erstellen Sie mit diesem Verfahren eine Bestellung, die auf einem verfügbaren Budget basiert.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 319eb0070a3677035e2a5d89744e80cd38c08d8e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980506"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="0e01f-103">Eine durch das Budget gesteuerte Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="0e01f-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e01f-104">Erstellen Sie mit diesem Verfahren eine Bestellung, die auf einem verfügbaren Budget basiert.</span><span class="sxs-lookup"><span data-stu-id="0e01f-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="0e01f-105">Für diese Aufzeichnung wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e01f-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="0e01f-106">Budgetsteuerungskonfiguration überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0e01f-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="0e01f-107">Klicken auf Budgetierung >Einrichtung > Budgetsteuerung > Budgetsteuerungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e01f-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="0e01f-108">Klicken Sie auf verfügbare Budgetmittel.</span><span class="sxs-lookup"><span data-stu-id="0e01f-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="0e01f-109">Klicken Sie auf die Dokument- und Erfassungsregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="0e01f-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="0e01f-110">Klicken Sie auf die Registerkarte Budgetsteuerregel definieren.</span><span class="sxs-lookup"><span data-stu-id="0e01f-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="0e01f-111">Klicken Sie auf die Registerkarte Budgetgruppe definieren.</span><span class="sxs-lookup"><span data-stu-id="0e01f-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="0e01f-112">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0e01f-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="0e01f-113">Erstellen Sie den Bestellkopf</span><span class="sxs-lookup"><span data-stu-id="0e01f-113">Create the purchase order header</span></span>
1. <span data-ttu-id="0e01f-114">Wechseln Sie zu "Beschaffung" > "Bestellung" > "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="0e01f-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0e01f-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0e01f-115">Click New.</span></span>
3. <span data-ttu-id="0e01f-116">Geben Sie im Feld "Kreditorenkonto" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e01f-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="0e01f-117">Erweitern Sie den Abschnitt "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="0e01f-117">Expand the General section.</span></span>
5. <span data-ttu-id="0e01f-118">Wählen Sie im Feld Buchhaltungsdatum das Datum auf 2016-01-01 fest.</span><span class="sxs-lookup"><span data-stu-id="0e01f-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="0e01f-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0e01f-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="0e01f-120">Fügen Sie eine Bestellposition hinzu</span><span class="sxs-lookup"><span data-stu-id="0e01f-120">Add a purchase order line</span></span>
1. <span data-ttu-id="0e01f-121">Geben Sie im Feld "Beschaffungskategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e01f-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="0e01f-122">Legen Sie "Menge" auf "2" fest.</span><span class="sxs-lookup"><span data-stu-id="0e01f-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="0e01f-123">Geben Sie im Feld 'Einheit' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0e01f-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="0e01f-124">Legen Sie "Preis je Einheit" auf "10000" fest.</span><span class="sxs-lookup"><span data-stu-id="0e01f-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="0e01f-125">Klicken Sie auf "Finanzdaten".</span><span class="sxs-lookup"><span data-stu-id="0e01f-125">Click Financials.</span></span>
6. <span data-ttu-id="0e01f-126">Verteilungsbeträge anzeigen</span><span class="sxs-lookup"><span data-stu-id="0e01f-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="0e01f-127">Geben Sie im Feld "Sachkonto" den Wert 601300-001-023-- an.</span><span class="sxs-lookup"><span data-stu-id="0e01f-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="0e01f-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0e01f-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="0e01f-129">Budgetprüfung ausführen</span><span class="sxs-lookup"><span data-stu-id="0e01f-129">Perform budget checking</span></span>
1. <span data-ttu-id="0e01f-130">Klicken Sie auf "Finanzdaten".</span><span class="sxs-lookup"><span data-stu-id="0e01f-130">Click Financials.</span></span>
2. <span data-ttu-id="0e01f-131">Budgetprüfung ausführen anklicken.</span><span class="sxs-lookup"><span data-stu-id="0e01f-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="0e01f-132">Klicken Sie auf "Finanzdaten".</span><span class="sxs-lookup"><span data-stu-id="0e01f-132">Click Financials.</span></span>
4. <span data-ttu-id="0e01f-133">Klicken Sie auf Fehler oder Warnungen der Budgetprüfung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0e01f-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="0e01f-134">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="0e01f-134">Click Close.</span></span>

