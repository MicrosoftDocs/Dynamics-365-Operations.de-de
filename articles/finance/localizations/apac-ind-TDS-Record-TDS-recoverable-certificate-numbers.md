---
title: Die Nummern wiederherstellbarer TDS-Zertifikate erfassen
description: In diesem Thema wird erklärt, wie Sie auf der Seite „Wiederherstellbare Zertifikate“ die Zertifikatsnummern und -daten für die Quellenbesteuerung (TDS-Zertifikate) erfassen, die für einen bestimmten Kreditor, Debitor oder ein bestimmtes Sachkonto eingehen.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023254"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="44455-103">Die Nummern wiederherstellbarer TDS-Zertifikate erfassen</span><span class="sxs-lookup"><span data-stu-id="44455-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44455-104">In diesem Thema wird erklärt, wie Sie auf der Seite **Wiederherstellbare Zertifikate** die Zertifikatsnummern und -daten für die Quellenbesteuerung (TDS-Zertifikate) erfassen, die für einen bestimmten Kreditor, Debitor oder ein bestimmtes Sachkonto eingehen.</span><span class="sxs-lookup"><span data-stu-id="44455-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="44455-105">Verwenden Sie, um TDS-Zertifikatsnummern und -daten zu aktualisieren, die für TDS-Buchungen auf dieser Seite erfasst wurden, die Seite **Zertifikat aktualisieren** (**Hauptbuch \> Periodisch \> Quellensteuer \> Zertifikat aktualisieren**).</span><span class="sxs-lookup"><span data-stu-id="44455-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="44455-106">Schließen Sie die TDS-Zertifikatnummern, nachdem Sie sie aktualisiert haben.</span><span class="sxs-lookup"><span data-stu-id="44455-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="44455-107">Gehen Sie wie folgt vor, um die TDS-Zertifikatsnummern und -daten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="44455-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="44455-108">Gehen Sie zu **Steuer \> Indirekte Steuer \> Quellensteuer \> Wiederherstellbare Zertifikate**.</span><span class="sxs-lookup"><span data-stu-id="44455-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="44455-109">[![Seite „Wiederherstellbare Zertifikate“](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="44455-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="44455-110">Wählen Sie auf der Seite **Wiederherstellbare Zertifikate** im Feld **Steuertyp** **TDS** aus.</span><span class="sxs-lookup"><span data-stu-id="44455-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="44455-111">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44455-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="44455-112">Geben Sie im Feld **Zertifikatnummer** die TDS-Zertifikatnummer ein.</span><span class="sxs-lookup"><span data-stu-id="44455-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="44455-113">Wählen Sie im Feld **Kontotyp** den Kontotyp aus, für den das TDS-Zertifikat eingegangen ist: **Kreditor**, **Debitor** oder **Sachkonto**.</span><span class="sxs-lookup"><span data-stu-id="44455-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="44455-114">Wählen Sie im Feld **Konto** die Kontonummer des Kreditors, Debitors oder Sachkontos aus, je nachdem, welchen Kontotyp Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="44455-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="44455-115">Das Feld **Name** Namen des Kreditor-, Debitor- oder Sachkontos an.</span><span class="sxs-lookup"><span data-stu-id="44455-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="44455-116">Geben Sie im Feld **Zertifikatbetrag** den Betrag des TDS-Zertifikats ein.</span><span class="sxs-lookup"><span data-stu-id="44455-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="44455-117">Geben Sie im Feld **Datum** die das Zertifikatsdatum für die Zertifikatnummer ein.</span><span class="sxs-lookup"><span data-stu-id="44455-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="44455-118">Wählen Sie **Anfragen**, um die Seite **Zertifikatsbuchung** zu öffnen, auf der Sie die TDS-Buchungen anzeigen können, für die die TDS-Zertifikatsnummer und das -datum aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="44455-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="44455-119">Diese Informationen können auf der Seite **Zertifikat aktualisieren** aktualisiert werden (**Steuer \> Erklärungen \> Quellensteuer \> Zertifikat aktualisieren**).</span><span class="sxs-lookup"><span data-stu-id="44455-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="44455-120">Die Seite **Zertifikat aktualisieren** zeigt die folgenden Informationen für jede offene TDS-Buchung an:</span><span class="sxs-lookup"><span data-stu-id="44455-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="44455-121">**Datum**: Das Buchungsdatum der TDS-Buchung.</span><span class="sxs-lookup"><span data-stu-id="44455-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="44455-122">**Beleg**: Die Belegnummer der TDS-Buchung.</span><span class="sxs-lookup"><span data-stu-id="44455-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="44455-123">**Quelle**: Das Modul, in dem die TDS-Buchung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="44455-124">**Konto**: Die Kreditor-, Debitor- oder Sachkontonummer, für die die TDS-Buchung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="44455-125">**Name**: Der Name des Kreditors, Debitors oder Sachkontos, für die die TDS-Buchung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="44455-126">**Betrag**: Der Rechnungsbetrag, auf dessen Grundlage die TDS berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="44455-127">**Steuerbetrag**: Der TDS-Steuerbetrag, der für die Buchung berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="44455-128">**Zertifikatsdatum**: Das Datum des TDS-Zertifikats, das für die TDS-Buchung aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="44455-129">**Zertifikatsnummer**: Die Nummer des TDS-Zertifikats, die für die TDS-Buchung aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44455-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="44455-130">Wählen Sie auf der Seite **Wiederherstellbare Zertifikate** das Kontrollkästchen **Geschlossen** aus, um die TDS-Zertifikatsnummer zu schließen, nachdem Sie die Aktualisierung für TDS-Buchungen auf der Seite **Zertifikat aktualisieren** beendet haben.</span><span class="sxs-lookup"><span data-stu-id="44455-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="44455-131">Um das Kontrollkästchen **Geschlossen** für alle Datensätze auf der Seite auszuwählen, wählen Sie **Alles markieren** aus.</span><span class="sxs-lookup"><span data-stu-id="44455-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="44455-132">Die TDS-Zertifikatsnummern, für die das Kontrollkästchen **Geschlossen** aktiviert ist, stehen auf der Seite **Zertifikat aktualisieren** nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="44455-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
