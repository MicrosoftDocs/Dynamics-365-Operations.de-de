---
title: ER Domänenspezifisches Datenmodell entwerfen
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551523"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="0d1fc-103">ER Domänenspezifisches Datenmodell entwerfen</span><span class="sxs-lookup"><span data-stu-id="0d1fc-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d1fc-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="0d1fc-105">Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="0d1fc-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationen unter Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="0d1fc-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="0d1fc-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0d1fc-109">Wählen Sie den Konfigurationsanbieter für Beispielunternehmen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="0d1fc-110">aus Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="0d1fc-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="0d1fc-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="0d1fc-112">Sie erstellen eine Konfiguration, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="0d1fc-113">Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="0d1fc-114">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="0d1fc-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="0d1fc-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="0d1fc-116">Geben Sie im Feld "Name" "Zahlungen (vereinfachtes Modell)" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="0d1fc-117">Zahlungen (vereinfachtes Modell)</span><span class="sxs-lookup"><span data-stu-id="0d1fc-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="0d1fc-118">Geben Sie im Feld "Beschreibung" "Zahlungsmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="0d1fc-119">Zahlungsmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0d1fc-119">Payment model configuration</span></span>  
    * <span data-ttu-id="0d1fc-120">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="0d1fc-121">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="0d1fc-122">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="0d1fc-123">Klicken Sie auf die Schaltfläche "Konfiguration erstellen", um die Konfigurationserstellungsaufgabe abzuschließen</span><span class="sxs-lookup"><span data-stu-id="0d1fc-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="0d1fc-124">Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="0d1fc-124">Create a data model</span></span>
    * <span data-ttu-id="0d1fc-125">Sie erstellen ein neues Datenmodell für die ausgewählte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="0d1fc-126">Diese Konfigurationsversion hat den Status "Entwurf".</span><span class="sxs-lookup"><span data-stu-id="0d1fc-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="0d1fc-127">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="0d1fc-128">Definieren der Struktur einer Partei, die an einem Zahlungsprozess teilnimmt</span><span class="sxs-lookup"><span data-stu-id="0d1fc-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="0d1fc-129">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0d1fc-130">Geben sie im Feld „Name” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="0d1fc-131">Partei</span><span class="sxs-lookup"><span data-stu-id="0d1fc-131">Party</span></span>  
3. <span data-ttu-id="0d1fc-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-132">Click Add.</span></span>
4. <span data-ttu-id="0d1fc-133">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="0d1fc-134">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0d1fc-135">Name</span><span class="sxs-lookup"><span data-stu-id="0d1fc-135">Name</span></span>  
6. <span data-ttu-id="0d1fc-136">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="0d1fc-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-137">Click Add.</span></span>
8. <span data-ttu-id="0d1fc-138">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0d1fc-139">Partei</span><span class="sxs-lookup"><span data-stu-id="0d1fc-139">Party</span></span>  
9. <span data-ttu-id="0d1fc-140">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="0d1fc-141">Definieren Sie die Bankstruktur für dieses Modell</span><span class="sxs-lookup"><span data-stu-id="0d1fc-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="0d1fc-142">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0d1fc-143">Geben Sie im Feld "Name" "Agent" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="0d1fc-144">Beauftragter</span><span class="sxs-lookup"><span data-stu-id="0d1fc-144">Agent</span></span>  
3. <span data-ttu-id="0d1fc-145">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="0d1fc-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-146">Click Add.</span></span>
5. <span data-ttu-id="0d1fc-147">Geben Sie im Feld „Beschreibung” die Bezeichnung „Finanzinstitut (z. B. eine Bank) ein, das ein Konto für die Partei (Debitor/Kreditor) verwaltet.”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="0d1fc-148">Finanzinstitut (z. B. eine Bank), das ein Konto für die Partei (Debitor/Kreditor) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="0d1fc-149">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="0d1fc-150">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0d1fc-151">Name</span><span class="sxs-lookup"><span data-stu-id="0d1fc-151">Name</span></span>  
8. <span data-ttu-id="0d1fc-152">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="0d1fc-153">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-153">Click Add.</span></span>
10. <span data-ttu-id="0d1fc-154">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="0d1fc-155">Geben Sie im Feld "Name" "SWIFT" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="0d1fc-156">SWIFT BIC</span><span class="sxs-lookup"><span data-stu-id="0d1fc-156">SWIFT</span></span>  
12. <span data-ttu-id="0d1fc-157">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-157">Click Add.</span></span>
13. <span data-ttu-id="0d1fc-158">Geben Sie im Feld „Beschreibung” die Bezeichnung „Bankidentifizierungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="0d1fc-159">Bankidentifizierungscode</span><span class="sxs-lookup"><span data-stu-id="0d1fc-159">Bank identification code</span></span>  
14. <span data-ttu-id="0d1fc-160">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="0d1fc-161">Geben Sie im Feld "Name" "RoutingNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="0d1fc-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="0d1fc-162">RoutingNumber</span></span>  
16. <span data-ttu-id="0d1fc-163">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-163">Click Add.</span></span>
17. <span data-ttu-id="0d1fc-164">Geben Sie im Feld „Beschreibung” die Bezeichnung „Routingnummer” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="0d1fc-165">Bankleitzahl</span><span class="sxs-lookup"><span data-stu-id="0d1fc-165">Routing number</span></span>  
18. <span data-ttu-id="0d1fc-166">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="0d1fc-167">Definieren Sie die Kontostruktur für dieses Modell</span><span class="sxs-lookup"><span data-stu-id="0d1fc-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="0d1fc-168">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0d1fc-169">Geben Sie im Feld "Name" "Konto" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="0d1fc-170">Konto</span><span class="sxs-lookup"><span data-stu-id="0d1fc-170">Account</span></span>  
3. <span data-ttu-id="0d1fc-171">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="0d1fc-172">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-172">Click Add.</span></span>
5. <span data-ttu-id="0d1fc-173">Geben Sie im Feld „Beschreibung” die Bezeichnung „Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="0d1fc-174">Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).</span><span class="sxs-lookup"><span data-stu-id="0d1fc-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="0d1fc-175">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="0d1fc-176">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0d1fc-177">Währung</span><span class="sxs-lookup"><span data-stu-id="0d1fc-177">Currency</span></span>  
8. <span data-ttu-id="0d1fc-178">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="0d1fc-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-179">Click Add.</span></span>
10. <span data-ttu-id="0d1fc-180">Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="0d1fc-181">Währungscode</span><span class="sxs-lookup"><span data-stu-id="0d1fc-181">Currency code</span></span>  
11. <span data-ttu-id="0d1fc-182">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0d1fc-183">Geben Sie im Feld "Name" "Nummer" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="0d1fc-184">Anzahl</span><span class="sxs-lookup"><span data-stu-id="0d1fc-184">Number</span></span>  
13. <span data-ttu-id="0d1fc-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-185">Click Add.</span></span>
14. <span data-ttu-id="0d1fc-186">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="0d1fc-187">Geben Sie im Feld "Name" "IBAN" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="0d1fc-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="0d1fc-188">IBAN</span></span>  
16. <span data-ttu-id="0d1fc-189">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-189">Click Add.</span></span>
17. <span data-ttu-id="0d1fc-190">Geben Sie im Feld „Beschreibung” die „Internationale Bankkontonummer” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="0d1fc-191">Internationale Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="0d1fc-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="0d1fc-192">Definieren der Zahlungsmeldungsstruktur für Kreditübertragungs-Zahlungstyp.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="0d1fc-193">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0d1fc-194">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="0d1fc-195">Geben Sie im Feld "Name" "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="0d1fc-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0d1fc-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0d1fc-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="0d1fc-197">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-197">Click Add.</span></span>
5. <span data-ttu-id="0d1fc-198">Geben Sie im Feld „Suchen” die Bezeichnung „CustomerCreditTransferInitiation” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0d1fc-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0d1fc-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="0d1fc-200">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-200">Click Find previous.</span></span>
7. <span data-ttu-id="0d1fc-201">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="0d1fc-202">Geben Sie im Feld "Name" 'MessageIdentification' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="0d1fc-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="0d1fc-203">MessageIdentification</span></span>  
9. <span data-ttu-id="0d1fc-204">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-204">Click Add.</span></span>
10. <span data-ttu-id="0d1fc-205">Geben Sie im Feld „Beschreibung” die Bezeichnung „Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen wird (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="0d1fc-206">Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="0d1fc-207">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0d1fc-208">Geben Sie im Feld "Name" 'ProcessingDateTime' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="0d1fc-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="0d1fc-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="0d1fc-210">Wählen Sie im Feld "Artikeltyp" 'DateTime' aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="0d1fc-211">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-211">Click Add.</span></span>
15. <span data-ttu-id="0d1fc-212">Geben Sie im Feld „Beschreibung” die Bezeichnung „Das Datum und die Uhrzeit der Erstellung der Zahlungsnachricht.” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="0d1fc-213">Das Datum und die Uhrzeit der Erstellung der Zahlungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="0d1fc-214">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="0d1fc-215">Definieren Sie die Zahlungsbuchungsstruktur für dieses Modell.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="0d1fc-216">Geben Sie im Feld "Name" "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0d1fc-217">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="0d1fc-217">Payments</span></span>  
18. <span data-ttu-id="0d1fc-218">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="0d1fc-219">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-219">Click Add.</span></span>
20. <span data-ttu-id="0d1fc-220">Geben Sie im Feld "Beschreibung" "Zahlungspositionen der aktuellen Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="0d1fc-221">Zahlungspositionen der aktuellen Nachricht</span><span class="sxs-lookup"><span data-stu-id="0d1fc-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="0d1fc-222">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="0d1fc-223">Geben Sie im Feld "Name" 'Kreditor' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="0d1fc-224">Zahlungsempfänger</span><span class="sxs-lookup"><span data-stu-id="0d1fc-224">Creditor</span></span>  
23. <span data-ttu-id="0d1fc-225">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="0d1fc-226">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-226">Click Add.</span></span>
25. <span data-ttu-id="0d1fc-227">Geben Sie im Feld „Beschreibung” die „Bezeichnung Partei, für die ein Geldbetrag fällig ist” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="0d1fc-228">Partei, für die ein Geldbetrag fällig ist.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="0d1fc-229">Klicken Sie auf „Artikelreferenz wechseln”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="0d1fc-230">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0d1fc-231">Partei</span><span class="sxs-lookup"><span data-stu-id="0d1fc-231">Party</span></span>  
28. <span data-ttu-id="0d1fc-232">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-232">Click Find next.</span></span>
29. <span data-ttu-id="0d1fc-233">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0d1fc-233">Click OK.</span></span>
30. <span data-ttu-id="0d1fc-234">Geben Sie im Feld „Suchen” die Bezeichnung „Zahlungen” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="0d1fc-235">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="0d1fc-235">Payments</span></span>  
31. <span data-ttu-id="0d1fc-236">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-236">Click Find next.</span></span>
32. <span data-ttu-id="0d1fc-237">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="0d1fc-238">Geben Sie im Feld "Name" "Zahlungspflichtiger" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="0d1fc-239">Zahlungspflichtiger</span><span class="sxs-lookup"><span data-stu-id="0d1fc-239">Debtor</span></span>  
34. <span data-ttu-id="0d1fc-240">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-240">Click Add.</span></span>
35. <span data-ttu-id="0d1fc-241">Geben Sie im Feld „Beschreibung” „Partei, die dem (letztendlichen) Kreditor einen Geldbetrag schuldet.” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="0d1fc-242">Partei, die dem (letztendlichen) Kreditor einen Geldbetrag schuldet.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="0d1fc-243">Klicken Sie auf „Artikelreferenz wechseln”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="0d1fc-244">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0d1fc-245">Partei</span><span class="sxs-lookup"><span data-stu-id="0d1fc-245">Party</span></span>  
38. <span data-ttu-id="0d1fc-246">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-246">Click Find next.</span></span>
39. <span data-ttu-id="0d1fc-247">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="0d1fc-247">Click OK.</span></span>
40. <span data-ttu-id="0d1fc-248">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-248">Click Find next.</span></span>
41. <span data-ttu-id="0d1fc-249">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="0d1fc-250">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="0d1fc-251">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d1fc-251">Description</span></span>  
43. <span data-ttu-id="0d1fc-252">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="0d1fc-253">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-253">Click Add.</span></span>
45. <span data-ttu-id="0d1fc-254">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="0d1fc-255">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0d1fc-256">Währung</span><span class="sxs-lookup"><span data-stu-id="0d1fc-256">Currency</span></span>  
47. <span data-ttu-id="0d1fc-257">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-257">Click Add.</span></span>
48. <span data-ttu-id="0d1fc-258">Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="0d1fc-259">Währungscode</span><span class="sxs-lookup"><span data-stu-id="0d1fc-259">Currency code</span></span>  
49. <span data-ttu-id="0d1fc-260">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="0d1fc-261">Geben Sie im Feld "Name" 'TransactionDate' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="0d1fc-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="0d1fc-262">TransactionDate</span></span>  
51. <span data-ttu-id="0d1fc-263">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="0d1fc-264">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-264">Click Add.</span></span>
53. <span data-ttu-id="0d1fc-265">Geben Sie im Feld „Beschreibung” das „Transaktionsdatum” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="0d1fc-266">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="0d1fc-266">Transaction date</span></span>  
54. <span data-ttu-id="0d1fc-267">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="0d1fc-268">Geben Sie im Feld "Name" 'InstructedAmount' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="0d1fc-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="0d1fc-269">InstructedAmount</span></span>  
56. <span data-ttu-id="0d1fc-270">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="0d1fc-271">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-271">Click Add.</span></span>
58. <span data-ttu-id="0d1fc-272">Geben Sie im Feld „Beschreibung” „Der zwischen Debitor und Kreditor vor Abzug von Gebühren zu transferierende Geldbetrag, vor Abzug von Gebühren”.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="0d1fc-273">Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.'</span><span class="sxs-lookup"><span data-stu-id="0d1fc-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="0d1fc-274">Zwischen Debitor und Kreditor vor Abzug von Gebühren transferierter Geldbetrag.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="0d1fc-275">Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="0d1fc-276">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="0d1fc-277">Geben Sie im Feld "Name" 'End2EndID' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="0d1fc-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="0d1fc-278">End2EndID</span></span>  
61. <span data-ttu-id="0d1fc-279">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="0d1fc-280">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-280">Click Add.</span></span>
63. <span data-ttu-id="0d1fc-281">Geben Sie im Feld „Beschreibung” „Die eindeutige Kennung, die von der initiierenden Partei zugewiesen wird” ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="0d1fc-282">Diese Kennung wird unverändert in der gesamten End-to-End-Kette übergeben' ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="0d1fc-283">Die eindeutige Kennung, die von der initiierenden Partei zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="0d1fc-284">Diese Kennung wird unverändert in der gesamten End-to-End-Kette übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="0d1fc-285">Geben Sie im Feld "Name" "PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="0d1fc-286">Der PaymentModel-Name wird an vordefinierten Schnittstellen von Zahlungsformularen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="0d1fc-287">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0d1fc-287">Click Save.</span></span>
66. <span data-ttu-id="0d1fc-288">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0d1fc-288">Close the page.</span></span>

