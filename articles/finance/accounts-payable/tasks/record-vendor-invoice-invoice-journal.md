---
title: Eine Kreditorenrechnung in der Rechnungserfassung erfassen
description: Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35862195f3c2c13711157be919956f40fea0989b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820640"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="2f5a2-103">Eine Kreditorenrechnung in der Rechnungserfassung erfassen</span><span class="sxs-lookup"><span data-stu-id="2f5a2-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f5a2-104">Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="2f5a2-105">Beispiele dieses Typs der Rechnung umfassen Ausgaben für Verbrauchsmaterial oder Dienstleistungen.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="2f5a2-106">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="2f5a2-107">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Arbeitsbereiche > Kreditorenrechnungseintrag**.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="2f5a2-108">Klicken Sie im **Aktivitätsbereich** auf **Neue Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="2f5a2-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-109">Click **New**.</span></span>
4. <span data-ttu-id="2f5a2-110">Geben Sie im Feld **Name** den Erfassungsnamen ein, oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="2f5a2-111">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="2f5a2-112">Klicken Sie im **Aktivitätsbereich** auf **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="2f5a2-113">Geben Sie im Feld **Datum** das Buchungsdatum ein, das das Hauptbuch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="2f5a2-114">Geben Sie im Feld **Konto** das **Kreditorenkonto** an.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="2f5a2-115">Geben Sie im Feld **Rechnung** die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="2f5a2-116">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="2f5a2-117">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="2f5a2-118">Geben Sie im Feld **Gegenkonto** den Kontonamen ein, oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="2f5a2-119">Die **Mehrwertsteuergruppe** bezieht sich standardmäßig auf das Kreditorenkonto.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="2f5a2-120">Die **Artikel-Mehrwertsteuergruppe** bezieht sich standardmäßig auf das Hauptkonto, das im Feld **Gegenkonto** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="2f5a2-121">Das **Fälligkeitsdatum** wird anhand der Zahlungsbedingungen berechnet.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="2f5a2-122">Der **Skonto** wird standardmäßig aus dem Kreditorenkonto ermittelt.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="2f5a2-123">Wenn Sie den Workflow für die Kreditorenrechnungserfassung aktiviert haben, klicken Sie auf **Workflow > Senden**.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="2f5a2-124">Wenn Ihre Übermittlung genehmigt wurde, wird das Datum auf den ersten Tag des nächsten offenen Zeitraums vorverlegt, wenn das Datum der Transaktionsbuchung in einen Zeitraum fällt, der für die Buchung im Hauptbuch gesperrt oder geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="2f5a2-125">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-125">Click **Post**.</span></span>
13. <span data-ttu-id="2f5a2-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]