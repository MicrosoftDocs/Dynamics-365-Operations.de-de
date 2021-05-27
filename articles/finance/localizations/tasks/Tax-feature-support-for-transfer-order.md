---
title: Unterstützung für Steuerfunktionen für Umlagerungsaufträge
description: In diesem Thema wird die neue Steuerfunktionsunterstützung für Umlagerungsaufträge mithilfe des Steuerberechnungsdienstes erläutert.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3a5c2b6fb48d98ba045c77ed034d976f7d89af98
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021368"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="14397-103">Unterstützung für Steuerfunktionen für Umlagerungsaufträge</span><span class="sxs-lookup"><span data-stu-id="14397-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14397-104">Dieses Thema enthält Informationen zur Steuerberechnung und Buchungsintegration in Umlagerungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="14397-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="14397-105">Mit dieser Funktion können Sie die Steuerberechnung und Buchung in Umlagerungsaufträgen für Bestandsübertragungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="14397-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="14397-106">Nach den Bestimmungen der Europäischen Union (EU) zur Mehrwertsteuer (MwSt.) werden Bestandsübertragungen als innergemeinschaftliche Versorgung und innergemeinschaftliche Akquisitionen betrachtet.</span><span class="sxs-lookup"><span data-stu-id="14397-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="14397-107">Um diese Funktionalität zu konfigurieren und zu verwenden, müssen Sie drei Hauptschritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="14397-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="14397-108">**RCS-Einrichtung:** Richten Sie im Regulatory Configuration Service die Steuerfunktion, Steuercodes und die Anwendbarkeit von Steuercodes für die Ermittlung des Steuercodes in Umlagerungsaufträgen ein.</span><span class="sxs-lookup"><span data-stu-id="14397-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="14397-109">**Finance-Einrichtung:** Aktivieren Sie in Microsoft Dynamics 365 Finance die Funktion **Steuer im Umlagerungsauftrag**, richten Sie die Steuerdienstparameter für den Bestand ein und richten Sie die wichtigsten Steuerparameter ein.</span><span class="sxs-lookup"><span data-stu-id="14397-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="14397-110">**Bestandseinrichtung:** Richten Sie die Bestandskonfiguration für Umlagerungsauftragstransaktionen ein.</span><span class="sxs-lookup"><span data-stu-id="14397-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="14397-111">Einrichten von RCS für Steuer- und Umlagerungsauftragstransaktionen</span><span class="sxs-lookup"><span data-stu-id="14397-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="14397-112">Befolgen Sie diese Schritte, um die Steuer einzurichten, die in einem Umlagerungsauftrag enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="14397-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="14397-113">In dem hier gezeigten Beispiel erfolgt der Umlagerungsauftrag von den Niederlanden nach Belgien.</span><span class="sxs-lookup"><span data-stu-id="14397-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="14397-114">Wählen Sie auf der Seite **Steuerliche Merkmale** auf der Registerkarte **Versionen** den Entwurf der Funktionsversion aus und wählen Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="14397-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Auswählen von „Bearbeiten“](../media/tax-feature-support-01.png)

2. <span data-ttu-id="14397-116">Wählen Sie auf der Seite **Einrichtung der Steuerfunktionen** auf der **Steuercode**-Registerkarte **Hinzufügen** aus, um neue Steuercodes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="14397-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="14397-117">In diesem Beispiel werden drei Steuercodes erstellt: **NL-befreit**, **BE-RC-21** und **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="14397-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="14397-118">Wenn ein Umlagerungsauftrag aus einem Lager in den Niederlanden versendet wird, wird der niederländische Steuercode für Mehrwertsteuerbefreiung (**NL-befreit**) angewandt.</span><span class="sxs-lookup"><span data-stu-id="14397-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="14397-119">Erstellen Sie den Steuercode **NL-befreit**.</span><span class="sxs-lookup"><span data-stu-id="14397-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="14397-120">Wählen Sie **Hinzufügen**, geben Sie **NL-befreit** in dem **Steuercode**-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="14397-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="14397-121">Wählen Sie **Nach Nettobetrag** in dem **Steuerkomponente**-Feld.</span><span class="sxs-lookup"><span data-stu-id="14397-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="14397-122">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-122">Select **Save**.</span></span>
        4. <span data-ttu-id="14397-123">Wählen Sie **Hinzufügen** in der **Satz**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14397-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="14397-124">Schalten Sie **Ist befreit** auf **Ja** im Abschnitt **Allgemein** um.</span><span class="sxs-lookup"><span data-stu-id="14397-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Steuerbefreiungscode](../media/tax-feature-support-02.png)

    - <span data-ttu-id="14397-126">Wenn ein Umlagerungsauftrag in einem belgischen Lager eingeht, wird die Verlagerung der Steuerschuld mithilfe der Steuercodes **BE-RC-21** und **BE-RC+21** angewendet.</span><span class="sxs-lookup"><span data-stu-id="14397-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="14397-127">Erstellen Sie den Steuercode **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="14397-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="14397-128">Wählen Sie **Hinzufügen**, geben Sie **BE-RC-21** in dem **Steuercode**-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="14397-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="14397-129">Wählen Sie **Nach Nettobetrag** in dem **Steuerkomponente**-Feld.</span><span class="sxs-lookup"><span data-stu-id="14397-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="14397-130">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-130">Select **Save**.</span></span>
        4. <span data-ttu-id="14397-131">Wählen Sie **Hinzufügen** in der **Satz**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14397-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="14397-132">Geben Sie **-21** im Feld **Steuersatz** ein.</span><span class="sxs-lookup"><span data-stu-id="14397-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="14397-133">Schalten Sie **Ist Verlagerung der Steuerschuld** auf **Ja** im Abschnitt **Allgemein** um.</span><span class="sxs-lookup"><span data-stu-id="14397-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="14397-134">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-134">Select **Save**.</span></span>

        ![BE-RC-21-Steuercode für Verlagerungen der Steuerschuld](../media/tax-feature-support-03.png)
        
        <span data-ttu-id="14397-136">Erstellen Sie den Steuercode **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="14397-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="14397-137">Wählen Sie **Hinzufügen**, geben Sie **BE-RC-21** in dem **Steuercode**-Feld ein.</span><span class="sxs-lookup"><span data-stu-id="14397-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="14397-138">Wählen Sie **Nach Nettobetrag** in dem **Steuerkomponente**-Feld.</span><span class="sxs-lookup"><span data-stu-id="14397-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="14397-139">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-139">Select **Save**.</span></span>
        4. <span data-ttu-id="14397-140">Wählen Sie **Hinzufügen** in der **Satz**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14397-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="14397-141">Geben Sie **21** im Feld **Steuersatz** ein.</span><span class="sxs-lookup"><span data-stu-id="14397-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="14397-142">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-142">Select **Save**.</span></span>

        ![BE-RC+21-Steuercode für Verlagerungen der Steuerschuld](../media/tax-feature-support-04.png)

3. <span data-ttu-id="14397-144">Definieren Sie die Anwendbarkeit der Steuercodes.</span><span class="sxs-lookup"><span data-stu-id="14397-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="14397-145">Wählen Sie **Spalten verwalten** und dann Spalten aus, die zum Erstellen der Anwendbarkeitstabelle verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="14397-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="14397-146">Stellen Sie sicher, dass Sie die Spalten **Geschäftsprozess** und **Steuerarten** zur Tabelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14397-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="14397-147">Beide Spalten sind für die Steuerfunktionalität in Umlagerungsaufträgen von wesentlicher Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="14397-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="14397-148">Fügen Sie Anwendbarkeitsregeln hinzu.</span><span class="sxs-lookup"><span data-stu-id="14397-148">Add applicability rules.</span></span> <span data-ttu-id="14397-149">Lassen Sie nicht die Felder **Steuercode**, **Steuergruppe** und **Artikelsteuergruppe** leer.</span><span class="sxs-lookup"><span data-stu-id="14397-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="14397-150">Fügen Sie eine neue Regel für die Lieferung von Umlagerungsaufträgen hinzu.</span><span class="sxs-lookup"><span data-stu-id="14397-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="14397-151">Wählen Sie **Hinzufügen** in der **Anwendbarkeitsregeln**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14397-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="14397-152">Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus, um die Regel für einen Umlagerungsauftrag anwendbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="14397-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="14397-153">Geben Sie im **Lieferung von Land/Region**-Feld **NLD** ein.</span><span class="sxs-lookup"><span data-stu-id="14397-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="14397-154">Geben Sie im **Lieferung an Land/Region**-Feld **BEL** ein.</span><span class="sxs-lookup"><span data-stu-id="14397-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="14397-155">Wählen Sie im **Steuerart**-Feld **Ausgabe** aus, um die Regel für die Lieferung eines Umlagerungsauftrags anwendbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="14397-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="14397-156">Wählen Sie im **Steuercodes**-Feld **NL-befreit** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="14397-157">Geben Sie im **Steuergruppe**-Feld und in **Artikelsteuergruppe** die zugehörige Mehrwertsteuergruppe und Artikelmehrwertsteuergruppe ein, die in Ihrem Finance-System definiert sind.</span><span class="sxs-lookup"><span data-stu-id="14397-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="14397-158">Fügen Sie eine weitere Regel für den Empfang von Umlagerungsaufträgen hinzu.</span><span class="sxs-lookup"><span data-stu-id="14397-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="14397-159">Wählen Sie **Hinzufügen** in der **Anwendbarkeitsregeln**-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="14397-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="14397-160">Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus, um die Regel für einen Umlagerungsauftrag anwendbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="14397-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="14397-161">Geben Sie im **Lieferung von Land/Region**-Feld **NLD** ein.</span><span class="sxs-lookup"><span data-stu-id="14397-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="14397-162">Geben Sie im **Lieferung an Land/Region**-Feld **BEL** ein.</span><span class="sxs-lookup"><span data-stu-id="14397-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="14397-163">Wählen Sie im **Steuerart**-Feld **Eingabe** aus, um die Regel für den Empfang eines Umlagerungsauftrags anwendbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="14397-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="14397-164">Wählen Sie im **Steuercode**-Feld **BE-RC+21** und **BE-RC-21** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="14397-165">Geben Sie im **Steuergruppe**-Feld und in **Artikelsteuergruppe** die zugehörige Mehrwertsteuergruppe und Artikelmehrwertsteuergruppe ein, die in Ihrem Finance-System definiert sind.</span><span class="sxs-lookup"><span data-stu-id="14397-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Regeln für die Anwendbarkeit](../media/image5.png)

4. <span data-ttu-id="14397-167">Vervollständigen und veröffentlichen Sie die neue Steuerfunktionsversion.</span><span class="sxs-lookup"><span data-stu-id="14397-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="14397-168">[![Ändern des Status der neuen Version](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="14397-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="14397-169">Einrichten von Finance für Umlagerungsauftragstransaktionen</span><span class="sxs-lookup"><span data-stu-id="14397-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="14397-170">Führen Sie folgende Schritte aus, um Steuern für Umlagerungsaufträge zu aktivieren und einzurichten.</span><span class="sxs-lookup"><span data-stu-id="14397-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="14397-171">Wechseln Sie in Finance zu **Arbeitsbereiche** \> **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="14397-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="14397-172">Suchen und wählen Sie in der Liste die Funktion **Steuer im Umlagerungsauftrag** und dann **Jetzt aktivieren** aus, um sie einzuschalten.</span><span class="sxs-lookup"><span data-stu-id="14397-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="14397-173">Die Funktion **Steuer im Umlagerungsauftrag** ist vollständig vom Steuerdienst abhängig.</span><span class="sxs-lookup"><span data-stu-id="14397-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="14397-174">Daher kann es erst aktiviert werden, nachdem Sie den Steuerdienst installiert haben.</span><span class="sxs-lookup"><span data-stu-id="14397-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Funktion „Steuer in Umlagerungsauftrag“](../media/image7.png)

3. <span data-ttu-id="14397-176">Aktivieren Sie den Steuerdienst und wählen Sie den **Bestand**-Geschäftsprozess.</span><span class="sxs-lookup"><span data-stu-id="14397-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="14397-177">Sie müssen diesen Schritt für jede juristische Person in Finance ausführen, für die der Steuerdienst und die Funktionalität für Steuern in Umlagerungsaufträgen verfügbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="14397-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="14397-178">Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Steuerkonfiguration** \> **Steuerdiensteinrichtung**.</span><span class="sxs-lookup"><span data-stu-id="14397-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="14397-179">Wählen Sie im **Geschäftsprozess**-Feld **Bestand** aus.</span><span class="sxs-lookup"><span data-stu-id="14397-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Festlegen des Felds „Geschäftsprozess“](../media/image8.png)

4. <span data-ttu-id="14397-181">Stellen Sie sicher, dass der Mechanismus zur Verlagerung der Steuerschuld eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14397-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="14397-182">Gehen Sie zu **Hauptbuch** \> **Einrichtung** \> **Parameter** und überprüfen Sie dann auf der Registerkarte **Verlagerung der Steuerschuld**, ob die Option **Verlagerung der Steuerschuld aktivieren** auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="14397-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Aktivieren der Option zur Verlagerung der Steuerschuld](../media/image9.png)

5. <span data-ttu-id="14397-184">Stellen Sie sicher, dass die zugehörigen Steuercodes, Steuergruppen, Artikelsteuergruppen und Mehrwertsteuererfassungsnummern in Finance gemäß dem Steuerdienstleitfaden eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="14397-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="14397-185">Richten Sie ein Zwischentransitkonto ein.</span><span class="sxs-lookup"><span data-stu-id="14397-185">Set up an interim transit account.</span></span> <span data-ttu-id="14397-186">Dieser Schritt ist nur erforderlich, wenn die Steuer, die auf einen Umlagerungsauftrag angewendet wird, nicht auf einen Mechanismus für Steuerbefreiung oder Verlagerung der Steuerschuld anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="14397-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="14397-187">Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **Sachkontenbuchungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="14397-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="14397-188">Wählen Sie im Feld **Zwischentransit** ein Sachkonto aus.</span><span class="sxs-lookup"><span data-stu-id="14397-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Auswählen eines Zwischentransitkontos](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="14397-190">Einrichten von Basisbestand für Umlagerungsauftragstransaktionen</span><span class="sxs-lookup"><span data-stu-id="14397-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="14397-191">Befolgen Sie diese Schritte, um den Grundbestand einzurichten und Umlagerungsauftragstransaktionen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="14397-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="14397-192">Erstellen Sie „Lieferung von“- und „Lieferung an“-Sites für Ihre Lager in verschiedenen Ländern oder Regionen und fügen Sie die primäre Adresse für jede Site hinzu.</span><span class="sxs-lookup"><span data-stu-id="14397-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="14397-193">Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerort** \> **Sites**.</span><span class="sxs-lookup"><span data-stu-id="14397-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="14397-194">Wählen Sie **Neu**, um die Site zu erstellen, die Sie später einem Lager zuweisen werden.</span><span class="sxs-lookup"><span data-stu-id="14397-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="14397-195">Wiederholen Sie Schritt 2 für alle anderen Sites, die Sie erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="14397-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14397-196">Eine der von Ihnen erstellten Sites sollte **Transit** benannt werden.</span><span class="sxs-lookup"><span data-stu-id="14397-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="14397-197">In späteren Schritten dieses Verfahrens ordnen Sie diese Site dem Transitlager zu, damit steuerliche Bestandsbelege in „Lieferung“- und „Empfang“-Transaktionen für Umlagerungsaufträge gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="14397-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="14397-198">Die Adresse der Transit-Site spielt für die Steuerberechnung keine Rolle.</span><span class="sxs-lookup"><span data-stu-id="14397-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="14397-199">Sie können es daher leer lassen.</span><span class="sxs-lookup"><span data-stu-id="14397-199">Therefore, you can leave it blank.</span></span>

    ![Einrichten von Sites](../media/image11.png)

2. <span data-ttu-id="14397-201">Erstellen Sie „Lieferung von“-, „Transit“- und „Lieferung an“-Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="14397-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="14397-202">Alle Adressinformationen, die in einem Lagerhaus verwaltet werden, überschreiben die Site-Adresse bei der Steuerberechnung.</span><span class="sxs-lookup"><span data-stu-id="14397-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="14397-203">Wechseln Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerort** \> **Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="14397-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="14397-204">Wählen Sie **Neu**, um einen Lagerort zu erstellen und einer entsprechenden Site zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="14397-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="14397-205">Wiederholen Sie Schritt 2, um nach Bedarf ein Lager für jede Site zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="14397-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Einrichten von Lagerorten](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="14397-207">Für ein „Lieferung von“-Lager muss ein Transitlager im Feld **Transitlager** für Umlagerungsauftragstransaktionen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="14397-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Transitlager auswählen](../media/image13.png)

3. <span data-ttu-id="14397-209">Überprüfen Sie, ob die Bestandsbuchungskonfiguration für Umlagerungsauftragstransaktionen eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14397-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="14397-210">Gehen Sie zu **Bestandsverwaltung** \> **Einrichtung** \> **Buchung** \> **Buchung**.</span><span class="sxs-lookup"><span data-stu-id="14397-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="14397-211">Überprüfen Sie auf der Registerkarte **Bestand**, ob ein Sachkonto für beide Buchungen, **Lagerabgang** und **Lagerzugang**, eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14397-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Einrichten der Lagerabgang- und Lagerzugang-Buchung](../media/image14.png)

    3. <span data-ttu-id="14397-213">Stellen Sie sicher, dass ein Sachkonto für die **Umlagerungszugang**-Buchung eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14397-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Einrichten der Umlagerungszugang-Buchung](../media/image15.png)

    4. <span data-ttu-id="14397-215">Stellen Sie sicher, dass ein Sachkonto für die **Umlagerungsabgang**-Buchung eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="14397-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Einrichten der Umlagerungsabgang-Buchung](../media/image16.png)
