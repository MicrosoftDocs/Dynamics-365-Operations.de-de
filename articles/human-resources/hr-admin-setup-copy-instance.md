---
title: Instanz kopieren
description: Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6cb8050980b9b54480d09a59379430cd229ff141
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801094"
---
# <a name="copy-an-instance"></a><span data-ttu-id="08b2d-103">Instanz kopieren</span><span class="sxs-lookup"><span data-stu-id="08b2d-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="08b2d-104">Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="08b2d-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="08b2d-105">Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="08b2d-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="08b2d-106">Beachten Sie beim Kopieren einer Instanz die folgenden Hinweise:</span><span class="sxs-lookup"><span data-stu-id="08b2d-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="08b2d-107">Die Human Resources-Instanz, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.</span><span class="sxs-lookup"><span data-stu-id="08b2d-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="08b2d-108">Die Umgebungen, aus denen Sie kopieren, müssen sich in derselben Region befinden.</span><span class="sxs-lookup"><span data-stu-id="08b2d-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="08b2d-109">Sie können nicht über Regionen hinweg kopieren.</span><span class="sxs-lookup"><span data-stu-id="08b2d-109">You can't copy across regions.</span></span>

- <span data-ttu-id="08b2d-110">Sie müssen ein Administrator in der Zielumgebung sein, damit Sie sich nach dem Kopieren der Instanz anmelden können.</span><span class="sxs-lookup"><span data-stu-id="08b2d-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="08b2d-111">Wenn Sie die Human Resources-Datenbank kopieren, kopieren Sie nicht die Elemente (Apps oder Daten), die in einer Microsoft Power Apps-Umgebung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="08b2d-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="08b2d-112">Informationen zum Kopieren von Elementen in einer Power Apps-Umgebung finden Sie in [Umgebung kopieren](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="08b2d-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="08b2d-113">Die Power Apps-Umgebung, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.</span><span class="sxs-lookup"><span data-stu-id="08b2d-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="08b2d-114">Sie müssen ein globaler Mandantenadministrator sein, um eine Power Apps-Produktionsumgebung zu einer Sandkastenumgebung umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="08b2d-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="08b2d-115">Weitere Informationen zum Ändern einer Power Apps-Umgebung finden Sie in [Instanz wechseln](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="08b2d-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="08b2d-116">Wenn Sie eine Instanz in Ihre Sandbox-Umgebung kopieren und Ihre Sandbox-Umgebung in Dataverse integrieren möchten, müssen Sie benutzerdefinierte Felder erneut auf Dataverse-Tabellen anwenden.</span><span class="sxs-lookup"><span data-stu-id="08b2d-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="08b2d-117">Sehen Sie [Anwenden benutzerdefinierter Felder auf Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span><span class="sxs-lookup"><span data-stu-id="08b2d-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="08b2d-118">Auswirkungen des Kopierens einer Human Resources-Datenbank</span><span class="sxs-lookup"><span data-stu-id="08b2d-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="08b2d-119">Die folgenden Ereignisse treten auf, wenn Sie eine Human Resources-Datenbank kopieren:</span><span class="sxs-lookup"><span data-stu-id="08b2d-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="08b2d-120">Der Kopiervorgang löscht die vorhandene Datenbank in der Zielumgebung.</span><span class="sxs-lookup"><span data-stu-id="08b2d-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="08b2d-121">Nach Abschluss des Kopiervorgangs können Sie die vorhandene Datenbank nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="08b2d-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="08b2d-122">Die Zielumgebung ist erst verfügbar, wenn der Kopiervorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="08b2d-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="08b2d-123">Dokumente im Microsoft Azure Blob-Speicher werden nicht von einer Umgebung in eine andere kopiert.</span><span class="sxs-lookup"><span data-stu-id="08b2d-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="08b2d-124">Als Ergebnis werden angehängte Dokumente und Vorlagen nicht kopiert und verbleiben in der Quellumgebung.</span><span class="sxs-lookup"><span data-stu-id="08b2d-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="08b2d-125">Bis auf den Administrator und andere interne Servicebenutzer werden alle Benutzer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="08b2d-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="08b2d-126">Der Administrator kann Daten löschen oder verschleiern, bevor andere Benutzer wieder Zugriff auf das System erhalten.</span><span class="sxs-lookup"><span data-stu-id="08b2d-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="08b2d-127">Der Administrator muss die erforderlichen Konfigurationsänderungen vornehmen, z. B. das erneute Verbinden von Integrationsendpunkten mit bestimmten Diensten oder URLs.</span><span class="sxs-lookup"><span data-stu-id="08b2d-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="08b2d-128">Human Resources-Datenbank kopieren</span><span class="sxs-lookup"><span data-stu-id="08b2d-128">Copy the Human Resources database</span></span>

<span data-ttu-id="08b2d-129">Um diese Aufgabe abzuschließen, kopieren Sie zuerst eine Instanz und melden sich dann im Microsoft Power Platform Admin Center an, um Ihre Power Apps-Umgebung zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="08b2d-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="08b2d-130">Wenn Sie eine Instanz kopieren, wird die Datenbank in der Zielinstanz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="08b2d-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="08b2d-131">Die Zielinstanz ist während dieses Vorgangs nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08b2d-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="08b2d-132">Melden Sie sich bei LCS an und wählen Sie das LCS-Projekt aus, das die zu kopierende Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="08b2d-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="08b2d-133">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="08b2d-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="08b2d-134">Wählen Sie die zu kopierende Instanz aus und wählen Sie dann **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="08b2d-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="08b2d-135">Wählen Sie im Aufgabenbereich **Instanz kopieren** die zu überschreibende Instanz und anschließend **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="08b2d-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="08b2d-136">Warten Sie, bis der Wert des Felds **Kopierstatus** zu **Abgeschlossen** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="08b2d-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="08b2d-137">Zu überschreibende Instanz auswählen</span><span class="sxs-lookup"><span data-stu-id="08b2d-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="08b2d-138">Wählen Sie **Power Platform** aus und melden Sie sich im Microsoft Power Platform Admin Center an.</span><span class="sxs-lookup"><span data-stu-id="08b2d-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="08b2d-139">Power Platform auswählen</span><span class="sxs-lookup"><span data-stu-id="08b2d-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="08b2d-140">Wählen Sie die zu kopierende Power Apps-Umgebung aus und wählen Sie dann **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="08b2d-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="08b2d-141">Wenn der Kopiervorgang abgeschlossen ist, melden Sie sich bei der Zielinstanz an und aktivieren Sie die Dataverse-Integration.</span><span class="sxs-lookup"><span data-stu-id="08b2d-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="08b2d-142">Weitere Informationen und Anleitungen finden Sie unter [Dataverse-Integration konfigurieren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="08b2d-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="08b2d-143">Datenelemente und ‑status</span><span class="sxs-lookup"><span data-stu-id="08b2d-143">Data elements and statuses</span></span>

<span data-ttu-id="08b2d-144">Die folgenden Datenelemente werden beim Kopieren einer Human Resources-Instanz nicht kopiert:</span><span class="sxs-lookup"><span data-stu-id="08b2d-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="08b2d-145">E-Mail-Adressen in der Tabelle **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="08b2d-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="08b2d-146">Die Batchauftrag-Historie in den Tabellen **BatchJobHistory**, **BatchHistory** und **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="08b2d-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="08b2d-147">Das SMTP-Kennwort (Simple Mail Transfer Protocol) in der Tabelle **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="08b2d-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="08b2d-148">Der SMTP-Relay-Server in der Tabelle **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="08b2d-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="08b2d-149">Druckverwaltungseinstellungen in den Tabellen **PrintMgmtSettings** und **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="08b2d-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="08b2d-150">Umgebungsspezifische Datensätze in den Tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** und **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="08b2d-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="08b2d-151">Dokumentanhänge in der DocuValue-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="08b2d-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="08b2d-152">Diese Anhänge enthalten alle Microsoft Office-Vorlagen, die in der Quellumgebung überschrieben wurden</span><span class="sxs-lookup"><span data-stu-id="08b2d-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="08b2d-153">Die Verbindungszeichenfolge in der Tabelle **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="08b2d-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="08b2d-154">Einige dieser Elemente werden nicht kopiert, da sie umgebungsspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="08b2d-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="08b2d-155">Dazu zählen beispielsweise die Datensätze **BatchServerConfig** und **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="08b2d-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="08b2d-156">Andere Elemente werden aufgrund des Umfangs der Support-Tickets nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="08b2d-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="08b2d-157">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="08b2d-157">For example:</span></span>

- <span data-ttu-id="08b2d-158">Möglicherweise werden doppelte E-Mails gesendet, da SMTP in der Umgebung für Benutzerakzeptanztests (Sandkasten) weiterhin aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="08b2d-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="08b2d-159">Möglicherweise werden ungültige Integrationsnachrichten gesendet, da Batchaufträge noch aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="08b2d-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="08b2d-160">Benutzer werden möglicherweise aktiviert, bevor Administratoren Bereinigungsaktionen nach der Aktualisierung ausführen können.</span><span class="sxs-lookup"><span data-stu-id="08b2d-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="08b2d-161">Außerdem ändern sich die folgenden Status beim Kopieren einer Instanz:</span><span class="sxs-lookup"><span data-stu-id="08b2d-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="08b2d-162">Alle Benutzer außer Administratoren werden auf **Deaktiviert** gestellt.</span><span class="sxs-lookup"><span data-stu-id="08b2d-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="08b2d-163">Alle Batchaufträge außer einigen Systemaufträgen werden auf **Zurückhalten** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="08b2d-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="08b2d-164">Umgebungsadministrator</span><span class="sxs-lookup"><span data-stu-id="08b2d-164">Environment admin</span></span>

<span data-ttu-id="08b2d-165">Alle Benutzer in der Ziel-Sandkastenumgebung, einschließlich Administratoren, werden durch die Benutzer der Quellumgebung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="08b2d-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="08b2d-166">Stellen Sie vor dem Kopieren einer Instanz sicher, dass Sie ein Administrator in der Quellumgebung sind.</span><span class="sxs-lookup"><span data-stu-id="08b2d-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="08b2d-167">Andernfalls können Sie sich nach Abschluss des Kopiervorgangs nicht bei der Ziel-Sandkastenumgebung anmelden.</span><span class="sxs-lookup"><span data-stu-id="08b2d-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="08b2d-168">Alle Nicht-Administrator-Benutzer in der Ziel-Sandkastenumgebung sind deaktiviert, um unerwünschte Anmeldungen in der Sandkastenumgebung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="08b2d-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="08b2d-169">Administratoren können Benutzer bei Bedarf erneut aktivieren.</span><span class="sxs-lookup"><span data-stu-id="08b2d-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="08b2d-170">Benutzerdefinierte Felder auf Dataverse anwenden</span><span class="sxs-lookup"><span data-stu-id="08b2d-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="08b2d-171">Wenn Sie eine Instanz in Ihre Sandbox-Umgebung kopieren und Ihre Sandbox-Umgebung in Dataverse integrieren möchten, müssen Sie benutzerdefinierte Felder erneut auf Dataverse-Tabellen anwenden.</span><span class="sxs-lookup"><span data-stu-id="08b2d-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="08b2d-172">Für jedes benutzerdefinierte Feld, das in Dataverse-Tabellen angezeigt wird, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="08b2d-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="08b2d-173">Gehen Sie zum benutzerdefinierten Feld und wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="08b2d-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="08b2d-174">Deaktivieren Sie das Feld **Aktiviert** für jede cdm_\*-Entität, für die das benutzerdefinierte Feld aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="08b2d-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="08b2d-175">Wählen Sie **Änderungen übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="08b2d-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="08b2d-176">Wählen Sie erneut **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="08b2d-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="08b2d-177">Wählen Sie das Feld **Aktiviert** für jede cdm_\*-Entität aus, für die das benutzerdefinierte Feld aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="08b2d-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="08b2d-178">Wählen Sie erneut **Änderungen übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="08b2d-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="08b2d-179">Beim Aufheben der Auswahl, dem Anwenden von Änderungen, dem erneuten Auswählen und erneuten Anwenden von Änderungen wird das Schema zur Aktualisierung in Dataverse aufgefordert, die benutzerdefinierten Felder einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="08b2d-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="08b2d-180">Weitere Informationen über benutzerdefinierte Felder finden Sie unter [Erstellen und Arbeiten mit benutzerdefinierten Feldern](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="08b2d-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="08b2d-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08b2d-181">See also</span></span>

[<span data-ttu-id="08b2d-182">Personalverwaltung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="08b2d-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="08b2d-183">Eine Instanz entfernen</span><span class="sxs-lookup"><span data-stu-id="08b2d-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="08b2d-184">Aktualisierungsprozess</span><span class="sxs-lookup"><span data-stu-id="08b2d-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]