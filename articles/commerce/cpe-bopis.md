---
title: BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren
description: In diesem Thema wird erläutert, wie Sie den Online-Kauf und die Abholung im Geschäft (BOPIS) in einer Microsoft Dynamics 365 Commerce-Evaluierungsumgebung konfigurieren, nachdem sie bereitgestellt wurde.
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 219504da62fd4637ed01f9acbab32f873cef81b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795954"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="048a9-103">BOPIS in einer Dynamics 365 Commerce-Evaluierungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="048a9-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="048a9-104">In diesem Thema wird erläutert, wie Sie den Online-Kauf und die Abholung im Geschäft (BOPIS) in einer Microsoft Dynamics 365 Commerce-Evaluierungsumgebung konfigurieren, nachdem sie bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="048a9-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="048a9-105">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="048a9-105">Prerequisite</span></span>

<span data-ttu-id="048a9-106">Führen Sie die in diesem Thema beschriebenen Prozeduren erst aus, nachdem Ihre Commerce-Auswertungsumgebung bereitgestellt und konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="048a9-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="048a9-107">Informationen zum Bereitstellen und Konfigurieren Ihrer Umgebung finden Sie unter [Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung](provisioning-guide.md) und [Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="048a9-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="048a9-108">Nachdem Ihre Commerce-Umgebung komplett bereitgestellt und konfiguriert wurde, können Sie dieses Thema verwenden, um BOPIS-Szenarien zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="048a9-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="048a9-109">POS konfigurieren</span><span class="sxs-lookup"><span data-stu-id="048a9-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="048a9-110">Modern POS konfigurieren</span><span class="sxs-lookup"><span data-stu-id="048a9-110">Configure Modern POS</span></span>

<span data-ttu-id="048a9-111">Für BOPIS-Szenarien mit Kreditkartenzahlung ist eine Hardwarestation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="048a9-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="048a9-112">Die Hardwarestation ist in die Modern POS-Programme für Windows- und Android-Clients integriert.</span><span class="sxs-lookup"><span data-stu-id="048a9-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="048a9-113">Wenn Sie Cloud POS oder Modern POS für iOS verwenden, muss der POS-Client (Point of Sale) mit einer gemeinsam genutzten Hardwarestation gekoppelt sein.</span><span class="sxs-lookup"><span data-stu-id="048a9-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="048a9-114">In diesem Thema wird erläutert, wie Sie BOPIS für Windows- und Android-Clients konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="048a9-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="048a9-115">Weitere Informationen zur Installation einer geteilten Hardware-Station finden Sie unter [Konfiguration und Installation der Retail-Hardware-Station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="048a9-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="048a9-116">Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> POS-Einstellungen \> Kassen**.</span><span class="sxs-lookup"><span data-stu-id="048a9-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="048a9-117">Wählen Sie Kasse **SANFRAN-5** und dann **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="048a9-118">Ändern Sie den Wert im Feld **Hardwareprofil** von **HW002** in **HW001** und wählen dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="048a9-119">Um die Änderungen z synchronisieren, wechseln Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="048a9-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="048a9-120">Wählen Sie den Vertriebsplan **1090** und wählen Sie dann im Aktionsbereich **Jetzt ausführen**.</span><span class="sxs-lookup"><span data-stu-id="048a9-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="048a9-121">Wählen Sie **Ja** und dann **OK**, um die Datensynchronisation zu starten.</span><span class="sxs-lookup"><span data-stu-id="048a9-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="048a9-122">Modern POS installieren</span><span class="sxs-lookup"><span data-stu-id="048a9-122">Install Modern POS</span></span>

1. <span data-ttu-id="048a9-123">Wechseln Sie zu **Einzelhandel und Handel \> Kanaleinstellungen \> POS-Einstellungen \> Geräte**.</span><span class="sxs-lookup"><span data-stu-id="048a9-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="048a9-124">Wählen Sie Gerät **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="048a9-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="048a9-125">Wählen Sie im Aktionsbereich **Herunterladen** aus, und wählen Sie dann **Konfigurationsdatei** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="048a9-126">Wählen Sie zunächst **Herunterladen** und dann **Retail Modern POS** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="048a9-127">Nach Download der **ModernPOSSetup.exe**-Datei wählen Sie **Datei öffnen**.</span><span class="sxs-lookup"><span data-stu-id="048a9-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Datei öffnen](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="048a9-129">Wählen Sie **Weiter**, um den Installationsprozess zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="048a9-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="048a9-130">Wenn die Installation abgeschlossen ist, wählen Sie **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="048a9-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="048a9-131">Aktivieren Sie Modern POS</span><span class="sxs-lookup"><span data-stu-id="048a9-131">Activate Modern POS</span></span>

1. <span data-ttu-id="048a9-132">Wählen Sie auf dem Windows-Desktop die Option **Start** und geben Sie **Retail Modern POS** ein.</span><span class="sxs-lookup"><span data-stu-id="048a9-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="048a9-133">Wählen Sie die **Retail Modern POS**-Anwendung, um die Aktivierung zu starten.</span><span class="sxs-lookup"><span data-stu-id="048a9-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="048a9-134">Wählen Sie **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="048a9-134">Select **Next**.</span></span> <span data-ttu-id="048a9-135">Die Felder **Server-URL**, **Geräte ID** und **Registriernummer** sollten mithilfe von Informationen aus der Konfigurationsdatei voreingestellt werden, die Sie im vorherigen Verfahren heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="048a9-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="048a9-136">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-136">Select **Activate**.</span></span>
5. <span data-ttu-id="048a9-137">Ein Authentifizierungsdialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048a9-137">An authentication dialog box appears.</span></span> <span data-ttu-id="048a9-138">Wählen Sie das Konto aus, das die E-Mail-Adresse verwendet, die zuvor dem Mitarbeiter **000713 – Andrew Collette** zugeordnet war.</span><span class="sxs-lookup"><span data-stu-id="048a9-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="048a9-139">Wenn Sie noch keinen Mitarbeiter mit Ihrer Identität verknüpft haben, ist die Aktivierung nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="048a9-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="048a9-140">Befolgen Sie in diesem Fall die Schritte im Abschnitt „Mitarbeiter Ihrer Identität zuordnen“ im Thema [Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="048a9-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="048a9-141">Wenn Sie aufgefordert werden, das Gerät von Ihrer Organisation verwalten zu lassen, wählen Sie **Nur diese App**.</span><span class="sxs-lookup"><span data-stu-id="048a9-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="048a9-142">Wenn die Aktivierung abgeschlossen ist, wählen Sie **Erste Schritte**.</span><span class="sxs-lookup"><span data-stu-id="048a9-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="048a9-143">Aktivieren Sie BOPIS in Modern POS</span><span class="sxs-lookup"><span data-stu-id="048a9-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="048a9-144">Melden Sie sich mit **000713** als Bediener-ID und **123** als Passwort bei Modern POS an.</span><span class="sxs-lookup"><span data-stu-id="048a9-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="048a9-145">Aktivieren Sie während der Wiedergabe des Einführungsvideos die beiden Kontrollkästchen in der unteren linken Ecke des Dialogfelds und schließen Sie das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="048a9-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="048a9-146">Wenn Sie nicht aufgefordert werden, die Schicht zu schließen, scrollen Sie auf der Seite **Willkommen bei** nach rechts, wählen **Schicht schließen** und melden Sie sich dann wieder am POS an.</span><span class="sxs-lookup"><span data-stu-id="048a9-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="048a9-147">Wenn Sie nach dem Anmelden aufgefordert werden, wählen Sie **Ausführen von Vorgängen ohne Kassenlade**.</span><span class="sxs-lookup"><span data-stu-id="048a9-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="048a9-148">Auf der Seite **Willkommen bei** scrollen Sie nach rechts und wählen den Vorgang **Hardwarestation auswählen**.</span><span class="sxs-lookup"><span data-stu-id="048a9-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="048a9-149">Wählen Sie **Verwalten**, stellen Sie die **Hardwarestation verwenden**-Option auf **Ein** ein und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="048a9-150">Melden Sie sich am POS ab und wieder an.</span><span class="sxs-lookup"><span data-stu-id="048a9-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="048a9-151">Nachdem Sie angemeldet sind, wählen Sie **Neue Schicht öffnen** und dann **Schublade** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="048a9-152">Schließen Sie ein BOPIS-Szenario ab</span><span class="sxs-lookup"><span data-stu-id="048a9-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="048a9-153">Erstellen Sie eine Storefront-Bestellung für die Abholung im Geschäft</span><span class="sxs-lookup"><span data-stu-id="048a9-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="048a9-154">Gehen Sie zu der URL, die Sie im Schritt [E-Commerce initialisieren](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) während der Umgebungskonfiguration angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="048a9-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="048a9-155">Wählen Sie ein Element aus und dann **In den Einkaufskorb**.</span><span class="sxs-lookup"><span data-stu-id="048a9-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="048a9-156">Wählen Sie auf der Einkaufskorbseite **Abholung** für die Bestellposition aus, die Sie gerade hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="048a9-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="048a9-157">Geben Sie im **Auswählen eines Shops**-Dialogfeld **San Francisco** ein und wählen Sie dann die **Suche**-Taste.</span><span class="sxs-lookup"><span data-stu-id="048a9-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="048a9-158">Suchen Sie in der Ergebnisliste den Shop in San Francisco und wählen Sie **Hier abholen**.</span><span class="sxs-lookup"><span data-stu-id="048a9-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="048a9-159">Wählen Sie auf der Einkaufskorbseite **Als Gast auschecken** aus.</span><span class="sxs-lookup"><span data-stu-id="048a9-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="048a9-160">Um mit dem Auschecken fortzufahren, müssen Sie den Cookie-Hinweis akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="048a9-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="048a9-161">Dieser Hinweis wird als Banner oben auf der Checkout-Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048a9-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="048a9-162">Geben Sie für die Kreditkartenzahlungsmethode die folgenden Details ein:</span><span class="sxs-lookup"><span data-stu-id="048a9-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="048a9-163">**Name des Karteninhabers:** Geben Sie einen beliebigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="048a9-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="048a9-164">**Kartennummer:** Geben Sie **4111-1111-1111-1111** ein.</span><span class="sxs-lookup"><span data-stu-id="048a9-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="048a9-165">**Ablaufdatum:** Geben Sie **10/20** ein.</span><span class="sxs-lookup"><span data-stu-id="048a9-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="048a9-166">**Kartenprüfwert (CVV)-Code:** Geben Sie **737** ein.</span><span class="sxs-lookup"><span data-stu-id="048a9-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="048a9-167">Sie sollten unter keinen Umständen versuchen, die tatsächlichen Kreditkarteninformationen auf der Testseite zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="048a9-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="048a9-168">Fahren Sie mit der Kaufabwicklung fort, indem Sie Details zur Rechnungsadresse eingeben und dann **Speichern und fortfahren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="048a9-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="048a9-169">Wenn die Bestellung aufgegeben werden kann, wählen Sie **Auschecken**.</span><span class="sxs-lookup"><span data-stu-id="048a9-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="048a9-170">Synchronisieren Sie Online-Bestellungen mit dem Backoffice</span><span class="sxs-lookup"><span data-stu-id="048a9-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="048a9-171">Informationen zum Synchronisieren von Online-Bestellungen finden Sie unter [Onlineverkäufe und -zahlungen buchen](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="048a9-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="048a9-172">Bestellung im Shop abholen</span><span class="sxs-lookup"><span data-stu-id="048a9-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="048a9-173">Melden Sie sich am POS an.</span><span class="sxs-lookup"><span data-stu-id="048a9-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="048a9-174">Auf der Seite **Willkommen bei** wählen Sie **Auftragserfüllung** aus</span><span class="sxs-lookup"><span data-stu-id="048a9-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="048a9-175">Wählen Sie in der Liste der Artikel zur Abholung die Position aus der Bestellung aus, die online aufgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="048a9-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="048a9-176">Wählen Sie **Abholen**, während die Bestellposition ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="048a9-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="048a9-177">Der Positionsartikel wird dem Transaktionsbildschirm hinzugefügt, und **$ 0,00** wird als fälliger Saldo angezeigt.</span><span class="sxs-lookup"><span data-stu-id="048a9-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="048a9-178">Wählen Sie den Restbetrag von **$ 0,00** oder wählen Sie eine Zahlungsmethode aus, um die Transaktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="048a9-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="048a9-179">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="048a9-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="048a9-180">Bei Online-Bestellungen, die am POS abgerufen werden, ist ein Saldo ungleich null fällig</span><span class="sxs-lookup"><span data-stu-id="048a9-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="048a9-181">Wenn eine Bestellung für die Abholung im Geschäft abgerufen wird und der fällige Restbetrag nicht 0 (null) beträgt, stellen Sie sicher, dass Modern POS verwendet wird und die Hardwarestation aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="048a9-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="048a9-182">Wenn Cloud POS oder Modern POS für iOS verwendet wird, stellen Sie sicher, dass eine gemeinsam genutzte Hardwarestation aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="048a9-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="048a9-183">Zum Abrufen von Online-Zahlungen ist eine aktive Hardwarestation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="048a9-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="048a9-184">Allgemeine Probleme bei der Zahlungserfassung</span><span class="sxs-lookup"><span data-stu-id="048a9-184">General issues with payment capture</span></span>

<span data-ttu-id="048a9-185">Bei allen allgemeinen Problemen sollten Sie als ersten Schritt immer die Ereignisprotokolle der Modern POS- oder IIS-Hardwarestation (Internet Information Services) konsultieren.</span><span class="sxs-lookup"><span data-stu-id="048a9-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="048a9-186">Sie finden diese Protokolle unter den folgenden Knoten im Windows-Ereignisprotokoll:</span><span class="sxs-lookup"><span data-stu-id="048a9-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="048a9-187">Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="048a9-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="048a9-188">Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="048a9-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="048a9-189">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="048a9-189">Additional resources</span></span>

[<span data-ttu-id="048a9-190">Dynamics 365 Commerce-Auswertungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="048a9-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="048a9-191">Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="048a9-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="048a9-192">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="048a9-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="048a9-193">Dynamics 365 Commerce-Auswertungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="048a9-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="048a9-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="048a9-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="048a9-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="048a9-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="048a9-196">Microsoft Azure-Portal</span><span class="sxs-lookup"><span data-stu-id="048a9-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="048a9-197">Dynamics 365 Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="048a9-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="048a9-198">Connector für Adyen-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="048a9-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="048a9-199">Online-Zahlungsmittel mit dem Adyen Connector speichern</span><span class="sxs-lookup"><span data-stu-id="048a9-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="048a9-200">Überblick über Omni-Channel-Zahlungen</span><span class="sxs-lookup"><span data-stu-id="048a9-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]