---
title: Hinzufügen einer Datenschutzrichtlinienseite
description: In diesem Thema wird beschrieben, wie Sie eine Datenschutzrichtlinienseite zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a9e09a1d0dbd6c0dc94b5668bb29de6605e2ca9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980206"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="230ad-103">Hinzufügen einer Datenschutzrichtlinienseite</span><span class="sxs-lookup"><span data-stu-id="230ad-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="230ad-104">In diesem Thema wird beschrieben, wie Sie eine Datenschutzrichtlinienseite zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="230ad-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="230ad-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="230ad-105">Overview</span></span>

<span data-ttu-id="230ad-106">Die Einhaltung der Datenschutzbestimmungen umfasst organisatorische Maßnahmen, die die Benutzer der Website darüber informieren, wie ihre Daten erfasst und verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="230ad-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="230ad-107">Benutzer können dann entscheiden, wie sie mit ihren persönlichen Daten umgehen möchten, und entsprechende Maßnahmen ergreifen.</span><span class="sxs-lookup"><span data-stu-id="230ad-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="230ad-108">Microsoft-Datenschutzbestimmungen in Dynamics 365 Commerce prüfen</span><span class="sxs-lookup"><span data-stu-id="230ad-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="230ad-109">Um die Microsoft-Datenschutzbestimmungen zu prüfen, während Sie bei den Dynamics 365 Commerce Authoring-Tools angemeldet sind, wählen Sie die **Hilfe**-Taste (**?**) in der oberen rechten Ecke und wählen Sie dann **Datenschutz und Cookies** aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="230ad-110">Es wird eine neue Registerkarte geöffnet, die einen Link zur [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement) enthält.</span><span class="sxs-lookup"><span data-stu-id="230ad-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="230ad-111">Erstellen Sie eine Datenschutzrichtlinie für Ihre Website</span><span class="sxs-lookup"><span data-stu-id="230ad-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="230ad-112">In Dynamics 365 Commerce gibt es verschiedene Möglichkeiten, Benutzern Ihrer Website Zugriff auf Ihre Datenschutzbestimmungen zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="230ad-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="230ad-113">In diesem Abschnitt wird gezeigt, wie Sie eine Seite mit Datenschutzrichtlinien erstellen und dann mithilfe eines Fußzeilenfragments auf die Seite verweisen.</span><span class="sxs-lookup"><span data-stu-id="230ad-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="230ad-114">Die folgende Anleitung ist ein Beispiel zum Erstellen einer allgemeinen Datenschutzrichtlinie für eine Commerce-Site.</span><span class="sxs-lookup"><span data-stu-id="230ad-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="230ad-115">Sie sind dafür verantwortlich, eine Lösung für Datenschutzrichtlinienseiten zu entwerfen und zu implementieren, die den gesetzlichen Anforderungen Ihres Unternehmens am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="230ad-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="230ad-116">Wechseln Sie zunächst in den Authoring-Tools zu der Site, für die Sie eine Seite mit Datenschutzrichtlinien erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="230ad-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="230ad-117">Eine Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="230ad-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="230ad-118">Wenn bereits eine Vorlage erstellt wurde, die für die Datenschutzrichtlinie verwendet werden kann, fahren Sie mit dem Abschnitt [Erstellen Sie eine Seite mit Datenschutzrichtlinien](#build-a-privacy-policy-page) fort.</span><span class="sxs-lookup"><span data-stu-id="230ad-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="230ad-119">Um eine Vorlage zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="230ad-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="230ad-120">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine Seitenvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="230ad-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="230ad-121">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Werbebanner-Vorlage** ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="230ad-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="230ad-122">Fügen Sie in der Vorlage alle erforderlichen Module zu den erforderlichen Seiten-Slots hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="230ad-123">Bewegen Sie den Mauszeiger zur Orientierung über die roten Ausrufezeichen.</span><span class="sxs-lookup"><span data-stu-id="230ad-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="230ad-124">(Zum Beispiel erfordert der Slot **HTML-Kopf** möglicherweise das Modul **Standardmäßiges externes Skript**.)</span><span class="sxs-lookup"><span data-stu-id="230ad-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="230ad-125">Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="230ad-126">Fügen Sie im Modul **Standardseite** im Slot **Haupt** das Modul **Umfangreiches Inhaltsblockmodul** hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="230ad-127">Fügen Sie im Modul **Umfangreiches Inhaltsblockmodul** das Modul **Umfangreiches Inhaltsblockelement** hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="230ad-128">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="230ad-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="230ad-129">Erstellen einer Datenschutzrichtlinienseite</span><span class="sxs-lookup"><span data-stu-id="230ad-129">Build a privacy policy page</span></span>

<span data-ttu-id="230ad-130">Gehen Sie folgendermaßen vor, um eine Datenschutzrichtlinienseite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="230ad-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="230ad-131">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="230ad-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="230ad-132">Wählen Sie im Dialogfeld **Eine Vorlage auswählen** die Vorlage für die Seite mit den Datenschutzrichtlinien aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="230ad-133">Geben Sie einen Seitennamen und die Seiten-URL ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="230ad-134">Fügen Sie im Slot **Haupt** der Seite das Modul **Umfangreiches Inhaltsblockmodul** hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="230ad-135">Fügen Sie im Modul **Umfangreiches Inhaltsblockmodul** das Modul **Umfangreiches Inhaltsblockelement** hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="230ad-136">Wählen Sie im Eigenschaftenfenster für das Modul **Inhaltsreicher Block** die Option **Datenquelle hinzufügen** und dann **Rich-Text-Inhalt** aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="230ad-137">Geben Sie im Rich-Text-Editor den Inhalt für die Seite mit den Datenschutzrichtlinien ein.</span><span class="sxs-lookup"><span data-stu-id="230ad-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="230ad-138">Erweitern Sie den Rich-Text-Editor nach Bedarf in den Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="230ad-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="230ad-139">Wenn Sie den Inhalt eingegeben haben, wählen Sie **Vorschau** aus, um eine Vorschau der Seite im Webbrowser anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="230ad-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="230ad-140">Vervollständigen Sie alle verbleibenden Ergänzungen der Seiten- und Moduleigenschaften.</span><span class="sxs-lookup"><span data-stu-id="230ad-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="230ad-141">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="230ad-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="230ad-142">Um die URL für die Datenschutzrichtlinienseite zu konfigurieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="230ad-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="230ad-143">Navigieren Sie zu **URLs**, und wählen Sie die URL für die Datenschutzrichtlinienseite aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="230ad-144">Wählen Sie **Veröffentlichen**, um die ausgewählte URL zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="230ad-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="230ad-145">Einen Link zur Datenschutzrichtlinienseite in einer Fußzeile erstellen</span><span class="sxs-lookup"><span data-stu-id="230ad-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="230ad-146">Sie können einem Fragment den Link zu einer Datenschutzrichtlinienseite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="230ad-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="230ad-147">Auf diese Weise können Sie den Link freigeben und über mehrere Websiteseiten hinweg aktualisieren, indem Sie auf das Fragment verweisen.</span><span class="sxs-lookup"><span data-stu-id="230ad-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="230ad-148">In diesem Beispiel wird gezeigt, wie einem Fußzeilenfragment ein Link zur Seite mit den Datenschutzrichtlinien hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="230ad-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="230ad-149">Gehen Sie folgendermaßen vor, um einem Fußzeilenfragment einen Link hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="230ad-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="230ad-150">Wechseln Sie zu **Fragmente** und wählen Sie dann **Neu** aus, um ein Seitenfragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="230ad-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="230ad-151">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Fußzeile** aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-151">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="230ad-152">Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-152">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="230ad-153">Fügen Sie dem Slot **Fußzeilenkategorie** das Modul **Fußzeilenelement** hinzu.</span><span class="sxs-lookup"><span data-stu-id="230ad-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="230ad-154">Wählen Sie im Eigenschaftenbereich rechts **Linktext** aus.</span><span class="sxs-lookup"><span data-stu-id="230ad-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="230ad-155">Geben Sie im Dialogfeld **Linktext** den Linktext und das Linkziel der Datenschutzrichtlinienseite ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="230ad-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="230ad-156">Um die URL der Datenschutzrichtlinie zu erhalten, gehen Sie zu **Seiten**, dann zur Datenschutzrichtlinienseite, und kopieren Sie die URL aus dem Eigenschaftenbereich.</span><span class="sxs-lookup"><span data-stu-id="230ad-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="230ad-157">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="230ad-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="230ad-158">Zeigen Sie eine Vorschau des Fragments an und testen Sie den Link zur Seite mit den Datenschutzrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="230ad-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="230ad-159">Das Fragment kann jetzt in der Vorlage für andere Websiteseiten referenziert werden.</span><span class="sxs-lookup"><span data-stu-id="230ad-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="230ad-160">Wenn auf dieses Fragment im Modul **Fußzeile** einer Vorlage verwiesen wird, erscheint der Linkverweis auf allen Seiten, die mit dieser Vorlage erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="230ad-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="230ad-161">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="230ad-161">Additional resources</span></span>

[<span data-ttu-id="230ad-162">Konformitätsübersicht</span><span class="sxs-lookup"><span data-stu-id="230ad-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="230ad-163">Funktionen und Leistungsspektrum der Eingabehilfe</span><span class="sxs-lookup"><span data-stu-id="230ad-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="230ad-164">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="230ad-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="230ad-165">Benutzer-IDs ersetzen, die nachverfolgten Inhalten zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="230ad-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
