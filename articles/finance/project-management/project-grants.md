---
title: Projektzuschüsse
description: In diesem Thema wird erläutert, wie Sie einen Zuschuss erstellen oder ändern.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282828"
---
# <a name="project-grants"></a><span data-ttu-id="283e6-103">Projektzuschüsse</span><span class="sxs-lookup"><span data-stu-id="283e6-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="283e6-104">Ein Zuschuss stellt eine monetäre Zuwendung für einen bestimmten Zweck oder ein Projekt dar.</span><span class="sxs-lookup"><span data-stu-id="283e6-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="283e6-105">Die Verwendung von Zuschüssen unterliegt in der Regel Beschränkungen.</span><span class="sxs-lookup"><span data-stu-id="283e6-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="283e6-106">Unter "Projektverwaltung und Buchhaltung" können Zuschüsse eingegeben und nachverfolgt sowie deren Beziehungen zu Projekten und Projektverträgen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="283e6-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="283e6-107">So können Sie etwa die folgenden Aufgaben durchführen:</span><span class="sxs-lookup"><span data-stu-id="283e6-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="283e6-108">Zuordnen von Zuschüssen zu Projekten und Finanzierungsquellen, indem Sie Links zu den Seiten **Projekt** und **Projektvertragsdetails** verwenden.</span><span class="sxs-lookup"><span data-stu-id="283e6-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="283e6-109">Eingeben und Nachverfolgen von Änderungen an Zuschüssen bei einem Statuswechsel.</span><span class="sxs-lookup"><span data-stu-id="283e6-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="283e6-110">Eingeben und Nachverfolgen von Kosten, angeforderten Beträgen und vergebenen Beträgen.</span><span class="sxs-lookup"><span data-stu-id="283e6-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="283e6-111">Erstellen von Hauptzuschüssen und Zuordnen von entsprechenden untergeordneten Zuschüssen.</span><span class="sxs-lookup"><span data-stu-id="283e6-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="283e6-112">Sie können einen Zuschuss erstellen, indem Sie alle Details in einen neuen Datensatz eingeben, oder Sie können die Details aus einem vorhandenen Zuschuss kopieren und dann überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="283e6-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="283e6-113">Neuen Zuschuss erstellen</span><span class="sxs-lookup"><span data-stu-id="283e6-113">Create a new grant</span></span>

1. <span data-ttu-id="283e6-114">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.</span><span class="sxs-lookup"><span data-stu-id="283e6-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="283e6-115">Wählen Sie **Neu** \> **Zuschüsse** aus.</span><span class="sxs-lookup"><span data-stu-id="283e6-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="283e6-116">Geben Sie auf der Seite "Zuschussdetails" im Inforegister **Allgemein** in das Feld **Zuschuss-ID** einen alphanumerischen Bezeichner für den Zuschuss ein.</span><span class="sxs-lookup"><span data-stu-id="283e6-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="283e6-117">Geben Sie in das Feld **Zuschussname** einen Namen für den Zuschuss ein.</span><span class="sxs-lookup"><span data-stu-id="283e6-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="283e6-118">Fügen Sie im Feld **Beschreibung** Details zum neuen Zuschuss hinzu.</span><span class="sxs-lookup"><span data-stu-id="283e6-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="283e6-119">Die meisten anderen Felder auf der Seite sind optional und die Informationen können nach Bedarf eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="283e6-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="283e6-120">In der folgenden Liste werden die Informationen beschrieben, die in jedem Inforegister der Seite "Zuschussdetails" angegeben sind:</span><span class="sxs-lookup"><span data-stu-id="283e6-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="283e6-121">**Allgemein** – Geben Sie Name, Status, Beschreibung, Zweck und Betrag des Zuschusses ein.</span><span class="sxs-lookup"><span data-stu-id="283e6-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="283e6-122">**Kontaktdaten** – Geben Sie Details zu Mitarbeitern, zur für die Zuschussverwaltung zuständigen Abteilung sowie zum Zuschussdebitor bzw. der Organisation ein, von der der Zuschuss stammt.</span><span class="sxs-lookup"><span data-stu-id="283e6-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="283e6-123">Sie können auch angeben, ob Ihre Organisation als Vermittler fungiert, der den Zuschuss entgegennimmt und an einen anderen Empfänger weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="283e6-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="283e6-124">Wählen Sie **Hinzufügen** aus, um Kontaktdaten wie Telefonnummern und E-Mail-Adressen der Organisation hinzuzufügen, die den Zuschuss vergibt.</span><span class="sxs-lookup"><span data-stu-id="283e6-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="283e6-125">**Stichtage und Fristen** – Geben Sie die für den Zuschuss und den Zuschussantrag relevanten Datumsangaben ein.</span><span class="sxs-lookup"><span data-stu-id="283e6-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="283e6-126">Beispiele hierfür sind der Stichtag für den Antrag, das Einreichungsdatum und das Datum, an dem der Zuschuss genehmigt oder abgelehnt wird.</span><span class="sxs-lookup"><span data-stu-id="283e6-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="283e6-127">**Zugeordnete Projekte und Projektverträge** – In dieses Inforegister können Sie Informationen nur dann eingeben, wenn das Feld **Zuschuss gewähren** im Inforegister **Allgemein** auf **Aktiv**oder **Ausgezeichnet** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="283e6-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="283e6-128">Wählen Sie eine der folgenden Optionen aus, um die zugehörige Aufgabe abzuschließen:</span><span class="sxs-lookup"><span data-stu-id="283e6-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="283e6-129">**Finanzierungsquelle hinzufügen** – Fügen Sie eine neue Finanzierungsquelle für den Zuschuss hinzu.</span><span class="sxs-lookup"><span data-stu-id="283e6-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="283e6-130">Sie können dabei entweder alle Details sofort eingeben oder die Standardinformationen übernehmen und diese später ändern.</span><span class="sxs-lookup"><span data-stu-id="283e6-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="283e6-131">**Projektvertrag hinzufügen** – Fügen Sie Projektvertragsinformationen hinzu oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="283e6-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="283e6-132">**Projekt hinzufügen** – Fügen Sie Projektdetails hinzu oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="283e6-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="283e6-133">**Einrichtung** – Geben Sie Details zu passenden Fonds ein, falls diese Informationen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="283e6-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="283e6-134">Viele Organisationen, die Zuschüsse vergeben, machen es den Empfängern zur Auflage, einen bestimmten, dem bewilligten Zuschuss entsprechenden Betrag ihrer eigenen Mittel oder Ressourcen aufzuwenden.</span><span class="sxs-lookup"><span data-stu-id="283e6-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="283e6-135">In das Feld **Kennung für lokales Projekt oder Überwachungskennung** können Sie eine Kennung eingeben, die sich von der Projektkennung unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="283e6-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="283e6-136">Wenn ein Teil des Zuschusses an eine andere Organisation vergeben wird, legen Sie die Option **Untergeordneter Geber** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="283e6-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="283e6-137">Bei in den Vereinigten Staaten vergebenen Zuschüssen können Sie angeben, ob der Zuschuss von einem Bundesstaat oder vom Bund geregelt wird.</span><span class="sxs-lookup"><span data-stu-id="283e6-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="283e6-138">**Details zur Inanspruchnahme** – Geben Sie Informationen zur Häufigkeit ein, mit der Zuschussmittel entnommen, abgerechnet oder ausgegeben werden können (oder aktualisieren Sie die Informationen).</span><span class="sxs-lookup"><span data-stu-id="283e6-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="283e6-139">Erstellen eines neuen Zuschusses aus einer Kopie</span><span class="sxs-lookup"><span data-stu-id="283e6-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="283e6-140">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.</span><span class="sxs-lookup"><span data-stu-id="283e6-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="283e6-141">Wählen Sie **Neu** \> **Aus Zuschuss kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="283e6-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="283e6-142">Geben Sie einen alphanumerischen Bezeichner und einen Namen für den neuen Zuschuss ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="283e6-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="283e6-143">Überprüfen Sie auf der Seite "Zuschussdetails" die Details des kopierten Zuschusses und nehmen Sie alle notwendigen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="283e6-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="283e6-144">Die meisten Felder auf der Seite sind optional.</span><span class="sxs-lookup"><span data-stu-id="283e6-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="283e6-145">Anzeigen oder Ändern von Zuschussdetails</span><span class="sxs-lookup"><span data-stu-id="283e6-145">View or modify grant details</span></span>

1. <span data-ttu-id="283e6-146">Wechseln Sie zu **Projektverwaltung und Buchhaltung** \> **Zuschüsse** \> **Zuschüsse**.</span><span class="sxs-lookup"><span data-stu-id="283e6-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="283e6-147">Wählen Sie den Zuschuss aus, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="283e6-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="283e6-148">Klicken Sie im Aktivitätsbereich auf der Registerkarte **Zuschuss** in der Gruppe **Verwalten** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="283e6-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="283e6-149">Überprüfen Sie die Zuschussdetails und nehmen Sie alle notwendigen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="283e6-149">Review the grant details, and make any changes that are required.</span></span>
