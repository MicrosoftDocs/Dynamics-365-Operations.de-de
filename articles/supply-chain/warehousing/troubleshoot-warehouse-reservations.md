---
title: Fehlerbehebung bei Reservierungen in der Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645119"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="208e8-103">Fehlerbehebung bei Reservierungen in der Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="208e8-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="208e8-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="208e8-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="208e8-105">Ich erhalte die folgende Fehlermeldung: „Reservierungen können nicht entfernt werden, da Arbeit erstellt wurde, die sich auf die Reservierungen stützt.“</span><span class="sxs-lookup"><span data-stu-id="208e8-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="208e8-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="208e8-106">Issue description</span></span>

<span data-ttu-id="208e8-107">Sie können die Reservierung von Bestand in einer Zeile nicht aufheben, weil es offene Arbeit gegen die Zeile gibt.</span><span class="sxs-lookup"><span data-stu-id="208e8-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="208e8-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="208e8-108">Issue resolution</span></span>

<span data-ttu-id="208e8-109">Untersuchen Sie, ob offene Packgruppenarbeit existiert, um das Element von einem Packplatz zu einem anderen Lagerplatz zu bringen (z. B. *Baydoor*).</span><span class="sxs-lookup"><span data-stu-id="208e8-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="208e8-110">Überprüfen Sie die Datensätze auf den Seiten **Arbeitserstellungsprotokoll** und **Arbeitsdetails**, um festzustellen, was den Bestand physisch reserviert, und schließen Sie dann die Arbeit ab oder löschen Sie sie, um die Reservierung freizugeben.</span><span class="sxs-lookup"><span data-stu-id="208e8-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="208e8-111">Ich erhalte die folgende Fehlermeldung: „Bestandsmenge - %1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2.... vorliegen.“</span><span class="sxs-lookup"><span data-stu-id="208e8-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="208e8-112">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="208e8-112">Issue description</span></span>

<span data-ttu-id="208e8-113">Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben.</span><span class="sxs-lookup"><span data-stu-id="208e8-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="208e8-114">Hier ist der vollständige Text der Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="208e8-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="208e8-115">Bestandsmenge -%1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2 mit den Dimensionen Größe=%3, Farbe=%4, Zugänge=%5, Standort=%6, Lagerort=%7, Ort=%8, Bestandsstatus=Verfügbar, Ladungsträger=%9, Chargennummer=%10 für Referenz-ID %11 auf Los-ID %12.</span><span class="sxs-lookup"><span data-stu-id="208e8-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="208e8-116">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="208e8-116">Issue resolution</span></span>

<span data-ttu-id="208e8-117">Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren.</span><span class="sxs-lookup"><span data-stu-id="208e8-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="208e8-118">Diese Transaktionen könnten z. B. Qualitätsaufträge, Bestandssperrsätze oder Ausgabeaufträge öffnen.</span><span class="sxs-lookup"><span data-stu-id="208e8-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="208e8-119">Ich erhalte die folgende Fehlermeldung: „Physischer Bestand...kann nicht reserviert werden, da nur 0,00 im Bestand vorhanden sind.“</span><span class="sxs-lookup"><span data-stu-id="208e8-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="208e8-120">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="208e8-120">Issue description</span></span>

<span data-ttu-id="208e8-121">Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben.</span><span class="sxs-lookup"><span data-stu-id="208e8-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="208e8-122">Hier ist der vollständige Text der Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="208e8-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="208e8-123">Physischer Bestand Standort=%1, Lagerort=%2, Bestandsstatus=Verfügbar, Chargennummer=%3, Besitzer=%4: %5 kann nicht reserviert werden, da nur 0,00 im Bestand verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="208e8-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="208e8-124">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="208e8-124">Issue resolution</span></span>

<span data-ttu-id="208e8-125">Dieses Problem wird wahrscheinlich durch offene Arbeit verursacht.</span><span class="sxs-lookup"><span data-stu-id="208e8-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="208e8-126">Beenden Sie entweder die Arbeit oder empfangen Sie ohne Arbeitserstellung.</span><span class="sxs-lookup"><span data-stu-id="208e8-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="208e8-127">Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren.</span><span class="sxs-lookup"><span data-stu-id="208e8-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="208e8-128">Diese Vorgänge können z. B. offene Qualitätsaufträge, Bestandssperrungen oder Ausgabeaufträge sein.</span><span class="sxs-lookup"><span data-stu-id="208e8-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="208e8-129">Ich erhalte die folgende Fehlermeldung: „Um einer Welle zugewiesen zu werden, müssen Ladungszeilen die Dimensionen oberhalb des Lagerplatzes angeben.</span><span class="sxs-lookup"><span data-stu-id="208e8-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="208e8-130">Um diese Dimensionen zuzuweisen, reservieren Sie und erstellen Sie die Ladelinie neu.“</span><span class="sxs-lookup"><span data-stu-id="208e8-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="208e8-131">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="208e8-131">Issue description</span></span>

<span data-ttu-id="208e8-132">Wenn Sie ein Element verwenden, das eine Reservierungshierarchie „Charge oben“ hat (mit der Dimension **Chargennummer**, die *über* der Dimension **Lagerplatz** platziert ist), funktioniert der Befehl **Freigeben an Lagerort** auf der Seite **Ladungsplanung Workbench** für eine Teilmenge nicht.</span><span class="sxs-lookup"><span data-stu-id="208e8-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="208e8-133">Sie erhalten diese Fehlermeldung, und es wird keine Arbeit für die Teilmenge erstellt.</span><span class="sxs-lookup"><span data-stu-id="208e8-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="208e8-134">Wenn Sie jedoch ein Element verwenden, das eine Reservierungshierarchie „Charge unten“ hat (mit der Dimension **Chargennummer**, die *unter* der Dimension **Lagerplatz** platziert ist), können Sie auf der Seite **Ladungsplanung Werkbank** für eine Teilmenge eine Ladung freigeben.</span><span class="sxs-lookup"><span data-stu-id="208e8-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="208e8-135">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="208e8-135">Issue resolution</span></span>

<span data-ttu-id="208e8-136">Dieses Verhalten ist beabsichtigt.</span><span class="sxs-lookup"><span data-stu-id="208e8-136">This behavior is by design.</span></span> <span data-ttu-id="208e8-137">Wenn Sie in der Reservierungshierarchie eine Dimension oberhalb der **Ort**-Dimension einlagern, muss diese vor der Freigabe zum Lagerort angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="208e8-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="208e8-138">Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion bei Freigaben an das Lagerort aus der Ladeplanungs-Workbench handelt.</span><span class="sxs-lookup"><span data-stu-id="208e8-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="208e8-139">Teilmengen können nicht freigegeben werden, wenn eine oder mehrere Dimensionen über **Lagerplatz** nicht angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="208e8-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="208e8-140">Weitere Informationen finden Sie unter [Flexible Richtlinie für die Reservierung von Dimensionen auf Lagerebene](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="208e8-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
