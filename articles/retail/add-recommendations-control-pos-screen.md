---
title: Ein Empfehlungssteuerelement des Transaktionsbildschirms auf POS-Geräten
description: In diesem Thema wird beschrieben, wie Sie ein Empfehlungssteuerelement zum Transaktionsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail hinzufügen.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6f0b75c8d81a5ac6ec90020375aec39120d4406
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811215"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="acff5-103">Ein Empfehlungssteuerelement des Transaktionsbildschirms auf POS-Geräten</span><span class="sxs-lookup"><span data-stu-id="acff5-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="acff5-104">In diesem Thema wird beschrieben, wie Sie ein Empfehlungssteuerelement zum Transaktionsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 Retail hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="acff5-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="acff5-105">Weitere Informationen zu Produktempfehlungsfunktionen finden Sie im [Produktempfehlungsüberblick zur POS-Dokumentation.](product.md).</span><span class="sxs-lookup"><span data-stu-id="acff5-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="acff5-106">Sie können Produktempfehlungen zu Ihrem POS-Gerät anzeigen, wenn Sie Microsoft Dynamics 365 Retail verwenden.</span><span class="sxs-lookup"><span data-stu-id="acff5-106">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="acff5-107">Um Produktempfehlungen anzuzeigen, müssen Sie dem Buchungsbildschirm eine Steuerung mithilfe des Bildschirmlayoutdesigners hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="acff5-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="acff5-108">Layoutdesigner öffnen</span><span class="sxs-lookup"><span data-stu-id="acff5-108">Open Layout designer</span></span>

1. <span data-ttu-id="acff5-109">Wechseln Sie zu **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS** &gt; **Bildschirmlayouts**.</span><span class="sxs-lookup"><span data-stu-id="acff5-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="acff5-110">Suchen Sie mithilfe der Filteroptionen den Bildschirm, dem Sie eine Steuerung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="acff5-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="acff5-111">Filtern Sie beispielsweise im Feld **Bildschirmlayout-ID** mit einem Wert von **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="acff5-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="acff5-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="acff5-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="acff5-113">Wählen Sie beispielsweise **Name: F2CP16: 9M Bildschirmlayout-ID: F2CP16: 9M**.</span><span class="sxs-lookup"><span data-stu-id="acff5-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="acff5-114">Klicken Sie auf **Layout-Designer**</span><span class="sxs-lookup"><span data-stu-id="acff5-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="acff5-115">Folgen Sie den Aufforderungen, um den Layout-Designer zu starten.</span><span class="sxs-lookup"><span data-stu-id="acff5-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="acff5-116">Wenn Sie aufgefordert werden, die Anmeldeinformationen einzugeben, geben Sie die gleichen Anmeldeinformationen ein, die verwendet wurden, als die Seite **Bildschirmlayouts** ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="acff5-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="acff5-117">Wenn Sie sich anmelden, erscheint eine Seite, ähnlich jener unten.</span><span class="sxs-lookup"><span data-stu-id="acff5-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="acff5-118">Das Layout ist verschieden, abhängig von den Anpassungen, die für Ihre Filiale vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="acff5-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="acff5-119">[![Layout-Designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="acff5-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="acff5-120">Einen Anzeigeoption auswählen</span><span class="sxs-lookup"><span data-stu-id="acff5-120">Choose a display option</span></span>

<span data-ttu-id="acff5-121">Es stehen zwei Optionen für die Konfiguration zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="acff5-121">There are two configurations options available.</span></span> <span data-ttu-id="acff5-122">Wählen Sie die Option, die am besten für Ihren Shop passt und folgen Sie den Anweisungen, um die Steueurung eizrichten.</span><span class="sxs-lookup"><span data-stu-id="acff5-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="acff5-123">Es gibt zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="acff5-123">The two options are:</span></span>

- <span data-ttu-id="acff5-124">Empfehlungen sind immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="acff5-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="acff5-125">A Registerkarte **Empfehlungen** wird im Gitter auf der rechten Seite des Bildschirms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="acff5-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="acff5-126">Empfehlungen immer sichtbar machen</span><span class="sxs-lookup"><span data-stu-id="acff5-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="acff5-127">Reduzieren Sie die Höhe des Buchungspositionsdetailbereichs, so dass er die gleiche Höhe hat wie der Debitorenbereich links.</span><span class="sxs-lookup"><span data-stu-id="acff5-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="acff5-128">[![Höhe des Buchungspositionsdetail-Bereichs reduziert](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="acff5-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="acff5-129">Klicken Sie im Menü auf der linken Seite, und ziehen Sie das Empfehlungssteuerelement zwischen den Buchungspositionsdetailbereich und den Schaltflächenraster im mittleren unteren Transaktlions-Bildschirmrands.</span><span class="sxs-lookup"><span data-stu-id="acff5-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="acff5-130">Ändern Sie die Steuerung, so dass die Größe in diesen Bereich passt.</span><span class="sxs-lookup"><span data-stu-id="acff5-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="acff5-131">[![Empfehlungssteuerelement dem Layout hinzugefügt](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="acff5-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="acff5-132">Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="acff5-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="acff5-133">Gehen Sie in Dynamics 365 for Retail zu **Einzelhandel** &gt; **IT für den Einzelhandel** &gt; **Vertriebszeitpläne**.</span><span class="sxs-lookup"><span data-stu-id="acff5-133">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="acff5-134">Wählen Sie in der **1090 Anmelden**</span><span class="sxs-lookup"><span data-stu-id="acff5-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="acff5-135">Klicken Sie auf **Jetzt ausführen**</span><span class="sxs-lookup"><span data-stu-id="acff5-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="acff5-136">Eine Registerkarte "Empfehlungen" dem Schaltflächengitter auf der rechten Seite des Bildschirms hinzufügen</span><span class="sxs-lookup"><span data-stu-id="acff5-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="acff5-137">Machen Sie einen Rechtsklick im Leerraum unter der letzten Registerkarte im Schaltflächenraster auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="acff5-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="acff5-138">Klicken Sie auf **Anpassen**.</span><span class="sxs-lookup"><span data-stu-id="acff5-138">Click **Customize**.</span></span>

    <span data-ttu-id="acff5-139">[![Anpassung – Registerkartensteuerelement-Dialogfeld](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="acff5-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="acff5-140">Klicken Sie auf **Neue Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="acff5-140">Click **New tab**.</span></span>
4. <span data-ttu-id="acff5-141">Suchen Sie die neue Registerkarte, die Sie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="acff5-141">Find the new tab that you just added.</span></span> <span data-ttu-id="acff5-142">Sie müssen möglicherweise einen Bildlauf nach unten machen.</span><span class="sxs-lookup"><span data-stu-id="acff5-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="acff5-143">Wählen Sie im Dropdown-Menü unter **Inhalte** **Empfohlene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="acff5-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="acff5-144">[![Auswählen empfohlener Produkte im Feld „Inhalte“](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="acff5-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="acff5-145">Wählen Sie im Feld **Beschriftung** einen Namen für die Registerkarte "Empfehlungen". Zum Beispiel Tpy 'Empfohlene Produkte'.</span><span class="sxs-lookup"><span data-stu-id="acff5-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="acff5-146">Wählen Sie im Feld **Fild** das Bild, das auf der Registerkarte angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="acff5-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="acff5-147">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="acff5-147">Click **OK**.</span></span> <span data-ttu-id="acff5-148">Die Registerkarte wird im neuen Schaltflächenraster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="acff5-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="acff5-149">Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="acff5-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="acff5-150">Gehen Sie in Dynamics 365 for Retail zu **Einzelhandel** &gt; **IT für den Einzelhandel** &gt; **Vertriebszeitpläne**.</span><span class="sxs-lookup"><span data-stu-id="acff5-150">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="acff5-151">Wählen Sie in der **1090 Anmelden**</span><span class="sxs-lookup"><span data-stu-id="acff5-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="acff5-152">Klicken Sie auf **Jetzt ausführen**</span><span class="sxs-lookup"><span data-stu-id="acff5-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acff5-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="acff5-153">Additional resources</span></span>

[<span data-ttu-id="acff5-154">Produktempfehlungen im POS</span><span class="sxs-lookup"><span data-stu-id="acff5-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="acff5-155">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="acff5-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
