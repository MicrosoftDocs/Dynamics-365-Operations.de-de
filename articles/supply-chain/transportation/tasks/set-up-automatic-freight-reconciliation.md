---
title: Automatische Frachtabstimmung einrichten
description: Dieses Verfahren zeigt, wie Daten für die automatische Frachtabstimmung eingerichtet werden.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 057d1b3a1b5294c75f02f4ed443ae6f525ac6b83
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837613"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="01e73-103">Automatische Frachtabstimmung einrichten</span><span class="sxs-lookup"><span data-stu-id="01e73-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01e73-104">Dieses Verfahren zeigt, wie Daten für die automatische Frachtabstimmung eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="01e73-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="01e73-105">Dies wird normalerweise von einer Lagerortverwaltung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="01e73-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="01e73-106">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="01e73-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="01e73-107">Frachtbrieftyp einrichten</span><span class="sxs-lookup"><span data-stu-id="01e73-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="01e73-108">Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Frachtbrieftyp".</span><span class="sxs-lookup"><span data-stu-id="01e73-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="01e73-109">Der Frachtbrieftyp definiert, wie Frachtbriefe und Spediteursrechnungen abgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01e73-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="01e73-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="01e73-110">Click New.</span></span>
3. <span data-ttu-id="01e73-111">Geben Sie im Feld "Frachtbrieftyp" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="01e73-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="01e73-112">Geben Sie im Feld "Modulklasse" den Typ 'Microsoft.Dynamics.Ax.Tms.dll' ein.</span><span class="sxs-lookup"><span data-stu-id="01e73-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="01e73-113">Dies ist die Standardtransportverwaltungs-Zuordnungsmodul-Codebibliothek.</span><span class="sxs-lookup"><span data-stu-id="01e73-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="01e73-114">Geben Sie im Feld "Modulklasse" den Typ 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer' ein.</span><span class="sxs-lookup"><span data-stu-id="01e73-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="01e73-115">Dies ist die Standardtransportverwaltungs-Zuordnungsmodul-Klasse.</span><span class="sxs-lookup"><span data-stu-id="01e73-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="01e73-116">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="01e73-116">Click New.</span></span>
7. <span data-ttu-id="01e73-117">Wählen Sie im Feld "Beschreibung" den Wert aus, der auf dem Frachtbrief und der Spediteursrechnung übereinstimmen sollten.</span><span class="sxs-lookup"><span data-stu-id="01e73-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="01e73-118">Wählen Sie "Ja" im Feld "Abgleich erforderlich" aus.</span><span class="sxs-lookup"><span data-stu-id="01e73-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="01e73-119">Wenn Sie dieses Feld auf "Ja" festgelegt haben, heißt dies, dass der Wert, der im Feld "Beschreibung" ausgewählt ist, dem Frachtbrief und der Spediteursrechnung entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="01e73-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="01e73-120">Wenn Sie es auf "Nein" festlegen, kann das Feld für einen der Werte leer sein.</span><span class="sxs-lookup"><span data-stu-id="01e73-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="01e73-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="01e73-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="01e73-122">Frachtbrieftypzuweisung einrichten</span><span class="sxs-lookup"><span data-stu-id="01e73-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="01e73-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01e73-123">Close the page.</span></span>
2. <span data-ttu-id="01e73-124">Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Frachtbrieftyp-Zuweisungen".</span><span class="sxs-lookup"><span data-stu-id="01e73-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="01e73-125">Die Frachtbrieftyp-Zuweisung wird verwendet, um anzugeben, welcher Frachtbrieftyp für einen bestimmten Spediteur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01e73-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="01e73-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="01e73-126">Click New.</span></span>
4. <span data-ttu-id="01e73-127">Geben Sie im Feld 'Modus' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01e73-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="01e73-128">Geben Sie im Feld 'Spediteur' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01e73-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="01e73-129">Wählen Sie im Frachtbrieftyp-Feld den Frachtbrieftyp aus, den Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="01e73-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="01e73-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01e73-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="01e73-131">Überwachungsmaster einrichten</span><span class="sxs-lookup"><span data-stu-id="01e73-131">Set up the audit master</span></span>
1. <span data-ttu-id="01e73-132">Wechseln Sie zu "Transportverwaltung" > "Einrichtung" > "Frachtabstimmung" > "Überwachungsmaster".</span><span class="sxs-lookup"><span data-stu-id="01e73-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="01e73-133">Der Überwachungsmaster definiert die Toleranzgrenzen für die automatische Frachtabstimmung.</span><span class="sxs-lookup"><span data-stu-id="01e73-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="01e73-134">Er gibt an, um wie viel die Geldbeträge auf dem Frachtbrief und in der Spediteursrechnung abweichen können, und noch eine Abstimmung zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="01e73-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="01e73-135">Er definiert auch, wie Abweichungen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="01e73-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="01e73-136">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="01e73-136">Click New.</span></span>
3. <span data-ttu-id="01e73-137">Geben Sie im Feld "Überwachungsmasterkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="01e73-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="01e73-138">Wählen Sie im Spediteur-Feld den gleichen Spediteur aus, die Sie eben verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="01e73-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="01e73-139">Wählen Sie im Frachtbrieftyp-Feld den Frachtbrieftyp aus, den Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="01e73-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="01e73-140">Erweitern Sie den Abschnitt "Toleranz".</span><span class="sxs-lookup"><span data-stu-id="01e73-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="01e73-141">Geben Sie im Feld "Minimale Toleranzstufe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="01e73-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="01e73-142">Geben Sie im Feld "Maximale Toleranzstufe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="01e73-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="01e73-143">Erweitern Sie den Abschnitt Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="01e73-143">Expand the Result section.</span></span>
10. <span data-ttu-id="01e73-144">Geben Sie im Feld "Überzahlungs-Ursachencode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01e73-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="01e73-145">Wenn Geldbeträge auf dem Frachtbrief und der Spediteursrechnung abweichen, enthalten die Über- oder Unterzahlungsursachencodes die Konten, für die die Differenz erfasst werden soll, sofern die Differenz innerhalb der Toleranzebenen ist.</span><span class="sxs-lookup"><span data-stu-id="01e73-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="01e73-146">Geben Sie im Feld "Unterzahlungs-Ursachencode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="01e73-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="01e73-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="01e73-147">Close the page.</span></span>

