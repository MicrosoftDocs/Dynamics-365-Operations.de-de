---
title: Nach Kreditoren suchen
description: Informieren Sie, wie nach Kreditoren anhand bestimmter Kriterien sucht.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf93307600aac6fa6e45524092ec4811742010e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244038"
---
# <a name="search-for-vendors"></a><span data-ttu-id="1c061-103">Nach Kreditoren suchen</span><span class="sxs-lookup"><span data-stu-id="1c061-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c061-104">Informieren Sie, wie nach Kreditoren anhand bestimmter Kriterien sucht.</span><span class="sxs-lookup"><span data-stu-id="1c061-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="1c061-105">In diesem Beispiel wird Ihnen angegeben, wie nach Kreditoren findet, die für eine bestimmte Beschaffungskategorie genehmigt werden und deren primäre Adresse sich in einem bestimmten Land hat.</span><span class="sxs-lookup"><span data-stu-id="1c061-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="1c061-106">Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c061-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="1c061-107">Diese Aufgabe ist in der Regel von einem Beschaffungsspezialisten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c061-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="1c061-108">Klicken Sie auf "Beschaffung" > "Kreditoren" > "Kreditorensuche".</span><span class="sxs-lookup"><span data-stu-id="1c061-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="1c061-109">Klicken Sie im Plussymbol, um die Beschaffungskategorie-Auswahlseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1c061-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="1c061-110">Wählen Sie in der Strukturdarstellung "CORP-BESCHAFFUNGSKATEGORIEN \ BÜROMASCHINEN" aus.</span><span class="sxs-lookup"><span data-stu-id="1c061-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="1c061-111">Wenn Sie die Prozedur wie ein Aufgabenhandbuch ausführen, müssen Sie möglicherweise auf die Schaltfläche "Entsperren" klicken, bevor Sie den korrekten Knoten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="1c061-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="1c061-112">Wenn Sie nicht USMF verwenden, wählen Sie eine der Kategorien aus, die Sie haben.</span><span class="sxs-lookup"><span data-stu-id="1c061-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="1c061-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c061-113">Click Add.</span></span>
    * <span data-ttu-id="1c061-114">Es ist möglich, mehrere Kategorie hier auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="1c061-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="1c061-115">Wenn Sie das tun, sucht die Suche alle Kreditoren, die für mindestens eine der Kategorien genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="1c061-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="1c061-116">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c061-116">Click OK.</span></span>
6. <span data-ttu-id="1c061-117">Geben Sie im Feld "Land/Region" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1c061-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="1c061-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c061-118">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]