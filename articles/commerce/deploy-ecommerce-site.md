---
title: Bereitstellen eines neuen E-Commerce-Mandanten
description: In diesem Thema wird beschrieben, wie Sie einen neuen E-Commerce-Mandanten bereitstellen, indem Microsoft Dynamics Lifecycle Services (LCS) verwenden.
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945512"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="3a9d8-103">Bereitstellen eines neuen E-Commerce-Mandanten</span><span class="sxs-lookup"><span data-stu-id="3a9d8-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3a9d8-104">In diesem Thema wird beschrieben, wie Sie eine neue E-Commerce-Site bereitstellen, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="3a9d8-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="3a9d8-105">Overview</span></span>
    
<span data-ttu-id="3a9d8-106">Microsoft Dynamics Lifecycle Services (LCS) ist ein Cloud-basierter kooperativer Arbeitsbereich, den Partnern und Kunden verwenden können, um die Projekte und Umgebung zu verwalten, die neuesten Informationen anzuzeigen über die Microsoft Dynamics Produkte und Funktionen und Stützvorfälle zu erstellen, nachzuverfolgen und zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="3a9d8-107">E-Commerce-Verwaltungsfunktionen sind in LCS integriert.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="3a9d8-108">Weitere Informationen zu LCS finden Sie unter [Lifecycle Services Benutzerhandbuch](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="3a9d8-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="3a9d8-109">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="3a9d8-109">Get started</span></span>

<span data-ttu-id="3a9d8-110">Bevor Sie E-Commerce initialisieren können, müssen Sie ein Projekt, eine Umgebung und ein Retail Cloud Scale Unit (RCSU) initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="3a9d8-111">Um die Initialisierung in LCS zu bewerkstelligen, müssen Sie über Berechtigungen entweder als Projekt-Inhaber oder Umgebungsmanager haben.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="3a9d8-112">Die Produktion und Sandboxumgebungstopologien werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="3a9d8-113">Weitere Informationen über Umgebungen finden Sie unter [Umgebungsplanung](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="3a9d8-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="3a9d8-114">Weitere Informationen zur RCSU-Compliance finden Sie unter [Retail Cloud Scale Unit initialisieren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="3a9d8-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="3a9d8-115">E-Commerce initialisieren</span><span class="sxs-lookup"><span data-stu-id="3a9d8-115">Initialize e-Commerce</span></span>

<span data-ttu-id="3a9d8-116">Verwenden Sie diese Prozedur, um die E-Commerce-Funktion in einer vorhandenen Umgebung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="3a9d8-117">Bevor Sie beginnen, stellen Sie sicher, dass Sie folgende Informationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="3a9d8-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="3a9d8-118">Die RCSU,die verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="3a9d8-119">Die Microsoft Azure Active Directory Sicherheitsgruppe, die für E-Commerce-Systemadministratoren verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="3a9d8-120">Die Microsoft Azure Active Directory Sicherheitsgruppe, die für Bewertungen verwendet wird und Moderatoren überprüft.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="3a9d8-121">Die Domänen, die der Umgebung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="3a9d8-122">Zudem können Sie folgende optionale Informationen erfassen:</span><span class="sxs-lookup"><span data-stu-id="3a9d8-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="3a9d8-123">Azure AD Onlinebankenlösung Informationen (B2C):</span><span class="sxs-lookup"><span data-stu-id="3a9d8-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="3a9d8-124">Mandantenname.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-124">Tenant Name.</span></span>
    - <span data-ttu-id="3a9d8-125">Kundenkennung.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-125">Client ID.</span></span>
    - <span data-ttu-id="3a9d8-126">Benutzerdefinierte Domäne für Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="3a9d8-127">Antwort auf URL.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-127">Reply URL.</span></span>
    - <span data-ttu-id="3a9d8-128">Richtlinienkennung zur Registrierung anmelden.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="3a9d8-129">Richtlinienkennung für „Kennwort zurücksetzen“.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="3a9d8-130">Profilrichtlinienkennung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="3a9d8-131">Diese Information kann später über eine Serviceanforderung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="3a9d8-132">Nachdem Sie die erforderlichen Informationen gesammelt haben, folgen Sie diesen Schritten, um E-Commerce zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="3a9d8-133">Melden Sie sich bei [LCS](https://lcs.dynamics.com) an.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="3a9d8-134">Öffnet das Projekt, das die Umgebung enthält, in der Sie E-Commerce initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="3a9d8-135">Im Abschnitt **Umgebung** wählen Sie die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="3a9d8-136">Wählen Sie unter **Umgebungsfunktionen** den Link **Einzelhandel verwalten** aus.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="3a9d8-137">Auf der Registerkarte **E-Commerce** wählen Sie **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="3a9d8-138">Ein Dialogfeld wird angezeigt, in dem Sie die Informationen eingeben müssen, die für die Bereitstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="3a9d8-139">Geben Sie die erforderlichen Informationen ein und wechseln dann zur nächsten Seite.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="3a9d8-140">Auf der nächsten Seite geben Sie die erforderlichen Informationen ein und übermitteln das Formular.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="3a9d8-141">Sie werden zur Registerkarte **E-Commerce** zurückgeführt, wo Sie die Initialisierung sehen sollten, die begonnen wurde.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="3a9d8-142">Um den Initialisierungsstatus später anzuzeigen, **Aktualisieren** Sie oder kehren später zur Registerkarte **E-Commerce** zurück.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="3a9d8-143">Wenn E-Commerce von LCS initialisiert wird, erstellt das System mehrere Komponenten, die für E-Commerce erforderlich sind bereit und ordnet sie der Umgebung zu.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="3a9d8-144">Nachdem das Bereitstellen abgeschlossen ist, wird die Registerkarte **E-Commerce** auf der Seite **Retailverwaltung** aktualisiert, um der Bereitstellung zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="3a9d8-145">Die Seite zeigt die aktuellsten Anpassungsbereitstellungen und den aktuellen Status aller anderen Bereitstellungen an.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="3a9d8-146">Sie schließt auch Links zur E-Commerce-Site und das E-Commerce-Site-Verwaltungstol ein (das Erstellungstool).</span><span class="sxs-lookup"><span data-stu-id="3a9d8-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="3a9d8-147">Zugriff auf die Erstellungsumgebung</span><span class="sxs-lookup"><span data-stu-id="3a9d8-147">Access the authoring environment</span></span>

<span data-ttu-id="3a9d8-148">Um auf die Erstellungsumgebung zuzugreifen, wechseln zur Registerkarte **E-Commerce** auf der Seite **Retailverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="3a9d8-149">Dort finden Sie Links zu Ihre E-Commerce-Site und das Site-Verwaltungstool.</span><span class="sxs-lookup"><span data-stu-id="3a9d8-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a9d8-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3a9d8-150">Additional resources</span></span>

[<span data-ttu-id="3a9d8-151">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="3a9d8-151">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3a9d8-152">Erstellen einer E-Commerce-Webseite</span><span class="sxs-lookup"><span data-stu-id="3a9d8-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3a9d8-153">Zuordnen einer Onlinewebseite zu einem Kanal</span><span class="sxs-lookup"><span data-stu-id="3a9d8-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3a9d8-154">Verwalten von robots.txt-Dateien</span><span class="sxs-lookup"><span data-stu-id="3a9d8-154">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3a9d8-155">Einrichten angepasster Seiten für die Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="3a9d8-155">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3a9d8-156">Unterstützung für ein Content Delivery Network (CDN) hinzufügen</span><span class="sxs-lookup"><span data-stu-id="3a9d8-156">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3a9d8-157">Standortbasierte Shop-Erkennung aktivieren</span><span class="sxs-lookup"><span data-stu-id="3a9d8-157">Enable location-based store detection</span></span>](enable-store-detection.md)
