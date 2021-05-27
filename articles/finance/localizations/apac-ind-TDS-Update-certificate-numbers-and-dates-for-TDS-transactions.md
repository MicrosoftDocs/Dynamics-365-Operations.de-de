---
title: Zertifikatsnummern und -daten für TDS-Buchungen aktualisieren
description: In diesem Thema wird erklärt, wie Sie auf die Nummern und Daten wiederherstellbarer Zertifikat aktualisieren, die für die Quellensteuerung (TDS) für Kreditor-, Debitor- und Sachkonten erstellt wurden.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023264"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="b46c1-103">Zertifikatsnummern und -daten für TDS-Buchungen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b46c1-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b46c1-104">In diesem Thema wird erklärt, wie Sie auf die Nummern und Daten wiederherstellbarer Zertifikat aktualisieren, die für die Quellensteuerung (TDS) für Kreditor-, Debitor- und Sachkonten erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b46c1-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="b46c1-105">Sie können sich die Zertifikate für TDS-Buchungen auf der Seite **Wiederherstellbare Zertifikate** anzeigen lassen.</span><span class="sxs-lookup"><span data-stu-id="b46c1-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="b46c1-106">Sie können die Zertifikate mithilfe der Seite **Zertifikate aktualisieren** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b46c1-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="b46c1-107">Gehen Sie wie folgt vor, um die Zertifikatsnummern und -daten für TDS-Buchungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b46c1-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="b46c1-108">Gehen Sie zu **Steuer \> Erklärungen \> Quellensteuer \> Zertifikat aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="b46c1-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="b46c1-109">[![Seite „Zertifikat aktualisieren“](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="b46c1-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="b46c1-110">Wählen Sie auf der Seite **Zertifikat aktualisieren** im Abschnitt **Auswählen** im Feld **Steuertyp** **TDS** aus.</span><span class="sxs-lookup"><span data-stu-id="b46c1-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="b46c1-111">Wählen Sie im Feld **Zertifikatsnummer** die TDS-Zertifikatsnummer des Debitors oder Kreditors aus.</span><span class="sxs-lookup"><span data-stu-id="b46c1-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b46c1-112">Das Feld **Zertifikatsnummer** enthält nur TDS-Zertifikatsnummern, bei denen **Geschlossen** auf der Seite **Wiederherstellbare Zertifikate** nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b46c1-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="b46c1-113">Im Feld **Zertifikatsdatum** ist das Zertifikatsdatum angegeben.</span><span class="sxs-lookup"><span data-stu-id="b46c1-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="b46c1-114">Im Feld **Kontotyp** ist der Kontotyp angegeben, für den die TDS-Zertifikatsnummer eingegangen ist. Das Feld **Name** zeigt den Namen des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b46c1-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="b46c1-115">Wählen Sie in den Feldern **Startdatum** und **Enddatum** das Start- und Enddatum des Zeitraums aus, für den TDS-Buchungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b46c1-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="b46c1-116">Wählen Sie **Daten anzeigen** aus, um die TDS-Buchungen anzuzeigen, die im ausgewählten Zeitraum gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="b46c1-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="b46c1-117">Das Raster im oberen Bereich der Registerkarte **Übersicht** enthält zu jeder TDS-Buchung, die im ausgewählten Zeitraum für den Kreditor oder Debitor gebucht wurde, die folgende Informationen:</span><span class="sxs-lookup"><span data-stu-id="b46c1-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="b46c1-118">**Beleg**: Die Belegnummer der TDS-Buchung.</span><span class="sxs-lookup"><span data-stu-id="b46c1-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="b46c1-119">**Datum**: Das Datum der TDS-Buchung.</span><span class="sxs-lookup"><span data-stu-id="b46c1-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="b46c1-120">**Betrag**: Der Rechnungsbetrag, auf dessen Grundlage die TDS berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="b46c1-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="b46c1-121">**Steuerbetrag**: Der TDS-Steuerbetrag, der für die Buchung berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="b46c1-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="b46c1-122">Um bestimmte TDS-Buchungen vom oberen in das untere Raster zu verschieben, wählen Sie die Buchungen und dann **Einschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="b46c1-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="b46c1-123">Alternativ wählen Sie **Alle einschließen** aus, um alle TDS-Buchungen vom oberen in das untere Raster zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="b46c1-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="b46c1-124">Um bestimmte oder alle TDS-Buchungen vom unteren in das obere Raster zu verschieben, nutzen Sie die Schaltfläche **Ausschließen** oder **Alle ausschließen**.</span><span class="sxs-lookup"><span data-stu-id="b46c1-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="b46c1-125">Wählen Sie **Aktualisieren**, um die Felder **Zertifikatsnummer** und **Zertifikatsdatum** für TDS-Buchungen im unteren Raster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b46c1-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="b46c1-126">Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Wiederherstellbares Zertifikat** und wählen Sie **Anfrage** aus, um die aktualisierten Buchungspositionen mit den neuen Zertifikatsnummern auf der Seite **Zertifikatsbuchungen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b46c1-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="b46c1-127">[![Seite „Zertifikatsbuchungen“](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="b46c1-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
