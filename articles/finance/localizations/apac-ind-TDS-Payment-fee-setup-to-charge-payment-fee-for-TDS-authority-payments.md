---
title: Einrichten einer Zahlungsgebühr für TDS-Behördenzahlungen
description: In diesem Thema wird erläutert, wie Sie Zahlungsgebühren einrichten, die für Behördenzahlungen für die Quellenbesteuerung (TDS) erhoben werden.
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023283"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="c29da-103">Einrichten einer Zahlungsgebühr für TDS-Behördenzahlungen</span><span class="sxs-lookup"><span data-stu-id="c29da-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c29da-104">In diesem Thema wird erläutert, wie Sie Zahlungsgebühren einrichten, die für Behördenzahlungen für die Quellenbesteuerung (TDS) erhoben werden.</span><span class="sxs-lookup"><span data-stu-id="c29da-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="c29da-105">Gehen Sie zu **Kreditorenkonten \> Zahlungseinstellungen \> Zahlungsgebühr**.</span><span class="sxs-lookup"><span data-stu-id="c29da-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="c29da-106">[![Seite „Zahlungsgebühr“](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="c29da-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="c29da-107">Wählen Sie **Neu** aus, um eine Zahlungsgebühr zu erstellen, und geben Sie die erforderlichen Details ein.</span><span class="sxs-lookup"><span data-stu-id="c29da-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="c29da-108">Wählen Sie im Feld **Gebührentyp** den Typ der Zahlungsgebühr aus:</span><span class="sxs-lookup"><span data-stu-id="c29da-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="c29da-109">**Keines**</span><span class="sxs-lookup"><span data-stu-id="c29da-109">**None**</span></span>
    - <span data-ttu-id="c29da-110">**Zinsen**: Zinsen fallen für verspätete Zahlungen an den TDS-Behördenkreditor an.</span><span class="sxs-lookup"><span data-stu-id="c29da-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="c29da-111">**Andere**: Andere Gebühren, die für verspätete Zahlungen an den TDS-Behördenkreditor anfallen.</span><span class="sxs-lookup"><span data-stu-id="c29da-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="c29da-112">Wenn Sie **Zinsen** oder **Andere** auswählen wird das Feld **Belastung** automatisch auf **Hauptbuch** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="c29da-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="c29da-113">Wenn Sie **Zinsen** oder **Andere** im Feld **Feldtyp** auswählt haben, wählen Sie im Feld **Hauptkonto** das Sachkonto aus, auf das die Zinsen oder andere Gebühren gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c29da-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="c29da-114">Geben Sie die weiteren erforderlichen Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="c29da-114">Enter the other required details.</span></span>
6. <span data-ttu-id="c29da-115">Wählen Sie im Aktionsbereich die Option **Zahlungsgebühreinstellungen** aus, um die Seite **Zahlungsgebühreinstellungen** zu öffnen, auf der Sie Zahlungsgebühren für verschiedene Kombinationen von Banken, Zahlungsmethoden, Zahlungsspezifikationen, Währungen und Datumsintervallen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="c29da-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="c29da-116">[![Seite „Zahlungsgebühreinstellungen“](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="c29da-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="c29da-117">Legen Sie auf der Registerkarte **Übersicht** im Feld **Gruppierungen** fest, für welche Banken Sie die Zahlungsgebühr einrichten:</span><span class="sxs-lookup"><span data-stu-id="c29da-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="c29da-118">**Tabelle**: Die Gebühr gilt für ein bestimmtes Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="c29da-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="c29da-119">**Gruppe**: Die Gebühr gilt für eine bestimmte Bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="c29da-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="c29da-120">**Alle**: Die Gebühr ist für alle Bankkonten gültig.</span><span class="sxs-lookup"><span data-stu-id="c29da-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="c29da-121">Wenn Sie **Tabelle** oder **Gruppe** im Feld **Gruppierungen** ausgewählt haben, wählen Sie im Feld **Bankrelation** das spezifische Bankkonto oder die Bankgruppe aus, für die Sie die Zahlungsgebühr einrichten.</span><span class="sxs-lookup"><span data-stu-id="c29da-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="c29da-122">Wählen Sie im Feld **Zahlungsmethode** die Zahlungsmethode für die Zahlung der Zahlungsgebühren aus.</span><span class="sxs-lookup"><span data-stu-id="c29da-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="c29da-123">Wählen Sie im Feld **Zahlungsspezifikation** den Zahlungsspezifikationscode aus, der auf der Seite **Zahlungsspezifikation** generiert wurde, oder geben Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="c29da-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="c29da-124">Die Zahlungsspezifikation wird mit Methoden des elektronischen Geldverkehrs für Zahlungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c29da-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="c29da-125">Wählen Sie im Feld **Zahlungswährung** die Währung aus, welche die Gebühr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c29da-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="c29da-126">Nur Buchungen, die die ausgewählte Währung verwenden, können die Gebühr aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c29da-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="c29da-127">Wenn Sie dieses Feld leer lassen, aktivieren alle Währungen die Gebühr.</span><span class="sxs-lookup"><span data-stu-id="c29da-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="c29da-128">Wählen Sie im Feld **Prozentsatz/Betrag** die Berechnungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="c29da-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="c29da-129">Als Optionen stehen **Betrag**, **Prozent** und **Intervall** zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c29da-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="c29da-130">Geben Sie im Feld **Gebührenbetrag** den Gebührenbetrag entweder als Prozentsatz der Zahlung oder als Betrag pro Zahlung an.</span><span class="sxs-lookup"><span data-stu-id="c29da-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="c29da-131">Wählen Sie im Feld **Gebührenwährung** den Währungscode für die Gebühr aus.</span><span class="sxs-lookup"><span data-stu-id="c29da-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="c29da-132">Wählen Sie die Registerkarte **Allgemein** aus, um die Details des ausgewählten Bankkontos anzuzeigen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c29da-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="c29da-133">[![Registerkarte „Allgemeines“](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="c29da-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="c29da-134">Geben Sie im Feld **Minimum** den Mindestbuchungsbetrag an, der die Gebühr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c29da-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="c29da-135">Geben Sie im Feld **Maximum** den Höchstbuchungsbetrag an, der die Gebühr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c29da-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="c29da-136">Legen Sie in den Feldern **Startdatum** und **Enddatum** einen Datumsbereich für die Berechnung der Gebühren fest.</span><span class="sxs-lookup"><span data-stu-id="c29da-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="c29da-137">Geben Sie im Feld **Mindestgebühr** den Gebührenbetrag entweder als Prozentsatz der Zahlung oder als Betrag pro Zahlung an.</span><span class="sxs-lookup"><span data-stu-id="c29da-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="c29da-138">Wählen Sie im Feld **Mehrwertsteuergruppe** die Mehrwertsteuergruppe aus, anhand der die Mehrwertsteuer für den Gebührenbetrag berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c29da-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="c29da-139">Wählen Sie im Feld **Artikel-Mehrwertsteuergruppe** die Artikel-Mehrwertsteuergruppe aus, anhand der die Artikel-Mehrwertsteuer für den Gebührenbetrag berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c29da-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="c29da-140">Wählen Sie die Registerkarte **Intervall** aus.</span><span class="sxs-lookup"><span data-stu-id="c29da-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="c29da-141">[![Registerkarte „Intervall“](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="c29da-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="c29da-142">Geben Sie im Feld **Tage** die Anzahl der Tage zwischen dem Buchungsdatum (Skontodatum) der Zahlung und dem Fälligkeitsdatum des Solawechsels ein.</span><span class="sxs-lookup"><span data-stu-id="c29da-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="c29da-143">Wählen Sie im Feld **Prozentsatz/Betrag** aus, ob es sich bei der Spezifikation um einen Prozentsatz oder einen festen Betrag handelt.</span><span class="sxs-lookup"><span data-stu-id="c29da-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="c29da-144">Geben Sie im Feld **Gebührenbetrag** den Gebührenbetrag entweder als Prozentsatz der Zahlung oder als Betrag pro Zahlung an.</span><span class="sxs-lookup"><span data-stu-id="c29da-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="c29da-145">Schließen Sie die Seite **Zahlungsgebühreinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="c29da-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="c29da-146">Schließen Sie die Seite **Zahlungsgebühr**.</span><span class="sxs-lookup"><span data-stu-id="c29da-146">Close the **Payment fee** page.</span></span>
