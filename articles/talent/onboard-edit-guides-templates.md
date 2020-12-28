---
title: Bearbeiten von Onboarding-Anleitungen und Vorlagen in Dynamics 365 Talent - Onboard
description: In diesem Thema wird erläutert, wie die Aktivitäten und anderen Informationen Onboarding Anleitungen und Vorlagen in Microsoft Dynamics 365 Talent - Onboard hinzugefügt werden.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 291f7aefac61c26dfab81cfff28c1c6580d46de5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461298"
---
# <a name="edit-onboarding-guides-and-templates"></a><span data-ttu-id="1d49a-103">Bearbeiten von Onboarding Anleitungen und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="1d49a-103">Edit onboarding guides and templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d49a-104">Nachdem Sie ein Onboarding Anleitung oder eine Vorlage erstellt haben in Microsoft Dynamics 365 Talent: Onboard, müssen Sie eine Einleitung, Aktivitäten, Kontakte und Ressourcen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="1d49a-105">Mit Onboard können Sie umfangreiche Inhalte der Onboarding-Anleitung hinzufügen, inklusive:</span><span class="sxs-lookup"><span data-stu-id="1d49a-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="1d49a-106">YouTube Videos</span><span class="sxs-lookup"><span data-stu-id="1d49a-106">YouTube videos</span></span>
- <span data-ttu-id="1d49a-107">Microsoft Sway Präsentationen</span><span class="sxs-lookup"><span data-stu-id="1d49a-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="1d49a-108">Microsoft PowerApps Apps</span><span class="sxs-lookup"><span data-stu-id="1d49a-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="1d49a-109">Microsoft Stream Videos</span><span class="sxs-lookup"><span data-stu-id="1d49a-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="1d49a-110">Microsoft Forms Formulare</span><span class="sxs-lookup"><span data-stu-id="1d49a-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="1d49a-111">Iframes, das den Webinhalt enthält</span><span class="sxs-lookup"><span data-stu-id="1d49a-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="1d49a-112">Bearbeiten Sie die Einführungen oder Aktivitäten, die anhand einer Vorlage importiert werden</span><span class="sxs-lookup"><span data-stu-id="1d49a-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="1d49a-113">Wenn Sie ein Onboarding Handbuch aus einer Vorlage erstellen oder wenn Sie Aktivitäten aus einer Vorlage in andere importieren, sehen Sie eine Schaltfläche **Sperren** für die importierten Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="1d49a-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="1d49a-114">Diese werden *verwaltete Aktivitäten* genannt.</span><span class="sxs-lookup"><span data-stu-id="1d49a-114">These are called *managed activities*.</span></span>

<span data-ttu-id="1d49a-115">[![Verwaltete Aktivitäten](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="1d49a-116">Wenn Sie eine verwaltete Aktivität auswählen, können Sie die Quellvorlage oben an der Aktivität anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="1d49a-117">[![Verwaltete Aktivitätsquelle](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="1d49a-118">Wenn Sie eine Aktivität in einer Vorlage bearbeiten, überträgt Onboard die Änderungen per Push auf alle Anleitungen, Vorlagen und ungesendeten Anleitungen, die auf dieser Vorlage basieren.</span><span class="sxs-lookup"><span data-stu-id="1d49a-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="1d49a-119">Wenn Sie ein ungesendetes Handbuch auf Basis einer Vorlage auswählen, die Sie bearbeitet haben und dann die Registerkarte  **Aktivitäten** im Handbuch auswählen, lesen Sie einen Hinweis, dass die Anleitung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1d49a-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="1d49a-120">Wenn Sie die Benachrichtigung ablehnen, wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="1d49a-121">[![Benachrichtigung ändern](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="1d49a-122">Sie finden einen schwarzen Fleck neben den aktualisierten Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="1d49a-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="1d49a-123">[![Aktivität geändert](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="1d49a-124">Sie können Aktivitäten nicht außerhalb der ursprünglichen Vorlage verwalten mit Ausnahme der nicht bearbeiten, um eine zugewiesener Person, Fälligkeitsdatum oder andere Informationen im rechten Bereich der Aktivität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="1d49a-125">Wenn Sie eine verwaltete Aktivität bearbeiten möchten oder wenn Sie keine Aktivität von Aktualisierungen der Vorlage erhalten möchten, wählen Sie die Schaltfläche **Sperren** für diese Aktivität.</span><span class="sxs-lookup"><span data-stu-id="1d49a-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="1d49a-126">Die Schaltfläche **Sperren** wird nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d49a-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="1d49a-127">Die Aktivität wird nicht mehr von der ursprüngliche Vorlage verwaltet und erhält keine weiteren Aktualisierungen aus der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="1d49a-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="1d49a-128">Aktualisierungen, die für eine Aktivität vornehmen, haben keinen Einfluss auf die ursprüngliche Vorlage.</span><span class="sxs-lookup"><span data-stu-id="1d49a-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="1d49a-129">Wenn Sie eine Aktivität von einer Anleitung löschen und Änderungen aus der Vorlage dieser Anleitung puschen, bleibt die Aktivität gelöscht in der Anleitung.</span><span class="sxs-lookup"><span data-stu-id="1d49a-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="1d49a-130">Kontakte und Ressourcen werden nicht von Vorlagen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1d49a-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="1d49a-131">Darüber hinaus werden Abschnitte nicht verwaltet, wenn Sie einen Abschnitt in einer Vorlage hinzufügen oder bearbeiten, werden die Änderungen nicht auf Anleitungen oder Vorlagen gepusht,  die auf dieser Vorlage basieren.</span><span class="sxs-lookup"><span data-stu-id="1d49a-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="1d49a-132">Wenn Sie neue Aktivitäten einer Vorlage hinzufügen, werden die neuen Aktivitäten auf die Anleitungen und Vorlagen basierende auf dieser Vorlage gepusht und neue Aktivitäten werden oben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d49a-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="1d49a-133">Importieren von Aktivitäten aus einer anderen Vorlage</span><span class="sxs-lookup"><span data-stu-id="1d49a-133">Import activities from another template</span></span>

<span data-ttu-id="1d49a-134">Sie können Aktivitäten aus einer oder mehrerer Vorlagen in eine Anleitung oder Vorlage importieren.</span><span class="sxs-lookup"><span data-stu-id="1d49a-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="1d49a-135">Wählen Sie die Anleitung oder Vorlage, die Sie bearbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="1d49a-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="1d49a-136">Wählen Sie die Registerkarte **Aktivitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="1d49a-137">Wählen Sie die Registerkarte **Importieren** im Abschnitt auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="1d49a-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="1d49a-138">[![Importieren Sie Aktivitäten](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="1d49a-139">Um die Aufgaben im Vergleich zur Registerkarte in Ihrem Browser in der Vorschau anzuzeigen, wählen Sie die Schaltfläche **Öffnen in neuer Registerkarte** auf einer beliebigen Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="1d49a-140">[![Importieren Sie Aktivitäten](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="1d49a-141">Drag & Drop der gewünschten Vorlage an den Ort in der Anleitungsvorlage, in dem die Aktivitäten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="1d49a-142">Setzt das Bearbeiten der Anleitung oder der Vorlage fort.</span><span class="sxs-lookup"><span data-stu-id="1d49a-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="1d49a-143">Die importierten Aktivitäten beinhalten eine Schaltfläche **Sperren**, die anzeigt, dass diese Aktivitäten verwaltet werden von der Vorlage, aus er Sie importiert haben.</span><span class="sxs-lookup"><span data-stu-id="1d49a-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="1d49a-144">Wenn Sie Änderungen vornehmen an der Vorlage, die Sie importiert haben, werden diese Aktivitäten in der Vorlage aktualisiert, in die Sie importiert haben.</span><span class="sxs-lookup"><span data-stu-id="1d49a-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="1d49a-145">Allerdings werden die Änderungen nicht automatisch zu einer beliebigen Anleitung gepusht aus der Vorlage erstellt haben, in die Sie importiert haben.</span><span class="sxs-lookup"><span data-stu-id="1d49a-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="1d49a-146">Push ändert sich von einer Vorlage in eine andere Vorlage oder eine Anleitung</span><span class="sxs-lookup"><span data-stu-id="1d49a-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="1d49a-147">Wenn sie eine Vorlage bearbeiten, die Aktivitäten enthält, die in anderen Vorlagen oder in Anleitungen verwendet werden, müssen die Änderungen gepusht werden. wenn diese in anderen Vorlagen oder in den Anleitungen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="1d49a-148">Wenn Sie nicht sicher sind, ob die Aktivitäten der Vorlage in anderen Vorlagen oder in Anleitungen verwendet werden, wählen Sie die Registerkarte **Verwendet in** aus, um anzuzeigen, wo diese Aktivitäten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d49a-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="1d49a-149">[![Hier finden Sie Anleitungen und  Vorlagenaktivitäten, die verwendet werden in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="1d49a-150">Um Ihre Änderungen zu pushen:</span><span class="sxs-lookup"><span data-stu-id="1d49a-150">To push your changes:</span></span>

1. <span data-ttu-id="1d49a-151">Speichert die Änderungen, **Speichern** indem Sie die Schaltfläche auswählen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="1d49a-152">Wenn Sie keine Auswahl treffen, werden Sie aufgefordert, im nächsten Schritt die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1d49a-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="1d49a-153">Wählen Sie **Diese Änderungen pushen**.</span><span class="sxs-lookup"><span data-stu-id="1d49a-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="1d49a-154">Hinzufügen oder bearbeiten Sie eine Einleitung</span><span class="sxs-lookup"><span data-stu-id="1d49a-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="1d49a-155">Auf der Registerkarte **Einführung** geben Sie einen Titel für Anleitung und eine Öffnungsnachricht ein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="1d49a-156">Um den Beispieltext zu verwenden, wählen Sie **Verwenden Sie diese Meldung**.</span><span class="sxs-lookup"><span data-stu-id="1d49a-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="1d49a-157">[![Einführungsregisterkarte in einer Onboard Vorlage](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="1d49a-158">Verwenden Sie die Formatierungsschaltflächen, um Text auszurufen, wie Sie ihn benötigen, oder um Links oder Bilder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="1d49a-159">Wählen Sie **Speichern** aus, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1d49a-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="1d49a-160">Hinzufügen oder Bearbeiten auswählen</span><span class="sxs-lookup"><span data-stu-id="1d49a-160">Add or edit activities</span></span>

1. <span data-ttu-id="1d49a-161">Auf der Registerkarte **Aktivitäten** ziehen Sie Artikel von Rechts in den Bearbeitungsbereich.</span><span class="sxs-lookup"><span data-stu-id="1d49a-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="1d49a-162">Um Ihre Anleitung in Abschnitte zu organisieren, ziehen Sie das Element **Neuer Abschnitt** in den zu bearbeitenden Bereich und geben einen Namen und eine optionale Beschreibung für den Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="1d49a-163">Hinzufügen eines neuen Abschnitts zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage</span><span class="sxs-lookup"><span data-stu-id="1d49a-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="1d49a-164">Um die Aktivitäten hinzuzufügen, um die Einstellung abzuschließen, ziehen Sie das Element **Neue Aktivität** in den zu bearbeitenden Bereich und geben Sie einen Namen und eine Beschreibung für die Aktivität ein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="1d49a-165">Hinzufügen einer neuen Aktivität zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage</span><span class="sxs-lookup"><span data-stu-id="1d49a-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="1d49a-166">Fügen Sie umfangreichen Inhalt Ihrer Onboarding Anleitung hinzu:</span><span class="sxs-lookup"><span data-stu-id="1d49a-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="1d49a-167">Um ein YouTube Videodatei hinzuzufügen, ziehen Sie den Artikel des zu bearbeitenden Bereichs **YouTube**, geben Sie einen Namen und eine Beschreibung für die Aktivität ein, und geben Sie die URL für die YouTube Videodatei ein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="1d49a-168">Um eine Sway Präsentation oder einen Newsletter hinzufügen, ziehen Sie das Element **Sway** in den zu bearbeitenden Bereich und geben einen Namen und eine Beschreibung für die Aktivität oder die eingebettete URL für die Sway Präsentation oder den Newsletter ein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="1d49a-169">Um eine Microsoft Power Apps-App hinzuzufügen, ziehen Sie den Artikel in den zu bearbeitenden Bereich **Power Apps**, geben Sie einen Namen und eine Beschreibung für die Aktivität ein, und wählen Sie entweder die Power Apps-App oder die Power Apps-App Kennung ein</span><span class="sxs-lookup"><span data-stu-id="1d49a-169">To add a Microsoft Power Apps app, drag the **Power Apps** item to the editing area, enter a name and description for the activity, and either select the Power Apps app or enter the Power Apps app ID.</span></span>
    - <span data-ttu-id="1d49a-170">Um ein Microsoft Stream Videodatei hinzuzufügen, ziehen Sie den Artikel des zu bearbeitenden Bereichs **Microsoft Stream**, geben Sie einen Namen und eine Beschreibung für die Aktivität ein, und geben Sie die URL für die Microsoft Stream Videodatei ein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="1d49a-171">Um ein Microsoft Forms-Formular hinzuzufügen, ziehen Sie den Artikel in den zu bearbeitenden Bereich **Microsoft Forms**, geben Sie einen Namen und eine Beschreibung für die Aktivität, die URL für das Microsoft Forms-Formular ein, und geben Sie die Größe des Bildschirmbereichs an.</span><span class="sxs-lookup"><span data-stu-id="1d49a-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="1d49a-172">Um einen iFrame hinzuzufügen, der Internetinhalt enthält, ziehen Sie das Element **Web Inhalt (iFrame)** in den zu bearbeitenden Bereich, geben einen Namen und eine Beschreibung ein, geben die URL für den Internetinhalt ein und definieren die Größe des Bildschirmbereichs.</span><span class="sxs-lookup"><span data-stu-id="1d49a-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="1d49a-173">Hinzufügen eines umfangreichen Inhalts zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage</span><span class="sxs-lookup"><span data-stu-id="1d49a-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="1d49a-174">Optional: Im Bereich auf der rechten Seite weisen Sie jeder Aktivität eine bestimmte Person oder einer Rolle die Aktivität zu, fügen Sie ein Fälligkeitsdatum und eine Kontaktperson ein, und weisen Sie eine Kategoriefarbe zu.</span><span class="sxs-lookup"><span data-stu-id="1d49a-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="1d49a-175">Wenn Sie eine Person oder einer Rolle einer Aktivität zuweisen, wird eine Aufgabe für jede Person erstellt.</span><span class="sxs-lookup"><span data-stu-id="1d49a-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="1d49a-176">Diese Aufgabe wird im Onboard Menü unter **Aufgaben** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d49a-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="1d49a-177">[![Zuweisen einer Aktivität in eine Onboarding Anleitung oder Vorlage](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="1d49a-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="1d49a-178">Wählen Sie **Speichern** aus, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1d49a-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="1d49a-179">Wenn Sie eine Aktivität oder einen Abschnitt löschen, tun Sie dies, indem Sie die Schaltfläche **Löschen** (das Abfalleimersymbol) in der oberen rechten Ecke der Aktivität oder des Abschnitts auswählen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="1d49a-180">Um die Aktivitäten und Abschnitte neu anzuordnen, ziehen Sie sie an einen neuen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1d49a-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="1d49a-181">Kontakte hinzufügen oder bearbeiten</span><span class="sxs-lookup"><span data-stu-id="1d49a-181">Add or edit contacts</span></span>

<span data-ttu-id="1d49a-182">Sie können Kontaktpersonen hinzufügen, die Ihre neuen Mitarbeiter von Beginn weg unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="1d49a-183">Diese Kontakte können Personalverantwortliche, Teamkollegen, Onboarding-Kollegen, Mentoren, Administratoren und IT-Supportmitarbeiter sein.</span><span class="sxs-lookup"><span data-stu-id="1d49a-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="1d49a-184">Auf der Registerkarte **Kontakte** wählen Sie **Neuen Kontakt** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="1d49a-185">Im Dialogfeld **Fügen Sie Teammitglied hinzu** geben Sie den Namen oder die E-Mail-Adresse der Kontaktperson ein, eine kurze Beschreibung, die erläutert, wie die Kontaktperson den neuen Mitarbeiter unterstützen kann und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="1d49a-186">Hinzufügen eines Kontakts zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage</span><span class="sxs-lookup"><span data-stu-id="1d49a-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="1d49a-187">Alternativ können Sie einen oder mehrere Kontakte unter **Vorschlägen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="1d49a-188">Wählen Sie **Speichern** aus, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1d49a-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="1d49a-189">Um einen Kontakt zu löschen, wählen Sie die Schaltfläche **Löschen** (Abfalleimersymbol), das rechts neben dem Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="1d49a-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="1d49a-190">Um einen Kontakt zu bearbeiten, wählen Sie die Schaltfläche **Bearbeiten** (Stiftsymbol), das rechts neben dem Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="1d49a-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="1d49a-191">Ressourcen hinzufügen oder bearbeiten</span><span class="sxs-lookup"><span data-stu-id="1d49a-191">Add or edit resources</span></span>

<span data-ttu-id="1d49a-192">Sie können nützliche Dateien, Zuordnungen und Links im Abschnitt **Ressourcen** Ihrer Onboarding-Anleitung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d49a-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="1d49a-193">Auf der Registerkarte **Ressourcen** wählen Sie **Neue Ressource** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="1d49a-194">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1d49a-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="1d49a-195">Um eine Datei hinzufügen, wählen Sie die Registerkarte **Datei**, und ziehen Sie die Datei in den ausgewählten Bereich.</span><span class="sxs-lookup"><span data-stu-id="1d49a-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="1d49a-196">(Alternativ klicken Sie auf eine beliebige Stelle in diesem Bereich, um die Datei auf dem Computer zu suchen, oder wählen Sie **Durchsuchen OneDrive** aus.) Geben Sie einen Namen für die Datei ein, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="1d49a-197">Um eine Verknüpfung hinzuzufügen, wählen Sie die Registerkarte **Verknüpfung** aus, geben Sie einen Namen und die Adresse für die Verknüpfung ein, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="1d49a-198">Um eine Zuordnung hinzuzufügen, wählen Sie die Registerkarte **Zuordnen** aus, geben Sie einen Namen und die Adresse für die Zuordnung ein, und wählen Sie dann **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="1d49a-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="1d49a-199">Onboard eine Zuordnung der Adresse, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="1d49a-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="1d49a-200">Hinzufügen einer Ressource zu einem Onboarding-Leitfaden oder einer Onboarding-Vorlage</span><span class="sxs-lookup"><span data-stu-id="1d49a-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="1d49a-201">Wählen Sie **Speichern** aus, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1d49a-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="1d49a-202">Um eine Ressource zu löschen, wählen Sie die Schaltfläche **Löschen** (Abfalleimersymbol), das rechts neben der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="1d49a-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="1d49a-203">Um einen Kontakt zu bearbeiten, wählen Sie die Schaltfläche **Bearbeiten** (Stiftsymbol), das rechts neben der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="1d49a-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1d49a-204">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1d49a-204">Next steps</span></span>

- [<span data-ttu-id="1d49a-205">Hier können Sie Inhalte mit anderen Personen teilen</span><span class="sxs-lookup"><span data-stu-id="1d49a-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="1d49a-206">Anzeigen des Status von Aufgaben und dem Onboarding von Mitarbeitern</span><span class="sxs-lookup"><span data-stu-id="1d49a-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="1d49a-207">Erstellen von Einstellungsteams in Onboard</span><span class="sxs-lookup"><span data-stu-id="1d49a-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="1d49a-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d49a-208">See also</span></span>

- [<span data-ttu-id="1d49a-209">Testen oder kaufen Sie die Onbaord-App</span><span class="sxs-lookup"><span data-stu-id="1d49a-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="1d49a-210">Was ist neu oder geändert in Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="1d49a-210">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="1d49a-211">Release-Pläne</span><span class="sxs-lookup"><span data-stu-id="1d49a-211">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="1d49a-212">Sie erhalten Unterstützung für Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="1d49a-212">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
