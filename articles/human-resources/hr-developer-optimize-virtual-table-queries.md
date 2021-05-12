---
title: Virtuelle Dataverse-Tabellenabfragen optimieren
description: Optimieren und Behandeln von Leistungsproblemen bei virtuellen Dataverse-Tabellenabfragen
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8026abd5c3e0f9b78e8c016731fd7785490bc945
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891101"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="51bf3-103">Virtuelle Dataverse-Tabellenabfragen optimieren</span><span class="sxs-lookup"><span data-stu-id="51bf3-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="51bf3-104">Abgang</span><span class="sxs-lookup"><span data-stu-id="51bf3-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="51bf3-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="51bf3-105">Overview</span></span>

<span data-ttu-id="51bf3-106">Beim Benutzen von virtuellen Dataverse-Tabellen zum Entwickeln von Integrationen und anderen Datenverbindungen mit Dynamics 365 Human Resources können bei Abfragen der virtuellen Tabellen Leistungsprobleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="51bf3-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="51bf3-107">Die langsame Abfrageausführung kann über verschiedene Clients oder Schnittstellen hinweg erfolgen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="51bf3-108">Beispielsweise kann das Problem in den folgenden Umständen auftreten:</span><span class="sxs-lookup"><span data-stu-id="51bf3-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="51bf3-109">Bei der Abfrage einer virtuellen Tabelle über die Dataverse-Web-API</span><span class="sxs-lookup"><span data-stu-id="51bf3-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="51bf3-110">Beim Erstellen einer Power-App für eine virtuelle Tabelle</span><span class="sxs-lookup"><span data-stu-id="51bf3-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="51bf3-111">Beim Erstellen eines Power BI-Berichts über eine virtuelle Tabelle</span><span class="sxs-lookup"><span data-stu-id="51bf3-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="51bf3-112">Alle diese Schnittstellen können das Leistungsproblem auslösen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="51bf3-113">Eine Ursache für eine langsame Leistung mit virtuellen Dataverse-Tabellen für die Personalabteilung sind die Fremdschlüsselspalten der virtuellen Tabelle, die sich auf die [Navigationseigenschaften](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) der Tabelle beziehen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="51bf3-114">Wenn Navigationseigenschaften für eine virtuelle Tabelle erstellt werden, wird der Tabelle automatisch eine Fremdschlüsselspalte hinzugefügt, um den Wert des Schlüssels für die Schlüsselspalte der zugehörigen virtuellen Tabelle darzustellen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="51bf3-115">Die Spalte **_mshr_fk_Person_id_value** wird zum Beispiel der Entität **mshr_hcmworkerbaseentity** mit der Fremdschlüsseleigenschaft aus der **mshr_dirpersonentity**-Entität hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51bf3-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="51bf3-116">Aufgrund der Art und Weise, wie die Werte für diese Fremdschlüsselspalten in einer Tabelle verwaltet werden, kann sich das Abrufen der Werte negativ auf die Leistung einer Abfrage für die virtuelle Tabelle auswirken.</span><span class="sxs-lookup"><span data-stu-id="51bf3-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="51bf3-117">Mögliche Symptome</span><span class="sxs-lookup"><span data-stu-id="51bf3-117">Potential symptoms</span></span>

<span data-ttu-id="51bf3-118">Diese Auswirkungen treten zum Beispiel möglicherweise bei Abfragen an die Arbeitskraft- Entität (**mshr_hcmworkerentity**) oder Basisarbeitskraft-Entität (**mshr_hcmworkerbaseentity**) auf.</span><span class="sxs-lookup"><span data-stu-id="51bf3-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="51bf3-119">Möglicherweise tritt das Leistungsproblem auf verschiedene Arten auf:</span><span class="sxs-lookup"><span data-stu-id="51bf3-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="51bf3-120">**Langsame Abfrageausführung**: Die Abfrage für die virtuelle Tabelle gibt möglicherweise die erwarteten Ergebnisse zurück, es dauert jedoch länger als erwartet, bis die Ausführung der Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="51bf3-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="51bf3-121">**Abfragetimeout**: Bei der Abfrage kann es zu einer Zeitüberschreitung kommen und der folgende Fehler wird zurückgeben: „Es wurde ein Token zum Aufrufen von Finance and Operations erhalten, aber Finance and Operations hat einen Fehler vom Typ InternalServerError zurückgegeben.“</span><span class="sxs-lookup"><span data-stu-id="51bf3-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="51bf3-122">**Unerwarteter Fehler**: Die Abfrage gibt möglicherweise einen Fehler vom Typ 400 mit der folgenden Meldung zurück: „Ein unerwarteter Fehler ist aufgetreten.“</span><span class="sxs-lookup"><span data-stu-id="51bf3-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Fehler vom Typ 400 bei der HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="51bf3-124">**Drosselung**: Die Abfrage kann die Serverressourcen überbeanspruchen, sodass es zu einer Drosselung kommt.</span><span class="sxs-lookup"><span data-stu-id="51bf3-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="51bf3-125">In diesem Fall gibt die Abfrage den folgenden Fehler zurück: „Es wurde ein Token zum Aufrufen von Finance and Operations erhalten, aber Finance and Operations hat einen Fehler vom Typ 429 zurückgegeben.“</span><span class="sxs-lookup"><span data-stu-id="51bf3-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="51bf3-126">Weitere Informationen zur Drosselung in Humen Resources finden Sie unter [Drosselung – Häufig gestellte Fragen](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="51bf3-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Fehler vom Typ 429 bei der HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="51bf3-128">Lösung</span><span class="sxs-lookup"><span data-stu-id="51bf3-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="51bf3-129">Begrenzen Sie die Anzahl der Spalten, die in Ihrer Datenabfrage enthalten sind</span><span class="sxs-lookup"><span data-stu-id="51bf3-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="51bf3-130">Bei virtuellen Tabellen ist eine der Methoden mit dem größten Potenzial zur Verbesserung der Abfrageleistung die Begrenzung der Anzahl der für die Abfrage ausgewählten Spalten.</span><span class="sxs-lookup"><span data-stu-id="51bf3-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="51bf3-131">Die allgemeine Anleitung zur Optimierung der Abfrageleistung besteht darin, die in Ihrer Abfrage zurückgegebenen Spalten nur auf die Eigenschaften zu beschränken, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="51bf3-132">Dies gilt insbesondere für die Fremdschlüsselspalten in virtuellen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="51bf3-133">Wenn Sie die Werte in den Fremdschlüsselspalten für Ihre Integration oder Ihren Bericht nicht benötigen, strukturieren Sie die Abfrage so, dass nur die Spalten ausgewählt werden, die Sie benötigen, und die Fremdschlüsselspalten ausschließen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="51bf3-134">Spalten in einer OData-Abfrage auswählen</span><span class="sxs-lookup"><span data-stu-id="51bf3-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="51bf3-135">Bei der Abfrage einer virtuellen Tabelle über Dataverse-Web-API können Sie die Anzahl der in der Abfrage enthaltenen Spalten mithilfe der **$select**-Systemabfrageoption begrenzen und die Spalten definieren, für die Ergebnisse zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="51bf3-136">Um die Leistung zu maximieren, schließen Sie Fremdschlüsselspalten aus der Abfrage aus (mit dem Präfix **_mshr_FK_**).</span><span class="sxs-lookup"><span data-stu-id="51bf3-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="51bf3-137">Die folgende Abfrage der **mshr_hcmworkerbaseentity**-Entität enthält zum Beispiel nur die Spalten, die in der **$select**-Abfrageoptionsklausel enthalten sind; die Fremdschlüsselwerte sind ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="51bf3-138">Dies bietet eine erhebliche Leistungsverbesserung gegenüber einer Abfrage, die alle Tabellenspalten enthält.</span><span class="sxs-lookup"><span data-stu-id="51bf3-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="51bf3-139">Die Empfehlung, die Anzahl der ausgewählten Spalten zu begrenzen, gilt auch bei Verwendung der Abfrageoption **$expand** zum Erweitern der Abfrage auf dazugehörige virtuelle Tabellen über Navigationseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51bf3-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="51bf3-140">Die folgende Abfrage enthält beispielsweise Spalten aus der **mshr_hcmworkerbaseentity**-Entität mit erweiterten Spalten aus der **mshr_dirpersonentity**-Entität.</span><span class="sxs-lookup"><span data-stu-id="51bf3-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="51bf3-141">Bitte beachten Sie, dass die **$select**-Abfrageoption auch in der **$expand**-Abfrageoptionsklausel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="51bf3-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="51bf3-142">Wenn Sie diese Methode zum Abrufen von Daten mit der Abfrageoption **$select** in der Abfrageoptionsklausel **$expand** verwenden, werden in der Regel größere Leistungsverbesserungen festgestellt, wenn die Navigationseigenschaft zwischen den Entitäten eine n:1-Beziehung ist.</span><span class="sxs-lookup"><span data-stu-id="51bf3-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="51bf3-143">Eventuell stellen Sie beim Erweitern einer 1:n-Beziehung nicht dieselbe Verkürzung der Ausführungszeit für Abfragen fest.</span><span class="sxs-lookup"><span data-stu-id="51bf3-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="51bf3-144">Weitere Informationen zur Beziehungsdefinition für virtuelle Dataverse-Tabellen finden Sie unter [Tabellenbeziehungen](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="51bf3-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="51bf3-145">Weitere Informationen zur Verwendung der Systemabfrageoptionen **$select** und **$expand** in der Dataverse-Web-API finden Sie unter [Dazugehörige Entitätsdatensätze mit einer Abfrage abrufen](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="51bf3-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="51bf3-146">Spalten in Power BI auswählen</span><span class="sxs-lookup"><span data-stu-id="51bf3-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="51bf3-147">Wenn Sie beim Erstellen eines Power BI-Bericht für eine virtuelle Dataverse-Tabelle eines der oben genannten Anzeichen einer langsamen Leistung feststellen, können Sie die Leistung verbessern, indem Sie Fremdschlüsselspalten von den Spalten ausschließen, die in der Tabelle für den Bericht ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="51bf3-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="51bf3-148">Wenn Sie zum Beispiel Power BI Desktop verwenden, um einen Bericht für die Entität **mshr_hcmworkerbaseentity** zu erstellen, können Sie die folgenden Schritte ausführen, um die Spalten auszuwählen, die in die Berichtsabfrage enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="51bf3-149">Wählen Sie im Power BI Desktop **Mehr ...** in der Dropdownliste auf dem Aktionsband **Daten abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="51bf3-150">Geben Sie in dem Fenster **Daten abrufen** **Common Data Service** in das Suchfeld ein, wählen Sie den Connector **Common Data Service** und dann **Verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="51bf3-151">Geben Sie im Feld **Server-URL** des Common Data Service-Fensters die Organisations-URI für Ihre Dataverse-Umgebung ein und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="51bf3-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Die URI für Ihre Dataverse-Umgebung eingeben](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="51bf3-153">Erweitern Sie im Navigator-Fenster den Knoten **Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="51bf3-154">Geben Sie im Suchfeld **mshr_hcmworkerbaseentity** ein und wählen Sie die Entität aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="51bf3-155">Wählen Sie **Daten transformieren** aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="51bf3-156">Wählen Sie im Fenster des Power Query-Editor die Option **Erweiterter Editor** aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="51bf3-157">Aktualisieren Sie im **Erweiterten Editor** die Abfrage so, dass sie wie folgt aussieht, und fügen Sie dem Array Spalten nach Bedarf hinzu oder entfernen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="51bf3-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Die Abfrage im erweiterten Editor des Power Query-Editor aktualisieren](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="51bf3-159">Wählen Sie **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="51bf3-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="51bf3-160">Wenn Sie vor dem Aktualisieren einen Fehler vom Typ 429 von der Abfrage erhalten haben, müssen Sie möglicherweise die Wiederholungsperiode abwarten, bevor Sie die Abfrage aktualisieren, damit sie erfolgreich abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="51bf3-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="51bf3-161">Klicken Sie im Aktionsband des Power Query-Editors auf **Schließen & Übernehmen**.</span><span class="sxs-lookup"><span data-stu-id="51bf3-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="51bf3-162">Sie können dann mit dem Aufbau Ihres Power BI-Berichts für die aus der virtuellen Tabelle ausgewählten Spalten beginnen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="51bf3-163">Spalten in Power Apps auswählen</span><span class="sxs-lookup"><span data-stu-id="51bf3-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="51bf3-164">Ähnlich wie bei Dataverse Web-API-Abfragen und Power BI können Sie die Abfrageleistung für Power Apps basierend auf virtuellen Dataverse-Tabellen verbessern, indem Sie Spalten dazugehöriger Tabellen aus Ihrer App ausschließen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="51bf3-165">Wenn Spalten aus einer dazugehörigen Tabelle auf einer Seite enthalten sind, enthält die zum Abrufen der Daten erstellte Anforderungs-URL Fremdschlüsseleigenschaften der zugehörigen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="51bf3-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="51bf3-166">Wie in den Beispielen von [Spalten in einer OData-Abfrage auswählen](#selecting-columns-in-power-apps) oben, reduziert dies die Leistung, indem zusätzliche Datensuchen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="51bf3-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="51bf3-167">Um dies zu umgehen, können Sie sicherstellen, dass in keinem Datenformular Ihrer Power App Datenfelder aus dazugehörigen Tabellen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="51bf3-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="51bf3-168">Wählen Sie im Bereich der Strukturansicht das Datenformular für die Anzeige aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="51bf3-169">Wählen Sie im Bereich **Eigenschaften** **Bearbeiten** in der Eigenschaft **Felder** aus.</span><span class="sxs-lookup"><span data-stu-id="51bf3-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="51bf3-170">Stellen Sie im Bereich **Daten** sicher, dass keines der ausgewählten Felder zur virtuellen Tabelle der Datenquelle gehört.</span><span class="sxs-lookup"><span data-stu-id="51bf3-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="51bf3-171">Wenn beispielsweise eines der auf einer Seite in der App enthaltenen Datenfelder auf eine andere Tabelle, wie **ThisItem.Worker.Name** verweist, wo **Arbeitskraft** die dazugehörige Tabelle ist, besteht die Möglichkeit, dass die Leistung beim Abrufen der Daten geringer ist.</span><span class="sxs-lookup"><span data-stu-id="51bf3-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="51bf3-172">Sie können den [Power Apps-Monitor](/powerapps/maker/monitor-overview) benutzen, um sicherzustellen, dass nur die Spalten, die Sie benötigen, in die Abfrage aufgenommen werden, um die Daten für die Power App abzurufen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="51bf3-173">Sie können die für den getRows-Vorgang erstellte URL anzeigen lassen, um sicherzustellen, dass die für Ihre App ausgewählten Spalten für das Abrufen der Daten optimal sind.</span><span class="sxs-lookup"><span data-stu-id="51bf3-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Den Power Apps-Monitor benutzen, um den getData-Vorgang zu analysieren](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="51bf3-175">Die Datenabfrage filtern</span><span class="sxs-lookup"><span data-stu-id="51bf3-175">Filtering the data query</span></span>

<span data-ttu-id="51bf3-176">Eine andere Methode zur Verbesserung der Leistung der Abfrageausführung besteht darin, die Anzahl der in den Abfrageergebnissen zurückgegebenen Datensätze zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="51bf3-177">Sie können dazu die Ergebnisse filtern, um sicherzustellen, dass Sie nur die Datensätze erhalten, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="51bf3-178">Weitere Informationen zum Filtern von Abfragedaten finden Sie unter [Ergebnisse filtern](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).</span><span class="sxs-lookup"><span data-stu-id="51bf3-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="51bf3-179">Die Seitengröße der Abfrage begrenzen</span><span class="sxs-lookup"><span data-stu-id="51bf3-179">Limiting the page size of the query</span></span>

<span data-ttu-id="51bf3-180">Wenn Sie mit großen Datenmengen arbeiten, können Sie die Abfrageergebnisse auf mehrere Seiten aufteilen, indem Sie die `odata.maxpagesize`-Präferenzkopfzeile zu Datenabfragen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="51bf3-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="51bf3-181">Weitere Informationen zur Seitenverwaltung finden Sie unter [Anzahl der Entitäten festlegen, die auf einer Seite zurückgegeben werden sollen](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="51bf3-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="51bf3-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51bf3-182">See also</span></span>

- [<span data-ttu-id="51bf3-183">Virtuelle Dataverse-Tabellen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="51bf3-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="51bf3-184">Virtuelle Human Resources-Tabellen – Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="51bf3-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="51bf3-185">Drosselung – Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="51bf3-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]