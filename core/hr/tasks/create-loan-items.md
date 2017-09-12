--- 
title: Ausleihartikel einrichten
description: "Ausleihartikel sind Datensätze, die Ihnen helfen, physische Artikel, wie Telefone oder Computer, zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65655283c70c99b5d64289b319ecc69f6e414221
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="create-loan-items"></a><span data-ttu-id="81d65-103">Ausleihartikel einrichten</span><span class="sxs-lookup"><span data-stu-id="81d65-103">Create loan items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81d65-104">Ausleihartikel sind Datensätze, die Ihnen helfen, physische Artikel, wie Telefone oder Computer, zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht.</span><span class="sxs-lookup"><span data-stu-id="81d65-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="81d65-105">Jeder physische Artikel muss einen entsprechenden Ausleihartikel haben.</span><span class="sxs-lookup"><span data-stu-id="81d65-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="81d65-106">Jeder Ausleihartikel-Datensatz beschreibt, was ausgeliehen wird, wer für das Ausleihen zuständig ist und die Anzahl von Tage, die der Artikel ausgeliehen werden kann.</span><span class="sxs-lookup"><span data-stu-id="81d65-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="81d65-107">Sie können mehrere Ausleihartikel, wie Schlüssel, Zugangsberechtigungskarten oder Uniformen, gleichzeitig erstellen.</span><span class="sxs-lookup"><span data-stu-id="81d65-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="81d65-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="81d65-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="81d65-109">Ausleihtypen einrichten</span><span class="sxs-lookup"><span data-stu-id="81d65-109">Create Loan types</span></span>
1. <span data-ttu-id="81d65-110">Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Ausleihartikel" > "Ausleihtypen".</span><span class="sxs-lookup"><span data-stu-id="81d65-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="81d65-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="81d65-111">Click New.</span></span>
3. <span data-ttu-id="81d65-112">Geben Sie im Feld "Ausleihtypen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="81d65-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="81d65-114">Geben Sie die Anzahl der Tage ein, die diesem Ausleihtyp zugeordnete Artikel überfällig sein können.</span><span class="sxs-lookup"><span data-stu-id="81d65-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="81d65-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81d65-115">Click Save.</span></span>
7. <span data-ttu-id="81d65-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81d65-116">Close the page.</span></span>
8. <span data-ttu-id="81d65-117">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81d65-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="81d65-118">Ausleihartikel erstellen</span><span class="sxs-lookup"><span data-stu-id="81d65-118">Create Loan items</span></span>
1. <span data-ttu-id="81d65-119">Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Ausleihartikel" > "Ausleihartikel".</span><span class="sxs-lookup"><span data-stu-id="81d65-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="81d65-120">Klicken Sie auf "Ausleihartikel einrichten".</span><span class="sxs-lookup"><span data-stu-id="81d65-120">Click Create loan items.</span></span>
3. <span data-ttu-id="81d65-121">Im Feld "Mge."</span><span class="sxs-lookup"><span data-stu-id="81d65-121">In the Qty.</span></span> <span data-ttu-id="81d65-122">eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-122">field, enter a number.</span></span>
4. <span data-ttu-id="81d65-123">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-123">In the Description field, type a value.</span></span>
5. <span data-ttu-id="81d65-124">Klicken Sie im Feld "Ausleihtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81d65-124">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="81d65-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81d65-125">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="81d65-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81d65-126">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="81d65-127">Geben Sie hier die maximale Ausleihdauer in Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-127">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="81d65-128">Der Standardwert im Feld "Geplante Rückgabe" auf der Seite "Ausgeliehene Ausrüstung" wird als aktuelles Datum zuzüglich der Nummer berechnet.</span><span class="sxs-lookup"><span data-stu-id="81d65-128">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="81d65-129">Klicken Sie im Feld "Zuständige Person" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81d65-129">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="81d65-130">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="81d65-130">Click Select.</span></span>
11. <span data-ttu-id="81d65-131">Geben Sie eine Zahl in das Feld "Anfangswert" ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-131">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="81d65-132">Geben Sie im Feld "Intervall" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-132">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="81d65-133">Geben Sie im Feld "Format" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-133">In the Format field, type a value.</span></span>
    * <span data-ttu-id="81d65-134">Wenn die Startnummer für einen Ausleihartikel beispielsweise 10 ist, geben Sie im Feld "Format" zwei Nummernzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="81d65-134">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="81d65-135">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="81d65-135">Click OK.</span></span>
15. <span data-ttu-id="81d65-136">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81d65-136">Refresh the page.</span></span>


