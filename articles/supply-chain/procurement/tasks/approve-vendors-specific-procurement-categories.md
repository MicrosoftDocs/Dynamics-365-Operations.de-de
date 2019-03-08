---
title: Kreditoren für spezifische Beschaffungskategorien genehmigen
description: Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308390"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="c0ea6-103">Kreditoren für spezifische Beschaffungskategorien genehmigen</span><span class="sxs-lookup"><span data-stu-id="c0ea6-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0ea6-104">Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="c0ea6-105">Diese Prozedur zeigt Ihnen, wie man angibt, dass ein Kreditor für eine spezifische Beschaffungskategorie genehmigt oder bevorzugt ist.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="c0ea6-106">Diese Aufgabe ist in der Regel von einem Beschaffungsspezialisten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="c0ea6-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="c0ea6-108">Klicken Sie auf "Beschaffung" > "Kreditoren" > "Alle Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="c0ea6-109">Wählen Sie den Kreditor aus, den Sie als genehmigten oder bevorzugten Kreditor für eine Kategorie festgelegt haben möchten.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="c0ea6-110">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="c0ea6-111">Klicken Sie auf "Kategorien".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-111">Click Categories.</span></span>
5. <span data-ttu-id="c0ea6-112">Klicken Sie auf "Kategorie hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-112">Click Add category.</span></span>
6. <span data-ttu-id="c0ea6-113">Wählen Sie im Feld "Kategorie" die Option "BÜRO- UND SCHREIBTISCHZUBEHÖR (BÜRO- UND SCHREIBTISCHZUBEHÖR) aus.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="c0ea6-114">Wählen Sie im Feld "Kreditorkategoriestatus" die Option "Bevorzugt" aus.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="c0ea6-115">Es ist möglich, mehr als einen bevorzugten Kreditor für eine Kategorie anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="c0ea6-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-116">Click Save.</span></span>
9. <span data-ttu-id="c0ea6-117">Wechseln Sie zu "Beschaffung" > "Beschaffungskategorien".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="c0ea6-118">Wählen Sie im Baum die Option "UNTERNEHMENSBESCHAFFUNGSKATEGORIEN\BÜRO- UND SCHREIBTISCHZUBEHÖR" aus.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="c0ea6-119">Erweitern Sie den Abschnitt "Kreditoren".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="c0ea6-120">Überprüfen Sie, ob der Kreditor, den Sie ausgewählt haben, als bevorzugter Kreditor für die Kategorie "Büro- und Schreibtischzubehör" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="c0ea6-121">Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie möglicherweise auf die Schaltfläche "Entsperren" klicken, um einen Bildlauf nach unten zur Kreditorenliste durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="c0ea6-122">Es ist auch möglich, bevorzugte und genehmigte Kreditoren auf dieser Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="c0ea6-123">Erweitern Sie im Baum die Option "BÜRO- UND SCHREIBTISCHZUBEHÖR".</span><span class="sxs-lookup"><span data-stu-id="c0ea6-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="c0ea6-124">Wählen Sie im Baum "Scheren" aus.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="c0ea6-125">Wählen Sie "Nein" im Feld "Kreditoren aus übergeordneter Kategorie erben:" aus.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="c0ea6-126">Wählen Sie "Ja" im Feld "Kreditoren aus übergeordneter Kategorie erben:" aus.</span><span class="sxs-lookup"><span data-stu-id="c0ea6-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

