---
title: Berechnen Sie TDS-Rechnungen mithilfe des Bestellformulars und des Auftragsformulars
description: Dieses Thema erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für verschiedene Rechnungsarten.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023258"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="68538-103">Berechnen Sie TDS-Rechnungen mithilfe des Bestellformulars und des Auftragsformulars</span><span class="sxs-lookup"><span data-stu-id="68538-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68538-104">Dieses Thema erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für verschiedene Rechnungsarten mithilfe der Seiten **Bestellung**, **Einkaufserfassung**, **Rahmenauftrag** und **Auftrag**.</span><span class="sxs-lookup"><span data-stu-id="68538-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="68538-105">Erstellen Sie auf der aufgeführten Seite eine Bestellung, ein Einkaufserfassung, einen Rahmenauftrag oder einen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="68538-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="68538-106">Geben Sie die erforderlichen Details ein.</span><span class="sxs-lookup"><span data-stu-id="68538-106">Enter the required details.</span></span>

2. <span data-ttu-id="68538-107">Wählen Sie die Registerkarte **Setup** aus, um sich die Art des Steuerschuldners des Kreditors oder Debitors anzeigen zu lassen.</span><span class="sxs-lookup"><span data-stu-id="68538-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="68538-108">Diese Informationen sind im Feld **Art des Steuerschuldners** unter der Feldgruppe **Quellensteuergruppe** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="68538-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="68538-109">Ändern oder lassen Sie sich im Feld **TDS-Gruppe** die Standard-TDS-Gruppe anzeigen, die für den Kreditor oder Debitor festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68538-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="68538-110">Das Feld **TCS-Gruppe** ist nicht verfügbar, wenn Sie eine TDS-Gruppe im Feld **TDS-Gruppe** auswählen.</span><span class="sxs-lookup"><span data-stu-id="68538-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="68538-111">TDS wird nur berechnet, wenn **Quellensteuer berechnen** für den Kreditor oder Debitor auf der Seite **Alle Kreditoren** oder **Alle Debitoren** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="68538-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="68538-112">Erstellen Sie Artikelpositionen in der Registerkarte **Positionen** und geben Sie die erforderlichen Details ein.</span><span class="sxs-lookup"><span data-stu-id="68538-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="68538-113">Wählen Sie (auf Positionsebene) die Registerkarte **Setup** um die auf Kopfzeilenebene definierte TDS-Gruppe anzusehen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="68538-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="68538-114">Die TDS-Gruppe wird im Feld **TDS-Gruppe** angezeigt, das Sie unter der Feldgruppe **Quellensteuergruppe** finden.</span><span class="sxs-lookup"><span data-stu-id="68538-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="68538-115">Wählen Sie die Registerkarte **Steuerliche Angaben** und dann alternative Adressen aus, die für den in diesem Feld angezeigten Unternehmensnamen eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="68538-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="68538-116">Der Unternehmensname wird im Feld **Name** angezeigt, das Sie unter der Feldgruppe **Unternehmensdaten** finden.</span><span class="sxs-lookup"><span data-stu-id="68538-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="68538-117">Die TAN des ausgewählten Unternehmensnamens wird im Feld **Steuerkontonummer** (**TAN**) unter der Feldgruppe **Quellensteuer**.</span><span class="sxs-lookup"><span data-stu-id="68538-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="68538-118">Wählen Sie **Quellensteuer** aus, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68538-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="68538-119">Sehen Sie sich die folgenden Felder im oberen Bereich der Seite **Temporäre Quellensteuerbuchungen** an.</span><span class="sxs-lookup"><span data-stu-id="68538-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="68538-120">**Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="68538-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="68538-121">**Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="68538-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="68538-122">Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt ist, die der Steuergruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="68538-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="68538-123">**Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="68538-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="68538-124">**TDS**: Ist dieses Feld ausgewählt, ist der Buchung eine TDS-Gruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="68538-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="68538-125">Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** auf der Seite **Temporäte Quellensteuerbuchungen** zeigen den berechneten TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68538-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="68538-126">Wählen Sie **Schwellenwert**, um die Seite **Schwellenwert** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68538-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="68538-127">Sehen Sie sich auf dieser Seite den Schwellenwert an, der für die TDS-Steuerkomponente definiert ist, die einem bestimmten TDS-Steuercode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68538-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="68538-128">Wählen Sie **Formeldesigner** aus, um die Seite **Formeldesigner** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68538-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="68538-129">Sehen Sie sich auf dieser Seite die Formel an, die für einen bestimmten TDS-Steuercode festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68538-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="68538-130">Buchen Sie die Rechnung.</span><span class="sxs-lookup"><span data-stu-id="68538-130">Post the invoice.</span></span> <span data-ttu-id="68538-131">Der auf Einkaufsrechnungen berechnete TDS-Betrag wird auf das Kreditorenkonto gebucht, und der auf Verkaufsrechnungen berechnete TDS-Betrag wird auf das Debitorenkonto gebucht, das für den jeweiligen Steuercode in der TDS-Gruppe festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="68538-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="68538-132">Die Kreditorenkonten für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68538-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="68538-133">Wählen Sie die Schaltfläche **Anfrage** **> Rechnung > Gebuchte Quellensteuer**, um die Seite **Quellensteuerbuchungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68538-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="68538-134">Im Feld **Wert** finden Sie den Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="68538-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="68538-135">Die Felder auf den Registerkarten **Übersicht**, **Allgemein** und **Betrag** auf der Seite **Quellensteuerbuchungen** enthalten die Informationen zur für die Buchung berechneten TDS.</span><span class="sxs-lookup"><span data-stu-id="68538-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="68538-136">Sehen Sie sich die Angaben zur TDS-Berechnung für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="68538-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
