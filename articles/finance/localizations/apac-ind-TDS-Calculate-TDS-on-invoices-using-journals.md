---
title: TDS auf Rechnungen mithilfe von Erfassungen berechnen
description: Dieses Thema erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für Erfassungen.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023282"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="f5e5d-103">TDS auf Rechnungen mithilfe von Erfassungen berechnen</span><span class="sxs-lookup"><span data-stu-id="f5e5d-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5e5d-104">Dieses Thema erklärt die Schritte zur Berechnung der Quellenbesteuerung (TDS) für Erfassungen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="f5e5d-105">Öffnen sie zunächst die Seite **Allgemeine Erfassungen** (**Hauptbuch > Erfassungseinträge > Allgemeine Erfassungen**).</span><span class="sxs-lookup"><span data-stu-id="f5e5d-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="f5e5d-106">[![Allgemeine Erfassungen](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="f5e5d-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="f5e5d-107">Erstellen Sie Erfassungspositionen mit den in der Tabelle aufgeführten Erfassungsformularen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="f5e5d-108">Wählen Sie den Kontotyp und den Gegenkontotyp aus und geben Sie den Betrag für die Buchung ein.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="f5e5d-109">Geben Sie auf der Seite **Rechnungsgenehmigungserfassung** **Belege finden** und wählen Sie die Rechnungen aus, für die TDS berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="f5e5d-110">Zeigen Sie die Rechnungen an, die auf der Seite **Rechnungsregister** oder der Seite **Belege finden** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="f5e5d-111">Sehen Sie auf der Seite **Allgemein** der Seite **Alle Journale** im Feld **TDS-Gruppe** die Standard-TDS-Gruppe an und aktualisieren Sie sie, die für den Kreditor bzw. Debitor festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="f5e5d-112">Der TDS-Betrag, der in Erfassungspositionen berechnet wird, basiert auf der Formel, die für die TDS-Steuercodes im Feld **TDS-Gruppe** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="f5e5d-113">Wenn Sie eine TDS-Gruppe im Feld **TDS-Gruppe** auswählen, sind die Felder **Quellensteuergruppe** und **TCS-Gruppe** nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="f5e5d-114">Das Feld **Quellensteuergruppe** ist nur auf der Seite **Allgemeine Erfassung** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="f5e5d-115">TDS wird nur berechnet, wenn **Quellensteuer berechnen** für den Kreditor oder Debitor auf den Seiten **Alle Kreditoren** oder **Alle Debitoren** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="f5e5d-116">Wählen Sie die Registerkarte **Steuerliche Angaben** und dann gegebenenfalls die alternative Adressen eines Unternehmens aus, das in diesem Feld als Unternehmen eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="f5e5d-117">Sie können sich den Unternehmensnamen im Feld **Name** anzeigen lassen, das Sie unter der Feldgruppe **Unternehmensdaten** finden.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="f5e5d-118">Lassen sie sich die Steuerschuldnerkategorie dieses Kreditors oder Debitors im Feld **Art des Steuerschuldners** anzeigen, das Sie in der Feldgruppe **Quellensteuer** finden.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="f5e5d-119">Lassen Sie sich im Feld **Steuerkontonummer** (**TAN**) die TAN des ausgewählten, angezeigten Unternehmensnamens, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="f5e5d-120">Wählen Sie **Quellensteuer** im Menü **Quellensteuer** aus, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="f5e5d-121">Im oberen Bereich der Seite **Temporäre Quellensteuerbuchungen** werden die folgenden Felder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="f5e5d-122">**Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="f5e5d-123">**Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="f5e5d-124">Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt ist, die der Steuergruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="f5e5d-125">**Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="f5e5d-126">**TDS**: Ist dieses Feld ausgewählt, ist der Buchung eine TDS-Gruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="f5e5d-127">Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** auf der Seite **Temporäte Quellensteuerbuchungen** zeigen den berechneten TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="f5e5d-128">Wählen Sie **Schwellenwert**, um die Seite **Schwellenwert** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="f5e5d-129">Sehen Sie den Schwellenwert und Ausnahmeschwellenwert an, die für die TDS-Steuerkomponente definiert sind, die einem bestimmten TDS-Steuercode zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="f5e5d-130">Wählen Sie **Formeldesigner** aus, um das Formular **Formeldesigner** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="f5e5d-131">Sehen Sie sich auf dieser Seite die Formel an, die für einen bestimmten TDS-Steuercode festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="f5e5d-132">Schließen Sie den **Formeldesigner** und die Seiten **Temporäre Quellensteuerbuchungen**, um zu der Seite **Alle Journale** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="f5e5d-133">Geben Sie die weiteren erforderlichen Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-133">Enter the other required details.</span></span> <span data-ttu-id="f5e5d-134">Prüfen und buchen Sie die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-134">Validate and post the journal.</span></span> <span data-ttu-id="f5e5d-135">Der auf Einkaufrechnungen berechnete TDS-Betrag wird auf das Kreditorenkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="f5e5d-136">Der auf Einkaufsrechnungen berechnete TDS-Betrag wird auf das zu Debitorenkonto gebucht, das für den jeweiligen TDS-Steuercode in der TDS-Gruppe festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="f5e5d-137">Die Kreditorenkonten für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="f5e5d-138">Wählen Sie **Gebuchte Quellensteuer** aus, um die Seite **Quellensteuerbuchungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="f5e5d-139">Im Feld **Wert** wird der Gesamtprozentsatz angezeigt, der zur Berechnung der TDS für die Buchung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="f5e5d-140">Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Betrag** auf der Seite „Quellensteuerbuchungen“ zeigen den berechneten TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5e5d-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
