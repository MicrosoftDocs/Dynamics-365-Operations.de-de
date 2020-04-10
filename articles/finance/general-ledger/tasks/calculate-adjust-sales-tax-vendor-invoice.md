---
title: Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen
description: In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung in Dynamics 365 Finance anpassen.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139966"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="b6d5f-103">Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen</span><span class="sxs-lookup"><span data-stu-id="b6d5f-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6d5f-104">In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung anpassen.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="b6d5f-105">Wenn das ursprüngliche Quelldokument verschiedene Steuerbeträge anzeigt, können Sie diese Beträge vor dem Buchen anpassen.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="b6d5f-106">Für diese Aufgabe wird das Demo-Unternehmen DEMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="b6d5f-107">Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="b6d5f-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-108">Select **New**.</span></span>
3. <span data-ttu-id="b6d5f-109">Wählen Sie im Feld **Name** der neuen Zeile eine Option im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="b6d5f-110">Wählen Sie im Aktivitätsbereich **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="b6d5f-111">Geben Sie im Feld **Konto** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="b6d5f-112">Geben Sie im Feld **Rechnung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="b6d5f-113">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="b6d5f-114">Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="b6d5f-115">Wählen Sie **Mehrwertsteuer** aus.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="b6d5f-116">Geben Sie im Feld **Gesamter tatsächlicher Mehrwertsteuerbetrag** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="b6d5f-117">Auf der Registerkarte **Regulierung** können die Mehrwertsteuerbeträge pro Mehrwertsteuercode angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="b6d5f-118">Wählen Sie **Istwerte aus berechneten Beträgen zurücksetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="b6d5f-119">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-119">Select **OK**.</span></span>
14. <span data-ttu-id="b6d5f-120">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b6d5f-120">Select **Save**.</span></span>

