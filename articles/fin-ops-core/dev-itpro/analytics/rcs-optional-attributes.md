---
title: Import von Dateien im XML-Format mit optionalen Attributen
description: Dieses Thema enthält Informationen zum Entwurf von ER-Formaten, die XML-Attributen angeben, um eingehende elektronische Dokumente im XML-Format zu analysieren.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e2989906c5aa3ead9e46b8ed5333e880e5cf1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769946"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="7fef1-103">Import von Dateien im XML-Format mit optionalen Attributen</span><span class="sxs-lookup"><span data-stu-id="7fef1-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="7fef1-104">Sie können Elektronische Berichterstellung (ER)-Formate entwerfen, um eingehende Dokumente im XML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7fef1-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="7fef1-105">Bestimmte Attribute von XML-Elementen können in entworfenem ER-Format als optional angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fef1-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="7fef1-106">Es ermöglicht Ihnen, eingehende Dateien mit und ohne diese XML-Attribute korrekt zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7fef1-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="7fef1-107">Sie können den Inhalt aus diesen Dateien dann verwenden, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7fef1-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="7fef1-108">Um mehr über diese Funktion zu erfahren, führen Sie die Schritte im Thema [(RCS) Importieren von Dateien im XML-Format mit optionalen Attributen](tasks/import-files-xml-format-optional-attributes.md) aus, die Teil des Geschäftsprozesses 7.5.4.3 Acquire/Develop IT service/solution components (10677) sind.</span><span class="sxs-lookup"><span data-stu-id="7fef1-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="7fef1-109">Sie können diesen Aufgabenleitfaden und die zugeordneten Beispieldateien vom [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="7fef1-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="7fef1-110">Inhaltsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="7fef1-110">Content description</span></span>       | <span data-ttu-id="7fef1-111">Datei</span><span class="sxs-lookup"><span data-stu-id="7fef1-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7fef1-112">Beispieldatei im XML-Format</span><span class="sxs-lookup"><span data-stu-id="7fef1-112">Sample file in XML format</span></span> | <span data-ttu-id="7fef1-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="7fef1-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="7fef1-114">Aufgabenleitfaden</span><span class="sxs-lookup"><span data-stu-id="7fef1-114">Task guide</span></span>                | <span data-ttu-id="7fef1-115">(RCS) Importiert Dateien im XML-Format mit optionalen Attributen.axtr</span><span class="sxs-lookup"><span data-stu-id="7fef1-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="7fef1-116">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle Entwickler für elektronische Berichterstellung zugewiesen ist, eine ER-Formatkonfiguration entwerfen kann, um die Dateien im XML-Format, die optionale Attribute enthalten, zu importieren.</span><span class="sxs-lookup"><span data-stu-id="7fef1-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="7fef1-117">Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte der Vorgehensweise [Konfigurationsanbieter anlegen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7fef1-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="7fef1-118">Bevor Sie beginnen, laden Sie die IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-Datei aus dem Microsoft Download Center(https://go.microsoft.com/fwlink/?linkid=874684) und herunter speichern Sie sie lokal.</span><span class="sxs-lookup"><span data-stu-id="7fef1-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="7fef1-119">Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="7fef1-120">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="7fef1-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="7fef1-121">Wenn Sie diesen Konfigurationsanbieter nicht sehen, führen Sie die Schritte im Thema [Konfigurationsanbieter anlegen aus und markieren Sie ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7fef1-121">If you don’t see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="7fef1-122">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="7fef1-123">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="7fef1-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="7fef1-124">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fef1-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="7fef1-125">Geben Sie im Feld **Name** Modell ein, um die XML-Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="7fef1-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="7fef1-126">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="7fef1-127">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-127">Click **Designer**.</span></span>
5. <span data-ttu-id="7fef1-128">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="7fef1-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="7fef1-129">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="7fef1-130">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-130">Click **Add**.</span></span>
8. <span data-ttu-id="7fef1-131">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="7fef1-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="7fef1-132">Geben Sie im Feld **Name** Liste ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="7fef1-133">Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="7fef1-134">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-134">Click **Add**.</span></span>
12. <span data-ttu-id="7fef1-135">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="7fef1-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="7fef1-136">Geben Sie im Feld **Name** 'Code' ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="7fef1-137">Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="7fef1-138">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-138">Click **Add**.</span></span>
16. <span data-ttu-id="7fef1-139">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-139">Click **Save**.</span></span>
17. <span data-ttu-id="7fef1-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fef1-140">Close the page.</span></span>
18. <span data-ttu-id="7fef1-141">Klicken Sie auf **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-141">Click **Change status**.</span></span>
19. <span data-ttu-id="7fef1-142">Klicken Sie auf **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-142">Click **Complete**.</span></span>
20. <span data-ttu-id="7fef1-143">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="7fef1-144">Erstellen Sie ein Format für den Datenimport</span><span class="sxs-lookup"><span data-stu-id="7fef1-144">Create a format for data import</span></span>
1. <span data-ttu-id="7fef1-145">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fef1-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="7fef1-146">Geben Sie im Feld **Neu** Format basierend auf Datenmodell, um die xml Datei zum importieren ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="7fef1-147">Geben Sie im Feld **Name** 'Formatieren, um XML-Datei zu importieren' ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="7fef1-148">Wählen Sie die Option **Ja** im Feld **Unterstützt Datenimport** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="7fef1-149">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="7fef1-150">Entwerfen Sie ein Format, um eingehende Datei im XML-Format zu analysieren</span><span class="sxs-lookup"><span data-stu-id="7fef1-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="7fef1-151">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-151">Click **Designer**.</span></span>
2. <span data-ttu-id="7fef1-152">Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7fef1-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="7fef1-153">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="7fef1-154">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="7fef1-155">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-155">Click **OK**.</span></span>
6. <span data-ttu-id="7fef1-156">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="7fef1-157">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="7fef1-158">Geben Sie im Feld **Name** 'Dokument' ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="7fef1-159">Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="7fef1-160">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-160">Click **OK**.</span></span>
11. <span data-ttu-id="7fef1-161">Wählen Sie in der Struktur **Root\Dokument**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="7fef1-162">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="7fef1-163">Wählen Sie in der Struktur **XML\Attribute** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="7fef1-164">Geben Sie im Feld **Name** 'ID' ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="7fef1-165">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-165">Click **OK**.</span></span>
16. <span data-ttu-id="7fef1-166">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="7fef1-167">Entwerfen Sie eine Formatzuordnung, um analysierte Informationen zum Datenmodell zu speichern</span><span class="sxs-lookup"><span data-stu-id="7fef1-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="7fef1-168">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="7fef1-169">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-169">Click **New**.</span></span>
3.  <span data-ttu-id="7fef1-170">Geben Sie im Feld **Definition** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="7fef1-171">Geben Sie im Feld **Name** 'Zuordnung' ein.</span><span class="sxs-lookup"><span data-stu-id="7fef1-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="7fef1-172">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-172">Click **Save**.</span></span>
6.  <span data-ttu-id="7fef1-173">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="7fef1-174">Erweitern Sie in der Struktur **Format**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="7fef1-175">Erweitern Sie in der Struktur **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="7fef1-176">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="7fef1-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="7fef1-177">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="7fef1-177">(document)\*\*.</span></span>
10. <span data-ttu-id="7fef1-178">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-178">Click **Bind**.</span></span>
11. <span data-ttu-id="7fef1-179">Erweitern Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="7fef1-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="7fef1-180">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="7fef1-180">(document)\*\*.</span></span>
12. <span data-ttu-id="7fef1-181">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="7fef1-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="7fef1-182">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="7fef1-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="7fef1-183">Erweitern Sie in der Struktur **Liste = format.root.dokument**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="7fef1-184">Wählen Sie in der Struktur **Liste = format.root.dokument\code**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="7fef1-185">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-185">Click **Bind**.</span></span>
16. <span data-ttu-id="7fef1-186">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-186">Click **Save**.</span></span>
17. <span data-ttu-id="7fef1-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fef1-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="7fef1-188">Formularzuordnung ausführen</span><span class="sxs-lookup"><span data-stu-id="7fef1-188">Run format mapping</span></span>
1. <span data-ttu-id="7fef1-189">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-189">Click **Run**.</span></span>
2. <span data-ttu-id="7fef1-190">Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="7fef1-191">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="7fef1-192">Die ausgewählte Datei wurde nicht importiert, da das Formatdesign die Präsenz der Kennung des Attributs für das Element Dokument annimmt, aber die importierte Datei enthält kein solches Attribut.</span><span class="sxs-lookup"><span data-stu-id="7fef1-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="7fef1-193">Ändern Sie die Formatstruktur, um XML-Attribute optional zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="7fef1-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="7fef1-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7fef1-194">Close the page.</span></span>
2. <span data-ttu-id="7fef1-195">Erweitern Sie in der Struktur **root\dokument**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="7fef1-196">Wählen Sie in der Struktur **Root\dokument\id**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="7fef1-197">Wählen Sie **Ja** im Feld **Leere Zeichenfolge für fehlendes Attribut** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="7fef1-198">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="7fef1-199">Führen Sie die Formatzuordnung zu den Teständerungen aus</span><span class="sxs-lookup"><span data-stu-id="7fef1-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="7fef1-200">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="7fef1-201">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-201">Click **Run**.</span></span>
3. <span data-ttu-id="7fef1-202">Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="7fef1-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="7fef1-203">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fef1-203">Click **OK**.</span></span>
5. <span data-ttu-id="7fef1-204">Erstellte XML Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7fef1-204">Review the generated file.</span></span> <span data-ttu-id="7fef1-205">Beachten Sie, dass dieselbe Datei importiert wurde, da das Formatdesign nun das  ID-Attribut für das Element Dokument als optional betrachtet.</span><span class="sxs-lookup"><span data-stu-id="7fef1-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
