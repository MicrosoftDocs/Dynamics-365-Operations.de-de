---
title: App für wiederkehrenden Datenexport erstellen
description: Dieser Artikel zeigt das Erstellen einer Microsoft Azure Logic App, die regelmäßig nach einem Zeitplan Daten aus Microsoft Dynamics 365 Human Resources exportiert.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4a963bcfe5932f5642b43751ccd96c472fec0d9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055003"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="a124a-103">App für wiederkehrenden Datenexport erstellen</span><span class="sxs-lookup"><span data-stu-id="a124a-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a124a-104">Dieser Artikel zeigt das Erstellen einer Microsoft Azure Logic App, die regelmäßig nach einem Zeitplan Daten aus Microsoft Dynamics 365 Human Resources exportiert.</span><span class="sxs-lookup"><span data-stu-id="a124a-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="a124a-105">Das Tutorial nutzt die Vorteile der REST-Anwendungsprogrammierschnittstelle (API) des Human Resources-DMF-Pakets, um die Daten zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="a124a-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="a124a-106">Nachdem die Daten exportiert wurden, speichert die Logic App das exportierte Datenpaket in einem Microsoft OneDrive for Business-Ordner.</span><span class="sxs-lookup"><span data-stu-id="a124a-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="a124a-107">Geschäftsszenario</span><span class="sxs-lookup"><span data-stu-id="a124a-107">Business scenario</span></span>

<span data-ttu-id="a124a-108">In einem typischen Geschäftsszenario für Microsoft Dynamics 365-Integrationen müssen Daten regelmäßig nach einem festen Zeitplan in ein nachgeschaltetes System exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="a124a-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="a124a-109">Dieses Tutorial zeigt, wie Sie alle Arbeitskraft-Datensätze von Microsoft Dynamics 365 Human Resources exportieren und die Liste der Arbeitskräfte in einem OneDrive for Business-Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="a124a-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="a124a-110">Die spezifischen Daten, die in diesem Tutorial exportiert werden, sowie das Ziel der exportierten Daten sind nur Beispiele.</span><span class="sxs-lookup"><span data-stu-id="a124a-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="a124a-111">Sie können sie einfach ändern und an Ihre Unternehmensanforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="a124a-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="a124a-112">Verwendete Technologien</span><span class="sxs-lookup"><span data-stu-id="a124a-112">Technologies used</span></span>

<span data-ttu-id="a124a-113">In diesem Tutorial werden die folgenden Technologien verwendet:</span><span class="sxs-lookup"><span data-stu-id="a124a-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="a124a-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**- Die Stammdatenquelle für die zu exportierenden Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="a124a-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="a124a-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Die Technologie zur Orchestrierung und Planung des wiederkehrenden Exports.</span><span class="sxs-lookup"><span data-stu-id="a124a-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="a124a-116">**[Connector](/azure/connectors/apis-list)** – Die Technologie, mit der die Logic App mit den erforderlichen Endpunkten verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="a124a-116">**[Connectors](/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="a124a-117">[HTTP mit Azure AD](/connectors/webcontents/)-Connector</span><span class="sxs-lookup"><span data-stu-id="a124a-117">[HTTP with Azure AD](/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="a124a-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness)-Connector</span><span class="sxs-lookup"><span data-stu-id="a124a-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="a124a-119">**[DMF-Paket REST-API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – Die Technologie, die zum Auslösen des Exports und zum Überwachen des Fortschritts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a124a-119">**[DMF package REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="a124a-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – Das Ziel für die exportierten Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="a124a-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a124a-121">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a124a-121">Prerequisites</span></span>

<span data-ttu-id="a124a-122">Bevor Sie mit der Übung in diesem Tutorial beginnen, muss Folgendes gegeben sein:</span><span class="sxs-lookup"><span data-stu-id="a124a-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="a124a-123">Eine Human Resources-Umgebung, die über Berechtigungen auf Administratorebene in der Umgebung verfügt</span><span class="sxs-lookup"><span data-stu-id="a124a-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="a124a-124">Ein [Azure-Abonnement](https://azure.microsoft.com/free/), um die Logic App zu hosten</span><span class="sxs-lookup"><span data-stu-id="a124a-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="a124a-125">Übung</span><span class="sxs-lookup"><span data-stu-id="a124a-125">The exercise</span></span>

<span data-ttu-id="a124a-126">Am Ende dieser Übung steht Ihnen eine Logic App zur Verfügung, die mit Ihrer Human Resources-Umgebung und Ihrem OneDrive for Business-Konto verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a124a-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="a124a-127">Die Logic App exportiert ein Datenpaket aus Human Resources. Warten Sie, bis der Export abgeschlossen ist. Laden Sie das exportierte Datenpaket herunter und speichern Sie das Datenpaket im OneDrive for Business-Ordner, den Sie angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a124a-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="a124a-128">Die fertige Logic App ähnelt der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="a124a-128">The completed logic app will resemble the following illustration.</span></span>

![Übersicht über die Logic App](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="a124a-130">Schritt 1: Erstellen eines Datenexportprojekts in Human Resources</span><span class="sxs-lookup"><span data-stu-id="a124a-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="a124a-131">Erstellen Sie in Human Resources ein Datenexportprojekt, das Arbeitskräfte exportiert.</span><span class="sxs-lookup"><span data-stu-id="a124a-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="a124a-132">Nennen Sie das Projekt **Export Workers** und stellen Sie sicher, dass die Option **Datenpaket generieren** auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="a124a-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="a124a-133">Fügen Sie eine einzelne Entität (**Arbeitskraft**) zum Projekt hinzu und wählen Sie das Format aus, in das exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a124a-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="a124a-134">(Microsoft Excel-Format wird in diesem Tutorial verwendet.)</span><span class="sxs-lookup"><span data-stu-id="a124a-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Export Workers-Datenprojekt](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="a124a-136">Merken Sie sich den Namen des Datenexportprojekts.</span><span class="sxs-lookup"><span data-stu-id="a124a-136">Remember the name of the data export project.</span></span> <span data-ttu-id="a124a-137">Sie benötigen ihn, wenn Sie im nächsten Schritt die Logic App erstellen.</span><span class="sxs-lookup"><span data-stu-id="a124a-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="a124a-138">Schritt 2: Erstellen der Logic App</span><span class="sxs-lookup"><span data-stu-id="a124a-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="a124a-139">Der Großteil der Übung besteht darin, die Logic App zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a124a-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="a124a-140">Erstellen Sie im Azure-Portal eine Logic App.</span><span class="sxs-lookup"><span data-stu-id="a124a-140">In the Azure portal, create a logic app.</span></span>

    ![Seite zur Erstellung der Logic App](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="a124a-142">Beginnen Sie im Logic Apps Designer mit einer leeren Logic App.</span><span class="sxs-lookup"><span data-stu-id="a124a-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="a124a-143">Fügen Sie einen [Auslöser für einen Serienzeitplan](/azure/connectors/connectors-native-recurrence) hinzu, um die Logic App alle 24 Stunden (oder nach einem Zeitplan Ihrer Wahl) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a124a-143">Add a [Recurrence Schedule trigger](/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Dialogfeld „Wiederholung“](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="a124a-145">Rufen Sie die [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF-REST-API zum Planen des Exports Ihres Datenpakets auf.</span><span class="sxs-lookup"><span data-stu-id="a124a-145">Call the [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="a124a-146">Verwenden Sie die Aktion für **HTTP-Anfrage aufrufen** über den HTTP mit Azure AD-Connector auf.</span><span class="sxs-lookup"><span data-stu-id="a124a-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="a124a-147">**Basisressourcen-URL:** Die URL Ihrer Human Resources-Umgebung (keine Pfad-/Namespace-Informationen einschließen.)</span><span class="sxs-lookup"><span data-stu-id="a124a-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="a124a-148">**Azure AD Ressourcen-URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="a124a-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="a124a-149">Der Human Resources-Dienst stellt noch keinen Connector bereit, der alle APIs verfügbar macht, aus denen die REST-API des DMF-Pakets besteht, beispielsweise **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a124a-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="a124a-150">Stattdessen müssen Sie die APIs mithilfe von rohen HTTPS-Anforderungen über den HTTP mit Azure AD-Connector aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a124a-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="a124a-151">Dieser Connector verwendet Azure Active Directory (Azure AD) zur Authentifizierung und Autorisierung gegenüber Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a124a-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP mit Azure AD-Connector](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="a124a-153">Melden Sie sich in der Human Resources-Umgebung über HTTP mit Azure AD-Connector an.</span><span class="sxs-lookup"><span data-stu-id="a124a-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="a124a-154">Richten Sie eine HTTP-**POST**-Anforderungen ein, um die **ExportToPackage**-DMF-REST-API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a124a-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="a124a-155">**Methode:** POST</span><span class="sxs-lookup"><span data-stu-id="a124a-155">**Method:** POST</span></span>
        - <span data-ttu-id="a124a-156">**URL der Anforderung:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="a124a-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="a124a-157">**Text der Anforderung:**</span><span class="sxs-lookup"><span data-stu-id="a124a-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktion „HTTP-Anforderung aufrufen“](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="a124a-159">Möglicherweise möchten Sie die einzelnen Schritte umbenennen, damit deren Bedeutung klarer wird als der Standardname **HTTP-Anforderung aufrufen**.</span><span class="sxs-lookup"><span data-stu-id="a124a-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="a124a-160">Sie können diesen Schritt beispielsweise umbenennen in **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="a124a-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="a124a-161">[Initialisieren Sie eine Variable](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable), um den Ausführungsstatus der **ExportToPackage**-Anforderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a124a-161">[Initialize a variable](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Aktion „Variable initialisieren“](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="a124a-163">Warten Sie, bis der Ausführungsstatus des Datenexports **Erfolgreich** ist.</span><span class="sxs-lookup"><span data-stu-id="a124a-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="a124a-164">Fügen Sie eine [Bis-Schleife](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) hinzu, die wiederholt wird, bis der Wert der **ExecutionStatus**-Variable **Erfolgreich** lautet.</span><span class="sxs-lookup"><span data-stu-id="a124a-164">Add an [Until loop](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="a124a-165">Fügen Sie eine **Verzögern**-Aktion hinzu, durch die fünf Sekunden gewartet wird, bevor der aktuelle Ausführungsstatus des Exports abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a124a-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Container für Bis-Schleife](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="a124a-167">Setzen Sie den Grenzwert auf **15**, damit maximal 75 Sekunden gewartet wird (15 Iterationen × 5 Sekunden), bis der Export abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a124a-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="a124a-168">Wenn Ihr Export länger dauert, passen Sie den Grenzwert entsprechend an.</span><span class="sxs-lookup"><span data-stu-id="a124a-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="a124a-169">Fügen Sie eine **HTTP-Anforderung aufrufen**-Aktion zum Aufrufen der [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus)-DMF-REST-API hinzu und setzen Sie die **ExecutionStatus**-Variable auf das Ergebnis der **GetExecutionSummaryStatus**-Antwort.</span><span class="sxs-lookup"><span data-stu-id="a124a-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="a124a-170">Dieses Beispiel führt keine Fehlerprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="a124a-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="a124a-171">Die **GetExecutionSummaryStatus**-API kann nicht erfolgreiche Terminalzustände zurückgeben (also andere Zustände als **Erfolgreich**).</span><span class="sxs-lookup"><span data-stu-id="a124a-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="a124a-172">Weitere Informationen finden Sie in der [API-Dokumentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="a124a-172">For more information, see the [API documentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="a124a-173">**Methode:** POST</span><span class="sxs-lookup"><span data-stu-id="a124a-173">**Method:** POST</span></span>
        - <span data-ttu-id="a124a-174">**URL der Anforderung:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="a124a-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="a124a-175">**Hauptteil der Anforderung:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="a124a-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="a124a-176">Möglicherweise müssen Sie den **Hauptteil der Anforderung**-Wert in der Codeansicht oder im Funktionseditor im Designer eingeben.</span><span class="sxs-lookup"><span data-stu-id="a124a-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Aktion „HTTP-Anforderung aufrufen 2“](media/integration-logic-app-get-execution-status-step.png)

        ![Aktion „Variable festlegen“](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="a124a-179">Der Wert für die **Variable festlegen**-Aktion (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) unterscheidet sich vom Wert für den **HTTP-Anforderung aufrufen 2**-Hauptteilwert, auch wenn der Designer die Werte auf gleiche Weise anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a124a-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="a124a-180">Erhalten Sie die Download-URL für das exportierte Paket.</span><span class="sxs-lookup"><span data-stu-id="a124a-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="a124a-181">Fügen Sie eine **HTTP-Anforderung aufrufen**-Aktion hinzu, um die [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl)-DMF-REST-API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a124a-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="a124a-182">**Methode:** POST</span><span class="sxs-lookup"><span data-stu-id="a124a-182">**Method:** POST</span></span>
        - <span data-ttu-id="a124a-183">**URL der Anforderung:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="a124a-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="a124a-184">**Hauptteil der Anforderung:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="a124a-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL-Aktion](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="a124a-186">Laden Sie das exportierte Paket herunter.</span><span class="sxs-lookup"><span data-stu-id="a124a-186">Download the exported package.</span></span>

    - <span data-ttu-id="a124a-187">Fügen Sie eine HTTP-**GET**-Anforderung (eine integrierte [HTTP-Connector-Aktion](/azure/connectors/connectors-native-http)) hinzu, um das Paket von der URL herunterzuladen, die im vorherigen Schritt zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a124a-187">Add an HTTP **GET** request (a built-in [HTTP connector action](/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="a124a-188">**Methode:** GET</span><span class="sxs-lookup"><span data-stu-id="a124a-188">**Method:** GET</span></span>
        - <span data-ttu-id="a124a-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="a124a-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="a124a-190">Möglicherweise müssen Sie den **URI**-Wert in der Codeansicht oder im Funktionseditor im Designer eingeben.</span><span class="sxs-lookup"><span data-stu-id="a124a-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GET-Aktion](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="a124a-192">Diese Anforderung erfordert keine zusätzliche Authentifizierung, da die URL, die die **GetExportedPackageUrl**-API zurückgibt, ein Token für gemeinsame Zugriffssignaturen enthält, mit dem der Zugriff zum Herunterladen der Datei gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="a124a-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="a124a-193">Speichern Sie das heruntergeladene Paket mit dem [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness)-Connector.</span><span class="sxs-lookup"><span data-stu-id="a124a-193">Save the downloaded package by using the [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="a124a-194">Fügen Sie eine OneDrive for Business [Datei erstellen](/connectors/onedriveforbusinessconnector/#create-file)-Aktion hinzu.</span><span class="sxs-lookup"><span data-stu-id="a124a-194">Add a OneDrive for Business [Create File](/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="a124a-195">Stellen Sie eine Verbindung zu Ihrem OneDrive for Business-Konto her, wenn erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a124a-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="a124a-196">**Ordnerpfad:** Ein Ordner Ihrer Wahl</span><span class="sxs-lookup"><span data-stu-id="a124a-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="a124a-197">**Dateiname:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="a124a-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="a124a-198">**Dateiinhalt:** Der Hauptteil aus dem vorherigen Schritt (dynamischer Inhalt)</span><span class="sxs-lookup"><span data-stu-id="a124a-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Aktion „Datei erstellen“](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="a124a-200">Schritt 3: Testen der Logic App</span><span class="sxs-lookup"><span data-stu-id="a124a-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="a124a-201">Um Ihre Logic App zu testen, wählen Sie im Designer **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="a124a-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="a124a-202">Sie werden sehen, dass die Schritte der Logic App ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a124a-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="a124a-203">Nach 30 bis 40 Sekunden sollte die Logic App-Ausführung beendet sein und Ihr OneDrive for Business-Ordner sollte eine neue Paketdatei enthalten, die die exportierten Arbeitskräfte enthält.</span><span class="sxs-lookup"><span data-stu-id="a124a-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="a124a-204">Wenn für einen Schritt ein Fehler gemeldet wird, wählen Sie den fehlgeschlagenen Schritt im Designer aus und überprüfen Sie die Felder **Eingaben** und **Ausgaben** für diesen.</span><span class="sxs-lookup"><span data-stu-id="a124a-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="a124a-205">Debuggen Sie und passen Sie den Schritt nach Bedarf an, um die Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="a124a-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="a124a-206">Die folgende Abbildung zeigt, wie der Logic Apps Designer aussieht, wenn alle Schritte der Logic App erfolgreich ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="a124a-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Erfolgreiche Ausführung der Logic App](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="a124a-208">Summe</span><span class="sxs-lookup"><span data-stu-id="a124a-208">Summary</span></span>

<span data-ttu-id="a124a-209">In diesem Tutorial haben Sie gelernt, wie Sie mit einer Logic App Daten aus Human Resources exportieren und die exportierten Daten in einem OneDrive for Business-Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="a124a-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="a124a-210">Sie können die Schritte dieses Tutorials nach Bedarf an Ihre geschäftlichen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="a124a-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]