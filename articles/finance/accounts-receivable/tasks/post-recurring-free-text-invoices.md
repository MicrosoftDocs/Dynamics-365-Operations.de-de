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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b31dbf296a06ea6253a8ae71bfea6193a1e03e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443564"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="08c51-103">Freitext-Serienrechnungen generieren und buchen</span><span class="sxs-lookup"><span data-stu-id="08c51-103">Generate and post recurring free text invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08c51-104">Mit Serienrechnungen wird Debitoren regelmäßig ein stets identischer Betrag in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="08c51-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="08c51-105">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="08c51-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="08c51-106">Die Erfassung ist für die Person bestimmt, die für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="08c51-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="08c51-107">Serienrechnungen generieren</span><span class="sxs-lookup"><span data-stu-id="08c51-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="08c51-108">Serienrechnungen buchen</span><span class="sxs-lookup"><span data-stu-id="08c51-108">Post recurring invoices</span></span>
1. <span data-ttu-id="08c51-109">en" Wechseln Sie zu "Debitor" > "Rechnungen" > "Wiederkehrende Rechnungen" > "Wiederkehrende Rechnungen buchen".</span><span class="sxs-lookup"><span data-stu-id="08c51-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="08c51-110">Verwenden Sie diese Seite, um Serienrechnungen anzuzeigen und zu drucken, die bereits generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="08c51-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="08c51-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="08c51-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="08c51-112">Wählen Sie die Serienrechnungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="08c51-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="08c51-113">Klicken Sie auf "Summen".</span><span class="sxs-lookup"><span data-stu-id="08c51-113">Click Totals.</span></span>
    * <span data-ttu-id="08c51-114">Überprüfen Sie Summen für die Serienrechnungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="08c51-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="08c51-115">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="08c51-115">Click Close.</span></span>
    * <span data-ttu-id="08c51-116">Jede Position unten ist eine Serien-Freitextrechnung.</span><span class="sxs-lookup"><span data-stu-id="08c51-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="08c51-117">Sie können eine Position auswählen und auf die Schaltfläche "Details" klicken, um Details zur Freitextrechnung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="08c51-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="08c51-118">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="08c51-118">Click Validate.</span></span>
    * <span data-ttu-id="08c51-119">Überprüfen Sie, dass die ausgewählten Rechnungen keine Fehler enthalten, aber buchen Sie die Rechnungen nicht.</span><span class="sxs-lookup"><span data-stu-id="08c51-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="08c51-120">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="08c51-120">Click Post.</span></span>
    * <span data-ttu-id="08c51-121">Bucht die ausgewählten Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="08c51-121">Post the selected invoices.</span></span>  

