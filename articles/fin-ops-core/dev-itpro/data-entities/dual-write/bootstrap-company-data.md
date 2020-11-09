---
title: Ausführen von Bootstrap mit Unternehmensdaten – FAQ
description: Hier erhalten Sie Informationen dazu, wie Sie Daten in Common Data Service oder anderen Dynamics 365-Apps mit Unternehmensinformationen laden, bevor Sie die Verbindung für duales Schreiben aktivieren.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: a2adf284111f2ccc9a830635ab3fb8f4731c84d9
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997575"
---
# <a name="bootstrap-with-company-data-faq"></a><span data-ttu-id="71ae6-103">Ausführen von Bootstrap mit Unternehmensdaten – FAQ</span><span class="sxs-lookup"><span data-stu-id="71ae6-103">Bootstrap with company data FAQ</span></span>
 
[!include [banner](../../includes/banner.md)]


## <a name="why-do-i-need-bootstrapping"></a><span data-ttu-id="71ae6-104">Warum benötige ich Bootstrapping?</span><span class="sxs-lookup"><span data-stu-id="71ae6-104">Why do I need bootstrapping?</span></span> 
<span data-ttu-id="71ae6-105">Sie verfügen möglicherweise über eine vorhandene Common Data Service- oder andere Dynamics 365-App-Instanz mit Geschäftsdaten und möchten die Verbindung für duales Schreiben für diese aktivieren.</span><span class="sxs-lookup"><span data-stu-id="71ae6-105">You might have an existing Common Data Service or other Dynamics 365 app instance with business data, and you want to enable dual-write connection against it.</span></span> <span data-ttu-id="71ae6-106">In diesem Fall müssen Sie ein Bootstrap für Daten in Common Data Service oder anderen Dynamics 365-Apps mit Unternehmensinformationen ausführen, bevor Sie die Verbindung für duales Schreiben aktivieren.</span><span class="sxs-lookup"><span data-stu-id="71ae6-106">In this case, you need to bootstrap Common Data Service or other Dynamics 365 app data with company information before enabling dual-write connection.</span></span>  
 
## <a name="when-should-i-use-bootstrapping"></a><span data-ttu-id="71ae6-107">Wann sollte Bootstrapping verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="71ae6-107">When should I use bootstrapping?</span></span> 
<span data-ttu-id="71ae6-108">Sie sollten Bootstrapping verwenden, bevor Sie  Entitätszuordnungen für duales Schreiben aktivieren (in Schritt 5).</span><span class="sxs-lookup"><span data-stu-id="71ae6-108">You should use bootstrapping before enabling dual-write entity maps (during step #5).</span></span>  
1. <span data-ttu-id="71ae6-109">Um die Verbindung für duales Schreiben zwischen Instanzen der Finance and Operations-App und Common Data Service oder einer anderen Dynamics 365-App einzurichten, melden Sie sich bei der Finance and Operations-App als Administrator an.</span><span class="sxs-lookup"><span data-stu-id="71ae6-109">To setup the dual-write connection between instances of your Finance and Operations app and the Common Data Service or other Dynamics 365 app, log in to the Finance and Operations app as an administrator.</span></span> 
2. <span data-ttu-id="71ae6-110">Wechseln Sie zum Modul **Datenverwaltung** , und klicken Sie auf die Schaltfläche **Duales Schreiben**.</span><span class="sxs-lookup"><span data-stu-id="71ae6-110">Go to the **Data Management** module and click the **Dual-Write** button.</span></span> <span data-ttu-id="71ae6-111">Dadurch wird **Data Integrator** gestartet.</span><span class="sxs-lookup"><span data-stu-id="71ae6-111">This launches the **Data Integrator**.</span></span> 
3. <span data-ttu-id="71ae6-112">Stellen Sie die Verbindung für duales Schrieben für mindestens ein Unternehmen her.</span><span class="sxs-lookup"><span data-stu-id="71ae6-112">Create the dual-write connection for one or more companies.</span></span>  
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="71ae6-113">![Herstellen der Verbindung für duales Schreiben](media/dual-write-boot-1.png)</span><span class="sxs-lookup"><span data-stu-id="71ae6-113">![Create dual-write connection](media/dual-write-boot-1.png)</span></span>
4. <span data-ttu-id="71ae6-114">Aktivieren Sie die Entitätszuordnung **Cdm_companies**.</span><span class="sxs-lookup"><span data-stu-id="71ae6-114">Enable the **Cdm_companies** entity map.</span></span> <span data-ttu-id="71ae6-115">Dies synchronisiert Unternehmen aus der Finance and Operations-App zu Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="71ae6-115">This synchronizes companies from the Finance and Operations app to Common Data Service.</span></span>  
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="71ae6-116">![Aktivieren der Entitätszuordnung](media/dual-write-boot-2.png)</span><span class="sxs-lookup"><span data-stu-id="71ae6-116">![Enable the entity map](media/dual-write-boot-2.png)</span></span>
5. <span data-ttu-id="71ae6-117">Führen Sie den Beispielbootstrappingcode auf der Common Data Service- oder einer anderen Dynamics 365-App-Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="71ae6-117">Run the sample bootstrapping code on the Common Data Service or other Dynamics 365 app instance.</span></span>  
6. <span data-ttu-id="71ae6-118">Nachdem das Bootstrapping abgeschlossen und das System für die Live-Synchronisierung bereit ist, aktivieren Sie die Entitätszuordnungen.</span><span class="sxs-lookup"><span data-stu-id="71ae6-118">When the bootstrapping is done and the system is ready for the live sync, enable the entity maps.</span></span>  

    <span data-ttu-id="71ae6-119">Durch die Aktivierung von Entitätszuordnungen wird die Erstsynchronisierung der Daten für die aktivierten Entitätszuordnungen ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="71ae6-119">Enabling the entity maps triggers the initial data sync for the enabled entity maps.</span></span> <span data-ttu-id="71ae6-120">Die Daten, die den über die Verbindung für duales Schreiben ausgewählten Unternehmen entsprechen, werden zwischen der Finance and Operations-App und Common Data Service synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="71ae6-120">The data corresponding to the companies chosen on the dual-write connection is synchronized between the Finance and Operations app and Common Data Service.</span></span> 
 
## <a name="how-to-i-use-the-code-sample"></a><span data-ttu-id="71ae6-121">Wie verwende ich das Codebeispiel?</span><span class="sxs-lookup"><span data-stu-id="71ae6-121">How to I use the code sample?</span></span>
<span data-ttu-id="71ae6-122">Der Beispielcode ist eine C#-Anwendung, die Sie in Visual Studio laden können.</span><span class="sxs-lookup"><span data-stu-id="71ae6-122">The sample code is a C# application that you can load in Visual Studio.</span></span> <span data-ttu-id="71ae6-123">Es werden NuGet-Paketabhängigkeiten im Common Data Service SDK verwendet, die Sie durch standardmäßige Visual Studio-Tools aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="71ae6-123">It takes NuGet package dependencies on the Common Data Service SDK, that you can refresh through standard Visual Studio tooling.</span></span> 

<span data-ttu-id="71ae6-124">Nachdem Sie die Lösung in Visual Studio entzippt und geöffnet und die NuGet-Pakete wiederhergestellt haben, suchen Sie im Code nach **TODO**.</span><span class="sxs-lookup"><span data-stu-id="71ae6-124">After unzipping and opening the solution in Visual Studio and restoring the NuGet packages, search for **TODO** in the code.</span></span> <span data-ttu-id="71ae6-125">Jede Entscheidung, die Sie zur Art und Weise der Ausführung von Bootstrapping für Unternehmensinformationen treffen müssen, wird durch ein **TODO** mit Beispielcode für eine kanonische Implementierung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="71ae6-125">Each decision you need to make about how you want to bootstrap company information is noted by a **TODO** , with sample code for a canonical implementation.</span></span> 

<span data-ttu-id="71ae6-126">Der Beispielcode zeigt nur eine von vielen Methoden zum Kategorisieren von Entitätsdatensätzen nach Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="71ae6-126">The sample code shows only one of many ways you might categorize entity records by company.</span></span> <span data-ttu-id="71ae6-127">Wenn Sie die Logik in den **TODO** -Abschnitten ändern, können Sie Ihre benutzerdefinierte Kategorisierung erstellen.</span><span class="sxs-lookup"><span data-stu-id="71ae6-127">By changing the logic in the **TODO** sections, you can create your custom categorization.</span></span> 
 
## <a name="what-should-i-expect"></a><span data-ttu-id="71ae6-128">Was sollte ich erwarten?</span><span class="sxs-lookup"><span data-stu-id="71ae6-128">What should I expect?</span></span>
<span data-ttu-id="71ae6-129">Mit der Beispielanwendung können Sie standardmäßig ein Wörterbuch mit Zuordnungen zwischen Geschäftseinheiten und Unternehmenscodes bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="71ae6-129">By default, the sample application lets you provide a dictionary of business unit-to-company code mappings.</span></span> <span data-ttu-id="71ae6-130">Jede Entität, für die Sie Bootstrapping mit dem Feld **OwningBusinessUnit** ausführen, wird automatisch für die Verwendung des angegebenen Unternehmens festgelegt.</span><span class="sxs-lookup"><span data-stu-id="71ae6-130">Any entity you bootstrap with an **OwningBusinessUnit** field is automatically set to use the specified company.</span></span> <span data-ttu-id="71ae6-131">Jede Entität ohne das Feld **OwningBusinessUnit** , z. B. Produkt, legt das Unternehmen basierend auf der Zuordnung mit einem leeren Unternehmenseinheitswert fest.</span><span class="sxs-lookup"><span data-stu-id="71ae6-131">Any entity without an **OwningBusinessUnit** field, such as product, will set the company based on the mapping with an empty business unit value.</span></span>

<span data-ttu-id="71ae6-132">Die Konsolenanwendung erwartet einen Parameter, entweder **–simulate** oder **–apply**.</span><span class="sxs-lookup"><span data-stu-id="71ae6-132">The console application expects one parameter, either **–simulate** or **–apply**.</span></span> <span data-ttu-id="71ae6-133">Wenn Sie den Befehlszeilenparameter **– simuliert werden** verwenden, werden keine Daten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71ae6-133">If you use the **–simulate** command line parameter, then no data is updated.</span></span> <span data-ttu-id="71ae6-134">Nur **simulation_<entityname>.csv** -Dateien werden im selben Verzeichnis wie das Tool generiert, eine für jede Entität, die aktualisiert worden wäre.</span><span class="sxs-lookup"><span data-stu-id="71ae6-134">Only **simulation_<entityname>.csv** files are generated in the same directory as the tool, one for each entity that would have been updated.</span></span> <span data-ttu-id="71ae6-135">Sie können diese Dateien während der Arbeit iterativ überprüfen, um sicherzustellen, dass der Code die Unternehmenswerte wie erwartet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71ae6-135">You can iteratively review these files while working to ensure the code updates company values as expected.</span></span> 

<span data-ttu-id="71ae6-136">Verwenden Sie den **–apply** -Parameter, wenn Sie die simulierten Aktualisierungen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="71ae6-136">When you finish with the simulated updates, then use the **–apply** parameter.</span></span> <span data-ttu-id="71ae6-137">Dadurch werden alle Datensätze, die aktuell einen falschen Unternehmenswert aufweisen, in Stapeln von 1000 Datensätzen gleichzeitig (standardmäßig) aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71ae6-137">This updates all records that currently have an incorrect company value, in batches of 1000 records at a time (by default).</span></span> <span data-ttu-id="71ae6-138">Der Code ist wie angegeben idempotent, d. h. Sie können ihn erneut ausführen, sodass nur die falsch zugeordneten Unternehmen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="71ae6-138">The code is idempotent as provided, meaning you can re-run it and only the incorrectly assigned companies will be updated.</span></span> <span data-ttu-id="71ae6-139">Bei Ausführung mit **–apply** gibt der Code CSV-Dateien der vorgenommenen Änderungen aus, die als **applied_<entityname>.csv** bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="71ae6-139">When running with **–apply** , the code outputs CSV files of the changes made, which are named **applied_<entityname>.csv**.</span></span> 

 ```csharp
 using Microsoft.Crm.Sdk.Messages;
using Microsoft.Xrm.Sdk;
using Microsoft.Xrm.Sdk.Messages;
using Microsoft.Xrm.Sdk.Query;
using Microsoft.Xrm.Tooling.Connector;
using System;
using System.Collections.Generic;
using System.Diagnostics;
using System.IO;

namespace BootstrapCompany
{
    /// <summary>
    /// Application to bootstrap the company field on existing records in CDS in preparation for integration to Finance and Operations.
    /// </summary>
    /// <remarks>
    /// This application assumes that the target companies already exist in the CDS environment in the cdm_Company table and are
    /// identified by their company code. It also assumes that the current owning business unit of each record should be used
    /// to categorize by company. This logic can easily be updated to utilize alternate sources of categorization including
    /// custom entities, teams, custom fields on tables, or any other data. This code is provided only as a sample. 
    /// 
    /// To utilize this code, update each of the locations currently denoted with a TODO statement.
    /// 
    /// This code is provided AS IS with no warranties or guarantees, and confers no rights.
    /// </remarks>
    public class Program
    {
        /// <summary>
        /// The number of records to query and update in CDS in a single operation.
        /// </summary>
        /// <remarks>
        /// The larger this number, the fewer calls will need to be made, so the faster the updates
        /// will complete. However, larger batch sizes are more likely to cause contention. Additionally,
        /// when SQL exceeds some threshold of locks (generally around 5,000), it will escalate to
        /// an entire table lock, which blocks all other activity in the live system on this table. As 
        /// such, a batch size of around 1,000 is relatively fast, while also relatively safe in terms
        /// of contention and transaction time.
        /// </remarks>
        const int requestBatchSize = 1000;

        /// <summary>
        /// The number of faults that may be seen in CDS before the operation is aborted and an exception is thrown.
        /// </summary>
        /// <remarks>
        /// An occassional error due to contention when updating large tables in production is expected, so by default
        /// errors are logged and skipped. However, if a large number of errors are seen, ignoring those errors
        /// in subsequent batches gets expensive, and is usually indicative of a larger issue that should be addressed
        /// before continuing. Faulted requests are *not* retried, but would be picked up in a subsequent run of this script.
        /// </remarks>
        const int maxFaultThreshold = 100;

        /// <summary>
        /// The maximum number of records per business unit to export when simulating.
        /// </summary>
        /// <remarks>
        /// During simulation, queries are not batched since doing so would require ordering and so be slightly
        /// different from the actual execution logic. To keep this the same between both paths, simulates are
        /// not batched and so a separate maximum number of records per business unit can be specified.
        /// </remarks>
        const int maxSimulateRecordsPerBusinessUnit = 10000;

        /// <summary>
        /// Whether or not operations should continue if any errors are encountered.
        /// </summary>
        /// <remarks>
        /// This is different than setting maxFaultThreshold = 0, since the first batch of updates will be processed
        /// together. If continueOnError is true and maxFaultThreshold is 0, it is possible that multiple errors may
        /// be encountered and at the same time some records successfully updated. In a healthy system when updating
        /// a higher number of records, an occasional spurious error is expected, so it is recommended this be left as true.
        /// </remarks>
        const bool continueOnError = true;

        #region private variables
        private static Dictionary<string, EntityReference> cachedCompanyReferences = new Dictionary<string, EntityReference>();
        #endregion

        /// <summary>
        /// The main execution loop of the program.
        /// </summary>
        /// <param name="args">No arguments are expected.</param>
        static void Main(string[] args)
        {
            if (args.Length != 1 && args[0] != "-simulate" && args[0] != "-apply")
            {
                Console.WriteLine("Usage: BootstrapCompany -simulate");
                Console.WriteLine("       BootstrapCompany -apply");
                Console.WriteLine("The -simulate flag will create a file called simulation.csv in the working");
                Console.WriteLine("directory, but will not change any data. The -apply flag will update live data");
                Console.WriteLine("in the same way that was demonstrated in the simulation.");

                return;
            }

            bool isSimulate = args[0].Equals("-simulate", StringComparison.OrdinalIgnoreCase);

            // Delete the simulation or applied files if existing
            foreach (string existingSimulate in Directory.EnumerateFiles(Directory.GetCurrentDirectory(), $"{(isSimulate ? "simulation" : "applied")}_*.csv"))
            {
                File.Delete(existingSimulate);
            }

            IOrganizationService orgService;

            // TODO: Provide your connection string details for your environment
            CrmServiceClient cdsConnection = new CrmServiceClient("AuthType=Office365;Username=youraliashere@yourdomainhere.com;Password=yourpasswordhere;URL=https://yourorganizationurlhere.crm.dynamics.com/;");
            orgService = (IOrganizationService)cdsConnection.OrganizationWebProxyClient != null ? (IOrganizationService)cdsConnection.OrganizationWebProxyClient : (IOrganizationService)cdsConnection.OrganizationServiceProxy;

            if (orgService != null)
            {
                // Get the current user ID to verify the connection was successful
                Guid userid = ((WhoAmIResponse)orgService.Execute(new WhoAmIRequest())).UserId;

                if (userid != Guid.Empty)
                {
                    Console.WriteLine("Connection Successful!");
                }

                // TODO: Provide a mapping of OwningBusinessUnit name to cdm_Company company ID. You can reuse
                // the same company ID for multiple business units if desired. In this example, it assumes that
                // the business unit named "USMF" is related to the company "USMF". If all records were owned
                // by the same root business unit, then the first field in the dictionary should be set to the 
                // name of the root business unit, usually the same value as the organization (eg, "Contoso").
                Dictionary<string, string> businessUnitToCompanyMapping = new Dictionary<string, string>()
                {
                    { "", "USMF" }, // The default mapping to use for any entity that doesn't have an owningbusinessunit field
                    { "USMF", "USMF" },
                    { "FRRT", "FRRT" },
                };

                // TODO: Provide a list of entities for which the company field should be backfilled based
                // on owning business unit. The list below represents all existing entities for which a cdm_Company
                // lookup field was added as part of the Finance and Operations dual write project.
                BatchUpdateEntity(orgService, "account", "msdyn_company", businessUnitToCompanyMapping, true, isSimulate, "accountnumber", "name");
                BatchUpdateEntity(orgService, "contact", "msdyn_company", businessUnitToCompanyMapping, true, isSimulate, "fullname");
                // ... Add more here

                // Note, the product entity does not have an owningbusinessunit field like most other entities, so
                // assigning company by Business Unit is not applicable. In this case, whichever mapping specifies an
                // empty business unit will be used to categorize entities without an owningbusinessunit field.
                BatchUpdateEntity(orgService, "product", "msdyn_companyid", businessUnitToCompanyMapping, false, isSimulate, "productnumber");
            }
            else
            {
                Console.WriteLine("Connection failed...");
            }

            Console.WriteLine("Done");
            Console.ReadLine();
        }

        /// <summary>
        /// Updates all incorrectly assigned company relationships for the specified entity.
        /// </summary>
        /// <param name="orgService">The connection to CDS.</param>
        /// <param name="entityName">The logical name of the entity to update.</param>
        /// <param name="companyFieldName">The physical name of the field in the entity being updated which contains the cdm_Company id.</param>
        /// <param name="businessUnitToCompanyMapping">A dictionary of business unit name to company code.</param>
        /// <param name="hasOwningBusinessUnit">true if the entity has an owningbusinessunit field; otherwise, false.</param>
        /// <param name="isSimulate">true to simulate output; otherwise, false.</param>
        /// <param name="fieldsToExport">A set of fields to export into a CSV for this entity if simulating.</param>
        /// <returns>true if the entity was successfully processed without any errors; otherwise, false.</returns>
        private static bool BatchUpdateEntity(
            IOrganizationService orgService, 
            string entityName, 
            string companyFieldName, 
            Dictionary<string, string> businessUnitToCompanyMapping, 
            bool hasOwningBusinessUnit, 
            bool isSimulate, 
            params string[] fieldsToExport)
        {
            List<Guid> faultedIds = new List<Guid>();
            int totalRecordsProcessed = 0;
            Stopwatch stopwatch = new Stopwatch();
            stopwatch.Start();

            string fileName = isSimulate ? "simulation" : "applied";
            StreamWriter simulationWriter = new StreamWriter(Path.Combine(Directory.GetCurrentDirectory(), $"{fileName}_{entityName}.csv"), true);
            simulationWriter.Write("EntityName,EntityId,");
            foreach (string fieldToExport in fieldsToExport)
            {
                simulationWriter.Write($"{fieldToExport},");
            }
            simulationWriter.WriteLine("BusinessUnit,NewCompanyId");

            // Process each mapped business unit individually
            foreach (string businessUnitName in businessUnitToCompanyMapping.Keys)
            {
                Console.WriteLine("Updating any {0} records for business unit {1} to company {2}...", entityName, businessUnitName, businessUnitToCompanyMapping[businessUnitName]);

                // The empty business unit value is only applicable for entities without an owning business unit field
                if (hasOwningBusinessUnit && string.IsNullOrEmpty(businessUnitName))
                {
                    continue;
                }
                else if (!hasOwningBusinessUnit && !string.IsNullOrEmpty(businessUnitName))
                {
                    continue;
                }

                var companyRef = GetCompanyReference(orgService, businessUnitToCompanyMapping[businessUnitName]);

                // Iteratively loop in batches to keep transaction lock size small
                bool moreRecordsExist = true;

                while (moreRecordsExist)
                {
                    moreRecordsExist = false;

                    // Find the first batch of records for this business unit with the wrong company ID. Ordering
                    // is not explicity specified, but SQL will most likely process based on the index starting with
                    // company ID, since all new company ID fields added for Finance and Operations integration have
                    // also added a new index starting with company ID. Explicitly specifying order would reduce the
                    // query plan options for SQL and introduce unnecessary overhead.
                    QueryExpression query = new QueryExpression(entityName);
                    query.ColumnSet.AddColumns(companyFieldName);
                    foreach (string fieldToExport in fieldsToExport)
                    {
                        query.ColumnSet.AddColumn(fieldToExport);
                    }
                    query.Criteria.AddCondition(companyFieldName, ConditionOperator.NotEqual, companyRef.Id);

                    // TODO: Uncomment the line below if you only want to fill in companies that are empty
                    // as opposed to the line above which updates the company any time it differs from the 
                    // desired value
                    // query.Criteria.AddCondition(companyFieldName, ConditionOperator.Equal, Guid.Empty);

                    if (isSimulate)
                    {
                        // During simulation, get as a single block of records to avoid positioning complexities
                        query.TopCount = maxSimulateRecordsPerBusinessUnit;
                    }
                    else
                    {
                        // Only batch records during actual application, otherwise retrieve all as a single operation
                        query.TopCount = requestBatchSize + faultedIds.Count;
                    }

                    // For entities with an owning business unit, join based on business unit name
                    if (hasOwningBusinessUnit)
                    {
                        // TODO: Replace this logic with different algorithms to determine the correct company
                        // in situations where business unit is not the best way to categorize.
                        LinkEntity linkEntity = query.AddLink("businessunit", "owningbusinessunit", "businessunitid", JoinOperator.Inner);
                        linkEntity.Columns.AddColumns("name");
                        linkEntity.LinkCriteria.AddCondition("name", ConditionOperator.Equal, businessUnitName);
                    }

                    var multipleRequest = new ExecuteMultipleRequest()
                    {
                        Settings = new ExecuteMultipleSettings()
                        {
                            ContinueOnError = true,
                            ReturnResponses = true
                        },
                        Requests = new OrganizationRequestCollection()
                    };

                    EntityCollection result = orgService.RetrieveMultiple(query);

                    int recordsAddedToBatch = 0;

                    foreach (var entity in result.Entities)
                    {
                        // Skip any previously faulted ID's. These values will be re-queried with each batch
                        // which is inefficient, but is more efficient than passing hundreds of ID values to 
                        // the underlying SQL query to be skipped at the database level (assuming the 
                        // max fault count is relatively small).
                        if (faultedIds.Contains(entity.Id))
                        {
                            continue;
                        }

                        entity.Attributes[companyFieldName] = companyRef;
                        
                        UpdateRequest updateRequest = new UpdateRequest()
                        {
                            Target = entity
                        };

                        simulationWriter.Write($"{entityName},{entity.Id},");
                        foreach (string fieldToExport in fieldsToExport)
                        {
                            simulationWriter.Write($"{entity.Attributes[fieldToExport]},");
                        }
                        simulationWriter.WriteLine($"{businessUnitName},{businessUnitToCompanyMapping[businessUnitName]}");

                        // Only add the update request when applying for real
                        if (!isSimulate)
                        {
                            multipleRequest.Requests.Add(updateRequest);
                        }

                        recordsAddedToBatch++;
                        Console.Write(".");
                    }

                    totalRecordsProcessed += recordsAddedToBatch;

                    if (recordsAddedToBatch > 0 && !isSimulate)
                    {
                        Console.Write("Sending {0} updates in a batch", recordsAddedToBatch);
                        var updateResult = orgService.Execute(multipleRequest) as ExecuteMultipleResponse;
                        moreRecordsExist = true;
                        Console.WriteLine(" done");

                        // If any faults are encountered, flag those IDs to not be processed again
                        // in subsequent batches.
                        if (updateResult.IsFaulted)
                        {
                            foreach (var response in updateResult.Responses)
                            {
                                if (response.Fault != null)
                                {
                                    Console.WriteLine(response.Fault);
                                    faultedIds.Add(((UpdateRequest)multipleRequest.Requests[response.RequestIndex]).Target.Id);

                                    if (faultedIds.Count > 100)
                                    {
                                        throw new ApplicationException("Excessive number of update failures, aborting operation");
                                    }
                                }
                            }
                        }
                    }
                    else
                    {
                        Console.WriteLine("No {0} records remain to be updated for {1}->{2}", entityName, businessUnitName, businessUnitToCompanyMapping[businessUnitName]);
                    }
                }
            }

            simulationWriter.Close();
            simulationWriter = null;

            stopwatch.Stop();
            Console.WriteLine("Processed {0} records for the {1} entity in {2}ms.", totalRecordsProcessed, entityName, stopwatch.ElapsedMilliseconds);

            return (faultedIds.Count == 0);
        }

        /// <summary>
        /// Gets an entity reference to the company with the specified ID if one exists.
        /// </summary>
        /// <param name="orgService">The CDS connection.</param>
        /// <param name="companyId">The company ID to search for.</param>
        /// <returns>An entity reference if one exists; otherwise, null.</returns>
        private static EntityReference GetCompanyReference(IOrganizationService orgService, string companyId)
        {
            if (cachedCompanyReferences.ContainsKey(companyId))
            {
                return cachedCompanyReferences[companyId];
            }

            QueryExpression query = new QueryExpression("cdm_company");
            query.ColumnSet.AddColumns("cdm_companyid");
            query.Criteria.AddCondition("cdm_companycode", ConditionOperator.Equal, companyId);
            query.TopCount = 1;

            EntityCollection result = orgService.RetrieveMultiple(query);

            EntityReference entityRef = null;

            foreach (var entity in result.Entities)
            {
                entityRef = entity.ToEntityReference();
                break;
            }

            cachedCompanyReferences[companyId] = entityRef;

            return entityRef;
        }
    }
}

 ```
 
 
