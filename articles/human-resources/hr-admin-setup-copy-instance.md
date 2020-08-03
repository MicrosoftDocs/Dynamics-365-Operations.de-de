---
title: Instanz kopieren
description: Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b14baf49517f5d606038af20366944788b22eba2
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554324"
---
# <a name="copy-an-instance"></a><span data-ttu-id="9a829-103">Instanz kopieren</span><span class="sxs-lookup"><span data-stu-id="9a829-103">Copy an instance</span></span>

<span data-ttu-id="9a829-104">Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="9a829-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="9a829-105">Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="9a829-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="9a829-106">Um eine Instanz zu kopieren, müssen Sie Folgendes sicherstellen:</span><span class="sxs-lookup"><span data-stu-id="9a829-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="9a829-107">Die Human Resources-Instanz, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.</span><span class="sxs-lookup"><span data-stu-id="9a829-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="9a829-108">Die Umgebungen, aus denen Sie kopieren, müssen sich in derselben Region befinden.</span><span class="sxs-lookup"><span data-stu-id="9a829-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="9a829-109">Sie können nicht über Regionen hinweg kopieren.</span><span class="sxs-lookup"><span data-stu-id="9a829-109">You can't copy across regions.</span></span>

- <span data-ttu-id="9a829-110">Sie müssen ein Administrator in der Zielumgebung sein, damit Sie sich nach dem Kopieren der Instanz anmelden können.</span><span class="sxs-lookup"><span data-stu-id="9a829-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="9a829-111">Wenn Sie die Human Resources-Datenbank kopieren, kopieren Sie nicht die Elemente (Apps oder Daten), die in einer Microsoft PowerApps-Umgebung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="9a829-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="9a829-112">Informationen zum Kopieren von Elementen in einer PowerApps-Umgebung finden Sie in [Umgebung kopieren](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="9a829-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="9a829-113">Die PowerApps-Umgebung, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.</span><span class="sxs-lookup"><span data-stu-id="9a829-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="9a829-114">Sie müssen ein globaler Mandantenadministrator sein, um eine PowerApps-Produktionsumgebung zu einer Sandkastenumgebung umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="9a829-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="9a829-115">Weitere Informationen zum Ändern einer PowerApps-Umgebung finden Sie in [Instanz wechseln](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="9a829-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="9a829-116">Auswirkungen des Kopierens einer Human Resources-Datenbank</span><span class="sxs-lookup"><span data-stu-id="9a829-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="9a829-117">Die folgenden Ereignisse treten auf, wenn Sie eine Human Resources-Datenbank kopieren:</span><span class="sxs-lookup"><span data-stu-id="9a829-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="9a829-118">Der Kopiervorgang löscht die vorhandene Datenbank in der Zielumgebung.</span><span class="sxs-lookup"><span data-stu-id="9a829-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="9a829-119">Nach Abschluss des Kopiervorgangs können Sie die vorhandene Datenbank nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="9a829-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="9a829-120">Die Zielumgebung ist erst verfügbar, wenn der Kopiervorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9a829-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="9a829-121">Dokumente im Microsoft Azure Blob-Speicher werden nicht von einer Umgebung in eine andere kopiert.</span><span class="sxs-lookup"><span data-stu-id="9a829-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="9a829-122">Daher werden angehängte Dokumente und Vorlagen nicht kopiert und verbleiben in der Quellumgebung.</span><span class="sxs-lookup"><span data-stu-id="9a829-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="9a829-123">Bis auf den Administrator und andere interne Servicebenutzer werden alle Benutzer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9a829-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="9a829-124">Dadurch kann der Administrator Daten löschen oder verschleiern, bevor andere Benutzer wieder Zugriff auf das System erhalten.</span><span class="sxs-lookup"><span data-stu-id="9a829-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="9a829-125">Der Administrator muss die erforderlichen Konfigurationsänderungen vornehmen, z. B. das erneute Verbinden von Integrationsendpunkten mit bestimmten Diensten oder URLs.</span><span class="sxs-lookup"><span data-stu-id="9a829-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="9a829-126">Human Resources-Datenbank kopieren</span><span class="sxs-lookup"><span data-stu-id="9a829-126">Copy the Human Resources database</span></span>

<span data-ttu-id="9a829-127">Um diese Aufgabe abzuschließen, kopieren Sie zuerst eine Instanz und melden sich dann im Microsoft Power Platform Admin Center an, um Ihre PowerApps-Umgebung zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9a829-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="9a829-128">Wenn Sie eine Instanz kopieren, wird die Datenbank in der Zielinstanz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9a829-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="9a829-129">Die Zielinstanz ist während dieses Vorgangs nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a829-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="9a829-130">Melden Sie sich bei LCS an und wählen Sie das LCS-Projekt aus, das die zu kopierende Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="9a829-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="9a829-131">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="9a829-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="9a829-132">Wählen Sie die zu kopierende Instanz aus und wählen Sie dann **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="9a829-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="9a829-133">Wählen Sie im Aufgabenbereich **Instanz kopieren** die zu überschreibende Instanz und anschließend **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9a829-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="9a829-134">Warten Sie, bis der Wert des Felds **Kopierstatus** zu **Abgeschlossen** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9a829-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="9a829-135">Zu überschreibende Instanz auswählen</span><span class="sxs-lookup"><span data-stu-id="9a829-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="9a829-136">Wählen Sie **Power Platform** aus und melden Sie sich im Microsoft Power Platform Admin Center an.</span><span class="sxs-lookup"><span data-stu-id="9a829-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="9a829-137">Power Platform auswählen</span><span class="sxs-lookup"><span data-stu-id="9a829-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="9a829-138">Wählen Sie die zu kopierende PowerApps-Umgebung aus und wählen Sie dann **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="9a829-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="9a829-139">Wenn der Kopiervorgang abgeschlossen ist, melden Sie sich bei der Zielinstanz an und aktivieren Sie die Common Data Service-Integration.</span><span class="sxs-lookup"><span data-stu-id="9a829-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="9a829-140">Weitere Informationen und Anleitungen finden Sie unter [Common Data Service-Integration konfigurieren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="9a829-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="9a829-141">Datenelemente und ‑status</span><span class="sxs-lookup"><span data-stu-id="9a829-141">Data elements and statuses</span></span>

<span data-ttu-id="9a829-142">Die folgenden Datenelemente werden beim Kopieren einer Human Resources-Instanz nicht kopiert:</span><span class="sxs-lookup"><span data-stu-id="9a829-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="9a829-143">E-Mail-Adressen in der Tabelle **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="9a829-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="9a829-144">Die Batchauftrag-Historie in den Tabellen **BatchJobHistory**, **BatchHistory** und **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="9a829-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="9a829-145">Das SMTP-Kennwort (Simple Mail Transfer Protocol) in der Tabelle **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="9a829-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="9a829-146">Der SMTP-Relay-Server in der Tabelle **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="9a829-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="9a829-147">Druckverwaltungseinstellungen in den Tabellen **PrintMgmtSettings** und **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="9a829-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="9a829-148">Umgebungsspezifische Datensätze in den Tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** und **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="9a829-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="9a829-149">Dokumentanhänge in der DocuValue-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9a829-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="9a829-150">Diese Anhänge enthalten alle Microsoft Office-Vorlagen, die in der Quellumgebung überschrieben wurden</span><span class="sxs-lookup"><span data-stu-id="9a829-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="9a829-151">Die Verbindungszeichenfolge in der Tabelle **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="9a829-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="9a829-152">Einige dieser Elemente werden nicht kopiert, da sie umgebungsspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="9a829-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="9a829-153">Dazu zählen beispielsweise die Datensätze **BatchServerConfig** und **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="9a829-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="9a829-154">Andere Elemente werden aufgrund des Umfangs der Support-Tickets nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="9a829-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="9a829-155">Beispielsweise können doppelte E-Mails gesendet werden, weil SMTP in der Benutzerakzeptanztest-(Sandkasten-)Umgebung weiterhin aktiviert ist, ungültige Integrationsnachrichten werden möglicherweise gesendet, weil Batchaufträge weiterhin aktiviert sind und Benutzer werden möglicherweise aktiviert, bevor Administratoren Bereinigungsaktionen nach dem Aktualisieren ausführen können.</span><span class="sxs-lookup"><span data-stu-id="9a829-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="9a829-156">Darüber hinaus ändern sich die folgenden Status beim Kopieren einer Instanz:</span><span class="sxs-lookup"><span data-stu-id="9a829-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="9a829-157">Alle Benutzer außer Administratoren werden auf **Deaktiviert** gestellt.</span><span class="sxs-lookup"><span data-stu-id="9a829-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="9a829-158">Alle Batchaufträge außer einigen Systemaufträgen werden auf **Zurückhalten** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="9a829-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="9a829-159">Umgebungsadministrator</span><span class="sxs-lookup"><span data-stu-id="9a829-159">Environment admin</span></span>

<span data-ttu-id="9a829-160">Alle Benutzer in der Ziel-Sandkastenumgebung, einschließlich Administratoren, werden durch die Benutzer der Quellumgebung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9a829-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="9a829-161">Stellen Sie vor dem Kopieren einer Instanz sicher, dass Sie ein Administrator in der Quellumgebung sind.</span><span class="sxs-lookup"><span data-stu-id="9a829-161">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="9a829-162">Andernfalls können Sie sich nach Abschluss des Kopiervorgangs nicht mehr bei der Ziel-Sandkastenumgebung anmelden.</span><span class="sxs-lookup"><span data-stu-id="9a829-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="9a829-163">Alle Nicht-Administrator-Benutzer in der Ziel-Sandkastenumgebung sind deaktiviert, um unerwünschte Anmeldungen in der Sandkastenumgebung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="9a829-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="9a829-164">Administratoren können Benutzer bei Bedarf erneut aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9a829-164">Administrators can reenable users if needed.</span></span>
