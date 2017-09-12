---
title: Verbinden des Hilfesystems
description: "Dieses Thema beschreibt die Komponenten des Hilfesystems für Microsoft Dynamics 365 for Finance and Operation und enthält einen Überblick, wie sie verbunden und benutzerdefinierte Hilfen erstellt werden können."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="6cc6c-103">Verbinden des Hilfesystems</span><span class="sxs-lookup"><span data-stu-id="6cc6c-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6cc6c-104">In diesem Thema werden die Komponenten des Hilfesystems von Microsoft Dynamics 365 for Finance and Operations aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6cc6c-105">Es bietet einen Überblick darüber, wie diese Komponenten und eine Zusammenfassung zu aus, wie Sie benutzerdefinierte Hilfe erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="6cc6c-106">Hilfearchitektur</span><span class="sxs-lookup"><span data-stu-id="6cc6c-106">Help architecture</span></span>
<span data-ttu-id="6cc6c-107">Die folgende Abbildung zeigt Teile des Hilfesystems von Finance and Operations an.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="6cc6c-108">Das Hilfesystem zieht Artikel aus dem Finance and Operations-Website auf https://docs.microsoft.com und zeigt Aufgabenleitfäden aus dem Geschäftsprozessmodellierer in Microsoft Dynamics Lifecycle Services (LCS) an.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="6cc6c-109">Die Funktionen, die im Diagramm mit einem Sternchen (\*) aufgeführt sind (), sind geplant, aber noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="6cc6c-110">[![Hilfearchitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="6cc6c-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="6cc6c-111">Verbindung des Hilfesystems</span><span class="sxs-lookup"><span data-stu-id="6cc6c-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="6cc6c-112">Die Registerkarte **Aufgabenleitfäden** ist derzeit nicht in Microsoft Dynamics 365 for Talent und Microsoft Dynamics 365 for Retail verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="6cc6c-113">Wir arbeiten derzeit daran, diese Funktion in einer künftigen Version zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="6cc6c-114">Die Aufgabenleitfäden in der "Erste Schritte"-Erfahrung in Talent bleiben verfügbar, um Grundfunktionen abzudecken.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="6cc6c-115">Prozedurale Hilfe auf der docs.microsoft.com-Website ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) für Retail und Talent ebenfalls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="6cc6c-116">Mit dem Formular "**Systemparameter**" verbinden Systemadministratoren die Teile des Hilfesystems für eine Implementierung.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="6cc6c-117">[![Systemparameterformular aus Hilfeeinstellungen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Auf der Seite **Systemparameter** folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="6cc6c-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cc6c-118">Beim erstmaligen Öffnen der Registerkarte **Hilfe** müssen Sie die Verbindung zu den Lifecycle Services herstellen.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="6cc6c-119">Klicken Sie auf den Link mitten im Formular, warten Sie auf die Verbindung, schließen Sie das Dialogfeld, und klicken Sie anschließend auf **OK**, um zur Seite **Systemparameter** zu gelangen.[![Mit LCS verbinden](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="6cc6c-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="6cc6c-120">Wählen Sie das Projekt Lifecycle Services, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="6cc6c-121">Wählen Sie die BPM-Bibliotheken (innerhalb des ausgewählten Projekts) aus, von denen Sie die Aufgabenaufzeichnungen abrufen wollen.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="6cc6c-122">Für Finance and Operations wählen Sie für Microsoft-Inhalt die QPC vereinheitlichte Bibliothek für Microsoft Dynamics 365 for Finance and Operations, Februar 2017 aus.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="6cc6c-123">Für Retail wird im Juli eine Bibliothek veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="6cc6c-124">Für Talent muss keine Bibliothek ausgewählt werden – die Verbindung zur richtigen Bibliothek wird für Sie eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="6cc6c-125">Wählen Sie die Anzeigereihenfolge der BMP-Bibliotheken aus.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="6cc6c-126">So können Sie bestimmen, in welcher Reihenfolge Aufgabenaufzeichnungen aus den Bibliotheken im Bereich **Hilfe** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="6cc6c-127">Nachdem Sie diese Schritte abgeschlossen haben, können Sie den Bereich **Hilfe** öffnen und auf die Registerkarte **Aufgabenleitfäden** klicken.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="6cc6c-128">Sie finden nun die Aufgabenhandbücher, die für die Seite gelten, an denen Sie derzeit in Finance and Operations sind.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="6cc6c-129">Wenn keine Aufgabenhandbücher gefunden werden, können Sie Schlüsselwörter eingeben, um die Suche genauer zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="6cc6c-130">Zeigt übersetzte Aufgabenleitfäden</span><span class="sxs-lookup"><span data-stu-id="6cc6c-130">Showing translated task guides</span></span>

<span data-ttu-id="6cc6c-131">Übersetzte Aufgabenleitfäden wurden mit der APQC Unified Bibliothek (Mai 2016) und der Erste Schritte-Bibliothek zuerst geliefert.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="6cc6c-132">Um lokalisierte Aufgabenleitfäden in Finance and Operations anzuzeigen, stellen Sie sicher, dass die mit der Mai-Bibliothek verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="6cc6c-133">Die im Aufgabenleitfaden angezeigte Sprache wird für jeden Benutzer durch Spracheinstellungen unter **Optionen** &gt; **Voreinstellungen** gesteuert.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6cc6c-134">Auch wenn viele Aufgabenleitfäden übersetzt wurden, zeigt der Finance and Operations-Client im Moment nicht die übersetzten Namen der Aufgabenleitfäden an.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="6cc6c-135">Außerdem sind zum jetzigen Zeitpunkt nur die im Februar 2016 veröffentlichten Aufgabenleitfäden als Übersetzung in der Mai-Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="6cc6c-136">Wir werden eine aktualisierte Bibliothek mit zusätzlichen Übersetzung veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="6cc6c-137">Wenn ein Aufgabenleitfaden übersetzt wurde, wird beim Öffnen der gesamte Text des Leitfadens in der ausgewählten Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="6cc6c-138">Wenn ein Aufgabenleitfaden noch nicht übersetzt wurde, wird beim Öffnen nur ein Teil des Texts (der Text der Steuerelemente) in der ausgewählten Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="6cc6c-139">Erstellen einer benutzerdefinierten Hilfe</span><span class="sxs-lookup"><span data-stu-id="6cc6c-139">Creating custom help</span></span>
<span data-ttu-id="6cc6c-140">Sie können eine benutzerdefinierte Hilfe für Finance and Operations und für Retail erstellen, indem Sie Aufgabenaufzeichnungen erstellen, die die Implementierung widerspiegeln, und diese in einer LCS Business Process Library speichern.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="6cc6c-141">Sie können keine benutzerdefinierten Aufgabenleitfäden für Talent erstellen.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="6cc6c-142">Wenn Partner eine Bibliothek auf eine Unternehmensbibliothek hochstufen und in eine Lösung aufnehmen, wir diese für die Kunden verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="6cc6c-143">Sie können eine Kopie der globalen APQC Unified Bibliothek für Dynamics AX erstellen und dann Ihre Kopie öffnen, Aufgabenaufzeichnungen aus dieser öffnen, sie ändern und dann Aufzeichnungen mit den Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="6cc6c-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="6cc6c-144">Weitere Informationen finden Sie unter [Erstellen einer Aufgabenaufzeichnung als Dokumentation oder Schulung](../user-interface/task-recorder.md)...</span><span class="sxs-lookup"><span data-stu-id="6cc6c-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="6cc6c-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cc6c-145">See also</span></span>
--------

[<span data-ttu-id="6cc6c-146">Hilfe – Überblick</span><span class="sxs-lookup"><span data-stu-id="6cc6c-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="6cc6c-147">Über zur Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="6cc6c-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="6cc6c-148">Wie Sie Aufgabenaufzeichnungen zu Dokumentations- und Schulungszwecken erstellen</span><span class="sxs-lookup"><span data-stu-id="6cc6c-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





