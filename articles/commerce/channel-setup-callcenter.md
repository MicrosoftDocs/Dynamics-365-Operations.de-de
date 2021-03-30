---
title: Einen Callcenterkanal einrichten
description: In diesem Thema wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 878774c8e5485211525e7e7b63973173f6874b26
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218368"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="83f96-103">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="83f96-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="83f96-104">In diesem Thema wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="83f96-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="83f96-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="83f96-105">Overview</span></span>


<span data-ttu-id="83f96-106">In Dynamics 365 Commerce ist ein Callcenter ein Commerce Channel, der in der Anwendung definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="83f96-106">In Dynamics 365 Commerce, a call center is a type of Commerce channel that can be defined in the application.</span></span> <span data-ttu-id="83f96-107">Durch das Definieren eines Kanals für Ihre Callcenter-Entitäten kann das System bestimmte Daten und Auftragsverarbeitungsstandards mit Aufträgen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="83f96-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="83f96-108">Während ein Unternehmen mehrere Call-Center-Kanäle in Commerce definieren kann, ist es wichtig zu beachten, dass ein einzelner Benutzer nur mit einem Call-Center-Kanal verbunden sein darf.</span><span class="sxs-lookup"><span data-stu-id="83f96-108">While a company can define multiple call center channels in Commerce, it is important to note that an individual user may only be linked to one call center channel.</span></span> 

<span data-ttu-id="83f96-109">Bevor Sie einen neuen Callcenter-Kanal anlegen, stellen Sie sicher, dass Sie die Voraussetzungen [Kanal-Einrichtung](channels-prerequisites.md) erfüllt haben.</span><span class="sxs-lookup"><span data-stu-id="83f96-109">Before you create a new call center channel, ensure that you have completed the [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="83f96-110">Einen neuen Callcenterkanal erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="83f96-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="83f96-111">Um einen Callcenterkanal zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="83f96-112">Gehen Sie im Navigationsbereich zu **Retail and Commerce \> Kanäle \> Callcenter \> Alle Callcenter**.</span><span class="sxs-lookup"><span data-stu-id="83f96-112">In the navigation pane, go to **Retail and Commerce \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="83f96-113">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="83f96-114">Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.</span><span class="sxs-lookup"><span data-stu-id="83f96-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="83f96-115">Wählen Sie aus der Dropdown-Liste die entsprechende **Juristische Person** aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-115">Select the appropriate **Legal entity** from the drop-down.</span></span>
1. <span data-ttu-id="83f96-116">Wählen Sie aus der Dropdown-Liste den entsprechenden **Lager** Lagerplatz aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-116">Select the appropriate **Warehouse** location from the drop-down.</span></span> <span data-ttu-id="83f96-117">Dieser Standort wird als Standard bei Kundenaufträgen verwendet, die für diesen Call-Center-Kanal angelegt werden, es sei denn, auf Kunden- oder Artikelebene wurden andere Standardeinstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="83f96-117">This location will be used as the default on sales orders created for this call center channel, unless other defaults have been defined at the customer or item level.</span></span>
1. <span data-ttu-id="83f96-118">Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.</span><span class="sxs-lookup"><span data-stu-id="83f96-118">In the **Default customer** field, provide a valid default customer.</span></span> <span data-ttu-id="83f96-119">Diese Daten werden für die Unterstützung der automatischen Bestückung mit Standardeinstellungen verwendet, wenn neue Kundendatensätze angelegt werden.</span><span class="sxs-lookup"><span data-stu-id="83f96-119">This data is used to assist in autopopulating defaults when new customer records are created.</span></span> <span data-ttu-id="83f96-120">Beim Anlegen von Callcenter-Aufträgen ist es nicht ratsam, Aufträge für den Standardkunden anzulegen.</span><span class="sxs-lookup"><span data-stu-id="83f96-120">When creating call center orders, it is not advisable to create orders for the default customer.</span></span>
1. <span data-ttu-id="83f96-121">Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="83f96-121">In the **Email notification profile** field, provide a valid email notification profile.</span></span> <span data-ttu-id="83f96-122">Beim Anlegen und Verarbeiten von Callcenter-Aufträgen wird das E-Mail-Benachrichtigungsprofil verwendet, um automatische E-Mail-Benachrichtigungen an Kunden mit Informationen über ihren Auftragsstatus auszulösen.</span><span class="sxs-lookup"><span data-stu-id="83f96-122">As call center orders are created and processed, the email notification profile is used to trigger automated email alerts to customers with information about their order status.</span></span>
1. <span data-ttu-id="83f96-123">Geben Sie einen Infocode **Preisüberschreibung** an.</span><span class="sxs-lookup"><span data-stu-id="83f96-123">Provide a **Price override** info code.</span></span> <span data-ttu-id="83f96-124">Dazu müssen Sie möglicherweise zuerst einen Info-Code anlegen.</span><span class="sxs-lookup"><span data-stu-id="83f96-124">You may need to create an info code for this first.</span></span> <span data-ttu-id="83f96-125">Dieser Infocode enthält eine Reihe von Begründungscodes, aus denen der Benutzer bei der Verwendung der Funktion zur Preisüberschreibung bei einer Call-Center-Bestellung aufgefordert wird, eine Auswahl zu treffen.</span><span class="sxs-lookup"><span data-stu-id="83f96-125">This info code provides the set of reason codes that the user will be prompted to choose from when using the price override functionality on a call center order.</span></span>
1. <span data-ttu-id="83f96-126">Geben Sie einen Infocode **Code halten** ein.</span><span class="sxs-lookup"><span data-stu-id="83f96-126">Provide a **Hold code** info code.</span></span> <span data-ttu-id="83f96-127">Dazu müssen Sie möglicherweise zuerst einen Info-Code anlegen.</span><span class="sxs-lookup"><span data-stu-id="83f96-127">You may need to create an info code for this first.</span></span> <span data-ttu-id="83f96-128">Dieser Infocode enthält eine Reihe von optionalen Begründungscodes, aus denen der Benutzer bei der Platzierung einer zurückgestellten Bestellung zur Auswahl aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="83f96-128">This info code provides the set of optional reason codes that the user will be prompted to choose from when placing an order on hold.</span></span>
1. <span data-ttu-id="83f96-129">Geben Sie einen Infocode **Haben** ein.</span><span class="sxs-lookup"><span data-stu-id="83f96-129">Provide a **Credit** info code.</span></span> <span data-ttu-id="83f96-130">Dazu müssen Sie möglicherweise zuerst einen Info-Code anlegen.</span><span class="sxs-lookup"><span data-stu-id="83f96-130">You may need to create an info code for this first.</span></span> <span data-ttu-id="83f96-131">Dieser Infocode stellt die Menge der Begründungscodes zur Verfügung, aus denen der Benutzer wählen kann, wenn er die Auftragskreditfunktion des Call Centers verwendet, um dem Kunden aus Gründen des Kundendienstes verschiedene Rückerstattungen zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="83f96-131">This info code provides the set of reason codes that the user can choose from when using the order credit functionality of call center to give misc refunds to the customer for customer service reasons.</span></span>
1. <span data-ttu-id="83f96-132">Optional: Richten Sie die finanziellen Dimensionen auf der Registerkarte **Finanzielle Dimensionen** ein.</span><span class="sxs-lookup"><span data-stu-id="83f96-132">Optional: set up financial dimensions on the **Financial dimensions** FastTab.</span></span> <span data-ttu-id="83f96-133">Die hier eingegebenen Dimensionen werden bei jedem Kundenauftrag, der in diesem Callcenter-Kanal angelegt wird, als Standardeinstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="83f96-133">The dimensions entered here will default on any sales order created in this call center channel.</span></span>
1. <span data-ttu-id="83f96-134">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="83f96-134">Click **Save**.</span></span>

<span data-ttu-id="83f96-135">Das folgende Bild zeigt die Erstellung eines neuen Callcenterkanals.</span><span class="sxs-lookup"><span data-stu-id="83f96-135">The following image shows the creation of a new call center channel.</span></span>

![Neuer Callcenterkanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="83f96-137">Das folgende Bild zeigt ein Beispiel für einen Callcenterkanal.</span><span class="sxs-lookup"><span data-stu-id="83f96-137">The following image shows an example call center channel.</span></span>

![Beispiel eines Callcenterkanals](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="83f96-139">Einrichtung eines zusätzlichen Kanals</span><span class="sxs-lookup"><span data-stu-id="83f96-139">Additional channel setup</span></span>

<span data-ttu-id="83f96-140">Zusätzliche Aufgaben, die für das Einrichten des Callcenterkanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden und Lieferarten.</span><span class="sxs-lookup"><span data-stu-id="83f96-140">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="83f96-141">Die folgende Abbildung zeigt **Lieferarten** und **Zahlungsmethoden** Einrichtungsoptionen auf der Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="83f96-141">The following image shows **Modes of delivery** and **Payment methods** setup options on the **Set up** tab.</span></span>

![Zusätzliche Aktionen zum Einrichten von Callcenterkanälen](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="83f96-143">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="83f96-143">Set up payment methods</span></span>

<span data-ttu-id="83f96-144">Um die Zahlungsmethoden einzurichten, befolgen Sie diese Schritte für jede in diesem Kanal unterstützte Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="83f96-144">To set up payment methods, follow these steps for each payment type supported on this channel.</span></span> <span data-ttu-id="83f96-145">Die Benutzer müssen aus vordefinierten Zahlungsmethoden auswählen, um sie mit dem Call-Center-Kanal zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="83f96-145">Users will be required to select from pre-defined payment methods to link them to the call center channel.</span></span> <span data-ttu-id="83f96-146">Bevor Sie Ihre Call-Center-Zahlungsmethoden einrichten, richten Sie zunächst Ihre Hauptzahlungsmethoden unter **Retail and Commerce \> \> Zahlungsmethoden \> Zahlungsmethoden** ein.</span><span class="sxs-lookup"><span data-stu-id="83f96-146">Before setting up your call center payment methods, first set up your master methods of payment in **Retail and Commerce \> Channel setup \> Payment methods \> Payment methods**.</span></span>

1. <span data-ttu-id="83f96-147">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="83f96-147">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="83f96-148">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-148">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="83f96-149">Wählen Sie im Navigationsfenster eine Zahlungsmethode aus den vordefinierten verfügbaren Zahlungen aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-149">In the navigation pane, select a payment method from the pre-defined payments available.</span></span>
1. <span data-ttu-id="83f96-150">Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="83f96-150">Configure any additional settings as required for the payment type.</span></span> <span data-ttu-id="83f96-151">Für Kreditkarten, Geschenkkarten oder Kundenkarten ist eine zusätzliche Einrichtung erforderlich, indem Sie die Funktion **Karteneinrichtung** wählen.</span><span class="sxs-lookup"><span data-stu-id="83f96-151">For credit cards, gift cards, or loyalty cards, additional setup is required by selecting the **Card setup** function.</span></span> 
1. <span data-ttu-id="83f96-152">Konfigurieren Sie die richtigen Buchungskonten für die Zahlungsart im Abschnitt **Buchung**.</span><span class="sxs-lookup"><span data-stu-id="83f96-152">Configure proper posting accounts for the payment type in the **Posting** section.</span></span>
1. <span data-ttu-id="83f96-153">Klicken Sie im Aktionsfenster auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="83f96-153">On the action pane, click **Save**.</span></span>

<span data-ttu-id="83f96-154">Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="83f96-154">The following image shows an example of a cash payment method.</span></span>

![Beispielzahlungsmethoden](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="83f96-156">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="83f96-156">Set up modes of delivery</span></span>

<span data-ttu-id="83f96-157">Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.</span><span class="sxs-lookup"><span data-stu-id="83f96-157">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="83f96-158">Um eine dem Call-Center-Kanal zuzuordnende Zustellungsart zu ändern oder hinzuzufügen, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="83f96-158">To change or add a mode of delivery to be associated to the call center channel, follow these steps.</span></span>

1. <span data-ttu-id="83f96-159">Wählen Sie im Call-Center-Zustellungsmodi-Formular **Zustellungsmodi verwalten**.</span><span class="sxs-lookup"><span data-stu-id="83f96-159">From the Call center modes of delivery form, select **Manage modes of delivery**</span></span>
1. <span data-ttu-id="83f96-160">Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-160">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="83f96-161">Klicken Sie in der Sektion **Einzelhandelskanäle** auf **Zeile hinzufügen**, um den Call-Center-Kanal hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="83f96-161">In the **Retail channels** section, click **Add line** to add the call center channel.</span></span> <span data-ttu-id="83f96-162">Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="83f96-162">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>
1. <span data-ttu-id="83f96-163">Vergewissern Sie sich, dass der Zustellungsmodus mit Daten über **Produkte** und **Adressen** konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="83f96-163">Ensure the mode of delivery has been configured with data on the **Products** FastTab and the **Addresses** FastTab.</span></span> <span data-ttu-id="83f96-164">Wenn keine Produkte oder Lieferadressen für die Lieferart gültig sind, führt die Auswahl der Lieferart bei der Auftragserfassung zu Fehlern.</span><span class="sxs-lookup"><span data-stu-id="83f96-164">If no products or delivery addresses are valid for the mode of delivery, choosing it during order entry will result in errors.</span></span>
1. <span data-ttu-id="83f96-165">Nachdem Änderungen an den Call-Center-Lieferartenkonfigurationen vorgenommen wurden, muss der Job **Lieferarten bearbeiten** ausgeführt werden, um die Änderungsmatrix aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="83f96-165">After any changes have been made to the call center mode of delivery configurations, the **Process delivery modes** job must be run to explode the change matrix.</span></span> <span data-ttu-id="83f96-166">Diesen Job finden Sie, indem Sie zu **Retail and Commerce \> Retail and Commerce IT \> Prozesslieferungsarten** navigieren.</span><span class="sxs-lookup"><span data-stu-id="83f96-166">This job can be found by navigating to **Retail and Commerce \> Retail and Commerce IT \> Process delivery modes**.</span></span>

<span data-ttu-id="83f96-167">Das folgende Bild zeigt ein Beispiel für eine Lieferart.</span><span class="sxs-lookup"><span data-stu-id="83f96-167">The following image shows an example of a mode of delivery.</span></span>

![Lieferarten einrichten](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a><span data-ttu-id="83f96-169">Channel-Benutzer einrichten</span><span class="sxs-lookup"><span data-stu-id="83f96-169">Set up channel users</span></span>

<span data-ttu-id="83f96-170">Um einen Kundenauftrag anzulegen, der mit dem Call-Center-Kanal vpm Commerce Headquarters verknüpft ist, muss der Benutzer, der den Kundenauftrag anlegt, mit dem Call-Center-Kanal verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="83f96-170">To create a sales order that is linked to the call center channel from Commerce Headquarters, the user creating the sales order must be linked to the call center channel.</span></span> <span data-ttu-id="83f96-171">Der Benutzer kann einen in Commerce Headquarters angelegten Kundenauftrag nicht manuell mit dem Kanal Call Center verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="83f96-171">The user cannot manually link a sales order created in Commerce Headquarters to the call center channel.</span></span> <span data-ttu-id="83f96-172">Die Verknüpfung ist systematisch und basiert auf dem Benutzer und seiner Beziehung zum Channel Call Center.</span><span class="sxs-lookup"><span data-stu-id="83f96-172">The link is systematic, and is based on the user and the user's relationship to the call center channel.</span></span> <span data-ttu-id="83f96-173">Ein Benutzer kann nur mit einem Callcenter-Channel verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="83f96-173">A user may only be linked to one call center channel.</span></span>

1. <span data-ttu-id="83f96-174">Wählen Sie im Aktionsbereich die Registerkarte **Kanal** und dann **Benutzer des Kanals**.</span><span class="sxs-lookup"><span data-stu-id="83f96-174">On the action pane, select the **Channel** tab, and then select **Channel users**.</span></span>
1. <span data-ttu-id="83f96-175">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="83f96-175">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="83f96-176">Wählen Sie aus der Dropdown-Auswahlliste eine vorhandene **Benutzer-ID**, um diesen Benutzer mit dem Callcenter-Kanal zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="83f96-176">Choose an existing **User ID** from the dropdown selection list to link this user to the call center channel</span></span>

<span data-ttu-id="83f96-177">Nachdem die Einrichtung des Kanalbenutzers abgeschlossen ist und der Benutzer einen neuen Kundenauftrag in der Handelszentrale erstellt hat, wird der Kundenauftrag mit dem zugehörigen Callcenter-Kanal verknüpft.</span><span class="sxs-lookup"><span data-stu-id="83f96-177">After the channel user setup is done and the user creates a new sales order in Commerce Headquarters, the sales order will be linked to their associated call center channel.</span></span> <span data-ttu-id="83f96-178">Alle Konfigurationen für diesen Kanal werden systematisch auf den Kundenauftrag angewendet.</span><span class="sxs-lookup"><span data-stu-id="83f96-178">Any configurations for this channel will be applied systematically to the sales order.</span></span> <span data-ttu-id="83f96-179">Ein Benutzer kann bestätigen, mit welchem Callcenter-Kanal der Kundenauftrag verknüpft ist, indem er die Referenz des Kanalnamens im Auftragskopf anzeigt.</span><span class="sxs-lookup"><span data-stu-id="83f96-179">A user can confirm which call center channel the sales order is linked to by viewing the channel name reference on the sales order header.</span></span>


### <a name="set-up-price-groups"></a><span data-ttu-id="83f96-180">Einrichten von Preisgruppen</span><span class="sxs-lookup"><span data-stu-id="83f96-180">Set up price groups</span></span>

<span data-ttu-id="83f96-181">Preisgruppen sind optional, können aber, wenn sie verwendet werden, steuern, welche Verkaufspreise den Kunden, die Aufträge im Callcenter-Kanal erteilen, angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="83f96-181">Price groups are optional, but if used, can control which sales prices will be offered to customers placing orders in the call center channel.</span></span> <span data-ttu-id="83f96-182">Wenn für den Kunden keine Preisgruppe konfiguriert wurde oder wenn Katalogpreisgruppen nicht auf den Kundenauftrag angewendet werden (über das Feld **Quellcode-ID** im Auftragskopf des Callcenters), wird die Kanalpreisgruppe zur Ermittlung von Artikelpreisen verwendet.</span><span class="sxs-lookup"><span data-stu-id="83f96-182">If a price group has not been configured for the customer, or if catalog price groups are not being applied to the sales order (using the **Source code ID** field on the call center order header), then the channel price group is used to locate item prices.</span></span> <span data-ttu-id="83f96-183">Wenn eine Preisgruppe im Kanal des Callcenters nicht gefunden wird, werden die Standardartikelstammpreise verwendet.</span><span class="sxs-lookup"><span data-stu-id="83f96-183">If a price group is not found on the call center channel, the default item master prices are used.</span></span> 

<span data-ttu-id="83f96-184">Um eine Preisgruppe einzurichten, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="83f96-184">To set up a price group, do the following.</span></span>

1. <span data-ttu-id="83f96-185">Klicken Sie im Aktionsbereich auf die Registerkarte **Kanal**, und wählen Sie dann **Preisgruppen**.</span><span class="sxs-lookup"><span data-stu-id="83f96-185">On the action pane, click the **Channel** tab, and then select **Price groups**.</span></span>
1. <span data-ttu-id="83f96-186">Klicken Sie im Aktivitätsbereich auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="83f96-186">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="83f96-187">Wählen Sie aus der Dropdown-Auswahlliste eine **Einzelhandelspreisgruppe**.</span><span class="sxs-lookup"><span data-stu-id="83f96-187">Select a **Retail price group** from the dropdown selection list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83f96-188">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83f96-188">Additional resources</span></span>

[<span data-ttu-id="83f96-189">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="83f96-189">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="83f96-190">Callcenter-Vertriebsfunktionen</span><span class="sxs-lookup"><span data-stu-id="83f96-190">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="83f96-191">Callcenter-Auftragsabwicklungsoptionen einrichten</span><span class="sxs-lookup"><span data-stu-id="83f96-191">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="83f96-192">Callcenterkataloge</span><span class="sxs-lookup"><span data-stu-id="83f96-192">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="83f96-193">Einrichten und Verwenden von Betrugswarnungen</span><span class="sxs-lookup"><span data-stu-id="83f96-193">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="83f96-194">Einrichten von Anschlussprogrammen für Callcenter</span><span class="sxs-lookup"><span data-stu-id="83f96-194">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]