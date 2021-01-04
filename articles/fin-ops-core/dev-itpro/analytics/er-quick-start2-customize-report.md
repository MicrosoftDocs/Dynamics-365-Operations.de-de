---
title: Anpassen eines EB-Formats, um ein benutzerdefiniertes elektronisches Dokument zu generieren
description: In diesem Thema wird erläutert, wie Sie ein von Microsoft bereitgestelltes EB-Format (Elektronische Berichterstellung) so anpassen, dass ein benutzerdefiniertes elektronisches Dokument generiert wird.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680169"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="ec31e-103">Anpassen eines EB-Formats, um ein benutzerdefiniertes elektronisches Dokument zu generieren</span><span class="sxs-lookup"><span data-stu-id="ec31e-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ec31e-104">Die Prozeduren in diesem Thema erläutern, wie ein Benutzer mit der Rolle des Systemadministrators oder des funktionalen Beraters für die elektronische Berichterstellung die folgenden Aufgaben ausführen kann:</span><span class="sxs-lookup"><span data-stu-id="ec31e-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="ec31e-105">Konfigurieren der Parameter für das [Framework für elektronische Berichterstellung (EB)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="ec31e-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="ec31e-106">Importieren von EB-Konfigurationen, die von Microsoft bereitgestellt und zum Generieren einer Zahlungsdatei verwendet werden, während eine [Kreditorenzahlung](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="ec31e-107">Erstellen einer benutzerdefinierten Version einer standardmäßigen EB-Formatkonfiguration, die von Microsoft bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="ec31e-108">Ändern der benutzerdefinierten EB-Formatkonfiguration, sodass Zahlungsdateien generiert werden, die den Anforderungen einer bestimmten Bank entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="ec31e-109">Übernehmen von Änderungen, die an der standardmäßigen EB-Formatkonfiguration vorgenommen wurden, in die benutzerdefinierte EB-Formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="ec31e-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="ec31e-110">Alle der folgenden Prozeduren können im **GBSI**-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="ec31e-111">Eine Codierung ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec31e-111">No coding is required.</span></span>

- [<span data-ttu-id="ec31e-112">Konfigurieren des EB-Frameworks</span><span class="sxs-lookup"><span data-stu-id="ec31e-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="ec31e-113">Parameter der elektronischen Berichterstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ec31e-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="ec31e-114">Aktivieren eines EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ec31e-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="ec31e-115">Überprüfen der Liste der EB-Konfigurationsanbieter</span><span class="sxs-lookup"><span data-stu-id="ec31e-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="ec31e-116">Hinzufügen eines neuen EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ec31e-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="ec31e-117">Aktivieren eines EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ec31e-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="ec31e-118">Importieren der standardmäßigen EB-Formatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="ec31e-119">Importieren der standardmäßigen EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="ec31e-120">Überprüfen der importierten EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="ec31e-121">Vorbereiten einer Kreditorenzahlung zur Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ec31e-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="ec31e-122">Hinzufügen von Bankdaten für ein Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="ec31e-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="ec31e-123">Eingeben einer Kreditorenzahlung</span><span class="sxs-lookup"><span data-stu-id="ec31e-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="ec31e-124">Verarbeiten einer Kreditorenzahlung durch Verwendung des standardmäpigen EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="ec31e-125">Einrichten der elektronischen Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="ec31e-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="ec31e-126">Verarbeiten einer Kreditorenzahlung</span><span class="sxs-lookup"><span data-stu-id="ec31e-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="ec31e-127">Anpassen des standardmäßigen EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="ec31e-128">Erstellen eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="ec31e-129">Bearbeiten eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="ec31e-130">Markieren eines benutzerdefinierten Formats als ausführbar</span><span class="sxs-lookup"><span data-stu-id="ec31e-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="ec31e-131">Verarbeiten einer Kreditorenzahlung durch Verwendung des benutzerdefinierten EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="ec31e-132">Einrichten der elektronischen Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="ec31e-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="ec31e-133">Verarbeiten einer Kreditorenzahlung</span><span class="sxs-lookup"><span data-stu-id="ec31e-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="ec31e-134">Importieren neuer Versionen der standardmäßigen EB-Formatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="ec31e-135">Importieren neuer Versionen der standardmäßigen EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="ec31e-136">Überprüfen der importierten EB-Formatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="ec31e-137">Übernehmen der Änderungen in der neuen Version eines importierten Formats in ein benutzerdefiniertes Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="ec31e-138">Vervollständigen der aktuellen Entwurfsversion eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="ec31e-139">Zurücksetzen eines benutzerdefinierten Formats auf eine neue Basisversion</span><span class="sxs-lookup"><span data-stu-id="ec31e-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="ec31e-140">Verarbeiten einer Kreditorenzahlung durch Verwendung eines zurückgesetzten EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="ec31e-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ec31e-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="ec31e-142">Konfigurieren des EB-Frameworks</span><span class="sxs-lookup"><span data-stu-id="ec31e-142">Configure the ER framework</span></span>

<span data-ttu-id="ec31e-143">Als Benutzer mit der Rolle des funktionalen Beraters für die elektronische Berichterstellung müssen Sie den minimalen Satz von EB-Parametern konfigurieren, bevor Sie das EB-Framework zum Entwerfen einer benutzerdefinierten Version eines standardmäßigen EB-Formats verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ec31e-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="ec31e-144">Parameter der elektronischen Berichterstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ec31e-144">Configure ER parameters</span></span>

1. <span data-ttu-id="ec31e-145">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-146">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Parameter für elektronische Berichterstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="ec31e-147">Auf der Seite **Parameter für elektronische Berichterstellung** legen Sie auf der Registerkarte **Allgemein** die Option **Entwurfsmodus aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="ec31e-148">Legen Sie auf der Registerkarte **Anhänge** die folgenden Parameter fest:</span><span class="sxs-lookup"><span data-stu-id="ec31e-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="ec31e-149">Wählen Sie im Feld **Konfigurationen** den **Dateityp** für das **USMF**-Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="ec31e-150">Wählen Sie in den Feldern **Einzelvorgangsarchiv**, **Temporär**, **Grundlage** und **Andere** den **Dateityp** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="ec31e-151">Weitere Informationen zu EB-Parametern finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ec31e-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="ec31e-152">Aktivieren eines EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ec31e-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="ec31e-153">Jede hinzugefügte EB-Konfiguration wird als Eigentum eines EB-Konfigurationsanbieters markiert.</span><span class="sxs-lookup"><span data-stu-id="ec31e-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="ec31e-154">Der EB-Konfigurationsanbieter, der im Arbeitsbereich **Elektronische Berichterstellung** aktiviert ist, wird zu diesem Zweck verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec31e-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="ec31e-155">Daher müssen Sie im Arbeitsbereich **Elektronische Berichterstellung** einen EB-Konfigurationsanbieter aktivieren, bevor Sie mit dem Hinzufügen oder Bearbeiten von EB-Konfigurationen beginnen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="ec31e-156">Nur der Besitzer einer EB-Konfiguration kann diese bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ec31e-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="ec31e-157">Daher muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden, bevor eine EB-Konfigurationen bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec31e-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="ec31e-158">Überprüfen der Liste der EB-Konfigurationsanbieter</span><span class="sxs-lookup"><span data-stu-id="ec31e-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="ec31e-159">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-160">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="ec31e-161">Auf der Seite **Konfigurationsanbietertabelle** hat jeder Anbieterdatensatz einen eindeutigen Namen und eine eindeutige URL.</span><span class="sxs-lookup"><span data-stu-id="ec31e-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="ec31e-162">Überprüfen Sie den Inhalt dieser Seite.</span><span class="sxs-lookup"><span data-stu-id="ec31e-162">Review the contents of this page.</span></span> <span data-ttu-id="ec31e-163">Wenn bereits ein Datensatz für **Litware, Inc.** (`https://www.litware.com`) vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="ec31e-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="ec31e-164">Hinzufügen eines neuen EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ec31e-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="ec31e-165">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-166">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="ec31e-167">Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="ec31e-168">Geben Sie im Feld **Name** **Litware, Inc.** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="ec31e-169">Geben Sie im Feld **Internetadresse** `https://www.litware.com` ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="ec31e-170">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="ec31e-171">Aktivieren eines EB-Konfigurationsanbieters</span><span class="sxs-lookup"><span data-stu-id="ec31e-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="ec31e-172">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-173">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus. Wählen Sie dann **Als aktiv festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="ec31e-174">Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ec31e-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="ec31e-175">Importieren der standardmäßigen EB-Formatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="ec31e-176">Importieren der standardmäßigen EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-176">Import the standard ER configurations</span></span>

<span data-ttu-id="ec31e-177">Um Ihrer aktuellen Instanz von Microsoft Dynamics 365 Finance die standardmäßigen EB-Konfigurationen hinzuzufügen, müssen Sie sie aus dem EB-[Repository](general-electronic-reporting.md#Repository) importieren, das für diese Instanz konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ec31e-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="ec31e-178">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-179">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den Microsoft-Anbieter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="ec31e-180">Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="ec31e-181">Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum Regulatory Configuration Service zu autorisieren, folgen Sie den Autorisierungsanweisungen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="ec31e-182">Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **BACS (UK)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="ec31e-183">Wählen Sie auf dem Inforegister **Versionen** die Version **1.1** der ausgewählten EB-Formatkonfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="ec31e-184">Wählen Sie **Importieren** aus, um die ausgewählte Version aus dem globalen Repository auf die aktuelle Finance-Instanz herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigurationsrepository-Seite](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="ec31e-186">Wenn Sie Probleme beim Zugriff auf das [globale Repository](er-download-configurations-global-repo.md) haben, können Sie für das [Herunterladen von Konfigurationen](download-electronic-reporting-configuration-lcs.md) stattdessen Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="ec31e-187">Überprüfen der importierten EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="ec31e-188">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-189">Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="ec31e-190">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="ec31e-191">Beachten Sie, dass zusätzlich zum ausgewählten EB-Format **BACS (UK)** weitere erforderliche EB-Konfigurationen importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="ec31e-192">Stellen Sie sicher, dass die folgenden EB-Konfigurationen in der Konfigurationsstruktur verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="ec31e-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="ec31e-193">**Zahlungsmodell**: Diese Konfiguration enthält die EB-Komponente [Datenmodell](general-electronic-reporting.md#data-model-and-model-mapping-components), die die Datenstruktur der Zahlungsgeschäftsdomäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec31e-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="ec31e-194">**Zahlungsmodellzuordnung 1611**: Diese Konfiguration enthält die EB-Komponente [Modellzuordnung](general-electronic-reporting.md#data-model-and-model-mapping-components), die beschreibt, wie das Datenmodell zur Laufzeit mit Anwendungsdaten gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="ec31e-195">**BACS (UK)**: Diese Konfiguration enthält die EB-Komponenten [Format](general-electronic-reporting.md#FormatComponentOutbound) und Formatzuordnung.</span><span class="sxs-lookup"><span data-stu-id="ec31e-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="ec31e-196">Die Formatkomponente legt das Berichtslayout fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-196">The format component specifies the report layout.</span></span> <span data-ttu-id="ec31e-197">Die Formatzuordnungskomponente enthält die Modelldatenquelle und legt fest, wie das Berichtslayout mithilfe dieser Datenquelle zur Laufzeit ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Konfigurationsseite](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="ec31e-199">Vorbereiten einer Kreditorenzahlung zur Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ec31e-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="ec31e-200">Hinzufügen von Bankdaten für ein Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="ec31e-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="ec31e-201">Sie müssen Bankdaten für ein Kreditorenkonto hinzufügen, auf die später in einer registrierten Zahlung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="ec31e-202">Wechseln Sie zu **Kreditorenkonten** \> **Kreditoren** \> **Alle Kreditoren**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="ec31e-203">Wählen Sie auf der Seite **Alle Kreditoren** das Kreditorenkonto **GB_SI_000001** aus. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Kreditor** in der Gruppe **Einrichtung** die Option **Bankkonten** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="ec31e-204">Wählen Sie auf der Seite **Kreditoren-Bankkonten** die Option **Neu** aus und geben Sie dann die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="ec31e-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="ec31e-205">In das Feld **Bankkonto** geben Sie **GBP OPER** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="ec31e-206">Wählen Sie im Feld **Bankgruppen** die Option **BankGBP** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="ec31e-207">Im Feld **Bankkontonummer** geben Sie **202015** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="ec31e-208">Im Feld **SWIFT-Code** geben Sie <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="ec31e-209">Im Feld **IBAN** geben Sie **GB33BUKB20201555555555** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="ec31e-210">Im Feld **Bankleitzahl** können Sie den Standardwert <a id="DefineRoutingNumber"></a>**123456** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ec31e-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Seite „Kreditoren-Bankkonten“](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="ec31e-212">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-212">Select **Save**.</span></span>
5. <span data-ttu-id="ec31e-213">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ec31e-213">Close the page.</span></span>
6. <span data-ttu-id="ec31e-214">Öffnen Sie auf der Seite **Alle Kreditoren** das Kreditorenkonto **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="ec31e-215">Wählen Sie auf der Seite mit den Kreditorendetails **Bearbeiten** aus, um die Seite bei Bedarf bearbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="ec31e-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="ec31e-216">Wählen Sie auf dem Inforegister **Zahlung** im Feld **Bankkonto** die Option **GBP OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Seite „Kreditorendetails“](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="ec31e-218">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-218">Select **Save**.</span></span>
10. <span data-ttu-id="ec31e-219">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ec31e-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="ec31e-220">Eingeben einer Kreditorenzahlung</span><span class="sxs-lookup"><span data-stu-id="ec31e-220">Enter a vendor payment</span></span>

<span data-ttu-id="ec31e-221">Sie müssen eine neue Kreditorenzahlung eingeben, indem Sie einen [Zahlungsvorschlag](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="ec31e-222">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ec31e-223">Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="ec31e-224">Wählen Sie im Feld **Name** die Option **VendPay** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="ec31e-225">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-225">Select **Lines**.</span></span>
5. <span data-ttu-id="ec31e-226">Wählen Sie **Zahlungsvorschlag** \> **Zahlungsvorschlag erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="ec31e-227">Konfigurieren Sie im Dialogfeld **Kreditorenzahlungsvorschlag** Bedingungen, um ausschließlich nach Datensätzen für das Kreditorenkonto **GB_SI_000001** zu filtern, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="ec31e-228">Wählen Sie die Zeile für die Rechnung **00000007_Inv** aus und wählen Sie dann **Zahlung erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Dialogfeld „Kreditorenzahlungsvorschlag“](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="ec31e-230">Überprüfen Sie, ob die eingegebene Zahlung für die Verwendung der Zahlungsmethode **Elektronisch** konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ec31e-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Seite für Kreditorenzahlungen](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="ec31e-232">Verarbeiten einer Kreditorenzahlung durch Verwendung des standardmäpigen EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="ec31e-233">Einrichten der elektronischen Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="ec31e-233">Set up the electronic payment method</span></span>

<span data-ttu-id="ec31e-234">Sie müssen die elektronische Zahlungsmethode so konfigurieren, dass sie die importierte EB-Formatkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec31e-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="ec31e-235">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungseinstellungen** \> **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="ec31e-236">Wählen Sie auf der Seite **Zahlungsmethoden – Kreditoren** im linken Bereich die Zahlungsmethode **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="ec31e-237">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-237">Select **Edit**.</span></span>
4. <span data-ttu-id="ec31e-238">Legen Sie auf dem Inforegister **Dateiformate** die Option **Allgemeines elektronisches Exportformat** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="ec31e-239">Wählen Sie im Feld **Formatkonfiguration exportieren** die Formatkonfiguration **BACS (UK)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Seite „Zahlungsmethoden – Kreditoren“](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="ec31e-241">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="ec31e-242">Verarbeiten einer Kreditorenzahlung</span><span class="sxs-lookup"><span data-stu-id="ec31e-242">Process a vendor payment</span></span>

1. <span data-ttu-id="ec31e-243">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ec31e-244">Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Zahlungserfassung aus, die Sie zuvor hinzugefügt haben, und wählen Sie dann **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="ec31e-245">Wählen Sie auf der Seiite **Kreditorenzahlungen** die Option **Zahlungen generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="ec31e-246">Geben Sie im Dialogfeld **Zahlungen generieren** die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="ec31e-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ec31e-247">Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="ec31e-248">Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="ec31e-249">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-249">Select **OK**.</span></span>
6. <span data-ttu-id="ec31e-250">Legen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **Kontrollbericht drucken** auf **Ja** fest und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Dialogfeld „Elektronische Berichtsparameter“](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="ec31e-252">Zusätzlich zur Zahlungsdatei können Sie jetzt den Kontrollbericht generieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="ec31e-253">Laden Sie die ZIP-Datei herunter und entpacken Sie daraus die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="ec31e-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="ec31e-254">Den Kontrollbericht im Excel-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-254">The control report in Excel format</span></span>
    - <span data-ttu-id="ec31e-255">Die Zahlungsdatei im TXT-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-255">The payment file in TXT format</span></span>

        <span data-ttu-id="ec31e-256">Beachten Sie, dass in Übereinstimmung mit der [Struktur](#PositionRoutingNumber) des angegebenen EB-Formats die Zahlungsposition in der generierten Datei mit der Bankleitzahl beginnt, die für das konfigurierte Bankkonto [definiert](#DefineRoutingNumber) wurde.</span><span class="sxs-lookup"><span data-stu-id="ec31e-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Zahlungsdatei im TXT-Format](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="ec31e-258">Anpassen des standardmäßigen EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-258">Customize the standard ER format</span></span>

<span data-ttu-id="ec31e-259">Für das Beispiel in diesem Abschnitt verwenden Sie die von Microsoft bereitgestellten EB-Konfigurationen, um Kreditorenzahlungsdateien im BACS-Format zu generieren. Sie müssen jedoch eine Anpassung vornehmen, um die Anforderungen einer bestimmten Bank zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="ec31e-260">Sie möchten außerdem Ihr benutzerdefiniertes Format aktualisieren können, wenn neue Versionen von EB-Konfigurationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ec31e-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="ec31e-261">Dieses Upgrade sollte jedoch möglichst wenig kosten.</span><span class="sxs-lookup"><span data-stu-id="ec31e-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="ec31e-262">In diesem Fall müssen Sie als Vertreter von Litware, Inc. eine neue EB-Formatkonfiguration erstellen (ableiten), indem Sie die von Microsoft bereitgestellte Konfiguration **BACS (UK)** als Basis verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="ec31e-263">Erstellen eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-263">Create a custom format</span></span>

1. <span data-ttu-id="ec31e-264">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec31e-265">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="ec31e-266">Litware, Inc. verwendet Version 1.1 dieser EB-Formatkonfiguration als Basis für die benutzerdefinierte Version.</span><span class="sxs-lookup"><span data-stu-id="ec31e-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="ec31e-267">Wählen Sie **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="ec31e-268">Sie können dieses Dialogfeld verwenden, um eine neue Konfiguration für ein benutzerdefiniertes Zahlungsformat zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="ec31e-269">Wählen Sie in der Feldgruppe **Neu** die Option **Von Name ableiten: BACS (UK), Microsoft** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="ec31e-270">In das Feld **Name** geben Sie **BACS (UK, benutzerdefiniert)** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Konfigurations-Dropdown-Dialogfeld erstellen](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="ec31e-272">Wählen Sie **Konfiguration erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-272">Select **Create configuration**.</span></span>

<span data-ttu-id="ec31e-273">Version 1.1.1 der EB-Formatkonfiguration **BACS (UK, benutzerdefiniert)** wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec31e-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="ec31e-274">Diese Version hat den [Status](general-electronic-reporting.md#component-versioning) **Entwurf** und kann bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="ec31e-275">Der aktuelle Inhalt Ihres benutzerdefinierten EB-Formats entspricht dem Inhalt des von Microsoft bereitgestellten Formats.</span><span class="sxs-lookup"><span data-stu-id="ec31e-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Konfigurationsseite](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="ec31e-277">Bearbeiten eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-277">Edit a custom format</span></span>

<span data-ttu-id="ec31e-278">Sie müssen Ihr benutzerdefiniertes Format so konfigurieren, dass es den bankspezifischen Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="ec31e-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="ec31e-279">Beispielsweise kann eine Bank verlangen, dass generierte Zahlungsdateien den SWIFT-Code (Society for Worldwide Interbank Financial Telecommunication) einer Bank enthalten, der in der verarbeiteten Kreditorenzahlung die Agentenrolle zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ec31e-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="ec31e-280">SWIFT-Codes sind internationale Bankleitzahlen, die bestimmte Banken weltweit identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="ec31e-281">Sie werden auch als Bank Identifier Codes (BICs) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ec31e-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="ec31e-282">Der SWIFT-Code muss 11 Zeichen lang sein und am Anfang jeder Zahlungsposition in eine generierte Zahlungsdatei eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="ec31e-283">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec31e-284">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK, benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="ec31e-285">Wählen Sie auf dem Inforegister **Versionen** die Version **1.1.1** der ausgewählten Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="ec31e-286">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-286">Select **Designer**.</span></span>
5. <span data-ttu-id="ec31e-287">Wählen Sie auf der Seite **Formatdesigner** die Option **Details anzeigen** aus, um weitere Informationen zu den Formatelementen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="ec31e-288">Erweitern und überprüfen Sie die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="ec31e-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="ec31e-289">Das Element **BACSReportsFolder** vom Typ **Ordner**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="ec31e-290">Dieses Element wird verwendet, um eine Ausgabe im ZIP-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="ec31e-291">Das Element **file** vom Typ **Datei**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="ec31e-292">Dieses Element wird verwendet, um eine Zahlungsdatei im TXT-Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="ec31e-293">Das Element **transactions** vom Typ **Sequenz**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="ec31e-294">Dieses Element wird verwendet, um eine einzelne Zahlungsposition in einer Zahlungsdatei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="ec31e-295">Das Element **transaction** vom Typ **Sequenz**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="ec31e-296">Dieses Element wird verwendet, um die einzelnen Felder einer Zahlungsposition zu generieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="ec31e-297">Wählen Sie das Element **transaction** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-297">Select the **transaction** element.</span></span>

    ![Transaktionselement im EB-Vorgangsdesigner](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="ec31e-299">Der bereitgestellte Bericht ist so konfiguriert, dass <a id="PositionRoutingNumber"></a>jede Zahlungsposition mit der Bankleitzahl beginnt.</span><span class="sxs-lookup"><span data-stu-id="ec31e-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="ec31e-300">Das Formatelement **vendBankRouteNum** wird zu diesem Zweck verwendet.</span><span class="sxs-lookup"><span data-stu-id="ec31e-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="ec31e-301">Wählen Sie **Hinzufügen** und dann den Typ **Text\\Zeichenfolge** des Formatelements aus, das Sie hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ec31e-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="ec31e-302">In das Feld **Name** geben Sie **vendBankSWIFT** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="ec31e-303">In das Feld **Mindestlänge** geben Sie **11** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="ec31e-304">In das Feld **Höchstlänge** geben Sie **11** ein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="ec31e-305">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec31e-306">Das Element **vendBankSWIFT** wird verwendet, um den SWIFT-Code einer Kreditorenbank in generierte Dateien einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ec31e-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="ec31e-307">Wählen Sie in der Formatstruktur den Punkt **vendBankSWIFT** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="ec31e-308">Wählen Sie **Nach oben verschieben** aus, um das ausgewählte Formatelement um eine Ebene nach oben zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ec31e-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="ec31e-309">Wiederholen Sie diesen Schritt, bis das Element **vendBankSWIFT** das <a id="PositionSWIFTCode"></a>erste Element unter dem übergeordneten Element **transaction** ist.</span><span class="sxs-lookup"><span data-stu-id="ec31e-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![„vendBankSWIFT“ als erstes Element unter „transaction“ im EB-Vorgangsdesigner](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="ec31e-311">Während **vendBankSWIFT** in der Formatstruktur ausgewählt ist, wählen Sie die Registerkarte **Zuordnung** aus und erweitern Sie dann die **Modelldatenquelle**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="ec31e-312">Erweitern Sie **model.Payment** \> **model.Payment.CreditorAgent** und wählen Sie das Datenquellenfeld **model.Payment.CreditorAgent.BICFI** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="ec31e-313">Dieses Datenquellenfeld stellt den SWIFT-Code einer Kreditorenbank bereit, der die Agentenrolle in der verarbeiteten Kreditorenzahlung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ec31e-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="ec31e-314">Wählen Sie **Bindung** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-314">Select **Bind**.</span></span> <span data-ttu-id="ec31e-315">Das Formatelement **vendBankSWIFT** ist jetzt an das Datenquellenfeld **model.Payment.CreditorAgent.BICFI** gebunden, sodass SWIFT-Codes in generierte Zahlungsdateien eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![Formatelement „vendBankSWIFT“ gebunden an das Datenquellenfeld „model.Payment.CreditorAgent.BICFI“ im EB-Vorgangsdesigner](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="ec31e-317">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-317">Select **Save**.</span></span>
15. <span data-ttu-id="ec31e-318">Schließen Sie die Designerseite.</span><span class="sxs-lookup"><span data-stu-id="ec31e-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="ec31e-319">Markieren eines benutzerdefinierten Formats als ausführbar</span><span class="sxs-lookup"><span data-stu-id="ec31e-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="ec31e-320">Nachdem die erste Version Ihres benutzerdefinierten Formats mit dem Status **Entwurf** erstellt wurde, können Sie es zu Testzwecken ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="ec31e-321">Um den Bericht auszuführen, müssen Sie eine Kreditorenzahlung mithilfe der Zahlungsmethode verarbeiten, die sich auf Ihr benutzerdefiniertes EB-Format bezieht.</span><span class="sxs-lookup"><span data-stu-id="ec31e-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="ec31e-322">Beim Aufrufen eines EB-Formats aus der Anwendung werden standardmäßig nur Versionen mit dem Status **Abgeschlossen** oder **Freigegeben** [berücksichtigt](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="ec31e-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="ec31e-323">Dieses Verhalten verhindert, dass EB-Formate mit unfertigen Designs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="ec31e-324">Für Ihre Testläufe können Sie die Anwendung jedoch zwingen, die Version Ihres EB-Formats mit dem Status **Entwurf** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="ec31e-325">Auf diese Weise können Sie die aktuelle Formatversion anpassen, falls Änderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ec31e-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="ec31e-326">Weitere Informationen finden Sie unter [Anwendbarkeit](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="ec31e-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="ec31e-327">Um die Entwurfsversion eines EB-Formats zu verwenden, müssen Sie das EB-Format explizit markieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="ec31e-328">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec31e-329">Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="ec31e-330">Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="ec31e-331">Wählen Sie **Bearbeiten** aus, um die aktuelle Seite bei Bedarf bearbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="ec31e-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="ec31e-332">Wählen Sie in der Konfigurationsstruktur im linken Bereich den Punkt **BACS (UK, benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="ec31e-333">Legen Sie die Option **Entwurf ausführen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Option „Entwurf ausführen“ auf der Konfigurationsseite](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="ec31e-335">Verarbeiten einer Kreditorenzahlung durch Verwendung des benutzerdefinierten EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="ec31e-336">Einrichten der elektronischen Zahlungsmethode</span><span class="sxs-lookup"><span data-stu-id="ec31e-336">Set up the electronic payment method</span></span>

<span data-ttu-id="ec31e-337">Sie müssen die elektronische Zahlungsmethode so konfigurieren, dass Ihr benutzerdefiniertes EB-Format zur Verarbeitung von Kreditorenzahlungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="ec31e-338">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungseinstellungen** \> **Zahlungsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="ec31e-339">Wählen Sie auf der Seite **Zahlungsmethoden – Kreditoren** im linken Bereich die Zahlungsmethode **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="ec31e-340">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-340">Select **Edit**.</span></span>
4. <span data-ttu-id="ec31e-341">Legen Sie auf dem Inforegister **Dateiformate** die Option **Allgemeines elektronisches Exportformat** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="ec31e-342">Wählen Sie im Feld **Formatkonfiguration exportieren** die Formatkonfiguration **BACS (UK, benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Seite „Zahlungsmethoden – Kreditoren“](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="ec31e-344">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="ec31e-345">Verarbeiten einer Kreditorenzahlung</span><span class="sxs-lookup"><span data-stu-id="ec31e-345">Process a vendor payment</span></span>

1. <span data-ttu-id="ec31e-346">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ec31e-347">Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Zahlungserfassung aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ec31e-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="ec31e-348">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-348">Select **Lines**.</span></span>
4. <span data-ttu-id="ec31e-349">Wählen Sie auf der Seite **Kreditorenzahlungen** über dem Raster **Zahlungsstatus** \> **Kein** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="ec31e-350">Wählen Sie **Zahlung generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="ec31e-351">Geben Sie im Dialogfeld **Zahlungen generieren** die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="ec31e-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ec31e-352">Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="ec31e-353">Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="ec31e-354">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-354">Select **OK**.</span></span>
8. <span data-ttu-id="ec31e-355">Legen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **Kontrollbericht drucken** auf **Ja** fest und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec31e-356">Zusätzlich zur Zahlungsdatei können Sie nur den Kontrollbericht generieren.</span><span class="sxs-lookup"><span data-stu-id="ec31e-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="ec31e-357">Laden Sie die ZIP-Datei herunter und entpacken Sie daraus die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="ec31e-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="ec31e-358">Den Kontrollbericht im Excel-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-358">The control report in Excel format</span></span>
    - <span data-ttu-id="ec31e-359">Die Zahlungsdatei im TXT-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-359">The payment file in TXT format</span></span>

        <span data-ttu-id="ec31e-360">Beachten Sie, dass gemäß der Struktur Ihres benutzerdefinierten EB-Formats die Zahlungsposition in der generierten Datei jetzt mit dem SWIFT-Code [beginnt](#PositionSWIFTCode), der für das Bankkonto des Kreditors [eingegeben](#DefineSWIFTCode) wurde, dessen Zahlung verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec31e-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Zahlungsdatei im TXT-Format](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="ec31e-362">Importieren neuer Versionen der standardmäßigen EB-Formatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="ec31e-363">Für das Beispiel in diesem Abschnitt erhalten Sie eine Benachrichtigung über den Knowledge Base-Artikel [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span><span class="sxs-lookup"><span data-stu-id="ec31e-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="ec31e-364">Diese Benachrichtigung informiert Sie über die neue Version des EB-Formats **BACS (UK)**, das von Microsoft veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="ec31e-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="ec31e-365">Zusätzlich zum Kontrollbericht können Benutzer mit dieser neuen Version noch den Zahlungsavisbericht und den Begleitzettel-Bericht erstellen, während eine Kreditorenzahlung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="ec31e-366">Sie möchten diese Funktion jetzt nutzen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="ec31e-367">Importieren neuer Versionen der standardmäßigen EB-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="ec31e-368">Um neue Versionen der EB-Konfigurationen zur aktuellen Finance-Instanz hinzuzufügen, müssen Sie sie aus dem EB-[Repository](general-electronic-reporting.md#Repository) importieren, das Sie konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="ec31e-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="ec31e-369">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-370">Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Microsoft** aus. Wählen Sie dann **Repositorys** aus, um die Liste der Repositorys für den Microsoft-Anbieter anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="ec31e-371">Wählen Sie auf der Seite **Konfigurationsrepositorys** das Repository des Typs **Global** aus. Wählen Sie dann **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="ec31e-372">Wenn Sie aufgefordert werden, das Herstellen einer Verbindung zum Regulatory Configuration Service zu autorisieren, folgen Sie den Autorisierungsanweisungen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="ec31e-373">Wählen Sie auf der Seite **Konfigurationsrepositorys** in der Konfigurationsstruktur im linken Bereich die Formatkonfiguration **BACS (UK)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="ec31e-374">Wählen Sie auf dem Inforegister **Versionen** die Version **3.3** der ausgewählten EB-Formatkonfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="ec31e-375">Wählen Sie **Importieren** aus, um die ausgewählte Version aus dem globalen Repository auf die aktuelle Finance-Instanz herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfigurationsrepository-Seite](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="ec31e-377">Wenn Sie Probleme beim Zugriff auf das [globale Repository](er-download-configurations-global-repo.md) haben, können Sie für das [Herunterladen von Konfigurationen](download-electronic-reporting-configuration-lcs.md) stattdessen LCS verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="ec31e-378">Überprüfen der importierten EB-Formatkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="ec31e-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="ec31e-379">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-380">Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="ec31e-381">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="ec31e-382">Wählen Sie im Inforegister **Versionen** die Version **3.3** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="ec31e-383">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-383">Select **Designer**.</span></span>
6. <span data-ttu-id="ec31e-384">Erweitern Sie auf der Seite **Formatdesigner** das Formatelement **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="ec31e-385">Beachten Sie, dass Version 3.3 das Formatelement **PaymentAdviceReport** enthält, das zum Generieren eines Zahlungsavisberichts verwendet wird, wenn eine Kreditorenzahlung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ec31e-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![Formatelement „PaymentAdviceReport“ im EB-Vorgangsdesigner](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="ec31e-387">Schließen Sie die Designerseite.</span><span class="sxs-lookup"><span data-stu-id="ec31e-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="ec31e-388">Übernehmen der Änderungen in der neuen Version eines importierten Formats in ein benutzerdefiniertes Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="ec31e-389">Vervollständigen der aktuellen Entwurfsversion eines benutzerdefinierten Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="ec31e-390">Wenn Sie den aktuellen Status Ihres benutzerdefinierten Formats beibehalten möchten, vervollständigen Sie den Entwurf von Version 1.1.1, indem Sie ihren Status von **Entwurf** zu **Abgeschlossen** ändern.</span><span class="sxs-lookup"><span data-stu-id="ec31e-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="ec31e-391">Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="ec31e-392">Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="ec31e-393">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich zunächst den Punkt **Zahlungsmodell** und dann den Punkt **BACS (UK, benutzerdefiniert)**. Wählen Sie dann **BACS (UK, benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="ec31e-394">Wechseln Sie auf dem Inforegister **Versionen** zu **Status ändern** \> **Abgeschlossen** und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="ec31e-395">Der Status von Version 1.1.1 wird von **Entwurf** zu **Abgeschlossen** geändert und die Version ist jetzt schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ec31e-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="ec31e-396">Eine neue bearbeitbare Version 1.1.2 mit dem Status **Entwurf** wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ec31e-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="ec31e-397">Mit dieser Version können Sie weitere Änderungen an Ihrem benutzerdefinierten EB-Format vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="ec31e-398">Zurücksetzen eines benutzerdefinierten Formats auf eine neue Basisversion</span><span class="sxs-lookup"><span data-stu-id="ec31e-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="ec31e-399">Um die neuen Funktionen von Version 3.3 des Formats **BACS (UK)** in Ihrer Anpassung nutzen zu können, müssen Sie die Basiskonfigurationsversion für die benutzerdefinierte Konfiguration ändern, **BACS (UK, benutzerdefiniert)**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="ec31e-400">Dieser Prozess wird als [Rebasierung](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ec31e-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="ec31e-401">Verwenden Sie anstelle von Version 1.1 von **BACS (UK)** Version 3.3.</span><span class="sxs-lookup"><span data-stu-id="ec31e-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="ec31e-402">Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="ec31e-403">Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Zahlungsmodell** und wählen Sie dann **BACS (UK, benutzerdefiniert)** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="ec31e-404">Wählen Sie auf dem Inforegister **Versionen** Version **1.1.2** und dann **Zurücksetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="ec31e-405">Wählen Sie im Dialogfeld **Zurücksetzen** im Feld **Zielversion** Version **3.3** der Basiskonfiguration aus, um sie als neue Basis anzuwenden und zum Aktualisieren der Konfiguration zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Dialogfeld zurücksetzen](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="ec31e-407">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-407">Select **OK**.</span></span>
6. <span data-ttu-id="ec31e-408">Beachten Sie, dass die Nummer der Entwurfsversion von **1.1.2** zu **3.3.2** geändert wurde, um die Änderung in der Basisversion widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="ec31e-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="ec31e-409">Wenn die benutzerdefinierte Version und eine neue Basisversion zusammengeführt werden, können aufgrund von Formatänderungen, die nicht automatisch zusammengeführt werden können, einige Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="ec31e-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Zurückgesetzte Konfiguration mit Konflikten auf der Konfigurationsseite](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="ec31e-411">Wenn Konflikte auftreten, müssen sie im Formatdesigner manuell gelöst werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="ec31e-412">Wählen Sie im Inforegister **Versionen** die Version **3.3.2** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="ec31e-413">Wählen Sie **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-413">Select **Designer**.</span></span>
9. <span data-ttu-id="ec31e-414">Wählen Sie auf der Seite **Formatdesigner** auf dem Inforegister **Details** einen durch das Zurücksetzen verursachten Konfliktdatensatz aus und wählen Sie dann **Basiswert anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Durch Zurücksetzen verursachter Konfliktdatensatz im EB-Vorgangdesigner](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="ec31e-416">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-416">Select **Save**.</span></span>

    <span data-ttu-id="ec31e-417">Der durch das Zurücksetzen verursachte Konfliktdatensatz sollte auf dem Inforegister **Details** nicht mehr angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konflikt gelöst im EB-Vorgangdesigner](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="ec31e-419">Sie haben den Konflikt gelöst, indem Sie bestätigt haben, dass in diesem EB-Format Version 3 des Basismodells verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ec31e-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="ec31e-420">Erweitern Sie **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="ec31e-421">Beachten Sie auf der Registerkarte **Zuordnung**, dass Version 3.3.2 Ihres benutzerdefinierten EB-Formats sowohl Ihre Anpassung (das Formatelement **vendBankSWIFT** und seine Bindung) als auch die neuen Funktionen von Version 3.3 des von Microsoft bereitgestellten Basis-EB-Formats (das Formatelement **PaymentAdviceReport** zusammen mit seinen verschachtelten Elementen und konfigurierten Bindungen) enthält.</span><span class="sxs-lookup"><span data-stu-id="ec31e-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="ec31e-422">Mit nur wenigen Mausklicks haben Sie die Änderungen einer neuen Basisversion übernommen, indem Sie sie mit Ihrer Anpassung zusammengeführt haben.</span><span class="sxs-lookup"><span data-stu-id="ec31e-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Zusammengeführtes Format im EB-Vorgangdesigner](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="ec31e-424">Schließen Sie die Designerseite.</span><span class="sxs-lookup"><span data-stu-id="ec31e-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="ec31e-425">Das Zurücksetzen kann nicht rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="ec31e-425">The rebase action is reversible.</span></span> <span data-ttu-id="ec31e-426">Um das Zurücksetzen abzubrechen, wählen Sie Version **1.1.1** des Formats **BACS (UK, benutzerdefiniert)** auf dem Inforegister **Versionen** aus und wählen Sie dann **Diese Version abrufen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="ec31e-427">Version 3.3.2 wird dann in 1.1.2 umnummeriert und der Inhalt der Entwurfsversion 1.1.2 stimmt mit dem Inhalt von Version 1.1.1 überein.</span><span class="sxs-lookup"><span data-stu-id="ec31e-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="ec31e-428">Verarbeiten einer Kreditorenzahlung durch Verwendung eines zurückgesetzten EB-Formats</span><span class="sxs-lookup"><span data-stu-id="ec31e-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="ec31e-429">Wechseln Sie zu **Kreditorenkonten** \> **Zahlungen** \> **Kreditorenzahlungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="ec31e-430">Wählen Sie auf der Seite **Kreditorenzahlungserfassung** die Zahlungserfassung aus, die Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ec31e-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="ec31e-431">Wählen Sie **Positionen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-431">Select **Lines**.</span></span>
4. <span data-ttu-id="ec31e-432">Wählen Sie auf der Seite **Kreditorenzahlungen** über dem Raster **Zahlungsstatus** \> **Kein** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="ec31e-433">Wählen Sie **Zahlung generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="ec31e-434">Geben Sie im Dialogfeld **Zahlungen generieren** die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="ec31e-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ec31e-435">Wählen Sie im Feld **Zahlungsmethode** die Option **Elektronisch** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="ec31e-436">Wählen Sie im Feld **Bankkonto** die Option **GBSI OPER** aus.</span><span class="sxs-lookup"><span data-stu-id="ec31e-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="ec31e-437">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-437">Select **OK**.</span></span>
8. <span data-ttu-id="ec31e-438">Geben Sie im Dialogfeld **Elektronische Berichtsparameter** die folgenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="ec31e-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="ec31e-439">legen Sie die **Kontrollbereicht drucken** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="ec31e-440">Legen Sie die Option **Zahlungsavis drucken** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="ec31e-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Dialogfeld für elektronische Berichtsparameter](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="ec31e-442">Zusätzlich zur Zahlungsdatei können Sie jetzt sowohl den Kontrollbericht als auch den Zahlungsavisbericht erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec31e-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="ec31e-443">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec31e-443">Select **OK**.</span></span>
10. <span data-ttu-id="ec31e-444">Laden Sie die ZIP-Datei herunter und entpacken Sie daraus die folgenden Dateien:</span><span class="sxs-lookup"><span data-stu-id="ec31e-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="ec31e-445">Den Kontrollbericht im Excel-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-445">The control report in Excel format</span></span>
    - <span data-ttu-id="ec31e-446">Den Zahlungsavisbericht im Excel-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-446">The payment advice report in Excel format</span></span>

        ![Zahlungsavisbericht im Excel-Format](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="ec31e-448">Die Zahlungsdatei im TXT-Format</span><span class="sxs-lookup"><span data-stu-id="ec31e-448">The payment file in TXT format</span></span>

        <span data-ttu-id="ec31e-449">Beachten Sie, dass die Zahlungsposition in der generierten Datei mit dem SWIFT-Code beginnt, der für das Bankkonto eines Kreditors eingegeben wurde, dessen Zahlung verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec31e-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Zahlungsdatei im TXT-Format](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="ec31e-451">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ec31e-451">Additional resources</span></span>

- [<span data-ttu-id="ec31e-452">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="ec31e-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="ec31e-453">Herunterladen elektronischer Berichterstellungskonfigurationen von Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ec31e-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="ec31e-454">Herunterladen von EB-Konfigurationen aus dem globalen Repository des Konfigurationsdienstes</span><span class="sxs-lookup"><span data-stu-id="ec31e-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
