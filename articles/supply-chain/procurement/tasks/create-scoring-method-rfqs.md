---
title: Eine Bewertungsmethode für Angebotsanforderungen erstellen
description: Diese Prozedur zeigt Ihnen, wie eine Bewertungsmethode erstellt wird.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba3f0b2be16c02129616025c0ee6258996189c6a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211813"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="3e629-103">Eine Bewertungsmethode für Angebotsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="3e629-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e629-104">Diese Prozedur zeigt Ihnen, wie eine Bewertungsmethode erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e629-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="3e629-105">Eine Bewertungsmethode ist ein Satz von Kriterien, der verwendet werden kann, um Angebote zu vergleichen, die als Antwort auf eine Angebotsanforderung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e629-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="3e629-106">Sie möchten beispielsweise einen Kreditors für eine Leistung in der Vergangenheit bewerten, oder bewerten, ob das Unternehmen umweltfreundlich ist oder gut zusammenarbeitet, oder Sie möchten möglicherweise Angebote basierend auf dem Preis vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3e629-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="3e629-107">Die Bewertungsmethode kann einem Ausschreibungstyp als Standardbewertungsmethode für Angebotsanforderungen dieses Typs zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3e629-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="3e629-108">Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e629-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="3e629-109">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e629-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="3e629-110">Wechseln Sie zu Beschaffung > Einstellungen > Angebotsanforderung > Bewertungsmethode.</span><span class="sxs-lookup"><span data-stu-id="3e629-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="3e629-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3e629-111">Click New.</span></span>
3. <span data-ttu-id="3e629-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3e629-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3e629-114">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="3e629-114">Click Save.</span></span>
6. <span data-ttu-id="3e629-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3e629-115">Click New.</span></span>
7. <span data-ttu-id="3e629-116">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="3e629-117">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="3e629-118">Diese Beschreibung wird zusammen mit dem Bewertungsmethodennamen angezeigt, wenn eine Bewertungsmethode für eine Angebotsanforderung ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3e629-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="3e629-119">Geben Sie im Feld "Bereich ab" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="3e629-120">Der Bereich begrenzt, was der Prokurist als eine Bewertung eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="3e629-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="3e629-121">Wenn es mehrere Bewertungskriterien für eine Angebotsanforderung gibt, werden die Bewertungen, die eingegeben wurden, zueinander hinzugefügt und die Summe wird verfügbar gemacht, damit die Angebote verglichen werden können.</span><span class="sxs-lookup"><span data-stu-id="3e629-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="3e629-122">Geben Sie im Feld "Bereich bis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="3e629-123">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3e629-123">Click New.</span></span>
12. <span data-ttu-id="3e629-124">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="3e629-125">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="3e629-126">Geben Sie im Feld "Bereich ab" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="3e629-127">Geben Sie im Feld "Bereich bis" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="3e629-127">In the Range to field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]