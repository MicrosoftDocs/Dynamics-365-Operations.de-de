---
title: Freitext-Serienrechnungen generieren und buchen
description: Mit Serienrechnungen wird Debitoren regelmäßig ein stets identischer Betrag in Rechnung gestellt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysLookupMultiSelectGrid, CustRecurrenceInvoiceGroup, CustFreeInvoice, CustRecurrenceInvoiceTotals
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56600abe791c2a299f6c8f77398e0e5ac51710a3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220178"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="e6a2c-103">Freitext-Serienrechnungen generieren und buchen</span><span class="sxs-lookup"><span data-stu-id="e6a2c-103">Generate and post recurring free text invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6a2c-104">Mit Serienrechnungen wird Debitoren regelmäßig ein stets identischer Betrag in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="e6a2c-105">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="e6a2c-106">Die Erfassung ist für die Person bestimmt, die für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="e6a2c-107">Serienrechnungen generieren</span><span class="sxs-lookup"><span data-stu-id="e6a2c-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="e6a2c-108">Serienrechnungen buchen</span><span class="sxs-lookup"><span data-stu-id="e6a2c-108">Post recurring invoices</span></span>
1. <span data-ttu-id="e6a2c-109">en" Wechseln Sie zu "Debitor" > "Rechnungen" > "Wiederkehrende Rechnungen" > "Wiederkehrende Rechnungen buchen".</span><span class="sxs-lookup"><span data-stu-id="e6a2c-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="e6a2c-110">Verwenden Sie diese Seite, um Serienrechnungen anzuzeigen und zu drucken, die bereits generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="e6a2c-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e6a2c-112">Wählen Sie die Serienrechnungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="e6a2c-113">Klicken Sie auf "Summen".</span><span class="sxs-lookup"><span data-stu-id="e6a2c-113">Click Totals.</span></span>
    * <span data-ttu-id="e6a2c-114">Überprüfen Sie Summen für die Serienrechnungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="e6a2c-115">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="e6a2c-115">Click Close.</span></span>
    * <span data-ttu-id="e6a2c-116">Jede Position unten ist eine Serien-Freitextrechnung.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="e6a2c-117">Sie können eine Position auswählen und auf die Schaltfläche "Details" klicken, um Details zur Freitextrechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="e6a2c-118">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="e6a2c-118">Click Validate.</span></span>
    * <span data-ttu-id="e6a2c-119">Überprüfen Sie, dass die ausgewählten Rechnungen keine Fehler enthalten, aber buchen Sie die Rechnungen nicht.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="e6a2c-120">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="e6a2c-120">Click Post.</span></span>
    * <span data-ttu-id="e6a2c-121">Bucht die ausgewählten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="e6a2c-121">Post the selected invoices.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]