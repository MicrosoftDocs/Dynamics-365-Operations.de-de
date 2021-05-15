---
title: Auf das Partei- und globale Adressbuchmodell aktualisieren
description: In diesem Thema wird beschrieben, wie Sie Daten aus dualem Schreiben auf das Partei- und das globale Adressbuchmodell aktualisieren.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941082"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="2c4cb-103">Auf das Partei- und globale Adressbuchmodell aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2c4cb-104">Die [Azure Data Factory-Vorlage](https://aka.ms/dual-write-gab-adf) hilft Ihnen beim Aktualisieren vorhandener **Konto**-, **Kontakt**- und **Kreditor**-Tabellendaten in dualem Schreiben in das Partei- und das globale Adressbuchmodell.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="2c4cb-105">Die Vorlage stimmt die Daten sowohl von Finance and Operations-Apps als auch von Anwendungen zur Kundenbindung ab.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="2c4cb-106">Am Ende des Prozesses werden die Felder **Partei** und **Kontakt** für **Partei**-Datensätze erstellt und mit **Konto**-, **Kontakt**- und **Kreditor**-Datensätzen in Anwendungen zur Kundenbindung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="2c4cb-107">Eine .csv-Datei (`FONewParty.csv`) wird generiert, um einen neuen **Partei**-Datensatz in der Finance and Operations-App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="2c4cb-108">Dieses Thema enthält Anweisungen zur Verwendung der Data Factory-Vorlage und zum Aktualisieren Ihrer Daten.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="2c4cb-109">Wenn Sie keine Anpassungen vorgenommen haben, können Sie die Vorlage unverändert verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="2c4cb-110">Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage anhand der folgenden Anweisungen ändern.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="2c4cb-111">Die Vorlage hilft nur, die **Partei**-Daten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="2c4cb-112">Ein zukünftiger Release wird postalische und elektronische Adressen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c4cb-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-113">Prerequisites</span></span>

<span data-ttu-id="2c4cb-114">Es gelten die folgenden Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="2c4cb-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="2c4cb-115">Azure-Abonnement</span><span class="sxs-lookup"><span data-stu-id="2c4cb-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="2c4cb-116">Zugriff auf die Vorlage</span><span class="sxs-lookup"><span data-stu-id="2c4cb-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="2c4cb-117">Sie sind ein bestehender Kunde für duales Schreiben.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="2c4cb-118">Vorbereitung auf die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="2c4cb-119">**Vollständig synchronisiert**: Beide Umgebungen sind vollständig im Hinblick auf **Konto (Kunde)**, **Kontakt** und **Kreditor** synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="2c4cb-120">**Integrationsschlüssel**: Die Tabellen **Konto (Kunde)**, **Kontakt** und **Kreditor** in Apps zur Kundenbindung verwenden die sofort einsatzbereiten Integrationsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="2c4cb-121">Wenn Sie die Integrationsschlüssel angepasst haben, müssen Sie die Vorlage anpassen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="2c4cb-122">**Parteinummer**: Alle **Konto (Kunde)**-, **Kontakt**- und **Kreditor**-Datensätze, die aktualisiert werden, haben eine **Partei**-Nummer.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="2c4cb-123">Aufzeichnungen ohne **Partei**-Nummer werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="2c4cb-124">Wenn Sie diese Datensätze aktualisieren möchten, fügen Sie eine **Partei**-Nummer hinzu, bevor Sie den Aktualisierungsprozess starten.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="2c4cb-125">**Systemausfall**: Während des Aktualisierungsprozesses müssen Sie sowohl die Finance and Operations- als auch die Kundenbindungsumgebung offline nehmen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="2c4cb-126">**Momentaufnahme**: Machen Sie sowohl von der Finance and Operations als auch der App zur Kundenbindung eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="2c4cb-127">Verwenden Sie die Momentaufnahmen, um bei Bedarf den vorherigen Status wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="2c4cb-128">Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-128">Deployment</span></span>

1. <span data-ttu-id="2c4cb-129">Laden Sie die Vorlage von [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf) herunter.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="2c4cb-130">Melden Sie sich auf [Microsoft Azure](https://portal.azure.com/) an.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="2c4cb-131">Erstellen Sie eine [Ressourcengruppe](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="2c4cb-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="2c4cb-132">Erstellen Sie ein [Speicherkonto](/azure/storage/common/storage-account-create?tabs=azure-portal) in der von Ihnen erstellten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="2c4cb-133">Erstellen Sie eine [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) über der von Ihnen erstellten Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="2c4cb-134">Öffnen Sie die Data Factory und wählen Sie die Kachel **Erstellen und überwachen** aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="2c4cb-135">Wählen Sie in der Registerkarte **Verwalten** die **ARM-Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="2c4cb-136">Wählen Sie **ARM-Vorlage importieren** aus, um die **Partei**-Vorlage zu importieren.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="2c4cb-137">Importieren Sie die Vorlage in die Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-137">Import the template into the data factory.</span></span> <span data-ttu-id="2c4cb-138">Geben Sie die folgenden Werte für **Projektdetails** und **Instanzdetails** ein.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="2c4cb-139">Feld</span><span class="sxs-lookup"><span data-stu-id="2c4cb-139">Field</span></span> | <span data-ttu-id="2c4cb-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2c4cb-140">Value</span></span>
    ---|---
    <span data-ttu-id="2c4cb-141">Abonnement</span><span class="sxs-lookup"><span data-stu-id="2c4cb-141">Subscription</span></span> | <span data-ttu-id="2c4cb-142">Azure-Abonnement</span><span class="sxs-lookup"><span data-stu-id="2c4cb-142">Azure subscription</span></span>
    <span data-ttu-id="2c4cb-143">Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2c4cb-143">Resource group</span></span> | <span data-ttu-id="2c4cb-144">Geben Sie dieselbe Ressource an, unter der das Speicherkonto erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="2c4cb-145">Region</span><span class="sxs-lookup"><span data-stu-id="2c4cb-145">Region</span></span> | <span data-ttu-id="2c4cb-146">Geben Sie die Region an.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-146">Specify region.</span></span>
    <span data-ttu-id="2c4cb-147">Name der Factory</span><span class="sxs-lookup"><span data-stu-id="2c4cb-147">Factory Name</span></span> | <span data-ttu-id="2c4cb-148">Geben Sie den Namen der Factory an.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-148">Specify factory name.</span></span>
    <span data-ttu-id="2c4cb-149">FO Linked Service_service Principal Key</span><span class="sxs-lookup"><span data-stu-id="2c4cb-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="2c4cb-150">Geben Sie den Schlüssel der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-150">Specify the application's key.</span></span>
    <span data-ttu-id="2c4cb-151">Azure Blob Storage_connection String</span><span class="sxs-lookup"><span data-stu-id="2c4cb-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="2c4cb-152">Azure Blob Storage-Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="2c4cb-153">Dynamics Crm Linked Service_password</span><span class="sxs-lookup"><span data-stu-id="2c4cb-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="2c4cb-154">Das Kennwort für das Benutzerkonto, das Sie als Benutzernamen angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="2c4cb-155">FO Linked Service_properties_type Properties_url</span><span class="sxs-lookup"><span data-stu-id="2c4cb-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="2c4cb-156">FO Linked Service_properties_type Properties_tenant</span><span class="sxs-lookup"><span data-stu-id="2c4cb-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="2c4cb-157">Geben Sie die Mandanteninformationen (Domänenname oder Mandanten-ID) an, unter denen sich Ihre Anwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="2c4cb-158">FO Linked Service_properties_type Properties_aad Resource Id</span><span class="sxs-lookup"><span data-stu-id="2c4cb-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="2c4cb-159">FO Linked Service_properties_type Properties_service Principal Id</span><span class="sxs-lookup"><span data-stu-id="2c4cb-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="2c4cb-160">Geben Sie den Schlüssel der Client-ID an.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="2c4cb-161">Dynamics Crm Linked Service_properties_type Properties_username</span><span class="sxs-lookup"><span data-stu-id="2c4cb-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="2c4cb-162">Der Benutzername für die Verbindung zu Dynamics.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="2c4cb-163">Weitere Informationen finden Sie unter [Manuelles Höherstufen einer Resource Manager-Vorlage für jede Umgebung](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Eigenschaften des verknüpften Diensts](/azure/data-factory/connector-dynamics-ax#linked-service-properties) und [Daten mit Azure Data Factory kopieren](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="2c4cb-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="2c4cb-164">Überprüfen Sie nach der Bereitstellung die Datensätze, den Datenfluss und den verknüpften Dienst der Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datensätze, Datenfluss und verknüpfter Dienst](media/data-factory-validate.png)

11. <span data-ttu-id="2c4cb-166">Gehen Sie zu **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-166">Navigate to **Manage**.</span></span> <span data-ttu-id="2c4cb-167">Wählen Sie unter **Verbindungen** **Verknüpfter Dienst** aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="2c4cb-168">Wählen Sie **DynamicsCrmLinkedService** aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="2c4cb-169">Geben Sie im Formular **Verknüpften Dienst bearbeiten (Dynamics CRM)** die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="2c4cb-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="2c4cb-170">Feld</span><span class="sxs-lookup"><span data-stu-id="2c4cb-170">Field</span></span> | <span data-ttu-id="2c4cb-171">Wert</span><span class="sxs-lookup"><span data-stu-id="2c4cb-171">Value</span></span>
    ---|---
    <span data-ttu-id="2c4cb-172">Name</span><span class="sxs-lookup"><span data-stu-id="2c4cb-172">Name</span></span> | <span data-ttu-id="2c4cb-173">DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="2c4cb-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="2c4cb-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-174">Description</span></span> | <span data-ttu-id="2c4cb-175">Verknüpfte Dienste zur Verbindung mit der CRM-Instanz zum Abrufen von Entitätsdaten</span><span class="sxs-lookup"><span data-stu-id="2c4cb-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="2c4cb-176">Verbindung über Integration Runtime herstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-176">Connect via integration runtime</span></span> | <span data-ttu-id="2c4cb-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c4cb-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="2c4cb-178">Bereitstellungstyp</span><span class="sxs-lookup"><span data-stu-id="2c4cb-178">Deployment type</span></span> | <span data-ttu-id="2c4cb-179">Online</span><span class="sxs-lookup"><span data-stu-id="2c4cb-179">Online</span></span>
    <span data-ttu-id="2c4cb-180">Dienst-URI</span><span class="sxs-lookup"><span data-stu-id="2c4cb-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="2c4cb-181">Authentifizierungstyp</span><span class="sxs-lookup"><span data-stu-id="2c4cb-181">Authentication type</span></span> | <span data-ttu-id="2c4cb-182">Office365</span><span class="sxs-lookup"><span data-stu-id="2c4cb-182">Office365</span></span>
    <span data-ttu-id="2c4cb-183">Benutzername</span><span class="sxs-lookup"><span data-stu-id="2c4cb-183">User name</span></span> |
    <span data-ttu-id="2c4cb-184">Kennwort oder Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2c4cb-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="2c4cb-185">Kennwort</span><span class="sxs-lookup"><span data-stu-id="2c4cb-185">Password</span></span>
    <span data-ttu-id="2c4cb-186">Kennwort</span><span class="sxs-lookup"><span data-stu-id="2c4cb-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="2c4cb-187">Die Vorlage ausführen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-187">Run the template</span></span>

1. <span data-ttu-id="2c4cb-188">Halten Sie das folgende duale Schreiben für **Konto**, **Kontakt** und **Kreditor** mit der Finance and Operations-App an.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="2c4cb-189">Debitoren V3 (Konten)</span><span class="sxs-lookup"><span data-stu-id="2c4cb-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="2c4cb-190">Debitoren V3 (Kontakte)</span><span class="sxs-lookup"><span data-stu-id="2c4cb-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="2c4cb-191">CDS-Kontakte V2 (Kontakte)</span><span class="sxs-lookup"><span data-stu-id="2c4cb-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="2c4cb-192">CDS-Kontakte V2 (Kontakte)</span><span class="sxs-lookup"><span data-stu-id="2c4cb-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="2c4cb-193">Kreditor V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="2c4cb-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="2c4cb-194">Stellen Sie sicher, dass die Karten aus der Tabelle `msdy_dualwriteruntimeconfig` in Dataverse entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="2c4cb-195">Installieren Sie [Partei- und globale Adressbuchlösungen mit dualem Schreiben](https://aka.ms/dual-write-gab) aus AppSource.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="2c4cb-196">Führen Sie in der Finance and Operations-App **Erstsynchronisierung** für die folgenden Tabellen durch, die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="2c4cb-197">Anreden</span><span class="sxs-lookup"><span data-stu-id="2c4cb-197">Salutations</span></span>
    + <span data-ttu-id="2c4cb-198">Arten von Persönlichkeitsmerkmalen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-198">Personal character types</span></span>
    + <span data-ttu-id="2c4cb-199">Schlussformel</span><span class="sxs-lookup"><span data-stu-id="2c4cb-199">Complimentary closing</span></span>
    + <span data-ttu-id="2c4cb-200">Titel von Kontaktpersonen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-200">Contact person titles</span></span>
    + <span data-ttu-id="2c4cb-201">Entscheidungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-201">Decision making roles</span></span>
    + <span data-ttu-id="2c4cb-202">Treueebenen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-202">Loyalty levels</span></span>

5. <span data-ttu-id="2c4cb-203">Deaktivieren Sie in der App zur Kundenbindung die folgenden Plugin-Schritte.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="2c4cb-204">Konto aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-204">Account Update</span></span>
         + <span data-ttu-id="2c4cb-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="2c4cb-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="2c4cb-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="2c4cb-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="2c4cb-207">Kontakt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-207">Contact Update</span></span>
         + <span data-ttu-id="2c4cb-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="2c4cb-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="2c4cb-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="2c4cb-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="2c4cb-210">msdyn_party-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-210">msdyn_party Update</span></span>
         + <span data-ttu-id="2c4cb-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party</span><span class="sxs-lookup"><span data-stu-id="2c4cb-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="2c4cb-212">msdyn_vendor-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="2c4cb-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="2c4cb-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="2c4cb-214">Deaktivieren Sie in der App zur Kundenbindung die folgenden Workflows:</span><span class="sxs-lookup"><span data-stu-id="2c4cb-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="2c4cb-215">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c4cb-216">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c4cb-217">Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="2c4cb-218">Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="2c4cb-219">Lieferanten in der Kontotabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c4cb-220">Lieferanten in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="2c4cb-221">Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="2c4cb-222">Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="2c4cb-223">Führen Sie in der Data Factory die Vorlage aus, indem Sie **Jetzt auslösen** wie im folgenden Bild gezeigt auswählen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="2c4cb-224">Dieser Prozess kann je nach Datenvolumen einige Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Ausführung auslösen](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="2c4cb-226">Wenn Sie Anpassungen für **Konto**, **Kontakt** und **Kreditor** vorgenommen haben, müssen Sie die Vorlage ändern.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="2c4cb-227">Importieren Sie den neuen **Partei**-Datensatz in der Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="2c4cb-228">Laden Sie die Datei `FONewParty.csv` aus dem Azure Blob Storage herunter.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="2c4cb-229">Der Pfad lautet `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="2c4cb-230">Konvertieren Sie die Datei `FONewParty.csv` in eine Excel-Datei und importieren Sie die Excel-Datei in die Finance and Operations-App.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="2c4cb-231">Wenn der CSV-Import bei Ihnen funktioniert, können Sie die CSV-Datei direkt importieren.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="2c4cb-232">Das Importieren kann je nach Datenvolumen einige Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="2c4cb-233">Weitere Informationen finden Sie unter [Übersicht über Datenimport- und -exportaufträge](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="2c4cb-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Die Datavers-Partei-Datensätze importieren](media/data-factory-import-party.png)

9. <span data-ttu-id="2c4cb-235">Aktivieren Sie in den Apps zur Kundenbindung die folgenden Plugin-Schritte:</span><span class="sxs-lookup"><span data-stu-id="2c4cb-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="2c4cb-236">Konto aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-236">Account Update</span></span>
         + <span data-ttu-id="2c4cb-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="2c4cb-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="2c4cb-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Aktualisieren des Kontos</span><span class="sxs-lookup"><span data-stu-id="2c4cb-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="2c4cb-239">Kontakt aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-239">Contact Update</span></span>
         + <span data-ttu-id="2c4cb-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="2c4cb-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="2c4cb-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Aktualisieren des Kontakts</span><span class="sxs-lookup"><span data-stu-id="2c4cb-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="2c4cb-242">msdyn_party-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-242">msdyn_party Update</span></span>
         + <span data-ttu-id="2c4cb-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Aktualisieren von msdyn_party</span><span class="sxs-lookup"><span data-stu-id="2c4cb-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="2c4cb-244">msdyn_vendor-Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="2c4cb-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Aktualisieren von msdyn_vendor</span><span class="sxs-lookup"><span data-stu-id="2c4cb-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="2c4cb-246">Aktivieren Sie in den Kundenbindungs-Apps die folgenden Workflows, wenn Sie sie in den vorherigen Schritten deaktiviert haben:</span><span class="sxs-lookup"><span data-stu-id="2c4cb-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="2c4cb-247">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c4cb-248">Lieferanten in der Kontotabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c4cb-249">Kreditoren vom Typ „Person“ in der Kontakttabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="2c4cb-250">Lieferanten vom Typ „Person“ in der Lieferantentabelle erstellen</span><span class="sxs-lookup"><span data-stu-id="2c4cb-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="2c4cb-251">Lieferanten in der Kontotabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="2c4cb-252">Lieferanten in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="2c4cb-253">Lieferanten vom Typ „Person“ in der Kontakttabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="2c4cb-254">Lieferanten vom Typ „Person“ in der Lieferantentabelle aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2c4cb-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="2c4cb-255">Führen Sie die mit der **Partei** zusammenhängenden Karten wie in [Partei- und globales Adressbuch](party-gab.md) angewiesen aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2c4cb-256">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="2c4cb-256">Troubleshooting</span></span>

1. <span data-ttu-id="2c4cb-257">Wenn der Prozess fehlschlägt, führen Sie die Data Factory beginnend mit der fehlgeschlagenen Aktivität erneut aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="2c4cb-258">Einige Dateien werden von der Data Factory generiert, die Sie zur Datenüberprüfung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="2c4cb-259">Die Data Factory wird basierend auf durch Kommas getrennten CSV-Dateien ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="2c4cb-260">Wenn ein Feldwert ein Komma hat, kann dies die Ergebnisse beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="2c4cb-261">Sie müssen die Kommas entfernen.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="2c4cb-262">Die Registerkate **Überwachung** enthält Informationen zu allen Schritten und verarbeiteten Daten.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="2c4cb-263">Wählen Sie einen bestimmten Schritt zum Debuggen aus.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-263">Select a specific step to debug it.</span></span>

    ![Registerkarte „Überwachung“](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="2c4cb-265">Mehr über die Vorlage</span><span class="sxs-lookup"><span data-stu-id="2c4cb-265">Learn more about the template</span></span>

<span data-ttu-id="2c4cb-266">In der [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)-Datei finden Sie Anmerkungen zur Vorlage.</span><span class="sxs-lookup"><span data-stu-id="2c4cb-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>