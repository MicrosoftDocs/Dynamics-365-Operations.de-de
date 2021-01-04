---
title: Probleme bezüglich Aktualisierungen von Finance and Operations Apps beheben
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c76b35ed3af766f42484a118a4a0407d969b5240
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683598"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="46509-103">Probleme bezüglich Aktualisierungen von Finance and Operations Apps beheben</span><span class="sxs-lookup"><span data-stu-id="46509-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="46509-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="46509-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="46509-105">Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="46509-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46509-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="46509-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="46509-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="46509-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="46509-108">Datenbanksynchronisierungsfehler</span><span class="sxs-lookup"><span data-stu-id="46509-108">Database synchronization errors</span></span>

<span data-ttu-id="46509-109">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="46509-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="46509-110">Möglicherweise erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt, wenn Sie versuchen, die **DualWriteProjectConfiguration** Entität zu verwenden, um eine Finance and Operations App auf Plattform Update 30 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="46509-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="46509-111">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="46509-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="46509-112">Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.</span><span class="sxs-lookup"><span data-stu-id="46509-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="46509-113">Öffnen von Visual Studio als Administrator und öffnen Sie den Application Object Tree (AOT).</span><span class="sxs-lookup"><span data-stu-id="46509-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="46509-114">Suchen nach **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="46509-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="46509-115">Klicken Sie im AOT mit der rechten Maustaste auf **DualWriteProjectConfiguration** und wählen Sie **Zu neuem Projekt hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="46509-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="46509-116">Wählen Sie **OK**, um das neue Projekt zu erstellen, das Standardoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="46509-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="46509-117">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf **Projekteigenschaften** und setzen Sie **Datenbank beim Erstellen synchronisieren** auf **Wahr** fest.</span><span class="sxs-lookup"><span data-stu-id="46509-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="46509-118">Erstellen Sie das Projekt und bestätigen Sie, dass der Build erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="46509-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="46509-119">Auf dem **Dynamics 365** Menü wählen Sie **Datenbank synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="46509-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="46509-120">Wählen Sie **Synchronisieren**, um eine vollständige Datenbanksynchronisation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="46509-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="46509-121">Nachdem die vollständige Datenbanksynchronisierung erfolgreich war, führen Sie den Schritt zur Datenbanksynchronisierung erneut aus in Microsoft Dynamics Lifecycle Services (LCS) und verwenden Sie gegebenenfalls die manuellen Upgrade-Skripte, damit Sie mit dem Update fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="46509-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="46509-122">Fehlende Entitätsfelder treten auf Zuordnungen auf</span><span class="sxs-lookup"><span data-stu-id="46509-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="46509-123">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="46509-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="46509-124">Auf der Seite **Duales Schreiben** wird möglicherweise eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt:</span><span class="sxs-lookup"><span data-stu-id="46509-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="46509-125">*Fehlendes Quellfeld \<field name\> im Schema.*</span><span class="sxs-lookup"><span data-stu-id="46509-125">*Missing source field \<field name\> in the schema.*</span></span>

![Beispiel für die fehlende Quellfeldfehlermeldung](media/error_missing_field.png)

<span data-ttu-id="46509-127">Führen Sie die folgenden Schritte aus, um das Problem zu beheben und sicherzustellen, dass sich die Felder in der Entität befinden.</span><span class="sxs-lookup"><span data-stu-id="46509-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="46509-128">Melden Sie sich bei der virtuellen Maschine (VM) an für die Finance and Operations App.</span><span class="sxs-lookup"><span data-stu-id="46509-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="46509-129">Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Kachel **Framework-Parameter** aus und wählen Sie dann auf der Registerkarte **Tabelleneinstellungen** die Option **Entitätsliste aktualisieren** aus, um die Tabellen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="46509-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh entity list** to refresh the tables.</span></span>
3. <span data-ttu-id="46509-130">Wechseln Sie zu **Arbeitsbereiche \> Datenmanagement**, wählen Sie die Registerkarte **Datentabellen** aus und stellen Sie sicher, dass die Entität aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="46509-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="46509-131">Wenn die Entität nicht aufgeführt ist, melden Sie sich bei der VM für die Finance and Operations App an und stellen Sie sicher, dass die Entität verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="46509-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="46509-132">Öffnen Sie die Seite **Tabellenzuordnung** über die Seite **Duales Schreiben** in der Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="46509-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="46509-133">Wählen Sie **Entitätsliste aktualisieren** aus, um die Felder in den Tabellenzuordnungen automatisch auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="46509-133">Select **Refresh entity list** to automatically fill the fields in the table mappings.</span></span>

<span data-ttu-id="46509-134">Wenn das Problem immer noch nicht behoben ist, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="46509-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46509-135">Diese Schritte führen Sie durch den Vorgang des Löschens und anschließenden Hinzufügens einer Entität.</span><span class="sxs-lookup"><span data-stu-id="46509-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="46509-136">Befolgen Sie die Schritte genau, um Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="46509-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="46509-137">Gehen Sie in der Finance and Operations-App zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Datentabellen** aus.</span><span class="sxs-lookup"><span data-stu-id="46509-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="46509-138">Suchen Sie die Entität, der das Attribut fehlt.</span><span class="sxs-lookup"><span data-stu-id="46509-138">Find the entity that is missing the attribute.</span></span> <span data-ttu-id="46509-139">Klicken Sie in der Symbolleiste auf **Zielzuordnung ändern**.</span><span class="sxs-lookup"><span data-stu-id="46509-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="46509-140">Klicken Sie im Bereich **Abbildung auf Ziel** auf **Zuordnung generieren**.</span><span class="sxs-lookup"><span data-stu-id="46509-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="46509-141">Öffnen Sie die Seite **Tabellenzuordnung** über die Seite **Duales Schreiben** in der Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="46509-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="46509-142">Wenn das Attribut nicht automatisch in die Zuordnung eingefügt wird, fügen Sie es manuell hinzu, indem Sie auf **Attribut hinzufügen** und dann auf **Speichern** klicken.</span><span class="sxs-lookup"><span data-stu-id="46509-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="46509-143">Wählen Sie die Zuordnung aus, und klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="46509-143">Select the map and click **Run**.</span></span>
