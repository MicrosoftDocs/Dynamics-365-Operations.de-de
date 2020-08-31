---
title: Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie
description: In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686813"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="fb410-103">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="fb410-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb410-104">In diesem Thema wird beschrieben, wie ein clientseitiger Skriptcode den Standortsseiten hinzugefügt wird, um die Sammlung der clientseitigen Telemetrie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fb410-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="fb410-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="fb410-105">Overview</span></span>

<span data-ttu-id="fb410-106">Internet-Analyse ist ein wichtiges Tool, wenn Sie verstehen möchten, wie Ihre Debitoren mit der Site interagieren und Entscheidungen treffen, die Ihnen helfen, die Erfahrung für maximale Umrechnung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="fb410-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="fb410-107">Viele Internet-Analysepakete sind verfügbar, um zu helfen, diese Ziele zu erreichen wie Google Analytics, Clicky, Moz-Analyse und KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="fb410-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="fb410-108">Die meisten Internet-Analysepakete erfordern, dass Sie clientseitigen Scriptcode im **\<head\>**-Element der HTML für alle Seiten Ihrer Website hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fb410-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="fb410-109">Die Anweisungen in diesem Thema gelten auch für benutzerdefinierte clientseitige andere Funktionen, die Microsoft Dynamics 365 Commerce System intern nicht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fb410-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="fb410-110">Erstellen Sie ein wiederverwendbares Seitenfragment für Ihren Skriptcode</span><span class="sxs-lookup"><span data-stu-id="fb410-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="fb410-111">Mit einem Seitenfragment können Sie Inline- oder externen Skriptcode auf allen Seiten Ihrer Site wiederverwenden, unabhängig von der verwendeten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="fb410-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="fb410-112">Erstellen Sie ein wiederverwendbares Seitenfragment für Ihren Inline-Skriptcode</span><span class="sxs-lookup"><span data-stu-id="fb410-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="fb410-113">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Seitenfragment für Ihren Inline-Skriptcode im Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb410-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fb410-114">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="fb410-115">Wählen Sie im Dialogfeld **Neues Seitenfragment** die Option **Inline-Skript** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="fb410-116">Geben Sie unter **Name des Seitenfragments** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="fb410-117">Wählen Sie unter dem von Ihnen erstellten Seitenfragment die Option aus **Standard-Inline-Skript** Modul.</span><span class="sxs-lookup"><span data-stu-id="fb410-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="fb410-118">Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein.</span><span class="sxs-lookup"><span data-stu-id="fb410-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="fb410-119">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="fb410-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fb410-120">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fb410-121">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="fb410-122">Erstellen Sie ein wiederverwendbares Seitenfragment für Ihren externen Skriptcode</span><span class="sxs-lookup"><span data-stu-id="fb410-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="fb410-123">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Seitenfragment für Ihren externen Skriptcode im Site Builder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb410-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fb410-124">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="fb410-125">Wählen Sie im Dialogfeld **Neues Seitenfragment** die Option **Externes Skript** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="fb410-126">Geben Sie unter **Name des Seitenfragments** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="fb410-127">Wählen Sie unter dem von Ihnen erstellten Seitenfragment die Option aus **Externes Standard-Skript** Modul.</span><span class="sxs-lookup"><span data-stu-id="fb410-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="fb410-128">Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb410-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="fb410-129">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="fb410-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fb410-130">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fb410-131">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="fb410-132">Fügen Sie einer Vorlage ein Seitenfragment hinzu, das Skriptcode enthält</span><span class="sxs-lookup"><span data-stu-id="fb410-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="fb410-133">Führen Sie die folgenden Schritte aus, um ein wiederverwendbares Seitenfragment mit Skriptcode einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fb410-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fb410-134">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fb410-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="fb410-135">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb410-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="fb410-136">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Seitenfragment hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fb410-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="fb410-137">Wählen Sie das Fragment aus, das Sie für den Skriptcode erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fb410-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="fb410-138">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fb410-139">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="fb410-140">Fügen Sie einer Vorlage ein externes Skript oder ein Inline-Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="fb410-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="fb410-141">Wenn Sie ein Inline- oder externes Skript direkt in eine Reihe von Seiten einfügen möchten, die von einer einzelnen Vorlage gesteuert werden, müssen Sie nicht zuerst ein Seitenfragment erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb410-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="fb410-142">Fügen Sie einer Vorlage ein Inline-Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="fb410-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="fb410-143">Führen Sie die folgenden Schritte aus, um ein Inline-Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fb410-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fb410-144">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fb410-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="fb410-145">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb410-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="fb410-146">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fb410-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fb410-147">In dem **Modul hinzufügen** Dialogfeld wählen Sie **Inline-Skript**.</span><span class="sxs-lookup"><span data-stu-id="fb410-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="fb410-148">Im Eigenschaftenfenster rechts unter **Inline-Skript** geben Sie Ihr clientseitiges Skript ein.</span><span class="sxs-lookup"><span data-stu-id="fb410-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="fb410-149">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="fb410-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fb410-150">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fb410-151">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="fb410-152">Fügen Sie einer Vorlage ein externes Skript direkt hinzu</span><span class="sxs-lookup"><span data-stu-id="fb410-152">Add an external script directly to a template</span></span>

<span data-ttu-id="fb410-153">Führen Sie die folgenden Schritte aus, um ein externes Skript direkt zu einer Vorlage im Site Builder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fb410-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fb410-154">Gehen Sie zu **Vorlagen** und öffnen Sie die Vorlage für die Seiten, dies Sie dem Skriptcode hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fb410-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="fb410-155">Erweitern Sie im linken Fensterbereich die Vorlagenhierarchie, um den **HTML-Kopf** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fb410-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="fb410-156">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **HTML Kopf** Slot und wählen Sie **Modul  hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fb410-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fb410-157">In dem **Modul hinzufügen** Dialogfeld wählen Sie **Externes Skript**.</span><span class="sxs-lookup"><span data-stu-id="fb410-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="fb410-158">Im Eigenschaftenfenster rechts unter **Skriptquelle** fügen Sie eine externe oder relative URL für die externe Skriptquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb410-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="fb410-159">Konfigurieren Sie dann andere Optionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="fb410-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fb410-160">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fb410-161">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="fb410-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb410-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fb410-162">Additional resources</span></span>

[<span data-ttu-id="fb410-163">Hinzufügen eines Logos</span><span class="sxs-lookup"><span data-stu-id="fb410-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="fb410-164">Auswählen eines Sitedesigns</span><span class="sxs-lookup"><span data-stu-id="fb410-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="fb410-165">Arbeiten mit CSS-Überschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="fb410-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fb410-166">Hinzufügen eines Favicons</span><span class="sxs-lookup"><span data-stu-id="fb410-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="fb410-167">Hinzufügen einer Begrüßungsnachricht</span><span class="sxs-lookup"><span data-stu-id="fb410-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="fb410-168">Hinzufügen eines Urheberrechtshinweises</span><span class="sxs-lookup"><span data-stu-id="fb410-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fb410-169">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="fb410-169">Add languages to your site</span></span>](add-languages-to-site.md)
