---
title: Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie
description: In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797430"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="ad799-103">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="ad799-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad799-104">In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ad799-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="ad799-105">Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="ad799-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="ad799-106">Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="ad799-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="ad799-107">Die meisten Internet-Analysepakete erfordern, dass Sie clientseitigen Scriptcode im **\<head\>**-Element der HTML für alle Seiten Ihrer Website hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad799-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="ad799-108">Die Anweisungen in diesem Thema gelten auch für andere benutzerdefinierte clientseitige Funktionen, die Microsoft Dynamics 365 Commerce intern nicht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ad799-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="ad799-109">Erstellen Sie ein wiederverwendbares Fragment für Ihren Skriptcode</span><span class="sxs-lookup"><span data-stu-id="ad799-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="ad799-110">Mit einem Fragment können Sie Inline- oder externen Skriptcode auf allen Seiten Ihrer Site wiederverwenden, unabhängig von der verwendeten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="ad799-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="ad799-111">Erstellen Sie ein wiederverwendbares Fragment für Ihren Inline-Skriptcode</span><span class="sxs-lookup"><span data-stu-id="ad799-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="ad799-112">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment für Ihren Inline-Skriptcode im Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad799-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad799-113">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="ad799-114">Wählen Sie im Dialogfeld **Neues Fragment** die Option **Inline-Skript** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="ad799-115">Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ad799-116">Wählen Sie unter dem von Ihnen erstellten Fragment die Option aus **Standard-Inline-Skript** Modul.</span><span class="sxs-lookup"><span data-stu-id="ad799-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="ad799-117">Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein.</span><span class="sxs-lookup"><span data-stu-id="ad799-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="ad799-118">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ad799-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="ad799-119">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ad799-120">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="ad799-121">Erstellen Sie ein wiederverwendbares Fragment für Ihren externen Skriptcode</span><span class="sxs-lookup"><span data-stu-id="ad799-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="ad799-122">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment für Ihren externen Skriptcode im Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad799-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad799-123">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="ad799-124">Wählen Sie im Dialogfeld **Neues Fragment** die Option **Externes Skript** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="ad799-125">Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ad799-126">Wählen Sie unter dem von Ihnen erstellten Fragment die Option aus **Externes Standard-Skript** Modul.</span><span class="sxs-lookup"><span data-stu-id="ad799-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="ad799-127">Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad799-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="ad799-128">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ad799-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="ad799-129">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ad799-130">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="ad799-131">Wenn die Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) für Ihre Site aktiviert ist, stellen Sie sicher, dass alle externen URLs zur Inhaltssicherheitsrichtlinie **script-src** im Commerce Site Builder hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ad799-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="ad799-132">Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="ad799-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="ad799-133">Fügen Sie einer Vorlage ein Fragment hinzu, das Skriptcode enthält</span><span class="sxs-lookup"><span data-stu-id="ad799-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="ad799-134">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment mit Skriptcode einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad799-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad799-135">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad799-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="ad799-136">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad799-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="ad799-137">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Fragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ad799-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="ad799-138">Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ad799-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="ad799-139">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ad799-140">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="ad799-141">Fügen Sie einer Vorlage ein externes Skript oder ein Inline-Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="ad799-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="ad799-142">Wenn Sie ein Inline- oder externes Skript direkt in eine Reihe von Seiten einfügen möchten, die von einer einzelnen Vorlage gesteuert werden, müssen Sie nicht zuerst ein Fragment erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad799-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="ad799-143">Fügen Sie einer Vorlage ein Inline-Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="ad799-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="ad799-144">Führen Sie die folgenden Schritte aus, um ein Inline-Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad799-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad799-145">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad799-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="ad799-146">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad799-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="ad799-147">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ad799-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ad799-148">In dem **Modul hinzufügen** Dialogfeld wählen Sie **Inline-Skript**.</span><span class="sxs-lookup"><span data-stu-id="ad799-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="ad799-149">Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein.</span><span class="sxs-lookup"><span data-stu-id="ad799-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="ad799-150">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ad799-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="ad799-151">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ad799-152">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="ad799-153">Fügen Sie einer Vorlage ein externes Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="ad799-153">Add an external script directly to a template</span></span>

<span data-ttu-id="ad799-154">Führen Sie die folgenden Schritte aus, um ein externes Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad799-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad799-155">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad799-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="ad799-156">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad799-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="ad799-157">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ad799-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ad799-158">In dem **Modul hinzufügen** Dialogfeld wählen Sie **Externes Skript**.</span><span class="sxs-lookup"><span data-stu-id="ad799-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="ad799-159">Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad799-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="ad799-160">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ad799-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="ad799-161">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ad799-162">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ad799-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad799-163">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad799-163">Additional resources</span></span>

[<span data-ttu-id="ad799-164">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="ad799-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ad799-165">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="ad799-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ad799-166">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="ad799-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="ad799-167">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="ad799-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ad799-168">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="ad799-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="ad799-169">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="ad799-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="ad799-170">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="ad799-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
