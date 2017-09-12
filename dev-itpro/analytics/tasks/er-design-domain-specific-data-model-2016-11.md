--- 
title: "Entwerfen eines domänenspezifisches Datenmodell für elektronische Berichterstellung"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle \"Entwickler für elektronische Berichterstellung\" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3349d4e910cf1a97eb099aaa7d1155732be3a21f
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="48859-103">Entwerfen eines domänenspezifisches Datenmodell für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="48859-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48859-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="48859-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="48859-105">Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="48859-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="48859-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationen unter Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="48859-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="48859-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="48859-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="48859-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="48859-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="48859-109">Wählen Sie den Konfigurationsanbieter für Beispielunternehmen Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="48859-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="48859-110">aus Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="48859-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="48859-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="48859-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="48859-112">Sie erstellen eine Konfiguration, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="48859-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="48859-113">Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="48859-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="48859-114">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="48859-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="48859-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="48859-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="48859-116">Geben Sie im Feld "Name" "Zahlungen (vereinfachtes Modell)" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="48859-117">Zahlungen (vereinfachtes Modell)</span><span class="sxs-lookup"><span data-stu-id="48859-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="48859-118">Geben Sie im Feld "Beschreibung" "Zahlungsmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="48859-119">Zahlungsmodellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="48859-119">Payment model configuration</span></span>  
    * <span data-ttu-id="48859-120">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="48859-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="48859-121">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="48859-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="48859-122">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="48859-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="48859-123">Klicken Sie auf die Schaltfläche "Konfiguration erstellen", um die Konfigurationserstellungsaufgabe abzuschließen</span><span class="sxs-lookup"><span data-stu-id="48859-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="48859-124">Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="48859-124">Create a data model</span></span>
    * <span data-ttu-id="48859-125">Sie erstellen ein neues Datenmodell für die ausgewählte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="48859-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="48859-126">Diese Konfigurationsversion hat den Status "Entwurf".</span><span class="sxs-lookup"><span data-stu-id="48859-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="48859-127">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="48859-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="48859-128">Definieren der Struktur einer Partei, die an einem Zahlungsprozess teilnimmt</span><span class="sxs-lookup"><span data-stu-id="48859-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="48859-129">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="48859-130">Geben sie im Feld „Name” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="48859-131">Partei</span><span class="sxs-lookup"><span data-stu-id="48859-131">Party</span></span>  
3. <span data-ttu-id="48859-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-132">Click Add.</span></span>
4. <span data-ttu-id="48859-133">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="48859-134">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="48859-135">Name</span><span class="sxs-lookup"><span data-stu-id="48859-135">Name</span></span>  
6. <span data-ttu-id="48859-136">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="48859-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="48859-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-137">Click Add.</span></span>
8. <span data-ttu-id="48859-138">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="48859-139">Partei</span><span class="sxs-lookup"><span data-stu-id="48859-139">Party</span></span>  
9. <span data-ttu-id="48859-140">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="48859-141">Definieren Sie die Bankstruktur für dieses Modell</span><span class="sxs-lookup"><span data-stu-id="48859-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="48859-142">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="48859-143">Geben Sie im Feld "Name" "Agent" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="48859-144">Beauftragter</span><span class="sxs-lookup"><span data-stu-id="48859-144">Agent</span></span>  
3. <span data-ttu-id="48859-145">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="48859-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="48859-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-146">Click Add.</span></span>
5. <span data-ttu-id="48859-147">Geben Sie im Feld „Beschreibung” die Bezeichnung „Finanzinstitut (z. B. eine Bank) ein, das ein Konto für die Partei (Debitor/Kreditor) verwaltet.”.</span><span class="sxs-lookup"><span data-stu-id="48859-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="48859-148">Finanzinstitut (z. B. eine Bank), das ein Konto für die Partei (Debitor/Kreditor) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="48859-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="48859-149">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="48859-150">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="48859-151">Name</span><span class="sxs-lookup"><span data-stu-id="48859-151">Name</span></span>  
8. <span data-ttu-id="48859-152">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="48859-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="48859-153">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-153">Click Add.</span></span>
10. <span data-ttu-id="48859-154">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="48859-155">Geben Sie im Feld "Name" "SWIFT" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="48859-156">SWIFT BIC</span><span class="sxs-lookup"><span data-stu-id="48859-156">SWIFT</span></span>  
12. <span data-ttu-id="48859-157">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-157">Click Add.</span></span>
13. <span data-ttu-id="48859-158">Geben Sie im Feld „Beschreibung” die Bezeichnung „Bankidentifizierungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="48859-159">Bankidentifizierungscode</span><span class="sxs-lookup"><span data-stu-id="48859-159">Bank identification code</span></span>  
14. <span data-ttu-id="48859-160">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="48859-161">Geben Sie im Feld "Name" "RoutingNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="48859-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="48859-162">RoutingNumber</span></span>  
16. <span data-ttu-id="48859-163">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-163">Click Add.</span></span>
17. <span data-ttu-id="48859-164">Geben Sie im Feld „Beschreibung” die Bezeichnung „Routingnummer” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="48859-165">Bankleitzahl</span><span class="sxs-lookup"><span data-stu-id="48859-165">Routing number</span></span>  
18. <span data-ttu-id="48859-166">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="48859-167">Definieren Sie die Kontostruktur für dieses Modell</span><span class="sxs-lookup"><span data-stu-id="48859-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="48859-168">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="48859-169">Geben Sie im Feld "Name" "Konto" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="48859-170">Konto</span><span class="sxs-lookup"><span data-stu-id="48859-170">Account</span></span>  
3. <span data-ttu-id="48859-171">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="48859-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="48859-172">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-172">Click Add.</span></span>
5. <span data-ttu-id="48859-173">Geben Sie im Feld „Beschreibung” die Bezeichnung „Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="48859-174">Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).</span><span class="sxs-lookup"><span data-stu-id="48859-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="48859-175">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="48859-176">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="48859-177">Währung</span><span class="sxs-lookup"><span data-stu-id="48859-177">Currency</span></span>  
8. <span data-ttu-id="48859-178">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="48859-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="48859-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-179">Click Add.</span></span>
10. <span data-ttu-id="48859-180">Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="48859-181">Währungscode</span><span class="sxs-lookup"><span data-stu-id="48859-181">Currency code</span></span>  
11. <span data-ttu-id="48859-182">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="48859-183">Geben Sie im Feld "Name" "Nummer" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="48859-184">Anzahl</span><span class="sxs-lookup"><span data-stu-id="48859-184">Number</span></span>  
13. <span data-ttu-id="48859-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-185">Click Add.</span></span>
14. <span data-ttu-id="48859-186">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="48859-187">Geben Sie im Feld "Name" "IBAN" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="48859-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="48859-188">IBAN</span></span>  
16. <span data-ttu-id="48859-189">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-189">Click Add.</span></span>
17. <span data-ttu-id="48859-190">Geben Sie im Feld „Beschreibung” die „Internationale Bankkontonummer” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="48859-191">Internationale Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="48859-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="48859-192">Definieren der Zahlungsmeldungsstruktur für Kreditübertragungs-Zahlungstyp.</span><span class="sxs-lookup"><span data-stu-id="48859-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="48859-193">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="48859-194">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="48859-195">Geben Sie im Feld "Name" "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="48859-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="48859-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="48859-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="48859-197">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-197">Click Add.</span></span>
5. <span data-ttu-id="48859-198">Geben Sie im Feld „Suchen” die Bezeichnung „CustomerCreditTransferInitiation” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="48859-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="48859-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="48859-200">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-200">Click Find previous.</span></span>
7. <span data-ttu-id="48859-201">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="48859-202">Geben Sie im Feld "Name" 'MessageIdentification' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="48859-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="48859-203">MessageIdentification</span></span>  
9. <span data-ttu-id="48859-204">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-204">Click Add.</span></span>
10. <span data-ttu-id="48859-205">Geben Sie im Feld „Beschreibung” die Bezeichnung „Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen wird (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="48859-206">Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="48859-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="48859-207">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="48859-208">Geben Sie im Feld "Name" 'ProcessingDateTime' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="48859-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="48859-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="48859-210">Wählen Sie im Feld "Artikeltyp" 'DateTime' aus.</span><span class="sxs-lookup"><span data-stu-id="48859-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="48859-211">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-211">Click Add.</span></span>
15. <span data-ttu-id="48859-212">Geben Sie im Feld „Beschreibung” die Bezeichnung „Das Datum und die Uhrzeit der Erstellung der Zahlungsnachricht.” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="48859-213">Das Datum und die Uhrzeit der Erstellung der Zahlungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="48859-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="48859-214">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="48859-215">Definieren Sie die Zahlungsbuchungsstruktur für dieses Modell.</span><span class="sxs-lookup"><span data-stu-id="48859-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="48859-216">Geben Sie im Feld "Name" "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="48859-217">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="48859-217">Payments</span></span>  
18. <span data-ttu-id="48859-218">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="48859-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="48859-219">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-219">Click Add.</span></span>
20. <span data-ttu-id="48859-220">Geben Sie im Feld "Beschreibung" "Zahlungspositionen der aktuellen Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="48859-221">Zahlungspositionen der aktuellen Nachricht</span><span class="sxs-lookup"><span data-stu-id="48859-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="48859-222">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="48859-223">Geben Sie im Feld "Name" 'Kreditor' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="48859-224">Zahlungsempfänger</span><span class="sxs-lookup"><span data-stu-id="48859-224">Creditor</span></span>  
23. <span data-ttu-id="48859-225">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="48859-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="48859-226">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-226">Click Add.</span></span>
25. <span data-ttu-id="48859-227">Geben Sie im Feld „Beschreibung” die „Bezeichnung Partei, für die ein Geldbetrag fällig ist” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="48859-228">Partei, für die ein Geldbetrag fällig ist.</span><span class="sxs-lookup"><span data-stu-id="48859-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="48859-229">Klicken Sie auf „Artikelreferenz wechseln”.</span><span class="sxs-lookup"><span data-stu-id="48859-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="48859-230">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="48859-231">Partei</span><span class="sxs-lookup"><span data-stu-id="48859-231">Party</span></span>  
28. <span data-ttu-id="48859-232">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-232">Click Find next.</span></span>
29. <span data-ttu-id="48859-233">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="48859-233">Click OK.</span></span>
30. <span data-ttu-id="48859-234">Geben Sie im Feld „Suchen” die Bezeichnung „Zahlungen” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="48859-235">Zahlungen</span><span class="sxs-lookup"><span data-stu-id="48859-235">Payments</span></span>  
31. <span data-ttu-id="48859-236">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-236">Click Find next.</span></span>
32. <span data-ttu-id="48859-237">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="48859-238">Geben Sie im Feld "Name" "Zahlungspflichtiger" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="48859-239">Zahlungspflichtiger</span><span class="sxs-lookup"><span data-stu-id="48859-239">Debtor</span></span>  
34. <span data-ttu-id="48859-240">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-240">Click Add.</span></span>
35. <span data-ttu-id="48859-241">Geben Sie im Feld „Beschreibung” „Partei, die dem (letztendlichen) Kreditor einen Geldbetrag schuldet.” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="48859-242">Partei, die dem (letztendlichen) Kreditor einen Geldbetrag schuldet.</span><span class="sxs-lookup"><span data-stu-id="48859-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="48859-243">Klicken Sie auf „Artikelreferenz wechseln”.</span><span class="sxs-lookup"><span data-stu-id="48859-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="48859-244">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="48859-245">Partei</span><span class="sxs-lookup"><span data-stu-id="48859-245">Party</span></span>  
38. <span data-ttu-id="48859-246">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-246">Click Find next.</span></span>
39. <span data-ttu-id="48859-247">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="48859-247">Click OK.</span></span>
40. <span data-ttu-id="48859-248">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="48859-248">Click Find next.</span></span>
41. <span data-ttu-id="48859-249">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="48859-250">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="48859-251">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48859-251">Description</span></span>  
43. <span data-ttu-id="48859-252">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="48859-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="48859-253">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-253">Click Add.</span></span>
45. <span data-ttu-id="48859-254">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="48859-255">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="48859-256">Währung</span><span class="sxs-lookup"><span data-stu-id="48859-256">Currency</span></span>  
47. <span data-ttu-id="48859-257">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-257">Click Add.</span></span>
48. <span data-ttu-id="48859-258">Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="48859-259">Währungscode</span><span class="sxs-lookup"><span data-stu-id="48859-259">Currency code</span></span>  
49. <span data-ttu-id="48859-260">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="48859-261">Geben Sie im Feld "Name" 'TransactionDate' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="48859-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="48859-262">TransactionDate</span></span>  
51. <span data-ttu-id="48859-263">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="48859-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="48859-264">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-264">Click Add.</span></span>
53. <span data-ttu-id="48859-265">Geben Sie im Feld „Beschreibung” das „Transaktionsdatum” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="48859-266">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="48859-266">Transaction date</span></span>  
54. <span data-ttu-id="48859-267">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="48859-268">Geben Sie im Feld "Name" 'InstructedAmount' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="48859-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="48859-269">InstructedAmount</span></span>  
56. <span data-ttu-id="48859-270">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="48859-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="48859-271">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-271">Click Add.</span></span>
58. <span data-ttu-id="48859-272">Geben Sie im Feld „Beschreibung” „Der zwischen Debitor und Kreditor vor Abzug von Gebühren zu transferierende Geldbetrag, vor Abzug von Gebühren”.</span><span class="sxs-lookup"><span data-stu-id="48859-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="48859-273">Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.'</span><span class="sxs-lookup"><span data-stu-id="48859-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="48859-274">Zwischen Debitor und Kreditor vor Abzug von Gebühren transferierter Geldbetrag.</span><span class="sxs-lookup"><span data-stu-id="48859-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="48859-275">Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.</span><span class="sxs-lookup"><span data-stu-id="48859-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="48859-276">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48859-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="48859-277">Geben Sie im Feld "Name" 'End2EndID' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="48859-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="48859-278">End2EndID</span></span>  
61. <span data-ttu-id="48859-279">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="48859-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="48859-280">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="48859-280">Click Add.</span></span>
63. <span data-ttu-id="48859-281">Geben Sie im Feld „Beschreibung” „Die eindeutige Kennung, die von der initiierenden Partei zugewiesen wird” ein.</span><span class="sxs-lookup"><span data-stu-id="48859-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="48859-282">Diese Kennung wird unverändert in der gesamten End-to-End-Kette übergeben' ein.</span><span class="sxs-lookup"><span data-stu-id="48859-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="48859-283">Die eindeutige Kennung, die von der initiierenden Partei zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="48859-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="48859-284">Diese Kennung wird unverändert in der gesamten End-to-End-Kette übergeben.</span><span class="sxs-lookup"><span data-stu-id="48859-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="48859-285">Geben Sie im Feld "Name" "PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="48859-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="48859-286">Der PaymentModel-Name wird an vordefinierten Schnittstellen von Zahlungsformularen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="48859-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="48859-287">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="48859-287">Click Save.</span></span>
66. <span data-ttu-id="48859-288">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="48859-288">Close the page.</span></span>


