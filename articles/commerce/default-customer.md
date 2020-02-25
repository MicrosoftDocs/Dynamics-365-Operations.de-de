---
title: Einen Standarddebitoren erstellen
description: In diesem Thema wird beschrieben, wie Sie einen Standarddebitoren erstellen, der beim Erstellen eines Kanals in Microsoft Dynamics 365 Commerce verwendet wird.
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
ms.openlocfilehash: 9e1087821b357c578993cdd5742399c5ec0ecc95
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001805"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="d14a0-103">Einen Standarddebitoren erstellen</span><span class="sxs-lookup"><span data-stu-id="d14a0-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d14a0-104">In diesem Thema wird beschrieben, wie Sie einen Standarddebitoren erstellen, der beim Erstellen eines Kanals in Microsoft Dynamics 365 Commerce verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d14a0-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d14a0-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d14a0-105">Overview</span></span>

<span data-ttu-id="d14a0-106">Beim Erstellen eines Einzelhandels- oder Onlinekanals müssen Sie einen Standardkunden angeben.</span><span class="sxs-lookup"><span data-stu-id="d14a0-106">When creating a retail or online channel, you will need to provide a default customer.</span></span> <span data-ttu-id="d14a0-107">Ein Standardkunde kann einfach erstellt werden, nachdem zuerst die Kundengruppe und das Kundenadressbuch erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d14a0-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="d14a0-108">Eine Debitorengruppe erstellen</span><span class="sxs-lookup"><span data-stu-id="d14a0-108">Create a customer group</span></span>

<span data-ttu-id="d14a0-109">Wenn noch keine Debitorengruppen vorhanden sind, können Sie eine erstellen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="d14a0-110">Beispiele können Gruppen sein, um verschiedene Kundengruppen darzustellen, z. B. Großhandel, Einzelhandel, Internet, Mitarbeiter usw.</span><span class="sxs-lookup"><span data-stu-id="d14a0-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="d14a0-111">Gehen Sie folgendermaßen vor, um eine Debitorengruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="d14a0-112">Wechseln Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Debitoren \> Debitorengruppen**.</span><span class="sxs-lookup"><span data-stu-id="d14a0-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="d14a0-113">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d14a0-114">Geben Sie im Feld **Debitorengruppe** eine Debitorengruppenkennung ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="d14a0-115">Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="d14a0-116">Geben Sie im Feld **Zahlungsbedingungen** einen entsprechenden Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="d14a0-117">Geben Sie in das Feld **Zeit zwischen Rechnungsfälligkeitsdatum und Zahlungsdatum** einen geeigneten Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="d14a0-118">Geben Sie im Feld **Standardsteuergruppe** eine Steuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="d14a0-119">Aktivieren Sie gegebenenfalls das Kontrollkästchen **Preise inkl. Mehrwertsteuer**.</span><span class="sxs-lookup"><span data-stu-id="d14a0-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="d14a0-120">Geben Sie ggf. im Feld **Standardabschreibungsgrund** einen geeigneten Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="d14a0-121">Das folgende Bild zeigt mehrere konfigurierte Kundengruppen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-121">The following image shows several configured customer groups.</span></span>

![Debitorengruppen](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="d14a0-123">Ein neues Debitorenadressbuch erstellen</span><span class="sxs-lookup"><span data-stu-id="d14a0-123">Create a customer address book</span></span>

<span data-ttu-id="d14a0-124">Ein Debitor muss mit einem Adressbuch verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="d14a0-125">Wenn noch keins erstellt wurde, müssen Sie eins erstellen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="d14a0-126">Gehen Sie folgendermaßen vor, um ein Adressbuch zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="d14a0-127">Gehen Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Kanaleinrichtung \> Adressbücher**.</span><span class="sxs-lookup"><span data-stu-id="d14a0-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="d14a0-128">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d14a0-129">Geben Sie im Kästchen **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="d14a0-130">Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="d14a0-131">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d14a0-132">Das folgende Bild zeigt ein Beispiel für ein Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="d14a0-132">The following image shows an example address book.</span></span>

![Adressbuch](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="d14a0-134">Einen Standarddebitoren erstellen</span><span class="sxs-lookup"><span data-stu-id="d14a0-134">Create a default customer</span></span>

<span data-ttu-id="d14a0-135">Gehen Sie folgendermaßen vor, um einen Standarddebitor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="d14a0-136">Wechseln Sie im Navigationsbereich zu **Module \> Retail und Commerce \> Debitoren \> Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="d14a0-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="d14a0-137">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d14a0-138">Wählen Sie in der Dropdownliste **Typ** „Person“ aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="d14a0-139">Wählen Sie in der Dropdownliste **Kundenkonto** eine Kontonummer aus (z. B. „100001”).</span><span class="sxs-lookup"><span data-stu-id="d14a0-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="d14a0-140">Wählen Sie in der Dropdownliste **Vorname** einen Namen aus, oder geben Sie einen Namen ein (z. B. „Standard”).</span><span class="sxs-lookup"><span data-stu-id="d14a0-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="d14a0-141">Wählen Sie in der Dropdownliste **Zweiter Vorname** einen Namen aus, oder geben Sie einen Namen ein (z. B. „Retail”).</span><span class="sxs-lookup"><span data-stu-id="d14a0-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="d14a0-142">Wählen Sie in der Dropdownliste **Nachname** einen Namen aus, oder geben Sie einen Namen ein (z. B. „Debitor”).</span><span class="sxs-lookup"><span data-stu-id="d14a0-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="d14a0-143">Wählen Sie in der Dropdownliste **Währung** eine Währung aus, oder geben Sie eine Währung ein (z. B. „USD”).</span><span class="sxs-lookup"><span data-stu-id="d14a0-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="d14a0-144">Wählen Sie in der Dropdownliste **Währung** die zuvor erstellte Debitorengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="d14a0-145">Wählen Sie in der Dropdownliste **Adressbücher** ein vorhandenes Debitorenadressbuch aus.</span><span class="sxs-lookup"><span data-stu-id="d14a0-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="d14a0-146">Wählen **Speichern**, um den neuen Debitor zu speichern und zum Debitorendetails-Bildschirm zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="d14a0-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="d14a0-147">Es ist nicht erforderlich, eine Adresse für einen Standarddebitoren hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d14a0-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="d14a0-148">Die folgende Abbildung zeigt ein Beispiel für die Erstellung eines Debitors.</span><span class="sxs-lookup"><span data-stu-id="d14a0-148">The following image shows an example of customer creation.</span></span>

![Erstellung eines Standarddebitors](media/default-customer-creation.png)

<span data-ttu-id="d14a0-150">Das folgende Bild zeigt die Konfiguration eines Standarddebitors.</span><span class="sxs-lookup"><span data-stu-id="d14a0-150">The following image shows a default customer configuration.</span></span>

![Beispieldebitorenkonfiguration](media/default-customer-configuration1.png)

<span data-ttu-id="d14a0-152">Die meisten Standardwerte auf dem Debitorendetailsbildschirm können beibehalten werden, es sollten jedoch zwei Werte geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d14a0-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="d14a0-153">Erweitern Sie auf dem Bildschirm mit den Kundendetails die Option **Standardwerte für Aufträge**.</span><span class="sxs-lookup"><span data-stu-id="d14a0-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="d14a0-154">Wählen Sie in der Dropdownliste **Site** eine vorkonfigurierte Site aus oder geben Sie sie ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="d14a0-155">Wählen Sie in der Dropdownliste **Lagerort** einen vorkonfigurierten Lagerort aus oder geben Sie einen ein.</span><span class="sxs-lookup"><span data-stu-id="d14a0-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="d14a0-156">Die folgende Abbildung zeigt ein Beispiel für die Konfiguration eines Debitors.</span><span class="sxs-lookup"><span data-stu-id="d14a0-156">The following image shows an example customer configuration.</span></span>

![Beispielkonfiguration eines Debitors](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="d14a0-158">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d14a0-158">Additional resources</span></span>

[<span data-ttu-id="d14a0-159">Kanäle – Übersicht</span><span class="sxs-lookup"><span data-stu-id="d14a0-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d14a0-160">Kanaleinstellungen – Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d14a0-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
