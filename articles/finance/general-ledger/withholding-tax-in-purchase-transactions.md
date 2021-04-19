---
title: Quellensteuer bei Kaufbuchungen
description: Bei Kreditoren, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Quellensteuergruppe** auf der Seite **Alle Kreditoren** zuweisen.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: faeaf0746532875d3517a208c9c338c112bf2c77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816882"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="09965-103">Quellensteuer bei Kaufbuchungen</span><span class="sxs-lookup"><span data-stu-id="09965-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="09965-104">Bei Kreditoren, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Quellensteuergruppe** auf der Seite **Alle Kreditoren** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="09965-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="09965-105">Rufen Sie **Navigationsbereich > Module > Kreditorenkonten > Kreditoren > Alle Kreditoren** auf.</span><span class="sxs-lookup"><span data-stu-id="09965-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="09965-106">Klicken Sie auf das entsprechende Kreditorenkonto und dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="09965-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="09965-107">Setzen Sie auf der Registerkarte **Rechnung und Lieferung** das Feld **Quellensteuer berechnen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="09965-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="09965-108">Die Quellensteuer wird nicht berechnet, wenn für diesen Kreditor in den Daten nicht **Quellensteuer berechnen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="09965-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="09965-109">Wählen Sie eine Quellensteuergruppe unter **Quellensteuergruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="09965-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="09965-110">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="09965-110">Click **Save**.</span></span>

<span data-ttu-id="09965-111">Für Artikel/Dienstleistungen, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Artikel-Quellensteuergruppe** in **Freigegebene Produkte** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="09965-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="09965-112">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="09965-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="09965-113">Klicken Sie auf die entsprechende Artikelnummer und dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="09965-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="09965-114">Klicken Sie auf der Registerkarte **Kauf** auf **Quellensteuer berechnen**.</span><span class="sxs-lookup"><span data-stu-id="09965-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="09965-115">Die Quellensteuer wird nicht berechnet, wenn **Quellensteuer berechnen** für diesen Artikel auf der Registerkarte **Kauf** der Seite **Freigegebenes Produkt** nicht auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="09965-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="09965-116">Wählen Sie eine Artikel-Quellensteuergruppe in der Liste **Artikel-Quellensteuergruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="09965-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="09965-117">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="09965-117">Click **Save**.</span></span>

<span data-ttu-id="09965-118">Quellensteuergruppen und Artikel-Quellensteuergruppen können auf folgenden Seiten zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="09965-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="09965-119">**Bestellung**</span><span class="sxs-lookup"><span data-stu-id="09965-119">**Purchase order**</span></span>
- <span data-ttu-id="09965-120">**Kreditorenrechnung**</span><span class="sxs-lookup"><span data-stu-id="09965-120">**Vendor invoice**</span></span>
- <span data-ttu-id="09965-121">**Rechnungserfassung**</span><span class="sxs-lookup"><span data-stu-id="09965-121">**Invoice journal**</span></span>

<span data-ttu-id="09965-122">Die Standard-Quellensteuergruppe und die Artikel-Quellensteuergruppe werden beim Erstellten von **Bestellungen** und/oder **Ausstehende Kreditorenrechnungen** in die Positionen übernommen.</span><span class="sxs-lookup"><span data-stu-id="09965-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="09965-123">Sie können für die **Kreditorenrechnungserfassung** die Option **Quellensteuer berechnen** aktivieren und auf der Registerkarte **Allgemein** der Erfassung **Artikel-Quellensteuergruppe** auswählen.</span><span class="sxs-lookup"><span data-stu-id="09965-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="09965-124">Der vorübergehende Quellensteuerbetrag wird im Feld **Angepasste Quellensteuer** der Registerkarte **Summen** auf der Seite **Bestellung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09965-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Die Quellensteuer ist in der Bestellung enthalten](media/withholding-tax-adjusted.png)

<span data-ttu-id="09965-126">Die Quellensteuer wird in der **Kreditorenzahlungserfassung** berechnet.</span><span class="sxs-lookup"><span data-stu-id="09965-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="09965-127">Sie können die entsprechenden Quellensteuercodes sowie die tatsächlichen Quellensteuerbeträge auf der Registerkarte **Quellensteuer** der Seite **Buchungen ausgleichen** manuell anpassen.</span><span class="sxs-lookup"><span data-stu-id="09965-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Die Quellensteuer kann auf der Seite „Buchungen ausgleichen“ manuell angepasst werden](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="09965-129">Der abgeleitete Quellensteuerbetrag wird von der Kreditorenzahlung abgezogen und auf das **Quellensteuerkonto** über einen dazugehörigen Beleg gebucht.</span><span class="sxs-lookup"><span data-stu-id="09965-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Das Quellensteuerkonto zeigt einen dazugehörigen Beleg an](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]