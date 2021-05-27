---
title: TDS-Steuercodes zu TDS-Steuergruppen hinzufügen und die Formel zur TDS-Berechnung festlegen
description: In diesem Thema wird erklärt, wie Sie Steuergruppen für die Quellenbesteuerung (TDS) einrichten und TDS-Steuercodes mit TDS-Steuergruppen verknüpfen. Um die TDS für eine TDS-Steuergruppe zu berechnen, müssen Sie die Formel für die damit verbundenen TDS-Steuercodes festlegen.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023277"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="ccfb0-104">TDS-Steuercodes zu TDS-Steuergruppen hinzufügen und die Formel zur TDS-Berechnung festlegen</span><span class="sxs-lookup"><span data-stu-id="ccfb0-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccfb0-105">In diesem Thema wird erklärt, wie Sie Steuergruppen für die Quellenbesteuerung (TDS) einrichten und TDS-Steuercodes mit TDS-Steuergruppen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="ccfb0-106">Um die TDS für eine TDS-Steuergruppe zu berechnen, müssen Sie die Formel für die damit verbundenen TDS-Steuercodes festlegen.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="ccfb0-107">Gehen Sie wie folgt vor, um eine TDS-Steuergruppe einzurichten, TDS-Steuercodes anzuhängen und die Formel für die TDS-Berechnung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="ccfb0-108">Gehen Sie zu **Steuer \> Indirekte Steuern \> Quellensteuer \> Quellensteuergruppen**.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="ccfb0-109">[![Seite „Quellensteuergruppen“](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="ccfb0-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="ccfb0-110">Wählen Sie im Aktionsbereich die Option **Neu** aus, um eine Quellensteuergruppe für TDS zu erstellen und die erforderlichen Details einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="ccfb0-111">Wählen Sie im Feld **Steuertyp** die Option **TDS** aus.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="ccfb0-112">Wählen Sie im Inforegister **Setup** **Hinzufügen** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="ccfb0-113">Wählen Sie im Feld **Quellensteuercode** den TDS-Steuercode für die TDS-Steuergruppe aus.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="ccfb0-114">Das Feld **Quellensteuername** zeigt den Namen des TDS-Steuercodes und das Feld **Wert** zeigt den Wert.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="ccfb0-115">Um den Schwellenwert und den Ausnahmeschwellenwert zu ignorieren, die für die TDS-Steuerkomponente festgelegt sind, die in TDS-Buchungen mit dem TDS-Steuercode verbunden sind, wählen Sie die Option **Schwellenwert übersehen**.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="ccfb0-116">Um zu verhindern, dass die Steuergruppe in Buchungen berechnet wird, aktivieren Sie **Befreit**.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="ccfb0-117">Wählen Sie im Aktionsbereich **Designer** aus, um den Formeldesigner zu öffnen, damit Sie die Formel zur Berechnung der TDS für die TDS-Steuergruppe festlegen können.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="ccfb0-118">Auf der Seite **Designer** werden unter der Registerkarte **Steuern** die TDS-Steuercodes angezeigt, die für die TDS-Steuergruppe ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="ccfb0-119">[![Designerseite](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="ccfb0-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="ccfb0-120">Wählen Sie auf der Registerkarte **Berechnung** **ALT + N** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="ccfb0-121">Im Feld **Kennung** wird die automatisch generierte Prioritätskennung für die TDS-Berechnung.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="ccfb0-122">Wählen Sie im Feld **Steuercode** den TDS-Steuercode aus, für den Sie eine Formel festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="ccfb0-123">In diesem Feld können alle TDS-Steuercodes ausgewählt werden, die für die TDS-Steuergruppe ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="ccfb0-124">Wählen Sie im Feld **Steuerbemessungsgrundlage** die Grundlage für die Berechnung der TDS aus:</span><span class="sxs-lookup"><span data-stu-id="ccfb0-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="ccfb0-125">**Bruttobetrag**: Berechnen Sie die TDS auf Grundlage des Bruttobuchungsbetrags (d. h. des Rechnungsbetrags) unter Verwendung des für das Steuercodes definierten Berechnungsausdrucks.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="ccfb0-126">**Ohne Bruttobetrag**: Berechnen Sie TDS auf Basis des Berechnungsausdrucks, der für den Steuercode festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccfb0-127">Das Feld **Bemessungsgrundlage** kann nicht auf **Ohne Bruttobetrag** gesetzt werden, wenn der Steuercode die Prioritätskennung **1** hat.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="ccfb0-128">Die TDS-Berechnung basiert auf der Formel, die im Feld **Berechnungsausdruck** für jeden Steuercode festgelegt ist, der der TDS-Steuergruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="ccfb0-129">Wählen Sie das Pluszeichen (**+**), Minuszeichen (**-**), Multiplikationszeichen (**\**_) oder Divisonszeichen (_*/**), um den Berechnungsausdruck für den ausgewählten TDS-Steuercode in das Feld **Berechnungsausdruck** einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccfb0-130">Für den TDS-Steuercode mit der Prioritätskennung **1** kann kein Berechnungsausdruck definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="ccfb0-131">Um den Berechnungsausdruck für den Steuercode im Feld **Berechnungsausdruck** festzulegen, fügen Sie im Feld TDS-Steuercodes hinzu, die in der Registerkarte **Steuern** verfügbar sind. Um TDS-Steuercodes in das Feld **Berechnungsausdruck** einzufügen können Sie eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="ccfb0-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="ccfb0-132">Ziehen Sie den gewünschten Steuercode aus der Registerkarte **Steuern** in das Feld **Berechnungsausdruck**.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="ccfb0-133">Tippen Sie auf den erforderlichen Steuercode in der Registerkarte **Steuern** (oder machen Sie einen Doppelklick darauf).</span><span class="sxs-lookup"><span data-stu-id="ccfb0-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="ccfb0-134">Wählen Sie den erforderlichen Steuercode in der Registerkarte **Steuern** aus und halten Sie ihn fest (oder klicken Sie mit der rechten Maustaste darauf) und wählen Sie dann **Steuercode hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccfb0-135">Fügen Sie vor jedem TDS-Steuercode einen Berechnungsausdruck ein.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="ccfb0-136">Die dem Berechnungsausdruck hinzugefügten TDS-Steuercodes werden in Klammern angezeigt (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="ccfb0-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="ccfb0-137">Um den Berechnungsausdruck zu löschen, der für einen Steuercode im Feld **Berechnungsausdruck** festgelegt ist, drücken Sie die **C**-Taste.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="ccfb0-138">Um einen Datensatz aus der Registerkarte **Berechnung** zu löschen, wählen Sie **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="ccfb0-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ccfb0-139">Close the page.</span></span>
