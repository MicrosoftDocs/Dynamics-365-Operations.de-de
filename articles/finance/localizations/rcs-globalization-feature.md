---
title: Regulatory Configuration Services (RCS) – Globalisierungsfunktionen
description: In diesem Thema wird erläutert, wie Sie Microsoft Regulatory Configuration Services (RCS) und die das globale nutzen, um die Globalisierungsfunktionen zu erstellen und zu nutzen.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822780"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="ae64b-103">Regulatory Configuration Services (RCS) – Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae64b-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae64b-104">Mit Microsoft Regulatory Configuration Services (RCS) können Sie eine Globalisierungsfunktion erstellen, die in Globalisierungsdiensten verwendet werden kann, z. B. als E-Invoicing-Service.</span><span class="sxs-lookup"><span data-stu-id="ae64b-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="ae64b-105">Mit RCS können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="ae64b-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="ae64b-106">Definieren Sie verwandte Komponenten einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="ae64b-106">Define related components of a feature.</span></span>
- <span data-ttu-id="ae64b-107">Verwalten Sie den Lebenszyklusfunktion über den Status einer Funktion.</span><span class="sxs-lookup"><span data-stu-id="ae64b-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="ae64b-108">Stellen Sie eine Funktion für definierte Umgebungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ae64b-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="ae64b-109">Teilen Sie eine Funktion mit anderen Organisationen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="ae64b-110">In den folgenden Verfahren wird erläutert, wie ein Benutzer in RCS eine Globalisierungsfunktion und zugehörige Komponenten hinzufügen, den Status der Funktion aktualisieren und die Funktion verfügbar machen kann, damit sie in Globalisierungsdiensten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae64b-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="ae64b-111">Bevor Sie die Prozeduren ausführen, müssen Sie die Schritte ausführen, die sich auf die folgenden Aufgaben beziehen:</span><span class="sxs-lookup"><span data-stu-id="ae64b-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="ae64b-112">Zugriff auf eine RCS-Instanz.</span><span class="sxs-lookup"><span data-stu-id="ae64b-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="ae64b-113">Konfigurationsanbieter erstellen und aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ae64b-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="ae64b-114">Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ae64b-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="ae64b-115">In Ihren Finance and Operations Apps Instanzen befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="ae64b-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="ae64b-116">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ae64b-117">Wenn keine RCS-Umgebung für Ihr Unternehmen bereitgestellt wurde, klicken Sie auf **Regulatory services – Konfiguration** und folgen Sie den Anweisungen zur Bereitstellung einer RCS-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ae64b-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="ae64b-118">Wenn für Ihr Unternehmen bereits eine RCS-Umgebung bereitgestellt wurde, verwenden Sie die Seiten-URL, um auf die Umgebung zuzugreifen, indem Sie die Anmeldeoption auswählen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="ae64b-119">Aktivieren Sie die Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae64b-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="ae64b-120">Wählen Sie in Ihrer RCS-Instanz die Kachel **Funktionsverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="ae64b-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="ae64b-121">In dem **Funktionsverwaltung** Arbeitsbereich wählen Sie **Globalisierungsfunktionen** in der Liste und wählen Sie dann **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globalisierungsfunktionen in der Funktionsverwaltung](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="ae64b-123">Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae64b-123">Globalization features</span></span>

<span data-ttu-id="ae64b-124">Um eine Globalisierungsfunktion zu verwenden, müssen Sie sie zuerst aus dem globalen Repository importieren und eine eigene Version davon erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="ae64b-125">Es gibt zwei Möglichkeiten, Globalisierungsfunktionen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="ae64b-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="ae64b-126">Fügen Sie eine abgeleitete Funktion hinzu, die auf einer vorhandenen Funktion basiert, die veröffentlicht oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ae64b-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="ae64b-127">Fügen Sie eine neue Funktion hinzu, die Sie von Grund auf neu erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ae64b-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="ae64b-128">Zugreifen auf Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae64b-128">Access Globalization features</span></span>

1. <span data-ttu-id="ae64b-129">Stellen Sie sicher, dass die **Globalisierungsfunktionen** Funktion in der Funktionsverwaltung aktiviert ist wie weiter oben in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ae64b-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="ae64b-130">Öffnen Sie den neuen Arbeitsbereich **Globalisierungsfunktionen** und dann unter **Eigenschaften** wählen Sie die Kachel **elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="ae64b-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Arbeitsbereich für globale Funktionen](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="ae64b-132">Die Seite **Funktionen für die elektronische Rechnungsstellung** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ae64b-132">The **e-Invoicing Features** page is opened.</span></span>

    ![Seite mit den Funktionen für die elektronische Rechnungsstellung](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="ae64b-134">Fügen Sie eine abgeleitete Globalisierungsfunktion hinzu</span><span class="sxs-lookup"><span data-stu-id="ae64b-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="ae64b-135">Sie können eine neue Globalisierungsfunktion hinzufügen, indem Sie sie von einer vorhandenen Funktion ableiten, die veröffentlicht oder freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ae64b-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="ae64b-136">Wählen Sie **Importieren**, um die Seite **Importfunktion aus dem globalen Repository** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Funktion von der globalen Repository-Seite importieren](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="ae64b-138">Wählen Sie **Synchronisieren**, um die neuesten Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae64b-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="ae64b-139">Die synchronisierte Liste enthält Funktionen, die Ihnen entweder zur Verfügung stehen, weil sie von Microsoft veröffentlicht wurden oder weil sie von einem anderen Konfigurationsanbieter für Sie freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Synchronisierte Liste der Funktionen](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="ae64b-141">Wählen Sie in der Liste die zu importierenden Funktionen aus und wählen Sie dann **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="ae64b-142">Sie erhalten eine Nachricht, wenn die ausgewählten Funktionen erfolgreich importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Meldung für erfolgreichen Import](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="ae64b-144">Wählen Sie **Hinzufügen** und dann im Dropdown-Dialogfeld die Option **Basierend auf der vorhandenen Version** aus.</span><span class="sxs-lookup"><span data-stu-id="ae64b-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="ae64b-145">Geben Sie einen Namen und eine Beschreibung für die Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="ae64b-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="ae64b-146">Wählen Sie in der Liste der verfügbaren Funktionen die Basisversion der Funktion aus und wählen Sie dann **Funktion erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Hinzufügen einer abgeleiteten Funktion](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="ae64b-148">Die von Ihnen hinzugefügte Funktion wird erstellt und hat den Status **Entwurf**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Abgeleitete Funktion mit Entwurfsstatus](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="ae64b-150">Überprüfen Sie die Funktionskomponenten, um festzustellen, ob Aktualisierungen erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="ae64b-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="ae64b-151">Überprüfen Sie die Konfigurationen, falls Sie die ER-Formate (Electronic Reporting) und ihre Bindung mit Formatzuordnungen für die Funktion-Version anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="ae64b-152">Überprüfen Sie die Einrichtung, falls Sie die Registerkarte **Aktionen**, die Registerkarte **Anwendbarkeitsregeln** oder die Registerkarte **Variablen** für die Funktion-Version anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="ae64b-153">Auf der Registerkarte **Versionen** wählen Sie **Gültig ab** Datum aus und geben Sie eine Beschreibung ein, wenn das Feld **Beschreibung** leer ist.</span><span class="sxs-lookup"><span data-stu-id="ae64b-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="ae64b-154">Wählen Sie **Status ändern**, um die Funktion zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="ae64b-155">Abgeschlossene Funktionen können für eine bestimmte Umgebung verfügbar gemacht werden, damit sie in Globalisierungsdiensten verwendet oder im globalen Repository veröffentlicht werden können.</span><span class="sxs-lookup"><span data-stu-id="ae64b-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="ae64b-156">Funktionen, die einen **Funktionsversionsstatus**-Wert **Veröffentlicht** haben, können mit externen Organisationen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="ae64b-157">Fügen Sie eine neue Globalisierungsfunktion hinzu</span><span class="sxs-lookup"><span data-stu-id="ae64b-157">Add a new Globalization feature</span></span>

<span data-ttu-id="ae64b-158">Sie können eine neue Globalisierungsfunktion hinzufügen, indem Sie sie von Grund auf neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="ae64b-159">Auf der Seite **Importfunktion aus dem globalen Repository** wählen Sie **Hinzufügen** und dann im Dropdown-Dialogfeld die Option **Neue Funktion** aus.</span><span class="sxs-lookup"><span data-stu-id="ae64b-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="ae64b-160">Geben Sie einen Namen und eine Beschreibung für die Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="ae64b-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="ae64b-161">Wählen Sie **Funktion erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-161">Select **Create feature**.</span></span>

    ![Hinzufügen einer neuen Funktion](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="ae64b-163">Auf der Registerkarte **Versionen** wählen Sie **Gültig ab** Datum und wählen Sie dann **Status ändern**, um die Funktion zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="ae64b-164">Abgeschlossene Funktionen können für eine bestimmte Umgebung verfügbar gemacht werden, damit sie in Globalisierungsdiensten verwendet oder im globalen Repository veröffentlicht werden können.</span><span class="sxs-lookup"><span data-stu-id="ae64b-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="ae64b-165">Funktionen, die einen **Funktionsversionsstatus**-Wert **Veröffentlicht** haben, können mit externen Organisationen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="ae64b-166">Funktionskomponenten-Übersicht</span><span class="sxs-lookup"><span data-stu-id="ae64b-166">Feature component overview</span></span>

<span data-ttu-id="ae64b-167">Globalisierungsfunktionen bestehen aus mehreren Komponenten:</span><span class="sxs-lookup"><span data-stu-id="ae64b-167">Globalization features have several components:</span></span>

- <span data-ttu-id="ae64b-168">**Version** – Diese Komponente unterstützt die Verwaltung des Funktionslebenszyklus und ermöglicht Benutzern die Verwaltung des Status für verschiedene Versionen der Funktion.</span><span class="sxs-lookup"><span data-stu-id="ae64b-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="ae64b-169">**Konfigurationen** – Mit dieser Komponente können Benutzer verwandte ER-Formate und Formatzuordnungen verwalten, anzeigen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ae64b-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="ae64b-170">**Einrichtungen** – Mit dieser Komponente können Benutzer von Globalisierungsdiensten, z. B. einem E-Invoicing-Dienst, die Einrichtung der zugehörigen Funktionsversion verwalten.</span><span class="sxs-lookup"><span data-stu-id="ae64b-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="ae64b-171">Daher unterstützt es die flexible Erstellung von Kommunikations- und Antwortregeln.</span><span class="sxs-lookup"><span data-stu-id="ae64b-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="ae64b-172">**Umgebung** – Mit dieser Komponente können Benutzer von Globalisierungsdiensten, z. B. einem E-Invoicing-Dienst, die Umgebung verwalten, in der die Einrichtung der Funktions-Version verwendet wird, und den Benutzern, die Zugriff darauf haben, die Berechtigung erteilen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="ae64b-173">**Organisationen** – Mit dieser Komponente können Benutzer die Funktion für externe Organisationen freigeben.</span><span class="sxs-lookup"><span data-stu-id="ae64b-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="ae64b-174">Funktionskomponenten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ae64b-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="ae64b-175">Status und Version</span><span class="sxs-lookup"><span data-stu-id="ae64b-175">Version and status</span></span>

<span data-ttu-id="ae64b-176">Die Version wird zum Verwalten des Lebenszyklus von Globalisierungsfunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae64b-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="ae64b-177">Der Status kann im Feld **Status** auf der Registerkarte **Ausführung** geändert werden. Folgende Status sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ae64b-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="ae64b-178">**Entwurf** – Die Funktion kann nur bearbeitet werden, wenn sie sich in diesem Status befindet.</span><span class="sxs-lookup"><span data-stu-id="ae64b-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="ae64b-179">**Abgeschlossen** – Die Funktion und alle zugehörigen Komponenten wurden finalisiert (abgeschlossen) und können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="ae64b-180">**Veröffentlicht** – Die Funktion und alle zugehörigen Komponenten wurden im globalen Repository veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ae64b-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="ae64b-181">**Geteilt** – Die Funktion und alle zugehörigen Komponenten wurden an externe Organisationen weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="ae64b-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="ae64b-182">**Aktiviert** – Die Funktion und alle zugehörigen Komponenten wurden für die Verwendung in einem Globalisierungsdienst aktiviert, z. B. einem E-Invoicing-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ae64b-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="ae64b-183">Funktionen müssen sich nacheinander durch einige dieser Status bewegen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="ae64b-184">Daher ist möglicherweise nicht jeder Status in jeder Lebenszyklusphase verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae64b-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="ae64b-185">Varianten</span><span class="sxs-lookup"><span data-stu-id="ae64b-185">Configurations</span></span>

<span data-ttu-id="ae64b-186">Die folgenden Aktionen sind für Konfigurationen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ae64b-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="ae64b-187">**Anzeigen** – Zeigen Sie die zugrunde liegenden Funktionskonfigurationen an, für die keine Aktualisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ae64b-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="ae64b-188">**Bearbeiten** – Erstellen Sie eine Entwurfsversion einer ausgewählten Konfiguration, damit Sie das Format oder die Formatzuordnung im Format-Designer bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="ae64b-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="ae64b-189">**Löschen** – Löschen Sie eine ausgewählte Konfiguration aus der Funktion.</span><span class="sxs-lookup"><span data-stu-id="ae64b-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="ae64b-190">**Zurücksetzen** – Funktion zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="ae64b-191">Weitere Informationen finden Sie unter [Zurücksetzen abgeleiteter Glogalisierungsfunktionen](#rebase) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ae64b-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="ae64b-192">Einrichtungen</span><span class="sxs-lookup"><span data-stu-id="ae64b-192">Setups</span></span>

<span data-ttu-id="ae64b-193">Folgende Aktionen sind für die Funktionseinrichtung verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ae64b-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="ae64b-194">**Hinzufügen** – Erstellen Sie eine neue Funktionseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="ae64b-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="ae64b-195">Diese Funktioneinrichtung kann aus einer vorhandenen Funktionseinrichtung abgeleitet oder von Grund auf neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="ae64b-196">**Löschen** – Löschen Sie eine ausgewählte Funktionseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="ae64b-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="ae64b-197">**Anzeigen** – Zeigen Sie eine zugrunde liegende Funktionseinrichtung an, für die keine Änderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ae64b-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="ae64b-198">**Bearbeiten** – Erstellen, Löschen oder Ändern der Attribute der drei Hauptkomponenten einer Funktionseinrichtung:</span><span class="sxs-lookup"><span data-stu-id="ae64b-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="ae64b-199">Aktionen und ihre Parameter</span><span class="sxs-lookup"><span data-stu-id="ae64b-199">Actions and their parameters</span></span>
    - <span data-ttu-id="ae64b-200">Regeln für die Anwendbarkeit</span><span class="sxs-lookup"><span data-stu-id="ae64b-200">Applicability rules</span></span>
    - <span data-ttu-id="ae64b-201">Variable</span><span class="sxs-lookup"><span data-stu-id="ae64b-201">Variables</span></span>

![Funktionsversion-Einrichtungsseite](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="ae64b-203">Umgebungen</span><span class="sxs-lookup"><span data-stu-id="ae64b-203">Environments</span></span>

<span data-ttu-id="ae64b-204">Die folgenden Aktionen sind für Umgebungen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ae64b-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="ae64b-205">**Aktivieren** – Wählen Sie für eine ausgewählte Funktions-Version eine veröffentlichte Umgebung und ein **Gültig ab** Datum aus, an dem sie verfügbar sein sollte.</span><span class="sxs-lookup"><span data-stu-id="ae64b-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="ae64b-206">Weitere Informationen finden Sie unter [Umgebungen für Aktivieren](#configureenvironment) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ae64b-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="ae64b-207">**Stornieren** – Entfernen Sie eine Umgebung für eine Funktionseinrichtung.</span><span class="sxs-lookup"><span data-stu-id="ae64b-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="ae64b-208">Organisation</span><span class="sxs-lookup"><span data-stu-id="ae64b-208">Organizations</span></span>

<span data-ttu-id="ae64b-209">Befolgen Sie diese Schritte, um eine Globalisierungsfunktion für eine externe Organisation freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ae64b-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="ae64b-210">Auf der **Funktionen für die elektronische Rechnungsstellung** wählen Sie auf dieser Seite die Funktion und die Funktionsversion aus, die Sie freigeben möchten.</span><span class="sxs-lookup"><span data-stu-id="ae64b-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="ae64b-211">Auf der **Organisationen** Registerkarte wählen Sie **Teilen mit** und geben Sie dann im Dropdown-Dialogfeld den Domänennamen der Organisation ein.</span><span class="sxs-lookup"><span data-stu-id="ae64b-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="ae64b-212">Wählen Sie **Teilen**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-212">Select **Share**.</span></span>

    ![Teilen Sie eine Funktion mit einer Organisation](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="ae64b-214">Die Funktion wird für die ausgewählte Organisation freigegeben und steht dieser Organisation im globalen Repository zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ae64b-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="ae64b-215">Von dort kann die Funktion in die Instanz der Organisation von RCS oder Dynamics 365 Finance importiert werden, damit sie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae64b-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="ae64b-216">Zurücksetzen abgeleiteter Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae64b-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="ae64b-217">Sie können eine zurückgesetzte Globalisierungsfunktion auf die neue oder aktualisierte Version der Basisfunktion zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="ae64b-218">Auf diese Weise können Änderungen, die in der Basisversion aufgetreten sind, automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae64b-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="ae64b-219">Die aktualisierte Version der Basisfunktion wird vom ursprünglichen Konfigurationsanbieter erstellt und dann veröffentlicht oder freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ae64b-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Aktualisierte Version der Basisfunktion](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="ae64b-221">Wenn Sie beispielsweise die abgeleitete Version einer von Ihnen erstellten Funktion neu erstellen möchten, erhalten Sie zuerst die neueste Version der Funktion, indem Sie sie aus dem globalen Repository importieren.</span><span class="sxs-lookup"><span data-stu-id="ae64b-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="ae64b-222">Auf der **Funktionen für die elektronische Rechnungsstellung** Seite wählen Sie **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="ae64b-223">Wählen Sie **Synchronisieren**, um die neuesten Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae64b-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="ae64b-224">Wählen Sie in der Liste der Funktionen die zu importierenden Funktionen aus und wählen Sie dann **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Importieren der neuesten Version einer Funktion](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="ae64b-226">Wählen Sie in der Liste der Funktionen die Funktion aus, die neu erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae64b-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="ae64b-227">Auf der Registerkarte **Version** wählen Sie **Neu**, um eine Entwurfsversion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Neue Entwurfsversion erstellt](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="ae64b-229">Wählen Sie **Zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="ae64b-230">In dem Dialogfeld **Zurücksetzen** wählen Sie die neueste Version der Funktion aus zum Zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Dialogfeld zurücksetzen](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="ae64b-232">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae64b-232">Select **OK**.</span></span>
9. <span data-ttu-id="ae64b-233">Überprüfen Sie die Funktionskomponenten und nehmen Sie alle notwendigen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="ae64b-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="ae64b-234">Wählen Sie **Status ändern**, um die Funktion zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="ae64b-235">Wenn die Zurücksetzung abgeschlossen ist, können Sie zusätzliche Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="ae64b-236">Sie können die Funktion beispielsweise veröffentlichen und für die Verwendung in Globalisierungsdiensten verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Funktionsstatus auf Abgeschlossen aktualisiert](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="ae64b-238">Konfigurieren Sie Umgebungen für Globalisierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae64b-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="ae64b-239">Benutzer von Globalisierungsdiensten können die Umgebung verwalten, um eine Globalisierungsfunktion einzurichten und anderen Benutzern, die Zugriff darauf haben, die Berechtigung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="ae64b-240">Öffnen Sie die Umgebung **Globalisierungsfunktionen** und dann unter **Eigenschaften** wählen Sie die Kachel **elektronische Rechnungsstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="ae64b-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Arbeitsbereich für globale Funktionen](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="ae64b-242">Wählen **Key Vault-Parameter** und dann **Neu**, um den Azure Key Vault-Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="ae64b-243">Geben Sie einen Namen und eine Beschreibung für das Schlüsseldepot ein und geben dann in das Feld **Key Vault URI** die URL ein, die die Key Vault-Ressource in Azure identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ae64b-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="ae64b-244">Auf dem Inforegister **Zertifikate** wählen Sie **Hinzufügen**, um das Zertifikat hinzuzufügen, geben Sie einen Namen und eine Beschreibung für jedes Zertifikat ein.</span><span class="sxs-lookup"><span data-stu-id="ae64b-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Zertifikat hinzugefügt](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="ae64b-246">Wählen Sie **Neu** aus, um eine neue Umgebung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="ae64b-247">Geben Sie einen Namen, eine Beschreibung und den für das Speichern erforderliche Signatur-Token-Schlüssel für den gemeinsamen Zugriff ein.</span><span class="sxs-lookup"><span data-stu-id="ae64b-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="ae64b-248">Auf dem Inforegister **Benutzer** wählen Sie **Neu**, um einen Benutzer hinzuzufügen, der über die Berechtigung zum Zugriff auf diese Umgebung verfügt.</span><span class="sxs-lookup"><span data-stu-id="ae64b-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="ae64b-249">Geben Sie die Benutzer-ID und die E-Mail-Adresse des Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="ae64b-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="ae64b-250">Wiederholen Sie zum Hinzufügen weiterer Benutzer die Schritte 7 und 8.</span><span class="sxs-lookup"><span data-stu-id="ae64b-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="ae64b-251">Wählen Sie **Veröffentlichen**, um die Umgebung zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ae64b-251">Select **Publish** to publish the environment.</span></span>

    ![Veröffentlichte Umgebung](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]