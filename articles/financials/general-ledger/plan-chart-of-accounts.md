---
title: Ihren Kontenplan planen
description: "Dieser Artikel enthält Informationen, die Ihnen helfen, Kontenpläne für Ihre Organisation zu planen."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="118a3-103">Ihren Kontenplan planen</span><span class="sxs-lookup"><span data-stu-id="118a3-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="118a3-104">Dieser Artikel enthält Informationen, die Ihnen helfen, Kontenpläne für Ihre Organisation zu planen.</span><span class="sxs-lookup"><span data-stu-id="118a3-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="118a3-105">Um Finanzdaten in einer Organisation zu verfolgen und zu verwalten, können Sie einen Kontenplan einrichten.</span><span class="sxs-lookup"><span data-stu-id="118a3-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="118a3-106">Ein Kontenplan ist eine Reihe von Konten, die ein finanziellen Rahmen definieren.</span><span class="sxs-lookup"><span data-stu-id="118a3-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="118a3-107">Sie können Segmente hinzufügen, so genannte Finanzdimensionen, damit die Buchungen in diesen Konten noch weiter verfolgt werden können.</span><span class="sxs-lookup"><span data-stu-id="118a3-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="118a3-108">Beispielsweise kann ein Ausgabenkonto Finanzdimensionen mit der Bezeichnung "Abteilung", "Kostenstelle" und "Kostenträger" enthalten.</span><span class="sxs-lookup"><span data-stu-id="118a3-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="118a3-109">Mit benutzerdefinierten Regeln (Kontostrukturen und erweiterte Regeln genannt) wird bestimmt, wie diese Finanzdimensionen den Hauptkonten und anderen Finanzdimensionen angefügt werden und wie Buchungen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="118a3-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="118a3-110">Der Kontenplan ist eine strukturierte Liste der Hauptbuchkonten einer juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="118a3-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="118a3-111">Diese Liste wird verwendet, um Finanzberichte für Behörden und Eigentümer vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="118a3-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="118a3-112">Die Konten sind nach Kontenarten gruppiert und wiederum in übergeordneten Kategorien zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="118a3-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="118a3-113">Auf der allgemeinsten Ebene sind die Konten in Umsatzerlöse und Kosten (Betriebskonten) sowie Aktiva und Passiva (Bilanzkonten) unterteilt.</span><span class="sxs-lookup"><span data-stu-id="118a3-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="118a3-114">Ein Kontenplan kann freigegeben und von jeder juristischen Person in einer Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="118a3-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="118a3-115">Der Kontenplan für die juristischen Person wird auf der Seite **Sachkonto** definiert.</span><span class="sxs-lookup"><span data-stu-id="118a3-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="118a3-116">Hier einige der Faktoren, die Sie bei der Strukturierung des Kontenplans für Ihre Organisation berücksichtigen müssen:</span><span class="sxs-lookup"><span data-stu-id="118a3-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="118a3-117">Die Meldeanforderungen für das Land bzw. die Region, in der die Organisation ihren Sitz hat.</span><span class="sxs-lookup"><span data-stu-id="118a3-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="118a3-118">Die Meldeanforderungen für Ihre juristische Person</span><span class="sxs-lookup"><span data-stu-id="118a3-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="118a3-119">Der erforderliche Spezifikationsgrad, sowohl für externe Organisationen als auch für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="118a3-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="118a3-120">Erstellen Sie den Kontenplan auf der Seite **Kontenplan**.</span><span class="sxs-lookup"><span data-stu-id="118a3-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="118a3-121">Hauptkonten können über die Seite **Kontenplan** oder aus der Seite **Hauptkonten** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="118a3-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="118a3-122">Ihre Hauptkonten dürfen keine Sonderzeichen verwenden, die als Trennzeichen für Kontenplan verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="118a3-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="118a3-123">Wenn Sie ein Sonderzeichen haben, das das gleiche wie das Trennzeichen für Kontenplan ist, könnte Instabilität die Folge sein, oder dass Sie immer nachschlagen oder das Flyout nutzen müssen, wenn Sie Kombinationen aus Konten und Dimensionen eingeben.</span><span class="sxs-lookup"><span data-stu-id="118a3-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="118a3-124">Weitere Informationen finden Sie unter [Erstellen eines Hauptkontos](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="118a3-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="118a3-125">Es wird empfohlen, die Hauptkonten mit Hauptkontokategorien verknüpfen, sodass Sie die standardmäßige Finanzberichte nutzen können, ohne Änderungen vornehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="118a3-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="118a3-126">Daher können Sie Berichte schneller und einfacher entwerfen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="118a3-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="118a3-127">Verwenden Sie die Seite **Kontostrukturen konfigurieren**, um Kontostrukturen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="118a3-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="118a3-128">Kontostrukturen definieren zulässige Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="118a3-128">Account structures define valid combinations.</span></span> <span data-ttu-id="118a3-129">Diese Kombinationen bilden zusammen mit den Hauptkonten einen Kontenplan.</span><span class="sxs-lookup"><span data-stu-id="118a3-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="118a3-130">Weitere Informationen zu Kontostrukturen finden Sie unter [Kontostrukturen erstellen](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="118a3-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="118a3-131">**Juristische Person überschreibt**</span><span class="sxs-lookup"><span data-stu-id="118a3-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="118a3-132">Nicht alle Hauptkonten sind für alle juristischen Personen gültig und manche sind möglicherweise nur für eine bestimmte Zeitperiode relevant.</span><span class="sxs-lookup"><span data-stu-id="118a3-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="118a3-133">In diesem kann der Abschnitt "Überschreibungen der juristischen Person" dazu verwendet werden, um festzulegen, für welche Unternehmen das Hauptkonto ausgesetzt werden soll, wer der Besitzer ist und die Zeitperiode, während der die Dimension aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="118a3-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="118a3-134">Die Überschreibungen auf der freigegebenen Ebene können nicht einschränkender als die Überschreibungen auf der Ebene der juristischen Person sein.</span><span class="sxs-lookup"><span data-stu-id="118a3-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="118a3-135">Weitere Informationen finden Sie unter folgenden Themen: [Finanzdimensionen](financial-dimensions.md)
[Erstellen und Zuweisen von erweiterten Regelstrukturen](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="118a3-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




