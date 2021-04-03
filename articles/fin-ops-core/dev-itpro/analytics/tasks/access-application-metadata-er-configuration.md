---
title: Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration
description: In diesem Thema wird erläutert, wie ein Regulatory Configuration Service-Benutzer eine neue Modellzuordnung für elektronische Berichterstellung (EB) entwerfen kann, indem er die Metadaten verwendet.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c50047781fdc21c9157ceb634822c6cfb5a075
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559650"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="34bc4-103">Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="34bc4-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34bc4-104">In den folgenden Schritten wird erläutert, wie ein Regulatory Configuration Service (RCS)-Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Modellzuordnung für „Elektronische Berichterstellung (ER)“ entwerfen kann, indem er die Metadaten der Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="34bc4-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="34bc4-105">Auf Anwendungsmetadaten können zugegriffen werden, indem eine ER-Metadatenkonfiguration verwendet wird, die einen Beispielsatz der Metadaten enthält, um auf Außenhandelstransaktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="34bc4-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="34bc4-106">Um diese Schritte auszuführen, müssen Sie zunächst in RCS die Schritte in der Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="34bc4-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="34bc4-107">Schließen Sie dann die Schritte im Thema [Anwendungsmetadaten zur Verwendung in RCS vorbereiten](prepare-application-metadata-rcs.md) ab.</span><span class="sxs-lookup"><span data-stu-id="34bc4-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="34bc4-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="34bc4-108">Prerequisites</span></span>
1. <span data-ttu-id="34bc4-109">Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="34bc4-110">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="34bc4-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="34bc4-111">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und diesen als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="34bc4-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="34bc4-112">Importieren der Metadatenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="34bc4-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="34bc4-113">Klicken Sie auf **Metadatenkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="34bc4-114">Importieren Sie die ER-Metadatumenkonfiguration, die Metadaten enthält und die konfiguriert wurde, um elektronische Dokumente für das Außenhandelsgeschäft zu generieren.</span><span class="sxs-lookup"><span data-stu-id="34bc4-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="34bc4-115">Diese ER-Metadatumenkonfiguration wurde als XML-Datei exportiert, während die Schritte in der Prozedur [Anwendungsmetadaten vorbereiten, die in RCS verwendet werden](prepare-application-metadata-rcs.md) ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="34bc4-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="34bc4-116">Klicken Sie auf **Austauschen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="34bc4-117">Klicken Sie auf **Aus XML-Datei laden**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="34bc4-118">Klicken Sie **Durchsuchen** und wählen die Datei metadata.xml für Außenhandel aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="34bc4-119">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-119">Click **OK**.</span></span> 
7. <span data-ttu-id="34bc4-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="34bc4-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="34bc4-121">Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="34bc4-121">Create data model configuration</span></span>
1. <span data-ttu-id="34bc4-122">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="34bc4-123">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="34bc4-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="34bc4-124">Geben Sie im Feld **Name** „Außenhandelsmodell“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="34bc4-125">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="34bc4-126">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="34bc4-127">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34bc4-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="34bc4-128">Geben Sie im Feld **Name** Stamm ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="34bc4-129">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-129">Click **Add**.</span></span> 
9. <span data-ttu-id="34bc4-130">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34bc4-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="34bc4-131">Geben Sie im Feld **Name** „Transaktion“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="34bc4-132">Wählen Sie im Feld **Artikeltyp** **Datensatzliste** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="34bc4-133">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="34bc4-134">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34bc4-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="34bc4-135">Geben Sie im Feld **Name** „Warencode“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="34bc4-136">Wählen Sie im Feld **Artikeltyp** **Zeichenfolge** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="34bc4-137">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="34bc4-138">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34bc4-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="34bc4-139">Geben Sie im Feld **Name** „Fakturierter Betrag“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="34bc4-140">Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="34bc4-141">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="34bc4-142">Klicken Sie auf **Neu** zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="34bc4-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="34bc4-143">Geben Sie im Feld **Name** „Datum“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="34bc4-144">Wählen Sie im Feld **Artikeltyp** **Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="34bc4-145">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="34bc4-146">Klicken Sie auf **Stammreferenz**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="34bc4-147">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="34bc4-148">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="34bc4-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="34bc4-149">Close the page.</span></span> 
29.    <span data-ttu-id="34bc4-150">Klicken Sie auf **Status ändern**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="34bc4-151">Klicken Sie auf **Abgeschlossen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="34bc4-152">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="34bc4-153">Erstellen der Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="34bc4-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="34bc4-154">Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="34bc4-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="34bc4-155">Geben Sie im Feld **Neu** 'Modellzuordnung basierend auf Datenmodell-Außenhandelsmodell' ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="34bc4-156">Geben Sie im Feld **Name** „Außenhandelsmodellzuordnung“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="34bc4-157">Klicken Sie auf **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="34bc4-158">Erweitern Sie den Abschnitt **Voraussetzungen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="34bc4-159">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="34bc4-160">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-160">Click **New**.</span></span> 
8. <span data-ttu-id="34bc4-161">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="34bc4-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="34bc4-162">Wählen Sie im Feld **Vorausgesetzter Komponententyp** **Konfiguration** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="34bc4-163">Wählen Sie die Konfiguration **Außenhandelsmetadaten** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="34bc4-164">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="34bc4-165">Wir haben die Referenz der Version 1 der Außenhandelsmetadaten-Konfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="34bc4-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="34bc4-166">Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="34bc4-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="34bc4-167">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="34bc4-167">Close the page.</span></span> 
14.    <span data-ttu-id="34bc4-168">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="34bc4-169">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="34bc4-170">Wählen Sie in der Struktur **Dynamics 365 for Operations\Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="34bc4-171">Klicken Sie auf **Stamm hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="34bc4-172">Geben Sie im Feld **Name** „Intrastat“ ein.</span><span class="sxs-lookup"><span data-stu-id="34bc4-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="34bc4-173">Wählen Sie die **Intrastat** Tabellendatensätze aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="34bc4-174">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="34bc4-175">Die einzigen 2 Tabellen wurden angeboten, als die einzigen 2 Tabellen dem Satz der Metadaten hinzugefügt wurden, die gerade verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34bc4-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="34bc4-176">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="34bc4-177">Erweitern Sie in der Struktur **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="34bc4-178">In der Struktur wählen Sie **Intrastat\AmountMST** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="34bc4-179">Erweitern Sie in der Struktur **Transaction = Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="34bc4-180">Wählen Sie in der Struktur **Transaction = Intrastat\Fakturierter Betrag** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="34bc4-181">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="34bc4-182">In der Struktur wählen Sie **Intrastat\TransDate** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="34bc4-183">In der Struktur wählen Sie **Transaction = Intrastat\Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="34bc4-184">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="34bc4-185">Erweitern Sie in der Struktur **Intrastat\>Beziehungen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="34bc4-186">Erweitern Sie in der Struktur **Intrastat\>Beziehungen\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="34bc4-187">Wählen Sie in der Struktur **Intrastat\>Beziehungen\IntrastatCommodity\Code**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="34bc4-188">Wählen Sie in der Struktur **Transaction = Intrastat\Warencode** aus.</span><span class="sxs-lookup"><span data-stu-id="34bc4-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="34bc4-189">Klicken Sie auf **Binden**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="34bc4-190">Klicken Sie auf **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="34bc4-191">Es wurden erfolgreich Elemente des Datenmodells mit Datenquellenelementen gebunden, die mit Details aus Bewerbungsmetadaten aus der referenzierten ER-Metadatenkonfiguration beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="34bc4-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="34bc4-192">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="34bc4-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="34bc4-193">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="34bc4-193">Close the page.</span></span> 
38.    <span data-ttu-id="34bc4-194">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="34bc4-194">Close the page.</span></span> 
39.    <span data-ttu-id="34bc4-195">Bei Bedarf können Sie die vorhandene Gruppe von Metadaten erweitern und dann die abgeschlossene neue Version der ER-Metadatumenkonfiguration exportieren.</span><span class="sxs-lookup"><span data-stu-id="34bc4-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="34bc4-196">Sie können sie dann in RCS importieren und die Voraussetzungen der Zuordnungskonfiguration des Modells aktualisieren, die sich auf eine neue Version der importierten Metadatumenkonfiguration beziehen.</span><span class="sxs-lookup"><span data-stu-id="34bc4-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="34bc4-197">Diese Art des Informationsabrufs von Informationen zu Anwendungsmetadaten ist als einzige für lokal bereitgestellte Anwendungen verfügbar (wenn lokale Geschäftsdaten (LBD) oder ein lokales Bereitstellungsmodell verwendet werden).</span><span class="sxs-lookup"><span data-stu-id="34bc4-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]