--- 
title: Eine Kreditorenrechnung in der Rechnungserfassung erfassen
description: Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 26515140b020d824f99441b9f1ee560a44e28f8f
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="9ca31-103">Eine Kreditorenrechnung in der Rechnungserfassung erfassen</span><span class="sxs-lookup"><span data-stu-id="9ca31-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ca31-104">Diese Aufgabenanleitung zeigt, wie Kreditorenrechnungen erfasst werden, die keinen Bestellungen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ca31-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="9ca31-105">Beispiele dieses Typs der Rechnung umfassen Ausgaben für Verbrauchsmaterial oder Dienstleistungen.</span><span class="sxs-lookup"><span data-stu-id="9ca31-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="9ca31-106">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ca31-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="9ca31-107">Wechseln Sie zu "Kreditoren" > "Arbeitsbereiche" > "Kreditorenrechnungseintrag".</span><span class="sxs-lookup"><span data-stu-id="9ca31-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="9ca31-108">Klicken Sie auf "Neue Rechnungserfassung".</span><span class="sxs-lookup"><span data-stu-id="9ca31-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="9ca31-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="9ca31-109">Click New.</span></span>
4. <span data-ttu-id="9ca31-110">Geben Sie im Feld "Name" den Erfassungsname ein oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9ca31-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="9ca31-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9ca31-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9ca31-112">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="9ca31-112">Click Lines.</span></span>
    * <span data-ttu-id="9ca31-113">Geben Sie im Feld "Datum" das Buchungsdatum ein, das das Hauptbuch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9ca31-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="9ca31-114">Geben Sie im Feld "Konto" das "Kreditorenkonto" an.</span><span class="sxs-lookup"><span data-stu-id="9ca31-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="9ca31-115">Geben Sie im Feld "Rechnung" die Rechnungsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="9ca31-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="9ca31-116">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9ca31-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="9ca31-117">Geben Sie im Feld "Kredit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="9ca31-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="9ca31-118">Geben Sie im Feld "Gegenkonto" den Kontoname ein oder klicken Sie auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9ca31-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="9ca31-119">Die Mehrwertsteuergruppe bezieht sich standardmäßig auf das Kreditorenkonto.</span><span class="sxs-lookup"><span data-stu-id="9ca31-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="9ca31-120">Die Artikelmehrwertsteuer-Gruppe bezieht sich standardmäßig auf das Hauptkonto, das im Feld "Gegenkonto" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9ca31-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="9ca31-121">Das "Fälligkeitsdatum" wird anhand der "Zahlungsbedingungen" berechnet.</span><span class="sxs-lookup"><span data-stu-id="9ca31-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="9ca31-122">Der "Skonto" wird standardmäßig aus dem Kreditorenkonto ermittelt.</span><span class="sxs-lookup"><span data-stu-id="9ca31-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="9ca31-123">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="9ca31-123">Click Post.</span></span>
13. <span data-ttu-id="9ca31-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9ca31-124">Close the page.</span></span>


