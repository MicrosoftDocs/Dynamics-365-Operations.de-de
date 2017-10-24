--- 
title: Eine Formel kopieren
description: Diese Prozedur fokussiert sich auf das Erstellen einer Formel, die die gleichen Substanzen wie eine vorhandene Formel umfasst, jedoch mit kleinen Unterschieden.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 036bd9f592ca584afad9d4b9b7a49a9787076056
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="copy-a-formula"></a><span data-ttu-id="4291a-103">Eine Formel kopieren</span><span class="sxs-lookup"><span data-stu-id="4291a-103">Copy a formula</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4291a-104">Diese Prozedur fokussiert sich auf das Erstellen einer Formel, die die gleichen Substanzen wie eine vorhandene Formel umfasst, jedoch mit kleinen Unterschieden.</span><span class="sxs-lookup"><span data-stu-id="4291a-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="4291a-105">Um die Formelpositionen zu erstellen, können Sie die Kopierfunktion verwenden, um eine vorhandene Formel zu kopieren, die die meisten Substanzen hat, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="4291a-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="4291a-106">Sie können die erforderlichen Änderungen an den einzelnen Positionen in der neuen Version nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="4291a-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="4291a-107">Wenn Sie die Kopierfunktion verwenden, müssen Sie nicht mehrere nahezu identische Formeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="4291a-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="4291a-108">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USP2.</span><span class="sxs-lookup"><span data-stu-id="4291a-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="4291a-109">Erstellen einer Formel</span><span class="sxs-lookup"><span data-stu-id="4291a-109">Create a formula</span></span>
1. <span data-ttu-id="4291a-110">Wechseln Sie zu "Produktinformationsverwaltung" > "Stücklisten und Formeln" > "Formeln".</span><span class="sxs-lookup"><span data-stu-id="4291a-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="4291a-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4291a-111">Click New.</span></span>
3. <span data-ttu-id="4291a-112">Geben Sie im Feld "Formel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4291a-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="4291a-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4291a-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="4291a-114">Geben Sie einen aussagekräftigen Namen für die Formel ein.</span><span class="sxs-lookup"><span data-stu-id="4291a-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="4291a-115">Klicken Sie im Feld "Standort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4291a-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4291a-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4291a-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4291a-117">Klicken Sie im Feld "Artikelgruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4291a-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4291a-118">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4291a-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="4291a-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4291a-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4291a-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="4291a-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="4291a-121">Formelpositionen kopieren</span><span class="sxs-lookup"><span data-stu-id="4291a-121">Copy formula lines</span></span>
1. <span data-ttu-id="4291a-122">Klicken Sie im Aktivitätsbereich auf "Formel".</span><span class="sxs-lookup"><span data-stu-id="4291a-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="4291a-123">Klicken Sie auf Kopieren.</span><span class="sxs-lookup"><span data-stu-id="4291a-123">Click Copy.</span></span>
3. <span data-ttu-id="4291a-124">Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4291a-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4291a-125">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4291a-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4291a-126">Klicken Sie im Feld "Formelversion" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4291a-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4291a-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4291a-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4291a-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4291a-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="4291a-129">Kopierte Formelpositionen anpassen</span><span class="sxs-lookup"><span data-stu-id="4291a-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="4291a-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="4291a-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="4291a-131">Klicken Sie auf Löschen.</span><span class="sxs-lookup"><span data-stu-id="4291a-131">Click Delete.</span></span>
3. <span data-ttu-id="4291a-132">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="4291a-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="4291a-133">Formel genehmigen</span><span class="sxs-lookup"><span data-stu-id="4291a-133">Approve formula</span></span>
1. <span data-ttu-id="4291a-134">Klicken Sie im Aktivitätsbereich auf "Formel".</span><span class="sxs-lookup"><span data-stu-id="4291a-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="4291a-135">Klicken Sie auf Formel genehmigen.</span><span class="sxs-lookup"><span data-stu-id="4291a-135">Click Approve formula.</span></span>
3. <span data-ttu-id="4291a-136">Klicken Sie im Feld "Genehmigt von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4291a-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4291a-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4291a-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4291a-138">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="4291a-138">Click Select.</span></span>
6. <span data-ttu-id="4291a-139">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="4291a-139">Click OK.</span></span>


