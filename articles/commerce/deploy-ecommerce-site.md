---
title: Neuen E-Commerce-Mandanten bereitstellen
description: In diesem Thema wird beschrieben, wie Sie eine neue Dynamics 365 Commerce-E-Commerce-Website bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b750ee89a85688dcebe673f9c3ff13693e9fcad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976737"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="8257d-103">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="8257d-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8257d-104">In diesem Thema wird beschrieben, wie Sie eine neue Dynamics 365 Commerce-E-Commerce-Website bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="8257d-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="8257d-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="8257d-105">Overview</span></span>

<span data-ttu-id="8257d-106">Microsoft Dynamics Lifecycle Services (LCS) ist ein Cloud-basierter kooperativer Arbeitsbereich, den Partnern und Kunden verwenden können, um die Projekte und Umgebung zu verwalten, die neuesten Informationen anzuzeigen über die Microsoft Dynamics Produkte und Funktionen und Stützvorfälle zu erstellen, nachzuverfolgen und zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="8257d-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="8257d-107">E-Commerce-Verwaltungsfunktionen sind in LCS integriert.</span><span class="sxs-lookup"><span data-stu-id="8257d-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="8257d-108">Weitere Informationen zu LCS finden Sie unter [Lifecycle Services Benutzerhandbuch](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="8257d-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="8257d-109">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="8257d-109">Get started</span></span>

<span data-ttu-id="8257d-110">Bevor Sie E-Commerce initialisieren können, müssen Sie ein Projekt, eine Umgebung und eine Retail Cloud Scale Unit (RCSU) initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8257d-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="8257d-111">Um die Initialisierung in LCS zu bewerkstelligen, müssen Sie über Berechtigungen entweder als Projekt-Inhaber oder Umgebungsmanager haben.</span><span class="sxs-lookup"><span data-stu-id="8257d-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="8257d-112">Die Produktion und Sandboxumgebungstopologien werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8257d-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="8257d-113">Weitere Informationen über Umgebungen finden Sie unter [Umgebungsplanung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="8257d-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="8257d-114">Weitere Informationen zur RCSU-Compliance finden Sie unter [Retail Cloud Scale Unit initialisieren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="8257d-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="8257d-115">E-Commerce initialisieren</span><span class="sxs-lookup"><span data-stu-id="8257d-115">Initialize e-commerce</span></span>

<span data-ttu-id="8257d-116">Verwenden Sie diese Prozedur, um die E-Commerce-Funktion in einer vorhandenen Umgebung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8257d-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="8257d-117">Bevor Sie beginnen, stellen Sie sicher, dass Sie folgende Informationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="8257d-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="8257d-118">Die RCSU,die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8257d-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="8257d-119">Die Microsoft Azure Active Directory-Sicherheitsgruppe, die für E-Commerce-Systemadministratoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8257d-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="8257d-120">Die Microsoft Azure Active Directory Sicherheitsgruppe, die für Bewertungen verwendet wird und Moderatoren überprüft.</span><span class="sxs-lookup"><span data-stu-id="8257d-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="8257d-121">Die Domänen, die der Umgebung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8257d-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="8257d-122">Zudem können Sie folgende optionale Informationen erfassen:</span><span class="sxs-lookup"><span data-stu-id="8257d-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="8257d-123">Azure AD Onlinebankenlösung Informationen (B2C):</span><span class="sxs-lookup"><span data-stu-id="8257d-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="8257d-124">Mandantenname.</span><span class="sxs-lookup"><span data-stu-id="8257d-124">Tenant Name.</span></span>
    - <span data-ttu-id="8257d-125">Kundenkennung.</span><span class="sxs-lookup"><span data-stu-id="8257d-125">Client ID.</span></span>
    - <span data-ttu-id="8257d-126">Benutzerdefinierte Domäne für Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="8257d-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="8257d-127">Antwort auf URL.</span><span class="sxs-lookup"><span data-stu-id="8257d-127">Reply URL.</span></span>
    - <span data-ttu-id="8257d-128">Richtlinienkennung zur Registrierung anmelden.</span><span class="sxs-lookup"><span data-stu-id="8257d-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="8257d-129">Richtlinienkennung für „Kennwort zurücksetzen“.</span><span class="sxs-lookup"><span data-stu-id="8257d-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="8257d-130">Profilrichtlinienkennung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8257d-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="8257d-131">Diese Information kann später über eine Serviceanforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8257d-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="8257d-132">Nachdem Sie die erforderlichen Informationen gesammelt haben, folgen Sie diesen Schritten, um E-Commerce zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="8257d-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="8257d-133">Melden Sie sich bei [LCS](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="8257d-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="8257d-134">Öffnen Sie das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8257d-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="8257d-135">Im Abschnitt **Umgebung** wählen Sie die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8257d-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="8257d-136">Wählen Sie unter **Umgebungsfunktionen** den Link **Einzelhandel verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="8257d-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="8257d-137">Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="8257d-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="8257d-138">Ein Dialogfeld wird angezeigt, in dem Sie die Informationen eingeben müssen, die für die Bereitstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8257d-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="8257d-139">Geben Sie die erforderlichen Informationen ein und wechseln dann zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="8257d-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="8257d-140">Auf der nächsten Seite geben Sie die erforderlichen Informationen ein und übermitteln das Formular.</span><span class="sxs-lookup"><span data-stu-id="8257d-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="8257d-141">Sie werden zur Registerkarte **E-Commerce** zurückgeführt, wo Sie die Initialisierung sehen sollten, die begonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="8257d-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="8257d-142">Um den Initialisierungsstatus später anzuzeigen, **Aktualisieren** Sie oder kehren später zur Registerkarte **E-Commerce** zurück.</span><span class="sxs-lookup"><span data-stu-id="8257d-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="8257d-143">Wenn E-Commerce von LCS aus initialisiert wird, stellt das System mehrere Komponenten bereit, die für E-Commerce erforderlich sind, und ordnet sie der Umgebung zu.</span><span class="sxs-lookup"><span data-stu-id="8257d-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="8257d-144">Nachdem das Bereitstellen abgeschlossen ist, wird die Registerkarte **E-Commerce** auf der Seite **Retailverwaltung** aktualisiert, um der Bereitstellung zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8257d-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="8257d-145">Die Seite zeigt die aktuellsten Anpassungsbereitstellungen und den aktuellen Status aller anderen Bereitstellungen an.</span><span class="sxs-lookup"><span data-stu-id="8257d-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="8257d-146">Sie schließt auch Links zur E-Commerce-Website und dem E-Commerce-Website-Generator ein, in dem Websites erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8257d-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="8257d-147">Auf Commerce-Website-Generator zugreifen</span><span class="sxs-lookup"><span data-stu-id="8257d-147">Access Commerce site builder</span></span>

<span data-ttu-id="8257d-148">Um auf den Commerce-Website-Generator zuzugreifen, gehen Sie zur Registerkarte **E-Commerce** auf der Seite **Retail-Verwaltung** in LCS und wählen Sie den Link **E-Commerce-Websiteverwaltungs-Tool** aus.</span><span class="sxs-lookup"><span data-stu-id="8257d-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="8257d-149">Auf der Zielseite des Site Builders wird eine Ansicht auf Mandantenebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8257d-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="8257d-150">Auf dieser Seite können Sie folgende Aktivitäten durchführen:</span><span class="sxs-lookup"><span data-stu-id="8257d-150">From this page, you can:</span></span>

- <span data-ttu-id="8257d-151">Die Einstellungen auf Mandantenebene ändern.</span><span class="sxs-lookup"><span data-stu-id="8257d-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="8257d-152">Zu einer von Ihnen erstellten Site navigieren und die Berechtigung zum Anzeigen haben.</span><span class="sxs-lookup"><span data-stu-id="8257d-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="8257d-153">Auf Überprüfungsfunktionen wie Moderation und Berichterstattung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8257d-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="8257d-154">Erstellen einer neuer Site.</span><span class="sxs-lookup"><span data-stu-id="8257d-154">Create a new site.</span></span> <span data-ttu-id="8257d-155">Weitere Informationen zum Erstellen einer neuen Website finden Sie unter [Eine E-Commerce-Website erstellen](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="8257d-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="8257d-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8257d-156">Additional resources</span></span>

[<span data-ttu-id="8257d-157">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="8257d-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8257d-158">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="8257d-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8257d-159">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="8257d-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8257d-160">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="8257d-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8257d-161">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="8257d-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8257d-162">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="8257d-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8257d-163">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="8257d-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8257d-164">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="8257d-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8257d-165">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="8257d-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8257d-166">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="8257d-166">Enable location-based store detection</span></span>](enable-store-detection.md)
