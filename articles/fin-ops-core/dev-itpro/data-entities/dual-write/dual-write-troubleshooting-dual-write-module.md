---
title: Probleme mit dem Modul für duales Schreiben in Finance and Operations-Apps behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul Duales Schreiben in der Finance and Operations App zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172759"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="14037-103">Probleme mit dem Modul für duales Schreiben in Finance and Operations-Apps behandeln</span><span class="sxs-lookup"><span data-stu-id="14037-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="14037-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="14037-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="14037-105">Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul **Duales Schreiben** in der Finance and Operations App zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="14037-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14037-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="14037-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="14037-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="14037-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="14037-108">Sie können das Modul Duales Schreiben in der Finance and Operations App nicht laden</span><span class="sxs-lookup"><span data-stu-id="14037-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="14037-109">Wenn Sie die Seite **Duales Schreiben** nicht öffnen können durch Auswahl der Kachel **Duales Schreiben** im Arbeitsbereich **Datenmverwaltung**, ist der Datenintegrationsdienst wahrscheinlich ausgefallen.</span><span class="sxs-lookup"><span data-stu-id="14037-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="14037-110">Erstellen Sie ein Support-Ticket, um einen Neustart des Datenintegrationsdienstes anzufordern.</span><span class="sxs-lookup"><span data-stu-id="14037-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="14037-111">Fehler beim Versuch, eine neue Entitätszuordnung zu erstellen</span><span class="sxs-lookup"><span data-stu-id="14037-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="14037-112">**Erforderliche Anmeldeinformationen zum Lösen des Problems:** Azure AD Mandant Admin</span><span class="sxs-lookup"><span data-stu-id="14037-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="14037-113">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, eine neue Entität für Duales Schreiben zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="14037-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="14037-114">*Der Antwortstatuscode zeigt keinen Erfolg an: 401 (Nicht erlaubt)*</span><span class="sxs-lookup"><span data-stu-id="14037-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="14037-115">Dieser Fehler tritt auf, weil nur ein Azure AD Mandantenadministrator eine neue Entitätszuordnung hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="14037-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="14037-116">Um das Problem zu beheben, melden Sie sich bei der Finance and Operations App als Azure AD Administratormandant an.</span><span class="sxs-lookup"><span data-stu-id="14037-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="14037-117">Sie müssen auch ins Web.PowerApps.com gehen und Ihre Verbindung erneut bestätigen.</span><span class="sxs-lookup"><span data-stu-id="14037-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="14037-118">Fehler beim Öffnen der Benutzeroberfläche Duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="14037-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="14037-119">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, über den Arbeitsbereich **Datenmanagement** auf Duales Schreiben zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="14037-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="14037-120">*login.microsoftonline.com weigerte sich, eine Verbindung herzustellen.*</span><span class="sxs-lookup"><span data-stu-id="14037-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="14037-121">Um das Problem zu beheben, melden Sie sich über ein InPrivate-Fenster bei Microsoft Edge, ein Inkognito-Fenster in Chromium oder ein Inkognito-Fenster in Google Chrome an.</span><span class="sxs-lookup"><span data-stu-id="14037-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="14037-122">Sie müssen auch Cookies von Drittanbietern entsperren oder löschen.</span><span class="sxs-lookup"><span data-stu-id="14037-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="14037-123">Fehler beim Verknüpfen der Umgebung für Duales Schreiben oder Hinzufügen einer neuen Entitätszuordnung</span><span class="sxs-lookup"><span data-stu-id="14037-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="14037-124">**Erforderliche Anmeldeinformationen zum Lösen des Problems:** Azure AD Mandant Admin</span><span class="sxs-lookup"><span data-stu-id="14037-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="14037-125">Beim Verknüpfen oder Erstellen von Zuordnungen kann der folgende Fehler auftreten:</span><span class="sxs-lookup"><span data-stu-id="14037-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="14037-126">*Antwortstatuscode zeigt keinen Erfolg an: 403 (Token-Austausch).<br> Sitzungs-ID: \<Ihre Sitzungs-ID\><br> Stammaktivitäts-ID: \<Ihre Stammaktivitäts-ID\>*</span><span class="sxs-lookup"><span data-stu-id="14037-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="14037-127">Dieser Fehler kann auftreten, wenn Sie nicht über ausreichende Berechtigungen verfügen, um Duales Schreiben zu verknüpfen oder Zuordnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="14037-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="14037-128">Sie müssen ein Azure AD Mandantenadministratorkonto zum Verknüpfen von Umgebungen und Hinzufügen neuer Entitätszuordnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="14037-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="14037-129">Nach dem Einrichten können Sie jedoch ein Nicht-Administratorkonto verwenden, um den Status zu überwachen und die Zuordnungen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="14037-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="14037-130">Fehler beim Beenden der Entitätszuordnung</span><span class="sxs-lookup"><span data-stu-id="14037-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="14037-131">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Entitätszuordnung zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="14037-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="14037-132">*\[verboten\], \[{„Status“: 403, „Quelle“:„“,„Nachricht“:„Fehler beim Token-Austausch: Benutzer darf nicht auf die Verbindung dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx“}\] zugreifen. Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten.*</span><span class="sxs-lookup"><span data-stu-id="14037-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="14037-133">Dieser Fehler tritt auf, wenn die verknüpfte Common Data Service Umgebung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="14037-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="14037-134">Erstellen Sie ein Ticket für das Datenintegrationsteam, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="14037-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="14037-135">Fügen Sie die Netzwerkablaufverfolgung hinzu, damit das Datenintegrationsteam die Zuordnung als **wird nicht ausgeführt** im hinteren Ende markieren kann.</span><span class="sxs-lookup"><span data-stu-id="14037-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
