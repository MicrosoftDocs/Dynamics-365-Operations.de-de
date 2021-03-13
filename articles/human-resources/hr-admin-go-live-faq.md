---
title: FAQ live schalten
description: In diesem Thema werden häufig gestellte Fragen zur Liveschaltung mit einem Dynamics 365 Human Resources Implementierungsprojekt behandelt.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5041d515b261bb3e4b14885e0ec0ce788edf729
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112651"
---
# <a name="go-live-faq"></a><span data-ttu-id="399e9-103">FAQ live schalten</span><span class="sxs-lookup"><span data-stu-id="399e9-103">Go-live FAQ</span></span> 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="399e9-104">In diesem Thema werden häufig gestellte Fragen zur Liveschaltung mit einem Dynamics 365 Human Resources Implementierungsprojekt behandelt.</span><span class="sxs-lookup"><span data-stu-id="399e9-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="399e9-105">Wann kann ich meine Produktionsumgebung konfigurieren und anfordern?</span><span class="sxs-lookup"><span data-stu-id="399e9-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="399e9-106">In der Regel wird eine Produktionsumgebung bereitgestellt, nachdem die folgenden Kriterien erfüllt wurden:</span><span class="sxs-lookup"><span data-stu-id="399e9-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="399e9-107">Alle Anpassungen sind vollständig.</span><span class="sxs-lookup"><span data-stu-id="399e9-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="399e9-108">Der User Acceptance Test (UAT) ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="399e9-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="399e9-109">Der Kunde hat die Lösung abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="399e9-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="399e9-110">Es gibt keine Blockierungsprobleme für die Inbetriebnahme.</span><span class="sxs-lookup"><span data-stu-id="399e9-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="399e9-111">Wenn sich qualifizierte Kunden in dieser Phase befinden, arbeitet das Microsoft FastTrack-Team mit dem Projektteam zusammen, um eine Go-Live-Bewertung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="399e9-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="399e9-112">Was sind die Voraussetzungen für die Bereitstellung einer Produktionsumgebung?</span><span class="sxs-lookup"><span data-stu-id="399e9-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="399e9-113">Eine Liste der Voraussetzungen finden Sie unter [Bereiten Sie sich auf die Inbetriebnahme vor](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="399e9-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="399e9-114">Was ist eine Go-Live-Bewertung?</span><span class="sxs-lookup"><span data-stu-id="399e9-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="399e9-115">Die Go-Live-Bewertung ist Teil des [Microsoft FastTrack-Programms](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="399e9-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="399e9-116">Während dieser Überprüfung bewertet ein Lösungsarchitekt, ob ein Implementierungsprojekt für eine erfolgreiche Umstellung und Inbetriebnahme bereit ist.</span><span class="sxs-lookup"><span data-stu-id="399e9-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="399e9-117">Diese Überprüfung ist für jedes Implementierungsprojekt obligatorisch, bevor Sie die Inbetriebnahme in einer Produktionsumgebung anfordern können.</span><span class="sxs-lookup"><span data-stu-id="399e9-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="399e9-118">Unsere Sandbox-Umgebungen werden im zentralen US-Rechenzentrum bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="399e9-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="399e9-119">Wir möchten, dass unsere Produktionsumgebungen im Rechenzentrum im Westen der USA bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="399e9-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="399e9-120">Kann ich in meiner Produktionskonfiguration West US als Rechenzentrum auswählen?</span><span class="sxs-lookup"><span data-stu-id="399e9-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="399e9-121">LCS hindert Sie nicht daran, ein anderes Rechenzentrum auszuwählen, wenn Sie eine Personalumgebung bereitstellen. Wir empfehlen jedoch dringend, kein anderes Rechenzentrum auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="399e9-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="399e9-122">Wenn Sie möchten, dass sich Ihre Produktionsumgebung im Rechenzentrum in den USA befindet, sollten Sie zuerst Ihre Sandbox-Umgebungen im Rechenzentrum in den USA erneut bereitstellen, testen und abmelden.</span><span class="sxs-lookup"><span data-stu-id="399e9-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="399e9-123">Informationen zur Auswahl des richtigen Rechenzentrums finden Sie unter [Netzwerkanforderungen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="399e9-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="399e9-124">Welche Zugriffsebene habe ich für meine Personalumgebungen auf die Azure-Ressourcen?</span><span class="sxs-lookup"><span data-stu-id="399e9-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="399e9-125">Der Zugriff auf die Personalumgebungen ist begrenzt.</span><span class="sxs-lookup"><span data-stu-id="399e9-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="399e9-126">Sie können nicht auf die virtuelle Maschine (VM) oder Microsoft Internet Information Services (IIS) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="399e9-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="399e9-127">Sie können auch nicht über auf die Datenbank über Microsoft SQL Server Management Studio zugreifen.</span><span class="sxs-lookup"><span data-stu-id="399e9-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="399e9-128">Sie können zwar nicht auf Ihre Azure-Ressourcen Dynamics 365 Human Resources Umgebungen direkt zugreifen, aber es gibt es zusätzliche Funktionen, mit denen Sie auf Ihre Daten zugreifen können:</span><span class="sxs-lookup"><span data-stu-id="399e9-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="399e9-129">Sie können eine Azure SQL-Datenbank in Ihrem eigenen Azure-Mandanten bereitstellen und die BYOD-Funktion (Bring Your Own Database) zum Synchronisieren von Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="399e9-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="399e9-130">Weitere Informationen finden Sie unter [Eigene Datenbank nutzen (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="399e9-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="399e9-131">Sie können Dataverse Integration zum Synchronisieren ausgewählter Entitäten in die Dataverse Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="399e9-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="399e9-132">Weitere Informationen finden Sie in den [Dataverse-Tabellen](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="399e9-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="399e9-133">Wie oft wird meine Produktionsdatenbank gesichert?</span><span class="sxs-lookup"><span data-stu-id="399e9-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="399e9-134">Datenbanken werden durch automatische Sicherungen mit den folgenden Frequenzen geschützt:</span><span class="sxs-lookup"><span data-stu-id="399e9-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="399e9-135">Art der Sicherung</span><span class="sxs-lookup"><span data-stu-id="399e9-135">Type of backup</span></span> | <span data-ttu-id="399e9-136">Häufigkeit</span><span class="sxs-lookup"><span data-stu-id="399e9-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="399e9-137">Vollständige Datenbank-Sicherung</span><span class="sxs-lookup"><span data-stu-id="399e9-137">Full database backup</span></span> | <span data-ttu-id="399e9-138">Wöchentlich</span><span class="sxs-lookup"><span data-stu-id="399e9-138">Weekly</span></span> |
| <span data-ttu-id="399e9-139">Differenzielle Datenbanksicherung</span><span class="sxs-lookup"><span data-stu-id="399e9-139">Differential database backup</span></span> | <span data-ttu-id="399e9-140">Alle 12-24 Stunden</span><span class="sxs-lookup"><span data-stu-id="399e9-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="399e9-141">Transaktionsprotokollsicherung</span><span class="sxs-lookup"><span data-stu-id="399e9-141">Transaction log backup</span></span> | <span data-ttu-id="399e9-142">Alle 5 bis 10 Minuten</span><span class="sxs-lookup"><span data-stu-id="399e9-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="399e9-143">Microsoft verfügt über ausreichende Sicherungen, um die Point-in-Time-Wiederherstellung (PITR) innerhalb der letzten 14 Tage zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="399e9-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="399e9-144">Weitere Informationen über Sicherungen finden Sie unter  [Informationen zu automatischen SQL-Datenbanksicherungen](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="399e9-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="399e9-145">Kann ich eine Kopie der Sicherung meiner Produktionsdatenbank anfordern?</span><span class="sxs-lookup"><span data-stu-id="399e9-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="399e9-146">Nr.</span><span class="sxs-lookup"><span data-stu-id="399e9-146">No.</span></span> <span data-ttu-id="399e9-147">Sie können jedoch eine Datenbankaktualisierungsdienstanforderung senden, um Ihre Produktionsumgebung in Ihre Sandbox-Umgebung zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="399e9-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="399e9-148">Sie können eine Azure SQL-Datenbank in Ihrem eigenen Azure-Mandanten bereitstellen und die BYOD-Funktion zum Synchronisieren von Daten aus Ihrer Produktionsumgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="399e9-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="399e9-149">Weitere Informationen finden Sie unter [Eigene Datenbank nutzen (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="399e9-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="399e9-150">Wie verschiebe ich meine Sandbox-Umgebung für die Inbetriebnahme in die Produktion?</span><span class="sxs-lookup"><span data-stu-id="399e9-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="399e9-151">Da keine Kopierfunktion zum Verschieben Ihrer Umgebung von einer Sandbox in eine Produktionsumgebung verfügbar ist, müssen Sie Datenpakete verwenden, um Daten in Ihre Produktionsumgebung zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="399e9-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="399e9-152">Wir empfehlen, während des gesamten Projekts eine übersichtliche Liste der in Ihrer Sandbox konfigurierten Entitäten zu führen.</span><span class="sxs-lookup"><span data-stu-id="399e9-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="399e9-153">Testen Sie anschließend den Prozess der Umstellung und Migration aller für Ihre Inbetriebnahme erforderlichen Datenpakete.</span><span class="sxs-lookup"><span data-stu-id="399e9-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="399e9-154">Sie müssen alle Datenpakete manuell in die Produktionsumgebung verschieben, wenn Sie bereit sind, live zu gehen.</span><span class="sxs-lookup"><span data-stu-id="399e9-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="399e9-155">Was soll ich tun, wenn meine Produktionsumgebung nicht verfügbar ist?</span><span class="sxs-lookup"><span data-stu-id="399e9-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="399e9-156">Befolgen Sie die unter  [Produktionsausfall melden](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) beschriebenen Schritte.</span><span class="sxs-lookup"><span data-stu-id="399e9-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="399e9-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="399e9-157">See also</span></span>

 [<span data-ttu-id="399e9-158">Liveschaltung vorbereiten</span><span class="sxs-lookup"><span data-stu-id="399e9-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)
