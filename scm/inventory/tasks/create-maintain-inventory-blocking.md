---
title: Sperrung von Lagerbestand erstellen und verwalten
description: "Im folgenden Verfahren wird dargestellt, wie verhindert wird, dass physisch verfügbarer Lagerbestand durch andere ausgehende Quelldokumente mithilfe der Sperrung von Lagerbestand reserviert wird."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: de-de
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="2a458-103">Sperrung von Lagerbestand erstellen und verwalten</span><span class="sxs-lookup"><span data-stu-id="2a458-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a458-104">Im folgenden Verfahren wird dargestellt, wie verhindert wird, dass physisch verfügbarer Lagerbestand durch andere ausgehende Quelldokumente mithilfe der Sperrung von Lagerbestand reserviert wird.</span><span class="sxs-lookup"><span data-stu-id="2a458-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="2a458-105">Sie können die Prozedur im Demodatenunternehmen USMF mit den Beispielswerten ausführen, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2a458-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="2a458-106">Sie müssen einen Artikel mit physisch verfügbarem Lagerbestand haben, bevor Sie dieses Verfahren beginnen.</span><span class="sxs-lookup"><span data-stu-id="2a458-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="2a458-107">Erstellen einer Sperrung von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="2a458-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="2a458-108">Wechseln Sie zu "Lagerverwaltung" > "Periodische Aufgaben" > "Sperrung von Lagerbestand".</span><span class="sxs-lookup"><span data-stu-id="2a458-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="2a458-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2a458-109">Click New.</span></span>
3. <span data-ttu-id="2a458-110">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2a458-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2a458-111">Wählen Sie in der Liste den Artikel aus.</span><span class="sxs-lookup"><span data-stu-id="2a458-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="2a458-112">Wählen Sie eine Artikelnummer mit physischem Lagerbestand aus, die Sie sperren möchten.</span><span class="sxs-lookup"><span data-stu-id="2a458-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="2a458-113">Wenn Sie USMF verwenden, können Sie Artikel M9201 auswählen.</span><span class="sxs-lookup"><span data-stu-id="2a458-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="2a458-114">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="2a458-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2a458-115">Wenn Sie Artikel M9201 verwenden, müssen Sie weniger als 200 auswählen.</span><span class="sxs-lookup"><span data-stu-id="2a458-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="2a458-116">Schalten Sie die Erweiterung des Abschnitts "Lagerungsdimensionen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="2a458-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="2a458-117">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2a458-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2a458-118">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2a458-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2a458-119">Wenn Sie Artikel M9201 verwenden, können Sie Warehouse 51 auswählen.</span><span class="sxs-lookup"><span data-stu-id="2a458-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="2a458-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2a458-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="2a458-121">Aktualisieren Sie die Bedingungen der Sperrung von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="2a458-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="2a458-122">Geben Sie im Feld "Menge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="2a458-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2a458-123">Aktualisieren Sie das Felde "Lagermenge", um die zu sperrende Menge wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="2a458-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="2a458-124">Geben Sie im Feld "Erwartetes Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="2a458-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="2a458-125">Sie sollten angeben, wann damit gerechnet wird, dass der gesperrte Bestand für die Reservierung verfügbar wird, indem Sie ein erwartetes Datum zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2a458-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="2a458-126">Wenn die Option "Erwartete Zugänge" für die Sperrung des Lagerbestands aktiviert ist (Standardeinstellung, wenn Sie manuell eine Sperrung erstellen), wird dieses Datum auf der erwarteten Buchung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2a458-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="2a458-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2a458-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="2a458-128">Sperrung von Lagerbestand entfernen</span><span class="sxs-lookup"><span data-stu-id="2a458-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="2a458-129">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="2a458-129">Click Delete.</span></span>
2. <span data-ttu-id="2a458-130">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="2a458-130">Click Yes.</span></span>
3. <span data-ttu-id="2a458-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2a458-131">Close the page.</span></span>

