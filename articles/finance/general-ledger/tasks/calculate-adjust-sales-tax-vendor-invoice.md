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
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186278"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="1ad30-103">Mehrwertsteuer auf einer Kreditorenrechnung berechnen und anpassen</span><span class="sxs-lookup"><span data-stu-id="1ad30-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ad30-104">In diesem Thema wird erläutert, wie Sie die Mehrwertsteuer für eine Kreditorenrechnung anpassen.</span><span class="sxs-lookup"><span data-stu-id="1ad30-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="1ad30-105">Wenn das ursprüngliche Quelldokument verschiedene Steuerbeträge anzeigt, können Sie diese Beträge vor dem Buchen anpassen.</span><span class="sxs-lookup"><span data-stu-id="1ad30-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="1ad30-106">Für diese Aufgabe wird das Demo-Unternehmen DEMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ad30-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="1ad30-107">Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="1ad30-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="1ad30-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1ad30-108">Select **New**.</span></span>
3. <span data-ttu-id="1ad30-109">Wählen Sie im Feld **Name** der neuen Zeile eine Option im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="1ad30-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="1ad30-110">Wählen Sie im Aktivitätsbereich **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="1ad30-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="1ad30-111">Geben Sie im Feld **Konto** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="1ad30-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="1ad30-112">Geben Sie im Feld **Rechnung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1ad30-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="1ad30-113">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1ad30-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="1ad30-114">Geben Sie im Feld **Gegenkonto** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="1ad30-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="1ad30-115">Wählen Sie **Mehrwertsteuer** aus.</span><span class="sxs-lookup"><span data-stu-id="1ad30-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="1ad30-116">Geben Sie im Feld **Gesamter tatsächlicher Mehrwertsteuerbetrag** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1ad30-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="1ad30-117">Auf der Registerkarte **Regulierung** können die Mehrwertsteuerbeträge pro Mehrwertsteuercode angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="1ad30-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="1ad30-118">Wählen Sie **Istwerte aus berechneten Beträgen zurücksetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="1ad30-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="1ad30-119">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ad30-119">Select **OK**.</span></span>
14. <span data-ttu-id="1ad30-120">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1ad30-120">Select **Save**.</span></span>

