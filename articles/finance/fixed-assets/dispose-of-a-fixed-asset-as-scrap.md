---
title: Anlage als Ausschuss veräußern
description: Das Thema beschreibt den Prozess des Beseitigens von Transaktionen für eine Anlage, die als Ausschuss veräußert wurde.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 42eaa3df5ab09278ed96506d17e1b42d4fc2a9e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570263"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="03cd7-103">Anlage als Ausschuss veräußern</span><span class="sxs-lookup"><span data-stu-id="03cd7-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03cd7-104">Das Thema beschreibt den Prozess des Beseitigens von Transaktionen für eine Anlage, die als Ausschuss veräußert wurde.</span><span class="sxs-lookup"><span data-stu-id="03cd7-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="03cd7-105">Die Transaktionsarten, die beseitigt werden können, enthalten die Anschaffung einer Anlage und kumulierte Abschreibungsbuchungen sowie andere Anlagentransaktionen.</span><span class="sxs-lookup"><span data-stu-id="03cd7-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="03cd7-106">Die Beseitigung dieser Transaktionen wirkt sich auf Bilanzkonten aus, beispielsweise Anschaffungsänderungs-, Abschreibungsänderungs-, Neubewertungs-, Höherbewertungs- und Niedrigerbewertungskonten.</span><span class="sxs-lookup"><span data-stu-id="03cd7-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="03cd7-107">Buchung</span><span class="sxs-lookup"><span data-stu-id="03cd7-107">Transaction</span></span>                                         | <span data-ttu-id="03cd7-108">Soll (S)</span><span class="sxs-lookup"><span data-stu-id="03cd7-108">Debit (Dr.)</span></span> | <span data-ttu-id="03cd7-109">Haben (H)</span><span class="sxs-lookup"><span data-stu-id="03cd7-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="03cd7-110">Soll – kumulierte Abschreibung</span><span class="sxs-lookup"><span data-stu-id="03cd7-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="03cd7-111">X</span><span class="sxs-lookup"><span data-stu-id="03cd7-111">X</span></span>           |              |
| <span data-ttu-id="03cd7-112">H – Anlagengewinn/-verlust</span><span class="sxs-lookup"><span data-stu-id="03cd7-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="03cd7-113">X</span><span class="sxs-lookup"><span data-stu-id="03cd7-113">X</span></span>            |
| <span data-ttu-id="03cd7-114">S – Anlagengewinn/-verlust</span><span class="sxs-lookup"><span data-stu-id="03cd7-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="03cd7-115">X</span><span class="sxs-lookup"><span data-stu-id="03cd7-115">X</span></span>           |              |
| <span data-ttu-id="03cd7-116">H – Konto für Anlagenerwerb</span><span class="sxs-lookup"><span data-stu-id="03cd7-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="03cd7-117">X</span><span class="sxs-lookup"><span data-stu-id="03cd7-117">X</span></span>            |
| <span data-ttu-id="03cd7-118">S – Anlagengewinn/-verlust (Nettobuchwert \[NBW\])</span><span class="sxs-lookup"><span data-stu-id="03cd7-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="03cd7-119">X</span><span class="sxs-lookup"><span data-stu-id="03cd7-119">X</span></span>           |              |
| <span data-ttu-id="03cd7-120">H – Anlagengewinn/-verlust (NBW)</span><span class="sxs-lookup"><span data-stu-id="03cd7-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="03cd7-121">X</span><span class="sxs-lookup"><span data-stu-id="03cd7-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="03cd7-122">Wir empfehlen Ihnen, eng mit dem Leiter der Finanzabteilung (CFO) oder Controller Ihres Unternehmens zusammenzuarbeiten, um die korrekten Konten zu ermitteln, die für die einzelnen Transaktionstypen verwendet werden sollten, und sicherzustellen, dass bei dem Veräußerungsprozess und den dabei generierten Transaktionen diese Konten korrekt aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="03cd7-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="03cd7-123">Bevor eine Anlage als Ausschuss veräußert werden soll, müssen Sie Sachkonten erstellen, die mit dem Anschaffungswert der Anlage, der Abschreibung für das aktuelle Jahr, der Abschreibung für vorherige Jahre und dem NBW der Anlage verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="03cd7-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="03cd7-124">Die Anlagentransaktionsarten werden auf der Seite **Anlagenbuchungsprofile** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03cd7-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="03cd7-125">Gehen Sie zu **Anlagen \> Einstellungen \> Anlagenbuchungsprofile** und wählen Sie dann im Inforegister **Veräußerung** die Option **Ausschuss** im Feld über dem Raster aus.</span><span class="sxs-lookup"><span data-stu-id="03cd7-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="03cd7-126">Die folgende Abbildung zeigt die Liste der Anlagentransaktionsarten auf der Seite **Anlagenbuchungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="03cd7-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="03cd7-127">[![Veräußern einer Anlage als Ausschuss, Abb. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="03cd7-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="03cd7-128">Im folgenden Beispiel wurde eine Anlage am 1. Januar 2018 erworben und sie wird am 31. März 2019 zu Ausschuss veräußert.</span><span class="sxs-lookup"><span data-stu-id="03cd7-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="03cd7-129">**Anschaffungspreis:** 24.000,00 US-Dollar (USD)</span><span class="sxs-lookup"><span data-stu-id="03cd7-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="03cd7-130">**Nutzungsdauer:** Zwei Jahre</span><span class="sxs-lookup"><span data-stu-id="03cd7-130">**Service life:** Two years</span></span>
- <span data-ttu-id="03cd7-131">**Abschreibungsmethode:** Lineare Nutzungsdauer</span><span class="sxs-lookup"><span data-stu-id="03cd7-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="03cd7-132">**Abschreibungsbetrag:** 1.000,00 USD pro Monat</span><span class="sxs-lookup"><span data-stu-id="03cd7-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="03cd7-133">Der NBW einer Anlage wird mithilfe der folgenden Formel berechnet:</span><span class="sxs-lookup"><span data-stu-id="03cd7-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="03cd7-134">Nettobuchwert = Anschaffungspreis – Abschreibung</span><span class="sxs-lookup"><span data-stu-id="03cd7-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="03cd7-135">In diesem Beispiel wurde die Anlage erworben und wurde für 15 Monate abgeschrieben, von Januar 2018 bis März 2019.</span><span class="sxs-lookup"><span data-stu-id="03cd7-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="03cd7-136">Daher ist der NBW der Anlage 9.000,00 USD (24.000,00 USD - 15.000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="03cd7-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="03cd7-137">[![Abschreibungsbeispiel für eine Anlage](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="03cd7-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="03cd7-138">Um eine Anlagenentsorgung zu erstellen, gehen Sie zu **Anlagen \> Journaleinträge \> Anlagenerfassung**, und wählen Sie dann im Aktivitätsbereich die Option **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="03cd7-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="03cd7-139">Wählen Sie **Verschrottung** und dann eine Anlagenkennung aus.</span><span class="sxs-lookup"><span data-stu-id="03cd7-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="03cd7-140">Um die Anlage vollständig zu entsorgen, geben Sie weder im Feld **Soll** noch im Feld **Haben** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="03cd7-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="03cd7-141">[![Anlagenerfassung](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="03cd7-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="03cd7-142">Durch die Anlagen-Ausschusstransaktion werden die Feldwerte für das Anlagenbuch wie folgt geändert:</span><span class="sxs-lookup"><span data-stu-id="03cd7-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="03cd7-143">Im Abschnitt **Saldo** wird das Feld **Status** auf **Verschrottet** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="03cd7-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="03cd7-144">Im Abschnitt **Abgang** wird das Feld **Abgangsdatum** auf das Datum festgelegt, an dem die Anlage verschrottet wurde.</span><span class="sxs-lookup"><span data-stu-id="03cd7-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="03cd7-145">[![Details zur Anlagenerfassung](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="03cd7-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="03cd7-146">Die folgende Abbildung zeigt das Anlagensaldo.</span><span class="sxs-lookup"><span data-stu-id="03cd7-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="03cd7-147">[![Anlagensaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="03cd7-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="03cd7-148">Die folgende Abbildung zeigt den Beleg, der gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="03cd7-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="03cd7-149">[![Nettobuchwert](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="03cd7-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
