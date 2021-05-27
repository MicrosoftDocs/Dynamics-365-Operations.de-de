---
title: Quellensteuerausgleichsperioden für den Steuertyp „TDS“
description: In diesem Thema wird erklärt, wie Sie Ausgleichsperioden für die Quellenbesteuerung (TDS) einrichten.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023255"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="8013a-103">Quellensteuerausgleichsperioden für den Steuertyp „TDS“</span><span class="sxs-lookup"><span data-stu-id="8013a-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8013a-104">In diesem Thema wird erklärt, wie Sie Ausgleichsperioden für die Quellenbesteuerung (TDS) einrichten.</span><span class="sxs-lookup"><span data-stu-id="8013a-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="8013a-105">Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuerausgleichsperioden**.</span><span class="sxs-lookup"><span data-stu-id="8013a-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="8013a-106">[![Seite „Quellensteuerausgleichsperioden“](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="8013a-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="8013a-107">Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuerausgleichsperioden für den Steuertyp „TDS“ einzurichten.</span><span class="sxs-lookup"><span data-stu-id="8013a-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="8013a-108">Wählen Sie **Neu**, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8013a-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="8013a-109">Geben Sie im Feld **Ausgleichsperiode** einen Namen für die TDS-Ausgleichsperiode ein.</span><span class="sxs-lookup"><span data-stu-id="8013a-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="8013a-110">Geben Sie im Feld **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="8013a-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="8013a-111">Wählen Sie im Feld **Quellensteuerbehörde** die TDS-Behörde aus, für die Sie die TDS-Ausgleichsperiode festlegen.</span><span class="sxs-lookup"><span data-stu-id="8013a-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="8013a-112">Im Inforegister **Allgemein** wählen Sie im Feld **Periodenintervall** die Art des Periodenintervalls für die TDS-Ausgleichsperiode aus.</span><span class="sxs-lookup"><span data-stu-id="8013a-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="8013a-113">Geben Sie im Feld **Anzahl der Einheiten** Anzahl der Einheiten für den Periodenintervalltyp an.</span><span class="sxs-lookup"><span data-stu-id="8013a-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="8013a-114">Wählen Sie im Inforegister **Perioden** im Feld **Startdatum** das Startdatum für die TDS-Ausgleichsperiode aus.</span><span class="sxs-lookup"><span data-stu-id="8013a-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="8013a-115">Wählen Sie im Feld **Enddatum** das Enddatum aus.</span><span class="sxs-lookup"><span data-stu-id="8013a-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="8013a-116">Um für eine vorhandene Periode basierend auf dem Periodenintervall und den Periodeneinheiten eine nachfolgende TDS-Ausgleichsperiode zu erstellen, wählen Sie **Neue Periode**.</span><span class="sxs-lookup"><span data-stu-id="8013a-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="8013a-117">Um die Details des periodischen TDS-Ausgleichs anzuzeigen, der für eine bestimmte Ausgleichsperiode ausgeführt wird, wählen Sie **Quellensteuerzahlungen**, um die Seite **Quellensteuerzahlung** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8013a-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8013a-118">Um den periodischen TDS-Ausgleichsprozess auszuführen, gehen Sie zu **Hauptbuch \> Periodisch \> Quellensteuer \> Quellensteuerzahlung**.</span><span class="sxs-lookup"><span data-stu-id="8013a-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="8013a-119">[![Seite „Quellensteuerzahlung“](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="8013a-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="8013a-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8013a-120">Close the page.</span></span>
