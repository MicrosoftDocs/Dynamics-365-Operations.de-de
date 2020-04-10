---
title: (RCS) Importiert Dateien im XML-Format mit optionalen Attributen
description: Dieses Thema enthält Informationen darüber, wie ein Benutzer ER-Formatkonfiguration entwerfen kann, um Dateien im XML-Format mit optionalen Attributen zu importieren.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc28e9a2170929c6cd8daafd7eae54713cec36ff
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143199"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="41e67-103">(RCS) Importiert Dateien im XML-Format mit optionalen Attributen</span><span class="sxs-lookup"><span data-stu-id="41e67-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41e67-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle Entwickler für elektronische Berichterstellung zugewiesen ist, eine ER-Formatkonfiguration entwerfen kann, um die Dateien im XML-Format, die optionale Attribute enthalten, zu importieren.</span><span class="sxs-lookup"><span data-stu-id="41e67-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="41e67-105">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="41e67-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="41e67-106">Bevor Sie beginnen, laden Sie die IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-Datei aus [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) und herunter speichern Sie sie lokal.</span><span class="sxs-lookup"><span data-stu-id="41e67-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="41e67-107">Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="41e67-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="41e67-108">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="41e67-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="41e67-109">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und diesen als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="41e67-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="41e67-110">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="41e67-111">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="41e67-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="41e67-112">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="41e67-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="41e67-113">Geben Sie im Feld **Name** Modell ein, um die XML-Datei zu importieren.</span><span class="sxs-lookup"><span data-stu-id="41e67-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="41e67-114">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="41e67-115">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="41e67-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="41e67-116">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="41e67-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="41e67-117">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="41e67-118">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-118">Click **Add**.</span></span>
8.    <span data-ttu-id="41e67-119">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="41e67-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="41e67-120">Geben Sie im Feld **Name** Liste ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="41e67-121">Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="41e67-122">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-122">Click **Add**.</span></span>
12.    <span data-ttu-id="41e67-123">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="41e67-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="41e67-124">Geben Sie im Feld **Name** 'Code' ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="41e67-125">Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="41e67-126">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-126">Click **Add**.</span></span>
16.    <span data-ttu-id="41e67-127">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="41e67-127">Click **Save**.</span></span>
17.    <span data-ttu-id="41e67-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="41e67-128">Close the page.</span></span>
18.    <span data-ttu-id="41e67-129">Klicken Sie auf **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="41e67-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="41e67-130">Klicken Sie auf **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="41e67-131">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41e67-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="41e67-132">Erstellen Sie ein Format für den Datenimport</span><span class="sxs-lookup"><span data-stu-id="41e67-132">Create a format for data import</span></span>
1.    <span data-ttu-id="41e67-133">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="41e67-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="41e67-134">Geben Sie im Feld **Neu** Format basierend auf Datenmodell, um die xml Datei zum importieren ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="41e67-135">Geben Sie im Feld **Name** „Formatieren, um XML-Datei zu importieren“ ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="41e67-136">Wählen Sie die Option **Ja** im Feld **Unterstützt Datenimport** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="41e67-137">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="41e67-138">Entwerfen Sie ein Format, um eingehende Datei im XML-Format zu analysieren</span><span class="sxs-lookup"><span data-stu-id="41e67-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="41e67-139">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="41e67-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="41e67-140">Klicken Sie auf **Stamm hinzufügen**, um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="41e67-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="41e67-141">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="41e67-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="41e67-142">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="41e67-143">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41e67-143">Click **OK**.</span></span>
6.    <span data-ttu-id="41e67-144">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="41e67-145">Wählen Sie in der Struktur den Knoten **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="41e67-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="41e67-146">Geben Sie im Feld **Name** 'Dokument' ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="41e67-147">Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="41e67-148">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41e67-148">Click **OK**.</span></span>
11.    <span data-ttu-id="41e67-149">Wählen Sie in der Struktur **Root\Dokument**.</span><span class="sxs-lookup"><span data-stu-id="41e67-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="41e67-150">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="41e67-151">Wählen Sie in der Struktur **XML\Attribute** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="41e67-152">Geben Sie im Feld **Name** „ID“ ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="41e67-153">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41e67-153">Click **OK**.</span></span>
16.    <span data-ttu-id="41e67-154">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="41e67-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="41e67-155">Entwerfen Sie eine Formatzuordnung, um analysierte Informationen zum Datenmodell zu speichern</span><span class="sxs-lookup"><span data-stu-id="41e67-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="41e67-156">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="41e67-157">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="41e67-157">Click **New**.</span></span>
3. <span data-ttu-id="41e67-158">Geben Sie im Feld **Definition** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="41e67-159">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="41e67-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="41e67-160">Geben Sie im Feld **Name** 'Zuordnung' ein.</span><span class="sxs-lookup"><span data-stu-id="41e67-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="41e67-161">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="41e67-161">Click **Save**.</span></span>
7. <span data-ttu-id="41e67-162">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="41e67-162">Click **Designer**.</span></span>
8. <span data-ttu-id="41e67-163">Erweitern Sie in der Struktur **Format**.</span><span class="sxs-lookup"><span data-stu-id="41e67-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="41e67-164">Erweitern Sie in der Struktur **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="41e67-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="41e67-165">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="41e67-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="41e67-166">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="41e67-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="41e67-167">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="41e67-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="41e67-168">Erweitern Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="41e67-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="41e67-169">(dokument)\*\*.</span><span class="sxs-lookup"><span data-stu-id="41e67-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="41e67-170">Wählen Sie in der Struktur \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="41e67-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="41e67-171">(dokument)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="41e67-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="41e67-172">Erweitern Sie in der Struktur **Liste = format.root.dokument**.</span><span class="sxs-lookup"><span data-stu-id="41e67-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="41e67-173">Wählen Sie in der Struktur **Liste = format.root.dokument\code**.</span><span class="sxs-lookup"><span data-stu-id="41e67-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="41e67-174">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="41e67-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="41e67-175">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="41e67-175">Click **Save**.</span></span>
18.    <span data-ttu-id="41e67-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="41e67-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="41e67-177">Formularzuordnung ausführen</span><span class="sxs-lookup"><span data-stu-id="41e67-177">Run format mapping</span></span>
1. <span data-ttu-id="41e67-178">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-178">Click **Run**.</span></span>
2. <span data-ttu-id="41e67-179">Klicken Sie auf **Durchsuchen** und wählen Sie **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="41e67-180">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41e67-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="41e67-181">Die ausgewählte Datei wurde nicht importiert, da das Formatdesign die Präsenz der Kennung des Attributs für das Element Dokument annimmt, aber die importierte Datei enthält kein solches Attribut.</span><span class="sxs-lookup"><span data-stu-id="41e67-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="41e67-182">Ändern Sie die Formatstruktur, um XML-Attribute optional zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="41e67-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="41e67-183">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="41e67-183">Close the page.</span></span>
2. <span data-ttu-id="41e67-184">Erweitern Sie in der Struktur **root\dokument**.</span><span class="sxs-lookup"><span data-stu-id="41e67-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="41e67-185">Wählen Sie in der Struktur **Root\dokument\id**.</span><span class="sxs-lookup"><span data-stu-id="41e67-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="41e67-186">Wählen Sie **Ja** im Feld **Leere Zeichenfolge für fehlendes Attribut** aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="41e67-187">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="41e67-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="41e67-188">Führen Sie die Formatzuordnung zu den Teständerungen aus</span><span class="sxs-lookup"><span data-stu-id="41e67-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="41e67-189">Klicken Sie auf **Format zu Modell zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="41e67-190">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="41e67-190">Click **Run**.</span></span>
3. <span data-ttu-id="41e67-191">Klicken Sie auf **Durchsuchen** und wählen Sie die **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**-Datei aus.</span><span class="sxs-lookup"><span data-stu-id="41e67-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="41e67-192">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="41e67-192">Click **OK**.</span></span>
5. <span data-ttu-id="41e67-193">Erstellte XML Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="41e67-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="41e67-194">Dieselbe Datei wurde importiert, da das Formatdesign nun das „ID“-Attribut für das Element „Dokument“ als optional betrachtet.</span><span class="sxs-lookup"><span data-stu-id="41e67-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
