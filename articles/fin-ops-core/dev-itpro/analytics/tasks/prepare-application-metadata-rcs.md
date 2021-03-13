---
title: Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS
description: In diesem Thema wird beschrieben, wie Sie eine neue Berichterstellungskonfiguration erstellen, die Anwendungsmetadaten enthält.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5f55d089a88642cb2bda70274472ad0f0e45cd7
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094239"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="1dac4-103">Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS</span><span class="sxs-lookup"><span data-stu-id="1dac4-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1dac4-104">Die folgenden Schritte erklären, wie ein Benutzer in der Systemadministratorenrolle oder der elektronischen Berichtsentwicklerrolle eine neue elektronische Berichterstellungskonfiguration (ER) erstellen kann, die die Anwendungsmetadaten für das Entwerfen der ER-Modellzuordnungskonfigurationen im Regulatory Configuration Service (RCS) enthält.</span><span class="sxs-lookup"><span data-stu-id="1dac4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="1dac4-105">Diese Konfiguration wird für das Entwerfen einer Beispiel-ER-Modellzuordnungskonfiguration verwendet, um auf Außenhandelsbuchungen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="1dac4-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1dac4-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="1dac4-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1dac4-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1dac4-108">Prerequisites</span></span>
1.    <span data-ttu-id="1dac4-109">Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="1dac4-110">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="1dac4-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="1dac4-111">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und diesen als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="1dac4-112">Klicken Sie auf **Metadatenkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="1dac4-113">Angenommen, RCS wird verwendet um eine ER-Lösung für eine Finance and Operations Anwendung zu entwerfen, die elektronische Dokumente erstellt, die Informationen aus der Außenhandelsgeschäftsdomäne enthält.</span><span class="sxs-lookup"><span data-stu-id="1dac4-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="1dac4-114">Um die Zuordnung zwischen ER-Datenmodell und Quellen der erforderlichen Daten anzugeben, benötigen wir in RCS Zugriff auf die Metadaten in der Finance and Operations Anwendung</span><span class="sxs-lookup"><span data-stu-id="1dac4-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="1dac4-115">Daher konfigurieren wir als Teil der ER-Lösung eine neue ER-Metadatenkonfiguration, die alle Metadaten enthält, die zur Generierung der ER-Berichte für ausgewählte Geschäftsdomänen derzeit erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1dac4-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="1dac4-116">Metadatenkonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1dac4-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="1dac4-117">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="1dac4-118">Geben Sie im Feld **Name** den Typ Außenhandelsmetadaten ein.</span><span class="sxs-lookup"><span data-stu-id="1dac4-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="1dac4-119">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="1dac4-120">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="1dac4-121">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1dac4-122">Sie können alle Metadaten für die gesamte Anwendung, ausgewählten Modelle oder ausgewählten Module auswählen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="1dac4-123">Beachten Sie, dass in diesem Fall die folgenden Metadaten automatisch hinzugefügt werden: Tabellen von Datensätzen, Aufzählungen und erweiterte Datentypen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="1dac4-124">Wenn zusätzliche Arten von Metadaten erforderlich sind, müssen sie ggf. manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1dac4-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="1dac4-125">Wir haben einige zum Außenhandel zugehörige Metadaten, indem wir manuell Metadatenelemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="1dac4-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="1dac4-126">Klicken Sie auf **Datenquelle hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="1dac4-127">Klicken Sie auf **Tabellendatensätze**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="1dac4-128">Verwenden Sie den Schnellfilter, um im Feld **Name** nach dem Wert Intrastat zu filtern.</span><span class="sxs-lookup"><span data-stu-id="1dac4-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="1dac4-129">Wählen Sie den **Intrastat**-Tabellendatensatz aus.</span><span class="sxs-lookup"><span data-stu-id="1dac4-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="1dac4-130">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-130">Click **OK**.</span></span>
  
<span data-ttu-id="1dac4-131">Es werden Metadateninformationen zur Intrastat-Tabelle der Datensätze hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1dac4-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="1dac4-132">Erweitern Sie in der Struktur I **TAbellendatensätze Intrastat**\>**Beziehungen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="1dac4-133">Wählen Sie in der Strukturdarstellung **Intrastat Tabellendatensätze**\>**Relations\IntrastatCommodity (Table records EcoResCategory)** aus.</span><span class="sxs-lookup"><span data-stu-id="1dac4-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="1dac4-134">Klicken Sie auf **Hinzufügen von Metadaten**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1dac4-135">Metadaten über erforderliche Beziehungen für ausgewählte Tabelle von Datensätzen müssen manuell hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1dac4-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="1dac4-136">Klicken Sie auf **Datenquelle hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="1dac4-137">Klicken Sie auf **Enumeration**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="1dac4-138">Verwenden Sie den Schnellfilter, um im Feld **Name** nach dem Wert IntrastatDirection zu filtern.</span><span class="sxs-lookup"><span data-stu-id="1dac4-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="1dac4-139">Wählen Sie den Datensatz **IntrastatDirections-Enumeration** aus.</span><span class="sxs-lookup"><span data-stu-id="1dac4-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="1dac4-140">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="1dac4-141">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="1dac4-142">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1dac4-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="1dac4-143">Schließt die Entwurfsversion der Metadatenkonfiguration ab</span><span class="sxs-lookup"><span data-stu-id="1dac4-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="1dac4-144">Klicken Sie auf **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="1dac4-145">Klicken Sie auf **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="1dac4-146">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="1dac4-147">Wählen Sie die abgeschlossene Version **1**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="1dac4-148">Exportiert die abgeschlossene Version der Metadatenkonfiguration der Anwendung als XML-Datei</span><span class="sxs-lookup"><span data-stu-id="1dac4-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="1dac4-149">Klicken Sie auf **Austauschen**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="1dac4-150">Klicken Sie auf **Als XML-Datei exportieren**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="1dac4-151">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1dac4-151">Click **OK**.</span></span> 
    
<span data-ttu-id="1dac4-152">Die erstellte ER-Metadatenkonfiguration ist als XML Datei gespeichert, die in RCS importiert werden kann und als die Informationsquelle über Metadaten für die Außenhandelsdomäne verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1dac4-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="1dac4-153">Auf Basis dieser Informationen können wir die Zuordnung zwischen Bewerbungsmetadaten und ER-Datenmodell angeben.</span><span class="sxs-lookup"><span data-stu-id="1dac4-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
