---
title: Erstellen einer Prozessvorlage in Attract
description: "Dieses Thema enthält informationabout, wie eine Prozeßvorlage in Attract erstellt wird."
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="a64f4-103">Erstellen einer Prozessvorlage in Attract</span><span class="sxs-lookup"><span data-stu-id="a64f4-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a64f4-104">Eine *Einstellungs-Prozessvorlage* enthält alle Aktivitäten, die im Rahmen des Einrichtungsprozesses für einen Stelle einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="a64f4-105">In diesem Thema werden die Elemente in einer Prozeßvorlage in Microsoft Dynamics 365 for Talent beschrieben: Attract.</span><span class="sxs-lookup"><span data-stu-id="a64f4-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="a64f4-106">Es wird auch erklärt, wie eine Vorlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a64f4-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="a64f4-107">Vorlagenerstellung ist Teil des umfassenden Add-On für Neueinstellungen für Attract.</span><span class="sxs-lookup"><span data-stu-id="a64f4-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="a64f4-108">Vorlagenverwaltung</span><span class="sxs-lookup"><span data-stu-id="a64f4-108">Template management</span></span>

<span data-ttu-id="a64f4-109">Organisationen können entscheiden, ob nur Administratoren oder auch Teammitglieder Prozeßvorlagen  erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a64f4-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="a64f4-110">Um die Vorlagenverwaltung zu konfigurieren, wechseln Sie zu **Administrator-Center** \> **Vorlagenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="a64f4-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="a64f4-111">Damit Teammitglieder eigene Vorlagen erstellen können, aktivieren Sie die Vorlagenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="a64f4-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="a64f4-112">Wenn Sie sie nicht aktivieren, können nur Administratoren Vorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="a64f4-113">Standardvorlage</span><span class="sxs-lookup"><span data-stu-id="a64f4-113">Default template</span></span>

<span data-ttu-id="a64f4-114">Nur Administratoren können Standardvorlagen festlegen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-114">Only admins can set the default template.</span></span> <span data-ttu-id="a64f4-115">Die Standardvorlage wird verwendet, wenn eine Vorlage nicht aktiviert ist, wenn ein Auftrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a64f4-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="a64f4-116">Um die Standard-Vorlage zu konfigurieren, wechseln Sie zu **Administrator-Center** \> **Vorlagenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="a64f4-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="a64f4-117">Auf der Karte für die Vorlage, die die Standardvorlage werden soll, markieren Sie die Schaltfläche (**...**) und wählen Sie dann **Als Standard festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="a64f4-118">Erstellen einer Prozessvorlage</span><span class="sxs-lookup"><span data-stu-id="a64f4-118">Create a process template</span></span>

<span data-ttu-id="a64f4-119">Administratoren, Personalverantwortliche und Manager können Prozessvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="a64f4-120">Eine Prozessvorlage besteht aus *Phasen* und *Aktivitäten*.</span><span class="sxs-lookup"><span data-stu-id="a64f4-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="a64f4-121">Gruppieren Sie Phasen in eine oder mehrere Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-121">Stages group together one or more activities.</span></span> <span data-ttu-id="a64f4-122">Standardmäßig hat jede Prozessvorlage Interessenten, Anwendungen und Angebotsaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="a64f4-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="a64f4-123">Die Phasen, die diese Aktivitäten enthalten, können umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="a64f4-124">Sie können mehrere Phasen hinzufügen, indem Sie **+ Neue Phase** auswählen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="a64f4-125">Sie können Aktivitäten in einer Phase entweder durch ziehen oder doppelklicken einer Aktivitätenliste zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="a64f4-126">Phasennamen sind für Kandidaten auf der Seite **Bewerbungsstatus** sichtbar.</span><span class="sxs-lookup"><span data-stu-id="a64f4-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="a64f4-127">Sie sollten diesen Tatsache berücksichtigen, wenn Sie Namen für Phasen auswählen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="a64f4-128">Weitere Informationen über Aktivitäten finden Sie unter [Einstelungsaktivitäten in Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="a64f4-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="a64f4-129">Folgen Sie diesen Schritten, um eine Einstellungsvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="a64f4-130">Gehen Sie zu **Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="a64f4-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="a64f4-131">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-131">Select **New**.</span></span>
3. <span data-ttu-id="a64f4-132">Geben Sie im Feld **Vorlagenname** einen Namen für die Vorlage ein, und wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="a64f4-133">In der Liste **Wählen Sie den gewünschten Genehmigungsprozess**wählen Sie **Standard**, um die Genehmigung für eine Stelle anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a64f4-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="a64f4-134">Wählen Sie aus, um Interessenten zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a64f4-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="a64f4-135">Optional: Hinzufügen oder Entfernen von Phasen.</span><span class="sxs-lookup"><span data-stu-id="a64f4-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="a64f4-136">Um eine Phase hinzufügen, wählen Sie **+ Neue Phase** aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="a64f4-137">Um eine Phase zu entfernen, zeigen Sie mit dem Mauszeiger auf die Phase, und wählen Sie dann die Abfalleimerschaltfläche aus, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a64f4-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a64f4-138">Interessenten-, Bewerbungs- und Angebotphasen können nicht entfernt werden, jedoch können sie umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="a64f4-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="a64f4-139">Optional: Hinzufügen oder Entfernen von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="a64f4-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="a64f4-140">Wenn Sie eine Aktivität hinzufügen möchten, ziehen Sie sie aus der Aktivitätsliste auf der rechten Seite in die entsprechende Phase.</span><span class="sxs-lookup"><span data-stu-id="a64f4-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="a64f4-141">Alternativ doppelklicken Sie auf die Aktivität, und wählen Sie dann zum Hinzufügen die aus Phase aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="a64f4-142">Um eine Aktion zu entfernen, erweitern Sie sie und wählen Sie dann die Abfalleimerschaltfläche im Feld Aktivitätskopf aus.</span><span class="sxs-lookup"><span data-stu-id="a64f4-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="a64f4-143">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a64f4-143">Select **Save**.</span></span>

