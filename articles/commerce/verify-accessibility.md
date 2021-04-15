---
title: Überprüfen der Zugänglichkeit des Seiteninhalts
description: In diesem Thema wird beschrieben, wie Sie die Barrierefreiheit von Seiteninhalten in Microsoft Dynamics 365 Commerce überprüfen.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791630"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="5dda9-103">Barrierefreiheit von Seiteninhalten prüfen</span><span class="sxs-lookup"><span data-stu-id="5dda9-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5dda9-104">In diesem Thema wird beschrieben, wie Sie die Barrierefreiheit von Seiteninhalten in Microsoft Dynamics 365 Commerce überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5dda9-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5dda9-105">Wenn Sie mit dem Ändern einer Seite fertig sind, sollten Sie sicherstellen, dass der Inhalt für alle im Web zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="5dda9-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="5dda9-106">In den Commerce-Authoring-Tools können Sie mithilfe des integrierten Dienstes [Microsoft Accessibility Insights](https://accessibilityinsights.io/) auf einfache Weise die Zugänglichkeit von Seiteninhalten überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5dda9-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="5dda9-107">Dieser Dienst überprüft Ihren Seiteninhalt anhand der neuesten Richtlinien zur [World Wide Web Consortium (W3C Zugänglichkeit)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="5dda9-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="5dda9-108">Die [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Integration muss auf Mandanten- oder Site-Ebene aktiviert sein, bevor Sie sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5dda9-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="5dda9-109">Aktivieren Sie Microsoft Accessibility Insights für alle Websites in Ihrem Mandanten</span><span class="sxs-lookup"><span data-stu-id="5dda9-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="5dda9-110">Um [Microsoft Accessibility Insights](https://accessibilityinsights.io/) zu aktivieren, führen Sie die folgenden Schritte aus, um alle Commerce-Sites in Ihrem Mandanten zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="5dda9-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="5dda9-111">Um auf Mandanteneinstellungen zuzugreifen, müssen Sie als Systemadministrator bei Commerce angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="5dda9-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="5dda9-112">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="5dda9-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="5dda9-113">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="5dda9-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="5dda9-114">Wählen Sie unter **Mandanteneinstellungen** die Option **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="5dda9-115">Legen Sie die Option **Zugänglichkeitsprüfung** auf **Ein** fest.</span><span class="sxs-lookup"><span data-stu-id="5dda9-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="5dda9-116">Aktivieren Sie Microsoft Accessibility Insights für eine einzelne Site</span><span class="sxs-lookup"><span data-stu-id="5dda9-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="5dda9-117">Um die [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Integration für eine einzelne Commerce-Site zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="5dda9-118">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="5dda9-119">Wählen Sie im linken Navigationsbereich **Site-Einstellungen** aus, um den Bereich zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="5dda9-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="5dda9-120">Wählen Sie unter **Site-Einstellungen** die Option **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="5dda9-121">Legen Sie die Option **Zugänglichkeitsprüfung** auf **Ein** fest.</span><span class="sxs-lookup"><span data-stu-id="5dda9-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="5dda9-122">Überprüfen Sie die Zugänglichkeit des Inhalts auf der Homepage</span><span class="sxs-lookup"><span data-stu-id="5dda9-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="5dda9-123">Um den integrierten [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Dienst zu verwenden und so den Inhalt Ihrer Startseite in Commerce zu scannen und zu prüfen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="5dda9-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5dda9-124">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="5dda9-125">Wählen Sie im linken Navigationsbereich die Option **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="5dda9-126">Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5dda9-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="5dda9-127">Wählen Sie in der Befehlsleiste die Option **Zugänglichkeit prüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="5dda9-128">Die Seite **Zugänglichkeit prüfen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5dda9-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="5dda9-129">Überprüfen Sie nach Abschluss des Scans den Inhalt des Berichts.</span><span class="sxs-lookup"><span data-stu-id="5dda9-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="5dda9-130">Wenn Prüfungen fehlgeschlagen sind, wählen Sie jedes fehlgeschlagene Prüfelement aus, um es zu erweitern und weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5dda9-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="5dda9-131">Um den Bericht zu schließen, nachdem Sie ihn geprüft haben, scrollen Sie zur Seite **Zugänglichkeit prüfen**, und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5dda9-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dda9-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5dda9-132">Additional resources</span></span>

[<span data-ttu-id="5dda9-133">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="5dda9-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="5dda9-134">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5dda9-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5dda9-135">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="5dda9-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="5dda9-136">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="5dda9-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="5dda9-137">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="5dda9-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="5dda9-138">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="5dda9-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="5dda9-139">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="5dda9-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="5dda9-140">Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen</span><span class="sxs-lookup"><span data-stu-id="5dda9-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
