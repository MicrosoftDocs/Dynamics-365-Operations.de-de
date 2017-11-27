---
title: "Betrag der Rundung für Abschreibungsberechnungen"
description: "Dieser Artikel erläutert das Feld \"Rundungsart Abschreibung\", das Sie im Wertmodell und auf den Einstellungsseiten des Abschreibungsbuchs finden."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="4fd35-103">Betrag der Rundung für Abschreibungsberechnungen</span><span class="sxs-lookup"><span data-stu-id="4fd35-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4fd35-104">Dieser Artikel erläutert das Feld "Rundungsart Abschreibung", das Sie im Wertmodell und auf den Einstellungsseiten des Abschreibungsbuchs finden.</span><span class="sxs-lookup"><span data-stu-id="4fd35-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="4fd35-105">Rundungsart Abschreibungbeträge werden für jedes Buch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fd35-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="4fd35-106">Gerundete Abschreibungsbeträge werden im Anlagenabschreibungsprofil, das die zukünftige Abschreibung und den Wert der Anlage anzeigt, sowie in den Abschreibungsvorschlägen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4fd35-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="4fd35-107">Den niedrigsten Abschreibungsbetrag eingeben, der für dieses Buch zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="4fd35-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="4fd35-108">Unabhängig von der eingerichteten Rundung wird der Abschreibungsbetrag im letzten Abschreibungszeitraum nicht gerundet.</span><span class="sxs-lookup"><span data-stu-id="4fd35-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="4fd35-109">Am Ende des letzten Abschreibungszeitraums muss der Wert der Anlage 0 (Null) oder der Schrottwert sein, wenn Schrottwert verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fd35-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="4fd35-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4fd35-110">Example</span></span>

<span data-ttu-id="4fd35-111">Die Abschreibung ohne Rundung beträgt 2.444,44.</span><span class="sxs-lookup"><span data-stu-id="4fd35-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="4fd35-112">Wie die folgende Tabelle zeigt, sind die vorgeschlagenen Beträge unterschiedlich, abhängig davon, wie die Rundung eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="4fd35-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="4fd35-113">Rundungsmethode</span><span class="sxs-lookup"><span data-stu-id="4fd35-113">Rounding method</span></span> | <span data-ttu-id="4fd35-114">Abschreibungsbetrag</span><span class="sxs-lookup"><span data-stu-id="4fd35-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="4fd35-115">Rundung 0,1</span><span class="sxs-lookup"><span data-stu-id="4fd35-115">Rounding 0.1</span></span>    | <span data-ttu-id="4fd35-116">2.444,40</span><span class="sxs-lookup"><span data-stu-id="4fd35-116">2,444.40</span></span>            |
| <span data-ttu-id="4fd35-117">Rundung 1,00</span><span class="sxs-lookup"><span data-stu-id="4fd35-117">Rounding 1.00</span></span>   | <span data-ttu-id="4fd35-118">2.444,00</span><span class="sxs-lookup"><span data-stu-id="4fd35-118">2,444.00</span></span>            |
| <span data-ttu-id="4fd35-119">Rundung 10,00</span><span class="sxs-lookup"><span data-stu-id="4fd35-119">Rounding 10.00</span></span>  | <span data-ttu-id="4fd35-120">2.440,00</span><span class="sxs-lookup"><span data-stu-id="4fd35-120">2,440.00</span></span>            |
| <span data-ttu-id="4fd35-121">Rundung 100,00</span><span class="sxs-lookup"><span data-stu-id="4fd35-121">Rounding 100.00</span></span> | <span data-ttu-id="4fd35-122">2.400,00</span><span class="sxs-lookup"><span data-stu-id="4fd35-122">2,400.00</span></span>            |






