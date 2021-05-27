---
title: TDS-Berechnung auf Rechnungen von der Seite „Freitextrechnung“
description: In diesem Thema wird erklärt, wie Sie die Quellenbesteuerung (TDS) auf Rechnungen mithilfe der Seite „Freitextrechnung“ berechnen.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023274"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="1986f-103">TDS-Berechnung auf Rechnungen von der Seite „Freitextrechnung“</span><span class="sxs-lookup"><span data-stu-id="1986f-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1986f-104">In diesem Thema wird erklärt, wie Sie die Quellenbesteuerung (TDS) auf Rechnungen mithilfe der Seite **Freitextrechnung** berechnen.</span><span class="sxs-lookup"><span data-stu-id="1986f-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="1986f-105">Wechseln Sie zu **Debitoren \> Rechnungen \> Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="1986f-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="1986f-106">[![Freitextrechnungs-Seite](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="1986f-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="1986f-107">Wählen Sie **Neu** aus, um eine Freitextrechnung zu erstellen, und geben Sie die erforderlichen Details ein.</span><span class="sxs-lookup"><span data-stu-id="1986f-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="1986f-108">Wählen Sie die Registerkarte **Rechnung** aus. Im Abschnitt **Quellensteuergruppe** zeigt das Feld **Art des Steuerschuldners** die Steuerschuldnerkategorie des Debitors an.</span><span class="sxs-lookup"><span data-stu-id="1986f-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="1986f-109">Überprüfen oder ändern Sie im Feld **TDS-Gruppe** die Standard-TDS-Gruppe, die für den Debitor festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1986f-110">Wenn Sie das Feld **TDS-Gruppe** auswählen, ist das Feld **TCS-Gruppe** nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1986f-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="1986f-111">TDS wird nur berechnet, wenn die Option **Quellensteuer berechnen** für den Debitor auf der Seite **Alle Debitoren** auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="1986f-112">Auf der Registerkarte **Steuerliche Angaben** können Sie im Abschnitt **Unternehmensdaten** im Feld **Name** den Unternehmensnamen für eine alternative Adresse auswählen, die für das Unternehmen eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="1986f-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="1986f-113">Im Abschnitt **Quellensteuer** zeigt das Feld **Steuerkontonummer (TAN)** die Steuerkontonummer (TAN) für das ausgewählte Unternehmen an.</span><span class="sxs-lookup"><span data-stu-id="1986f-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="1986f-114">Erstellen Sie in der Registerkarte **Rechnungspositionen** Rechnungspositionen und geben Sie die erforderlichen Details ein.</span><span class="sxs-lookup"><span data-stu-id="1986f-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="1986f-115">Im Abschnitt **Quellensteuergruppe** wird im Feld **Steuerkontonummer (TAN)** die TAN und das Feld **TDS-Gruppe** die TDS-Gruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1986f-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="1986f-116">Wählen Sie **Quellensteuer** aus, um die Seite **Temporäre Quellensteuerbuchungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1986f-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="1986f-117">Der obere Teil dieser Seite enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="1986f-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="1986f-118">**Quellensteuergesamtbetrag**: Die Gesamt-TDS, die für die Buchung für die TDS-Gruppe berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="1986f-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="1986f-119">**Wert**: Der Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1986f-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="1986f-120">Der Gesamtprozentsatz basiert auf der Formel, die für die TDS-Steuercodes festgelegt und der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="1986f-121">**Angepasster Quellensteuergesamtbetrag**: Der angepasste TDS-Gesamtbetrag für alle Steuercodes in der TDS-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1986f-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="1986f-122">**TDS**: Ein ausgewähltes Kontrollkästchen zeigt an, dass der Buchung eine TDS-Gruppe zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="1986f-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="1986f-123">Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Anpassung** zeigen den berechnete TDS-Betrag und die Details des angepassten TDS-Betrags für jeden TDS-Steuercode an, der der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="1986f-124">Wählen Sie **Schwellenwert** aus, um die Seite **Schwellenwert** zu öffnen, wo Sie den Schwellenwert überprüfen, der für die TDS-Steuerkomponente definiert ist, die einem bestimmten TDS-Steuercode zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="1986f-125">Wählen Sie **Formeldesigner** aus, um die Seite **Formeldesigner** zu öffnen, auf der Sie die Formel überprüfen können, die für einen bestimmten TDS-Steuercode festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="1986f-126">Buchen Sie die Freitextrechnung.</span><span class="sxs-lookup"><span data-stu-id="1986f-126">Post the free text invoice.</span></span> <span data-ttu-id="1986f-127">Der für Freitextrechnungen berechnete TDS-Betrag wird auf das zu Debitorenkonto gebucht, das für den jeweiligen TDS-Steuercode in der TDS-Gruppe festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="1986f-128">Die Debitorenkonto für TDS-Steuercodes sind auf der Seite **Quellensteuercodes** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1986f-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="1986f-129">Wählen Sie die **Gebuchte Quellensteuer**, um die Seite **Quellensteuerbuchungen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1986f-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="1986f-130">Das Feld **Wert** zeigt den Gesamtprozentsatz, der zur Berechnung der TDS für die Buchung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1986f-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="1986f-131">Die Felder in den Registerkarten **Übersicht**, **Allgemein** und **Betrag** werden die TDS-Beträge angezeigt, die in den Rechnungspositionen berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="1986f-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="1986f-132">Überprüfen Sie die Angaben zur TDS-Berechnung für jeden TDS-Steuercode, der der TDS-Gruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1986f-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
