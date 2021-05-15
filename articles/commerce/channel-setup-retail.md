---
title: Einen Einzelhandelskanal einrichten
description: In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937533"
---
# <a name="set-up-a-retail-channel"></a><span data-ttu-id="70df3-103">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-103">Set up a retail channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70df3-104">In diesem Thema wird beschrieben, wie Sie einen neuen Retail Channel in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="70df3-104">This topic describes how to create a new retail channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="70df3-105">Dynamics 365 Commerce unterstützt mehrere Retail Channels.</span><span class="sxs-lookup"><span data-stu-id="70df3-105">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="70df3-106">Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt).</span><span class="sxs-lookup"><span data-stu-id="70df3-106">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="70df3-107">Jeder Einzelhandelskanal kann seine eigenen Zahlungsmethoden, Preisgruppen, POS-Register, Ein- und Ausgabenkonten und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="70df3-107">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="70df3-108">Sie müssen alle Elemente einrichten, bevor Sie ein Ladengeschäftskanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="70df3-108">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="70df3-109">Stellen Sie vor dem Erstellen eines Retail Channel sicher, dass Sie die folgenden [Kanalvoraussetzungen](channels-prerequisites.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="70df3-109">Before a retail channel is created, ensure you follow the [channel prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-retail-channel"></a><span data-ttu-id="70df3-110">Einen neuen Retail Channel erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="70df3-110">Create and configure a new retail channel</span></span>

1. <span data-ttu-id="70df3-111">Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Geschäfte \>Alle Geschäfte**.</span><span class="sxs-lookup"><span data-stu-id="70df3-111">In the navigation pane, go to **Modules \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="70df3-112">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-112">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70df3-113">Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-113">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="70df3-114">Wählen Sie im Feld **Shopnummer** eine einmalige Shopnummer aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-114">In the **Store number** field, provide a unique store number.</span></span> <span data-ttu-id="70df3-115">Die Nummer kann alphanumerisch mit maximal 10 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="70df3-115">The number can be alphanumeric with a maximum of 10 characters.</span></span>
1. <span data-ttu-id="70df3-116">Geben Sie in der Dropdown-Liste **Juristische Person** die entsprechende juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-116">In the **Legal entity** drop-down list, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="70df3-117">Geben Sie in der Dropdown-Liste **Lagerort** den entsprechenden Lagerort ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-117">In the **Warehouse** drop-down list, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="70df3-118">Wählen Sie im Feld **Zeitzone des Shops** die entsprechende Zeitzone aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="70df3-119">Wählen Sie in der Dropdown-Liste **Umsatzsteuergruppe** eine entsprechende Umsatzsteuergruppe für das Geschäft aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-119">In the **Sales tax group** drop-down list, select an appropriate sales tax group for the store.</span></span>
1. <span data-ttu-id="70df3-120">Wählen Sie im Feld **Währung** die entsprechende Währung aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-120">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="70df3-121">Geben Sie im Feld **Kundenadressbuch** ein gültiges Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="70df3-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="70df3-122">Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.</span><span class="sxs-lookup"><span data-stu-id="70df3-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="70df3-123">Wählen Sie im Feld **Funktionsprofil** gegebenenfalls ein Funktionsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-123">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="70df3-124">Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-124">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="70df3-125">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-125">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="70df3-126">Das folgende Bild zeigt die Erstellung eines neuen Retail Channel.</span><span class="sxs-lookup"><span data-stu-id="70df3-126">The following image shows the creation of a new retail channel.</span></span>

![Neuer Retail Channel](media/channel-setup-retail-1.png)

<span data-ttu-id="70df3-128">Das folgende Bild zeigt ein Beispiel für einen Retail Channel.</span><span class="sxs-lookup"><span data-stu-id="70df3-128">The following image shows an example retail channel.</span></span>

![Beispiel für einen Retail Channel](media/channel-setup-retail-2.png)

## <a name="other-settings"></a><span data-ttu-id="70df3-130">Andere Einstellungen</span><span class="sxs-lookup"><span data-stu-id="70df3-130">Other settings</span></span>

<span data-ttu-id="70df3-131">Es gibt zahlreiche andere optionale Einstellungen, die in den Abschnitten **Auszug/Abschluss** und **Sonstiges** basierend auf den Bedürfnissen des Einzelhandelsgeschäfts eingestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="70df3-131">There are numerous other optional settings that can be set in the **Statement/closing** and **Miscellaneous** sections, based on the needs of the retail store.</span></span>

<span data-ttu-id="70df3-132">Darüber hinaus siehe [Bildschirmlayouts für den Point of Sale (POS)](pos-screen-layouts.md)für Informationen zum Einrichten des Standard-Bildschirmlayouts im Abschnitt **Bildschirmlayout** und [konfigurieren und installieren Sie die Retail Hardware station](retail-hardware-station-configuration-installation.md) für Informationen zum Einrichten über den Abschnitt **Hardwarestationen**.</span><span class="sxs-lookup"><span data-stu-id="70df3-132">In addition, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information on setting up the default screen layout in the **Screen layout** section and [Configure and install Retail hardware station](retail-hardware-station-configuration-installation.md) for setup information about the **Hardware stations** section.</span></span>

<span data-ttu-id="70df3-133">Das folgende Bild zeigt ein Beispiel für einen Retail Channel-Einrichtungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="70df3-133">The following image shows an example retail channel setup configuration.</span></span>

![Retail Channel-Beispielkonfiguration](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a><span data-ttu-id="70df3-135">Einrichtung eines zusätzlichen Kanals</span><span class="sxs-lookup"><span data-stu-id="70df3-135">Additional channel set up</span></span>

<span data-ttu-id="70df3-136">Es gibt zusätzliche Elemente, die für einen Kanal festgelegt werden müssen, die Sie im Aktivitätsbereich unter dem Abschnitt **Einrichten** finden.</span><span class="sxs-lookup"><span data-stu-id="70df3-136">There are additional items that need to be set up for a channel that can be found on the Action Pane under the **Set up** section.</span></span>

<span data-ttu-id="70df3-137">Zusätzliche Aufgaben, die für das Einrichten des Onlinekanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, Bargelddeklaration, Lieferarten, Einnahmen-/Aufwandskonto, Abteilungen, Erfüllungsgruppenzuweisungen und Safes.</span><span class="sxs-lookup"><span data-stu-id="70df3-137">Additional tasks required for online channel setup include setting up payment methods, cash declaration, modes of delivery, income/expense account, sections, the fulfillment group assignment, and safes.</span></span>

<span data-ttu-id="70df3-138">Das folgende Bild zeigt verschiedene zusätzliche Optionen zum Einrichten von Retail Channels auf der Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="70df3-138">The following image shows various additional retail channel setup options on the **Set up** tab.</span></span>

![Kanal einrichten](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="70df3-140">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="70df3-140">Set up payment methods</span></span>

<span data-ttu-id="70df3-141">Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.</span><span class="sxs-lookup"><span data-stu-id="70df3-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="70df3-142">Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und wählen Sie dann **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="70df3-142">On the Action Pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="70df3-143">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70df3-144">Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="70df3-145">Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="70df3-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="70df3-146">Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="70df3-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="70df3-147">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-147">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="70df3-148">Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="70df3-148">The following image shows an example of a cash payment method.</span></span>

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a><span data-ttu-id="70df3-150">Bargelddeklaration einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-150">Set up cash declaration</span></span>

1. <span data-ttu-id="70df3-151">Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und klicken Sie dann auf **Kassenerklärung**.</span><span class="sxs-lookup"><span data-stu-id="70df3-151">On the Action Pane, select the **Set Up** tab, and then select **Cash declaration**.</span></span>
1. <span data-ttu-id="70df3-152">Wählen Sie im Aktivitätsbereich **Neu**, und erstellen Sie dann alle **Münzen** und **Noten**, die in Frage kommen.</span><span class="sxs-lookup"><span data-stu-id="70df3-152">On the Action Pane, select **New**, and then create all **Coin** and **Note** denominations that are applicable.</span></span>

<span data-ttu-id="70df3-153">Das folgende Bild zeigt ein Beispiel für eine Bargelddeklaration.</span><span class="sxs-lookup"><span data-stu-id="70df3-153">The following image shows an example of a cash declaration.</span></span>

![Bargelddeklarationen einrichten](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="70df3-155">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-155">Set up modes of delivery</span></span>

<span data-ttu-id="70df3-156">Sie können die konfigurierten Lieferarten sehen, indem Sie **Lieferarten** auf der Registerkarte **Einrichten** im Aktivitätsbereich auswählen.</span><span class="sxs-lookup"><span data-stu-id="70df3-156">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the Action Pane.</span></span>  

<span data-ttu-id="70df3-157">Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="70df3-157">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="70df3-158">Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.</span><span class="sxs-lookup"><span data-stu-id="70df3-158">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="70df3-159">Wählen Sie im Aktivitätsbereich **Neu**, um eine neue Art der Zustellung zu erstellen, oder wählen Sie eine vorhandene Art aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-159">On the Action Pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="70df3-160">Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="70df3-160">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="70df3-161">Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="70df3-161">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="70df3-162">Das folgende Bild zeigt ein Beispiel für eine Lieferart.</span><span class="sxs-lookup"><span data-stu-id="70df3-162">The following image shows an example of a mode of delivery.</span></span>

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a><span data-ttu-id="70df3-164">Einnahmen-/Aufwandskonto einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-164">Set up income/expense account</span></span>

<span data-ttu-id="70df3-165">Gehen Sie zum Einrichten eines Einnahmen-/Aufwandskontos folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="70df3-165">To set up income/expense account, follow these steps.</span></span>

1. <span data-ttu-id="70df3-166">Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und wählen Sie dann **Einnahme-/Ausgabekonto**.</span><span class="sxs-lookup"><span data-stu-id="70df3-166">On the Action Pane, select the **Set Up** tab, and then select **Income/Expense account**.</span></span>
1. <span data-ttu-id="70df3-167">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-167">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70df3-168">Geben Sie unter **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-168">Under **Name**, enter a name.</span></span>
1. <span data-ttu-id="70df3-169">Geben Sie unter **Suchbegriff** einen Suchbegriff ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-169">Under **Search name**, enter a search name.</span></span>
1. <span data-ttu-id="70df3-170">Geben Sie unter **Kontenart** die Kontenart ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-170">Under **Account type**, enter the account type.</span></span>
1. <span data-ttu-id="70df3-171">Geben Sie den Text für die **Meldungszeile 1**, **Meldungszeile 2**, **Belegtext 1** und **Belegtext 2** ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-171">Enter text for **Message line 1**, **Message line 2**, **Slip text 1**, and **Slip text 2** as needed.</span></span>
1. <span data-ttu-id="70df3-172">Geben Sie unter **Posten** die Buchungsinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-172">Under **Posting**, enter posting information.</span></span>
1. <span data-ttu-id="70df3-173">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-173">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="70df3-174">Die folgende Abbildung zeigt ein Beispiel für ein Einnahmen-/Ausgabenkonto.</span><span class="sxs-lookup"><span data-stu-id="70df3-174">The following image shows an example of an income/expense account.</span></span>

![Einnahmen-/Aufwandskonten einrichten](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a><span data-ttu-id="70df3-176">Abschnitte einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-176">Set up sections</span></span>

<span data-ttu-id="70df3-177">Gehen Sie zum Einrichten von Abschnitten folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="70df3-177">To set up sections, follow these steps.</span></span>

1. <span data-ttu-id="70df3-178">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und klicken Sie auf **Abschnitte**.</span><span class="sxs-lookup"><span data-stu-id="70df3-178">On the Action Pane, select the **Set Up** tab and click **Sections**.</span></span>
1. <span data-ttu-id="70df3-179">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-179">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70df3-180">Geben Sie unter **Abschnittsnummer** eine Abschnittsnummer ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-180">Under **Section number**, enter a section number.</span></span>
1. <span data-ttu-id="70df3-181">Geben Sie unter **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-181">Under **Description**, enter a description.</span></span>
1. <span data-ttu-id="70df3-182">Geben Sie unter **Abschnittsgröße** eine Abschnittsgröße ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-182">Under **Section size**, enter a section size.</span></span>
1. <span data-ttu-id="70df3-183">Konfigurieren Sie zusätzliche Einstellungen für **Allgemeines** und **Verkaufsstatistik**.</span><span class="sxs-lookup"><span data-stu-id="70df3-183">Configure additional settings for **General** and **Sales statistics** as needed.</span></span>
1. <span data-ttu-id="70df3-184">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-184">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="70df3-185">Eine Erfüllungsgruppenzuweisung einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-185">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="70df3-186">Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="70df3-186">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="70df3-187">Wählen Sie im Aktivitätsbereich die Registerkarte **Einrichten** und wählen Sie dann **Erfüllungsgruppenzuordnung**.</span><span class="sxs-lookup"><span data-stu-id="70df3-187">On the Action Pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="70df3-188">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-188">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70df3-189">Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-189">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="70df3-190">Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-190">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="70df3-191">Wählen Sie im Aktivitätsbereich **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="70df3-191">On the Action Pane, select **Save**</span></span>

<span data-ttu-id="70df3-192">Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="70df3-192">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Erfüllungsgruppenzuweisung einrichten](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a><span data-ttu-id="70df3-194">Safes einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-194">Set up safes</span></span>

<span data-ttu-id="70df3-195">Gehen Sie zum Einrichten von Safes folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="70df3-195">To set up safes, follow these steps.</span></span>

1. <span data-ttu-id="70df3-196">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und klicken Sie auf **Sicherheiten**.</span><span class="sxs-lookup"><span data-stu-id="70df3-196">On the Action Pane, select the **Set Up** tab and click **Safes**.</span></span>
1. <span data-ttu-id="70df3-197">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-197">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70df3-198">Geben Sie einen Namen für den Safe ein.</span><span class="sxs-lookup"><span data-stu-id="70df3-198">Enter a name for the safe.</span></span>
1. <span data-ttu-id="70df3-199">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="70df3-199">On the Action Pane, select **Save**.</span></span>

### <a name="ensure-unique-transaction-ids"></a><span data-ttu-id="70df3-200">Stellen Sie eindeutige Transaktions-IDs sicher</span><span class="sxs-lookup"><span data-stu-id="70df3-200">Ensure unique transaction IDs</span></span>

<span data-ttu-id="70df3-201">Ab der Commerce-Version 10.0.18 sind die für den Point of Sale (POS) generierten Transaktions-IDs sequenziell und umfassen die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="70df3-201">As of the Commerce version 10.0.18 , transaction IDs generated for the point of sale (POS) are sequential and include the following parts:</span></span>

- <span data-ttu-id="70df3-202">Ein fester Teil, der eine Verkettung von Filial-ID und Terminal-ID ist.</span><span class="sxs-lookup"><span data-stu-id="70df3-202">A fixed part, which is a concatenation of store ID and terminal ID.</span></span> 
- <span data-ttu-id="70df3-203">Ein sequenzieller Teil, bei dem es sich um eine Sequenz von Zahlen handelt.</span><span class="sxs-lookup"><span data-stu-id="70df3-203">A sequential part, which is a number sequence.</span></span> 

<span data-ttu-id="70df3-204">Konkret lautet das Format *{store}-{terminal}-{numbersequence}*.</span><span class="sxs-lookup"><span data-stu-id="70df3-204">Specifically, the format is *{store}-{terminal}-{numbersequence}*.</span></span> 

<span data-ttu-id="70df3-205">Da Transaktions-IDs im Offline- und Online-Modus erzeugt werden können, gab es Fälle, in denen doppelte Transaktions-IDs erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="70df3-205">Because transaction IDs can be generated in offline and online modes, there have been instances of duplicate transaction IDs being generated.</span></span> <span data-ttu-id="70df3-206">Das Eliminieren von doppelten Transaktions-IDs erfordert eine Menge manueller Datenkorrekturen.</span><span class="sxs-lookup"><span data-stu-id="70df3-206">Eliminating duplicate transaction IDs requires a lot of manual data fixing.</span></span> 

<span data-ttu-id="70df3-207">Mit Commerce Version 10.0.19 wurde das Format der Transaktions-ID aktualisiert, um den sequenziellen Teil zu entfernen und stattdessen eine 13-stellige Nummer zu verwenden, die durch Berechnung der Zeit in Millisekunden seit 1970 erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="70df3-207">With Commerce version 10.0.19, the transaction ID format has been updated to remove the sequential part and instead uses a 13-digit number generated by calculating the time in milliseconds since 1970.</span></span> <span data-ttu-id="70df3-208">Mit dieser Änderung lautet das neue Format der Transaktions-ID *{store}-{terminal}-{millisecondsSince1970}*.</span><span class="sxs-lookup"><span data-stu-id="70df3-208">With this change, the new transaction ID format is *{store}-{terminal}-{millisecondsSince1970}*.</span></span> <span data-ttu-id="70df3-209">Diese Aktualisierung macht die Transaktions-ID nicht-sequentiell und stellt sicher, dass die Transaktions-IDs immer eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="70df3-209">This update makes the transaction ID non-sequential and ensures that transaction IDs are always unique.</span></span> 

> [!NOTE]
> <span data-ttu-id="70df3-210">Transaktions-IDs sind nur für den internen Systemgebrauch gedacht, sie müssen also nicht fortlaufend sein.</span><span class="sxs-lookup"><span data-stu-id="70df3-210">Transaction IDs are meant for internal system use only, so they are not required to be sequential.</span></span> <span data-ttu-id="70df3-211">In vielen Ländern müssen die Beleg-IDs jedoch sequentiell sein.</span><span class="sxs-lookup"><span data-stu-id="70df3-211">However, many countries require receipt IDs to be sequential.</span></span>

<span data-ttu-id="70df3-212">Die neue Funktion für das Format der Transaktions-ID kann im Arbeitsbereich **Funktionsverwaltung** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="70df3-212">The new transaction ID format feature can be enabled from the **Feature management** workspace.</span></span> 

<span data-ttu-id="70df3-213">Um die Verwendung neuer Transaktions-IDs zu aktivieren, führen Sie diese Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="70df3-213">To enable the use of new transaction IDs, follow these steps:</span></span>

1. <span data-ttu-id="70df3-214">Gehen Sie in der Commerce-Zentrale zu **Systemadministration \> Arbeitsbereiche \> Funktionen verwalten**.</span><span class="sxs-lookup"><span data-stu-id="70df3-214">In Commerce headquarters, go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="70df3-215">Filter für das Modul „Retail und Commerce“.</span><span class="sxs-lookup"><span data-stu-id="70df3-215">Filter for the "retail and commerce" module.</span></span>
1. <span data-ttu-id="70df3-216">Suchen Sie nach der Funktion **Neue Transaktions-ID aktivieren, um doppelte Transaktions-IDs zu vermeiden**.</span><span class="sxs-lookup"><span data-stu-id="70df3-216">Search for the **Enable new transaction id to avoid duplicate transaction ids** feature name.</span></span>
1. <span data-ttu-id="70df3-217">Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** im rechten Fensterbereich.</span><span class="sxs-lookup"><span data-stu-id="70df3-217">Select the feature, and then select **Enable Now** in the right pane.</span></span>  
1. <span data-ttu-id="70df3-218">Gehen Sie zu **Einzelhandel und Handel \> Einzelhandel und Handel IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="70df3-218">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="70df3-219">Führen Sie die Jobs **1070 Kanalkonfiguration** und **1170 POS-Datensatz** aus, um die aktivierte Funktion mit den Filialen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="70df3-219">Run the **1070 Channel configuration** and **1170 POS task recorder** jobs to synchronize the enabled feature to the stores.</span></span>
1. <span data-ttu-id="70df3-220">Nachdem die Änderungen an die Filialen gesendet wurden, müssen die POS-Terminals geschlossen und erneut geöffnet werden, um das neue Transaktions-ID-Format zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="70df3-220">After the changes have been sent to the stores, POS terminals must be closed and reopened to use the new transaction ID format.</span></span> 

> [!NOTE]
> <span data-ttu-id="70df3-221">Nachdem die Funktion für das neue Transaktions-ID-Format aktiviert ist, können Sie diese Funktion nicht mehr deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="70df3-221">After the new transaction ID format feature is enabled, you will not be able to disable this feature.</span></span> <span data-ttu-id="70df3-222">Wenn es deaktiviert werden muss, wenden Sie sich bitte an den Commerce Support.</span><span class="sxs-lookup"><span data-stu-id="70df3-222">If it must be disabled, please contact Commerce Support.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70df3-223">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="70df3-223">Additional resources</span></span>

[<span data-ttu-id="70df3-224">Übersicht über Kanäle</span><span class="sxs-lookup"><span data-stu-id="70df3-224">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="70df3-225">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="70df3-225">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="70df3-226">Einen Onlinekanal einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-226">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="70df3-227">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="70df3-227">Set up a call center channel</span></span>](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
