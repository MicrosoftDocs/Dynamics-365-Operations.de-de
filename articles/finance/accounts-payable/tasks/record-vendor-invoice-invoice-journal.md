---
title: Eine Kreditorenrechnung in der Rechnungserfassung erfassen
description: Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140374"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="c5a55-103">Eine Kreditorenrechnung in der Rechnungserfassung erfassen</span><span class="sxs-lookup"><span data-stu-id="c5a55-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5a55-104">Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c5a55-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="c5a55-105">Beispiele dieses Typs der Rechnung umfassen Ausgaben für Verbrauchsmaterial oder Dienstleistungen.</span><span class="sxs-lookup"><span data-stu-id="c5a55-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="c5a55-106">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5a55-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="c5a55-107">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Arbeitsbereiche > Kreditorenrechnungseintrag**.</span><span class="sxs-lookup"><span data-stu-id="c5a55-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="c5a55-108">Klicken Sie im **Aktivitätsbereich** auf **Neue Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="c5a55-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="c5a55-109">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c5a55-109">Click **New**.</span></span>
4. <span data-ttu-id="c5a55-110">Geben Sie im Feld **Name** den Erfassungsnamen ein, oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5a55-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="c5a55-111">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c5a55-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="c5a55-112">Klicken Sie im **Aktivitätsbereich** auf **Positionen**.</span><span class="sxs-lookup"><span data-stu-id="c5a55-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="c5a55-113">Geben Sie im Feld **Datum** das Buchungsdatum ein, das das Hauptbuch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c5a55-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="c5a55-114">Geben Sie im Feld **Konto** das **Kreditorenkonto** an.</span><span class="sxs-lookup"><span data-stu-id="c5a55-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="c5a55-115">Geben Sie im Feld **Rechnung** die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="c5a55-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="c5a55-116">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c5a55-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="c5a55-117">Geben Sie im Feld **Kredit** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="c5a55-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="c5a55-118">Geben Sie im Feld **Gegenkonto** den Kontonamen ein, oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5a55-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="c5a55-119">Die **Mehrwertsteuergruppe** bezieht sich standardmäßig auf das Kreditorenkonto.</span><span class="sxs-lookup"><span data-stu-id="c5a55-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="c5a55-120">Die **Artikel-Mehrwertsteuergruppe** bezieht sich standardmäßig auf das Hauptkonto, das im Feld **Gegenkonto** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c5a55-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="c5a55-121">Das **Fälligkeitsdatum** wird anhand der Zahlungsbedingungen berechnet.</span><span class="sxs-lookup"><span data-stu-id="c5a55-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="c5a55-122">Der **Skonto** wird standardmäßig aus dem Kreditorenkonto ermittelt.</span><span class="sxs-lookup"><span data-stu-id="c5a55-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="c5a55-123">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="c5a55-123">Click **Post**.</span></span>
13. <span data-ttu-id="c5a55-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c5a55-124">Close the page.</span></span>

