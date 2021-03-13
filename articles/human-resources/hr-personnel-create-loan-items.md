---
title: Ausleihartikel einrichten
description: Ausleihartikel sind Datensätze, die Ihnen helfen, physische Artikel, wie Telefone oder Computer, zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7da578c57be57b55e9175600461549416faa1298
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130348"
---
# <a name="create-loan-items"></a><span data-ttu-id="ede94-103">Ausleihartikel einrichten</span><span class="sxs-lookup"><span data-stu-id="ede94-103">Create loan items</span></span>



<span data-ttu-id="ede94-104">Ausleihartikel sind Datensätze, die Ihnen helfen, physische Artikel, wie Telefone oder Computer, zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht.</span><span class="sxs-lookup"><span data-stu-id="ede94-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="ede94-105">Jeder physische Artikel muss einen entsprechenden Ausleihartikel haben.</span><span class="sxs-lookup"><span data-stu-id="ede94-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="ede94-106">Jeder Ausleihartikel-Datensatz beschreibt, was ausgeliehen wird, wer für das Ausleihen zuständig ist und die Anzahl von Tage, die der Artikel ausgeliehen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ede94-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="ede94-107">Sie können mehrere Ausleihartikel, wie Schlüssel, Zugangsberechtigungskarten oder Uniformen, gleichzeitig erstellen.</span><span class="sxs-lookup"><span data-stu-id="ede94-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="ede94-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="ede94-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="ede94-109">Ausleihtypen einrichten</span><span class="sxs-lookup"><span data-stu-id="ede94-109">Create Loan types</span></span>
1. <span data-ttu-id="ede94-110">Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Ausleihartikel" > "Ausleihtypen".</span><span class="sxs-lookup"><span data-stu-id="ede94-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="ede94-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ede94-111">Click New.</span></span>
3. <span data-ttu-id="ede94-112">Geben Sie im Feld "Ausleihtypen" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="ede94-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ede94-114">Geben Sie die Anzahl der Tage ein, die diesem Ausleihtyp zugeordnete Artikel überfällig sein können.</span><span class="sxs-lookup"><span data-stu-id="ede94-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="ede94-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ede94-115">Click Save.</span></span>
7. <span data-ttu-id="ede94-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ede94-116">Close the page.</span></span>
8. <span data-ttu-id="ede94-117">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ede94-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="ede94-118">Ausleihartikel erstellen</span><span class="sxs-lookup"><span data-stu-id="ede94-118">Create Loan items</span></span>
1. <span data-ttu-id="ede94-119">Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Ausleihartikel" > "Ausleihartikel".</span><span class="sxs-lookup"><span data-stu-id="ede94-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="ede94-120">Klicken Sie auf "Ausleihartikel einrichten".</span><span class="sxs-lookup"><span data-stu-id="ede94-120">Click Create loan items.</span></span>
3. <span data-ttu-id="ede94-121">Im Feld "Mge." eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="ede94-122">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ede94-123">Klicken Sie im Feld "Ausleihtyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ede94-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ede94-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ede94-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ede94-125">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ede94-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ede94-126">Geben Sie hier die maximale Ausleihdauer in Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="ede94-127">Der Standardwert im Feld "Geplante Rückgabe" auf der Seite "Ausgeliehene Ausrüstung" wird als aktuelles Datum zuzüglich der Nummer berechnet.</span><span class="sxs-lookup"><span data-stu-id="ede94-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="ede94-128">Klicken Sie im Feld "Zuständige Person" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ede94-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ede94-129">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="ede94-129">Click Select.</span></span>
11. <span data-ttu-id="ede94-130">Geben Sie eine Zahl in das Feld "Anfangswert" ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="ede94-131">Geben Sie im Feld "Intervall" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="ede94-132">Geben Sie im Feld "Format" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="ede94-133">Wenn die Startnummer für einen Ausleihartikel beispielsweise 10 ist, geben Sie im Feld "Format" zwei Nummernzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="ede94-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="ede94-134">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ede94-134">Click OK.</span></span>
15. <span data-ttu-id="ede94-135">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ede94-135">Refresh the page.</span></span>

