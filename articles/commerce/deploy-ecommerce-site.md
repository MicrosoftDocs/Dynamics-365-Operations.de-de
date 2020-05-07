---
title: Bereitstellen eines neuen E-Commerce-Mandanten
description: In diesem Thema wird beschrieben, wie Sie einen neuen E-Commerce-Mandanten bereitstellen, indem Microsoft Dynamics Lifecycle Services (LCS) verwenden.
author: psimolin
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3febd3ca36f4d517033e910c4087ad3a6ffff35a
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269934"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="44dfa-103">Bereitstellen eines neuen E-Commerce-Mandanten</span><span class="sxs-lookup"><span data-stu-id="44dfa-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="44dfa-104">In diesem Thema wird beschrieben, wie Sie eine neue E-Commerce-Site bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="44dfa-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="44dfa-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="44dfa-105">Overview</span></span>

<span data-ttu-id="44dfa-106">Microsoft Dynamics Lifecycle Services (LCS) ist ein Cloud-basierter kooperativer Arbeitsbereich, den Partnern und Kunden verwenden können, um die Projekte und Umgebung zu verwalten, die neuesten Informationen anzuzeigen über die Microsoft Dynamics Produkte und Funktionen und Stützvorfälle zu erstellen, nachzuverfolgen und zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="44dfa-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="44dfa-107">E-Commerce-Verwaltungsfunktionen sind in LCS integriert.</span><span class="sxs-lookup"><span data-stu-id="44dfa-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="44dfa-108">Weitere Informationen zu LCS finden Sie unter [Lifecycle Services Benutzerhandbuch](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="44dfa-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="44dfa-109">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="44dfa-109">Get started</span></span>

<span data-ttu-id="44dfa-110">Bevor Sie E-Commerce initialisieren können, müssen Sie ein Projekt, eine Umgebung und ein Retail Cloud Scale Unit (RCSU) initialisieren.</span><span class="sxs-lookup"><span data-stu-id="44dfa-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="44dfa-111">Um die Initialisierung in LCS zu bewerkstelligen, müssen Sie über Berechtigungen entweder als Projekt-Inhaber oder Umgebungsmanager haben.</span><span class="sxs-lookup"><span data-stu-id="44dfa-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="44dfa-112">Die Produktion und Sandboxumgebungstopologien werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44dfa-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="44dfa-113">Weitere Informationen über Umgebungen finden Sie unter [Umgebungsplanung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="44dfa-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="44dfa-114">Weitere Informationen zur RCSU-Compliance finden Sie unter [Retail Cloud Scale Unit initialisieren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="44dfa-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="44dfa-115">E-Commerce initialisieren</span><span class="sxs-lookup"><span data-stu-id="44dfa-115">Initialize e-Commerce</span></span>

<span data-ttu-id="44dfa-116">Verwenden Sie diese Prozedur, um die E-Commerce-Funktion in einer vorhandenen Umgebung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="44dfa-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="44dfa-117">Bevor Sie beginnen, stellen Sie sicher, dass Sie folgende Informationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="44dfa-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="44dfa-118">Die RCSU,die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44dfa-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="44dfa-119">Die Microsoft Azure Active Directory Sicherheitsgruppe, die für E-Commerce-Systemadministratoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44dfa-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="44dfa-120">Die Microsoft Azure Active Directory Sicherheitsgruppe, die für Bewertungen verwendet wird und Moderatoren überprüft.</span><span class="sxs-lookup"><span data-stu-id="44dfa-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="44dfa-121">Die Domänen, die der Umgebung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="44dfa-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="44dfa-122">Zudem können Sie folgende optionale Informationen erfassen:</span><span class="sxs-lookup"><span data-stu-id="44dfa-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="44dfa-123">Azure AD Onlinebankenlösung Informationen (B2C):</span><span class="sxs-lookup"><span data-stu-id="44dfa-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="44dfa-124">Mandantenname.</span><span class="sxs-lookup"><span data-stu-id="44dfa-124">Tenant Name.</span></span>
    - <span data-ttu-id="44dfa-125">Kundenkennung.</span><span class="sxs-lookup"><span data-stu-id="44dfa-125">Client ID.</span></span>
    - <span data-ttu-id="44dfa-126">Benutzerdefinierte Domäne für Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="44dfa-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="44dfa-127">Antwort auf URL.</span><span class="sxs-lookup"><span data-stu-id="44dfa-127">Reply URL.</span></span>
    - <span data-ttu-id="44dfa-128">Richtlinienkennung zur Registrierung anmelden.</span><span class="sxs-lookup"><span data-stu-id="44dfa-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="44dfa-129">Richtlinienkennung für „Kennwort zurücksetzen“.</span><span class="sxs-lookup"><span data-stu-id="44dfa-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="44dfa-130">Profilrichtlinienkennung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="44dfa-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="44dfa-131">Diese Information kann später über eine Serviceanforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="44dfa-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="44dfa-132">Nachdem Sie die erforderlichen Informationen gesammelt haben, folgen Sie diesen Schritten, um E-Commerce zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="44dfa-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="44dfa-133">Melden Sie sich bei [LCS](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="44dfa-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="44dfa-134">Öffnet das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="44dfa-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="44dfa-135">Im Abschnitt **Umgebung** wählen Sie die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="44dfa-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="44dfa-136">Wählen Sie unter **Umgebungsfunktionen** den Link **Einzelhandel verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="44dfa-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="44dfa-137">Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="44dfa-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="44dfa-138">Ein Dialogfeld wird angezeigt, in dem Sie die Informationen eingeben müssen, die für die Bereitstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="44dfa-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="44dfa-139">Geben Sie die erforderlichen Informationen ein und wechseln dann zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="44dfa-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="44dfa-140">Auf der nächsten Seite geben Sie die erforderlichen Informationen ein und übermitteln das Formular.</span><span class="sxs-lookup"><span data-stu-id="44dfa-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="44dfa-141">Sie werden zur Registerkarte **E-Commerce** zurückgeführt, wo Sie die Initialisierung sehen sollten, die begonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="44dfa-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="44dfa-142">Um den Initialisierungsstatus später anzuzeigen, **Aktualisieren** Sie oder kehren später zur Registerkarte **E-Commerce** zurück.</span><span class="sxs-lookup"><span data-stu-id="44dfa-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="44dfa-143">Wenn E-Commerce von LCS initialisiert wird, erstellt das System mehrere Komponenten, die für E-Commerce erforderlich sind bereit und ordnet sie der Umgebung zu.</span><span class="sxs-lookup"><span data-stu-id="44dfa-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="44dfa-144">Nachdem das Bereitstellen abgeschlossen ist, wird die Registerkarte **E-Commerce** auf der Seite **Retailverwaltung** aktualisiert, um der Bereitstellung zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="44dfa-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="44dfa-145">Die Seite zeigt die aktuellsten Anpassungsbereitstellungen und den aktuellen Status aller anderen Bereitstellungen an.</span><span class="sxs-lookup"><span data-stu-id="44dfa-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="44dfa-146">Sie schließt auch Links zur E-Commerce-Site und dem E-Commerce-Site-Builder ein, in dem Sites erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44dfa-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="44dfa-147">Site Builder aufrufen</span><span class="sxs-lookup"><span data-stu-id="44dfa-147">Access site builder</span></span>

<span data-ttu-id="44dfa-148">Um auf den Site Builder zuzugreifen, gehen Sie zur Registerkarte **E-Commerce** auf der Seite **Retail-Verwaltung** in LCS und wählen Sie den Link **E-Commerce-Site-Management-Tool**.</span><span class="sxs-lookup"><span data-stu-id="44dfa-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="44dfa-149">Auf der Zielseite des Site Builders wird eine Ansicht auf Mandantenebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44dfa-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="44dfa-150">Auf dieser Seite können Sie folgende Aktivitäten durchführen:</span><span class="sxs-lookup"><span data-stu-id="44dfa-150">From this page, you can:</span></span>

- <span data-ttu-id="44dfa-151">Die Einstellungen auf Mandantenebene ändern.</span><span class="sxs-lookup"><span data-stu-id="44dfa-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="44dfa-152">Zu einer von Ihnen erstellten Site navigieren und die Berechtigung zum Anzeigen haben.</span><span class="sxs-lookup"><span data-stu-id="44dfa-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="44dfa-153">Auf Überprüfungsfunktionen wie Moderation und Berichterstattung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="44dfa-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="44dfa-154">Erstellen einer neuer Site.</span><span class="sxs-lookup"><span data-stu-id="44dfa-154">Create a new site.</span></span> <span data-ttu-id="44dfa-155">Weitere Informationen zum Erstellen einer neuen Site finden Sie unter [E-Commerce-Site erstellen](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="44dfa-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="44dfa-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="44dfa-156">Additional resources</span></span>

[<span data-ttu-id="44dfa-157">Ihren Domänennamen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="44dfa-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="44dfa-158">E-Commerce-Site erstellen</span><span class="sxs-lookup"><span data-stu-id="44dfa-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="44dfa-159">Onlineshopkanal einrichten</span><span class="sxs-lookup"><span data-stu-id="44dfa-159">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="44dfa-160">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="44dfa-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="44dfa-161">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="44dfa-161">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="44dfa-162">URL-Weiterleitungen in großen Mengen hochladen</span><span class="sxs-lookup"><span data-stu-id="44dfa-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="44dfa-163">Einrichten eines B2C-Mandanten in Commerce</span><span class="sxs-lookup"><span data-stu-id="44dfa-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="44dfa-164">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="44dfa-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="44dfa-165">Konfigurieren Sie mehrere B2C-Mandanten in einer Commerce-Umgebung</span><span class="sxs-lookup"><span data-stu-id="44dfa-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="44dfa-166">Hinzufügen von Unterstützung für ein Content Delivery Network (CDN)</span><span class="sxs-lookup"><span data-stu-id="44dfa-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="44dfa-167">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="44dfa-167">Enable location-based store detection</span></span>](enable-store-detection.md)
