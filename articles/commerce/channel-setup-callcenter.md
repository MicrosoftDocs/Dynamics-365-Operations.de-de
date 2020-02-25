---
title: Einen Callcenterkanal einrichten
description: In diesem Thema wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.
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
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002449"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="dbb98-103">Einen Callcenterkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="dbb98-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dbb98-104">In diesem Thema wird beschrieben, wie ein Callcenterkanal in Microsoft Dynamics 365 Commerce erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dbb98-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dbb98-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="dbb98-105">Overview</span></span>

<span data-ttu-id="dbb98-106">In Dynamics 365 Commerce ist ein Callcenter ein Retail Channel-Typ, der in der Anwendung definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dbb98-106">In Dynamics 365 Commerce, a call center is a type of retail channel that can be defined in the application.</span></span> <span data-ttu-id="dbb98-107">Durch das Definieren eines Kanals für Ihre Callcenter-Entitäten kann das System bestimmte Daten und Auftragsverarbeitungsstandards mit Aufträgen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="dbb98-108">Ein Unternehmen kann Callcenterkanäle in Commerce definieren.</span><span class="sxs-lookup"><span data-stu-id="dbb98-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="dbb98-109">Vergewissern Sie sich vor dem Erstellen eines neuen Callcenterkanals, dass Sie die [Voraussetzungen für die Kanaleinrichtung](channels-prerequisites.md) erfüllen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="dbb98-110">Einen neuen Callcenterkanal erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="dbb98-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="dbb98-111">Um einen Callcenterkanal zu erstellen und zu konfigurieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="dbb98-112">Gehen Sie im Navigationsbereich zu **Module \> Kanäle \> Callcenter \>Alle Callcenter**.</span><span class="sxs-lookup"><span data-stu-id="dbb98-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="dbb98-113">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dbb98-114">Geben Sie im Feld **Name** einen Namen für den neuen Kanal ein.</span><span class="sxs-lookup"><span data-stu-id="dbb98-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="dbb98-115">Wählen Sie die entsprechende **Juristische Person** aus dem Dropdown aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="dbb98-116">Wählen Sie den entsprechenden Standort des **Lagerorts** aus dem Dropdown aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="dbb98-117">Geben Sie im Feld **Standardkunde** einen gültigen Standardkunden an.</span><span class="sxs-lookup"><span data-stu-id="dbb98-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="dbb98-118">Geben Sie in das Feld **E-Mail-Benachrichtigungsprofil** ein gültiges E-Mail-Benachrichtigungsprofil ein.</span><span class="sxs-lookup"><span data-stu-id="dbb98-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="dbb98-119">Geben Sie einen Infocode **Preisüberschreibung** an.</span><span class="sxs-lookup"><span data-stu-id="dbb98-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="dbb98-120">Beachten Sie, dass Sie möglicherweise zuerst einen Infocode dafür erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="dbb98-121">Geben Sie einen Infocode **Code halten** ein.</span><span class="sxs-lookup"><span data-stu-id="dbb98-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="dbb98-122">Beachten Sie, dass Sie möglicherweise zuerst einen Infocode dafür erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="dbb98-123">Geben Sie einen Infocode **Haben** ein.</span><span class="sxs-lookup"><span data-stu-id="dbb98-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="dbb98-124">Beachten Sie, dass Sie möglicherweise zuerst einen Infocode dafür erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="dbb98-125">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="dbb98-125">Select **Save**.</span></span>

<span data-ttu-id="dbb98-126">Das folgende Bild zeigt die Erstellung eines neuen Callcenterkanals.</span><span class="sxs-lookup"><span data-stu-id="dbb98-126">The following image shows the creation of a new call center channel.</span></span>

![Neuer Callcenterkanal](media/channel-setup-callcenter-1.png)

<span data-ttu-id="dbb98-128">Das folgende Bild zeigt ein Beispiel für einen Callcenterkanal.</span><span class="sxs-lookup"><span data-stu-id="dbb98-128">The following image shows an example call center channel.</span></span>

![Beispiel eines Callcenterkanals](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="dbb98-130">Einrichtung eines zusätzlichen Kanals</span><span class="sxs-lookup"><span data-stu-id="dbb98-130">Additional channel setup</span></span>

<span data-ttu-id="dbb98-131">Zusätzliche Aufgaben, die für das Einrichten des Callcenterkanals erforderlich sind, umfassen das Einrichten von Zahlungsmethoden und Lieferarten.</span><span class="sxs-lookup"><span data-stu-id="dbb98-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="dbb98-132">Das folgende Bild zeigt die Einrichtungsoptionen **Lieferarten** und **Zahlungsmethoden** auf der Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="dbb98-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![Zusätzliche Aktionen zum Einrichten von Callcenterkanälen](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="dbb98-134">Einrichten von Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="dbb98-134">Set up payment methods</span></span>

<span data-ttu-id="dbb98-135">Führen Sie die folgenden Schritte aus, um die Zahlungsmethoden für jede auf diesem Kanal unterstützte Zahlungsart einzurichten.</span><span class="sxs-lookup"><span data-stu-id="dbb98-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="dbb98-136">Wählen Sie im Aktionsbereich die Registerkarte **Einrichten** und dann **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="dbb98-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="dbb98-137">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dbb98-138">Wählen Sie im Navigationsbereich eine gewünschte Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="dbb98-139">Geben Sie im Abschnitt **Allgemeines** einen **Operationsname** an und konfigurieren Sie alle anderen gewünschten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="dbb98-140">Konfigurieren Sie ggf. zusätzliche Einstellungen für die Zahlungsart.</span><span class="sxs-lookup"><span data-stu-id="dbb98-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="dbb98-141">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="dbb98-142">Das folgende Bild zeigt ein Beispiel für eine Bargeldzahlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="dbb98-142">The following image shows an example of a cash payment method.</span></span>

![Beispielzahlungsmethoden](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="dbb98-144">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="dbb98-144">Set up modes of delivery</span></span>

<span data-ttu-id="dbb98-145">Sie können die konfigurierten Zustellmodi anzeigen, indem Sie **Lieferarten** aus der Registerkarte **Einrichten** im **Aktionsbereich** auswählen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="dbb98-146">Gehen Sie folgendermaßen vor, um eine Lieferart zu ändern oder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="dbb98-147">Gehen Sie im Navigationsbereich zu **Module \> Bestandsverwaltung \> Lieferarten**.</span><span class="sxs-lookup"><span data-stu-id="dbb98-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="dbb98-148">Wählen Sie im Aktionsbereich **Neu** aus, um eine neue Lieferart zu erstellen oder wählen Sie einen vorhandenen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="dbb98-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="dbb98-149">Im Abschnitt **Retail Channels** wählen Sie **Zeile hinzufügen** aus, um den Kanal hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dbb98-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="dbb98-150">Durch das Hinzufügen von Kanälen mithilfe von Organisationsknoten, anstatt jeden Kanal einzeln hinzuzufügen, kann das Hinzufügen von Kanälen rationalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="dbb98-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="dbb98-151">Das folgende Bild zeigt ein Beispiel für eine Lieferart.</span><span class="sxs-lookup"><span data-stu-id="dbb98-151">The following image shows an example of a mode of delivery.</span></span>

![Lieferarten einrichten](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="dbb98-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dbb98-153">Additional resources</span></span>

[<span data-ttu-id="dbb98-154">Voraussetzungen der Kanaleinrichtung</span><span class="sxs-lookup"><span data-stu-id="dbb98-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="dbb98-155">Callcenter-Vertriebsfunktionen</span><span class="sxs-lookup"><span data-stu-id="dbb98-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="dbb98-156">Callcenter-Auftragsabwicklungsoptionen einrichten</span><span class="sxs-lookup"><span data-stu-id="dbb98-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="dbb98-157">Callcenterkataloge</span><span class="sxs-lookup"><span data-stu-id="dbb98-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="dbb98-158">Einrichten und Verwenden von Betrugswarnungen</span><span class="sxs-lookup"><span data-stu-id="dbb98-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="dbb98-159">Einrichten von Anschlussprogrammen für Callcenter</span><span class="sxs-lookup"><span data-stu-id="dbb98-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
