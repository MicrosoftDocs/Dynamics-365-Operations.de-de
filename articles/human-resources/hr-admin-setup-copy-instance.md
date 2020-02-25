---
title: Instanz kopieren
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009100"
---
# <a name="copy-an-instance"></a><span data-ttu-id="7a6a1-102">Instanz kopieren</span><span class="sxs-lookup"><span data-stu-id="7a6a1-102">Copy an instance</span></span>

<span data-ttu-id="7a6a1-103">Sie können mit Microsoft Dynamics Lifecycle Services (LCS) eine Microsoft Dynamics 365 Human Resources-Datenbank in eine Sandkastenumgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="7a6a1-104">Wenn Sie eine andere Sandbox-Umgebung haben, können Sie die Datenbank auch aus dieser Umgebung in eine bestimmte Sandbox-Umgebung kopieren.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="7a6a1-105">Um eine Instanz zu kopieren, müssen Sie Folgendes sicherstellen:</span><span class="sxs-lookup"><span data-stu-id="7a6a1-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="7a6a1-106">Die Human Resources-Instanz, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="7a6a1-107">Die Umgebungen, aus denen Sie kopieren, müssen sich in derselben Region befinden.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="7a6a1-108">Sie können nicht über Regionen hinweg kopieren.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-108">You can't copy across regions.</span></span>

- <span data-ttu-id="7a6a1-109">Sie müssen ein Administrator in der Zielumgebung sein, damit Sie sich nach dem Kopieren der Instanz anmelden können.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="7a6a1-110">Wenn Sie die Human Resources-Datenbank kopieren, kopieren Sie nicht die Elemente (Apps oder Daten), die in einer Microsoft PowerApps-Umgebung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="7a6a1-111">Informationen zum Kopieren von Elementen in einer PowerApps-Umgebung finden Sie in [Umgebung kopieren](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="7a6a1-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="7a6a1-112">Die PowerApps-Umgebung, die Sie überschreiben möchten, muss eine Sandkastenumgebung sein.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="7a6a1-113">Sie müssen ein globaler Mandantenadministrator sein, um eine PowerApps-Produktionsumgebung zu einer Sandkastenumgebung umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="7a6a1-114">Weitere Informationen zum Ändern einer PowerApps-Umgebung finden Sie in [Instanz wechseln](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="7a6a1-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="7a6a1-115">Auswirkungen des Kopierens einer Human Resources-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7a6a1-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="7a6a1-116">Die folgenden Ereignisse treten auf, wenn Sie eine Human Resources-Datenbank kopieren:</span><span class="sxs-lookup"><span data-stu-id="7a6a1-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="7a6a1-117">Der Kopiervorgang löscht die vorhandene Datenbank in der Zielumgebung.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="7a6a1-118">Nach Abschluss des Kopiervorgangs können Sie die vorhandene Datenbank nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="7a6a1-119">Die Zielumgebung ist erst verfügbar, wenn der Kopiervorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="7a6a1-120">Dokumente im Microsoft Azure Blob-Speicher werden nicht von einer Umgebung in eine andere kopiert.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="7a6a1-121">Daher werden angehängte Dokumente und Vorlagen nicht kopiert und verbleiben in der Quellumgebung.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="7a6a1-122">Bis auf den Administrator und andere interne Servicebenutzer werden alle Benutzer deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="7a6a1-123">Dadurch kann der Administrator Daten löschen oder verschleiern, bevor andere Benutzer wieder Zugriff auf das System erhalten.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="7a6a1-124">Der Administrator muss die erforderlichen Konfigurationsänderungen vornehmen, z. B. das erneute Verbinden von Integrationsendpunkten mit bestimmten Diensten oder URLs.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="7a6a1-125">Human Resources-Datenbank kopieren</span><span class="sxs-lookup"><span data-stu-id="7a6a1-125">Copy the Human Resources database</span></span>

<span data-ttu-id="7a6a1-126">Um diese Aufgabe abzuschließen, kopieren Sie zuerst eine Instanz und melden sich dann im Microsoft Power Platform Admin Center an, um Ihre PowerApps-Umgebung zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="7a6a1-127">Wenn Sie eine Instanz kopieren, wird die Datenbank in der Zielinstanz gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="7a6a1-128">Die Zielinstanz ist während dieses Vorgangs nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="7a6a1-129">Melden Sie sich bei LCS an und wählen Sie das LCS-Projekt aus, das die zu kopierende Instanz enthält.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="7a6a1-130">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="7a6a1-131">Wählen Sie die zu kopierende Instanz aus und wählen Sie dann **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="7a6a1-132">Wählen Sie im Aufgabenbereich **Instanz kopieren** die zu überschreibende Instanz und anschließend **Kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="7a6a1-133">Warten Sie, bis der Wert des Felds **Kopierstatus** zu **Abgeschlossen** aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="7a6a1-134">Zu überschreibende Instanz auswählen</span><span class="sxs-lookup"><span data-stu-id="7a6a1-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="7a6a1-135">Wählen Sie **Power Platform** aus und melden Sie sich im Microsoft Power Platform Admin Center an.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="7a6a1-136">Power Platform auswählen</span><span class="sxs-lookup"><span data-stu-id="7a6a1-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="7a6a1-137">Wählen Sie die zu kopierende PowerApps-Umgebung aus und wählen Sie dann **Kopieren**.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="7a6a1-138">Wenn der Kopiervorgang abgeschlossen ist, melden Sie sich bei der Zielinstanz an und aktivieren Sie die Common Data Service-Integration.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="7a6a1-139">Weitere Informationen und Anleitungen finden Sie unter [Common Data Service-Integration konfigurieren](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="7a6a1-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="7a6a1-140">Datenelemente und ‑status</span><span class="sxs-lookup"><span data-stu-id="7a6a1-140">Data elements and statuses</span></span>

<span data-ttu-id="7a6a1-141">Die folgenden Datenelemente werden beim Kopieren einer Human Resources-Instanz nicht kopiert:</span><span class="sxs-lookup"><span data-stu-id="7a6a1-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="7a6a1-142">E-Mail-Adressen in der Tabelle **LogisticsElectronicAddress**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="7a6a1-143">Die Batchauftrag-Historie in den Tabellen **BatchJobHistory**, **BatchHistory** und **BatchConstraintHistory**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="7a6a1-144">Das SMTP-Kennwort (Simple Mail Transfer Protocol) in der Tabelle **SysEmailSMTPPassword**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="7a6a1-145">Der SMTP-Relay-Server in der Tabelle **SysEmailParameters**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="7a6a1-146">Druckverwaltungseinstellungen in den Tabellen **PrintMgmtSettings** und **PrintMgmtDocInstance**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="7a6a1-147">Umgebungsspezifische Datensätze in den Tabellen **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** und **BatchServerGroup**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="7a6a1-148">Dokumentanhänge in der DocuValue-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="7a6a1-149">Diese Anhänge enthalten alle Microsoft Office-Vorlagen, die in der Quellumgebung überschrieben wurden</span><span class="sxs-lookup"><span data-stu-id="7a6a1-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="7a6a1-150">Die Verbindungszeichenfolge in der Tabelle **PersonnelIntegrationConfiguration**</span><span class="sxs-lookup"><span data-stu-id="7a6a1-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="7a6a1-151">Einige dieser Elemente werden nicht kopiert, da sie umgebungsspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="7a6a1-152">Dazu zählen beispielsweise die Datensätze **BatchServerConfig** und **SysCorpNetPrinters**.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="7a6a1-153">Andere Elemente werden aufgrund des Umfangs der Support-Tickets nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="7a6a1-154">Beispielsweise können doppelte E-Mails gesendet werden, weil SMTP in der Benutzerakzeptanztest-(Sandkasten-)Umgebung weiterhin aktiviert ist, ungültige Integrationsnachrichten werden möglicherweise gesendet, weil Batchaufträge weiterhin aktiviert sind und Benutzer werden möglicherweise aktiviert, bevor Administratoren Bereinigungsaktionen nach dem Aktualisieren ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="7a6a1-155">Darüber hinaus ändern sich die folgenden Status beim Kopieren einer Instanz:</span><span class="sxs-lookup"><span data-stu-id="7a6a1-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="7a6a1-156">Alle Benutzer außer Administratoren werden auf **Deaktiviert** gestellt.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="7a6a1-157">Alle Batchaufträge außer einigen Systemaufträgen werden auf **Zurückhalten** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="7a6a1-158">Umgebungsadministrator</span><span class="sxs-lookup"><span data-stu-id="7a6a1-158">Environment admin</span></span>

<span data-ttu-id="7a6a1-159">Alle Benutzer in der Ziel-Sandkastenumgebung, einschließlich Administratoren, werden durch die Benutzer der Quellumgebung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="7a6a1-160">Stellen Sie vor dem Kopieren einer Instanz sicher, dass Sie ein Administrator in der Zielumgebung sind.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="7a6a1-161">Andernfalls können Sie sich nach Abschluss des Kopiervorgangs nicht mehr bei der Ziel-Sandkastenumgebung anmelden.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="7a6a1-162">Alle Nicht-Administrator-Benutzer in der Ziel-Sandkastenumgebung sind deaktiviert, um unerwünschte Anmeldungen in der Sandkastenumgebung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="7a6a1-163">Administratoren können Benutzer bei Bedarf erneut aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a6a1-163">Administrators can reenable users if needed.</span></span>
