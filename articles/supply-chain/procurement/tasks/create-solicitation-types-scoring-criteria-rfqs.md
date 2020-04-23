---
title: Ausschreibungstypen und Bewertungskriterien für Angebotsanforderungen erstellen
description: Dieser Leitfaden zeigt Ihnen, wie man einen Ausschreibungstyp erstellt und diesen einer Bewertungsmethode zuordnet.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b3876238a191cbbacc4e8c435bb798232e6fd6f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204676"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="cac62-103">Ausschreibungstypen und Bewertungskriterien für Angebotsanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="cac62-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cac62-104">Dieser Leitfaden zeigt Ihnen, wie man einen Ausschreibungstyp erstellt und diesen einer Bewertungsmethode zuordnet.</span><span class="sxs-lookup"><span data-stu-id="cac62-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="cac62-105">Er zeigt auch, wie man den Ausschreibungstyp auf eine Angebotsanforderung anwendet, wodurch die Standardbewertungsmethode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cac62-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="cac62-106">Diese Aufgaben werden normalerweise von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cac62-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="cac62-107">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="cac62-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="cac62-108">Sie müssen eine Bewertungsmethode verfügbar haben, bevor Sie beginnen.</span><span class="sxs-lookup"><span data-stu-id="cac62-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="cac62-109">Erstellt eines neuen Anforderungstyps</span><span class="sxs-lookup"><span data-stu-id="cac62-109">Create a solicitation type</span></span>
1. <span data-ttu-id="cac62-110">Wechseln Sie zu Beschaffung > Einstellungen > Angebotsanforderung > Anforderungstyp.</span><span class="sxs-lookup"><span data-stu-id="cac62-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="cac62-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="cac62-111">Click New.</span></span>
3. <span data-ttu-id="cac62-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="cac62-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cac62-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="cac62-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cac62-114">Wählen Sie im Feld "Bewertungsmethode" die Bewertungsmethode aus, die Sie für diesen Ausschreibungstyp verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="cac62-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="cac62-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="cac62-115">Click Save.</span></span>
7. <span data-ttu-id="cac62-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cac62-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="cac62-117">Den Ausschreibungstyp verwenden</span><span class="sxs-lookup"><span data-stu-id="cac62-117">Use the solicitation type</span></span>
1. <span data-ttu-id="cac62-118">Wechseln Sie zu "Beschaffung" > "Angebotsanforderungen" > "Alle Angebotsanforderungen".</span><span class="sxs-lookup"><span data-stu-id="cac62-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="cac62-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="cac62-119">Click New.</span></span>
3. <span data-ttu-id="cac62-120">Wählen Sie im Feld "Ausschreibungstyp" den Ausschreibungstyp aus, den Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="cac62-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="cac62-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cac62-121">Click OK.</span></span>
5. <span data-ttu-id="cac62-122">Klicken Sie auf "Bewertungskriterien".</span><span class="sxs-lookup"><span data-stu-id="cac62-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="cac62-123">Die Bewertungskriterien, die angezeigt werden, sind diejenigen von der Bewertungsmethode, die Sie dem Ausschreibungstyp zugeordnet haben.</span><span class="sxs-lookup"><span data-stu-id="cac62-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="cac62-124">Auf dieser Seite können Sie auswählen, Kriterien hinzuzufügen oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cac62-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="cac62-125">Es ist auch möglich, neue Kriterien hinzuzufügen, indem Sie diese aus anderen Bewertungsmethoden kopieren.</span><span class="sxs-lookup"><span data-stu-id="cac62-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="cac62-126">Klicken Sie auf "Kriterien kopieren".</span><span class="sxs-lookup"><span data-stu-id="cac62-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="cac62-127">Geben Sie im Feld "Bewertungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="cac62-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="cac62-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="cac62-128">Click OK.</span></span>
9. <span data-ttu-id="cac62-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cac62-129">Close the page.</span></span>

