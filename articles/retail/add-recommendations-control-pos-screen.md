---
title: "Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät"
description: "In diesem Thema wird beschrieben, wie Sie einem Empfehlungssteuerelement dem Buchungsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail Arbeitsgänge hinzufügen."
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7d1e5392e4d3fa86bf62943cb4f5b5f4c7b383
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="584c6-103">Hinzufügen eines Empfehlungssteuerelement der Buchungsseite auf einem POS-Gerät</span><span class="sxs-lookup"><span data-stu-id="584c6-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!INCLUDE [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="584c6-104">Wir entfernen die aktuelle Version des Produktempfehlungs-Service, da wir für diese Funktion einen besseren Algorithmus und neuere Einzelhandels-ausgerichtete Funktionen neu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="584c6-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="584c6-105">Weitere Informationen finden Sie unter [Entfernte oder veraltete Funktionen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features)</span><span class="sxs-lookup"><span data-stu-id="584c6-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="584c6-106">In diesem Thema wird beschrieben, wie Sie einem Empfehlungssteuerelement dem Buchungsbildschirm auf einem Verkaufsstelle (POS)-Gerät mithilfe des Bildschirmlayoutdesigners in Microsoft Dynamics 365 for Retail Arbeitsgänge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="584c6-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="584c6-107">Sie können Produktempfehlungen zu Ihrem POS-Gerät anzeigen, wenn Sie Microsoft Dynamics 365 for Retail verwenden.</span><span class="sxs-lookup"><span data-stu-id="584c6-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="584c6-108">*Empfehlungen* sind Artikel, die Ihre Kunden möglicherweise interessieren und zwar auf Basis der ihrer Einkaufshistorie, Artikel auf einem Wunschzettel und Artikel, die andere Kunden online und in der physische Filiale gekauft haben.</span><span class="sxs-lookup"><span data-stu-id="584c6-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="584c6-109">Um Produktempfehlungen anzuzeigen, müssen Sie dem Buchungsbildschirm eine Steuerung mithilfe des Bildschirmlayoutdesigners hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="584c6-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="584c6-110">Layoutdesigner öffnen</span><span class="sxs-lookup"><span data-stu-id="584c6-110">Open Layout designer</span></span>
1.  <span data-ttu-id="584c6-111">Wechseln Sie zu **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS** &gt; **Bildschirmlayouts**.</span><span class="sxs-lookup"><span data-stu-id="584c6-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="584c6-112">Suchen Sie mithilfe der Filteroptionen den Bildschirm, dem Sie eine Steuerung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="584c6-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="584c6-113">Filtern Sie beispielsweise im Feld **Bildschirmlayout-ID** einen Wert von "F2CP16: 9M".</span><span class="sxs-lookup"><span data-stu-id="584c6-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="584c6-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="584c6-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="584c6-115">Wählen Sie beispielsweise "Name: F2CP16: 9M Bildschirmlayout Kennung: F2CP16: 9M".</span><span class="sxs-lookup"><span data-stu-id="584c6-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="584c6-116">Klicken Sie auf **Layout-Designer**</span><span class="sxs-lookup"><span data-stu-id="584c6-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="584c6-117">Folgen Sie den Aufforderungen, um den Layout-Designer zu starten.</span><span class="sxs-lookup"><span data-stu-id="584c6-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="584c6-118">Wenn Sie aufgefordert werden, die Anmeldeinformationen einzugeben, geben Sie die gleichen Anmeldeinformationen ein, die verwendet wurden, als die Seite **Bildschirmlayouts** ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="584c6-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="584c6-119">Wenn Sie sich anmelden, erscheint eine Seite, ähnlich jener unten.</span><span class="sxs-lookup"><span data-stu-id="584c6-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="584c6-120">Das Layout ist verschieden, abhängig von den Anpassungen, die für Ihre Filiale vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="584c6-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="584c6-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Wählen eine Anzeigeoption aus</span><span class="sxs-lookup"><span data-stu-id="584c6-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="584c6-122">Es stehen zwei Optionen für die Konfiguration zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="584c6-122">There are two configurations options available.</span></span> <span data-ttu-id="584c6-123">Wählen Sie die Option, die am besten für Ihren Shop passt und folgen Sie den Anweisungen, um die Steueurung eizrichten.</span><span class="sxs-lookup"><span data-stu-id="584c6-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="584c6-124">Es gibt zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="584c6-124">The two options are:</span></span>
-   <span data-ttu-id="584c6-125">Empfehlungen sind immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="584c6-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="584c6-126">A Registerkarte **Empfehlungen** wird im Gitter auf der rechten Seite des Bildschirms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="584c6-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="584c6-127">Um Empfehlungen immer anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="584c6-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="584c6-128">Reduzieren Sie die Höhe des Buchungspositionsdetailbereichs, so dass er die gleiche Höhe hat wie der Debitorenbereich links.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="584c6-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="584c6-129">Klicken Sie im Menü auf der linken Seite, und ziehen Sie das Empfehlungssteuerelement zwischen den Buchungspositionsdetailbereich und den Schaltflächenraster im mittleren unteren Transaktlions-Bildschirmrands.</span><span class="sxs-lookup"><span data-stu-id="584c6-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="584c6-130">Ändern Sie die Steuerung, so dass die Größe in diesen Bereich passt.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="584c6-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="584c6-131">Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="584c6-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="584c6-132">In Dynamics 365 for Retail gehen Sie zu **Einzelhandel** &gt; **Einzelhandel IT** &gt; **Verteilungszeitpläne** .</span><span class="sxs-lookup"><span data-stu-id="584c6-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="584c6-133">Wählen Sie in der **1090 Anmelden**</span><span class="sxs-lookup"><span data-stu-id="584c6-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="584c6-134">Klicken Sie auf **Jetzt ausführen**</span><span class="sxs-lookup"><span data-stu-id="584c6-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="584c6-135">Um eine Registerkarte "Empfehlungen" dem Schaltflächengitter auf der rechten Seite des Bildschirms hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="584c6-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="584c6-136">Machen Sie einen Rechtsklick im Leerraum unter der letzten Registerkarte im Schaltflächenraster auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="584c6-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="584c6-137">Klicken Sie auf **Anpassen**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="584c6-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="584c6-138">Klicken Sie auf **Neue Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="584c6-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="584c6-139">Suchen Sie die neue Registerkarte, die Sie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="584c6-139">Find the new tab that you just added.</span></span> <span data-ttu-id="584c6-140">Sie müssen möglicherweise einen Bildlauf nach unten machen.</span><span class="sxs-lookup"><span data-stu-id="584c6-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="584c6-141">Wählen Sie im Dropdown-Menü unter **Inhalte** **Empfohlene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="584c6-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="584c6-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="584c6-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="584c6-143">Wählen Sie im Feld **Beschriftung** einen Namen für die Registerkarte "Empfehlungen". Zum Beispiel Tpy "Empfohlene Produkte".</span><span class="sxs-lookup"><span data-stu-id="584c6-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="584c6-144">Wählen Sie im Feld **Fild** das Bild, das auf der Registerkarte angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="584c6-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="584c6-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="584c6-145">Click **OK**.</span></span> <span data-ttu-id="584c6-146">Die Registerkarte wird im neuen Schaltflächenraster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="584c6-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="584c6-147">Klicken Sie auf **X**, um zu speichern und den Layout-Designer zu beenden.</span><span class="sxs-lookup"><span data-stu-id="584c6-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="584c6-148">In Dynamics 365 for Retail gehen Sie zu **Einzelhandel** &gt; **Einzelhandel IT** &gt; **Verteilungszeitpläne** .</span><span class="sxs-lookup"><span data-stu-id="584c6-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="584c6-149">Wählen Sie in der **1090 Anmelden**</span><span class="sxs-lookup"><span data-stu-id="584c6-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="584c6-150">Klicken Sie auf **Jetzt ausführen**</span><span class="sxs-lookup"><span data-stu-id="584c6-150">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="584c6-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="584c6-151">See also</span></span>
--------

[<span data-ttu-id="584c6-152">Personalisierte Produktempfehlungen, Übersicht</span><span class="sxs-lookup"><span data-stu-id="584c6-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




