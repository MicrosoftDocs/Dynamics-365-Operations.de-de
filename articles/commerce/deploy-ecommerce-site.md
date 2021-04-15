---
title: Neuen E-Commerce-Mandanten bereitstellen
description: In diesem Thema wird beschrieben, wie Sie eine neue Dynamics 365 Commerce-E-Commerce-Website bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0fff5d47d6eb3e08288d17853fcd94f9eab843c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801948"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="b9260-103">Neuen E-Commerce-Mandanten bereitstellen</span><span class="sxs-lookup"><span data-stu-id="b9260-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9260-104">In diesem Thema wird beschrieben, wie Sie eine neue Dynamics 365 Commerce-E-Commerce-Website bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9260-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="b9260-105">Microsoft Dynamics Lifecycle Services (LCS) ist ein Cloud-basierter kooperativer Arbeitsbereich, den Partnern und Kunden verwenden können, um die Projekte und Umgebung zu verwalten, die neuesten Informationen anzuzeigen über die Microsoft Dynamics Produkte und Funktionen und Stützvorfälle zu erstellen, nachzuverfolgen und zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="b9260-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="b9260-106">E-Commerce-Verwaltungsfunktionen sind in LCS integriert.</span><span class="sxs-lookup"><span data-stu-id="b9260-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="b9260-107">Weitere Informationen zu LCS finden Sie unter [Lifecycle Services Benutzerhandbuch](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="b9260-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="b9260-108">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="b9260-108">Get started</span></span>

<span data-ttu-id="b9260-109">Bevor Sie E-Commerce initialisieren können, müssen Sie ein Projekt, eine Umgebung und eine Retail Cloud Scale Unit (RCSU) initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9260-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="b9260-110">Um die Initialisierung in LCS zu bewerkstelligen, müssen Sie über Berechtigungen entweder als Projekt-Inhaber oder Umgebungsmanager haben.</span><span class="sxs-lookup"><span data-stu-id="b9260-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="b9260-111">Die Produktion und Sandboxumgebungstopologien werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9260-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="b9260-112">Weitere Informationen über Umgebungen finden Sie unter [Umgebungsplanung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="b9260-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="b9260-113">Weitere Informationen zur RCSU-Compliance finden Sie unter [Retail Cloud Scale Unit initialisieren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="b9260-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="b9260-114">E-Commerce initialisieren</span><span class="sxs-lookup"><span data-stu-id="b9260-114">Initialize e-commerce</span></span>

<span data-ttu-id="b9260-115">Verwenden Sie diese Prozedur, um die E-Commerce-Funktion in einer vorhandenen Umgebung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9260-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="b9260-116">Bevor Sie beginnen, stellen Sie sicher, dass Sie folgende Informationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="b9260-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="b9260-117">Die RCSU,die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9260-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="b9260-118">Die Microsoft Azure Active Directory-Sicherheitsgruppe, die für E-Commerce-Systemadministratoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9260-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="b9260-119">Die Microsoft Azure Active Directory Sicherheitsgruppe, die für Bewertungen verwendet wird und Moderatoren überprüft.</span><span class="sxs-lookup"><span data-stu-id="b9260-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="b9260-120">Die Domänen, die der Umgebung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b9260-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="b9260-121">Zudem können Sie folgende optionale Informationen erfassen:</span><span class="sxs-lookup"><span data-stu-id="b9260-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="b9260-122">Azure AD Onlinebankenlösung Informationen (B2C):</span><span class="sxs-lookup"><span data-stu-id="b9260-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="b9260-123">Mandantenname.</span><span class="sxs-lookup"><span data-stu-id="b9260-123">Tenant Name.</span></span>
    - <span data-ttu-id="b9260-124">Kundenkennung.</span><span class="sxs-lookup"><span data-stu-id="b9260-124">Client ID.</span></span>
    - <span data-ttu-id="b9260-125">Benutzerdefinierte Domäne für Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="b9260-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="b9260-126">Antwort auf URL.</span><span class="sxs-lookup"><span data-stu-id="b9260-126">Reply URL.</span></span>
    - <span data-ttu-id="b9260-127">Richtlinienkennung zur Registrierung anmelden.</span><span class="sxs-lookup"><span data-stu-id="b9260-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="b9260-128">Richtlinienkennung für „Kennwort zurücksetzen“.</span><span class="sxs-lookup"><span data-stu-id="b9260-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="b9260-129">Profilrichtlinienkennung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b9260-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="b9260-130">Diese Information kann später über eine Serviceanforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b9260-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="b9260-131">Nachdem Sie die erforderlichen Informationen gesammelt haben, folgen Sie diesen Schritten, um E-Commerce zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b9260-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="b9260-132">Melden Sie sich bei [LCS](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="b9260-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="b9260-133">Öffnen Sie das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b9260-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="b9260-134">Im Abschnitt **Umgebung** wählen Sie die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b9260-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="b9260-135">Wählen Sie unter **Umgebungsfunktionen** den Link **Einzelhandel verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="b9260-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="b9260-136">Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="b9260-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="b9260-137">Ein Dialogfeld wird angezeigt, in dem Sie die Informationen eingeben müssen, die für die Bereitstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b9260-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="b9260-138">Geben Sie die erforderlichen Informationen ein und wechseln dann zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="b9260-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="b9260-139">Auf der nächsten Seite geben Sie die erforderlichen Informationen ein und übermitteln das Formular.</span><span class="sxs-lookup"><span data-stu-id="b9260-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="b9260-140">Sie werden zur Registerkarte **E-Commerce** zurückgeführt, wo Sie die Initialisierung sehen sollten, die begonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9260-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="b9260-141">Um den Initialisierungsstatus später anzuzeigen, **Aktualisieren** Sie oder kehren später zur Registerkarte **E-Commerce** zurück.</span><span class="sxs-lookup"><span data-stu-id="b9260-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="b9260-142">Wenn E-Commerce von LCS aus initialisiert wird, stellt das System mehrere Komponenten bereit, die für E-Commerce erforderlich sind, und ordnet sie der Umgebung zu.</span><span class="sxs-lookup"><span data-stu-id="b9260-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="b9260-143">Nachdem das Bereitstellen abgeschlossen ist, wird die Registerkarte **E-Commerce** auf der Seite **Retailverwaltung** aktualisiert, um der Bereitstellung zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b9260-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="b9260-144">Die Seite zeigt die aktuellsten Anpassungsbereitstellungen und den aktuellen Status aller anderen Bereitstellungen an.</span><span class="sxs-lookup"><span data-stu-id="b9260-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="b9260-145">Sie schließt auch Links zur E-Commerce-Website und dem E-Commerce-Website-Generator ein, in dem Websites erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b9260-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="b9260-146">Auf Commerce-Website-Generator zugreifen</span><span class="sxs-lookup"><span data-stu-id="b9260-146">Access Commerce site builder</span></span>

<span data-ttu-id="b9260-147">Um auf den Commerce-Website-Generator zuzugreifen, gehen Sie zur Registerkarte **E-Commerce** auf der Seite **Retail-Verwaltung** in LCS und wählen Sie den Link **E-Commerce-Websiteverwaltungs-Tool** aus.</span><span class="sxs-lookup"><span data-stu-id="b9260-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="b9260-148">Auf der Zielseite des Site Builders wird eine Ansicht auf Mandantenebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b9260-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="b9260-149">Auf dieser Seite können Sie folgende Aktivitäten durchführen:</span><span class="sxs-lookup"><span data-stu-id="b9260-149">From this page, you can:</span></span>

- <span data-ttu-id="b9260-150">Die Einstellungen auf Mandantenebene ändern.</span><span class="sxs-lookup"><span data-stu-id="b9260-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="b9260-151">Zu einer von Ihnen erstellten Site navigieren und die Berechtigung zum Anzeigen haben.</span><span class="sxs-lookup"><span data-stu-id="b9260-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="b9260-152">Auf Überprüfungsfunktionen wie Moderation und Berichterstattung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b9260-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="b9260-153">Erstellen einer neuer Site.</span><span class="sxs-lookup"><span data-stu-id="b9260-153">Create a new site.</span></span> <span data-ttu-id="b9260-154">Weitere Informationen zum Erstellen einer neuen Website finden Sie unter [Eine E-Commerce-Website erstellen](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="b9260-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b9260-155">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9260-155">Additional resources</span></span>

[<span data-ttu-id="b9260-156">Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b9260-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b9260-157">E-Commerce-Website erstellen</span><span class="sxs-lookup"><span data-stu-id="b9260-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b9260-158">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="b9260-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b9260-159">Robots.txt-Dateien verwalten</span><span class="sxs-lookup"><span data-stu-id="b9260-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b9260-160">URL-Umleitungen in Massen hochladen</span><span class="sxs-lookup"><span data-stu-id="b9260-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b9260-161">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="b9260-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b9260-162">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="b9260-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b9260-163">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="b9260-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b9260-164">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="b9260-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b9260-165">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="b9260-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
