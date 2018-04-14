--- 
title: Einrichten elektronischer Signaturen
description: Verwenden Sie diese Prozedur, um elektronische Signaturen einzurichten.
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d57fc2bcc514f7be8d6edffca5ada0b91aadf073
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="87995-103">Einrichten elektronischer Signaturen</span><span class="sxs-lookup"><span data-stu-id="87995-103">Set up electronic signatures</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87995-104">Verwenden Sie diese Prozedur, um elektronische Signaturen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="87995-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="87995-105">Eine elektronische Signatur bestätigt die Identität einer Person, die im Begriff ist, einen Datenverarbeitungsprozess zu starten oder zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="87995-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="87995-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DAT.</span><span class="sxs-lookup"><span data-stu-id="87995-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="87995-107">Konfigurationsschlüssel "Elektronische Signatur " aktivieren</span><span class="sxs-lookup"><span data-stu-id="87995-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="87995-108">Gehen Sie zu "Systemadministration" > "Einstellungen" > "Lizenzkonfiguration".</span><span class="sxs-lookup"><span data-stu-id="87995-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="87995-109">Erweitern Sie 'Administration' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="87995-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="87995-110">Vergewissern Sie sich, dass das Kontrollkästchen Elektronische Signatur aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87995-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="87995-111">Wenn das Kontrollkästchen für elektronische Signatur nicht aktiviert ist, müssen Sie Wartungsmodus aktivieren.</span><span class="sxs-lookup"><span data-stu-id="87995-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="87995-112">Sie können den Wartungsmodus in dieser Umgebung aktivieren, indem Sie den Wartungsvorgang über Lifecycle Services durchführen oder das Deployment.Setup-Tool lokal verwenden.</span><span class="sxs-lookup"><span data-stu-id="87995-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="87995-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="87995-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="87995-114">Einrichten von Parametern für elektronische Signaturen</span><span class="sxs-lookup"><span data-stu-id="87995-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="87995-115">Wechseln Sie zu "Organisationsverwaltung" > "Einrichten" > "Elektronische Signatur" > "Parameter für elektronische Signatur".</span><span class="sxs-lookup"><span data-stu-id="87995-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="87995-116">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="87995-116">Click Edit.</span></span>
3. <span data-ttu-id="87995-117">Geben Sie im Feld Hinweis einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="87995-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="87995-118">Geben Sie den Hinweis ein, den Signaturgeber empfangen, wenn eine Signatur angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="87995-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="87995-119">Sie können einen beliebigen Text eingeben.</span><span class="sxs-lookup"><span data-stu-id="87995-119">You can enter any text.</span></span> <span data-ttu-id="87995-120">In der Regel informiert dieser Text den Benutzer über die Bedeutung des elektronischen Signierens eines Dokuments.</span><span class="sxs-lookup"><span data-stu-id="87995-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="87995-121">Klicken Sie auf die Schaltfläche Übersetzungen, um den Hinweistext in weiteren Sprachen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="87995-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="87995-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="87995-122">Click Save.</span></span>
5. <span data-ttu-id="87995-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="87995-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="87995-124">Einrichten von Ursachencodes für elektronische Signaturen</span><span class="sxs-lookup"><span data-stu-id="87995-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="87995-125">Wechseln Sie zu "Organisationsverwaltung" > "Elektronische Signatur einrichten" > "Gründe für elektronische Signatur".</span><span class="sxs-lookup"><span data-stu-id="87995-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="87995-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="87995-126">Click New.</span></span>
    * <span data-ttu-id="87995-127">Ursachencodes müssen vor der Verwendung elektronischer Signaturen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="87995-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="87995-128">Zum Signieren eines Dokuments ist ein gültiger Ursachencode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="87995-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="87995-129">Ein Signaturgeber wählt einen Ursachencode aus, um den Zweck einer elektronischen Signatur anzugeben.</span><span class="sxs-lookup"><span data-stu-id="87995-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="87995-130">Mit einem Ursachencode könnte z. B. eine rechtliche Genehmigung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="87995-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="87995-131">Geben Sie im Feld "Grundcode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="87995-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="87995-132">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="87995-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="87995-133">Geben Sie Ursachencodes, nach Bedarf ein.</span><span class="sxs-lookup"><span data-stu-id="87995-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="87995-134">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="87995-134">Click Save.</span></span>
6. <span data-ttu-id="87995-135">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="87995-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="87995-136">Anfordern elektronischer Signaturen für vorhandene Prozesse</span><span class="sxs-lookup"><span data-stu-id="87995-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="87995-137">Wechseln Sie zu "Organisationsverwaltung" > "Einrichtung" > "Elektronische Signatur einrichten" > "Anforderungen für elektronische Signatur".</span><span class="sxs-lookup"><span data-stu-id="87995-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="87995-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="87995-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="87995-139">Auswählen eines Prozesses, der elektronische Signaturen erfordert.</span><span class="sxs-lookup"><span data-stu-id="87995-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="87995-140">Aktivieren oder deaktivieren Sie das Kontrollkästchen Signatur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="87995-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="87995-141">Wiederholen Sie diese Schritte für jeden Prozess, der elektronische Signaturen erfordert.</span><span class="sxs-lookup"><span data-stu-id="87995-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="87995-142">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="87995-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="87995-143">Erstellen einer benutzerdefinierten Anforderung für elektronische Signaturen</span><span class="sxs-lookup"><span data-stu-id="87995-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="87995-144">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="87995-144">Click New.</span></span>
2. <span data-ttu-id="87995-145">Aktivieren oder deaktivieren Sie das Kontrollkästchen Signatur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="87995-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="87995-146">Geben Sie im Feld Name einen eindeutigen Namen für den Prozess ein, der elektronische Signaturen erfordert.</span><span class="sxs-lookup"><span data-stu-id="87995-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="87995-147">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="87995-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="87995-148">Suchen und wählen Sie in der Liste die Tabelle aus, in der die zu signierenden Daten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="87995-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="87995-149">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="87995-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="87995-150">Klicken Sie im Feld "Feldname" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="87995-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="87995-151">Wählen Sie in der Liste das Feld in der Tabelle aus, das überwacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="87995-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="87995-152">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="87995-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="87995-153">Geben Sie an, wann eine Signatur erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="87995-153">Specify when a signature is required.</span></span>     <span data-ttu-id="87995-154">Wählen Sie Immer aus, wenn eine Signatur erforderlich ist, wenn sich die Felddaten ändern.</span><span class="sxs-lookup"><span data-stu-id="87995-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="87995-155">Wählen Sie Nur aus, wenn eine Signatur nur unter bestimmten Bedingungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="87995-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="87995-156">Wenn Sie Nur auswählen, müssen Sie eine der folgenden Optionen auch auswählen: Wenn ein Datensatz eingefügt wird, wenn ein Datensatz aktualisiert wird oder wenn ein Datensatz gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="87995-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="87995-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="87995-157">Click Save.</span></span>
11. <span data-ttu-id="87995-158">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="87995-158">Close the page.</span></span>


