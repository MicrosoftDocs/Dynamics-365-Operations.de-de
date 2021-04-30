---
title: Finanzdimensionssätze
description: In diesem Thema werden Finanzdimensionssätze beschrieben und einige Tipps zur Optimierung ihrer Verwendung bereitgestellt.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864411"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="fa204-103">Finanzdimensionssätze</span><span class="sxs-lookup"><span data-stu-id="fa204-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa204-104">In diesem Thema werden Finanzdimensionssätze beschrieben und einige Tipps zur Optimierung ihrer Verwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fa204-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="fa204-105">Ein Dimensionssatz ist eine sortierte Liste von Finanzdimensionen, mit denen Hauptbuchdaten auf benutzerdefinierte Weise zusammengefasst werden können.</span><span class="sxs-lookup"><span data-stu-id="fa204-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="fa204-106">Eine primäre Verwendung von Dimensionssätzen besteht darin, eine Zwischenbilanz zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fa204-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="fa204-107">Der einzige Standarddimensionssatz ist der Dimensionssatz, der nur das Hauptkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="fa204-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="fa204-108">Sie verwenden die Seite **Finanzdimensionssätze** zum Erstellen und Verwalten von Finanzdimensionssätzen.</span><span class="sxs-lookup"><span data-stu-id="fa204-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="fa204-109">Dimensionssatzsalden</span><span class="sxs-lookup"><span data-stu-id="fa204-109">Dimension set balances</span></span>

<span data-ttu-id="fa204-110">Ein Dimensionssatz kann Salden haben, die auf seinen Finanzdimensionen basieren.</span><span class="sxs-lookup"><span data-stu-id="fa204-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="fa204-111">Die Salden befinden sich im Hauptbuch und basieren auf der Definition des Dimensionssatzes.</span><span class="sxs-lookup"><span data-stu-id="fa204-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="fa204-112">Die Salden werden aus den Hauptbuchdaten zusammengefasst, um die Leistung beim Abrufen zu verbessern (z. B. wenn eine Zwischenbilanz erstellt wird).</span><span class="sxs-lookup"><span data-stu-id="fa204-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="fa204-113">Salden erstellen</span><span class="sxs-lookup"><span data-stu-id="fa204-113">Create balances</span></span>

<span data-ttu-id="fa204-114">Verwenden Sie die Schaltfläche **Salden erstellen**, um die Salden für einen Dimensionssatz zu initialisieren, für den derzeit keine Salden vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fa204-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="fa204-115">Es wird empfohlen, die Anzahl der Dimensionssätze mit Salden zu begrenzen, da Saldenaktualisierungen alle Buchungsaktivitäten des Hauptbuchs betreffen.</span><span class="sxs-lookup"><span data-stu-id="fa204-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="fa204-116">Salden aktualisieren</span><span class="sxs-lookup"><span data-stu-id="fa204-116">Update balances</span></span>

<span data-ttu-id="fa204-117">Verwenden Sie die Schaltfläche **Salden aktualisieren**, um die letzte Buchungsaktivität des Hauptbuchs in die Salden aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="fa204-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="fa204-118">Saldenaktualisierungen sind leichte Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="fa204-118">Balance updates are light operations.</span></span> <span data-ttu-id="fa204-119">Sie dürfen nur die Buchungsaktivität des Hauptbuchs verarbeiten, die seit der letzten Aktualisierung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fa204-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="fa204-120">Die Anzeige der Zwischenbilanz erzwingt eine Aktualisierung, um sicherzustellen, dass die angezeigten Salden aktuell sind.</span><span class="sxs-lookup"><span data-stu-id="fa204-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="fa204-121">Verwenden Sie einen wiederkehrenden Stapelverarbeitungsauftrag, damit die Aktualisierungen Ihrer am häufigsten verwendeten Dimensionssätze schnell erfolgen.</span><span class="sxs-lookup"><span data-stu-id="fa204-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="fa204-122">Auf diese Weise können Sie die Wartezeit für Zwischenbilanzbenutzer minimieren.</span><span class="sxs-lookup"><span data-stu-id="fa204-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="fa204-123">Salden neu erstellen</span><span class="sxs-lookup"><span data-stu-id="fa204-123">Rebuild balances</span></span>

<span data-ttu-id="fa204-124">Verwenden Sie die Schaltfläche **Salden neu erstellen**, um die Salden von Grund auf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa204-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="fa204-125">Auf diese Weise stellen Sie sicher, dass sie mit den Daten im Hauptbuch übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fa204-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="fa204-126">Die Wiedererstellung der Salden ist sehr aufwändig und sollte normalerweise nicht erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="fa204-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="fa204-127">Wenn Sie ein Szenario haben, in dem regelmäßig Salden neu erstellt werden müssen, empfehlen wir Ihnen, sich an den Kundensupport zu wenden.</span><span class="sxs-lookup"><span data-stu-id="fa204-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="fa204-128">Mithilfe des Kundensupports können Sie feststellen, warum Salden nicht mit den Daten im Hauptbuch übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fa204-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="fa204-129">Salden leeren</span><span class="sxs-lookup"><span data-stu-id="fa204-129">Clear balances</span></span>

<span data-ttu-id="fa204-130">Verwenden Sie die Schaltfläche **Salden leeren**, um die Salden zu entfernen und weitere Aktualisierungen zu stoppen.</span><span class="sxs-lookup"><span data-stu-id="fa204-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="fa204-131">Der Dimensionssatz hat keine Auswirkungen mehr auf die Buchungsaktivitäten des Hauptbuchs.</span><span class="sxs-lookup"><span data-stu-id="fa204-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="fa204-132">Weitere Informationen finden Sie unter [Finanzdimensionen](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="fa204-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
