---
title: Kostenelement-Dimensionselemente einem allgemeinen Satz von Dimensionselementen zuordnen
description: Indem Sie verschiedene Kostenelement-Dimensionsmitglieder einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuordnen, führen Sie Daten in einem gemeinsamen Format zu Analysezwecken zusammen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb752ef853aedbe492dc2880b90d1683c5433a12
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217361"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="a8d44-103">Kostenelement-Dimensionselemente einem allgemeinen Satz von Dimensionselementen zuordnen</span><span class="sxs-lookup"><span data-stu-id="a8d44-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8d44-104">Indem Sie verschiedene Kostenelement-Dimensionsmitglieder einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuordnen, führen Sie Daten in einem gemeinsamen Format zu Analysezwecken zusammen.</span><span class="sxs-lookup"><span data-stu-id="a8d44-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="a8d44-105">Wenn Sie ein Weltkonzern sind und den gesetzlichen Buchhaltungsanforderungen entsprechen, verwenden Sie möglicherweise mehrere Kontenpläne.</span><span class="sxs-lookup"><span data-stu-id="a8d44-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="a8d44-106">Wenn Sie Kostenelement-Dimensionsmitglieder von unterschiedlichen Kontenplänen importieren, können Sie schließlich eine Mischung von Konten erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8d44-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="a8d44-107">Diese Konten können tatsächlich dieselben Eigenschaften haben und Sie möchten möglicherweise mithilfe eines gemeinsamen Formats die Kosten für sie analysisieren und zuteilen.</span><span class="sxs-lookup"><span data-stu-id="a8d44-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="a8d44-108">Kostenelement-Dimensionsmitglieder einem gemeinsamen Format zuordnen</span><span class="sxs-lookup"><span data-stu-id="a8d44-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="a8d44-109">Das folgende Beispiel veranschaulicht, wie Sie als Kostencontroller eine neue Kostenelementdimension in „Kostenrechnung” erstellen können, die Kostenelement-Dimensionsmitglieder aus der US-Kontenplanstruktur und der französischen Kontenplanstruktur einem gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern zuweist.</span><span class="sxs-lookup"><span data-stu-id="a8d44-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="a8d44-110">Sie können dann den gemeinsamen Satz von Kostenelement-Dimensionsmitgliedern verwenden, um Kostendaten aus zwei juristischen Personen in einem Kostenrechnungs-Sachkonto zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="a8d44-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="a8d44-111">Quelle: US-Kontenplan</span><span class="sxs-lookup"><span data-stu-id="a8d44-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="a8d44-112">Quelle: Französischer Kontenplan</span><span class="sxs-lookup"><span data-stu-id="a8d44-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="a8d44-113">Neuer gemeinsamer Satz von Kostenelement-Dimensionsmitgliedern</span><span class="sxs-lookup"><span data-stu-id="a8d44-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a8d44-114">Importierte Kostenelement-Dimensionsmitglieder vom US-Kontenplan</span><span class="sxs-lookup"><span data-stu-id="a8d44-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="a8d44-115">Importierte Kostenelement-Dimensionsmitglieder aus dem französischen Kontenplan</span><span class="sxs-lookup"><span data-stu-id="a8d44-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="a8d44-116">Zuordnung von US-amerikanischen und französischen Kostenelement-Dimensionsmitgliedern zu einem gemeinsamen Satz</span><span class="sxs-lookup"><span data-stu-id="a8d44-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="a8d44-117">5001: Vertrieb</span><span class="sxs-lookup"><span data-stu-id="a8d44-117">5001: Sales</span></span>                                                           | <span data-ttu-id="a8d44-118">5001: Vertrieb und Werbung</span><span class="sxs-lookup"><span data-stu-id="a8d44-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="a8d44-119">5000: Vertrieb und Werbung</span><span class="sxs-lookup"><span data-stu-id="a8d44-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="a8d44-120">5030: Werbung</span><span class="sxs-lookup"><span data-stu-id="a8d44-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="a8d44-121">6390: Bestandseinkauf\*</span><span class="sxs-lookup"><span data-stu-id="a8d44-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="a8d44-122">7000: Reinigungsausgaben</span><span class="sxs-lookup"><span data-stu-id="a8d44-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="a8d44-123">7001: Reinigungsausgaben</span><span class="sxs-lookup"><span data-stu-id="a8d44-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="a8d44-124">7001: Reisekosten</span><span class="sxs-lookup"><span data-stu-id="a8d44-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="a8d44-125">7001: Reisekosten</span><span class="sxs-lookup"><span data-stu-id="a8d44-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="a8d44-126">\*Das französische Kostenelement-Dimensionsmitglied des Bestandskaufs ist nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a8d44-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="a8d44-127">Währungskonvertierung</span><span class="sxs-lookup"><span data-stu-id="a8d44-127">Currency conversion</span></span>
<span data-ttu-id="a8d44-128">Die verschiedenen Kontenpläne, die Sie verwenden, sind möglicherweise für die Verwendung verschiedener Währungen eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a8d44-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="a8d44-129">In diesem Fall sollten Sie sicherstellen, dass Sie eine Währungsumrechnung angeben, sodass Kostendaten mithilfe der korrekten Währung verarbeitet werden, wie im Kostenrechnungs-Sachkonto definiert, wo die Kostenelement-Dimensionsmitglieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8d44-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="a8d44-130">Wenn im vorherigen Beispiel US-Dollar (USD) im Kostenrechnungs-Sachkonto verwendet werden, müssen Sie eine Währungsumrechnung von USD zu Euro (EUR) erstellen, um Buchungen für die zugeordneten Kostenelement-Dimensionsmitglieder zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a8d44-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="a8d44-131">Zuordnungen jederzeit aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a8d44-131">Update mappings at any time</span></span>
<span data-ttu-id="a8d44-132">Sie können die Zuordnungsdefinitionen für eine Kostenelementdimension jederzeit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a8d44-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="a8d44-133">Da Zuordnungen nicht ab einem bestimmten Datum gültig sind, werden Änderung das nächste Mal, wenn Sie Kostenbuchungen verarbeiten oder Kostenberechnungen ausführen, angewendet.</span><span class="sxs-lookup"><span data-stu-id="a8d44-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]