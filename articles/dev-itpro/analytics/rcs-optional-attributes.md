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
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849994"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="ded3d-103">Import von Dateien im XML-Format mit optionalen Attributen</span><span class="sxs-lookup"><span data-stu-id="ded3d-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="ded3d-104">Sie können Elektronische Berichterstellung (ER)-Formate entwerfen, um eingehende Dokumente im XML-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ded3d-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="ded3d-105">Bestimmte Attribute von XML-Elementen können in entworfenem ER-Format als optional angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ded3d-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="ded3d-106">Es ermöglicht Ihnen, eingehende Dateien mit und ohne diese XML-Attribute korrekt zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ded3d-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="ded3d-107">Sie können den Inhalt aus diesen Dateien dann verwenden, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ded3d-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="ded3d-108">Um mehr über diese Funktion zu erfahren, führen Sie die Schritte im Thema, [RCS-Importdateien im XML-Format mit optionalen Attributen](tasks/import-files-xml-format-optional-attributes.md) aus, das Teil ist von 7.5.4.3 IT-Service/Lösungskomponenten (10677) Geschäftsprozess abrufen/entwickeln.</span><span class="sxs-lookup"><span data-stu-id="ded3d-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="ded3d-109">Sie können diesen Aufgabenleitfaden und die zugeordneten Beispieldateien vom [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="ded3d-110">Inhaltsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ded3d-110">Content description</span></span>       | <span data-ttu-id="ded3d-111">Datei</span><span class="sxs-lookup"><span data-stu-id="ded3d-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="ded3d-112">Beispieldatei im XML-Format</span><span class="sxs-lookup"><span data-stu-id="ded3d-112">Sample file in XML format</span></span> | <span data-ttu-id="ded3d-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="ded3d-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="ded3d-114">Aufgabenleitfaden</span><span class="sxs-lookup"><span data-stu-id="ded3d-114">Task guide</span></span>                | <span data-ttu-id="ded3d-115">(RCS) Importiert Dateien im XML-Format mit optionalen Attributen.axtr</span><span class="sxs-lookup"><span data-stu-id="ded3d-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="ded3d-116">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle Entwickler für elektronische Berichterstellung zugewiesen ist, eine ER-Formatkonfiguration entwerfen kann, um die Dateien im XML-Format, die optionale Attribute enthalten, zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ded3d-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="ded3d-117">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="ded3d-118">Bevor Sie beginnen, laden Sie die IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-Datei aus dem Microsoft Download Center(https://go.microsoft.com/fwlink/?linkid=874684) und herunter speichern Sie sie lokal.</span><span class="sxs-lookup"><span data-stu-id="ded3d-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="ded3d-119">Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="ded3d-120">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ded3d-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ded3d-121">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="ded3d-122">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="ded3d-123">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="ded3d-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="ded3d-124">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="ded3d-125">Geben Sie im Feld **Name** Modell ein, um die XML-Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ded3d-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="ded3d-126">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="ded3d-127">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-127">Click **Designer**.</span></span>
5. <span data-ttu-id="ded3d-128">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="ded3d-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="ded3d-129">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="ded3d-130">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-130">Click **Add**.</span></span>
8. <span data-ttu-id="ded3d-131">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="ded3d-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="ded3d-132">Geben Sie im Feld **Name** Liste ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="ded3d-133">Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="ded3d-134">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-134">Click **Add**.</span></span>
12. <span data-ttu-id="ded3d-135">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="ded3d-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="ded3d-136">Geben Sie im Feld **Name** 'Code' ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="ded3d-137">Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="ded3d-138">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-138">Click **Add**.</span></span>
16. <span data-ttu-id="ded3d-139">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-139">Click **Save**.</span></span>
17. <span data-ttu-id="ded3d-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ded3d-140">Close the page.</span></span>
18. <span data-ttu-id="ded3d-141">Klicken Sie auf **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-141">Click **Change status**.</span></span>
19. <span data-ttu-id="ded3d-142">Klicken Sie auf **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-142">Click **Complete**.</span></span>
20. <span data-ttu-id="ded3d-143">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="ded3d-144">Erstellen Sie ein Format für den Datenimport</span><span class="sxs-lookup"><span data-stu-id="ded3d-144">Create a format for data import</span></span>
1. <span data-ttu-id="ded3d-145">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="ded3d-146">Geben Sie im Feld **Neu** Format basierend auf Datenmodell, um die xml Datei zum importieren ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="ded3d-147">Geben Sie im Feld **Name** 'Formatieren, um XML-Datei zu importieren' ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="ded3d-148">Wählen Sie die Option **Ja** im Feld **Unterstützt Datenimport** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="ded3d-149">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="ded3d-150">Entwerfen Sie ein Format, um eingehende Datei im XML-Format zu analysieren</span><span class="sxs-lookup"><span data-stu-id="ded3d-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="ded3d-151">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-151">Click **Designer**.</span></span>
2. <span data-ttu-id="ded3d-152">Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="ded3d-153">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="ded3d-154">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="ded3d-155">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-155">Click **OK**.</span></span>
6. <span data-ttu-id="ded3d-156">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="ded3d-157">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="ded3d-158">Geben Sie im Feld **Name** 'Dokument' ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="ded3d-159">Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="ded3d-160">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-160">Click **OK**.</span></span>
11. <span data-ttu-id="ded3d-161">Wählen Sie in der Struktur **Root\Dokument**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="ded3d-162">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="ded3d-163">Wählen Sie in der Struktur **XML\Attribute** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="ded3d-164">Geben Sie im Feld **Name** 'ID' ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="ded3d-165">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-165">Click **OK**.</span></span>
16. <span data-ttu-id="ded3d-166">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="ded3d-167">Entwerfen Sie eine Formatzuordnung, um analysierte Informationen zum Datenmodell zu speichern</span><span class="sxs-lookup"><span data-stu-id="ded3d-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="ded3d-168">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="ded3d-169">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-169">Click **New**.</span></span>
3.  <span data-ttu-id="ded3d-170">Geben Sie im Feld **Definition** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="ded3d-171">Geben Sie im Feld **Name** 'Zuordnung' ein.</span><span class="sxs-lookup"><span data-stu-id="ded3d-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="ded3d-172">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-172">Click **Save**.</span></span>
6.  <span data-ttu-id="ded3d-173">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="ded3d-174">Erweitern Sie in der Struktur **Format**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="ded3d-175">Erweitern Sie in der Struktur **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="ded3d-176">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="ded3d-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="ded3d-177">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="ded3d-177">(document)\*\*.</span></span>
10. <span data-ttu-id="ded3d-178">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-178">Click **Bind**.</span></span>
11. <span data-ttu-id="ded3d-179">Erweitern Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="ded3d-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="ded3d-180">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="ded3d-180">(document)\*\*.</span></span>
12. <span data-ttu-id="ded3d-181">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="ded3d-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="ded3d-182">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="ded3d-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="ded3d-183">Erweitern Sie in der Struktur **Liste = format.root.dokument**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="ded3d-184">Wählen Sie in der Struktur **Liste = format.root.dokument\code**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="ded3d-185">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-185">Click **Bind**.</span></span>
16. <span data-ttu-id="ded3d-186">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-186">Click **Save**.</span></span>
17. <span data-ttu-id="ded3d-187">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ded3d-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="ded3d-188">Formularzuordnung ausführen</span><span class="sxs-lookup"><span data-stu-id="ded3d-188">Run format mapping</span></span>
1. <span data-ttu-id="ded3d-189">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-189">Click **Run**.</span></span>
2. <span data-ttu-id="ded3d-190">Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="ded3d-191">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="ded3d-192">Die ausgewählte Datei wurde nicht importiert, da das Formatdesign die Präsenz der Kennung des Attributs für das Element Dokument annimmt, aber die importierte Datei enthält kein solches Attribut.</span><span class="sxs-lookup"><span data-stu-id="ded3d-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="ded3d-193">Ändern Sie die Formatstruktur, um XML-Attribute optional zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="ded3d-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="ded3d-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ded3d-194">Close the page.</span></span>
2. <span data-ttu-id="ded3d-195">Erweitern Sie in der Struktur **root\dokument**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="ded3d-196">Wählen Sie in der Struktur **Root\dokument\id**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="ded3d-197">Wählen Sie **Ja** im Feld **Leere Zeichenfolge für fehlendes Attribut** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="ded3d-198">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="ded3d-199">Führen Sie die Formatzuordnung zu den Teständerungen aus</span><span class="sxs-lookup"><span data-stu-id="ded3d-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="ded3d-200">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="ded3d-201">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-201">Click **Run**.</span></span>
3. <span data-ttu-id="ded3d-202">Klicken Sie auf **Durchsuchen** und wählen Sie die Datei **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="ded3d-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="ded3d-203">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ded3d-203">Click **OK**.</span></span>
5. <span data-ttu-id="ded3d-204">Erstellte XML Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ded3d-204">Review the generated file.</span></span> <span data-ttu-id="ded3d-205">Beachten Sie, dass dieselbe Datei importiert wurde, da das Formatdesign nun das  ID-Attribut für das Element Dokument als optional betrachtet.</span><span class="sxs-lookup"><span data-stu-id="ded3d-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
