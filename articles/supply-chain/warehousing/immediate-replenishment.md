---
title: Sofortige Wiederbeschaffung
description: In diesem Thema wird beschrieben, wie Sie die sofortige Wiederbeschaffung verwenden können, um den Lagerbestand wieder zu ergänzen, wenn eine Lagerplatzdirektive keinen Bestand zuordnen kann.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 006160a3f7eada95ebdcdbf6694ee54be439f349
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835653"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="bbbde-103">Sofortige Wiederbeschaffung</span><span class="sxs-lookup"><span data-stu-id="bbbde-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbbde-104">Mit der sofortigen Wiederbeschaffung können Sie Bestand sofort wiederbeschaffen, nachdem eine Lagerplatzdirektivenposition keinen Bestand zuteilen kann.</span><span class="sxs-lookup"><span data-stu-id="bbbde-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="bbbde-105">Die Wiederbeschaffung basiert auf einer einzelnen Position in den Einstellungen der Lagerplatzdirektive.</span><span class="sxs-lookup"><span data-stu-id="bbbde-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="bbbde-106">Wenn Lagerbestand nicht in der Maßeinheit vorhanden ist, die durch diese Position angegeben ist, erfolgt die Wiederbeschaffung dieser Maßeinheit umgehend.</span><span class="sxs-lookup"><span data-stu-id="bbbde-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="bbbde-107">Die sofortige Wiederbeschaffung bietet eine Alternative zur Methode, bei der die Zuteilung von Bestand auf mehr Positionen in der Lagerplatzdirektive basiert und bei der die Nachfrage am Ende der Zuteilung summiert und in der Maßeinheit wiederbeschafft wird, die durch die letzte Position in der Lagerplatzdirektive angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bbbde-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="bbbde-108">Die Vorteile der Verwendung der sofortigen Wiederbeschaffung bestehen darin, dass die Wiederbeschaffung auf bestimmte Einheiten begrenzt werden kann und die Menge an bestimmte Lagerplätzen gerichtet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bbbde-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="bbbde-109">Geschäftsszenario</span><span class="sxs-lookup"><span data-stu-id="bbbde-109">Business scenario</span></span>

<span data-ttu-id="bbbde-110">Beispielsweise haben Sie einen Lagerort, der separate Entnahmebereiche für die Maßeinheiten „Schachtel” und „Jeder/-e/-es” hat.</span><span class="sxs-lookup"><span data-stu-id="bbbde-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="bbbde-111">Sie möchten den Kommissionierprozess optimieren, indem so viele Schachteln wie möglich entnommen werden und dann die verbleibende Menge, die weniger als eine Schachtel ausmacht, aus dem Bereich „Jeder/-e/-es” entnommen wird.</span><span class="sxs-lookup"><span data-stu-id="bbbde-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="bbbde-112">In diesem Fall können Sie die sofortige Wiederbeschaffung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbbde-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="bbbde-113">In den Lagerplatzdirektiven können Sie die sofortige Wiederbeschaffung für Kartons einrichten, sodass die Bedarfswiederbeschaffung verwendet wird, sobald es einen Mangel an Schachteln gibt, die aus der Bedarfsmenge entnommen werden können.</span><span class="sxs-lookup"><span data-stu-id="bbbde-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="bbbde-114">Hierdurch optimieren Sie den Entnahmeprozess, sodass die Entnahme so viele Schachteln wie möglich umfasst.</span><span class="sxs-lookup"><span data-stu-id="bbbde-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="bbbde-115">Durch die sofortige Wiederbeschaffung wird eine Wiederbeschaffung der Schachteln generiert, und der Bedarf wird nicht übergeben, sodass die Mengen in der Maßeinheit „Jeder/-e/-es” entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="bbbde-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="bbbde-116">Das bedeutet in anderen Worten, dass nur die Mengen, die in der Maßeinheit „Jeder/-e/-es” entnommen werden sollen (das heißt, Mengen, die weniger als eine Schachtel umfassen), aus dem Bereich „Jeder/-e/-es” entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="bbbde-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="bbbde-117">Wenn ein Mangel im Bereich „Schachtel” auftritt, können Sie so viele Schachteln wie möglich aus dem Gesamtbedarf entnehmen.</span><span class="sxs-lookup"><span data-stu-id="bbbde-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="bbbde-118">Die verbleibenden Mengen werden dann aus dem Bereich „Jeder/-e/-es” entnommen.</span><span class="sxs-lookup"><span data-stu-id="bbbde-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="bbbde-119">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="bbbde-119">Where it applies</span></span>

<span data-ttu-id="bbbde-120">Sofortige Wiederbeschaffung wird während der Wellenausführung verwendet, wenn die Zuteilung für eine Lagerplatzdirektivenposition, für die eine Wiederbeschaffungsvorlage festgelegt ist, fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="bbbde-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="bbbde-121">Sofortige Wiederbeschaffung einrichten</span><span class="sxs-lookup"><span data-stu-id="bbbde-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="bbbde-122">Wechseln Sie zu **Lagerortverwaltung** \> **Setup** \> **Lagerplatzdirektiven**, und wählen Sie dann auf der Registerkarte **Positionen** in der Liste **Sofortige Wiederbeschaffungsvorlage** eine Wiederbeschaffungsvorlage für Wellenbedarf aus.</span><span class="sxs-lookup"><span data-stu-id="bbbde-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="bbbde-123">Die Wiederbeschaffungsvorlage wird angewendet, wenn die Lagerplatzdirektivenposition keine dedizierte Maßeinheit zuteilen kann.</span><span class="sxs-lookup"><span data-stu-id="bbbde-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="bbbde-124">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="bbbde-124">Troubleshooting</span></span>

<span data-ttu-id="bbbde-125">Wenn die sofortige Wiederbeschaffung für eine Lagerplatzdirektivenposition ausgewählt ist, aber keine Wiederbeschaffungsarbeit generiert ist, wenn Sie die Bedarfswiederbeschaffungsvorlagen für diese Lagerplatzdirektivenposition verwenden, müssen zwei Hauptursachen untersucht werden:</span><span class="sxs-lookup"><span data-stu-id="bbbde-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="bbbde-126">Stellen Sie sicher, dass die Bedarfswiederbeschaffungsvorlage, die angewendet wird, für die Verwendung der korrekten Lagerplatzvorlagen und Arbeitsvorlagen des Typs **Wiederbeschaffung** eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="bbbde-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="bbbde-127">Stellen Sie sicher, dass es genügend verfügbaren Lagerbestand an den Lagerplätzen gibt, in denen die Bedarfswiederbeschaffungsvorlage nach verfügbarem Lagerbestand für die Wiederbeschaffung sucht.</span><span class="sxs-lookup"><span data-stu-id="bbbde-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]