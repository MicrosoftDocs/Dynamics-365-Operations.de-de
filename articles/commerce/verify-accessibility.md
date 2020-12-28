---
title: Überprüfen der Zugänglichkeit des Seiteninhalts
description: In diesem Thema wird beschrieben, wie Sie die Barrierefreiheit von Seiteninhalten in Microsoft Dynamics 365 Commerce überprüfen.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fc3dca673510e1636f497bb7d5c295bebe025677
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4412691"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="304e3-103">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="304e3-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="304e3-104">In diesem Thema wird beschrieben, wie Sie die Barrierefreiheit von Seiteninhalten in Microsoft Dynamics 365 Commerce überprüfen.</span><span class="sxs-lookup"><span data-stu-id="304e3-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="304e3-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="304e3-105">Overview</span></span>

<span data-ttu-id="304e3-106">Wenn Sie mit dem Ändern einer Seite fertig sind, sollten Sie sicherstellen, dass der Inhalt für alle im Web zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="304e3-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="304e3-107">In den Commerce-Authoring-Tools können Sie mithilfe des integrierten Dienstes [Microsoft Accessibility Insights](https://accessibilityinsights.io/) auf einfache Weise die Zugänglichkeit von Seiteninhalten überprüfen.</span><span class="sxs-lookup"><span data-stu-id="304e3-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="304e3-108">Dieser Dienst überprüft Ihren Seiteninhalt anhand der neuesten Richtlinien zur [World Wide Web Consortium (W3C Zugänglichkeit)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="304e3-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="304e3-109">Die [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Integration muss auf Mandanten- oder Site-Ebene aktiviert sein, bevor Sie sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="304e3-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="304e3-110">Aktivieren Sie Microsoft Accessibility Insights für alle Websites in Ihrem Mandanten</span><span class="sxs-lookup"><span data-stu-id="304e3-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="304e3-111">Um [Microsoft Accessibility Insights](https://accessibilityinsights.io/) zu aktivieren, führen Sie die folgenden Schritte aus, um alle Commerce-Sites in Ihrem Mandanten zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="304e3-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="304e3-112">Um auf Mandanteneinstellungen zuzugreifen, müssen Sie als Systemadministrator bei Commerce angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="304e3-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="304e3-113">Melden Sie sich bei Commerce als Systemadministrator an.</span><span class="sxs-lookup"><span data-stu-id="304e3-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="304e3-114">Wählen Sie im linken Navigationsbereich **Mandanteneinstellungen** (neben dem Zahnradsymbol) aus, um es zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="304e3-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="304e3-115">Wählen Sie unter **Mandanteneinstellungen** die Option **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="304e3-116">Legen Sie die Option **Zugänglichkeitsprüfung** auf **Ein** fest.</span><span class="sxs-lookup"><span data-stu-id="304e3-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="304e3-117">Aktivieren Sie Microsoft Accessibility Insights für eine einzelne Site</span><span class="sxs-lookup"><span data-stu-id="304e3-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="304e3-118">Um die [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Integration für eine einzelne Commerce-Site zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="304e3-119">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="304e3-120">Wählen Sie im linken Navigationsbereich **Site-Einstellungen** aus, um den Bereich zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="304e3-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="304e3-121">Wählen Sie unter **Site-Einstellungen** die Option **Funktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="304e3-122">Legen Sie die Option **Zugänglichkeitsprüfung** auf **Ein** fest.</span><span class="sxs-lookup"><span data-stu-id="304e3-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="304e3-123">Überprüfen Sie die Zugänglichkeit des Inhalts auf der Homepage</span><span class="sxs-lookup"><span data-stu-id="304e3-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="304e3-124">Um den integrierten [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-Dienst zu verwenden und so den Inhalt Ihrer Startseite in Commerce zu scannen und zu prüfen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="304e3-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="304e3-125">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="304e3-126">Wählen Sie im linken Navigationsbereich die Option **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="304e3-127">Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="304e3-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="304e3-128">Wählen Sie in der Befehlsleiste die Option **Zugänglichkeit prüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="304e3-129">Die Seite **Zugänglichkeit prüfen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="304e3-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="304e3-130">Überprüfen Sie nach Abschluss des Scans den Inhalt des Berichts.</span><span class="sxs-lookup"><span data-stu-id="304e3-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="304e3-131">Wenn Prüfungen fehlgeschlagen sind, wählen Sie jedes fehlgeschlagene Prüfelement aus, um es zu erweitern und weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="304e3-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="304e3-132">Um den Bericht zu schließen, nachdem Sie ihn geprüft haben, scrollen Sie zur Seite **Zugänglichkeit prüfen**, und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="304e3-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="304e3-133">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="304e3-133">Additional resources</span></span>

[<span data-ttu-id="304e3-134">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="304e3-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="304e3-135">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="304e3-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="304e3-136">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="304e3-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="304e3-137">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="304e3-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="304e3-138">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="304e3-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="304e3-139">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="304e3-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="304e3-140">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="304e3-140">Enrich a category landing page</span></span>](enrich-category-page.md)
