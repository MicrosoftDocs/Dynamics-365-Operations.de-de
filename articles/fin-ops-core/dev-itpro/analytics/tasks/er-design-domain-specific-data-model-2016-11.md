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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268f661079b80551b36ad2e1877615d878350051
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681948"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="c5463-103">ER Domänenspezifisches Datenmodell entwerfen</span><span class="sxs-lookup"><span data-stu-id="c5463-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5463-104">In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine Konfiguration für elektronische Berichterstellung (ER) erstellen kann, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="c5463-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c5463-105">Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5463-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="c5463-106">In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in einem beliebigen Unternehmen ausgeführt werden, da ER-Konfigurationen unter Unternehmen geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c5463-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c5463-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="c5463-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="c5463-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="c5463-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="c5463-109">Wählen Sie den Konfigurationsanbieter für das Beispielunternehmen 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="c5463-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="c5463-110">Sollten Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="c5463-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="c5463-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="c5463-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="c5463-112">Sie erstellen eine Konfiguration, die ein Datenmodell für Dokumente zur elektronischen Zahlung enthält.</span><span class="sxs-lookup"><span data-stu-id="c5463-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c5463-113">Dieses Datenmodell wird später als Datenquelle verwendet, wenn Sie das Format der Zahlungsdokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5463-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c5463-114">Neue Datenmodellkonfiguration erstellen</span><span class="sxs-lookup"><span data-stu-id="c5463-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="c5463-115">Klicken Sie auf "Konfiguration erstellen", um das Dropdown-Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5463-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="c5463-116">Geben Sie im Feld "Name" "Zahlungen (vereinfachtes Modell)" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="c5463-117">Geben Sie im Feld "Beschreibung" "Zahlungsmodellkonfiguration" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="c5463-118">Der aktive Konfigurationsanbieter wird automatisch hier eingegeben.</span><span class="sxs-lookup"><span data-stu-id="c5463-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c5463-119">Dieser Anbieter ist in der Lage, diese Konfiguration verwalten.</span><span class="sxs-lookup"><span data-stu-id="c5463-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c5463-120">Andere Anbieter können diese Konfiguration verwenden, werden jedoch nicht in der Lage sein, sie zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c5463-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="c5463-121">Klicken Sie auf die Schaltfläche „Konfiguration erstellen“, um die Konfigurationserstellungsaufgabe abzuschließen</span><span class="sxs-lookup"><span data-stu-id="c5463-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="c5463-122">Datenmodell erstellen</span><span class="sxs-lookup"><span data-stu-id="c5463-122">Create a data model</span></span>
<span data-ttu-id="c5463-123">Sie erstellen ein neues Datenmodell für die ausgewählte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c5463-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="c5463-124">Diese Konfigurationsversion hat den Status "Entwurf".</span><span class="sxs-lookup"><span data-stu-id="c5463-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="c5463-125">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="c5463-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="c5463-126">Definieren der Struktur einer Partei, die an einem Zahlungsprozess teilnimmt</span><span class="sxs-lookup"><span data-stu-id="c5463-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="c5463-127">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c5463-128">Geben sie im Feld „Name” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="c5463-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-129">Click Add.</span></span>
4. <span data-ttu-id="c5463-130">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="c5463-131">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="c5463-132">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="c5463-133">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-133">Click Add.</span></span>
8. <span data-ttu-id="c5463-134">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="c5463-135">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="c5463-136">Definieren Sie die Bankstruktur für dieses Modell</span><span class="sxs-lookup"><span data-stu-id="c5463-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="c5463-137">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c5463-138">Geben Sie im Feld "Name" "Agent" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="c5463-139">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c5463-140">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-140">Click Add.</span></span>
5. <span data-ttu-id="c5463-141">Geben Sie im Feld „Beschreibung” die Bezeichnung „Finanzinstitut (z. B. eine Bank) ein, das ein Konto für die Partei (Debitor/Kreditor) verwaltet.”.</span><span class="sxs-lookup"><span data-stu-id="c5463-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="c5463-142">Finanzinstitut (z. B. eine Bank), das ein Konto für die Partei (Debitor/Kreditor) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c5463-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="c5463-143">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c5463-144">Geben Sie im Feld "Name" "Name" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="c5463-145">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c5463-146">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-146">Click Add.</span></span>
10. <span data-ttu-id="c5463-147">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="c5463-148">Geben Sie im Feld "Name" "SWIFT" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="c5463-149">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-149">Click Add.</span></span>
13. <span data-ttu-id="c5463-150">Geben Sie im Feld „Beschreibung” die Bezeichnung „Bankidentifizierungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="c5463-151">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c5463-152">Geben Sie im Feld "Name" "RoutingNumber" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="c5463-153">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-153">Click Add.</span></span>
17. <span data-ttu-id="c5463-154">Geben Sie im Feld „Beschreibung” die Bezeichnung „Routingnummer” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="c5463-155">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="c5463-156">Definieren Sie die Kontostruktur für dieses Modell</span><span class="sxs-lookup"><span data-stu-id="c5463-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="c5463-157">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c5463-158">Geben Sie im Feld "Name" "Konto" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="c5463-159">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c5463-160">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-160">Click Add.</span></span>
5. <span data-ttu-id="c5463-161">Geben Sie im Feld „Beschreibung” die Bezeichnung „Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="c5463-162">Kennung eines Kontos einer Partei in einem Finanzinstitut (beispielsweise eine Bank).</span><span class="sxs-lookup"><span data-stu-id="c5463-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="c5463-163">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c5463-164">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="c5463-165">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c5463-166">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-166">Click Add.</span></span>
10. <span data-ttu-id="c5463-167">Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="c5463-168">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c5463-169">Geben Sie im Feld "Name" "Nummer" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="c5463-170">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-170">Click Add.</span></span>
14. <span data-ttu-id="c5463-171">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c5463-172">Geben Sie im Feld "Name" "IBAN" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="c5463-173">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-173">Click Add.</span></span>
17. <span data-ttu-id="c5463-174">Geben Sie im Feld „Beschreibung” die „Internationale Bankkontonummer” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="c5463-175">Definieren der Zahlungsmeldungsstruktur für Kreditübertragungs-Zahlungstyp.</span><span class="sxs-lookup"><span data-stu-id="c5463-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="c5463-176">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c5463-177">Geben Sie im Feld „Neuer Knoten als ein Feld” die Bezeichnung „Modellwurzel” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="c5463-178">Geben Sie im Feld "Name" "CustomerCreditTransferInitiation".</span><span class="sxs-lookup"><span data-stu-id="c5463-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="c5463-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-179">Click Add.</span></span>
5. <span data-ttu-id="c5463-180">Geben Sie im Feld „Suchen” die Bezeichnung „CustomerCreditTransferInitiation” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="c5463-181">Klicken Sie auf „Vorheriges suchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-181">Click Find previous.</span></span>
7. <span data-ttu-id="c5463-182">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="c5463-183">Geben Sie im Feld "Name" 'MessageIdentification' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="c5463-184">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-184">Click Add.</span></span>
10. <span data-ttu-id="c5463-185">Geben Sie im Feld „Beschreibung” die Bezeichnung „Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen wird (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="c5463-186">Die Punkt-zu-Punkt-Referenz, die von der Anweisungspartei zugewiesen (und an die nächste Partei gesendet wird), um die Nachricht zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c5463-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="c5463-187">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c5463-188">Geben Sie im Feld "Name" 'ProcessingDateTime' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="c5463-189">Wählen Sie im Feld "Artikeltyp" 'DateTime' aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="c5463-190">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-190">Click Add.</span></span>
15. <span data-ttu-id="c5463-191">Geben Sie im Feld „Beschreibung” die Bezeichnung „Das Datum und die Uhrzeit der Erstellung der Zahlungsnachricht.” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="c5463-192">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="c5463-193">Definieren Sie die Zahlungsbuchungsstruktur für dieses Modell.</span><span class="sxs-lookup"><span data-stu-id="c5463-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="c5463-194">Geben Sie im Feld "Name" "Zahlungen" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="c5463-195">Wählen Sie im Feld "Artikeltyp" 'Datensatzliste' aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="c5463-196">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-196">Click Add.</span></span>
20. <span data-ttu-id="c5463-197">Geben Sie im Feld "Beschreibung" "Zahlungspositionen der aktuellen Nachricht" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="c5463-198">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="c5463-199">Geben Sie im Feld "Name" 'Kreditor' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="c5463-200">Wählen Sie im Feld "Artikeltyp" 'Datensatz' aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="c5463-201">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-201">Click Add.</span></span>
25. <span data-ttu-id="c5463-202">Geben Sie im Feld „Beschreibung” die „Bezeichnung Partei, für die ein Geldbetrag fällig ist” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="c5463-203">Klicken Sie auf „Artikelreferenz wechseln”.</span><span class="sxs-lookup"><span data-stu-id="c5463-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="c5463-204">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="c5463-205">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-205">Click Find next.</span></span>
29. <span data-ttu-id="c5463-206">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c5463-206">Click OK.</span></span>
30. <span data-ttu-id="c5463-207">Geben Sie im Feld „Suchen” die Bezeichnung „Zahlungen” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="c5463-208">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-208">Click Find next.</span></span>
32. <span data-ttu-id="c5463-209">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="c5463-210">Geben Sie im Feld "Name" "Zahlungspflichtiger" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="c5463-211">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-211">Click Add.</span></span>
35. <span data-ttu-id="c5463-212">Geben Sie im Feld „Beschreibung” „Partei, die dem (letztendlichen) Kreditor einen Geldbetrag schuldet.” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="c5463-213">Klicken Sie auf „Artikelreferenz wechseln”.</span><span class="sxs-lookup"><span data-stu-id="c5463-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="c5463-214">Geben sie im Feld „Suchen” das Wort „Partei” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="c5463-215">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-215">Click Find next.</span></span>
39. <span data-ttu-id="c5463-216">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c5463-216">Click OK.</span></span>
40. <span data-ttu-id="c5463-217">Klicken Sie auf „Weitersuchen”.</span><span class="sxs-lookup"><span data-stu-id="c5463-217">Click Find next.</span></span>
41. <span data-ttu-id="c5463-218">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="c5463-219">Geben Sie im Feld "Name" "Beschreibung" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="c5463-220">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="c5463-221">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-221">Click Add.</span></span>
45. <span data-ttu-id="c5463-222">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="c5463-223">Geben Sie im Feld "Name" 'Währung' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="c5463-224">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-224">Click Add.</span></span>
48. <span data-ttu-id="c5463-225">Geben Sie im Feld „Beschreibung” die Bezeichnung „Währungscode” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="c5463-226">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="c5463-227">Geben Sie im Feld "Name" 'TransactionDate' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="c5463-228">Wählen Sie im Feld "Artikeltyp" 'Datum' aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="c5463-229">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-229">Click Add.</span></span>
53. <span data-ttu-id="c5463-230">Geben Sie im Feld „Beschreibung” das „Transaktionsdatum” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="c5463-231">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="c5463-232">Geben Sie im Feld "Name" 'InstructedAmount' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="c5463-233">Wählen Sie im Feld "Artikeltyp" "Gleitkommazahl" aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="c5463-234">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-234">Click Add.</span></span>
58. <span data-ttu-id="c5463-235">Geben Sie im Feld „Beschreibung” „Der zwischen Debitor und Kreditor vor Abzug von Gebühren zu transferierende Geldbetrag, vor Abzug von Gebühren”.</span><span class="sxs-lookup"><span data-stu-id="c5463-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c5463-236">Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.'</span><span class="sxs-lookup"><span data-stu-id="c5463-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="c5463-237">Zwischen Debitor und Kreditor vor Abzug von Gebühren transferierter Geldbetrag.</span><span class="sxs-lookup"><span data-stu-id="c5463-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c5463-238">Der Betrag sollte in der Währung gezahlt werden, wie ursprünglich von der initiierenden Partei gestellt.</span><span class="sxs-lookup"><span data-stu-id="c5463-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="c5463-239">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c5463-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="c5463-240">Geben Sie im Feld "Name" 'End2EndID' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="c5463-241">Wählen Sie im Feld "Artikeltyp" "Zeichenfolge" aus.</span><span class="sxs-lookup"><span data-stu-id="c5463-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="c5463-242">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c5463-242">Click Add.</span></span>
63. <span data-ttu-id="c5463-243">Geben Sie im Feld „Beschreibung” „Die eindeutige Kennung, die von der initiierenden Partei zugewiesen wird” ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="c5463-244">Diese Kennung wird unverändert in der gesamten End-to-End-Kette übergeben' ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="c5463-245">Geben Sie im Feld "Name" "PaymentModel" ein.</span><span class="sxs-lookup"><span data-stu-id="c5463-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="c5463-246">Der PaymentModel-Name wird an vordefinierten Schnittstellen von Zahlungsformularen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="c5463-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="c5463-247">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c5463-247">Click Save.</span></span>
66. <span data-ttu-id="c5463-248">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c5463-248">Close the page.</span></span>

