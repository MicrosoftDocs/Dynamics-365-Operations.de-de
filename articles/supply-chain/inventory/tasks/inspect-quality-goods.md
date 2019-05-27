---
title: Qualität der Waren inspizieren
description: Diese Prozedur zeigt, wie ein Qualitätsprüfungsauftrag bearbeitet wird.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545404"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="5c52d-103">Qualität der Waren inspizieren</span><span class="sxs-lookup"><span data-stu-id="5c52d-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5c52d-104">Diese Prozedur zeigt, wie ein Qualitätsprüfungsauftrag bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5c52d-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="5c52d-105">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c52d-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="5c52d-106">Bevor Sie diese Beispielprozedur beginnen, müssen Sie Bestellung "000016 " bestätigen und einen Produktzugang buchen.</span><span class="sxs-lookup"><span data-stu-id="5c52d-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="5c52d-107">Dies erstellt automatisch einen Qualitätsprüfungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="5c52d-107">This will automatically create a quality order.</span></span> <span data-ttu-id="5c52d-108">Qualitätsinspektionen werden normalerweise von einem Sachbearbeiter für die Qualitätskontrolle ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c52d-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="5c52d-109">Wählen Sie einen Qualitätsprüfungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="5c52d-109">Select a quality order</span></span>
1. <span data-ttu-id="5c52d-110">Gehen Sie zu "Lagerverwaltung" > "Periodische Aufgaben" > "Qualitätsmanagement" > "Qualitätsprüfungsaufträge".</span><span class="sxs-lookup"><span data-stu-id="5c52d-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="5c52d-111">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5c52d-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5c52d-112">Wählen Sie den Qualitätsprüfungsauftrag, der erstellt wurde, bevor Sie dieses Verfahren gestartet haben.</span><span class="sxs-lookup"><span data-stu-id="5c52d-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="5c52d-113">Erfassen von Testergebnissen</span><span class="sxs-lookup"><span data-stu-id="5c52d-113">Record test results</span></span>
1. <span data-ttu-id="5c52d-114">Klicken Sie auf "Ergebnis".</span><span class="sxs-lookup"><span data-stu-id="5c52d-114">Click Results.</span></span>
2. <span data-ttu-id="5c52d-115">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="5c52d-115">Click Edit.</span></span>
3. <span data-ttu-id="5c52d-116">Geben Sie im Feld "Ergebnismenge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5c52d-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="5c52d-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="5c52d-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="5c52d-118">Klicken Sie im Feld "Ergebnis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5c52d-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5c52d-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5c52d-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5c52d-120">In diesem Beispiel basiert das Ergebnis auf einem vordefinierten Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="5c52d-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="5c52d-121">Normalerweise erfassen Sie ein spezifischeres Testergebnis, z. B. eine Größe oder eine andere Dimension.</span><span class="sxs-lookup"><span data-stu-id="5c52d-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="5c52d-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5c52d-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5c52d-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5c52d-123">Click Save.</span></span>
9. <span data-ttu-id="5c52d-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c52d-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="5c52d-125">Qualitätsprüfungsauftrag überprüfen</span><span class="sxs-lookup"><span data-stu-id="5c52d-125">Validate the quality order</span></span>
1. <span data-ttu-id="5c52d-126">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="5c52d-126">Click Validate.</span></span>
2. <span data-ttu-id="5c52d-127">Klicken Sie im Feld "Überprüft von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5c52d-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5c52d-128">Wählen Sie den Benutzer aus, der die Inspektion ausführt.</span><span class="sxs-lookup"><span data-stu-id="5c52d-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="5c52d-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5c52d-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5c52d-130">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="5c52d-130">Click Select.</span></span>
5. <span data-ttu-id="5c52d-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="5c52d-131">Click OK.</span></span>
6. <span data-ttu-id="5c52d-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5c52d-132">Close the page.</span></span>

