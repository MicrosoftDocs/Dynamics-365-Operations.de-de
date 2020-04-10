---
title: Eine Bewertungsmethode für Angebotsanforderungen erstellen
description: Diese Prozedur zeigt Ihnen, wie eine Bewertungsmethode erstellt wird.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0e1fe2a27998c01012e40d80eacf13aa11f5689
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147341"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="bdf79-103">Eine Bewertungsmethode für Angebotsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="bdf79-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdf79-104">Diese Prozedur zeigt Ihnen, wie eine Bewertungsmethode erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bdf79-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="bdf79-105">Eine Bewertungsmethode ist ein Satz von Kriterien, der verwendet werden kann, um Angebote zu vergleichen, die als Antwort auf eine Angebotsanforderung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdf79-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="bdf79-106">Sie möchten beispielsweise einen Kreditors für eine Leistung in der Vergangenheit bewerten, oder bewerten, ob das Unternehmen umweltfreundlich ist oder gut zusammenarbeitet, oder Sie möchten möglicherweise Angebote basierend auf dem Preis vergleichen.</span><span class="sxs-lookup"><span data-stu-id="bdf79-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="bdf79-107">Die Bewertungsmethode kann einem Ausschreibungstyp als Standardbewertungsmethode für Angebotsanforderungen dieses Typs zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="bdf79-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="bdf79-108">Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdf79-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="bdf79-109">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="bdf79-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="bdf79-110">Wechseln Sie zu Beschaffung > Einstellungen > Angebotsanforderung > Bewertungsmethode.</span><span class="sxs-lookup"><span data-stu-id="bdf79-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="bdf79-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="bdf79-111">Click New.</span></span>
3. <span data-ttu-id="bdf79-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bdf79-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bdf79-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="bdf79-114">Click Save.</span></span>
6. <span data-ttu-id="bdf79-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="bdf79-115">Click New.</span></span>
7. <span data-ttu-id="bdf79-116">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="bdf79-117">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="bdf79-118">Diese Beschreibung wird zusammen mit dem Bewertungsmethodennamen angezeigt, wenn eine Bewertungsmethode für eine Angebotsanforderung ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bdf79-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="bdf79-119">Geben Sie im Feld "Bereich ab" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="bdf79-120">Der Bereich begrenzt, was der Prokurist als eine Bewertung eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="bdf79-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="bdf79-121">Wenn es mehrere Bewertungskriterien für eine Angebotsanforderung gibt, werden die Bewertungen, die eingegeben wurden, zueinander hinzugefügt und die Summe wird verfügbar gemacht, damit die Angebote verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="bdf79-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="bdf79-122">Geben Sie im Feld "Bereich bis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="bdf79-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="bdf79-123">Click New.</span></span>
12. <span data-ttu-id="bdf79-124">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="bdf79-125">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="bdf79-126">Geben Sie im Feld "Bereich ab" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="bdf79-127">Geben Sie im Feld "Bereich bis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bdf79-127">In the Range to field, enter a number.</span></span>

