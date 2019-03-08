---
title: Ein Empfehlungssteuerelement des Transaktionsbildschirms auf POS-Geräten
description: In diesem Thema wird beschrieben, wie Sie ein Empfehlungssteuerelement zum Transaktionsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail hinzufügen.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: 213b47422a5e31c2cfc2d173b8c7d9efdecc7568
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320442"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="af337-103">Ein Empfehlungssteuerelement des Transaktionsbildschirms auf POS-Geräten</span><span class="sxs-lookup"><span data-stu-id="af337-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="af337-104">Wir entfernen die aktuelle Version des Produktempfehlungs-Service, da wir für diese Funktion einen besseren Algorithmus und neuere Einzelhandels-ausgerichtete Funktionen neu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="af337-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="af337-105">Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)</span><span class="sxs-lookup"><span data-stu-id="af337-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="af337-106">In diesem Thema wird beschrieben, wie Sie ein Empfehlungssteuerelement zum Transaktionsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="af337-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="af337-107">Sie können Produktempfehlungen zu Ihrem POS-Gerät anzeigen, wenn Sie Microsoft Dynamics 365 for Retail verwenden.</span><span class="sxs-lookup"><span data-stu-id="af337-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="af337-108">*Empfehlungen* sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben.</span><span class="sxs-lookup"><span data-stu-id="af337-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="af337-109">Um Produktempfehlungen anzuzeigen, müssen Sie dem Buchungsbildschirm eine Steuerung mithilfe des Bildschirmlayoutdesigners hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="af337-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="af337-110">Layoutdesigner öffnen</span><span class="sxs-lookup"><span data-stu-id="af337-110">Open Layout designer</span></span>

1. <span data-ttu-id="af337-111">Wechseln Sie zu **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS** &gt; **Bildschirmlayouts**.</span><span class="sxs-lookup"><span data-stu-id="af337-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="af337-112">Suchen Sie mithilfe der Filteroptionen den Bildschirm, dem Sie eine Steuerung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="af337-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="af337-113">Filtern Sie beispielsweise im Feld **Bildschirmlayout-ID** einen Wert von "F2CP16: 9M".</span><span class="sxs-lookup"><span data-stu-id="af337-113">For example, filter on the **Screen layout ID** field using a value of 'F2CP16:9M'.</span></span>
3. <span data-ttu-id="af337-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="af337-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="af337-115">Wählen Sie beispielsweise 'Name: F2CP16: 9M Bildschirmlayout Kennung: F2CP16: 9M'.</span><span class="sxs-lookup"><span data-stu-id="af337-115">For example, select 'Name: F2CP16:9M Screen Layout ID: F2CP16:9M'.</span></span>
4. <span data-ttu-id="af337-116">Klicken Sie auf **Layout-Designer**</span><span class="sxs-lookup"><span data-stu-id="af337-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="af337-117">Folgen Sie den Aufforderungen, um den Layout-Designer zu starten.</span><span class="sxs-lookup"><span data-stu-id="af337-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="af337-118">Wenn Sie aufgefordert werden, die Anmeldeinformationen einzugeben, geben Sie die gleichen Anmeldeinformationen ein, die verwendet wurden, als die Seite **Bildschirmlayouts** ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="af337-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="af337-119">Wenn Sie sich anmelden, erscheint eine Seite, ähnlich jener unten.</span><span class="sxs-lookup"><span data-stu-id="af337-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="af337-120">Das Layout ist verschieden, abhängig von den Anpassungen, die für Ihre Filiale vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="af337-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="af337-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="af337-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="af337-122">Einen Anzeigeoption auswählen</span><span class="sxs-lookup"><span data-stu-id="af337-122">Choose a display option</span></span>

<span data-ttu-id="af337-123">Es stehen zwei Optionen für die Konfiguration zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="af337-123">There are two configurations options available.</span></span> <span data-ttu-id="af337-124">Wählen Sie die Option, die am besten für Ihren Shop passt und folgen Sie den Anweisungen, um die Steueurung eizrichten.</span><span class="sxs-lookup"><span data-stu-id="af337-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="af337-125">Es gibt zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="af337-125">The two options are:</span></span>

- <span data-ttu-id="af337-126">Empfehlungen sind immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af337-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="af337-127">A Registerkarte **Empfehlungen** wird im Gitter auf der rechten Seite des Bildschirms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af337-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="af337-128">Empfehlungen immer sichtbar machen</span><span class="sxs-lookup"><span data-stu-id="af337-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="af337-129">Reduzieren Sie die Höhe des Buchungspositionsdetailbereichs, so dass er die gleiche Höhe hat wie der Debitorenbereich links.</span><span class="sxs-lookup"><span data-stu-id="af337-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="af337-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="af337-130">[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="af337-131">Klicken Sie im Menü auf der linken Seite, und ziehen Sie das Empfehlungssteuerelement zwischen den Buchungspositionsdetailbereich und den Schaltflächenraster im mittleren unteren Transaktlions-Bildschirmrands.</span><span class="sxs-lookup"><span data-stu-id="af337-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="af337-132">Ändern Sie die Steuerung, so dass die Größe in diesen Bereich passt.</span><span class="sxs-lookup"><span data-stu-id="af337-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="af337-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="af337-133">[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="af337-134">Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="af337-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="af337-135">Gehen Sie in Dynamics 365 for Retail zu **Einzelhandel** &gt; **IT für den Einzelhandel** &gt; **Vertriebszeitpläne**.</span><span class="sxs-lookup"><span data-stu-id="af337-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="af337-136">Wählen Sie in der  **1090 Anmelden**</span><span class="sxs-lookup"><span data-stu-id="af337-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="af337-137">Klicken Sie auf **Jetzt ausführen**</span><span class="sxs-lookup"><span data-stu-id="af337-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="af337-138">Eine Registerkarte "Empfehlungen" dem Schaltflächengitter auf der rechten Seite des Bildschirms hinzufügen</span><span class="sxs-lookup"><span data-stu-id="af337-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="af337-139">Machen Sie einen Rechtsklick im Leerraum unter der letzten Registerkarte im Schaltflächenraster auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="af337-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="af337-140"> *\*Anpasse** anklicken.</span><span class="sxs-lookup"><span data-stu-id="af337-140">Click **Customize**.</span></span>

    <span data-ttu-id="af337-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="af337-141">[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="af337-142">Klicken Sie auf **Neue Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="af337-142">Click **New tab**.</span></span>
4. <span data-ttu-id="af337-143">Suchen Sie die neue Registerkarte, die Sie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="af337-143">Find the new tab that you just added.</span></span> <span data-ttu-id="af337-144">Sie müssen möglicherweise einen Bildlauf nach unten machen.</span><span class="sxs-lookup"><span data-stu-id="af337-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="af337-145">Wählen Sie im Dropdown-Menü unter **Inhalte** **Empfohlene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="af337-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="af337-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="af337-146">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="af337-147">Wählen Sie im Feld **Beschriftung** einen Namen für die Registerkarte "Empfehlungen". Zum Beispiel Tpy 'Empfohlene Produkte'.</span><span class="sxs-lookup"><span data-stu-id="af337-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="af337-148">Wählen Sie im Feld **Fild** das Bild, das auf der Registerkarte angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af337-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="af337-149">Auf **OK** klicken.</span><span class="sxs-lookup"><span data-stu-id="af337-149">Click **OK**.</span></span> <span data-ttu-id="af337-150">Die Registerkarte wird im neuen Schaltflächenraster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af337-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="af337-151">Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="af337-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="af337-152">Gehen Sie in Dynamics 365 for Retail zu **Einzelhandel** &gt; **IT für den Einzelhandel** &gt; **Vertriebszeitpläne**.</span><span class="sxs-lookup"><span data-stu-id="af337-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="af337-153">Wählen Sie in der  **1090 Anmelden**</span><span class="sxs-lookup"><span data-stu-id="af337-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="af337-154">Klicken Sie auf **Jetzt ausführen**</span><span class="sxs-lookup"><span data-stu-id="af337-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af337-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af337-155">Additional resources</span></span>

[<span data-ttu-id="af337-156">Personalisierte Produktempfehlungsübersicht</span><span class="sxs-lookup"><span data-stu-id="af337-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
