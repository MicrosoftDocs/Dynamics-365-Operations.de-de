---
title: Einen Onlinechannel einrichten
description: In diesem Thema wird beschrieben, wie Sie einen neuen Onlinechannel in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
ms.date: 07/02/2020
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
ms.openlocfilehash: b6bf158361f95b6551b29f195616cf21f908b802
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800638"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="4d70b-103">Einen Onlinechannel einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4d70b-104">In diesem Thema wird beschrieben, wie Sie einen neuen Onlinechannel in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d70b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4d70b-105">Overview</span></span>

<span data-ttu-id="4d70b-106">Dynamics 365 Commerce unterstützt mehrere Retail Channels.</span><span class="sxs-lookup"><span data-stu-id="4d70b-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="4d70b-107">Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt).</span><span class="sxs-lookup"><span data-stu-id="4d70b-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="4d70b-108">Onlineshops geben Kunden die Gelegenheit, Produkte über die Onlinepräsenz des Einzelhändlers sowie aus dessen Einzelhandelsgeschäften zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="4d70b-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="4d70b-109">Um einen Onlineshop in Commerce zu erstellen, müssen Sie zunächst einen Onlinechannel erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-109">To create an online store in Commerce, you must first create an online channel.</span></span> <span data-ttu-id="4d70b-110">Vergewissern Sie sich vor dem Erstellen eines neuen Onlinechannels, dass Sie die [Voraussetzungen für die Kanaleinrichtung](channels-prerequisites.md) erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

<span data-ttu-id="4d70b-111">Bevor Sie eine neue Site erstellen können, muss mindestens ein Onlineshop in Commerce erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4d70b-111">Before you can create a new site, at least one online store must be created in Commerce.</span></span> <span data-ttu-id="4d70b-112">Weitere Informationen finden Sie unter [Erstellen einer E-Commerce-Webseite](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="4d70b-112">For more information, see [Create an e-Commerce site](create-ecommerce-site.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="4d70b-113">Einen neuen Onlinechannel erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="4d70b-113">Create and configure a new online channel</span></span>

<span data-ttu-id="4d70b-114">Um einen Onlinechannel zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-114">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="4d70b-115">Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Onlineshops**.</span><span class="sxs-lookup"><span data-stu-id="4d70b-115">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="4d70b-116">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-116">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d70b-117">Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.</span><span class="sxs-lookup"><span data-stu-id="4d70b-117">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="4d70b-118">Geben Sie im Dropdown **Juristische Person** die entsprechende juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="4d70b-118">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="4d70b-119">Geben Sie im Dropdown **Lagerort** den entsprechenden Lagerort ein.</span><span class="sxs-lookup"><span data-stu-id="4d70b-119">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="4d70b-120">Wählen Sie im Feld **Zeitzone des Shops** die entsprechende Zeitzone aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-120">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="4d70b-121">Wählen Sie im Feld **Währung** die entsprechende Währung aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-121">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="4d70b-122">Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.</span><span class="sxs-lookup"><span data-stu-id="4d70b-122">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="4d70b-123">Geben Sie im Feld **Kundenadressbuch** ein gültiges Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="4d70b-123">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="4d70b-124">Wählen Sie im Feld **Funktionsprofil** gegebenenfalls ein Funktionsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-124">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="4d70b-125">Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="4d70b-125">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="4d70b-126">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-126">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4d70b-127">Das folgende Bild zeigt die Erstellung eines neuen Onlinechannel.</span><span class="sxs-lookup"><span data-stu-id="4d70b-127">The following image shows the creation of a new online channel.</span></span>

![Neuer Onlinechannel](media/channel-setup-online-1.png)

<span data-ttu-id="4d70b-129">Das folgende Bild zeigt ein Beispiel für einen Onlinechannel.</span><span class="sxs-lookup"><span data-stu-id="4d70b-129">The following image shows an example online channel.</span></span>

![Beispiel-Onlinechannel](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="4d70b-131">Sprachen einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-131">Set up languages</span></span>

<span data-ttu-id="4d70b-132">Wenn Ihre E-Commerce-Site mehrere Sprachen unterstützt, erweitern Sie den Abschnitt **Sprachen** und fügen Sie nach Bedarf weitere Sprachen hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d70b-132">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="4d70b-133">Zahlungskonto einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-133">Set up payment account</span></span>

<span data-ttu-id="4d70b-134">Aus dem Abschnitt **Zahlungskonto** können Sie einen Drittanbieter für Zahlungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-134">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="4d70b-135">Mehr Informationen zum Einrichten eines Adyen-Zahlungskonnektors finden Sie unter [Dynamics 365 Adyen-Zahlungskonnektor](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="4d70b-135">For information on setting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-setup"></a><span data-ttu-id="4d70b-136">Einrichtung eines zusätzlichen Kanals</span><span class="sxs-lookup"><span data-stu-id="4d70b-136">Additional channel setup</span></span>

<span data-ttu-id="4d70b-137">Zusätzliche Aufgaben, die für das Einrichten des Onlinechannel erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, die Lieferarten und die Erfüllungsgruppenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-137">Additional tasks that are required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="4d70b-138">Das folgende Bild zeigt die Einrichtungsoptionen **Lieferarten**, **Zahlungsmethoden** und **Zuordnung der Erfüllungsgruppen** auf der Registerkarte **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="4d70b-138">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Zusätzliche Aktionen zum Einrichten von Onlinechannels](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="4d70b-140">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="4d70b-140">Set up payment methods</span></span>

<span data-ttu-id="4d70b-141">Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.</span><span class="sxs-lookup"><span data-stu-id="4d70b-141">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="4d70b-142">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="4d70b-142">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="4d70b-143">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-143">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d70b-144">Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-144">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="4d70b-145">Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-145">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="4d70b-146">Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="4d70b-146">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="4d70b-147">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4d70b-148">Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="4d70b-148">The following image shows an example of a cash payment method.</span></span>

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="4d70b-150">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-150">Set up modes of delivery</span></span>

<span data-ttu-id="4d70b-151">Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-151">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="4d70b-152">Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-152">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="4d70b-153">Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.</span><span class="sxs-lookup"><span data-stu-id="4d70b-153">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="4d70b-154">Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-154">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="4d70b-155">Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4d70b-155">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="4d70b-156">Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4d70b-156">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="4d70b-157">Das folgende Bild zeigt ein Beispiel für eine Lieferart.</span><span class="sxs-lookup"><span data-stu-id="4d70b-157">The following image shows an example of a mode of delivery.</span></span>

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="4d70b-159">Eine Erfüllungsgruppenzuweisung einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-159">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="4d70b-160">Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="4d70b-160">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="4d70b-161">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Erfüllungsgruppenzuweisung** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-161">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="4d70b-162">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-162">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d70b-163">Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-163">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="4d70b-164">Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="4d70b-164">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="4d70b-165">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="4d70b-165">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4d70b-166">Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="4d70b-166">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Erfüllungsgruppenzuweisung einrichten](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="4d70b-168">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4d70b-168">Additional resources</span></span>

[<span data-ttu-id="4d70b-169">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="4d70b-169">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="4d70b-170">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="4d70b-170">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="4d70b-171">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-171">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="4d70b-172">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="4d70b-172">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="4d70b-173">Connector für Adyen-Zahlungen für Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4d70b-173">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]