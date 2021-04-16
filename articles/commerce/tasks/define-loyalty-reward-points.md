---
title: " Treuebelohnungspunkte definieren"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Definieren von Treuebelohnungspunkten.
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7f3b19513bb25d1976d2e4d0e235c347c38ccb4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798464"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="ddacf-103"> Treuebelohnungspunkte definieren</span><span class="sxs-lookup"><span data-stu-id="ddacf-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddacf-104">Diese Prozedur führt Sie Schritt für Schritt durch das Definieren von Treuebelohnungspunkten.</span><span class="sxs-lookup"><span data-stu-id="ddacf-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="ddacf-105">Sie sollten Treuebelohnungspunkte einrichten, bevor Sie ein Treueprogramm einrichten.</span><span class="sxs-lookup"><span data-stu-id="ddacf-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="ddacf-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddacf-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="ddacf-107">Navigieren Sie zu Retail and Commerce > Debitoren > Treue > Treuebelohnungspunkte.</span><span class="sxs-lookup"><span data-stu-id="ddacf-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="ddacf-108">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="ddacf-108">Click New.</span></span>
3. <span data-ttu-id="ddacf-109">Geben Sie im Feld "Belohnungspunktkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddacf-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="ddacf-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddacf-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ddacf-111">Wählen Sie im Belohnungspunkttyp-Feld eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ddacf-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="ddacf-112">Wählen Sie "Menge" aus, wenn die Belohnungspunkte auf die nächste ganze Zahl gerundet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ddacf-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="ddacf-113">Wählen Sie "Betrag" aus, wenn die Belohnungspunkte gemäß Währungsrundungsregeln gerundet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ddacf-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="ddacf-114">Wenn Sie "Menge" auswählen, fahren Sie mit dem nächsten Schritt dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="ddacf-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="ddacf-115">Geben Sie im Feld "Währung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ddacf-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="ddacf-116">Für Betragstypbelohnungs-Punkte haben alle ausgegebenen Punkte die ausgewählte Währung.</span><span class="sxs-lookup"><span data-stu-id="ddacf-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="ddacf-117">Für Mengentyp-Belohnungspunkte gilt dieses Feld nicht – überspringen Sie diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="ddacf-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="ddacf-118">Aktivieren oder deaktivieren Sie das Kontrollkästchen ''Einlösbar".</span><span class="sxs-lookup"><span data-stu-id="ddacf-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="ddacf-119">Geben Sie eine Zahl im Feld "Einlöserang" ein.</span><span class="sxs-lookup"><span data-stu-id="ddacf-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="ddacf-120">Einlöserang wird verwendet, wenn zwei oder mehr einlösbare Belohnungspunkte verwendet werden können, um für Produkte zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="ddacf-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="ddacf-121">Wenn die beiden Belohnungspunkte den gleichen Einlöserang haben, wird der, dessen Punktzahl niedriger sein muss, verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddacf-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="ddacf-122">Geben Sie eine Zahl in das Feld "Wert für Ablaufzeit" ein.</span><span class="sxs-lookup"><span data-stu-id="ddacf-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="ddacf-123">Die Belohnungspunkte laufen die angegebene Anzahl von Tagen, Monaten oder Jahren ab, nachdem die Punkte ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ddacf-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="ddacf-124">Ein Wert von 0 bedeutet, dass die Loyalitätsbelohnungspunkte niemals ablaufen.</span><span class="sxs-lookup"><span data-stu-id="ddacf-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="ddacf-125">Wählen Sie im Feld "Einheit für Ablaufzeit" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ddacf-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="ddacf-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ddacf-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]