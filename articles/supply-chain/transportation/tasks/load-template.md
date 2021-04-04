---
title: Vorlagen laden
description: Dieses Thema beschreibt, wie Sie Ladungsvorlagen festlegen und wie Sie eine Ladungsvorlage mit einer neuen Ladung verknüpfen.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 80004b5d22e1cf81c1ffa9f74c2c479e1561df72
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247213"
---
# <a name="load-templates"></a><span data-ttu-id="1e1b4-103">Vorlagen laden</span><span class="sxs-lookup"><span data-stu-id="1e1b4-103">Load templates</span></span>

<span data-ttu-id="1e1b4-104">Wenn Sie eine neue Ladung erstellen, können Sie eine Ladungsvorlage zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="1e1b4-105">Die Beladungsvorlage enthält Informationen über das Equipment und über Kennzahlen wie Höhe, Breite, Tiefe und Volumen der Ladung.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="1e1b4-106">Dieses Thema beschreibt, wie Sie Ladungsvorlagen festlegen und wie Sie eine Ladungsvorlage mit einer neuen Ladung verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="1e1b4-107">Festlegen einer Ladung-Vorlage</span><span class="sxs-lookup"><span data-stu-id="1e1b4-107">Set up a load template</span></span>

1. <span data-ttu-id="1e1b4-108">Gehen Sie zu **Transportverwaltung \> Einrichten \> Ladungserstellung \> Ladungsvorlage**.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="1e1b4-109">Wählen Sie im Aktivitätsbereich **Neu**, um eine neue Vorlage hinzuzufügen oder **Bearbeiten**, um eine bestehende Vorlage zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="1e1b4-110">Legen Sie in der Zeile für die neue oder vorhandene Vorlage die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="1e1b4-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="1e1b4-111">**Ladevorlagen-ID** - Geben Sie einen eindeutigen Bezeichner (ID) für die Ladevorlage ein.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="1e1b4-112">**Ausrüstung** - Wählen Sie die Ausrüstung, die für den Versand der Ladung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="1e1b4-113">**Ladungshöhe**, **Ladungsbreite** und **Ladungstiefe** - Geben Sie die Dimensionen der Ladung ein.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="1e1b4-114">**Maximal zulässiges Ladevolumen** und **Maximal zulässiges Ladegewicht** - Geben Sie das maximal zulässige Volumen und Gewicht der Ladung ein.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="1e1b4-115">**Maximal zulässiges Bruttogewicht** - Geben Sie das maximal zulässige Bruttogewicht der Ladung ein.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="1e1b4-116">Das Bruttogewicht einer Ladung beinhaltet sowohl das Taragewicht als auch das Ladegewicht.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="1e1b4-117">**Maximal erlaubte Anzahl von Frachtstücken** - Geben Sie die maximale Anzahl von Frachtstücken ein, die die Ladung enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="1e1b4-118">**Ladung auf dem Boden stapeln** - Aktivieren Sie dieses Kontrollkästchen, um eine Bodenladung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="1e1b4-119">Bei einer Ladung auf dem Boden werden die Kisten innerhalb des Containers vom Boden bis zur Decke und von Wand zu Wand gestapelt, um die Kapazität zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="1e1b4-120">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="1e1b4-121">Verknüpfen einer Ladungsvorlage mit einer neuen Ladung</span><span class="sxs-lookup"><span data-stu-id="1e1b4-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="1e1b4-122">Gehen Sie zu **Transportverwaltung \> Planung \> Ladungsplanung Workbench**.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="1e1b4-123">Wählen Sie im oberen Teil der Seite eine der folgenden Registerkarten, je nachdem, für welche Art von Quelldokument Sie eine Ladung erstellen: **Sendungen**, **Verkaufszeilen**, **Übertragungszeilen** oder **Einkaufsbestellungen**.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="1e1b4-124">Wählen Sie das spezifische Dokument aus, für das die Ladung geplant werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="1e1b4-125">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Angebot und Nachfrage** in der Gruppe **Hinzufügen** die Option **Zu neuer Ladung** aus.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="1e1b4-126">Wählen Sie im Dialogfeld **Vorlage laden** im Feld **Vorlage-ID laden** die Vorlage, die Sie anwenden wollen.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="1e1b4-127">Wählen Sie **OK**, um die Vorlage anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="1e1b4-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]