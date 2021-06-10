---
title: Auf das Partei- und globale Adressbuchmodell aktualisieren
description: In diesem Thema wird beschrieben, wie Sie Daten aus dualem Schreiben auf das Partei- und das globale Adressbuchmodell aktualisieren.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112672"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="c6f34-103">Auf das Partei- und globale Adressbuchmodell aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c6f34-104">Die [Microsoft Azure Data Factory-Vorlage](https://aka.ms/dual-write-gab-adf) hilft Ihnen beim Aktualisieren vorhandener **Konto-**, **Kontakt**- und **Kreditor**-Tabellendaten in dualem Schreiben in das Partei- und das globale Adressbuchmodell.</span><span class="sxs-lookup"><span data-stu-id="c6f34-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="c6f34-105">Die Vorlage stimmt die Daten sowohl von Finance and Operations Apps als auch von Customer Engagement Anwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="c6f34-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="c6f34-106">Am Ende des Prozesses werden die Felder **Partei** und **Kontakt** für **Partei**-Datensätze erstellt und mit **Konto**-, **Kontakt**- und **Kreditor**-Datensätzen in Anwendungen zur Kundenbindung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="c6f34-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="c6f34-107">Eine .csv-Datei (`FONewParty.csv`) wird generiert, um einen neuen **Partei**-Datensatz in der Finance and Operations App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="c6f34-108">Dieses Thema enthält Anweisungen zur Verwendung der Data Factory-Vorlage und zum Aktualisieren Ihrer Daten.</span><span class="sxs-lookup"><span data-stu-id="c6f34-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="c6f34-109">Wenn Sie keine Anpassungen vorgenommen haben, können Sie die Vorlage unverändert verwenden.</span><span class="sxs-lookup"><span data-stu-id="c6f34-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="c6f34-110">Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage anhand der folgenden Anweisungen ändern.</span><span class="sxs-lookup"><span data-stu-id="c6f34-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="c6f34-111">Die Vorlage hilft nur, die **Partei**-Daten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c6f34-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="c6f34-112">Ein zukünftiger Release wird postalische und elektronische Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6f34-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c6f34-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c6f34-113">Prerequisites</span></span>

<span data-ttu-id="c6f34-114">Die folgenden Voraussetzungen sind erforderlich, um ein Upgrade auf das Partei- und das globale Adressbuchmodell durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="c6f34-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="c6f34-115">Azure-Abonnement</span><span class="sxs-lookup"><span data-stu-id="c6f34-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="c6f34-116">Zugriff auf die Vorlage</span><span class="sxs-lookup"><span data-stu-id="c6f34-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="c6f34-117">Sie müssen ein bestehender Kunde für duales Schreiben sein.</span><span class="sxs-lookup"><span data-stu-id="c6f34-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="c6f34-118">Vorbereitung auf die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="c6f34-118">Prepare for the upgrade</span></span>
<span data-ttu-id="c6f34-119">Die folgenden Aktivitäten sind erforderlich, um das Upgrade vorzubereiten:</span><span class="sxs-lookup"><span data-stu-id="c6f34-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="c6f34-120">**Vollständig synchronisiert**: Beide Umgebungen sind vollständig im Hinblick auf **Konto (Kunde)**, **Kontakt** und **Kreditor** synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c6f34-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="c6f34-121">**Integrationsschlüssel**: Die Tabellen **Konto (Kunde)**, **Kontakt** und **Kreditor** in Apps zur Kundenbindung verwenden die sofort einsatzbereiten Integrationsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c6f34-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="c6f34-122">Wenn Sie die Integrationsschlüssel angepasst haben, müssen Sie die Vorlage anpassen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="c6f34-123">**Parteinummer**: Alle **Konto (Kunde)**-, **Kontakt**- und **Kreditor**-Datensätze, die aktualisiert werden, haben eine **Partei**-Nummer.</span><span class="sxs-lookup"><span data-stu-id="c6f34-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="c6f34-124">Aufzeichnungen ohne **Partei**-Nummer werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c6f34-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="c6f34-125">Wenn Sie diese Datensätze aktualisieren möchten, fügen Sie eine **Partei**-Nummer hinzu, bevor Sie den Aktualisierungsprozess starten.</span><span class="sxs-lookup"><span data-stu-id="c6f34-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="c6f34-126">**Systemausfall**: Während des Aktualisierungsprozesses müssen Sie sowohl die Finance and Operations- als auch die Kundenbindungsumgebung offline nehmen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="c6f34-127">**Momentaufnahme**: Machen Sie sowohl von der Finance and Operations App als auch der Customer Engagement App eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="c6f34-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="c6f34-128">Verwenden Sie die Momentaufnahmen, um bei Bedarf den vorherigen Status wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="c6f34-129">Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c6f34-129">Deployment</span></span>

1. <span data-ttu-id="c6f34-130">Laden Sie die Vorlage von [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) herunter.</span><span class="sxs-lookup"><span data-stu-id="c6f34-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="c6f34-131">Melden Sie sich auf [Microsoft Azure](https://portal.azure.com/) an.</span><span class="sxs-lookup"><span data-stu-id="c6f34-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="c6f34-132">Erstellen Sie eine [Ressourcengruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="c6f34-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="c6f34-133">Erstellen Sie ein [Speicherkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) in der von Ihnen erstellten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c6f34-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="c6f34-134">Erstellen Sie eine [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) über der von Ihnen erstellten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c6f34-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="c6f34-135">Öffnen Sie die Data Factory und wählen Sie die Kachel **Erstellen und überwachen** aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="c6f34-136">Wählen Sie in der Registerkarte **Verwalten** die **ARM-Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="c6f34-137">Wählen Sie **ARM-Vorlage importieren** aus, um die **Partei**-Vorlage zu importieren.</span><span class="sxs-lookup"><span data-stu-id="c6f34-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="c6f34-138">Importieren Sie die Vorlage in die Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c6f34-138">Import the template into the data factory.</span></span> <span data-ttu-id="c6f34-139">Geben Sie die folgenden Werte für **Projektdetails** und **Instanzdetails** ein.</span><span class="sxs-lookup"><span data-stu-id="c6f34-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="c6f34-140">Feld</span><span class="sxs-lookup"><span data-stu-id="c6f34-140">Field</span></span> | <span data-ttu-id="c6f34-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f34-141">Value</span></span>
    ---|---
    <span data-ttu-id="c6f34-142">Abonnement</span><span class="sxs-lookup"><span data-stu-id="c6f34-142">Subscription</span></span> | <span data-ttu-id="c6f34-143">Azure-Abonnement</span><span class="sxs-lookup"><span data-stu-id="c6f34-143">Azure subscription</span></span>
    <span data-ttu-id="c6f34-144">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c6f34-144">Resource group</span></span> | <span data-ttu-id="c6f34-145">Geben Sie dieselbe Ressource an, unter der das Speicherkonto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6f34-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="c6f34-146">Region</span><span class="sxs-lookup"><span data-stu-id="c6f34-146">Region</span></span> | <span data-ttu-id="c6f34-147">Geben Sie die Region an.</span><span class="sxs-lookup"><span data-stu-id="c6f34-147">Specify region.</span></span>
    <span data-ttu-id="c6f34-148">Name der Factory</span><span class="sxs-lookup"><span data-stu-id="c6f34-148">Factory Name</span></span> | <span data-ttu-id="c6f34-149">Geben Sie den Namen der Factory an.</span><span class="sxs-lookup"><span data-stu-id="c6f34-149">Specify factory name.</span></span>
    <span data-ttu-id="c6f34-150">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="c6f34-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="c6f34-151">Geben Sie den Schlüssel der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c6f34-151">Specify the application's key.</span></span>
    <span data-ttu-id="c6f34-152">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="c6f34-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="c6f34-153">Azure Blob Storage-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c6f34-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="c6f34-154">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="c6f34-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="c6f34-155">Das Kennwort für das Benutzerkonto, das Sie als Benutzernamen angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="c6f34-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="c6f34-156">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="c6f34-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="c6f34-157">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="c6f34-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="c6f34-158">Geben Sie die Mandanteninformationen (Domänenname oder Mandanten-ID) an, unter denen sich Ihre Anwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="c6f34-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="c6f34-159">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="c6f34-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="c6f34-160">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="c6f34-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="c6f34-161">Geben Sie den Schlüssel der Client-ID an.</span><span class="sxs-lookup"><span data-stu-id="c6f34-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="c6f34-162">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="c6f34-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="c6f34-163">Der Benutzername für die Verbindung zu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c6f34-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="c6f34-164">Zusätzliche Informationen finden Sie unter einem der folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c6f34-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="c6f34-165">Manuelles Heraufstufen einer Resource Manager-Vorlage für jede Umgebung</span><span class="sxs-lookup"><span data-stu-id="c6f34-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="c6f34-166">Verknüpfte Serviceeigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6f34-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="c6f34-167">Kopieren Sie Daten mit Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="c6f34-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="c6f34-168">Überprüfen Sie nach der Bereitstellung die Datensätze, den Datenfluss und den verknüpften Dienst der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c6f34-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datensätze, Datenfluss und verknüpfter Dienst](media/data-factory-validate.png)

11. <span data-ttu-id="c6f34-170">Gehen Sie zu **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="c6f34-170">Navigate to **Manage**.</span></span> <span data-ttu-id="c6f34-171">Wählen Sie unter **Verbindungen** **Verknüpfter Dienst** aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="c6f34-172">Wählen Sie **DynamicsCrmLinkedService** aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="c6f34-173">Geben Sie im Formular **Verknüpften Dienst bearbeiten (Dynamics CRM)** die folgenden Werte ein.</span><span class="sxs-lookup"><span data-stu-id="c6f34-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="c6f34-174">Feld</span><span class="sxs-lookup"><span data-stu-id="c6f34-174">Field</span></span> | <span data-ttu-id="c6f34-175">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f34-175">Value</span></span>
    ---|---
    <span data-ttu-id="c6f34-176">Name</span><span class="sxs-lookup"><span data-stu-id="c6f34-176">Name</span></span> | <span data-ttu-id="c6f34-177">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="c6f34-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="c6f34-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6f34-178">Description</span></span> | <span data-ttu-id="c6f34-179">Verknüpfte Dienste zur Verbindung mit der CRM-Instanz zum Abrufen von Entitätsdaten</span><span class="sxs-lookup"><span data-stu-id="c6f34-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="c6f34-180">Verbindung über Integration Runtime herstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-180">Connect via integration runtime</span></span> | <span data-ttu-id="c6f34-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6f34-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="c6f34-182">Bereitstellungstyp</span><span class="sxs-lookup"><span data-stu-id="c6f34-182">Deployment type</span></span> | <span data-ttu-id="c6f34-183">Online</span><span class="sxs-lookup"><span data-stu-id="c6f34-183">Online</span></span>
    <span data-ttu-id="c6f34-184">Dienst-URI</span><span class="sxs-lookup"><span data-stu-id="c6f34-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="c6f34-185">Authentifizierungstyp</span><span class="sxs-lookup"><span data-stu-id="c6f34-185">Authentication type</span></span> | <span data-ttu-id="c6f34-186">Office365</span><span class="sxs-lookup"><span data-stu-id="c6f34-186">Office365</span></span>
    <span data-ttu-id="c6f34-187">Benutzername</span><span class="sxs-lookup"><span data-stu-id="c6f34-187">User name</span></span> |
    <span data-ttu-id="c6f34-188">Kennwort oder Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="c6f34-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="c6f34-189">Kennwort</span><span class="sxs-lookup"><span data-stu-id="c6f34-189">Password</span></span>
    <span data-ttu-id="c6f34-190">Kennwort</span><span class="sxs-lookup"><span data-stu-id="c6f34-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="c6f34-191">Die Vorlage ausführen</span><span class="sxs-lookup"><span data-stu-id="c6f34-191">Run the template</span></span>

1. <span data-ttu-id="c6f34-192">Halten Sie das folgende duale Schreiben für **Konto**, **Kontakt** und **Kreditor** mit der Finance and Operations-App an.</span><span class="sxs-lookup"><span data-stu-id="c6f34-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="c6f34-193">Debitoren V3 (Konten)</span><span class="sxs-lookup"><span data-stu-id="c6f34-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="c6f34-194">Debitoren V3 (Kontakte)</span><span class="sxs-lookup"><span data-stu-id="c6f34-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="c6f34-195">CDS-Kontakte V2 (Kontakte)</span><span class="sxs-lookup"><span data-stu-id="c6f34-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="c6f34-196">CDS-Kontakte V2 (Kontakte)</span><span class="sxs-lookup"><span data-stu-id="c6f34-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="c6f34-197">Kreditor V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="c6f34-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="c6f34-198">Stellen Sie sicher, dass die Karten aus der Tabelle `msdy_dualwriteruntimeconfig` in Dataverse entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c6f34-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="c6f34-199">Installieren Sie [Partei- und globale Adressbuchlösungen mit dualem Schreiben](https://aka.ms/dual-write-gab) aus AppSource.</span><span class="sxs-lookup"><span data-stu-id="c6f34-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="c6f34-200">Führen Sie in der Finance and Operations-App **Erstsynchronisierung** für die folgenden Tabellen durch, die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="c6f34-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="c6f34-201">Anreden</span><span class="sxs-lookup"><span data-stu-id="c6f34-201">Salutations</span></span>
    + <span data-ttu-id="c6f34-202">Arten von Persönlichkeitsmerkmalen</span><span class="sxs-lookup"><span data-stu-id="c6f34-202">Personal character types</span></span>
    + <span data-ttu-id="c6f34-203">Schlussformel</span><span class="sxs-lookup"><span data-stu-id="c6f34-203">Complimentary closing</span></span>
    + <span data-ttu-id="c6f34-204">Titel von Kontaktpersonen</span><span class="sxs-lookup"><span data-stu-id="c6f34-204">Contact person titles</span></span>
    + <span data-ttu-id="c6f34-205">Entscheidungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="c6f34-205">Decision making roles</span></span>
    + <span data-ttu-id="c6f34-206">Treueebenen</span><span class="sxs-lookup"><span data-stu-id="c6f34-206">Loyalty levels</span></span>

5. <span data-ttu-id="c6f34-207">Deaktivieren Sie in der App zur Kundenbindung die folgenden Plugin-Schritte.</span><span class="sxs-lookup"><span data-stu-id="c6f34-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="c6f34-208">Kontoupdate</span><span class="sxs-lookup"><span data-stu-id="c6f34-208">Account Update</span></span>
         + <span data-ttu-id="c6f34-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="c6f34-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="c6f34-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="c6f34-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="c6f34-211">Kontakt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-211">Contact Update</span></span>
         + <span data-ttu-id="c6f34-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="c6f34-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="c6f34-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="c6f34-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="c6f34-214">msdyn_party-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="c6f34-214">msdyn_party Update</span></span>
         + <span data-ttu-id="c6f34-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party</span><span class="sxs-lookup"><span data-stu-id="c6f34-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="c6f34-216">msdyn_vendor-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="c6f34-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="c6f34-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="c6f34-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="c6f34-218">Deaktivieren Sie in der App zur Kundenbindung die folgenden Workflows:</span><span class="sxs-lookup"><span data-stu-id="c6f34-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="c6f34-219">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="c6f34-220">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="c6f34-221">Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="c6f34-222">Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="c6f34-223">Lieferanten in der Kontotabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="c6f34-224">Lieferanten in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="c6f34-225">Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="c6f34-226">Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="c6f34-227">Führen Sie in der Data Factory die Vorlage aus, indem Sie **Jetzt auslösen** wie im folgenden Bild gezeigt auswählen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="c6f34-228">Dieser Prozess kann je nach Datenvolumen einige Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="c6f34-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Ausführung auslösen](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="c6f34-230">Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage ändern.</span><span class="sxs-lookup"><span data-stu-id="c6f34-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="c6f34-231">Importieren Sie den neuen **Partei**-Datensatz in der Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="c6f34-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="c6f34-232">Laden Sie die Datei `FONewParty.csv` aus dem Azure Blob Storage herunter.</span><span class="sxs-lookup"><span data-stu-id="c6f34-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="c6f34-233">Der Pfad lautet `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="c6f34-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="c6f34-234">Konvertieren Sie die Datei `FONewParty.csv` in eine Excel-Datei und importieren Sie die Excel-Datei in die Finance and Operations App.</span><span class="sxs-lookup"><span data-stu-id="c6f34-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="c6f34-235">Wenn der CSV-Import bei Ihnen funktioniert, können Sie die CSV-Datei direkt importieren.</span><span class="sxs-lookup"><span data-stu-id="c6f34-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="c6f34-236">Das Importieren kann je nach Datenvolumen einige Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="c6f34-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="c6f34-237">Weitere Informationen finden Sie unter [Übersicht über Datenimport- und -exportaufträge](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="c6f34-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Die Datavers-Partei-Datensätze importieren](media/data-factory-import-party.png)

9. <span data-ttu-id="c6f34-239">Aktivieren Sie in den Apps zur Kundenbindung die folgenden Plugin-Schritte:</span><span class="sxs-lookup"><span data-stu-id="c6f34-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="c6f34-240">Kontoupdate</span><span class="sxs-lookup"><span data-stu-id="c6f34-240">Account Update</span></span>
         + <span data-ttu-id="c6f34-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="c6f34-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="c6f34-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="c6f34-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="c6f34-243">Kontakt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-243">Contact Update</span></span>
         + <span data-ttu-id="c6f34-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="c6f34-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="c6f34-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="c6f34-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="c6f34-246">msdyn_party-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="c6f34-246">msdyn_party Update</span></span>
         + <span data-ttu-id="c6f34-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party</span><span class="sxs-lookup"><span data-stu-id="c6f34-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="c6f34-248">msdyn_vendor-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="c6f34-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="c6f34-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="c6f34-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="c6f34-250">Aktivieren Sie in den Kundenbindungs-Apps die folgenden Workflows, wenn Sie sie in den vorherigen Schritten deaktiviert haben:</span><span class="sxs-lookup"><span data-stu-id="c6f34-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="c6f34-251">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="c6f34-252">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="c6f34-253">Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="c6f34-254">Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="c6f34-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="c6f34-255">Lieferanten in der Kontotabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="c6f34-256">Lieferanten in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="c6f34-257">Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="c6f34-258">Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c6f34-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="c6f34-259">Führen Sie die mit der **Partei** zusammenhängenden Karten wie in [Partei- und globales Adressbuch](party-gab.md) angewiesen aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c6f34-260">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="c6f34-260">Troubleshooting</span></span>

1. <span data-ttu-id="c6f34-261">Wenn der Prozess fehlschlägt, führen Sie die Data Factory beginnend mit der fehlgeschlagenen Aktivität erneut aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="c6f34-262">Einige Dateien werden von der Data Factory generiert, die Sie zur Datenüberprüfung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c6f34-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="c6f34-263">Die Data Factory wird basierend auf durch Kommas getrennten CSV-Dateien ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6f34-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="c6f34-264">Wenn ein Feldwert ein Komma hat, kann dies die Ergebnisse beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="c6f34-265">Sie müssen die Kommas entfernen.</span><span class="sxs-lookup"><span data-stu-id="c6f34-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="c6f34-266">Die Registerkate **Überwachung** enthält Informationen zu allen Schritten und verarbeiteten Daten.</span><span class="sxs-lookup"><span data-stu-id="c6f34-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="c6f34-267">Wählen Sie einen bestimmten Schritt zum Debuggen aus.</span><span class="sxs-lookup"><span data-stu-id="c6f34-267">Select a specific step to debug it.</span></span>

    ![Registerkarte „Überwachung“](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="c6f34-269">Mehr über die Vorlage</span><span class="sxs-lookup"><span data-stu-id="c6f34-269">Learn more about the template</span></span>

<span data-ttu-id="c6f34-270">Weitere Informationen zur Vorlage finden Sie unter [Kommentare zur Readme-Datei für Azure Data Factory-Vorlagen](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="c6f34-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
