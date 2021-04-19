---
title: Quellensteuer bei Verkaufsbuchungen
description: In diesem Thema werden die Schritte aufgeführt, mit denen die Berechnung der Quellensteuer für ausgewählte Debitoren vermieden werden kann. Für Debitoren, die in ihren Zahlungen an Sie eine Quellensteuer angeben, können Sie die Standard-Quellensteuergruppe zuweisen.
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
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842343"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="cc70f-104">Quellensteuer bei Verkaufsbuchungen</span><span class="sxs-lookup"><span data-stu-id="cc70f-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="cc70f-105">In diesem Thema werden die Schritte aufgeführt, mit denen die Berechnung der Quellensteuer für ausgewählte Debitoren vermieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc70f-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="cc70f-106">Für Debitoren, die in ihren Zahlungen an Sie eine Quellensteuer angeben, können Sie die Standard-**Quellensteuergruppe** auf der Seite **Debitoren** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cc70f-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="cc70f-107">Rufen Sie **Navigationsbereich > Module > Debitorenkonten > Debitoren > Alle Debitoren** auf.</span><span class="sxs-lookup"><span data-stu-id="cc70f-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="cc70f-108">Klicken Sie auf das entsprechende Debitorenkonto und dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="cc70f-109">Setzen Sie auf der Registerkarte **Rechnung und Lieferung** das Feld **Quellensteuer berechnen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="cc70f-110">Die Quellensteuer wird nicht berechnet, wenn für diesen Debitoren in den Masterdaten nicht **Quellensteuer berechnen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cc70f-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="cc70f-111">Wählen Sie eine Quellensteuergruppe unter **Quellensteuergruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="cc70f-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="cc70f-112">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-112">Click **Save**.</span></span>

<span data-ttu-id="cc70f-113">Für Artikel/Dienstleistungen, die der Quellensteuer unterliegen, können Sie die Standardeinstellung **Artikel-Quellensteuergruppe** in **Freigegebene Produkte** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cc70f-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="cc70f-114">Wechseln Sie zu **Navigationsbereich > Module > Produktinformationsverwaltung > Produkte > Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="cc70f-115">Klicken Sie auf die entsprechende Artikelnummer und dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="cc70f-116">Klicken Sie auf der Registerkarte **Verkauf** auf **Quellensteuer berechnen**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="cc70f-117">Die Quellensteuer wird nicht berechnet, wenn **Quellensteuer berechnen** für diesen Artikel auf der Registerkarte **Verkauf** der Seite **Freigegebenes Produkt** nicht auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="cc70f-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="cc70f-118">Wählen Sie eine Artikel-Quellensteuergruppe in der Liste **Artikel-Quellensteuergruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="cc70f-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="cc70f-119">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="cc70f-119">Click **Save**.</span></span>

<span data-ttu-id="cc70f-120">Quellensteuergruppen und Artikel-Quellensteuergruppen können über die Seite **Auftrag** zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="cc70f-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="cc70f-121">Die Standard-Quellensteuergruppe und die Artikel-Quellensteuergruppe werden als Standardeinträge in Auftragspositionen verwendet, wenn Sie einen neuen Auftrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc70f-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="cc70f-122">Die Quellensteuer über die **Debitorzahlungserfassung** berechnet und gebucht.</span><span class="sxs-lookup"><span data-stu-id="cc70f-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="cc70f-123">Sie können den entsprechenden Quellensteuercode sowie den tatsächlichen Quellensteuerbetrag auf der Registerkarte **Quellensteuer** der Seite **Buchungen ausgleichen** manuell anpassen.</span><span class="sxs-lookup"><span data-stu-id="cc70f-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="cc70f-124">Der berechnete Quellensteuerbetrag wird von der Debitorenzahlung abgezogen und auf das **Quellensteuer-Gegenkonto** über einen dazugehörigen Beleg gebucht.</span><span class="sxs-lookup"><span data-stu-id="cc70f-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]