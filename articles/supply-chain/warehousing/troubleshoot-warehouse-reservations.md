---
title: Fehlerbehebung bei Reservierungen in der Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828105"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="11ef9-103">Fehlerbehebung bei Reservierungen in der Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="11ef9-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11ef9-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerort-Reservierungen in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="11ef9-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="11ef9-105">Informationen zu Themen, die sich auf die Registrierung von Chargen- und Seriennummern beziehen, finden Sie unter [Problembehandlung bei Chargen- und Serienreservierungshierarchien für Lagerorte](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="11ef9-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="11ef9-106">Ich erhalte die folgende Fehlermeldung: „Reservierungen können nicht entfernt werden, da Arbeit erstellt wurde, die sich auf die Reservierungen stützt.“</span><span class="sxs-lookup"><span data-stu-id="11ef9-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="11ef9-107">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="11ef9-107">Issue description</span></span>

<span data-ttu-id="11ef9-108">Sie können die Reservierung von Bestand in einer Zeile nicht aufheben, weil es offene Arbeit gegen die Zeile gibt.</span><span class="sxs-lookup"><span data-stu-id="11ef9-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="11ef9-109">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="11ef9-109">Issue resolution</span></span>

<span data-ttu-id="11ef9-110">Untersuchen Sie, ob offene Packgruppenarbeit existiert, um das Element von einem Packplatz zu einem anderen Lagerplatz zu bringen (z. B. *Baydoor*).</span><span class="sxs-lookup"><span data-stu-id="11ef9-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="11ef9-111">Überprüfen Sie die Datensätze auf den Seiten **Arbeitserstellungsprotokoll** und **Arbeitsdetails**, um festzustellen, was den Bestand physisch reserviert, und schließen Sie dann die Arbeit ab oder löschen Sie sie, um die Reservierung freizugeben.</span><span class="sxs-lookup"><span data-stu-id="11ef9-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="11ef9-112">Ich erhalte die folgende Fehlermeldung: „Bestandsmenge - %1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2.... vorliegen.“</span><span class="sxs-lookup"><span data-stu-id="11ef9-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="11ef9-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="11ef9-113">Issue description</span></span>

<span data-ttu-id="11ef9-114">Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben.</span><span class="sxs-lookup"><span data-stu-id="11ef9-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="11ef9-115">Hier ist der vollständige Text der Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="11ef9-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="11ef9-116">Bestandsmenge -%1 konnte nicht aktualisiert werden, da nicht genügend Bestandstransaktionen für Element %2 mit den Dimensionen Größe=%3, Farbe=%4, Zugänge=%5, Standort=%6, Lagerort=%7, Ort=%8, Bestandsstatus=Verfügbar, Ladungsträger=%9, Chargennummer=%10 für Referenz-ID %11 auf Los-ID %12.</span><span class="sxs-lookup"><span data-stu-id="11ef9-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="11ef9-117">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="11ef9-117">Issue resolution</span></span>

<span data-ttu-id="11ef9-118">Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren.</span><span class="sxs-lookup"><span data-stu-id="11ef9-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="11ef9-119">Diese Transaktionen könnten z. B. Qualitätsaufträge, Bestandssperrsätze oder Ausgabeaufträge öffnen.</span><span class="sxs-lookup"><span data-stu-id="11ef9-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="11ef9-120">Ich erhalte die folgende Fehlermeldung: „Physischer Bestand...kann nicht reserviert werden, da nur 0,00 im Bestand vorhanden sind.“</span><span class="sxs-lookup"><span data-stu-id="11ef9-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="11ef9-121">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="11ef9-121">Issue description</span></span>

<span data-ttu-id="11ef9-122">Dieses Problem kann auftreten, wenn das System eine Bestandsmenge nicht aktualisieren kann, weil es nicht genügend Bestandstransaktionen gibt, die die angegebenen Dimensionen haben.</span><span class="sxs-lookup"><span data-stu-id="11ef9-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="11ef9-123">Hier ist der vollständige Text der Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="11ef9-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="11ef9-124">Physischer Bestand Standort=%1, Lagerort=%2, Bestandsstatus=Verfügbar, Chargennummer=%3, Besitzer=%4: %5 kann nicht reserviert werden, da nur 0,00 im Bestand verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="11ef9-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="11ef9-125">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="11ef9-125">Issue resolution</span></span>

<span data-ttu-id="11ef9-126">Dieses Problem wird wahrscheinlich durch offene Arbeit verursacht.</span><span class="sxs-lookup"><span data-stu-id="11ef9-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="11ef9-127">Beenden Sie entweder die Arbeit oder empfangen Sie ohne Arbeitserstellung.</span><span class="sxs-lookup"><span data-stu-id="11ef9-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="11ef9-128">Stellen Sie sicher, dass keine Bestandstransaktionen die Menge physisch reservieren.</span><span class="sxs-lookup"><span data-stu-id="11ef9-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="11ef9-129">Diese Vorgänge können z. B. offene Qualitätsaufträge, Bestandssperrungen oder Ausgabeaufträge sein.</span><span class="sxs-lookup"><span data-stu-id="11ef9-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
