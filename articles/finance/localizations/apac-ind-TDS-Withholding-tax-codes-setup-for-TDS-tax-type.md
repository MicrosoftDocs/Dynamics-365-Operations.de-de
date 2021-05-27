---
title: Quellensteuercoes für den Steuertyp „TDS“ einrichten
description: In diesem Thema wird erklärt, wie die Steuercodes für Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023280"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="a15bb-103">Quellensteuercoes für den Steuertyp „TDS“ einrichten</span><span class="sxs-lookup"><span data-stu-id="a15bb-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a15bb-104">In diesem Thema wird erklärt, wie die Steuercodes für Quellenbesteuerung (TDS) einrichten.</span><span class="sxs-lookup"><span data-stu-id="a15bb-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="a15bb-105">Wechseln Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="a15bb-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="a15bb-106">[![Seite „Quellensteuercodes“](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="a15bb-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="a15bb-107">Wählen Sie im Aktionsbereich die Option **Neu** aus, um einen Quellensteuercode für TDS zu erstellen und die erforderlichen Details einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a15bb-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="a15bb-108">Im Inforegister **Allgemein** wählen Sie im Feld **Steuertyp** **TDS** aus, um den Steuercode als TDS-Steuercode zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="a15bb-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="a15bb-109">Wählen Sie im Feld **Ausgleichsperiode** die TDS-Ausgleichsperiode für den TDS-Steuercode.</span><span class="sxs-lookup"><span data-stu-id="a15bb-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="a15bb-110">Wählen Sie im Feld **Hauptkonto** das Sachkonto aus, auf das der TDS-Betrag gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a15bb-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="a15bb-111">Wählen Sie im Feld **Debitorenkonto** das Debitorenkonto aus, auf das der TDS-Betrag gebucht werden soll, der bei Verkaufsbuchungen abgezogen wird.</span><span class="sxs-lookup"><span data-stu-id="a15bb-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="a15bb-112">Das Feld **Ursprung** wird automatisch auf **Prozentanteil am Bruttobetrag** gesetzt und der Wert kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a15bb-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a15bb-113">Sie können den Ursprung bei Steuercodes des Steuertyps „TDS“ nicht auf **Prozentanteil am Nettobetrag** setzen.</span><span class="sxs-lookup"><span data-stu-id="a15bb-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="a15bb-114">Wählen Sie im Feld **Quellensteuerkomponente** die TDS-Steuerkomponente für den TDS-Steuercode aus.</span><span class="sxs-lookup"><span data-stu-id="a15bb-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="a15bb-115">Wählen Sie im Aktionsbereich **Werte** aus, um die Seite **Quellensteuerwerte** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a15bb-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="a15bb-116">Geben Sie im Feld **Startdatum** das Startdatum für des TDS-Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a15bb-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="a15bb-117">Geben Sie im Feld **Enddatum** das Enddatum ein.</span><span class="sxs-lookup"><span data-stu-id="a15bb-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a15bb-118">Die Felder **Untergrenze**, **Obergrenze** und **% ausschließen** sind für Steuercodes des Steuertyps „TDS“ nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a15bb-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="a15bb-119">Geben Sie im Feld **Wert** den Prozentsatz am TDS für den TDS-Steuercode ein.</span><span class="sxs-lookup"><span data-stu-id="a15bb-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="a15bb-120">Schließen Sie die Seite **Quellensteuerwerte**, um zur Seite **Quellensteuercodes** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a15bb-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a15bb-121">Die Schaltfläche **Grenzwerte** auf der Seite **Quellensteuercodes** ist für Steuercodes des Steuertyps „TDS“ nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a15bb-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="a15bb-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a15bb-122">Close the page.</span></span>
