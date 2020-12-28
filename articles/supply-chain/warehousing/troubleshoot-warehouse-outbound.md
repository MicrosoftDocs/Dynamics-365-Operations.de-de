---
title: Fehlerbehebung bei ausgehenden Lagerort-Vorgängen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit ausgehenden Lagerort-Vorgängen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
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
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645448"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="1f227-103">Fehlerbehebung bei ausgehenden Lagerort-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="1f227-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f227-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit ausgehenden Lagerort-Vorgängen in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="1f227-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="1f227-105">Ich erhalte die folgende Fehlermeldung: „Verkaufsauftrag konnte nicht freigegeben werden.“</span><span class="sxs-lookup"><span data-stu-id="1f227-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f227-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="1f227-106">Issue description</span></span>

<span data-ttu-id="1f227-107">Dieses Problem kann aus mehreren Gründen auftreten.</span><span class="sxs-lookup"><span data-stu-id="1f227-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="1f227-108">Zum Beispiel befindet sich der Auftrag in der Kreditverwaltung und es können keine Sendungen erstellt werden, bis eine gültige Postadresse für alle Verkaufszeilen, die mit einem Verkaufsauftrag verbunden sind, eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1f227-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="1f227-109">Oder es gibt eine Auftragssperre, die behoben werden muss, bevor der Auftrag für das Lagerort freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f227-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="1f227-110">Dieser Halt kann auftragsspezifisch sein oder sich auf das Kundenkonto beziehen.</span><span class="sxs-lookup"><span data-stu-id="1f227-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1f227-111">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="1f227-111">Issue resolution</span></span>

<span data-ttu-id="1f227-112">Fügen Sie die Adresse auf dem Auftrag und den Auftragszeilen hinzu oder aktualisieren Sie sie, und geben Sie den Auftrag dann für das Lager frei.</span><span class="sxs-lookup"><span data-stu-id="1f227-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="1f227-113">Aufträge können nur dann für das Lagerort freigegeben werden, wenn sie eine gültige Lieferadresse haben (gemäß dem Adressformat, das im Modul **Organisationsverwaltung** eingerichtet wurde).</span><span class="sxs-lookup"><span data-stu-id="1f227-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="1f227-114">Untersuchen Sie den Auftragsstopp und beheben Sie die Probleme.</span><span class="sxs-lookup"><span data-stu-id="1f227-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="1f227-115">Entfernen Sie dann die Sperrung des Auftrags oder des Kunden und geben Sie den Auftrag für das Lagerort frei.</span><span class="sxs-lookup"><span data-stu-id="1f227-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="1f227-116">Ich erhalte die folgende Meldung: „Die Lieferung für Ladung 1% wurde bestätigt.“</span><span class="sxs-lookup"><span data-stu-id="1f227-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="1f227-117">Es werden jedoch keine Zeilen gebucht.</span><span class="sxs-lookup"><span data-stu-id="1f227-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f227-118">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="1f227-118">Issue description</span></span>

<span data-ttu-id="1f227-119">Eine Sendung zu einer Ladung wurde bestätigt, aber es erfolgte keine weitere Buchung.</span><span class="sxs-lookup"><span data-stu-id="1f227-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1f227-120">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="1f227-120">Issue resolution</span></span>

<span data-ttu-id="1f227-121">Die Sendungsbestätigung hat keinen Einfluss auf die Buchung.</span><span class="sxs-lookup"><span data-stu-id="1f227-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="1f227-122">Sie aktualisiert nur den Status der Sendung und der Ladung.</span><span class="sxs-lookup"><span data-stu-id="1f227-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="1f227-123">Die Verbuchung muss in einem separaten Prozess erfolgen.</span><span class="sxs-lookup"><span data-stu-id="1f227-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="1f227-124">Ich erhalte die folgende Fehlermeldung: „Die Direktlieferung kann für Lagerort 1% nicht verarbeitet werden, da die Lagerortverwaltung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1f227-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="1f227-125">Bitte geben Sie einen anderen Lagerort an, für das die Lagerortverwaltung nicht aktiviert ist.“</span><span class="sxs-lookup"><span data-stu-id="1f227-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f227-126">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="1f227-126">Issue description</span></span>

<span data-ttu-id="1f227-127">Ein Element wird einer Verkaufszeile zur Direktlieferung aus einem Lagerort hinzugefügt, der für die Lagerortverwaltung (WMS) aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1f227-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="1f227-128">Sie erhalten diese Fehlermeldung, wenn die Verkaufszeile aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1f227-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="1f227-129">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="1f227-129">Issue resolution</span></span>

<span data-ttu-id="1f227-130">Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="1f227-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="1f227-131">Derzeit unterstützt WMS die direkte Lieferung nicht.</span><span class="sxs-lookup"><span data-stu-id="1f227-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="1f227-132">Um die direkte Lieferung zu verwenden, müssen Sie daher ein Element und ein Lagerort auswählen, die nicht zu WMS gehören.</span><span class="sxs-lookup"><span data-stu-id="1f227-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
