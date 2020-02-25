---
title: Verwalten von e-Commerce Benutzern und Rollen
description: In diesem Thema wird erläutert, wie Sie Benutzern Zugriff auf die Erstellungsumgebung für Microsoft Dynamics 365 Commerce gewähren.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003532"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="6ee89-103">Verwalten von e-Commerce Benutzern und Rollen</span><span class="sxs-lookup"><span data-stu-id="6ee89-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ee89-104">In diesem Thema wird erläutert, wie Sie Benutzern Zugriff auf die Erstellungsumgebung für Microsoft Dynamics 365 Commerce gewähren.</span><span class="sxs-lookup"><span data-stu-id="6ee89-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="6ee89-105">In der Umgebung zur Site-Erstellung werden von Ihnen in Microsoft erstellte Sicherheitsgruppen verwendet, um den Benutzerzugriff zu steuern und Benutzern die Berechtigung zum Ausführen bestimmter Aufgaben zu erteilen, die Sie in Microsoft Azure Active Directory (Azure AD) erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="6ee89-106">Zunächst weisen Sie jeder Rolle in der Erstellungsumgebung eine neue oder vorhandene Sicherheitsgruppe aus Azure AD zu.</span><span class="sxs-lookup"><span data-stu-id="6ee89-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="6ee89-107">Anschließend erteilen oder widerrufen Sie Berechtigungen für einzelne Benutzer, indem Sie diese Benutzer einer entsprechenden Sicherheitsgruppe hinzufügen oder aus einer Sicherheitsgruppe entfernen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="6ee89-108">Übersicht über Rollen in der Erstellungsumgebung</span><span class="sxs-lookup"><span data-stu-id="6ee89-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="6ee89-109">Die Dynamics 365 for Commerce Erstellungsumgebung unterstützt die folgenden Rollen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="6ee89-110">Rolle</span><span class="sxs-lookup"><span data-stu-id="6ee89-110">Role</span></span>                 | <span data-ttu-id="6ee89-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ee89-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="6ee89-112">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="6ee89-112">System Administrator</span></span> | <span data-ttu-id="6ee89-113">Benutzer mit dieser Rolle haben alle Berechtigungen für alle Tools sowie für alle Bewertungen und Überprüfungen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="6ee89-114">Sie können auch Sites erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-114">They can also create sites.</span></span> |
| <span data-ttu-id="6ee89-115">Administrator</span><span class="sxs-lookup"><span data-stu-id="6ee89-115">Administrator</span></span>   | <span data-ttu-id="6ee89-116">Benutzer mit dieser Rolle haben alle Berechtigungen für alle Tools und RnR in einer bestimmten Site-Struktur.</span><span class="sxs-lookup"><span data-stu-id="6ee89-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="6ee89-117">Internet-Producer</span><span class="sxs-lookup"><span data-stu-id="6ee89-117">Web Producer</span></span>         | <span data-ttu-id="6ee89-118">Benutzer mit dieser Rolle können Seiten, Fragmente und Vorlagen erstellen, Assets hochladen und verwalten sowie Produkte und Kategorien erweitern.</span><span class="sxs-lookup"><span data-stu-id="6ee89-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="6ee89-119">Leser</span><span class="sxs-lookup"><span data-stu-id="6ee89-119">Reader</span></span>               | <span data-ttu-id="6ee89-120">Benutzer mit dieser Rolle können Seiten, Vorlagen, Assets, Fragmente, Layouts und Einstellungen anzeigen, aber möglicherweise keine Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="6ee89-121">RnR-Moderator</span><span class="sxs-lookup"><span data-stu-id="6ee89-121">RnR Moderator</span></span>        | <span data-ttu-id="6ee89-122">Benutzer mit dieser Rolle können Produktbewertungen moderieren.</span><span class="sxs-lookup"><span data-stu-id="6ee89-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="6ee89-123">Systemadministratorrolle</span><span class="sxs-lookup"><span data-stu-id="6ee89-123">System Administrator role</span></span>

<span data-ttu-id="6ee89-124">Wenn Sie Dynamics 365 Commerce in der Microsoft Dynamics Lifecycle Services-(LCS-)Umgebung bereitstellen, werden Sie gebeten, eine Sicherheitsgruppe für die Rolle **Systemadministrator** bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="6ee89-125">Diese Rolle wird dann automatisch auf alle Sites angewendet, die Sie in der von Ihnen konfigurierten Umgebung erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="6ee89-126">Die Sicherheitsgruppe für diese Rolle kann nur in LCS aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ee89-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="6ee89-127">Auf der Seite **Websiteverwaltung** wird sie für alle Websites als schreibgeschützt angezeigt und dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="6ee89-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="6ee89-128">Administratorrolle</span><span class="sxs-lookup"><span data-stu-id="6ee89-128">Administrator role</span></span>

<span data-ttu-id="6ee89-129">Wenn Sie eine neue Site in Commerce erstellen, werden Sie aufgefordert, eine Sicherheitsgruppe für die Rolle **Administrator** bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="6ee89-130">In der Tabelle weiter oben in diesem Thema finden Sie eine Übersicht über die Berechtigungen, die diese Rolle gewährt.</span><span class="sxs-lookup"><span data-stu-id="6ee89-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="6ee89-131">Hinzufügen oder Aktualisieren von Sicherheitsgruppen</span><span class="sxs-lookup"><span data-stu-id="6ee89-131">Add or update security groups</span></span>

<span data-ttu-id="6ee89-132">Nachdem Ihre Site erstellt wurde, werden nur Benutzer in den Sicherheitsgruppen angezeigt, die dem **Systemadministrator** zugeordnet sind, und **Administrator**-Rollen können auf die Erstellungsumgebung für diese Site zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="6ee89-133">Um Benutzer den Rollen **Internet-Producer**, **RnR-Moderator** und **Leser** zuzuweisen, müssen Sie diesen Rollen Sicherheitsgruppen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="6ee89-134">Gehen Sie folgendermaßen vor, um einer Rolle eine Sicherheitsgruppe hinzuzufügen oder eine Sicherheitsgruppe zu aktualisieren, die derzeit einer Rolle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6ee89-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="6ee89-135">Gehen Sie zu der Site, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="6ee89-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="6ee89-136">Öffnen Sie in **Websiteverwaltung** die Seite **Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="6ee89-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="6ee89-137">Wählen Sie die zu ändernde Rolle aus.</span><span class="sxs-lookup"><span data-stu-id="6ee89-137">Select the role to modify.</span></span>
1. <span data-ttu-id="6ee89-138">Fügen Sie Sicherheitsgruppen zu Rollen hinzu oder entfernen Sie Sicherheitsgruppen aus Rollen.</span><span class="sxs-lookup"><span data-stu-id="6ee89-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ee89-139">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ee89-139">Additional resources</span></span>

[<span data-ttu-id="6ee89-140">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="6ee89-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="6ee89-141">Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site</span><span class="sxs-lookup"><span data-stu-id="6ee89-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="6ee89-142">Verwalten der Inhaltssicherheitsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="6ee89-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
