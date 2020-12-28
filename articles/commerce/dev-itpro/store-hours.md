---
title: Erstellen und Aktualisieren von Geschäftszeiten
description: In diesem Thema wird beschrieben, wie Sie Geschäftszeiten in Commerce Zentralverwaltung anlegen und aktualisieren.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 4706432234437d2dc7943fb194cd01004ab7e6b7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687510"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="78d87-103">Erstellen und Aktualisieren von Geschäftszeiten</span><span class="sxs-lookup"><span data-stu-id="78d87-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="78d87-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="78d87-104">Overview</span></span>

<span data-ttu-id="78d87-105">Von einem einzigen Ort aus können Einzelhändler die Geschäftszeiten für verschiedene Filialen über geografische Regionen hinweg anlegen, pflegen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="78d87-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="78d87-106">Die Geschäftszeiten können dann an POS-Terminals angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="78d87-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="78d87-107">Auf diese Weise können die Kassierer die Ladenöffnungszeiten mit den Kunden teilen und den Käufern, die an Beständen in anderen Filialen interessiert sind, besser helfen.</span><span class="sxs-lookup"><span data-stu-id="78d87-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="78d87-108">Die Geschäftszeiten können auch auf Belegen gedruckt werden, falls der Kunde später in die Filiale zurückkehren möchte.</span><span class="sxs-lookup"><span data-stu-id="78d87-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="78d87-109">Mehrere Geschäftszeiten können über verschiedene Kanäle konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="78d87-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="78d87-110">Zu diesen Kanälen gehören Filialen, Call Center, mobile Geräte und E-Commerce-Sites.</span><span class="sxs-lookup"><span data-stu-id="78d87-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="78d87-111">Wenn ein Kunde einen Abholauftrag für eine andere Filiale hat, kann der Kassierer einen Termin auswählen, an dem die Abholung in dieser Filiale verfügbar sein wird.</span><span class="sxs-lookup"><span data-stu-id="78d87-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="78d87-112">Das Store Lookup liefert einen Verweis auf die Daten und Zeiten des Ladens.</span><span class="sxs-lookup"><span data-stu-id="78d87-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="78d87-113">Der Kassierer kann ein Datum und einen Ort auswählen und einen Abholbeleg mit den Geschäftszeiten ausdrucken.</span><span class="sxs-lookup"><span data-stu-id="78d87-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="78d87-114">Diese Funktionalität ist in Microsoft Dynamics 365 Retail ab Version 8.1.2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78d87-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="78d87-115">Konfigurieren der Geschäftszeiten</span><span class="sxs-lookup"><span data-stu-id="78d87-115">Configure store hours</span></span>

<span data-ttu-id="78d87-116">Führen Sie diese Schritte aus, um die Geschäftszeiten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="78d87-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="78d87-117">Gehen Sie zu **Retail und Commerce** \> **Kanaleinrichtung** \> **Öffnungszeiten**.</span><span class="sxs-lookup"><span data-stu-id="78d87-117">Go to **Retail and Commerce** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="78d87-118">Wählen Sie **Neu**, um eine neue Geschäftszeitenvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78d87-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="78d87-119">Um eine vorhandene Vorlage zu verwenden, wählen Sie die Vorlage im linken Bereich aus.</span><span class="sxs-lookup"><span data-stu-id="78d87-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="78d87-120">Definieren Sie im Dialogfenster **Hinzufügen Bereich** den Datumsbereich, die Geschäftszeiten und eventuell erforderliche Feiertage.</span><span class="sxs-lookup"><span data-stu-id="78d87-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="78d87-121">Wenn sich die Geschäftszeiten nicht ändern, wählen Sie **Nie endet** im Feld **Enddatum**.</span><span class="sxs-lookup"><span data-stu-id="78d87-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="78d87-122">Wenn die Geschäftszeiten für einen bestimmten Monat, eine bestimmte Woche oder einen bestimmten Tag gelten, setzen Sie die entsprechenden Daten in den Feldern **Startdatum** und **Enddatum**.</span><span class="sxs-lookup"><span data-stu-id="78d87-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="78d87-123">Sie können mehrere Vorlagen erstellen, deren Start- und Enddatum sich überschneiden.</span><span class="sxs-lookup"><span data-stu-id="78d87-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="78d87-124">So können Sie z.B. für Filialen in verschiedenen Zeitzonen Geschäftszeiten definieren.</span><span class="sxs-lookup"><span data-stu-id="78d87-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="78d87-125">![Dialogfeld Bereich hinzufügen](../dev-itpro/media/Storehours1.png "Dialogfeld Bereich hinzufügen")</span><span class="sxs-lookup"><span data-stu-id="78d87-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="78d87-126">Ordnen Sie die Ladenöffnungsvorlage den Filialen zu, in denen sie verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78d87-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="78d87-127">Wählen Sie im Dialogfenster **Organisationsknoten auswählen** die Filialen, Regionen und Organisationen aus, denen die Vorlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78d87-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="78d87-128">Jeder Filiale kann nur eine Ladenöffnungsvorlage zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="78d87-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="78d87-129">Verwenden Sie die Pfeiltasten, um Filialen, Regionen oder Organisationen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="78d87-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="78d87-130">Der Kalender steht den Filialen oder Filialgruppen zur Verfügung und ist am POS als Referenz sichtbar.</span><span class="sxs-lookup"><span data-stu-id="78d87-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="78d87-131">![Dialogfeld-Organisationsknoten auswählen](../dev-itpro/media/Storehours2.png "Auswählen des Organisationsknoten-Dialogfensters")</span><span class="sxs-lookup"><span data-stu-id="78d87-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="78d87-132">Führen Sie auf der Seite **Verteilungsplan** die Jobs **1070** und **1090** aus, um die Geschäftszeiten für die Kasse verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="78d87-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="78d87-133">Hinzufügen von Geschäftszeiten zu gedruckten Belegen</span><span class="sxs-lookup"><span data-stu-id="78d87-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="78d87-134">Führen Sie diese Schritte aus, um den gedruckten Kassenbelegen Geschäftszeiten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="78d87-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="78d87-135">Öffnen Sie den Beleg-Designer.</span><span class="sxs-lookup"><span data-stu-id="78d87-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="78d87-136">Wählen Sie **Fußzeile** in der linken unteren Ecke.</span><span class="sxs-lookup"><span data-stu-id="78d87-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="78d87-137">Ziehen Sie das Element **Geschäftszeiten** aus dem linken Bereich in die Fußzeile am unteren Rand der Belegablage.</span><span class="sxs-lookup"><span data-stu-id="78d87-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="78d87-138">Sie können die Standardbeschriftung auf dem Element **Geschäftszeiten** beliebig bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="78d87-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="78d87-139">Speichern Sie den Beleg und schließen Sie den Belegdesigner.</span><span class="sxs-lookup"><span data-stu-id="78d87-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="78d87-140">Führen Sie auf der Seite **Verteilungsplan** die Jobs **1070** und **1090** aus.</span><span class="sxs-lookup"><span data-stu-id="78d87-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="78d87-141">Melden Sie sich am POS an.</span><span class="sxs-lookup"><span data-stu-id="78d87-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="78d87-142">Schließen Sie einen Verkauf ab und wählen Sie, um eine Quittung zu drucken.</span><span class="sxs-lookup"><span data-stu-id="78d87-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="78d87-143">Die Bons enthalten nun auch die Geschäftszeiten.</span><span class="sxs-lookup"><span data-stu-id="78d87-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="78d87-144">Wenn in der Vorlage Feiertage enthalten waren, werden diese auf dem Beleg angezeigt.</span><span class="sxs-lookup"><span data-stu-id="78d87-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="78d87-145">![Belegbeispiel](../dev-itpro/media/Storehours3.png "Belegbeispiel")</span><span class="sxs-lookup"><span data-stu-id="78d87-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
