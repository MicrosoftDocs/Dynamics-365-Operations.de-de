---
title: "Konfigurationsschlüssel und Datenentitäten"
description: "In diesem Thema wird die Beziehung zwischen Konfigurationsschlüsseln und Datenentitäten in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, beschrieben."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: f9ea932b48d57baad4b4ab66069191ebd7cbbd6c
ms.contentlocale: de-de
ms.lasthandoff: 02/27/2018

---

# <a name="configuration-keys-and-data-entities"></a><span data-ttu-id="e69dc-103">Konfigurationsschlüssel und Datenentitäten</span><span class="sxs-lookup"><span data-stu-id="e69dc-103">Configuration keys and data entities</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e69dc-104">Bevor Sie Datenentitäten verwenden, um Daten zu importieren oder zu exportieren, wird empfohlen, dass sie zuerst die Auswirkung von Konfigurationsschlüsseln auf die Datenentitäten bestimmen, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e69dc-104">Before you use data entities to import or export data, we recommended that you first determine the impact of configuration keys on the data entities that you are planning to use.</span></span> 

<span data-ttu-id="e69dc-105">Weitere Informationen über Konfigurationsschlüssel in Finance and Operations finden Sie unter [Lizenzcodes und Konfigurationsschlüsselbericht](../sysadmin/license-codes-configuration-keys-report.md) Sie unter.</span><span class="sxs-lookup"><span data-stu-id="e69dc-105">To learn more about configuration keys in Finance and Operations, see the [License codes and configuration keys report](../sysadmin/license-codes-configuration-keys-report.md).</span></span>

### <a name="configuration-key-assignments"></a><span data-ttu-id="e69dc-106">Konfigurationsschlüsselzuweisungen</span><span class="sxs-lookup"><span data-stu-id="e69dc-106">Configuration key assignments</span></span>
<span data-ttu-id="e69dc-107">Konfigurationsschlüssel können einem oder allen folgenden Artefakten zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="e69dc-107">Configuration keys can be assigned to one or all of the following artifacts.</span></span>
-   <span data-ttu-id="e69dc-108">Datenentitäten</span><span class="sxs-lookup"><span data-stu-id="e69dc-108">Data entities</span></span>
-   <span data-ttu-id="e69dc-109">Tabellen, die als Datenquellen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e69dc-109">Tables used as data sources</span></span>
-   <span data-ttu-id="e69dc-110">Tabellenfelder</span><span class="sxs-lookup"><span data-stu-id="e69dc-110">Table fields</span></span>
-   <span data-ttu-id="e69dc-111">Datenentitätsfelder</span><span class="sxs-lookup"><span data-stu-id="e69dc-111">Data entity fields</span></span>

<span data-ttu-id="e69dc-112">In der folgenden Tabelle wird zusammengefasst, wie Konfigurationsschlüsselwerte zu verschiedenen Artefakten, die einem Objekt zugrunde liegen, das erwartete Verhalten des Objekts ändern.</span><span class="sxs-lookup"><span data-stu-id="e69dc-112">The following table summarizes how configuration key values on the different artifacts that underlie an object change the expected behavior of the object.</span></span>

| <span data-ttu-id="e69dc-113">Konfigurationsschlüsseleinstellung zu Datenentität</span><span class="sxs-lookup"><span data-stu-id="e69dc-113">Configuation key setting on data entity</span></span> | <span data-ttu-id="e69dc-114">Konfigurationsschlüsseleinstellung zu Tabelle</span><span class="sxs-lookup"><span data-stu-id="e69dc-114">Configuration key setting on table</span></span> | <span data-ttu-id="e69dc-115">Konfigurationsschlüsseleinstellung zu Tabellenfeld</span><span class="sxs-lookup"><span data-stu-id="e69dc-115">Configuration key setting on table field</span></span> | <span data-ttu-id="e69dc-116">Konfigurationsschlüssel zu Datenentitätsfeld</span><span class="sxs-lookup"><span data-stu-id="e69dc-116">Configuration key on data entity field</span></span> | <span data-ttu-id="e69dc-117">Erwartetes Verhalten</span><span class="sxs-lookup"><span data-stu-id="e69dc-117">Expected behavior</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------|-----------------------------|-----------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69dc-118">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-118">Disabled</span></span>                          | <span data-ttu-id="e69dc-119">Nicht bewertet</span><span class="sxs-lookup"><span data-stu-id="e69dc-119">Not evaluated</span></span>               | <span data-ttu-id="e69dc-120">Nicht bewertet</span><span class="sxs-lookup"><span data-stu-id="e69dc-120">Not evaluated</span></span>                     | <span data-ttu-id="e69dc-121">Nicht bewertet</span><span class="sxs-lookup"><span data-stu-id="e69dc-121">Not evaluated</span></span>                   | <span data-ttu-id="e69dc-122">Wenn der Konfigurationsschlüssel für die Datenentität deaktiviert ist, ist die Datenentität nicht funktionsbereit.</span><span class="sxs-lookup"><span data-stu-id="e69dc-122">If the configuration key for the data entity is disabled, the data entity will not be functional.</span></span> <span data-ttu-id="e69dc-123">Es spielt keine Rolle, ob die Konfigurationsschlüssel in den zugrunde liegenden Tabellen und Feldern aktiviert oder deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="e69dc-123">It does not matter whether the configuration keys in the underlying tables and fields are enabled or disabled.</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e69dc-124">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-124">Enabled</span></span>                           | <span data-ttu-id="e69dc-125">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-125">Disabled</span></span>                    | <span data-ttu-id="e69dc-126">Nicht bewertet</span><span class="sxs-lookup"><span data-stu-id="e69dc-126">Not evaluated</span></span>                     | <span data-ttu-id="e69dc-127">Nicht bewertet</span><span class="sxs-lookup"><span data-stu-id="e69dc-127">Not evaluated</span></span>                   | <span data-ttu-id="e69dc-128">Wenn der Konfigurationsschlüssel für eine Datenentität aktiviert ist, wird vom Datenverwaltungsframework der Konfigurationsschlüssel für jede der zugrunde liegenden Tabellen überprüft.</span><span class="sxs-lookup"><span data-stu-id="e69dc-128">If the configuration key for a data entity is enabled, the data management framework checks the configuration key on each of the underlying tables.</span></span> <span data-ttu-id="e69dc-129">Wenn der Konfigurationsschlüssel für eine Tabelle deaktiviert ist, ist diese Tabelle in der Datenentität für die funktionale Verwendung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e69dc-129">If the configuration key for a table is disabled, that table will not be available in the data entity for functional use.</span></span> <span data-ttu-id="e69dc-130">Wenn der Konfigurationsschlüssel einer Tabelle deaktiviert ist, werden die Tabellen- und Datenentitätskonfigurationsschlüsseleinstellungen nicht ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="e69dc-130">If a table's configuration key is disabled, the table and data entity configuration key settings are not evaluated.</span></span> <span data-ttu-id="e69dc-131">Wenn bei der primären Tabelle in der Entität ihr Konfigurationsschlüssel deaktiviert ist, verhält sich das System so, als ob der Konfigurationsschlüssel der Entität deaktiviert wäre.</span><span class="sxs-lookup"><span data-stu-id="e69dc-131">If the primary table in the entity has its configuration key disabled, then the system will act as though the entity’s configuration key were disabled.</span></span> |
| <span data-ttu-id="e69dc-132">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-132">Enabled</span></span>                           | <span data-ttu-id="e69dc-133">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-133">Enabled</span></span>                     | <span data-ttu-id="e69dc-134">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-134">Disabled</span></span>                          | <span data-ttu-id="e69dc-135">Nicht bewertet</span><span class="sxs-lookup"><span data-stu-id="e69dc-135">Not evaluated</span></span>                   | <span data-ttu-id="e69dc-136">Wenn der Konfigurationsschlüssel für eine Datenentität aktiviert ist und die Konfigurationsschlüssel der zugrunde liegenden Tabellen aktiviert sind, überprüft das Datenverwaltungsframework den Konfigurationsschlüssel für die Felder in den Tabellen.</span><span class="sxs-lookup"><span data-stu-id="e69dc-136">If the configuration key for a data entity is enabled, and the underlying tables configuration keys are enabled, the data management framework will check the configuration key on of the fields in the tables.</span></span> <span data-ttu-id="e69dc-137">Wenn der Konfigurationsschlüssel für ein Feld deaktiviert, ist dieses Feld in der Datenentität für die funktionale Verwendung selbst dann nicht verfügbar, wenn beim entsprechenden Datenentitätsfeld der Konfigurationsschlüssel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-137">If the configuration key for a field is disabled, that field will not be available in the data entity for functional use even if the corresponding data entity field has the configuration key enabled.</span></span>                                                                                                                                   |
| <span data-ttu-id="e69dc-138">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-138">Enabled</span></span>                           | <span data-ttu-id="e69dc-139">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-139">Enabled</span></span>                     | <span data-ttu-id="e69dc-140">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-140">Enabled</span></span>                           | <span data-ttu-id="e69dc-141">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="e69dc-141">Disabled</span></span>                        | <span data-ttu-id="e69dc-142">Wenn der Konfigurationsschlüssel auf allen anderen Ebenen aktiviert ist, aber der Konfigurationsschlüssel des Entitätsfelds nicht aktiviert ist, dann ist das Feld nicht für die Verwendung in der Datenentität verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e69dc-142">If the configuration key is enabled at all other levels, but the entity field configuration key is not enabled, then the field will not be available for use in the data entity.</span></span>                                                                                                                                                                                                                                                                                                                                                                          |

> [!NOTE]
> <span data-ttu-id="e69dc-143">Wenn eine Entität eine andere Entität als Datenquelle hat, dann wird die obige Semantik in rekursiver Weise angewendet.</span><span class="sxs-lookup"><span data-stu-id="e69dc-143">If an entity has another entity as a data source then, the above semantics are applied in a recursive manner.</span></span>

### <a name="entity-list-refresh"></a><span data-ttu-id="e69dc-144">Entitätslistenaktualisierung</span><span class="sxs-lookup"><span data-stu-id="e69dc-144">Entity list refresh</span></span>
<span data-ttu-id="e69dc-145">Wenn die Entitätsliste aktualisiert wird, werden vom Datenverwaltungsframework die Konfigurationsschlüsselmetadaten für die Laufzweitverwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-145">When the entity list is refreshed, the data management framework builds the configuration key metadata for runtime use.</span></span> <span data-ttu-id="e69dc-146">Diese Metadaten werden mithilfe der oben beschriebenen Logik erstellt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-146">This metadata is built using the logic described above.</span></span> <span data-ttu-id="e69dc-147">Vor der Verwendung von Einzelvorgängen und Entitäten im Datenverwaltungsframework wird dringend empfohlen, dass Sie warten, bis die Entitätslistenaktualisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-147">We strongly recommend that you  wait for the entity list refresh to complete before using jobs and entities in the data management framework.</span></span> <span data-ttu-id="e69dc-148">Wenn Sie nicht warten, sind die Konfigurationsschlüsselmetadaten möglicherweise nicht auf dem neuesten Stand und könnten unerwartete Ergebnisse hervorrufen.</span><span class="sxs-lookup"><span data-stu-id="e69dc-148">If you don't wait, the configuration key metadata may not be up to date and could result in unexpected outcomes.</span></span> <span data-ttu-id="e69dc-149">Wenn die Entitätsliste aktualisiert wird, wird die folgende Nachricht in der Entitätslistenseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-149">When the entity list is being refreshed, the following message is shown in the entity list page.</span></span>

![Entitätslistenaktualisierung](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a><span data-ttu-id="e69dc-151">Datenentitätslistenseite</span><span class="sxs-lookup"><span data-stu-id="e69dc-151">Data entity list page</span></span>
<span data-ttu-id="e69dc-152">Die Datenentitätslistenseite im Datenverwaltungsarbeitsbereich zeigt die Konfigurationsschlüsseleinstellungen für die Entitäten an.</span><span class="sxs-lookup"><span data-stu-id="e69dc-152">The data entity list page in the Data management workspace shows the configuration key settings for the entities.</span></span> <span data-ttu-id="e69dc-153">Beginnen Sie von dieser Seite, um die Auswirkungen von Konfigurationsschlüsseln auf die Datenentität zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="e69dc-153">Start from this page  to understand the impact from configuration keys on the data entity.</span></span>
<span data-ttu-id="e69dc-154">Diese Informationen werden mithilfe der Metadaten angezeigt, die während der Entitätsaktualisierung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e69dc-154">This information is shown using the metadata that is built during entity refresh.</span></span> <span data-ttu-id="e69dc-155">Die Konfigurationsschlüsselspalte zeigt den Namen des Konfigurationsschlüssels an, der der Datenentität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-155">The configuration key column shows the name of the configuration key that is associated with the data entity.</span></span> <span data-ttu-id="e69dc-156">Wenn diese Spalte leer ist, bedeutet dies, dass es keinen Konfigurationsschlüssel gibt, der der Datenentität zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-156">If this column is blank it means that there is no configuration key associated with the data entity.</span></span> <span data-ttu-id="e69dc-157">Die Konfigurationsschlüssel-Statusspalte zeigt den Status des Konfigurationsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="e69dc-157">The configuration key status column shows the state of the configuration key.</span></span> <span data-ttu-id="e69dc-158">Wenn sie ein Häkchen hat, bedeutet dies, dass der Schlüssel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-158">If it has a checkmark, it means the key is enabled.</span></span> <span data-ttu-id="e69dc-159">Wenn sie leer ist, bedeutet dies, dass entweder der Schlüssel deaktiviert ist, oder dass kein Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-159">If it is blank, it means either the key is disabled or there is no key associated.</span></span>

![Entitätslistenseite](./media/Data_entity_list_page.png)

### <a name="target-fields"></a><span data-ttu-id="e69dc-161">Zielfelder</span><span class="sxs-lookup"><span data-stu-id="e69dc-161">Target fields</span></span>
<span data-ttu-id="e69dc-162">Im nächsten Schritt wird ein Drillinto in die Datenentität ausgeführt, um die Auswirkung der Konfigurationsschlüssel auf Tabellen und Felder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e69dc-162">The next step is to drill into the data entity to view the impact of configuration keys on tables and fields.</span></span> <span data-ttu-id="e69dc-163">Das Zielfelderformular für eine Datenentität zeigt Konfigurationsschlüssel und Schlüsselstatusinformationen für die zugeordneten Tabellen und Felder in der Datenentität an.</span><span class="sxs-lookup"><span data-stu-id="e69dc-163">The target fields form for a data entity shows configuration key and the key status information for the related tables and fields in the data entity.</span></span>  <span data-ttu-id="e69dc-164">Wenn bei der Datenentität selbst ihr Konfigurationsschlüssel deaktiviert ist, wird eine Warnmeldung angezeigt, um zu informieren, dass die Tabellen und Felder im Zielfelderformular für diese Entität überhaupt nicht verfügbar sein werden, ungeachtet ihres Konfigurationsschlüsselstatus.</span><span class="sxs-lookup"><span data-stu-id="e69dc-164">If the data entity itself has its configuration key disabled, a warning message is shown informing that the tables and fields in the target fields form for this entity will not be available at all regardless of their configuration key status.</span></span>

![Zielfelder](./media/Target_fields_1.png)

### <a name="child-entities"></a><span data-ttu-id="e69dc-166">Untergeordnete Entitäten</span><span class="sxs-lookup"><span data-stu-id="e69dc-166">Child entities</span></span> 
<span data-ttu-id="e69dc-167">Bestimmte Entitäten haben andere Entitäten als Datenquellen oder sind zusammengesetzte Datenentitäten: Konfigurationsschlüsselinformationen für diese Entitäten werden im Formular für untergeordnete Entitäten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-167">Certain entities have other entities as data sources, or are composite data entities: configuration key information for these entities is shown in the Child entities form.</span></span> <span data-ttu-id="e69dc-168">Verwenden Sie dieses Formular in ähnlicher Weise wie die oben beschriebene Entitätenlistenseite.</span><span class="sxs-lookup"><span data-stu-id="e69dc-168">Use this form in the similar way to the entities list page described above.</span></span> <span data-ttu-id="e69dc-169">Das Zielfelderformular für die untergeordnete Entität verhält sich auch wie das, was oben beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e69dc-169">The target fields form for the child entity also behaves like what is described above.</span></span>

![Zielfelder](./media/Target_fields_2.png)

### <a name="using-data-entities"></a><span data-ttu-id="e69dc-171">Datenentitäten verwenden</span><span class="sxs-lookup"><span data-stu-id="e69dc-171">Using data entities</span></span>
<span data-ttu-id="e69dc-172">Nachdem Sie die gesamte Auswirkung – sofern es eine gibt – von Konfigurationsschlüsseln auf die Datenentitäten verstehen, die Sie verwenden möchten, können Sie jetzt damit fortfahren, die Datenentitäten zu verwenden, indem Sie diese zu Datenprojekten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e69dc-172">After understanding the full impact, if any, of configuration keys on the data entities that you would like to use, you can now proceed to using the data entities by adding them to data projects.</span></span> 

### <a name="run-time-validations-for-configuration-keys"></a><span data-ttu-id="e69dc-173">Laufzeitüberprüfungen für Konfigurationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="e69dc-173">Run time validations for configuration keys</span></span>
<span data-ttu-id="e69dc-174">Mithilfe der Konfigurationsschlüsselmetadaten, die während der Entitätsaktualisierungsliste erstellt werden, werden Laufzeitüberprüfungen in den folgenden Anwendungsfällen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-174">Using the configuration key metadata built during entity refresh list, run time validations are performed in the following use cases.</span></span>

-   <span data-ttu-id="e69dc-175">Wenn eine Datenentität einem Einzelvorgang hinzugefügt wird</span><span class="sxs-lookup"><span data-stu-id="e69dc-175">When a data entity is added to a job</span></span>

-   <span data-ttu-id="e69dc-176">Wenn Benutzer auf „überprüfen” auf der Entitätsliste klicken</span><span class="sxs-lookup"><span data-stu-id="e69dc-176">When user clicks ‘validate’ on the entity list</span></span>

-   <span data-ttu-id="e69dc-177">Wenn der Benutzer ein Datenpaket in ein Datenprojekt lädt</span><span class="sxs-lookup"><span data-stu-id="e69dc-177">When the user loads a data package into a data project</span></span>

-   <span data-ttu-id="e69dc-178">Wenn der Benutzer eine Vorlage in ein Datenprojekt lädt</span><span class="sxs-lookup"><span data-stu-id="e69dc-178">When the user loads a template into a data project</span></span>

-   <span data-ttu-id="e69dc-179">Wenn ein vorhandenes Datenprojekt geladen wird</span><span class="sxs-lookup"><span data-stu-id="e69dc-179">When an existing data project is loaded</span></span>

-   <span data-ttu-id="e69dc-180">Wenn eine Vorlage in ein Datenprojekt geladen wird</span><span class="sxs-lookup"><span data-stu-id="e69dc-180">When a template is loaded into a data project</span></span>

-   <span data-ttu-id="e69dc-181">Bevor der Export-/Importeinzelvorgang ausgeführt wird (Charge, Nicht-Charge, wiederkehrend, Odata)</span><span class="sxs-lookup"><span data-stu-id="e69dc-181">Before the export/import job is executed (batch, non-batch, recurring, Odata)</span></span>

-   <span data-ttu-id="e69dc-182">Wenn der Benutzer eine Zuordnung generiert</span><span class="sxs-lookup"><span data-stu-id="e69dc-182">When the user generates mapping</span></span>

-   <span data-ttu-id="e69dc-183">Wenn der Benutzer Felder in die Zuordnungsbenutzeroberfläche zuordnet</span><span class="sxs-lookup"><span data-stu-id="e69dc-183">When the user maps fields in the mapping UI</span></span>

-   <span data-ttu-id="e69dc-184">Wenn der Benutzer nur „importierbare Felder” hinzufügt</span><span class="sxs-lookup"><span data-stu-id="e69dc-184">When the user adds only 'importable fields'</span></span>


### <a name="managing-configuration-key-changes"></a><span data-ttu-id="e69dc-185">Konfigurationsschlüsseländerungen verwalten</span><span class="sxs-lookup"><span data-stu-id="e69dc-185">Managing configuration key changes</span></span>
<span data-ttu-id="e69dc-186">Immer wenn Sie Konfigurationsschlüssel auf der Entitäts-, Tabellen- oder Feldebene aktualisieren, muss die Entitätsliste im Datenverwaltungsframework aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e69dc-186">Anytime that you update configuration keys at the entity, table or field level, the entity list in the data management framework must be refreshed.</span></span> <span data-ttu-id="e69dc-187">Durch diesen Prozess wird sichergestellt, dass der Framework die aktuellsten Konfigurationsschlüsseleinstellungen auswählt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-187">This process ensures that the framework picks up the latest configuration key settings.</span></span> <span data-ttu-id="e69dc-188">Bis die Entitätsliste aktualisiert ist, wird die folgende Warnung in der Entitätslistenseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e69dc-188">Until the entity list is refreshed, the following warning will be shown in the entity list page.</span></span> <span data-ttu-id="e69dc-189">Die aktualisierten Konfigurationsschlüsseländerungen treten sofort in Kraft, nachdem die Entitätsliste aktualisiert ist.</span><span class="sxs-lookup"><span data-stu-id="e69dc-189">The updated configuration key changes will take effect immediately after the entity list is refreshed.</span></span> <span data-ttu-id="e69dc-190">Es wird empfohlen, dass Sie die vorhandenen Datenprojekte und Einzelvorgänge überprüfen, um sicherzustellen, dass sie erwartungsgemäß funktionieren, nachdem die Konfigurationsschlüsseländerungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="e69dc-190">We recommend that you validate existing data projects and jobs to make sure that they function as expected after the configuration keys changes are put in effect.</span></span>

![Zielfelder](./media/Target_fields_3.png)

