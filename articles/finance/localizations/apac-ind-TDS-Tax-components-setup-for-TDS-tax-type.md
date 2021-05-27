---
title: Steuerkomponenten für den Steuertyp „TDS“ einrichten
description: In diesem Thema wird erläutert, wie Sie Quellensteuerkomponenten für den die Quellenbesteuerung (Steuertyp „TDS“) einrichten. Außerdem wird erläutert, wie Sie den Schwellenwert festlegen, der zur Berechnung der TDS für jede TDS-Komponente verwendet wird.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023263"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="cb7ba-104">Steuerkomponenten für den Steuertyp „TDS“ einrichten</span><span class="sxs-lookup"><span data-stu-id="cb7ba-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb7ba-105">In diesem Thema wird erläutert, wie Sie Quellensteuerkomponenten für den die Quellenbesteuerung (Steuertyp „TDS“) einrichten.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="cb7ba-106">Die TDS-Komponenten lauten TDS, Aufpreis, PE-Sondersteuer und SHE-Sondersteuer.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="cb7ba-107">Außerdem wird in diesem Thema erläutert, wie Sie den Schwellenwert festlegen, der zur Berechnung der TDS für jede TDS-Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="cb7ba-108">Darüber hinaus können Sie einen Ausnahmeschwellenwert festlegen, der zur Berechnung der TDS für jede TDS-Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="cb7ba-109">Gehen Sie folgendermaßen vor, um TDS-Komponenten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="cb7ba-110">Gehen Sie zu **Steuer \> Setup \> Quellensteuer \> Quellensteuerkomponenten**.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="cb7ba-111">[![Seite „Quellensteuerkomponenten“](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="cb7ba-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="cb7ba-112">Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuerkomponenten für den Steuertyp TDS einzurichten.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="cb7ba-113">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="cb7ba-114">Geben Sie im Feld **Quellensteuerkomponente** einen Namen für die TDS-Komponente ein.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="cb7ba-115">Wählen Sie im Feld **Quellensteuerkomponentengruppe** die TDS-Quellensteuerkomponentengruppe aus, mit der die TDS-Komponente verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="cb7ba-116">Geben Sie auf dem Inforegister **Allgemein** im Feld **Beschreibung** eine Beschreibung der TDS-Komponente an.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="cb7ba-117">Wählen Sie im Aktionsbereich die Option **Schwellenwert** aus, um die Seite **Schwellenwert** zu öffnen, damit Sie den Schwellenwert festlegen können, der zur Berechnung des TDS für die TDS-Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="cb7ba-118">Verwenden Sie die Felder **Startdatum** und **Enddatum**, um den Zeitraum festzulegen, für den der Schwellenwert gilt.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="cb7ba-119">Geben Sie im Feld **Allgemein** im Feld **Schwellenwert** den Schwellenwert ein, der zur Berechnung des TDS für die TDS-Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="cb7ba-120">Die Steuer wird an der Quelle erst abgezogen, wenn der kumulierte Rechnungsbetrag den Schwellenwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="cb7ba-121">Wenn der Schwellenwert beispielsweise 10.000 beträgt, wird die TDS berechnet, nachdem der kumulierte Rechnungsbetrag 10.000 überschritten hat (mit anderen Worten, wenn er mindestens 10.001 beträgt).</span><span class="sxs-lookup"><span data-stu-id="cb7ba-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="cb7ba-122">Geben Sie im Feld **Ausnahmeschwellenwert** den Ausnahmeschwellenwert ein, der zur Berechnung des TDS für die TDS-Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="cb7ba-123">Die Steuer für eine Rechnungsposition wird an der Quelle erst abgezogen, wenn der Betrag den Ausnahmeschwellenwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="cb7ba-124">Wenn der Ausnahmeschwellenwert beispielsweise 5.000 beträgt, wird die TDS für eine bestimmte Rechnungsposition berechnet, wenn der Betrag der Rechnungsposition 5.000 überschreitet (mit anderen Worten, wenn er mindestens 5.001 beträgt).</span><span class="sxs-lookup"><span data-stu-id="cb7ba-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="cb7ba-125">[![Seite „Schwellenseite“](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="cb7ba-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb7ba-126">Der Ausnahmeschwellenwert muss kleiner oder gleich dem Schwellenwert sein.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="cb7ba-127">Die Steuer wird für eine Buchung abgezogen, wenn der Buchungsbetrag den Ausnahmeschwellenwert überschreitet, auch wenn der kumulierte Rechnungsbetrag den im Feld **Schwellenwert** angegebenen Schwellenwert nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="cb7ba-128">Schließen Sie die Seite **Schwellenwert**, um zur Seite **Quellensteuerkomponenten** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="cb7ba-129">Wählen Sie im Aktionsbereich **Kopieren** aus, um das Dialogfeld **Quellensteuerkomponenten kopieren** zu öffnen, damit Sie die TDS-Komponenten, die für eine TDS-Komponentengruppe eingerichtet wurden, in eine andere TDS-Komponentengruppe kopieren können.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="cb7ba-130">Wählen Sie im Feld **Von** die TDS-Komponentengruppe aus, aus der die TDS-Komponenten kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="cb7ba-131">Wählen Sie im Feld **Nach** die Quellensteuerkomponentengruppe aus, in die die TDS-Komponenten kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb7ba-132">Gemeinsame TDS-Komponenten, die mit beiden TDS-Komponentengruppen verbunden sind, werden nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="cb7ba-133">Wählen Sie **OK**, um TDS-Komponenten für die andere TDS-Komponentengruppe auf der Seite **Quellensteuerkomponenten** zu kopieren und die erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="cb7ba-134">[![Dialogfeld „Quellensteuerkomponenten kopieren“](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="cb7ba-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="cb7ba-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="cb7ba-135">Close the page.</span></span>
