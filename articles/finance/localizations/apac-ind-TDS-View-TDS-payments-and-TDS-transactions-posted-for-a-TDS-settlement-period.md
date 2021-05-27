---
title: Gebuchte TDS-Zahlungen und -buchungen für eine TDS-Ausgleichsperiode anzeigen
description: In diesem Thema wird erklärt, wie Sie die Zahlungen für die Quellenbesteuerung (TDS-Zahlungen) und entsprechenden Buchungen anzeigen, die für eine Ausgleichsperiode gebucht wurden.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 2bada42073e46c69101e6d31f3328a2eeb95f880
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023261"
---
# <a name="view-posted-tds-payments-and-transactions-for-a-tds-settlement-period"></a><span data-ttu-id="f2e6b-103">Gebuchte TDS-Zahlungen und -buchungen für eine TDS-Ausgleichsperiode anzeigen</span><span class="sxs-lookup"><span data-stu-id="f2e6b-103">View posted TDS payments and transactions for a TDS settlement period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2e6b-104">In diesem Thema wird erklärt, wie Sie die Zahlungen für die Quellenbesteuerung (TDS-Zahlungen) und entsprechenden Buchungen anzeigen, die für eine Ausgleichsperiode gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-104">This topic explains how to view the Tax Deducted at Source (TDS) payments and transactions that were posted for a settlement period.</span></span>

1. <span data-ttu-id="f2e6b-105">Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuerausgleichsperioden**.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="f2e6b-106">[![Seite „Quellensteuerausgleichsperioden“](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span><span class="sxs-lookup"><span data-stu-id="f2e6b-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-50.png)](./media/apac-ind-TDS-50.png)</span></span>

2. <span data-ttu-id="f2e6b-107">Wählen Sie auf der Seite **Quellensteuerausgleichsperioden** **Quellensteuerzahlungen** aus, um die Seite **Quellensteuerzahlungen** zu öffnen, auf der Sie die TDS-Ausgleiche anzeigen können, die für eine bestimmte TDS-Ausgleichsperiode vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-107">On the **Withholding tax settlement periods** page, select **Withholding tax payments** to open the **Withholding tax payments** page, where you can view the TDS settlements that were made for a specific TDS settlement period.</span></span>

    <span data-ttu-id="f2e6b-108">Die Registerkarte **Übersicht** zeigt die folgenden Informationen an:</span><span class="sxs-lookup"><span data-stu-id="f2e6b-108">The **Overview** tab shows the following information:</span></span>

    - <span data-ttu-id="f2e6b-109">**Datum**: Das Datum des TDS-Ausgleichs.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-109">**Date** – The date of TDS settlement.</span></span>
    - <span data-ttu-id="f2e6b-110">**Beleg**: Die Belegnummer der TDS-Ausgleichsbuchung.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-110">**Voucher** – The voucher number of the TDS settlement transaction.</span></span>
    - <span data-ttu-id="f2e6b-111">**Steuertyp**: Der Steuertyp, für den der Ausgleichsprozess durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-111">**Tax type** – The tax type that the settlement process is run for.</span></span>
    - <span data-ttu-id="f2e6b-112">**Steuerkontonummer (TAN)**: Die Steuerkontonummer (TAN) der ausgeglichenen TDS-Buchung.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-112">**Tax Account Number (TAN)** – The Tax Account Number (TAN) of the settled TDS transaction.</span></span>
    - <span data-ttu-id="f2e6b-113">**Ausgleichsperiode**: Die TDS-Ausgleichsperiode, für die der TDS-Ausgleichsprozess ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-113">**Settlement period** – The settlement period that the TDS settlement process is run for.</span></span>
    - <span data-ttu-id="f2e6b-114">**Startdatum**: Das Startdatum der Ausgleichsperiode.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-114">**From date** – The start date of the settlement period.</span></span>
    - <span data-ttu-id="f2e6b-115">**Enddatum**: Das Enddatum der Ausgleichsperiode.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-115">**To date** – The end date of the settlement period.</span></span>
    - <span data-ttu-id="f2e6b-116">**Quellensteuerzahlungsversion**: Die Version der Quellensteuerzahlung: **Original**, **Neueste Korrekturen** oder **Gesamtliste**.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-116">**Withholding tax payment version** – The version of the withholding tax payment: **Original**, **Latest corrections**, or **Total list**.</span></span>

5. <span data-ttu-id="f2e6b-117">Wählen Sie **Belege**, um die Belegeinträge für die TDS-Buchung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-117">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
6. <span data-ttu-id="f2e6b-118">Wählen Sie **Quellensteuerbuchungen**, um die Details der TDS-Buchungen anzuzeigen, die während einer Ausgleichsperiode für eine bestimmte Periode ausgeglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-118">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for a specific period during a settlement period.</span></span> <span data-ttu-id="f2e6b-119">Wählen Sie **Belege**, um die Belegeinträge für die TDS-Buchung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-119">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span> <span data-ttu-id="f2e6b-120">Wählen Sie **Quellensteuerkomponenten** aus, um sich die TDS anzeigen zu lassen, die pro TDS-Steuerkomponente für einen bestimmten TDS-Steuercode berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-120">Select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>
7. <span data-ttu-id="f2e6b-121">Schließen Sie die Seite **Quellensteuerzahlungen**, um zur Seite **Quellensteuerausgleichsperioden** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-121">Close the **Withholding tax payments** page to return to the **Withholding tax settlement periods** page.</span></span>
8. <span data-ttu-id="f2e6b-122">Wählen Sie **Quellensteuerbuchungen**, um die Details der TDS-Buchungen anzuzeigen, die während der Ausgleichsperiode ausgeglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="f2e6b-122">Select **Withholding tax transactions** to view the details of the TDS transactions that were settled for the settlement period.</span></span>
