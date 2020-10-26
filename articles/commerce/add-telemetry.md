---
title: Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie
description: In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901495"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="7f316-103">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="7f316-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f316-104">In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7f316-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="7f316-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7f316-105">Overview</span></span>

<span data-ttu-id="7f316-106">Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="7f316-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="7f316-107">Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="7f316-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="7f316-108">Die meisten Internet-Analysepakete erfordern, dass Sie clientseitigen Scriptcode im **\<head\>**-Element der HTML für alle Seiten Ihrer Website hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f316-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="7f316-109">Die Anweisungen in diesem Thema gelten auch für benutzerdefinierte clientseitige andere Funktionen, die Microsoft Dynamics 365 Commerce System intern nicht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7f316-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="7f316-110">Erstellen Sie ein wiederverwendbares Fragment für Ihren Skriptcode</span><span class="sxs-lookup"><span data-stu-id="7f316-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="7f316-111">Mit einem Fragment können Sie Inline- oder externen Skriptcode auf allen Seiten Ihrer Site wiederverwenden, unabhängig von der verwendeten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="7f316-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="7f316-112">Erstellen Sie ein wiederverwendbares Fragment für Ihren Inline-Skriptcode</span><span class="sxs-lookup"><span data-stu-id="7f316-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="7f316-113">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment für Ihren Inline-Skriptcode im Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f316-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7f316-114">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="7f316-115">Wählen Sie im Dialogfeld **Neues Fragment** die Option **Inline-Skript** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="7f316-116">Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7f316-117">Wählen Sie unter dem von Ihnen erstellten Fragment die Option aus **Standard-Inline-Skript** Modul.</span><span class="sxs-lookup"><span data-stu-id="7f316-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="7f316-118">Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein.</span><span class="sxs-lookup"><span data-stu-id="7f316-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="7f316-119">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7f316-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7f316-120">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7f316-121">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="7f316-122">Erstellen Sie ein wiederverwendbares Fragment für Ihren externen Skriptcode</span><span class="sxs-lookup"><span data-stu-id="7f316-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="7f316-123">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment für Ihren externen Skriptcode im Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f316-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7f316-124">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="7f316-125">Wählen Sie im Dialogfeld **Neues Fragment** die Option **Externes Skript** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="7f316-126">Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7f316-127">Wählen Sie unter dem von Ihnen erstellten Fragment die Option aus **Externes Standard-Skript** Modul.</span><span class="sxs-lookup"><span data-stu-id="7f316-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="7f316-128">Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f316-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="7f316-129">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7f316-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7f316-130">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7f316-131">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="7f316-132">Wenn die Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) für Ihre Site aktiviert ist, stellen Sie sicher, dass alle externen URLs zur Inhaltssicherheitsrichtlinie **script-src** im Commerce Site Builder hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7f316-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="7f316-133">Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="7f316-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="7f316-134">Fügen Sie einer Vorlage ein Fragment hinzu, das Skriptcode enthält</span><span class="sxs-lookup"><span data-stu-id="7f316-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="7f316-135">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Fragment mit Skriptcode einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f316-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7f316-136">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f316-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7f316-137">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f316-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7f316-138">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Fragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7f316-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="7f316-139">Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="7f316-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="7f316-140">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7f316-141">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="7f316-142">Fügen Sie einer Vorlage ein externes Skript oder ein Inline-Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="7f316-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="7f316-143">Wenn Sie ein Inline- oder externes Skript direkt in eine Reihe von Seiten einfügen möchten, die von einer einzelnen Vorlage gesteuert werden, müssen Sie nicht zuerst ein Fragment erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f316-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="7f316-144">Fügen Sie einer Vorlage ein Inline-Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="7f316-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="7f316-145">Führen Sie die folgenden Schritte aus, um ein Inline-Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f316-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7f316-146">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f316-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7f316-147">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f316-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7f316-148">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7f316-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7f316-149">In dem **Modul hinzufügen** Dialogfeld wählen Sie **Inline-Skript**.</span><span class="sxs-lookup"><span data-stu-id="7f316-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="7f316-150">Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein.</span><span class="sxs-lookup"><span data-stu-id="7f316-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="7f316-151">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7f316-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7f316-152">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7f316-153">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="7f316-154">Fügen Sie einer Vorlage ein externes Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="7f316-154">Add an external script directly to a template</span></span>

<span data-ttu-id="7f316-155">Führen Sie die folgenden Schritte aus, um ein externes Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f316-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7f316-156">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f316-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7f316-157">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f316-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7f316-158">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7f316-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7f316-159">In dem **Modul hinzufügen** Dialogfeld wählen Sie **Externes Skript**.</span><span class="sxs-lookup"><span data-stu-id="7f316-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="7f316-160">Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f316-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="7f316-161">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="7f316-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7f316-162">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7f316-163">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="7f316-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f316-164">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f316-164">Additional resources</span></span>

[<span data-ttu-id="7f316-165">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="7f316-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="7f316-166">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="7f316-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="7f316-167">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="7f316-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="7f316-168">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="7f316-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7f316-169">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="7f316-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7f316-170">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="7f316-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="7f316-171">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="7f316-171">Add languages to your site</span></span>](add-languages-to-site.md)
