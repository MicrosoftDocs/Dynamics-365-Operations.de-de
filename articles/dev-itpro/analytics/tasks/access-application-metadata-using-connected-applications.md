---
title: Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen
description: Die Schritte in diesem Thema erläutern, wie ein Regulatory configuration service (RCS)-Benutzer eine neue Modellzuordnung für elektronische Berichterstellung (ER) entwerfen kann, indem er die Metadaten in Finance and Operations verwendet.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
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
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d3581f6ae2d91b9648da3ba69e6b1d36cd08196
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727051"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="c59c3-103">Zugriff auf Anwendungs-Metadaten über verbundene Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c59c3-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c59c3-104">In den folgenden Schritten wird erläutert, wie ein Regulatory Configuration Service (RCS)-Benutzer mit der Systemadministratorrolle oder der Rolle „Entwickler für elektronische Berichterstellung“ eine neue Modellzuordnung für „Elektronische Berichterstellung (ER)“ entwerfen kann, indem er die Metadaten in Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c59c3-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c59c3-105">Zugriff auf Anwendungs-Metadaten erfolgt online über die RCS verbundene Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c59c3-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="c59c3-106">Beispiel-ER-Modellzuordnung wird konfiguriert, um auf Außenhandelstransaktionen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c59c3-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="c59c3-107">Um diese Schritte auszuführen, müssen Sie in RCS zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="c59c3-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="c59c3-108">Wenn Sie die Schritte im Thema [Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](access-application-metadata-er-configuration.md) abgeschlossen haben, fahren Sie mit der [Beispielseite für elektronische Berichterstellung](https://go.microsoft.com/fwlink/?linkid=862266) fort, um die folgenden ER-Konfigurationen herunterzuladen und zu speichern: Außenhandelsmetadaten.xml; Außenhandelsmodel.xml; Außenhandelszuordnung.xml und führen Sie dann die Schritte in der Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c59c3-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c59c3-109">Prerequisites</span></span>
1. <span data-ttu-id="c59c3-110">Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="c59c3-111">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist.</span><span class="sxs-lookup"><span data-stu-id="c59c3-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="c59c3-112">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.</span><span class="sxs-lookup"><span data-stu-id="c59c3-112">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="c59c3-113">Erforderliche ER-Konfigurationen abrufen</span><span class="sxs-lookup"><span data-stu-id="c59c3-113">Get required ER configurations</span></span>
1. <span data-ttu-id="c59c3-114">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="c59c3-115">Wenn Sie die Schritte in der Prozedur [(RCS) Zugriff auf Anwendungs-Metadaten über die ER-Konfiguration](access-application-metadata-er-configuration.md) bereits abgeschlossen haben, haben Sie bereits alle erforderlichen ER-Konfigurationen (Außenhandelsmetadaten, Modell- und Zuordnungskonfigurationen) in der aktuellen RCS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="c59c3-115">If you already completed the steps in the [(RCS) Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="c59c3-116">Sie können alle übrigen Schritte dieser Unteraufgabe überspringen.</span><span class="sxs-lookup"><span data-stu-id="c59c3-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="c59c3-117">Klicken Sie auf **Austauschen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="c59c3-118">Klicken Sie auf **Aus XML-Datei laden**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="c59c3-119">Klicken Sie auf **Durchsuchen** und wählen die Datei **metadata.xml für Außenhandel** aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="c59c3-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-120">Click **OK**.</span></span> 
7. <span data-ttu-id="c59c3-121">Klicken Sie auf **Austauschen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="c59c3-122">Klicken Sie auf **Aus XML-Datei laden**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="c59c3-123">Klicken Sie auf **Durchsuchen** und wählen die Datei **model.xml für Außenhandel** aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="c59c3-124">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-124">Click **OK**.</span></span> 
11. <span data-ttu-id="c59c3-125">Klicken Sie auf **Austauschen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="c59c3-126">Klicken Sie auf **Aus XML-Datei laden**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="c59c3-127">Klicken Sie auf **Durchsuchen** und wählen die Datei **mapping.xml für Außenhandel** aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="c59c3-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-128">Click **OK**.</span></span> 

## <a name="register-connected-dynamics-365-for-finance-and-operations-application"></a><span data-ttu-id="c59c3-129">Registrieren Sie die verbundene Dynamics 365 for Finance and Operations-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c59c3-129">Register connected Dynamics 365 for Finance and Operations application</span></span>
1. <span data-ttu-id="c59c3-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-130">Close the page.</span></span> 
2. <span data-ttu-id="c59c3-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-131">Close the page.</span></span> 
3. <span data-ttu-id="c59c3-132">Wechseln Sie zu **Alle Arbeitsbereiche** > **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="c59c3-133">Klicken Sie auf **Verbundene Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="c59c3-134">Überprüfen Sie, dass die konfigurierte Anwendung Azura-basiert ist und der aktuelle RCS-Benutzer darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c59c3-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="c59c3-135">Es ist auch erforderlich, dass der aktuelle RCS-Benutzer Zugriff auf die ausgewählte Anwendung und als Benutzer dieser Anwendung registriert wurde. Dies spielt eine Rolle bei seinen Rechten für den Zugriff auf die Metadaten der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c59c3-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="c59c3-136">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-136">Click **New**.</span></span> 
7. <span data-ttu-id="c59c3-137">Geben Sie im Feld **Name** „MyConnectedApp“ ein.</span><span class="sxs-lookup"><span data-stu-id="c59c3-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="c59c3-138">Geben Sie im Feld **Anwendung** „https:// mycompany.operations.dynamics.com“ ein.</span><span class="sxs-lookup"><span data-stu-id="c59c3-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="c59c3-139">Geben Sie im Feld **Mandant** „mycompany.onmicrosoft.com“ ein.</span><span class="sxs-lookup"><span data-stu-id="c59c3-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="c59c3-140">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-140">Click **Save**.</span></span> 
11. <span data-ttu-id="c59c3-141">Wenn Sie Verbindungen zur konfigurierten Anwendung überprüfen, klicken Sie auf der Seite **Mit Remote-Anwendung verbinden** auf den Link **Hier klicken, um Verindung mit der ausgewählten Remote-Anwendung herzustellen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="c59c3-142">Klicken Sie auf **Verbindung prüfen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="c59c3-143">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-143">Click **Close**.</span></span> 
14. <span data-ttu-id="c59c3-144">Wenn die Verbindungsprüfung erfolgreich war, werden Versions- und Mandantendetails für die konfigurierte Anwendung im aktuellen Raster aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c59c3-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="c59c3-145">Überprüfen einer vorhandenen Modellzuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="c59c3-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="c59c3-146">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-146">Close the page.</span></span> 
2. <span data-ttu-id="c59c3-147">Klicken Sie auf **Berichterstellungskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="c59c3-148">Erweitern Sie **Außenhandelsmodell** in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="c59c3-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="c59c3-149">Wählen Sie in der Struktur **Außenhandelsmodell\Außenhandelszuordnung** aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="c59c3-150">Erweitern Sie den Abschnitt **Voraussetzungen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-150">Expand the **Prerequisites** section.</span></span> 

> [!NOTE]
> <span data-ttu-id="c59c3-151">Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c59c3-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="c59c3-152">Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="c59c3-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="c59c3-153">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="c59c3-154">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="c59c3-155">Wählen Sie in der Struktur **Dynamics 365 for Operations\Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="c59c3-156">Klicken Sie auf **Stamm hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="c59c3-157">Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-157">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="c59c3-158">Diese Zuordnung bezieht sich derzeit auf die Metadatenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c59c3-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="c59c3-159">Anwendungsmetadaten aus dieser Konfiguration werden angeboten, während diese Modellzuordnung entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="c59c3-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="c59c3-160">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="c59c3-161">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-161">Close the page.</span></span> 
13. <span data-ttu-id="c59c3-162">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="c59c3-163">Weisen Sie die verbundene Anwendung der Modellzuordnung zu</span><span class="sxs-lookup"><span data-stu-id="c59c3-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="c59c3-164">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="c59c3-165">Wählen Sie die **MyConnectedApp**-Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-165">Select **MyConnectedApp** application.</span></span> 

> [!NOTE]
> <span data-ttu-id="c59c3-166">Momentan bezieht sich diese Zuordnung auf die Metadaten der ausgewählten verbundenen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c59c3-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="c59c3-167">Wenn sich dieselbe Zuordnung gleichzeitig auf die Metadatenkonfiguration sowie die verbundene Anwendung bezieht, werden Metadaten der verbundenen Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c59c3-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="c59c3-168">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="c59c3-169">Klicken Sie auf **Designer**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="c59c3-170">Wählen Sie in der Struktur **Dynamics 365 for Operations\Tabellendatensätze** aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="c59c3-171">Klicken Sie auf **Stamm hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="c59c3-172">Geben Sie im Feld **Tabelle** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c59c3-172">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="c59c3-173">Mehr als zwei Anwendungstabellen wurden nun angeboten, da diese Zuordnung alle Metadaten der verbundenen Anwendung verwenden, die ihr zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c59c3-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="c59c3-174">Klicken Sie auf **Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="c59c3-175">Klicken Sie auf **Überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="c59c3-175">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="c59c3-176">Es wurden erfolgreich Elemente des Datenmodells mit Datenquellenelementen gebunden, die mit Details aus Metadaten der verbundenen Anwendung verwendet, die dieser Zuordnung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c59c3-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="c59c3-177">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-177">Close the page.</span></span> 
11. <span data-ttu-id="c59c3-178">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c59c3-178">Close the page.</span></span> 

<span data-ttu-id="c59c3-179">Wenn Sie diese Modellzuordnung überprüfen müssen, indem Sie Metadaten einer anderen Versionsanwendung verwenden, registrieren Sie eine andere verbundene Anwendung, weisen Sie sie dieser Modellzuordnung zu und prüfen Sie sie anhand der neuen Metadaten.</span><span class="sxs-lookup"><span data-stu-id="c59c3-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>