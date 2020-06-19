---
title: Arbeiten mit CSS-Überschreibungsdateien
description: In diesem Thema wird beschrieben, warum, wann und wie Cascading Style Sheets-Überschreibungsdateien (CSS) Dateien in Microsoft Dynamics 365 Commerce verwendet werden.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411246"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="13291-103">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="13291-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="13291-104">In diesem Thema wird beschrieben, warum, wann und wie Cascading Style Sheets-Überschreibungsdateien (CSS) Dateien in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13291-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="13291-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="13291-105">Overview</span></span>

<span data-ttu-id="13291-106">Permanente Site-Stile sollten normalerweise über das Thema einer Site verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="13291-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="13291-107">Designs bilden die grundlegenden CSS- und Stileinstellungen für die Module auf einer beliebigen Seite Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="13291-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="13291-108">Designs werden mit dem Dynamics 365 Commerce Online Software Development Kit (SDK) erstellt, und sie werden mit Microsoft Dynamics Lifecycle Services (LCS) auf Ihren Websites bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="13291-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="13291-109">Design-Debugging-Funktionen und Modulschnittstellenkonfigurationen im SDK helfen Site-Entwicklern, anpassbare und zusammenhängende Site-Design-Pakete zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13291-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="13291-110">Wenn diese Entwurfspakete auf einer Website bereitgestellt werden, können sich die Website-Autoren auf das Erstellen, Bearbeiten und Veröffentlichen von Inhalten konzentrieren, anstatt die Website zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="13291-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="13291-111">Angesichts des üblichen Lebenszyklus eines Themas kann die Abhängigkeit von Entwicklern, Stiländerungen über die SDK- und LCS-Bereitstellungspipeline vorzunehmen, in einigen Szenarien untragbar sein.</span><span class="sxs-lookup"><span data-stu-id="13291-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="13291-112">Site-Prototypen oder Hotfixes können mühsam erscheinen, wenn das SDK nicht konfiguriert ist oder Sie keine Zeit haben, auf eine LCS-Bereitstellung zu warten.</span><span class="sxs-lookup"><span data-stu-id="13291-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="13291-113">In diesen Szenarien können CSS-Überschreibungsdateien hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="13291-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="13291-114">In den Commerce-Authoring-Tools können authentifizierte Benutzer eine CSS-Datei hochladen, sie in einer Vorschau anzeigen, und sie anschließend aktivieren, um das Design einer Site zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="13291-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="13291-115">Der Overhead der SDK- oder LCS-Bereitstellung ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="13291-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="13291-116">Die in einer CSS-Überschreibungsdatei angegebenen Überschreibungen können so klein wie eine Änderung an einem einzelnen Textstil oder so umfangreich wie eine vollständige Markenüberholung sein.</span><span class="sxs-lookup"><span data-stu-id="13291-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="13291-117">Bevor Sie es CSS-Überschreibungsdateien verwenden, beachten Sie beim Überschreiben von Dateien die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="13291-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="13291-118">Nur eine CSS-Überschreibungsdatei kann gleichzeitig auf einer Site aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="13291-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="13291-119">Daher müssen alle aktiven Außerkraftsetzungen in einer einzigen Außerkraftsetzungsdatei vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="13291-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="13291-120">Obwohl Sie eine Vorschau der Überschreibungen in den Commerce-Authoring-Tools anzeigen können, gibt es keine dedizierten Debugging-Funktionen, mit denen Sie die durch die Überschreibungen verursachten Fehler identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="13291-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="13291-121">Mit anderen Worten, verfügen Sie bei Verwendung von CSS-Überschreibungsdateien nicht über dasselbe Toolset, das das SDK für die Modul- und Autorenvalidierung bietet.</span><span class="sxs-lookup"><span data-stu-id="13291-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="13291-122">Dennoch bieten CSS-Überschreibungsdateien eine schnelle Möglichkeit, ein Design zu prototypisieren oder einen Hotfix zu implementieren, bevor ein vollständiges Design-Update entwickelt und bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="13291-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="13291-123">Erstellen einer CSS-Überschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="13291-123">Create a CSS override file</span></span>

<span data-ttu-id="13291-124">Beim Erstellen einer CSS-Überschreibungsdatei können Sie eine beliebige integrierte Entwicklungsumgebung (IDE), einen Texteditor oder einen Quellcode-Editor verwenden.</span><span class="sxs-lookup"><span data-stu-id="13291-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="13291-125">Ein typischer Ansatz besteht darin, Standard-Web-Debugger in Ihrem Browser zu verwenden, um Stilselektoren, Eigenschaften und Werte auf Ihrer vorhandenen Site zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="13291-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="13291-126">In den meisten Browsern können Sie Werte ändern und im Debugger eine Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="13291-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="13291-127">Nachdem Sie die gewünschten Änderungen identifiziert haben, können Sie sie in Ihrer eigenen CSS-Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="13291-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="13291-128">Eine CSS-Überschreibungsdatei hochladen</span><span class="sxs-lookup"><span data-stu-id="13291-128">Upload a CSS override file</span></span>

<span data-ttu-id="13291-129">Gehen Sie folgendermaßen vor, um eine CSS-Datei zu Ihrer Site in Commerce hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="13291-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="13291-130">Gehen Sie in den Erstellungstools zu Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="13291-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="13291-131">Wählen Sie im linken Navigationsbereich **Design** aus.</span><span class="sxs-lookup"><span data-stu-id="13291-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13291-132">Abhängig von der Version der verwendeten Commerce-Authoring-Tools müssen Sie möglicherweise **Einstellungen** im Navigationsbereich erweitern, bevor Sie **Design** auswählen können.</span><span class="sxs-lookup"><span data-stu-id="13291-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="13291-133">Wählen Sie oben im Hauptdesignfenster die Registerkarte **CSS überschreiben** aus, soweit noch nicht geschehen.</span><span class="sxs-lookup"><span data-stu-id="13291-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="13291-134">Wählen Sie unter **Verfügbare CSS-Überschreibungen** die Option **CSS-Datei hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="13291-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="13291-135">Ein Dateiexplorerfenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13291-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="13291-136">Suchen Sie im Dateiexplorer eine CSS-Datei und wählen Sie sie aus. Klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="13291-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="13291-137">Die hochgeladene CSS-Datei erscheint jetzt unter **Verfügbare CSS-Überschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="13291-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="13291-138">Vorschau einer CSS-Überschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="13291-138">Preview a CSS override file</span></span>

<span data-ttu-id="13291-139">Um eine Vorschau einer CSS-Überschreibungsdatei anzuzeigen, bevor Sie diese aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="13291-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="13291-140">Wählen Sie im Navigationsbereich links **Design** aus, und suchen Sie dann auf der Registerkarte **CSS überschreiben** unter **Verfügbare CSS-Überschreibungen** die CSS-Datei, die Sie in der Vorschau anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="13291-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="13291-141">Wählen Sie neben dem CSS-Dateinamen die Option **Vorschau der Site**.</span><span class="sxs-lookup"><span data-stu-id="13291-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="13291-142">Wählen Sie im Dialogfeld **URL auswählen** die URL der Site, auf die die Überschreibung angewendet werden soll, und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="13291-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="13291-143">Wenn es verschiedene Varianten für die ausgewählte URL gibt, wählen Sie die gewünschte Variante im Dialogfeld **Vorschau der Variationen** aus, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="13291-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="13291-144">Ein neuer Browser-Tab oder ein neues Browser-Fenster wird geöffnet, in dem Sie Ihre Stilüberschreibungen für Ihre Site validieren können.</span><span class="sxs-lookup"><span data-stu-id="13291-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="13291-145">Anschließend können Sie die URL für andere authentifizierte Commerce-Benutzer zur Überprüfung und für Feedback freigeben.</span><span class="sxs-lookup"><span data-stu-id="13291-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="13291-146">Aktivieren einer CSS-Überschreibungsdatei auf Ihrer Live-Site</span><span class="sxs-lookup"><span data-stu-id="13291-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="13291-147">Nachdem Sie die CSS-Überschreibungsdatei als Vorschau angezeigt und genehmigt haben, können Sie sie auf Ihrer Live-Site aktivieren.</span><span class="sxs-lookup"><span data-stu-id="13291-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="13291-148">Nur eine CSS-Überschreibungsdatei kann gleichzeitig auf Ihrer Site aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="13291-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="13291-149">Wenn Sie eine neue Überschreibungsdatei aktivieren, wird die vorherige Überschreibungsdatei deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="13291-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="13291-150">Stellen Sie daher sicher, dass alle erforderlichen Überschreibungen in einer einzigen CSS-Überschreibungsdatei vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="13291-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="13291-151">Um eine CSS-Überschreibungsdatei zu aktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="13291-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="13291-152">Wählen Sie im Navigationsbereich links **Design** aus, und suchen Sie dann auf der Registerkarte **CSS überschreiben** unter **Verfügbare CSS-Überschreibungen** die CSS-Datei, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="13291-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="13291-153">Wählen Sie unter dem CSS-Dateinamen die Option **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="13291-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="13291-154">Die Überschreibungsdatei wird sofort auf Ihrer Live-Site aktiv.</span><span class="sxs-lookup"><span data-stu-id="13291-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="13291-155">Deaktivieren einer CSS-Überschreibungsdatei auf Ihrer Live-Site</span><span class="sxs-lookup"><span data-stu-id="13291-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="13291-156">Um eine CSS-Überschreibungsdatei auf Ihrer Site zu deaktivieren, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="13291-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="13291-157">Wählen Sie im Navigationsbereich links **Design** aus, und suchen Sie dann auf der Registerkarte **CSS überschreiben** unter **Verfügbare CSS-Überschreibungen** die CSS-Datei, die Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="13291-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="13291-158">Wählen Sie unter dem CSS-Dateinamen die Option **Deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="13291-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="13291-159">Die Überschreibungsdatei wird sofort auf Ihrer Live-Site inaktiv.</span><span class="sxs-lookup"><span data-stu-id="13291-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="13291-160">Wählen Sie zum Zugriff auf weitere Optionen für CSS-Überschreibungsdateien die Auslassungspunkte (**...**) neben dem CSS-Dateinamen aus.</span><span class="sxs-lookup"><span data-stu-id="13291-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="13291-161">Die Optionen **Herunterladen**, **Umbenennen** und **Ersetzen** sind nützlich für schnelle Änderungen an vorhandenen CSS-Überschreibungsdateien.</span><span class="sxs-lookup"><span data-stu-id="13291-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13291-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="13291-162">Additional resources</span></span>

[<span data-ttu-id="13291-163">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="13291-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="13291-164">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="13291-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="13291-165">Arbeiten Sie mit Stilvoreinstellungen</span><span class="sxs-lookup"><span data-stu-id="13291-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="13291-166">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="13291-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="13291-167">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="13291-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="13291-168">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="13291-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="13291-169">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="13291-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="13291-170">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="13291-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
