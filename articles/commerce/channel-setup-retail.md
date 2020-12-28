---
title: Einen Einzelhandelskanal einrichten
description: In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412527"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="b4887-103">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-103">Set up a retail channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b4887-104">In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="b4887-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4887-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b4887-105">Overview</span></span>

<span data-ttu-id="b4887-106">Dynamics 365 Commerce unterstützt mehrere Retail Channels.</span><span class="sxs-lookup"><span data-stu-id="b4887-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="b4887-107">Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt).</span><span class="sxs-lookup"><span data-stu-id="b4887-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="b4887-108">Jeder Einzelhandelskanal kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="b4887-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="b4887-109">Sie müssen alle Elemente einrichten, bevor Sie ein Ladengeschäftskanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b4887-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="b4887-110">Stellen Sie vor dem Erstellen eines Retail Channel sicher, dass Sie die folgenden [Kanalvoraussetzungen](channels-prerequisites.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="b4887-110">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="b4887-111">Einen neuen Retail Channel erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b4887-111">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="b4887-112">Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Geschäfte \>Alle Geschäfte**.</span><span class="sxs-lookup"><span data-stu-id="b4887-112">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="b4887-113">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4887-114">Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="b4887-115">Wählen Sie im Feld **Shopnummer** eine einmalige Shopnummer aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-115">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="b4887-116">Die Nummer kann alphanumerisch mit maximal 10 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="b4887-116">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="b4887-117">Geben Sie in der Dropdown-Liste **Juristische Person** die entsprechende juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-117">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="b4887-118">Geben Sie in der Dropdown-Liste **Lagerort** den entsprechenden Lagerort ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-118">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="b4887-119">Wählen Sie im Feld **Zeitzone des Shops** die entsprechende Zeitzone aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-119">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="b4887-120">Wählen Sie in der Dropdown-Liste **Umsatzsteuergruppe** eine entsprechende Umsatzsteuergruppe für das Geschäft aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-120">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="b4887-121">Wählen Sie im Feld **Währung** die entsprechende Währung aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="b4887-122">Geben Sie im Feld **Kundenadressbuch** ein gültiges Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="b4887-122">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="b4887-123">Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.</span><span class="sxs-lookup"><span data-stu-id="b4887-123">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="b4887-124">Wählen Sie im Feld **Funktionsprofil** gegebenenfalls ein Funktionsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="b4887-125">Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="b4887-126">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b4887-127">Das folgende Bild zeigt die Erstellung eines neuen Retail Channel.</span><span class="sxs-lookup"><span data-stu-id="b4887-127">The following image shows the creation of a new retail channel.</span></span>

![Neuer Retail Channel](media/channel-setup-retail-1.png)

<span data-ttu-id="b4887-129">Das folgende Bild zeigt ein Beispiel für einen Retail Channel.</span><span class="sxs-lookup"><span data-stu-id="b4887-129">The following image shows an example retail channel.</span></span>

![Beispiel für einen Retail Channel](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="b4887-131">Andere Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b4887-131">Other settings</span></span>

<span data-ttu-id="b4887-132">Es gibt zahlreiche andere optionale Einstellungen, die in den Abschnitten **Auszug/Abschluss** und **Sonstiges** basierend auf den Bedürfnissen des Einzelhandelsgeschäfts eingestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="b4887-132">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="b4887-133">Darüber hinaus siehe [Bildschirmlayouts für den Point of Sale (POS)](pos-screen-layouts.md)für Informationen zum Einrichten des Standard-Bildschirmlayouts im Abschnitt **Bildschirmlayout** und [konfigurieren und installieren Sie die Retail Hardware station](retail-hardware-station-configuration-installation.md) für Informationen zum Einrichten über den Abschnitt **Hardwarestationen**.</span><span class="sxs-lookup"><span data-stu-id="b4887-133">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="b4887-134">Das folgende Bild zeigt ein Beispiel für einen Retail Channel-Einrichtungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b4887-134">The following image shows an example retail channel setup configuration.</span></span>

![Retail Channel-Beispielkonfiguration](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="b4887-136">Einrichtung eines zusätzlichen Kanals</span><span class="sxs-lookup"><span data-stu-id="b4887-136">Additional channel set up</span></span>

<span data-ttu-id="b4887-137">Für einen Kanal, der im **Aktionsbereich** im Abschnitt **Einrichtung** zu finden ist, müssen zusätzliche Elemente eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b4887-137">There are additional items that need to be set up for a channel that can be found on the **Action pane** under the **Set up** section.</span></span>

<span data-ttu-id="b4887-138">Zusätzliche Aufgaben, die für das Einrichten des Onlinekanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, Bargelddeklaration, Lieferarten, Einnahmen-/Aufwandskonto, Abteilungen, Erfüllungsgruppenzuweisungen und Safes.</span><span class="sxs-lookup"><span data-stu-id="b4887-138">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="b4887-139">Das folgende Bild zeigt verschiedene zusätzliche Optionen zum Einrichten von Retail Channels auf der Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="b4887-139">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanal einrichten](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="b4887-141">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="b4887-141">Set up payment methods</span></span>

<span data-ttu-id="b4887-142">Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b4887-142">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="b4887-143">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="b4887-143">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="b4887-144">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-144">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4887-145">Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-145">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="b4887-146">Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b4887-146">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="b4887-147">Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="b4887-147">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="b4887-148">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b4887-149">Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="b4887-149">The following image shows an example of a cash payment method.</span></span>

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="b4887-151">Bargelddeklaration einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-151">Set up cash declaration</span></span>

1. <span data-ttu-id="b4887-152">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Bargelddeklaration**.</span><span class="sxs-lookup"><span data-stu-id="b4887-152">On the action pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="b4887-153">Wählen Sie im Aktionsbereich **Neu** aus und erstellen Sie dann alle zutreffenden Denominationen **Münze** und **Hinweis**.</span><span class="sxs-lookup"><span data-stu-id="b4887-153">On the action pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="b4887-154">Das folgende Bild zeigt ein Beispiel für eine Bargelddeklaration.</span><span class="sxs-lookup"><span data-stu-id="b4887-154">The following image shows an example of a cash declaration.</span></span>

![Bargelddeklarationen einrichten](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="b4887-156">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-156">Set up modes of delivery</span></span>

<span data-ttu-id="b4887-157">Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b4887-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="b4887-158">Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b4887-158">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="b4887-159">Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.</span><span class="sxs-lookup"><span data-stu-id="b4887-159">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="b4887-160">Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="b4887-161">Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b4887-161">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="b4887-162">Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b4887-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="b4887-163">Das folgende Bild zeigt ein Beispiel für eine Lieferart.</span><span class="sxs-lookup"><span data-stu-id="b4887-163">The following image shows an example of a mode of delivery.</span></span>

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="b4887-165">Einnahmen-/Aufwandskonto einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-165">Set up income/expense account</span></span>

<span data-ttu-id="b4887-166">Gehen Sie zum Einrichten eines Einnahmen-/Aufwandskontos folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="b4887-166">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="b4887-167">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Einnahmen-/Aufwandskonto**.</span><span class="sxs-lookup"><span data-stu-id="b4887-167">On the action pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="b4887-168">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-168">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4887-169">Geben Sie unter **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-169">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="b4887-170">Geben Sie unter **Suchbegriff** einen Suchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-170">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="b4887-171">Geben Sie unter **Kontenart** die Kontenart ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-171">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="b4887-172">Geben Sie den Text für die **Meldungszeile 1**, **Meldungszeile 2**, **Belegtext 1** und **Belegtext 2** ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-172">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="b4887-173">Geben Sie unter **Posten** die Buchungsinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-173">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="b4887-174">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-174">On the action pane, select **Save**.</span></span>

<span data-ttu-id="b4887-175">Die folgende Abbildung zeigt ein Beispiel für ein Einnahmen-/Ausgabenkonto.</span><span class="sxs-lookup"><span data-stu-id="b4887-175">The following image shows an example of an income/expense account.</span></span>

![Einnahmen-/Aufwandskonten einrichten](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="b4887-177">Abschnitte einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-177">Set up sections</span></span>

<span data-ttu-id="b4887-178">Gehen Sie zum Einrichten von Abschnitten folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="b4887-178">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="b4887-179">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** aus und klicken Sie dann auf **Abschnitte**.</span><span class="sxs-lookup"><span data-stu-id="b4887-179">On the action pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="b4887-180">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-180">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4887-181">Geben Sie unter **Abschnittsnummer** eine Abschnittsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-181">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="b4887-182">Geben Sie unter **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-182">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="b4887-183">Geben Sie unter **Abschnittsgröße** eine Abschnittsgröße ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-183">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="b4887-184">Konfigurieren Sie zusätzliche Einstellungen für **Allgemeines** und **Verkaufsstatistik**.</span><span class="sxs-lookup"><span data-stu-id="b4887-184">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="b4887-185">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-185">On the action pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="b4887-186">Eine Erfüllungsgruppenzuweisung einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-186">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="b4887-187">Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="b4887-187">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="b4887-188">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Erfüllungsgruppenzuweisung** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-188">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="b4887-189">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-189">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4887-190">Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-190">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="b4887-191">Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-191">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="b4887-192">Wählen Sie im Aktionsbereich **Speichern** aus</span><span class="sxs-lookup"><span data-stu-id="b4887-192">On the action pane, select **Save**</span></span>

<span data-ttu-id="b4887-193">Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="b4887-193">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Erfüllungsgruppenzuweisung einrichten](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="b4887-195">Safes einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-195">Set up safes</span></span>

<span data-ttu-id="b4887-196">Gehen Sie zum Einrichten von Safes folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="b4887-196">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="b4887-197">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** aus und klicken Sie dann auf **Safes**.</span><span class="sxs-lookup"><span data-stu-id="b4887-197">On the action pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="b4887-198">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-198">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b4887-199">Geben Sie einen Namen für den Safe ein.</span><span class="sxs-lookup"><span data-stu-id="b4887-199">Enter a name for the safe.</span></span>
1. <span data-ttu-id="b4887-200">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="b4887-200">On the action pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4887-201">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4887-201">Additional resources</span></span>

[<span data-ttu-id="b4887-202">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="b4887-202">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="b4887-203">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="b4887-203">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="b4887-204">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-204">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="b4887-205">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="b4887-205">Set up a call center channel</span></span>](channel-setup-callcenter.md)

