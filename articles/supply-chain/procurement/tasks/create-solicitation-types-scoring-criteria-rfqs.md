---
title: Ausschreibungstypen und Bewertungskriterien für Angebotsanforderungen erstellen
description: Dieser Leitfaden zeigt Ihnen, wie man einen Ausschreibungstyp erstellt und diesen einer Bewertungsmethode zuordnet.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812061"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="8e26d-103">Ausschreibungstypen und Bewertungskriterien für Angebotsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="8e26d-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e26d-104">Dieser Leitfaden zeigt Ihnen, wie man einen Ausschreibungstyp erstellt und diesen einer Bewertungsmethode zuordnet.</span><span class="sxs-lookup"><span data-stu-id="8e26d-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="8e26d-105">Er zeigt auch, wie man den Ausschreibungstyp auf eine Angebotsanforderung anwendet, wodurch die Standardbewertungsmethode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8e26d-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="8e26d-106">Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e26d-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="8e26d-107">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e26d-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8e26d-108">Sie müssen eine Bewertungsmethode verfügbar haben, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="8e26d-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="8e26d-109">Erstellt eines neuen Anforderungstyps</span><span class="sxs-lookup"><span data-stu-id="8e26d-109">Create a solicitation type</span></span>
1. <span data-ttu-id="8e26d-110">Wechseln Sie zu Beschaffung > Einstellungen > Angebotsanforderung > Anforderungstyp.</span><span class="sxs-lookup"><span data-stu-id="8e26d-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="8e26d-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8e26d-111">Click New.</span></span>
3. <span data-ttu-id="8e26d-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8e26d-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8e26d-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="8e26d-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8e26d-114">Wählen Sie im Feld "Bewertungsmethode" die Bewertungsmethode aus, die Sie für diesen Ausschreibungstyp verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8e26d-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="8e26d-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8e26d-115">Click Save.</span></span>
7. <span data-ttu-id="8e26d-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8e26d-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="8e26d-117">Den Ausschreibungstyp verwenden</span><span class="sxs-lookup"><span data-stu-id="8e26d-117">Use the solicitation type</span></span>
1. <span data-ttu-id="8e26d-118">Wechseln Sie zu "Beschaffung" > "Angebotsanforderungen" > "Alle Angebotsanforderungen".</span><span class="sxs-lookup"><span data-stu-id="8e26d-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="8e26d-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8e26d-119">Click New.</span></span>
3. <span data-ttu-id="8e26d-120">Wählen Sie im Feld "Ausschreibungstyp" den Ausschreibungstyp aus, den Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="8e26d-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="8e26d-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e26d-121">Click OK.</span></span>
5. <span data-ttu-id="8e26d-122">Klicken Sie auf "Bewertungskriterien".</span><span class="sxs-lookup"><span data-stu-id="8e26d-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="8e26d-123">Die Bewertungskriterien, die angezeigt werden, sind diejenigen von der Bewertungsmethode, die Sie dem Ausschreibungstyp zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="8e26d-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="8e26d-124">Auf dieser Seite können Sie auswählen, Kriterien hinzuzufügen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8e26d-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="8e26d-125">Es ist auch möglich, neue Kriterien hinzuzufügen, indem Sie diese aus anderen Bewertungsmethoden kopieren.</span><span class="sxs-lookup"><span data-stu-id="8e26d-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="8e26d-126">Klicken Sie auf "Kriterien kopieren".</span><span class="sxs-lookup"><span data-stu-id="8e26d-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="8e26d-127">Geben Sie im Feld "Bewertungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8e26d-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="8e26d-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e26d-128">Click OK.</span></span>
9. <span data-ttu-id="8e26d-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8e26d-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]