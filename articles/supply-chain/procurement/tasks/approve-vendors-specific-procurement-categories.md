---
title: Kreditoren für spezifische Beschaffungskategorien genehmigen
description: In diesem Thema wird erläutert, wie Kreditoren für bestimmte Beschaffungskategorien in Dynamics 365 Supply Chain Management genehmigt werden.
author: RichardLuan
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 159d918a4dd3b6502bc8ab411d0353545eb4fcba
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016348"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="a6e1f-103">Kreditoren für spezifische Beschaffungskategorien genehmigen</span><span class="sxs-lookup"><span data-stu-id="a6e1f-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6e1f-104">In diesem Thema wird erläutert, wie Kreditoren für bestimmte Beschaffungskategorien in Dynamics 365 Supply Chain Management genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a6e1f-105">Wenn eine Bestellanforderung erstellt wird, gibt es möglicherweise eine Anforderung, einen genehmigten oder bevorzugten Kreditor auszuwählen, je nachdem, wie Einkaufsrichtlinien eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="a6e1f-106">Diese Prozedur zeigt Ihnen, wie man angibt, dass ein Kreditor für eine spezifische Beschaffungskategorie genehmigt oder bevorzugt ist.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="a6e1f-107">Diese Aufgabe ist in der Regel von einem Beschaffungsspezialisten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="a6e1f-108">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="a6e1f-109">Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Kreditoren > Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="a6e1f-110">Wählen Sie den Kreditor aus, den Sie als genehmigten oder bevorzugten Kreditor für eine Kategorie festgelegt haben möchten.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="a6e1f-111">Wählen Sie im Aktivitätsbereich **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="a6e1f-112">Wählen Sie **Kategorien**.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-112">Select **Categories**.</span></span>
5. <span data-ttu-id="a6e1f-113">Wählen Sie **Kategorie hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-113">Select **Add category**.</span></span>
6. <span data-ttu-id="a6e1f-114">Wählen Sie im Feld **Kategorie** die Option **BÜRO- UND SCHREIBTISCHZUBEHÖR (BÜRO- UND SCHREIBTISCHZUBEHÖR)** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="a6e1f-115">Wählen Sie im Feld **Kreditorkategoriestatus** die Option **Bevorzugt** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="a6e1f-116">Es ist auch möglich, mehr als einen bevorzugten Kreditor für eine Kategorie anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="a6e1f-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-117">Select **Save**.</span></span>
9. <span data-ttu-id="a6e1f-118">Wechseln Sie im Navigationsbereich zu **Module > Beschaffung > Beschaffungskategorien**.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="a6e1f-119">Wählen Sie im Baum die Option **UNTERNEHMENSBESCHAFFUNGSKATEGORIEN\BÜRO- UND SCHREIBTISCHZUBEHÖR** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="a6e1f-120">Erweitern Sie den Abschnitt **Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="a6e1f-121">Überprüfen Sie, ob der Kreditor, den Sie ausgewählt haben, als bevorzugter Kreditor für die Kategorie "Büro- und Schreibtischzubehör" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="a6e1f-122">Wenn Sie diese Prozedur als Aufgabenleitfaden ausführen, müssen Sie möglicherweise die Schaltfläche **Entsperren** wählen, um einen Bildlauf nach unten zur Kreditorenliste durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="a6e1f-123">Es ist aber auch möglich, bevorzugte und genehmigte Kreditoren auf dieser Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="a6e1f-124">In der Struktur erweitern Sie den Knoten **BÜRO- UND SCHREIBTISCHZUBEHÖR** und wählen Sie **Scheren** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="a6e1f-125">Wählen Sie **Nein** im Feld **Kreditoren aus übergeordneter Kategorie erben:** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="a6e1f-126">Wählen Sie **Ja** im Feld **Kreditoren aus übergeordneter Kategorie erben:** aus.</span><span class="sxs-lookup"><span data-stu-id="a6e1f-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

