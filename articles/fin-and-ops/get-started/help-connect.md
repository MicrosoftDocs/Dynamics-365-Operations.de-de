---
title: Verbinden des Hilfesystems
description: Dieses Thema beschreibt die Komponenten des Hilfe-Systems für Microsoft Dynamics 365 for Finance and Operations und bietet einen Überblick, wie sie verbunden werden, und eine Zusammenfassung, wie benutzerdefinierte Hilfe erstellt werden kann.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 929e453987c6e2773d1886d03a4393a68033566b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850900"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="07a8c-103">Verbinden des Hilfesystems</span><span class="sxs-lookup"><span data-stu-id="07a8c-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07a8c-104">In diesem Thema werden die Komponenten des Hilfesystems von Microsoft Dynamics 365 for Finance and Operations aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="07a8c-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="07a8c-105">Es bietet einen Überblick darüber, wie diese Komponenten und eine Zusammenfassung zu aus, wie Sie benutzerdefinierte Hilfe erstellt.</span><span class="sxs-lookup"><span data-stu-id="07a8c-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="07a8c-106">Hilfearchitektur</span><span class="sxs-lookup"><span data-stu-id="07a8c-106">Help architecture</span></span>

<span data-ttu-id="07a8c-107">Die folgende Abbildung zeigt Teile des Hilfesystems von Finance and Operations an.</span><span class="sxs-lookup"><span data-stu-id="07a8c-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="07a8c-108">Das Hilfesystem zieht Artikel aus dem Finance and Operations-Website auf https://docs.microsoft.com und zeigt Aufgabenleitfäden aus dem Geschäftsprozessmodellierer in Microsoft Dynamics Lifecycle Services (LCS) an.</span><span class="sxs-lookup"><span data-stu-id="07a8c-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="07a8c-109">Die Funktionen, die im Diagramm mit einem Sternchen (\*) aufgeführt sind (), sind geplant, aber noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07a8c-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="07a8c-110">[![Hilfearchitektur](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="07a8c-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="07a8c-111">Verbindung des Hilfesystems</span><span class="sxs-lookup"><span data-stu-id="07a8c-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="07a8c-112">Die Registerkarte **Aufgabenleitfäden** ist derzeit nicht in Microsoft Dynamics 365 for Talent und Microsoft Dynamics 365 for Retail verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07a8c-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="07a8c-113">Wir arbeiten derzeit daran, diese Funktion in einer künftigen Version zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="07a8c-114">Die Aufgabenleitfäden in der "Erste Schritte"-Erfahrung in Talent bleiben verfügbar, um Grundfunktionen abzudecken.</span><span class="sxs-lookup"><span data-stu-id="07a8c-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="07a8c-115">Prozedurale Hilfe auf der docs.microsoft.com-Website ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) für Retail und Talent ebenfalls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07a8c-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="07a8c-116">Mit dem Formular "**Systemparameter**" verbinden Systemadministratoren die Teile des Hilfesystems für eine Implementierung.</span><span class="sxs-lookup"><span data-stu-id="07a8c-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="07a8c-117">[![Systemparameterformular mit Hilfe-Einstellungen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="07a8c-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="07a8c-118">Gehen Sie auf der Seite **Systemparameter** folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="07a8c-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="07a8c-119">Beim erstmaligen Öffnen der Registerkarte **Hilfe** müssen Sie die Verbindung zu den Lifecycle Services herstellen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="07a8c-120">Klicken Sie auf den Link mitten im Formular, warten Sie auf die Verbindung, schließen Sie das Dialogfeld, und klicken Sie anschließend auf **OK**, um zur Seite **Systemparameter** zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="07a8c-121">[![Mit LCS verbinden](./media/connect-to-lcs-crop-1024x365.png "Mit LCS verbinden")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="07a8c-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="07a8c-122">Wählen Sie das Projekt Lifecycle Services, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="07a8c-123">Wählen Sie die BPM-Bibliotheken (innerhalb des ausgewählten Projekts) aus, von denen Sie die Aufgabenaufzeichnungen abrufen wollen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="07a8c-124">Für Finance and Operations wählen Sie für Microsoft-Inhalt die aktuellste APQC vereinheitlichte Bibliothek für Microsoft Dynamics 365 for Finance and Operations aus.</span><span class="sxs-lookup"><span data-stu-id="07a8c-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="07a8c-125">Für Retail wird bald eine Bibliothek veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="07a8c-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="07a8c-126">Für Talent muss keine Bibliothek ausgewählt werden – die Verbindung zur richtigen Bibliothek wird für Sie eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="07a8c-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="07a8c-127">Wählen Sie die Anzeigereihenfolge der BMP-Bibliotheken aus.</span><span class="sxs-lookup"><span data-stu-id="07a8c-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="07a8c-128">So können Sie bestimmen, in welcher Reihenfolge Aufgabenaufzeichnungen aus den Bibliotheken im Bereich **Hilfe** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07a8c-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="07a8c-129">Wenn Sie zuerst den Hilfebereich öffnen und auf die Registerkarte **Hilfe** und dann **Aufgabenleitfaden** klicken, finden Sie die Artikel, die für die Seite gelten, an denen Sie derzeit in Finance and Operations sind.</span><span class="sxs-lookup"><span data-stu-id="07a8c-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="07a8c-130">Wenn keine Aufgabenhandbücher gefunden werden, können Sie Schlüsselwörter eingeben, um die Suche genauer zu definieren.</span><span class="sxs-lookup"><span data-stu-id="07a8c-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="07a8c-131">Zeigt übersetzte Aufgabenleitfäden</span><span class="sxs-lookup"><span data-stu-id="07a8c-131">Showing translated task guides</span></span>

<span data-ttu-id="07a8c-132">Übersetzte Aufgabenleitfäden wurden mit der APQC Unified Bibliothek (Mai 2016) und der Erste Schritte-Bibliothek zuerst geliefert.</span><span class="sxs-lookup"><span data-stu-id="07a8c-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="07a8c-133">Um lokalisierte Aufgabenleitfäden in Finance and Operations anzuzeigen, stellen Sie sicher, dass die mit der Mai-Bibliothek verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="07a8c-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="07a8c-134">Die im Aufgabenleitfaden angezeigte Sprache wird für jeden Benutzer durch Spracheinstellungen unter **Optionen** &gt; **Voreinstellungen** gesteuert.</span><span class="sxs-lookup"><span data-stu-id="07a8c-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="07a8c-135">Auch wenn viele Aufgabenleitfäden übersetzt wurden, zeigt der Finance and Operations-Client im Moment nicht die übersetzten Namen der Aufgabenleitfäden an.</span><span class="sxs-lookup"><span data-stu-id="07a8c-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="07a8c-136">Außerdem sind zum jetzigen Zeitpunkt nur die im Februar 2016 veröffentlichten Aufgabenleitfäden als Übersetzung in der Mai-Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07a8c-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="07a8c-137">Wir werden eine aktualisierte Bibliothek mit zusätzlichen Übersetzung veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="07a8c-138">Wenn ein Aufgabenleitfaden übersetzt wurde, wird beim Öffnen der gesamte Text des Leitfadens in der ausgewählten Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07a8c-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="07a8c-139">Wenn ein Aufgabenleitfaden noch nicht übersetzt wurde, wird beim Öffnen nur ein Teil des Texts (der Text der Steuerelemente) in der ausgewählten Sprache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07a8c-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="07a8c-140">Erstellen einer benutzerdefinierten Hilfe</span><span class="sxs-lookup"><span data-stu-id="07a8c-140">Creating custom help</span></span>

<span data-ttu-id="07a8c-141">Sie können Aufgabenleitfäden verwenden, um benutzerdefinierte Hilfe zu erstellen, oder eine Verbindung zwischen einer Website und dem Hilfebereich erstellen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="07a8c-142">Benutzerdefinierte Hilfe mit Aufgabenleitfäden erstellen</span><span class="sxs-lookup"><span data-stu-id="07a8c-142">Create custom help with task guides</span></span>

<span data-ttu-id="07a8c-143">Sie können eine benutzerdefinierte Hilfe für Finance and Operations und für Retail erstellen, indem Sie Aufgabenaufzeichnungen erstellen, die die Implementierung widerspiegeln, und diese in einer LCS Business Process Library speichern.</span><span class="sxs-lookup"><span data-stu-id="07a8c-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="07a8c-144">Sie können keine benutzerdefinierten Aufgabenleitfäden für Talent erstellen.</span><span class="sxs-lookup"><span data-stu-id="07a8c-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="07a8c-145">Wenn Partner eine Bibliothek auf eine Unternehmensbibliothek hochstufen und in eine Lösung aufnehmen, wir diese für die Kunden verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07a8c-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="07a8c-146">Sie können eine Kopie der globalen APQC Unified Bibliothek für Dynamics AX erstellen und dann Ihre Kopie öffnen, Aufgabenaufzeichnungen aus dieser öffnen, sie ändern und dann Aufzeichnungen mit den Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="07a8c-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="07a8c-147">Weitere Informationen finden Sie unter [Erstellen einer Aufgabenaufzeichnung als Dokumentation oder Schulung](../../dev-itpro/user-interface/task-recorder.md)...</span><span class="sxs-lookup"><span data-stu-id="07a8c-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="07a8c-148">Benutzerdefinierte Website verbinden</span><span class="sxs-lookup"><span data-stu-id="07a8c-148">Connect a custom site</span></span>

<span data-ttu-id="07a8c-149">Microsoft hat ein Whitepaper und einen Beispielcode bereitgestellt, die beschreiben wie ein benutzerdefinierter Hilfewebsite mit dem Hilfebereich verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="07a8c-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="07a8c-150">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="07a8c-150">For more information, see:</span></span>

- [<span data-ttu-id="07a8c-151">Benutzerdefinierte Hilfe für Finance and Operations erstellen (Whitepaper)</span><span class="sxs-lookup"><span data-stu-id="07a8c-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="07a8c-152">Benutzerdefiniertes Hilfe-GitHub-Repository</span><span class="sxs-lookup"><span data-stu-id="07a8c-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="07a8c-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="07a8c-153">Additional resources</span></span>

[<span data-ttu-id="07a8c-154">Hilfe – Überblick</span><span class="sxs-lookup"><span data-stu-id="07a8c-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="07a8c-155">Über zur Aufgabenaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="07a8c-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="07a8c-156">Wie Sie Aufgabenaufzeichnungen zu Dokumentations- und Schulungszwecken erstellen</span><span class="sxs-lookup"><span data-stu-id="07a8c-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
