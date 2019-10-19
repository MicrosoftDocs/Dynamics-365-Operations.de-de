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
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182829"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="bcb60-103">Import von Dateien im XML-Format mit optionalen Attributen</span><span class="sxs-lookup"><span data-stu-id="bcb60-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="bcb60-104">Sie können Elektronische Berichterstellung (ER)-Formate entwerfen, um eingehende Dokumente im XML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="bcb60-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="bcb60-105">Bestimmte Attribute von XML-Elementen können in entworfenem ER-Format als optional angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bcb60-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="bcb60-106">Es ermöglicht Ihnen, eingehende Dateien mit und ohne diese XML-Attribute korrekt zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bcb60-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="bcb60-107">Sie können den Inhalt aus diesen Dateien dann verwenden, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bcb60-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="bcb60-108">Um mehr über diese Funktion zu erfahren, führen Sie die Schritte im Thema, [RCS-Importdateien im XML-Format mit optionalen Attributen](tasks/import-files-xml-format-optional-attributes.md) aus, das Teil ist von 7.5.4.3 IT-Service/Lösungskomponenten (10677) Geschäftsprozess abrufen/entwickeln.</span><span class="sxs-lookup"><span data-stu-id="bcb60-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="bcb60-109">Sie können diesen Aufgabenleitfaden und die zugeordneten Beispieldateien vom [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="bcb60-110">Inhaltsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="bcb60-110">Content description</span></span>       | <span data-ttu-id="bcb60-111">Datei</span><span class="sxs-lookup"><span data-stu-id="bcb60-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bcb60-112">Beispieldatei im XML-Format</span><span class="sxs-lookup"><span data-stu-id="bcb60-112">Sample file in XML format</span></span> | <span data-ttu-id="bcb60-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="bcb60-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="bcb60-114">Aufgabenleitfaden</span><span class="sxs-lookup"><span data-stu-id="bcb60-114">Task guide</span></span>                | <span data-ttu-id="bcb60-115">(RCS) Importiert Dateien im XML-Format mit optionalen Attributen.axtr</span><span class="sxs-lookup"><span data-stu-id="bcb60-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="bcb60-116">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle Entwickler für elektronische Berichterstellung zugewiesen ist, eine ER-Formatkonfiguration entwerfen kann, um die Dateien im XML-Format, die optionale Attribute enthalten, zu importieren.</span><span class="sxs-lookup"><span data-stu-id="bcb60-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="bcb60-117">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="bcb60-118">Bevor Sie beginnen, laden Sie die IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-Datei aus dem Microsoft Download Center(https://go.microsoft.com/fwlink/?linkid=874684) und herunter speichern Sie sie lokal.</span><span class="sxs-lookup"><span data-stu-id="bcb60-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="bcb60-119">Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="bcb60-120">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="bcb60-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="bcb60-121">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="bcb60-122">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="bcb60-123">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="bcb60-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="bcb60-124">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="bcb60-125">Geben Sie im Feld **Name** Modell ein, um die XML-Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="bcb60-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="bcb60-126">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="bcb60-127">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-127">Click **Designer**.</span></span>
5. <span data-ttu-id="bcb60-128">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="bcb60-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="bcb60-129">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="bcb60-130">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-130">Click **Add**.</span></span>
8. <span data-ttu-id="bcb60-131">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="bcb60-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="bcb60-132">Geben Sie im Feld **Name** Liste ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="bcb60-133">Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="bcb60-134">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-134">Click **Add**.</span></span>
12. <span data-ttu-id="bcb60-135">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="bcb60-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="bcb60-136">Geben Sie im Feld **Name** 'Code' ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="bcb60-137">Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="bcb60-138">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-138">Click **Add**.</span></span>
16. <span data-ttu-id="bcb60-139">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-139">Click **Save**.</span></span>
17. <span data-ttu-id="bcb60-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bcb60-140">Close the page.</span></span>
18. <span data-ttu-id="bcb60-141">Klicken Sie auf **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-141">Click **Change status**.</span></span>
19. <span data-ttu-id="bcb60-142">Klicken Sie auf **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-142">Click **Complete**.</span></span>
20. <span data-ttu-id="bcb60-143">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="bcb60-144">Erstellen Sie ein Format für den Datenimport</span><span class="sxs-lookup"><span data-stu-id="bcb60-144">Create a format for data import</span></span>
1. <span data-ttu-id="bcb60-145">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="bcb60-146">Geben Sie im Feld **Neu** Format basierend auf Datenmodell, um die xml Datei zum importieren ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="bcb60-147">Geben Sie im Feld **Name** 'Formatieren, um XML-Datei zu importieren' ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="bcb60-148">Wählen Sie die Option **Ja** im Feld **Unterstützt Datenimport** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="bcb60-149">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="bcb60-150">Entwerfen Sie ein Format, um eingehende Datei im XML-Format zu analysieren</span><span class="sxs-lookup"><span data-stu-id="bcb60-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="bcb60-151">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-151">Click **Designer**.</span></span>
2. <span data-ttu-id="bcb60-152">Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="bcb60-153">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="bcb60-154">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="bcb60-155">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-155">Click **OK**.</span></span>
6. <span data-ttu-id="bcb60-156">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="bcb60-157">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="bcb60-158">Geben Sie im Feld **Name** 'Dokument' ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="bcb60-159">Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="bcb60-160">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-160">Click **OK**.</span></span>
11. <span data-ttu-id="bcb60-161">Wählen Sie in der Struktur **Root\Dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="bcb60-162">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="bcb60-163">Wählen Sie in der Struktur **XML\Attribute** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="bcb60-164">Geben Sie im Feld **Name** 'ID' ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="bcb60-165">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-165">Click **OK**.</span></span>
16. <span data-ttu-id="bcb60-166">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="bcb60-167">Entwerfen Sie eine Formatzuordnung, um analysierte Informationen zum Datenmodell zu speichern</span><span class="sxs-lookup"><span data-stu-id="bcb60-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="bcb60-168">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="bcb60-169">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-169">Click **New**.</span></span>
3.  <span data-ttu-id="bcb60-170">Geben Sie im Feld **Definition** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="bcb60-171">Geben Sie im Feld **Name** 'Zuordnung' ein.</span><span class="sxs-lookup"><span data-stu-id="bcb60-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="bcb60-172">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-172">Click **Save**.</span></span>
6.  <span data-ttu-id="bcb60-173">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="bcb60-174">Erweitern Sie in der Struktur **Format**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="bcb60-175">Erweitern Sie in der Struktur **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="bcb60-176">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="bcb60-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="bcb60-177">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="bcb60-177">(document)\*\*.</span></span>
10. <span data-ttu-id="bcb60-178">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-178">Click **Bind**.</span></span>
11. <span data-ttu-id="bcb60-179">Erweitern Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="bcb60-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="bcb60-180">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="bcb60-180">(document)\*\*.</span></span>
12. <span data-ttu-id="bcb60-181">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="bcb60-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="bcb60-182">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="bcb60-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="bcb60-183">Erweitern Sie in der Struktur **Liste = format.root.dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="bcb60-184">Wählen Sie in der Struktur **Liste = format.root.dokument\code**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="bcb60-185">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-185">Click **Bind**.</span></span>
16. <span data-ttu-id="bcb60-186">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-186">Click **Save**.</span></span>
17. <span data-ttu-id="bcb60-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bcb60-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="bcb60-188">Formularzuordnung ausführen</span><span class="sxs-lookup"><span data-stu-id="bcb60-188">Run format mapping</span></span>
1. <span data-ttu-id="bcb60-189">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-189">Click **Run**.</span></span>
2. <span data-ttu-id="bcb60-190">Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="bcb60-191">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="bcb60-192">Die ausgewählte Datei wurde nicht importiert, da das Formatdesign die Präsenz der Kennung des Attributs für das Element Dokument annimmt, aber die importierte Datei enthält kein solches Attribut.</span><span class="sxs-lookup"><span data-stu-id="bcb60-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="bcb60-193">Ändern Sie die Formatstruktur, um XML-Attribute optional zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bcb60-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="bcb60-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="bcb60-194">Close the page.</span></span>
2. <span data-ttu-id="bcb60-195">Erweitern Sie in der Struktur **root\dokument**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="bcb60-196">Wählen Sie in der Struktur **Root\dokument\id**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="bcb60-197">Wählen Sie **Ja** im Feld **Leere Zeichenfolge für fehlendes Attribut** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="bcb60-198">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="bcb60-199">Führen Sie die Formatzuordnung zu den Teständerungen aus</span><span class="sxs-lookup"><span data-stu-id="bcb60-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="bcb60-200">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="bcb60-201">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-201">Click **Run**.</span></span>
3. <span data-ttu-id="bcb60-202">Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="bcb60-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="bcb60-203">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb60-203">Click **OK**.</span></span>
5. <span data-ttu-id="bcb60-204">Erstellte XML Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bcb60-204">Review the generated file.</span></span> <span data-ttu-id="bcb60-205">Beachten Sie, dass dieselbe Datei importiert wurde, da das Formatdesign nun das  ID-Attribut für das Element Dokument als optional betrachtet.</span><span class="sxs-lookup"><span data-stu-id="bcb60-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
