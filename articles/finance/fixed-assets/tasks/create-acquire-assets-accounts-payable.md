---
title: Anlagen von "Kreditoren" erstellen und anschaffen
description: Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess.
author: saraschi2
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e3342c5e667ad3c8f3638afdcd9f3c15a815777
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823955"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="046f0-103">Anlagen von "Kreditoren" erstellen und anschaffen</span><span class="sxs-lookup"><span data-stu-id="046f0-103">Create and acquire assets from Accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="046f0-104">Diese Aufgabenanleitung führt Sie Schritt für Schritt durch die Erstellung und Anschaffung einer Anlage mit dem Einkaufsprozess.</span><span class="sxs-lookup"><span data-stu-id="046f0-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="046f0-105">Dabei werden der "Buchhalter" und die "Sachbearbeiter Kreditorenkonten" und das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="046f0-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="046f0-106">Anlagenparametern festlegen</span><span class="sxs-lookup"><span data-stu-id="046f0-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="046f0-107">Wechseln Sie im **Navigationsbereich** zu **Module > Anlagen > Einstellungen > Anlagenparameter**.</span><span class="sxs-lookup"><span data-stu-id="046f0-107">In the **Navigation pane**, go to **Modules > Fixed assets > Setup > Fixed assets parameters**.</span></span>
2. <span data-ttu-id="046f0-108">Erweitern Sie das Inforegister **Bestellungen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-108">Expand the **Purchase orders** fastTab.</span></span>
3. <span data-ttu-id="046f0-109">Aktivieren Sie das Kontrollkästchen **Anlagenanschaffung aus Einkauf zulassen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-109">Check the **Allow asset acquisition from Purchasing** checkbox.</span></span>
4. <span data-ttu-id="046f0-110">Aktivieren Sie das Kontrollkästchen **Anlage bei Buchung von Produktzugang oder Rechnung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-110">Check the **Create asset during product receipt or invoice posting** checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="046f0-111">Eine neue Kreditorenrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="046f0-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="046f0-112">Wechseln Sie im **Navigationsbereich** zu **Module > Kreditoren > Arbeitsbereiche > Kreditorenrechnungseintrag**.</span><span class="sxs-lookup"><span data-stu-id="046f0-112">In the **Navigation pane**, go to **Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="046f0-113">Klicken Sie auf **Neue Kreditorenrechnung**.</span><span class="sxs-lookup"><span data-stu-id="046f0-113">Click **New vendor invoice**.</span></span>
3. <span data-ttu-id="046f0-114">Klicken Sie im Feld **Rechnungskonto** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="046f0-114">In the **Invoice account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="046f0-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="046f0-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="046f0-116">Geben Sie im Feld **Zahl** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="046f0-116">In the **Number** field, type a value.</span></span>
6. <span data-ttu-id="046f0-117">Geben Sie im Feld **Buchungsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="046f0-117">In the **Posting date** field, enter a date.</span></span>
7. <span data-ttu-id="046f0-118">Klicken Sie auf **Position hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-118">Click **Add line**.</span></span>
8. <span data-ttu-id="046f0-119">Klicken Sie im Feld **Artikelnummer** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="046f0-119">In the **Item number** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="046f0-120">Entweder nicht gelagerte Artikel oder Beschaffungskategorien können für Anlagenanschaffung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="046f0-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="046f0-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="046f0-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="046f0-122">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="046f0-122">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="046f0-123">Eine Rechnungsposition erstellt nur eine Anlage, unabhängig von Menge.</span><span class="sxs-lookup"><span data-stu-id="046f0-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span> <span data-ttu-id="046f0-124">Der Rechnungsmengen-Feldwert wird zur Anlagenmenge übertragen.</span><span class="sxs-lookup"><span data-stu-id="046f0-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="046f0-125">Geben Sie im Feld **Einzelpreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="046f0-125">In the **Unit price** field, enter a number.</span></span>
12. <span data-ttu-id="046f0-126">Erweitern Sie das Inforegister **Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="046f0-126">Expand the **Line details** fastTab.</span></span>
13. <span data-ttu-id="046f0-127">Klicken Sie auf die Registerkarte **Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-127">Click the **Fixed assets** tab.</span></span>
14. <span data-ttu-id="046f0-128">Aktivieren Sie das Kontrollkästchen **Neue Anlage erstellen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-128">Check the **Create a new fixed asset** checkbox.</span></span>
15. <span data-ttu-id="046f0-129">Klicken Sie im Feld **Anlagengruppe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="046f0-129">In the **Fixed asset group** field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="046f0-130">Wählen Sie in der Liste die Anlagengruppe aus, die beim Erstellen der neuen Anlage zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="046f0-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="046f0-131">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="046f0-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="046f0-132">Klicken Sie auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="046f0-132">Click **Post**.</span></span> <span data-ttu-id="046f0-133">Die Anlage wird erstellt und abgerufen, wann die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="046f0-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]