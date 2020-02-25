---
title: Onlinechannel einrichten
description: In diesem Thema wird beschrieben, wie Sie einen neuen Onlinechannel in Microsoft Dynamics 365 Commerce erstellen.
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
ms.openlocfilehash: 9b7a2b8fd157df8b39e9e227d188a3802cacb4e3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002426"
---
# <a name="set-up-an-online-channel"></a><span data-ttu-id="f50b2-103">Onlinechannel einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-103">Set up an online channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f50b2-104">In diesem Thema wird beschrieben, wie Sie einen neuen Onlinechannel in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-104">This topic describes how to create a new online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f50b2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f50b2-105">Overview</span></span>

<span data-ttu-id="f50b2-106">Dynamics 365 Commerce unterstützt mehrere Retail Channels.</span><span class="sxs-lookup"><span data-stu-id="f50b2-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="f50b2-107">Diese Vertriebskanäle umfassen Onlineshops, Callcenter und Einzelhandelsgeschäfte (auch physische Läden genannt).</span><span class="sxs-lookup"><span data-stu-id="f50b2-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="f50b2-108">Onlineshops geben Kunden die Gelegenheit, Produkte über die Onlinepräsenz des Einzelhändlers sowie aus dessen Einzelhandelsgeschäften zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="f50b2-108">Online stores give customers the option of purchasing products from the retailer's online store in addition to its retail stores.</span></span>

<span data-ttu-id="f50b2-109">Um einen Onlineshop in Commerce zu erstellen, müssen Sie zunächst einen Onlinechannel erstellen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-109">To create an online store in Commerce, you must first create an online channel.</span></span> 

<span data-ttu-id="f50b2-110">Vergewissern Sie sich vor dem Erstellen eines neuen Onlinechannels, dass Sie die [Voraussetzungen für die Kanaleinrichtung](channels-prerequisites.md) erfüllen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-110">Before you create a new online channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-online-channel"></a><span data-ttu-id="f50b2-111">Einen neuen Onlinechannel erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f50b2-111">Create and configure a new online channel</span></span>

<span data-ttu-id="f50b2-112">Um einen Onlinechannel zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-112">To create and configure a new online channel, follow these steps.</span></span>

1. <span data-ttu-id="f50b2-113">Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Onlineshops**.</span><span class="sxs-lookup"><span data-stu-id="f50b2-113">In the navigation pane, go to **Modules \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="f50b2-114">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-114">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f50b2-115">Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.</span><span class="sxs-lookup"><span data-stu-id="f50b2-115">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="f50b2-116">Geben Sie im Dropdown **Juristische Person** die entsprechende juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="f50b2-116">In the **Legal entity** drop-down, enter the appropriate legal entity.</span></span>
1. <span data-ttu-id="f50b2-117">Geben Sie im Dropdown **Lagerort** den entsprechenden Lagerort ein.</span><span class="sxs-lookup"><span data-stu-id="f50b2-117">In the **Warehouse** drop-down, enter the appropriate warehouse.</span></span>
1. <span data-ttu-id="f50b2-118">Wählen Sie im Feld **Zeitzone des Shops** die entsprechende Zeitzone aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-118">In the **Store time zone** field, select the appropriate time zone.</span></span>
1. <span data-ttu-id="f50b2-119">Wählen Sie im Feld **Währung** die entsprechende Währung aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-119">In the **Currency** field, select the appropriate currency.</span></span>
1. <span data-ttu-id="f50b2-120">Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.</span><span class="sxs-lookup"><span data-stu-id="f50b2-120">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="f50b2-121">Geben Sie im Feld **Kundenadressbuch** ein gültiges Adressbuch an.</span><span class="sxs-lookup"><span data-stu-id="f50b2-121">In the **Customer address book** field, provide a valid address book.</span></span>
1. <span data-ttu-id="f50b2-122">Wählen Sie im Feld **Funktionsprofil** gegebenenfalls ein Funktionsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-122">In the **Functionality profile** field, select a functionality profile if applicable.</span></span>
1. <span data-ttu-id="f50b2-123">Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="f50b2-123">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="f50b2-124">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-124">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f50b2-125">Das folgende Bild zeigt die Erstellung eines neuen Onlinechannel.</span><span class="sxs-lookup"><span data-stu-id="f50b2-125">The following image shows the creation of a new online channel.</span></span>

![Neuer Onlinechannel](media/channel-setup-online-1.png)

<span data-ttu-id="f50b2-127">Das folgende Bild zeigt ein Beispiel für einen Onlinechannel.</span><span class="sxs-lookup"><span data-stu-id="f50b2-127">The following image shows an example online channel.</span></span>

![Beispiel-Onlinechannel](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a><span data-ttu-id="f50b2-129">Sprachen einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-129">Set up languages</span></span>

<span data-ttu-id="f50b2-130">Wenn Ihre E-Commerce-Site mehrere Sprachen unterstützt, erweitern Sie den Abschnitt **Sprachen** und fügen Sie nach Bedarf weitere Sprachen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f50b2-130">If your e-Commerce site will support multiple languages, expand the **Languages** section and add additional languages as needed.</span></span>

## <a name="set-up-payment-account"></a><span data-ttu-id="f50b2-131">Zahlungskonto einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-131">Set up payment account</span></span>

<span data-ttu-id="f50b2-132">Aus dem Abschnitt **Zahlungskonto** können Sie einen Drittanbieter für Zahlungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-132">From within the **Payment account** section, you can add a third-party payment provider.</span></span> <span data-ttu-id="f50b2-133">Informationen zum Einrichten eines Adyen-Zahlungskonnektors finden Sie unter [Dynamics 365 Adyen-Zahlungskonnektor](../retail/dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="f50b2-133">For information on settting up an Adyen payment connector, see [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).</span></span>

## <a name="additional-channel-set-up"></a><span data-ttu-id="f50b2-134">Einrichtung eines zusätzlichen Kanals</span><span class="sxs-lookup"><span data-stu-id="f50b2-134">Additional channel set up</span></span>

<span data-ttu-id="f50b2-135">Zusätzliche Aufgaben, die für das Einrichten des Onlinechannel erforderlich sind, umfassen das Einrichten von Zahlungsmethoden, Lieferarten und Erfüllungsgruppenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-135">Additional tasks required for online channel setup include setting up payment methods, modes of delivery, and the fulfillment group assignment.</span></span>

<span data-ttu-id="f50b2-136">Das folgende Bild zeigt die Einrichtungsoptionen **Lieferarten**, **Zahlungsmethoden** und **Zuordnung der Erfüllungsgruppen** auf der Registerkarte **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="f50b2-136">The following image shows **Modes of delivery**, **Payment methods**, and **Fulfillment group assignment** setup options on the **Set up** tab.</span></span>

![Zusätzliche Aktionen zum Einrichten von Onlinechannels](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="f50b2-138">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="f50b2-138">Set up payment methods</span></span>

<span data-ttu-id="f50b2-139">Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f50b2-139">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="f50b2-140">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="f50b2-140">On the action pane, select the **Set Up** tab, then select **Payment methods**.</span></span>
1. <span data-ttu-id="f50b2-141">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-141">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f50b2-142">Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-142">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="f50b2-143">Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-143">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="f50b2-144">Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="f50b2-144">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="f50b2-145">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-145">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f50b2-146">Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="f50b2-146">The following image shows an example of a cash payment method.</span></span>

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="f50b2-148">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-148">Set up modes of delivery</span></span>

<span data-ttu-id="f50b2-149">Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-149">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="f50b2-150">Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-150">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="f50b2-151">Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.</span><span class="sxs-lookup"><span data-stu-id="f50b2-151">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="f50b2-152">Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-152">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="f50b2-153">Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f50b2-153">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="f50b2-154">Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f50b2-154">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="f50b2-155">Das folgende Bild zeigt ein Beispiel für eine Lieferart.</span><span class="sxs-lookup"><span data-stu-id="f50b2-155">The following image shows an example of a mode of delivery.</span></span>

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a><span data-ttu-id="f50b2-157">Eine Erfüllungsgruppenzuweisung einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-157">Set up a fulfillment group assignment</span></span>

<span data-ttu-id="f50b2-158">Gehen Sie zum Einrichten einer Erfüllungsgruppe folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="f50b2-158">To set up a fulfillment group assignment, follow these steps.</span></span>

1. <span data-ttu-id="f50b2-159">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Erfüllungsgruppenzuweisung** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-159">On the action pane, select the **Set up** tab, then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="f50b2-160">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-160">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f50b2-161">Wählen Sie in der Dropdown-Liste **Erfüllungsgruppe** eine Erfüllungsgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-161">In the **Fulfillment group** drop-down list, select a fulfillment group.</span></span>
1. <span data-ttu-id="f50b2-162">Geben Sie in der Dropdown-Liste **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="f50b2-162">In the **Description** drop-down list, enter a description.</span></span>
1. <span data-ttu-id="f50b2-163">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="f50b2-163">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f50b2-164">Die folgende Abbildung zeigt ein Beispiel für die Einrichtung einer Erfüllungsgruppenzuweisung.</span><span class="sxs-lookup"><span data-stu-id="f50b2-164">The following image shows an example of a fulfillment group assignment setup.</span></span>

![Erfüllungsgruppenzuweisung einrichten](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a><span data-ttu-id="f50b2-166">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f50b2-166">Additional resources</span></span>

[<span data-ttu-id="f50b2-167">Kanalübersicht</span><span class="sxs-lookup"><span data-stu-id="f50b2-167">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f50b2-168">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="f50b2-168">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="f50b2-169">Einen Retail Channel einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-169">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="f50b2-170">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="f50b2-170">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="f50b2-171">Connector für Adyen-Zahlungen für Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f50b2-171">Dynamics 365 Payment Connector for Adyen</span></span>](../retail/dev-itpro/adyen-connector.md)
