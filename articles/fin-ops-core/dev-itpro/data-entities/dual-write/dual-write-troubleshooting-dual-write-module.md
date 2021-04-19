---
title: Probleme mit dem dualen Scheiben in Finance and Operations-Apps behandeln
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul Duales Schreiben in der Finance and Operations App zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 46f561d3cddf1a94ff71e284e8085ff86d678600
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754061"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a><span data-ttu-id="8f9c5-103">Probleme mit dem dualen Scheiben in Finance and Operations-Apps behandeln</span><span class="sxs-lookup"><span data-stu-id="8f9c5-103">Troubleshoot dual-write issues in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8f9c5-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="8f9c5-105">Dieses Thema enthält insbesondere Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Modul **Duales Schreiben** in der Finance and Operations App zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f9c5-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="8f9c5-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="8f9c5-108">Sie können das Modul Duales Schreiben in der Finance and Operations App nicht laden</span><span class="sxs-lookup"><span data-stu-id="8f9c5-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="8f9c5-109">Wenn Sie die Seite **Duales Schreiben** nicht öffnen können durch Auswahl der Kachel **Duales Schreiben** im Arbeitsbereich **Datenmverwaltung**, ist der Datenintegrationsdienst wahrscheinlich ausgefallen.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="8f9c5-110">Erstellen Sie ein Support-Ticket, um einen Neustart des Datenintegrationsdienstes anzufordern.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="8f9c5-111">Fehler beim Versuch, eine neue Tabellenzuordnung zu erstellen</span><span class="sxs-lookup"><span data-stu-id="8f9c5-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="8f9c5-112">**Erforderliche Anmeldeinformationen zur Behebung des Problems:** Derselbe Benutzer, der duales Schreiben eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="8f9c5-113">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, eine neue Tabelle für Duales Schreiben zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-113">You might receive the following error message when you try to configure a new table for dual-write.</span></span> <span data-ttu-id="8f9c5-114">Der einzige Benutzer, der eine Karte erstellen kann, ist der Benutzer, der die duale Schreibverbindung eingerichtet hat.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="8f9c5-115">*Der Antwortstatuscode zeigt keinen Erfolg an: 401 (Nicht erlaubt)*</span><span class="sxs-lookup"><span data-stu-id="8f9c5-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="8f9c5-116">Fehler beim Öffnen der Benutzeroberfläche Duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="8f9c5-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="8f9c5-117">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, über den Arbeitsbereich **Datenmanagement** auf Duales Schreiben zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="8f9c5-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="8f9c5-118">*login.microsoftonline.com weigerte sich, eine Verbindung herzustellen.*</span><span class="sxs-lookup"><span data-stu-id="8f9c5-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="8f9c5-119">Um das Problem zu beheben, melden Sie sich über ein InPrivate-Fenster bei Microsoft Edge, ein Inkognito-Fenster in Chromium oder ein Inkognito-Fenster in Google Chrome an.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="8f9c5-120">Sie müssen auch Cookies von Drittanbietern entsperren oder löschen.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="8f9c5-121">Fehler beim Verknüpfen der Umgebung für duales Schreiben oder Hinzufügen einer neuen Tabellenzuordnung</span><span class="sxs-lookup"><span data-stu-id="8f9c5-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="8f9c5-122">**Erforderliche Rolle zur Behebung des Problems:** Systemadministrator in Finance and Operations-Apps und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="8f9c5-123">Beim Verknüpfen oder Erstellen von Zuordnungen kann der folgende Fehler auftreten:</span><span class="sxs-lookup"><span data-stu-id="8f9c5-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="8f9c5-124">*Antwortstatuscode zeigt keinen Erfolg an: 403 (Token-Austausch).<br> Sitzungs-ID: \<your session id\><br> Stammaktivitäts-ID: \<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="8f9c5-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="8f9c5-125">Dieser Fehler kann auftreten, wenn Sie nicht über ausreichende Berechtigungen verfügen, um Duales Schreiben zu verknüpfen oder Zuordnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="8f9c5-126">Dieser Fehler kann auch auftreten, wenn die Dataverse-Umgebung zurückgesetzt wurde, ohne die Verknüpfung zum dualen Schreiben aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="8f9c5-127">Jeder Benutzer mit Systemadministratorrolle in Finance and Operations-Apps und Dataverse kann die Umgebungen verbinden.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="8f9c5-128">Nur der Benutzer, der die duale Schreibverbindung eingerichtet hat, kann neue Tabellenzuordnungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="8f9c5-129">Nach dem Setup kann jeder Benutzer mit Systemadministratorrolle den Status überwachen und die Zuordnungen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="8f9c5-130">Fehler beim Beenden der Tabellenzuordnung</span><span class="sxs-lookup"><span data-stu-id="8f9c5-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="8f9c5-131">Möglicherweise wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, die Tabellenzuordnung zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="8f9c5-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="8f9c5-132">*\[verboten\], \[{„Status“: 403, „Quelle“:„“,„Nachricht“:„Fehler beim Token-Austausch: Benutzer darf nicht auf die Verbindung dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx“}\] zugreifen. Der Remote-Server hat einen Fehler zurückgegeben: (403) Verboten.*</span><span class="sxs-lookup"><span data-stu-id="8f9c5-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="8f9c5-133">Dieser Fehler tritt auf, wenn die verknüpfte Dataverse Umgebung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="8f9c5-134">Erstellen Sie ein Ticket für das Datenintegrationsteam, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="8f9c5-135">Fügen Sie die Netzwerkablaufverfolgung hinzu, damit das Datenintegrationsteam die Zuordnung als **wird nicht ausgeführt** im hinteren Ende markieren kann.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-a-table-mapping"></a><span data-ttu-id="8f9c5-136">Fehler beim Versuch, eine Tabellenzuordnung zu starten</span><span class="sxs-lookup"><span data-stu-id="8f9c5-136">Error while trying to start a table mapping</span></span>

<span data-ttu-id="8f9c5-137">Möglicherweise wird eine Fehlermeldung wie die folgende angezeigt, wenn Sie versuchen, den Status einer Zuordnung auf **Laufend** festzulegen:</span><span class="sxs-lookup"><span data-stu-id="8f9c5-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="8f9c5-138">*Die anfängliche Datensynchronisierung kann nicht abgeschlossen werden. Fehler: Dualer Schreibfehler – Plugin-Registrierung fehlgeschlagen: Suchmetadaten für duales Schreiben können nicht erstellt werden. Fehlerobjektreferenz nicht auf eine Instanz eines Objekts festgelegt.*</span><span class="sxs-lookup"><span data-stu-id="8f9c5-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="8f9c5-139">Die Behebung dieses Fehlers hängt von der Fehlerursache ab:</span><span class="sxs-lookup"><span data-stu-id="8f9c5-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="8f9c5-140">Wenn die Zuordnung abhängige Zuordnungen enthält, müssen Sie die abhängigen Zuordnungen dieser Tabellenzuordnung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="8f9c5-141">In der Zuordnung fehlen möglicherweise Quell- oder Zielspalten.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-141">The mapping might be missing source or destination columns.</span></span> <span data-ttu-id="8f9c5-142">Wenn eine Spalte in der Finance and Operations-App fehlt, dann befolgen Sie die Schritte im Abschnitt [Fehlende Tabellenspalten treten in Zuordnungen auf](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span><span class="sxs-lookup"><span data-stu-id="8f9c5-142">If a column in the Finance and Operations app is missing, then follow the steps in the section [Missing table columns issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span></span> <span data-ttu-id="8f9c5-143">Wenn eine Spalte in Dataverse fehlt, klicken Sie in der Zuordnung auf die Schaltfläche **Tabellen aktualisieren**, damit die Spalten automatisch wieder in die Zuordnung eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8f9c5-143">If a column in Dataverse is missing, then click **Refresh tables** button on the mapping so that the columns are automatically populated back into the mapping.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]