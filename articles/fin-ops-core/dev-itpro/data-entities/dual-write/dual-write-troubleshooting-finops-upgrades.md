---
title: Probleme bei Aktualisierungen von Finance and Operations-Apps beheben
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.
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
ms.openlocfilehash: 97509ac662fad6181cbd60e5e0a44f674410acb9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754037"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="fd998-103">Probleme bei Aktualisierungen von Finance and Operations-Apps beheben</span><span class="sxs-lookup"><span data-stu-id="fd998-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="fd998-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fd998-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="fd998-105">Dieses Thema enthält speziell Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit dem Upgrade von Finance and Operations Apps zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="fd998-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd998-106">Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators.</span><span class="sxs-lookup"><span data-stu-id="fd998-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="fd998-107">Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fd998-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="fd998-108">Datenbanksynchronisierungsfehler</span><span class="sxs-lookup"><span data-stu-id="fd998-108">Database synchronization errors</span></span>

<span data-ttu-id="fd998-109">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="fd998-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="fd998-110">Möglicherweise erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt, wenn Sie versuchen, die Tabelle **DualWriteProjectConfiguration** zu verwenden, um eine Finance and Operations-App auf Plattform Update 30 zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fd998-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="fd998-111">Führen Sie folgende Schritte aus, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="fd998-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="fd998-112">Melden Sie sich bei der virtuellen Maschine (VM) für die Finance and Operations App an.</span><span class="sxs-lookup"><span data-stu-id="fd998-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="fd998-113">Öffnen von Visual Studio als Administrator und öffnen Sie den Application Object Tree (AOT).</span><span class="sxs-lookup"><span data-stu-id="fd998-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="fd998-114">Suchen nach **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="fd998-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="fd998-115">Klicken Sie im AOT mit der rechten Maustaste auf **DualWriteProjectConfiguration** und wählen Sie **Zu neuem Projekt hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fd998-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="fd998-116">Wählen Sie **OK**, um das neue Projekt zu erstellen, das Standardoptionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd998-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="fd998-117">Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf **Projekteigenschaften** und setzen Sie **Datenbank beim Erstellen synchronisieren** auf **Wahr** fest.</span><span class="sxs-lookup"><span data-stu-id="fd998-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="fd998-118">Erstellen Sie das Projekt und bestätigen Sie, dass der Build erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="fd998-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="fd998-119">Auf dem **Dynamics 365** Menü wählen Sie **Datenbank synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="fd998-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="fd998-120">Wählen Sie **Synchronisieren**, um eine vollständige Datenbanksynchronisation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="fd998-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="fd998-121">Nachdem die vollständige Datenbanksynchronisierung erfolgreich war, führen Sie den Schritt zur Datenbanksynchronisierung erneut aus in Microsoft Dynamics Lifecycle Services (LCS) und verwenden Sie gegebenenfalls die manuellen Upgrade-Skripte, damit Sie mit dem Update fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="fd998-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="fd998-122">Fehlende Tabellenspalten in Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="fd998-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="fd998-123">**Erforderliche Rolle zum Beheben der Fehler:** System Administrator</span><span class="sxs-lookup"><span data-stu-id="fd998-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="fd998-124">Auf der Seite **Duales Schreiben** wird möglicherweise eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt:</span><span class="sxs-lookup"><span data-stu-id="fd998-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="fd998-125">*Fehlendes Quellfeld \<field name\> im Schema.*</span><span class="sxs-lookup"><span data-stu-id="fd998-125">*Missing source field \<field name\> in the schema.*</span></span>

![Beispiel für die Fehlermeldung zu fehlenden Quellspalten](media/error_missing_field.png)

<span data-ttu-id="fd998-127">Führen Sie die folgenden Schritte aus, um das Problem zu beheben und sicherzustellen, dass sich die Spalten in der Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="fd998-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="fd998-128">Melden Sie sich bei der virtuellen Maschine (VM) an für die Finance and Operations App.</span><span class="sxs-lookup"><span data-stu-id="fd998-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="fd998-129">Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Kachel **Framework-Parameter** aus, und wählen Sie dann auf der Registerkarte **Tabelleneinstellungen** die Option **Tabellenliste aktualisieren** aus, um die Tabellen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fd998-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="fd998-130">Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**, wählen Sie die Registerkarte **Datentabellen** aus und stellen Sie sicher, dass die Tabelle aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="fd998-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="fd998-131">Wenn die Tabelle nicht aufgeführt ist, melden Sie sich bei der VM für die Finance and Operations-App an, und stellen Sie sicher, dass die Tabelle verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fd998-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="fd998-132">Öffnen Sie die Seite **Tabellenzuordnung** über die Seite **Duales Schreiben** in der Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="fd998-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="fd998-133">Wählen Sie **Tabellenliste aktualisieren** aus, um die Spalten in den Tabellenzuordnungen automatisch auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="fd998-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="fd998-134">Wenn das Problem immer noch nicht behoben ist, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="fd998-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd998-135">Diese Schritte führen Sie durch den Vorgang des Löschens und anschließenden Hinzufügens einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd998-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="fd998-136">Befolgen Sie die Schritte genau, um Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="fd998-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="fd998-137">Gehen Sie in der Finance and Operations-App zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Datentabellen** aus.</span><span class="sxs-lookup"><span data-stu-id="fd998-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="fd998-138">Suchen Sie die Tabelle, der das Attribut fehlt.</span><span class="sxs-lookup"><span data-stu-id="fd998-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="fd998-139">Klicken Sie in der Symbolleiste auf **Zielzuordnung ändern**.</span><span class="sxs-lookup"><span data-stu-id="fd998-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="fd998-140">Klicken Sie im Bereich **Abbildung auf Ziel** auf **Zuordnung generieren**.</span><span class="sxs-lookup"><span data-stu-id="fd998-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="fd998-141">Öffnen Sie die Seite **Tabellenzuordnung** über die Seite **Duales Schreiben** in der Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="fd998-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="fd998-142">Wenn das Attribut nicht automatisch in die Zuordnung eingefügt wird, fügen Sie es manuell hinzu, indem Sie auf **Attribut hinzufügen** und dann auf **Speichern** klicken.</span><span class="sxs-lookup"><span data-stu-id="fd998-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="fd998-143">Wählen Sie die Zuordnung aus, und klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="fd998-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]