---
title: Bereiten Sie anwendungsspezifische Metadaten für RCS und ER vor
description: In diesem Thema wird erläutert, wie anwendungsspezifische Metadaten für Regulatory Configuration Service (RCS) und elektronische Berichterstellung (ER) vorbereitet werden.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a540676ba11bc3c0fb7855a2fdaff998819dfbe
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849684"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="7fc76-103">Vorbereiten anwendungsspezifischer Metadaten für RCS</span><span class="sxs-lookup"><span data-stu-id="7fc76-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7fc76-104">Dieses Thema führt Sie durch Beispiele der folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="7fc76-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="7fc76-105">Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS</span><span class="sxs-lookup"><span data-stu-id="7fc76-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="7fc76-106">Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7fc76-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="7fc76-107">Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7fc76-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="7fc76-108">Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS</span><span class="sxs-lookup"><span data-stu-id="7fc76-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="7fc76-109">Die folgenden Prozedur zeigt, wie ein Finance and Operations-Benutzer mit der **Systemadministrator**- oder der **Elektronische Berichtsentwickler**-Rolle eine elektronische Berichterstellungskonfiguration (ER) erstellen kann, die die Metadaten für die Microsoft Dynamics 365 for Finance and Operations-Anwendung enthält und für das Entwerfen der ER-Modellzuordnungskonfigurationen im Regulatory Configuration Service (RCS) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fc76-109">The following procedure shows how a user of Finance and Operations who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the Microsoft Dynamics 365 for Finance and Operations application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="7fc76-110">Die Beispiel-ER-Modellzuordnungskonfiguration, die in diesem Beispiel erstellt wird, wird verwendet, um auf Außenhandelsbuchungen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="7fc76-111">In diesem Beispiel verwenden Sie RCS um eine ER-Lösung für eine Finance and Operations zu entwerfen, die verwendet wird, um elektronische Dokumente zu erstellen, die Informationen aus der Außenhandelsgeschäftsdomäne enthält.</span><span class="sxs-lookup"><span data-stu-id="7fc76-111">For this example, you want to use RCS to design an ER solution for Finance and Operations that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="7fc76-112">Um die Zuordnung zwischen dem ER-Datenmodell und den Quellen der erforderlichen Daten anzugeben, müssen Sie Zugriff auf die Anwendungs-Metadaten für Finance and Operations in RCS haben.</span><span class="sxs-lookup"><span data-stu-id="7fc76-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata for Finance and Operations in RCS.</span></span> <span data-ttu-id="7fc76-113">Daher konfigurieren müssen Sie als Teil des Entwurfsprozesses der ER-Lösung eine neue ER-Metadatenkonfiguration konfigurieren, die alle Metadaten enthält, die zur Generierung der ER-Berichte für ausgewählte Geschäftsdomänen derzeit erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7fc76-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="7fc76-114">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc76-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="7fc76-115">Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="7fc76-116">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="7fc76-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="7fc76-117">Wenn Sie diesen Konfigurationsanbieter nicht sehen, schließen Sie die Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) ab.</span><span class="sxs-lookup"><span data-stu-id="7fc76-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="7fc76-118">Wählen Sie **Metadatenkonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="7fc76-119">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="7fc76-120">Geben Sie im Drop-Down-Dialogfeld im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="7fc76-121">In vorliegenden Beispiel geben Sie **Außenhandelmetadaten** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="7fc76-122">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="7fc76-123">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-123">Select **Designer**.</span></span>
8. <span data-ttu-id="7fc76-124">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fc76-125">Sie können alle Metadaten entweder für die gesamte Anwendung, oder für ausgewählte Modelle oder Module auswählen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="7fc76-126">Beachten Sie In beiden Fällen, dass die folgenden Metadaten automatisch hinzugefügt werden: Tabellen von Datensätzen, Aufzählungen und erweiterte Datentypen (EDTs).</span><span class="sxs-lookup"><span data-stu-id="7fc76-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="7fc76-127">Wenn zusätzliche Arten von Metadaten erforderlich sind, müssen sie ggf. manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc76-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="7fc76-128">Sie müssen einige zum Außenhandel zugehörige Metadaten hinzufügen und manuell Metadatenelemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="7fc76-129">Wählen Sie **Datenquelle hinzufügen \> Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="7fc76-130">Filtern Sie auf Wert von **Intrastat** im Feld **Name**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="7fc76-131">Wählen Sie den **Intrastat**-Tabellendatensatz aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="7fc76-132">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-132">Select **OK**.</span></span>

<span data-ttu-id="7fc76-133">Sie müssen Metadateninformationen zur Intrastat-Datensatztabelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="7fc76-134">Wählen Sie in der Strukturdarstellung **Intrastat-Tabellendatensätze \> \>Beziehungen \> IntrastatCommodity (Tabellendatensätze EcoResCategory)** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="7fc76-135">Wählen Sie **Metadaten hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fc76-136">Metadaten über erforderliche Beziehungen für die ausgewählte Tabelle von Datensätzen müssen manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7fc76-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="7fc76-137">Wählen Sie **Datenquelle hinzufügen** aus:</span><span class="sxs-lookup"><span data-stu-id="7fc76-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="7fc76-138">Wählen Sie **Aufzählung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="7fc76-139">Filtern Sie auf Wert von **IntrastatDirection** im Feld **Name**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="7fc76-140">Wählen Sie den Aufzählungsdatensatz **IntrastatDirections** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="7fc76-141">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-141">Select **OK**.</span></span>
20. <span data-ttu-id="7fc76-142">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-142">Select **Save**.</span></span>
21. <span data-ttu-id="7fc76-143">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fc76-143">Close the page.</span></span>
22. <span data-ttu-id="7fc76-144">Schließt die Entwurfsversion der Metadatenkonfiguration ab:</span><span class="sxs-lookup"><span data-stu-id="7fc76-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="7fc76-145">Wählen Sie **Status ändern \>Abschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="7fc76-146">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-146">Select **OK**.</span></span>
    3. <span data-ttu-id="7fc76-147">Wählen Sie die abgeschlossene Version 1.</span><span class="sxs-lookup"><span data-stu-id="7fc76-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="7fc76-148">Exportiert die abgeschlossene Version der Metadatenkonfiguration der Anwendung als eine XML-Datei:</span><span class="sxs-lookup"><span data-stu-id="7fc76-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="7fc76-149">Wählen Sie **Austauschen \> Als XML-Datei exportieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="7fc76-150">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-150">Select **OK**.</span></span>

<span data-ttu-id="7fc76-151">Die ER-Metadatenkonfiguration, die Sie erstellt haben, wird als **Metadata.xml für Außenhandel** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7fc76-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="7fc76-152">Sie können es jetzt in RCS importieren, damit es als Metadatenquelle für die Außenhandelsgeschäftdomäne in Finance and Operations verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fc76-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="7fc76-153">Auf Basis dieser Informationen können Sie die Zuordnung zwischen Bewerbungsmetadaten und dem ER-Datenmodell angeben.</span><span class="sxs-lookup"><span data-stu-id="7fc76-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="7fc76-154">Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7fc76-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="7fc76-155">Die folgende Prozedur veranschaulicht, wie ein RCS-Benutzer, mit der Rolle **Systemadministrator** oder **Elektronischer Berichterstellungs-Entwickler** ein neues ER-Modell entwerfen kann, indem er Metadaten aus der Finance and Operations-Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fc76-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the Finance and Operations application.</span></span> <span data-ttu-id="7fc76-156">Auf Anwendungsmetadaten können zugegriffen werden, indem eine ER-Metadatenkonfiguration verwendet wird, die einen Beispielsatz der Metadaten enthält, um auf Außenhandelstransaktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="7fc76-157">Bevor Sie diese Prozedur abschließen können, müssen Sie zunächst die folgende Prozedur abschließen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="7fc76-158">Konfigurationsanbieter erstellen und als aktiv markieren</span><span class="sxs-lookup"><span data-stu-id="7fc76-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="7fc76-159">Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS</span><span class="sxs-lookup"><span data-stu-id="7fc76-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="7fc76-160">Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="7fc76-161">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="7fc76-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="7fc76-162">Wenn Sie diesen Konfigurationsanbieter nicht sehen, schließen Sie die Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) ab.</span><span class="sxs-lookup"><span data-stu-id="7fc76-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="7fc76-163">Importieren Sie die ER-Metadatumenkonfiguration, die Metadaten für die Finance and Operations-Anwendung enthält und die konfiguriert ist, um elektronische Dokumente für die Außenhandelsgeschäftsdomäne zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7fc76-163">Import the ER metadata configuration that contains metadata for the Finance and Operations application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="7fc76-164">Sie haben in der Prozedur [Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) zuvor in diesem Thema diese ER-Metadatumenkonfiguration erstellt und als eine XML-Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="7fc76-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="7fc76-165">Wählen Sie **Metadatenkonfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="7fc76-166">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="7fc76-167">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="7fc76-168">Durchsuchen, um die Datei **metadata.xml für Außenhandel** auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="7fc76-169">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-169">Select **OK**.</span></span>
    6. <span data-ttu-id="7fc76-170">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fc76-170">Close the page.</span></span>

4. <span data-ttu-id="7fc76-171">Eine Datenmodellkonfiguration erstellen:</span><span class="sxs-lookup"><span data-stu-id="7fc76-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="7fc76-172">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="7fc76-173">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="7fc76-174">Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Außenhandelsmodell** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="7fc76-175">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="7fc76-176">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="7fc76-177">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="7fc76-178">Geben Sie im Feld **Name** **Stamm** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="7fc76-179">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="7fc76-180">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="7fc76-181">Geben Sie im Feld **Name** **Transaktion** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="7fc76-182">Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="7fc76-183">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="7fc76-184">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="7fc76-185">Geben Sie im Feld **Name** **Warencode**ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="7fc76-186">Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="7fc76-187">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-187">Select **Add**.</span></span>

    9. <span data-ttu-id="7fc76-188">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="7fc76-189">Geben Sie im Feld „Name“ **Fakturierter Betrag** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="7fc76-190">Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="7fc76-191">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-191">Select **Add**.</span></span>

    10. <span data-ttu-id="7fc76-192">Wählen Sie **Neu** aus, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="7fc76-193">Geben Sie im Feld **Name** **Datum** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="7fc76-194">Wählen Sie im Feld **Artikeltyp** **Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="7fc76-195">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="7fc76-196">Wählen Sie **Hinzufügen \> Stammreferenz** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="7fc76-197">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-197">Select **OK**.</span></span>
    13. <span data-ttu-id="7fc76-198">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-198">Select **Save**.</span></span>
    14. <span data-ttu-id="7fc76-199">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fc76-199">Close the page.</span></span>
    15. <span data-ttu-id="7fc76-200">Wählen Sie **Status ändern \>Abschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="7fc76-201">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-201">Select **OK**.</span></span>

5. <span data-ttu-id="7fc76-202">Erstellen einer Modellzuordnungskonfiguration:</span><span class="sxs-lookup"><span data-stu-id="7fc76-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="7fc76-203">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="7fc76-204">Geben Sie im Dropdown-Dialogfeld **Neu** **Modellzuordnung basierend auf Datenmodell-Außenhandelsmodell** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="7fc76-205">Geben Sie im Feld **Name** **Außenhandelsmodellzuordnung** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="7fc76-206">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="7fc76-207">Wählen Sie auf dem Inforegister **Voraussetzungen** **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="7fc76-208">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-208">Select **New**.</span></span>
    7. <span data-ttu-id="7fc76-209">Wählen Sie im Feld **Vorausgesetzter Komponententyp** **Konfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="7fc76-210">Wählen Sie die Konfiguration **Außenhandelsmetadaten** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="7fc76-211">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-211">Select **Save**.</span></span> <span data-ttu-id="7fc76-212">Beachten Sie, dass der Verweis zur Version 1 der **Außenhandelsmetadaten**-Konfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="7fc76-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="7fc76-213">Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während die Modellzuordnung entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="7fc76-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="7fc76-214">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fc76-214">Close the page.</span></span>
    11. <span data-ttu-id="7fc76-215">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="7fc76-216">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="7fc76-217">Wählen Sie in der Struktur **Dynamics 365 for Operations \> Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="7fc76-218">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="7fc76-219">Geben Sie im Feld **Name** die Bezeichnung **Intrastat** ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="7fc76-220">Wählen Sie die **Intrastat** Tabellendatensätze aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="7fc76-221">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7fc76-222">Es werden nur zwei Tabellen angeboten, da nur zwei Tabellen dem Satz der Metadaten hinzugefügt wurden, der gerade verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fc76-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="7fc76-223">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="7fc76-224">In der Struktur wählen Sie **Intrastat \> AmountMST** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="7fc76-225">Wählen Sie in der Struktur **Transaktion = Intrastat \> Fakturierter Betrag** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="7fc76-226">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="7fc76-227">In der Struktur wählen Sie **Intrastat \> TransDate** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="7fc76-228">In der Struktur wählen Sie **Transaktion = Intrastat \> Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="7fc76-229">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="7fc76-230">Wählen Sie in der Struktur **Intrastat \> \> Beziehungen \> IntrastatCommodity \> Code** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="7fc76-231">Wählen Sie in der Struktur **Transaktion = Intrastat \> Warencode** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="7fc76-232">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="7fc76-233">Wählen Sie **Überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7fc76-234">Nach Abschluss der Validierung haben Sie die Elemente des Datenmodells erfolgreich an die Datenquellenelemente gebunden, die mit Details aus den Anwendungsmetadaten aus der referenzierten ER-Metadatenkonfiguration beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7fc76-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="7fc76-235">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-235">Select **Save**.</span></span>

<span data-ttu-id="7fc76-236">Nach Bedarf können Sie den vorhandenen Satz von Metadaten in Finance and Operations erweitern.</span><span class="sxs-lookup"><span data-stu-id="7fc76-236">As you require, you can extend the existing set of metadata in Finance and Operations.</span></span> <span data-ttu-id="7fc76-237">Sie können anschließend die neue abgeschlossene Version der ER-Metadatenkonfiguration aus Finance and Operations exportieren, sie in RCS importieren und die Voraussetzungen der konfigurierten Zuordnungsmodellkonfiguration aktualisieren und auf eine neue Version der importierten Metadatenkonfiguration verweisen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-237">You can then export the new completed version of the ER metadata configuration from Finance and Operations, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="7fc76-238">Diese Methode des Informationsabrufs von Informationen zu Anwendungsmetadaten ist die einzige Methode für Anwendungen, die lokal bereitgestellt werden (d. h., wenn lokale Geschäftsdaten \[LBD\] oder ein lokales Bereitstellungsmodell für Finance and Operations verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="7fc76-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for Finance and Operations).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="7fc76-239">Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7fc76-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="7fc76-240">Die folgende Prozedur veranschaulicht, wie ein RCS-Benutzer, mit der Rolle **Systemadministrator** oder **Elektronischer Berichterstellungs-Entwickler** ein neues ER-Modell entwerfen kann, indem er Metadaten von der Finance and Operations-Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fc76-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the Finance and Operations application.</span></span> <span data-ttu-id="7fc76-241">Zugriff auf Anwendungs-Metadaten erfolgt online über RCS verbundene Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="7fc76-242">Eine Beispiel-ER-Modellzuordnung wird konfiguriert, um auf Außenhandelstransaktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="7fc76-243">Um diese Prozedur auszuführen, müssen Sie zunächst die Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) in RCS abschließen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="7fc76-244">Wenn Sie die Prozedur [Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](#access-application-metadata-by-using-an-er-configuration) zuvor in diesem Thema noch nicht abgeschlossen haben, navigieren Sie zur Seite [Aufgabenleitfaden für elektronische Berichterstellung für Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), um die folgenden ER-Konfigurationsdateien im Voraus herunterzuladen und lokal zu speichern: **Metadata.xml für Außenhandel**, **Model.xml für Außenhandel** und **Mapping.xml für Außenhandel**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="7fc76-245">Erforderliche ER-Konfigurationen abrufen</span><span class="sxs-lookup"><span data-stu-id="7fc76-245">Get required ER configurations</span></span>

<span data-ttu-id="7fc76-246">Wenn Sie die Schritte in der Prozedur [Zugriff auf Anwendungs-Metadaten über eine ER-Konfiguration](#access-application-metadata-by-using-an-er-configuration) zuvor in diesem Thema bereits abgeschlossen haben, haben Sie bereits alle erforderlichen ER-Konfigurationen (Außenhandelsmetadaten, Modell- und Zuordnungskonfigurationen) in der aktuellen RCS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7fc76-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="7fc76-247">In diesem Fall können Sie diese Prozedur überspringen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="7fc76-248">Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="7fc76-249">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7fc76-250">Laden Sie die Konfigurationsdateien **metadata.xml für Außenhandel**, **model.xml für Außenhandel** und **mapping.xml für Außenhandel** und wiederholen Sie die folgende Schrittfolge für jede einzelne davon:</span><span class="sxs-lookup"><span data-stu-id="7fc76-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="7fc76-251">Wählen Sie **Wechselkurs** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="7fc76-252">Wählen Sie **Aus XML-Datei laden** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="7fc76-253">Wählen Sie **Duchsuchen** und eine Datei aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="7fc76-254">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-finance-and-operations"></a><span data-ttu-id="7fc76-255">Registrieren der Verbindung mit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7fc76-255">Register the connection with Finance and Operations</span></span>

1. <span data-ttu-id="7fc76-256">Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="7fc76-257">Wählen Sie **Verbundene Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="7fc76-258">Überprüfen Sie, ob die konfigurierte Anwendung auf Microsoft Azure basiert und dass RCS-Benutzer im Allgemeinen darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7fc76-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="7fc76-259">Der aktuelle RCS-Benutzer muss Zugriff auf die konfigurierte Anwendung haben und als Benutzer dieser Anwendung in einer Rolle registriert sein, die ihm oder ihr die Rechte für den Zugriff auf die die Metadaten der Anwendung gibt.</span><span class="sxs-lookup"><span data-stu-id="7fc76-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="7fc76-260">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-260">Select **New**.</span></span>
5. <span data-ttu-id="7fc76-261">Wählen Sie im Feld **Name** **MyConnectedApp** als den Namen der verbundenen Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="7fc76-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="7fc76-262">Geben Sie im Feld **Anwendung** die URL der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="7fc76-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="7fc76-263">Geben Sie im Feld **Mandant** den Anbieter der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="7fc76-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="7fc76-264">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-264">Select **Save**.</span></span> 
9. <span data-ttu-id="7fc76-265">Wenn Sie die Verbindung zur der konfigurierten Anwendung überprüfen, wählen Sie auf der Seite **Mit Remote-Anwendung verbinden** den Link **Hier klicken, um Verbindung mit der ausgewählten Remote-Anwendung herzustellen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="7fc76-266">Wählen Sie **Verbindung überprüfen** aus, um den Zugriff auf den konfigurierte Anwendung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7fc76-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="7fc76-267">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-267">Select **Close**.</span></span>

<span data-ttu-id="7fc76-268">Nach Abschluss dieser Prozedur und nach Validierung des Verbindungserfolgs, werden die Versions- und Mandantendetails für die konfigurierte Anwendung im aktuellen Raster aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fc76-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="7fc76-269">Überprüfen der vorhandenen Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="7fc76-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="7fc76-270">Wechseln Sie zu **Alle Arbeitsbereiche \> Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="7fc76-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="7fc76-271">Wählen Sie **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7fc76-272">Wählen Sie in der Struktur **Außenhandelsmodell \> Außenhandelszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="7fc76-273">Wählen Sie auf dem Inforegister **Voraussetzungen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fc76-274">Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fc76-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="7fc76-275">Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="7fc76-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="7fc76-276">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-276">Select **Designer**.</span></span>
5. <span data-ttu-id="7fc76-277">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-277">Select **Designer**.</span></span>
6. <span data-ttu-id="7fc76-278">Wählen Sie in der Struktur **Dynamics 365 for Operations \> Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="7fc76-279">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-279">Select **Add root**.</span></span>
8. <span data-ttu-id="7fc76-280">Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fc76-281">Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7fc76-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="7fc76-282">Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="7fc76-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="7fc76-283">Wählen Sie **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="7fc76-284">Weisen Sie die verbundene Anwendung einer Modellzuordnung zu</span><span class="sxs-lookup"><span data-stu-id="7fc76-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="7fc76-285">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-285">Select **Edit**.</span></span>
2. <span data-ttu-id="7fc76-286">Wählen Sie im Feld **Verbundene Anwendung** die Anwendung **MyConnectedApp** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fc76-287">Diese Zuordnung bezieht sich auf die Metadaten der ausgewählten verbundenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7fc76-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="7fc76-288">Wenn sich eine Zuordnung gleichzeitig auf die Metadatenkonfiguration sowie die verbundene Anwendung bezieht, werden die Metadaten der verbundenen Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fc76-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="7fc76-289">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-289">Select **Designer**.</span></span>
4. <span data-ttu-id="7fc76-290">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-290">Select **Designer**.</span></span>
5. <span data-ttu-id="7fc76-291">Wählen Sie in der Struktur **Dynamics 365 for Operations \> Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="7fc76-292">Wählen Sie **Stamm hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-292">Select **Add root**.</span></span>
7. <span data-ttu-id="7fc76-293">Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7fc76-294">An diesem Punkt werden mehr als zwei Anwendungstabellen angeboten, da diese Zuordnung alle Metadaten der verbundenen Anwendung verwenden, die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7fc76-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="7fc76-295">Wählen Sie **Abbrechen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="7fc76-296">Wählen Sie **Überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fc76-296">Select **Validate**.</span></span>

<span data-ttu-id="7fc76-297">Sie haben nun erfolgreich Elemente des Datenmodells an die Elemente der Datenquellen gebunden, die Details der Metadaten der verbundenen Anwendung verwendet, die dieser Zuordnung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7fc76-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="7fc76-298">Wenn Sie diese Modellzuordnung überprüfen müssen, indem Sie die Metadaten einer anderen Version der Anwendung verwenden, registrieren Sie eine andere verbundene Anwendung, weisen Sie sie dieser Modellzuordnung zu und prüfen Sie sie anhand der neuen Metadaten.</span><span class="sxs-lookup"><span data-stu-id="7fc76-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fc76-299">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7fc76-299">Additional resources</span></span>

<span data-ttu-id="7fc76-300">Alternativ können Sie den Aufgabenleitfaden **Anwendungsmetadaten vorbereiten, die in RCS verwendet werden können** in Finance and Operations sowie die Aufgabenleitfäden **Zugriff auf Anwendungsmetadaten über eine ER-Konfiguration** und **Zugriff auf Anwendungsmetadaten mithilfe verbundener Bewerbungen** in RCS wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="7fc76-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in Finance and Operationsas as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="7fc76-301">Diese Aufgabenleitfäden können von der Seite [Aufgabenleitfäden für elektronische Berichterstellung für Dynamics 365 for Finance and Operations 8,1](https://go.microsoft.com/fwlink/?linkid=2082739) heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="7fc76-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
