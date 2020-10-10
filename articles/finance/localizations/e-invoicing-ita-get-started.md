---
title: Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien
description: Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Italien in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management erleichtern.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ea0408f4ef72bf77a0659799075338e4e6b2aa30
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835959"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="ebe5b-103">Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien</span><span class="sxs-lookup"><span data-stu-id="ebe5b-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="ebe5b-104">Das Add-On für die elektronische Rechnungsstellung für Italien unterstützt derzeit möglicherweise nicht alle Funktionen, die für elektronische Rechnungen in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="ebe5b-105">Dieses Thema enthält Informationen, die Ihnen den Einstieg in das Add-On für die elektronische Rechnungsstellung für Italien erleichtern.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="ebe5b-106">Es führt Sie durch die Konfigurationsschritte, die in Regulatory Configuration Services (RCS) sowie in Finance länderabhängig sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="ebe5b-107">Es führt Sie auch durch den Übermittlungsprozess für elektronische Rechnungen, die über den Service im für Italien spezifischen Format **FatturaPA** erstellt werden, und es wird erläutert, wie die Ergebnisse der Verarbeitung überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ebe5b-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ebe5b-108">Prerequisites</span></span>

<span data-ttu-id="ebe5b-109">Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie die Schritte in [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md) ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="ebe5b-110">RCS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ebe5b-110">RCS setup</span></span>

<span data-ttu-id="ebe5b-111">Während der RCS-Einrichtung führen Sie folgende Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="ebe5b-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="ebe5b-112">Importieren Sie die Funktion für die elektronische Rechnungsstellung für den Export elektronischer Kundenrechnungen im Format **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="ebe5b-113">Überprüfen Sie die Formatkonfigurationen, die zum Generieren, Übermitteln und Empfangen von Antworten zu elektronischen Rechnungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="ebe5b-114">Konfigurieren Sie die Ereignisse, die die Szenarien für die elektronische Rechnungsübermittlung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="ebe5b-115">Veröffentlichen Sie die Funktion für die elektronische Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="ebe5b-116">„Die Funktion für die elektronische Rechnungsstellung“ ist der generische Name für die Ressource, die so konfiguriert und veröffentlicht ist, dass sie den Add-On-Server für die elektronische Rechnungsstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="ebe5b-117">In diesem Fall ist der Export elektronischer Kundenrechnungen die Funktion für die elektronische Rechnungsstellung, die Sie einrichten werden.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="ebe5b-118">Importieren der Funktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="ebe5b-119">Melden Sie sich bei Ihrem RCS-Konto an.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="ebe5b-120">Wählen Sie im Arbeitsbereich **Globalisierungsfunktionen** im Abschnitt **Funktionen** die Kachel **Elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="ebe5b-121">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** die Option **Importieren** aus, um die Funktion für die elektronische Rechnungsstellung aus dem globalen Repository zu importieren.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ebe5b-122">Wenn die Liste der verfügbaren Funktionen nicht angezeigt wird, wählen Sie **Synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="ebe5b-123">Wählen Sie die Funktion **Elektronische Rechnungen exportieren (IT)** aus und wählen Sie dann **Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Importieren der Funktion „Elektronische Rechnungen exportieren (IT)“](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="ebe5b-125">Wenn Sie die Funtion **Elektronische Rechnungen exportieren (IT)** aus dem globalen Repository importieren, werden auch alle Einstellungen importiert, die in den nächsten Abschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="ebe5b-126">Erstellen einer neuen Version der Funktion „Elektronische Rechnungen exportieren (IT)“</span><span class="sxs-lookup"><span data-stu-id="ebe5b-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="ebe5b-127">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Hinzufügen einer neuen Version der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="ebe5b-129">Als Nächstes konfigurieren Sie die EB-Formate (Elektronische Berichterstellung), die der Funktion für die elektronische Rechnungsstellung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="ebe5b-130">Wählen Sie auf der Registerkarte **Konfigurationen** die Option **Hinzufügen** aus, um die Konfigurationsversionen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Verwalten der Konfigurationsversionen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="ebe5b-132">In diesem Schritt fügen Sie die EB-Formate verschiedener Dateien hinzu, die zum Exportieren elektronischer Rechnungen in Italien verwendet werden, und konfigurieren sie.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="ebe5b-133">Verwenden Sie in Italien für elektronische Rechnungen im FatturaPA-Format entweder die folgenden Standardkonfigurationen oder die tatsächlich angepassten Konfigurationen, die Sie für die elektronische Rechnungsstellung verwenden:</span><span class="sxs-lookup"><span data-stu-id="ebe5b-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="ebe5b-134">Verkaufsrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="ebe5b-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="ebe5b-135">Projektrechnung (IT)</span><span class="sxs-lookup"><span data-stu-id="ebe5b-135">Project invoice (IT)</span></span>

    <span data-ttu-id="ebe5b-136">Wenn Sie eine Funktion für die elektronische Rechnungsstellung erstellen, die von einer anderen Funktion für die elektronische Rechnungsstellung abgeleitet ist, werden alle EB-Formate von der ursprünglichen Funktion geerbt.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="ebe5b-137">Wählen Sie eine bestimmte Dateikonfiguration im ER-Format aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="ebe5b-138">Wählen Sie **Bearbeiten** oder **Anzeigen** aus, um die Seite **Formatdesigner** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Öffnen der Seite „Formatdesigner“](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="ebe5b-140">Verwenden Sie die Seite **Formatdesigner**, um die EB-Formatkonfigurationen für Dateien zu bearbeiten und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Formatdesignerseite](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="ebe5b-142">Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="ebe5b-143">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** entweder **Hinzufügen**, **Löschen** oder **Bearbeiten** aus, um die Einrichtungen der Funktion für die elektronische Rechnungsstellung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Verwalten der Einrichtungen der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="ebe5b-145">In diesem Schritt konfigurieren Sie die Ereignisse, die für elektronische Rechnungen gelten, einschließlich der Generierung der XML-Ausgabedateien im Format **FatturaPA** und digitaler Signaturen (falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="ebe5b-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="ebe5b-146">Konfigurieren der Funktionseinrichtung „Verkaufsrechnung“</span><span class="sxs-lookup"><span data-stu-id="ebe5b-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="ebe5b-147">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Einrichtungen** in der Spalte **Funktionseinrichtung** die Option **Verkaufsrechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="ebe5b-148">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-148">Select **Edit**.</span></span>
3. <span data-ttu-id="ebe5b-149">Wählen Sie auf der Seite **Einrichtung der Funktionsversion** die Registerkarte **Aktionen** aus, um die Liste der Aktionen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="ebe5b-150">Aktionen definieren eine Liste von Vorgängen, die nacheinander ausgeführt werden müssen, um die vollständige Ausführung des Ereignisses zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Registerkarte „Aktionen“](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="ebe5b-152">Aktivitätskennung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-152">Action ID</span></span> | <span data-ttu-id="ebe5b-153">Aktivitätsname</span><span class="sxs-lookup"><span data-stu-id="ebe5b-153">Action name</span></span>        | <span data-ttu-id="ebe5b-154">Aktivitätsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="ebe5b-155">1</span><span class="sxs-lookup"><span data-stu-id="ebe5b-155">1</span></span>         | <span data-ttu-id="ebe5b-156">Umwandeln des Dokuments</span><span class="sxs-lookup"><span data-stu-id="ebe5b-156">Transform document</span></span> | <span data-ttu-id="ebe5b-157">Erstellen Sie die XML-Datei der elektronischen Rechnung im Format **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="ebe5b-158">2</span><span class="sxs-lookup"><span data-stu-id="ebe5b-158">2</span></span>         | <span data-ttu-id="ebe5b-159">Dokument signieren</span><span class="sxs-lookup"><span data-stu-id="ebe5b-159">Sign document</span></span>      | <span data-ttu-id="ebe5b-160">Wenden Sie die digitale Signatur auf die XML-Datei an.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="ebe5b-161">Wählen Sie die Registerkarte **Anwendbarkeitsregeln** aus, um die Anwendbarkeitsregeln anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="ebe5b-162">Anwendbarkeitsregeln definieren den Kontext, in dem die Aktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-162">Applicability rules define the context where the action will be run.</span></span>

    ![Registerkarte „Anwendbarkeitsregeln“](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="ebe5b-164">Wählen Sie die Registerkarte **Variablen** aus, um die Variablen anzuzeigen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Registerkarte „Variablen“](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="ebe5b-166">Definieren Sie die öffentlichen Variablen, die zum Ausführen der Aktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="ebe5b-167">Konfigurieren der Funktionseinrichtung „Projektrechnung“</span><span class="sxs-lookup"><span data-stu-id="ebe5b-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="ebe5b-168">Die Schritte und Einstellungen, die zum Konfigurieren der Funktionseinrichtung **Projektrechnung** erforderlich sind, sind den Schritten und Einstellungen für die Funktionseinrichtung **Verkaufsrechnung** sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="ebe5b-169">Wenn Sie mit Projektrechnungen arbeiten, lesen Sie die Prozeduren für Verkaufsrechnungen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="ebe5b-170">Zuweisen der Funktion für die elektronische Rechnungsstellung zur Umgebung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="ebe5b-171">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Umgebungen** die Option **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="ebe5b-172">Wählen Sie im Feld **Umgebung** die Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="ebe5b-173">Wählen Sie im Feld **Gültig ab** das Datum aus, an dem die Umgebung wirksam werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="ebe5b-174">Wählen Sie **Aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-174">Select **Enable**.</span></span> 

![Aktivieren der Umgebung für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="ebe5b-176">Veröffentlichen der Funktion für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="ebe5b-177">Sie können die Funktion für die elektronische Rechnungsstellung veröffentlichen, indem Sie den Versionsstatus in **Abgeschlossen** oder **Veröffentlicht** ändern.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="ebe5b-178">Ändern des Versionsstatus in „Abgeschlossen“</span><span class="sxs-lookup"><span data-stu-id="ebe5b-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="ebe5b-179">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Entwurf** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="ebe5b-180">Wählen Sie **Status ändern \>Abschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="ebe5b-181">Ändern des Versionsstatus in „Veröffentlicht“</span><span class="sxs-lookup"><span data-stu-id="ebe5b-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="ebe5b-182">Wählen Sie auf der Seite **Funktionen für die elektronische Rechnungsstellung** auf der Registerkarte **Versionen** die Version der Funktion für die elektronische Rechnungsstellung mit dem Status **Abgeschlossen** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="ebe5b-183">Wählen Sie **Status ändern \> Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-183">Select **Change status \> Publish**.</span></span>

![Ändern des Status der Funktion für die elektronische Rechnungsstellung](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="ebe5b-185">Einrichten der Integration des Add-Ons für die elektronische Rechnungsstellung in Finance</span><span class="sxs-lookup"><span data-stu-id="ebe5b-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="ebe5b-186">Während der Einrichtung von Finance führen Sie folgende Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="ebe5b-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="ebe5b-187">Importieren Sie das EB-Datenmodell, die EB-Datenmodellzuordnung und die Kontextkonfigurationen für elektronische Rechnungen im FatturaPA-Format.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="ebe5b-188">Konfigurieren Sie das Zertifikat, das zum digitalen Signieren elektronischer Rechnungen in Italien erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="ebe5b-189">Importieren des EB-Datenmodells, der Datenmodellzuordnung und der Formate</span><span class="sxs-lookup"><span data-stu-id="ebe5b-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="ebe5b-190">Überprüfen Sie im Arbeitsbereich **Elektronische Berichterstellung**, ob der Konfigurationsanbieter **Geschäftsdokumentservice** auf **Aktiv** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="ebe5b-191">Wählen Sie **Repositorys** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="ebe5b-192">Wählen Sie **Globale Ressource \> Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="ebe5b-193">Importieren Sie **Rechnungsmodell**, **Rechnungsmodellzuordnung** und **Kontextmodell Debitorenrechnung**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="ebe5b-194">Aktivieren der Funktion zum Exportieren von elektronischen Kundenrechnungen für Italien</span><span class="sxs-lookup"><span data-stu-id="ebe5b-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="ebe5b-195">Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="ebe5b-196">Aktivieren Sie auf der Registerkarte **Funktionen** das Kontrollkästchen **Aktivieren** in der Zeile für Funktionsreferenz **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Aktivieren der FatturaPA-Funktion](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="ebe5b-198">Konfigurieren elektronischer Dokumente</span><span class="sxs-lookup"><span data-stu-id="ebe5b-198">Configure electronic documents</span></span>

1. <span data-ttu-id="ebe5b-199">Navigieren Sie zu **Organisationsverwaltung \> Einrichtung \> Parameter elektronischer Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="ebe5b-200">Wählen Sie auf der Registerkarte **Elektronisches Dokument** die Option **Hinzufügen** aus und geben Sie die Tabellen ein, die zum Generieren elektronischer Rechnungen in Italien erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="ebe5b-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="ebe5b-201">**Tabellenname:** Debitorenrechnungserfassung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="ebe5b-202">**Tabellenname:** Projektrechnung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="ebe5b-203">Definieren Sie für jede Tabelle einen zugehörigen Dokumentkontext:</span><span class="sxs-lookup"><span data-stu-id="ebe5b-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="ebe5b-204">Wählen Sie für **Debitorenrechnungserfassung** die Option **Kontext Debitorenrechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="ebe5b-205">Wählen Sie für **Projektrechnung** die Option **Kontext Projektrechnung** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Einrichten von Antworttypen](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="ebe5b-207">Verarbeitung der elektronischen Rechnung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-207">Electronic invoice processing</span></span>

<span data-ttu-id="ebe5b-208">Während der Verarbeitung in Finance führen Sie folgende Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="ebe5b-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="ebe5b-209">Generieren elektronischer Rechnungen in Italien über das Add-On für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="ebe5b-210">Anzeigen der Ausführungsprotokolle und Überprüfen der Ergebnisse der Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="ebe5b-211">Generieren elektronischer Rechnungen</span><span class="sxs-lookup"><span data-stu-id="ebe5b-211">Generate electronic invoices</span></span>

<span data-ttu-id="ebe5b-212">Nachdem Sie die Funktion **Integration des konfigurierbaren Add-Ons für die elektronische Rechnungsstellung** und die Funktion **IT00036** aktiviert haben, kann der alte Prozess von Finance zum Generieren elektronischer Rechnungen in Italien nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="ebe5b-213">Er wird durch einen neuen Prozess mit dem Namen **Elektronische Dokumente übermitteln** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="ebe5b-214">Sie können die Dokumente manuell übermitteln, basierend auf Ihrer Nachfrage nach elektronischen Rechnungsdokumenten.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="ebe5b-215">Bevor Sie fortfahren, stellen Sie sicher, dass die für elektronische Rechnungen in Italien erforderliche Einrichtung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="ebe5b-216">Weitere Informationen finden Sie unter [Elektronische Rechnungen für Kunden](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="ebe5b-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="ebe5b-217">Beachten Sie, dass einige der in diesem Thema beschriebenen Einrichtungsschritte aufgrund der Aktivierung des Add-Ons für die elektronische Rechnungsstellung möglicherweise nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="ebe5b-218">Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Elektronische Dokumente übermitteln**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="ebe5b-219">Legen Sie für die erste Übermittlung irgendeines Dokuments die Option **Dokumente erneut übermitteln** auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="ebe5b-220">Wenn Sie ein Dokument erneut über den Service übermitteln müssen, legen Sie diese Option auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="ebe5b-221">Wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, um das Dialogfeld **Anfrage** zu öffnen, in dem Sie eine Abfrage erstellen können, um Dokumente für die Übermittlung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Dialogfeld „Elektronische Dokumente übermitteln“](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="ebe5b-223">Filterabfrage</span><span class="sxs-lookup"><span data-stu-id="ebe5b-223">Filter query</span></span>

1. <span data-ttu-id="ebe5b-224">Konfigurieren Sie im Dialogfeld **Anfrage** die Filterbedingungen für Verkaufs- und Projektrechnungen oder lassen Sie die Bedingungen leer, um alle nicht übermittelten Rechnungen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Einrichten von Filterkriterien für Übermittlungen](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="ebe5b-226">Wählen Sie **OK** aus, um das Dialogfeld **Anfrage** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="ebe5b-227">Wählen Sie **OK** aus, um die ausgewählten Dokumente zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="ebe5b-228">! [HINWEIS] Bei Ihrem ersten Versuch, ein Dokument über den Service zu übermitteln, werden Sie aufgefordert, die Verbindung mit dem Add-On für die elektronische Rechnungsstellung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="ebe5b-229">Wählen Sie **Hier klicken, um eine Verbindung mit dem Electronic Document Submission Service herzustellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="ebe5b-230">Anzeigen von Übermittlungsprotokollen</span><span class="sxs-lookup"><span data-stu-id="ebe5b-230">View submission logs</span></span>

<span data-ttu-id="ebe5b-231">Sie können die Übermittlungsprotokolle für alle übermittelten Dokumente anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="ebe5b-232">Navigieren Sie zu **Organisationsverwaltung \> Periodisch \> Elektronische Dokumente \> Übermittlungsprotokoll für elektronische Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="ebe5b-233">Wählen Sie im Feld **Dokumenttyp** entweder **Debitorenrechnungserfassung** oder **Projektrechnung** aus, um nach den erforderlichen elektronischen Dokumenten zu filtern.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Auswählen eines Dokumenttyps, um die Übermittlungsprotokolle anzuzeigen](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="ebe5b-235">Der Wert, der in der Spalte **Übermittlungsstatus** angezeigt wird, gibt den Status des Übermittlungsprozesses an.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="ebe5b-236">Er zeigt an, ob der Prozess wie konfiguriert ausgeführt wurde und ob zusätzliche Aktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="ebe5b-237">Wählen Sie im Aktivitätsbereich die Option **Anfragen \> Übermittlungsdetails** aus, um die Details der Ausführungsprotokolle für die Übermittlung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Anzeigen der Details des Übermittlungsprotokolls](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="ebe5b-239">Auf dem Inforegister **Verarbeitungsaktivitäten** können Sie das Ausführungsprotokoll für die Aktionen anzeigen, die in der in RCS eingerichteten Funktionsversion konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="ebe5b-240">Die Spalte **Status** zeigt an, ob die Aktion erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="ebe5b-241">Auf dem Inforegister **Aktionsdateien** können Sie die Zwischendateien anzeigen, die während der Ausführung der Aktionen generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="ebe5b-242">Sie können **Anzeigen** auswählen, um die ausgegebene-XML-Datei im Format **FatturaPA** herunterzuladen und ihren Inhalt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ebe5b-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebe5b-243">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ebe5b-243">Related topics</span></span>

- [<span data-ttu-id="ebe5b-244">Übersicht über das Add-On für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="ebe5b-245">Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="ebe5b-246">Einrichten des Add-Ons für die elektronische Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="ebe5b-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
