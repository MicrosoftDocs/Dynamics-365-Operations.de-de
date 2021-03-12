---
title: Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten
description: Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976265"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="6c200-103">Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten</span><span class="sxs-lookup"><span data-stu-id="6c200-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c200-104">Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c200-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="6c200-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c200-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="6c200-106">Hauptbuchparameter</span><span class="sxs-lookup"><span data-stu-id="6c200-106">General ledger parameter</span></span>
1. <span data-ttu-id="6c200-107">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="6c200-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="6c200-108">Erweitern Sie den Abschnitt 'Bankdokument'.</span><span class="sxs-lookup"><span data-stu-id="6c200-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="6c200-109">Wählen Sie diese Option aus, um den Garantiebrief zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6c200-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="6c200-110">Klicken Sie im Feld Transaktionserfassung auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6c200-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6c200-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="6c200-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6c200-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6c200-113">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="6c200-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="6c200-114">Definieren Sie Nummernkreiscode für Garantiebriefnummer und Garantiebriefbuchungsreferenzen</span><span class="sxs-lookup"><span data-stu-id="6c200-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="6c200-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c200-115">Click Save.</span></span>
9. <span data-ttu-id="6c200-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c200-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="6c200-117">Bankfazilität erstellen</span><span class="sxs-lookup"><span data-stu-id="6c200-117">Create Bank facility</span></span>
1. <span data-ttu-id="6c200-118">Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankinstitut".</span><span class="sxs-lookup"><span data-stu-id="6c200-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="6c200-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6c200-119">Click New.</span></span>
3. <span data-ttu-id="6c200-120">Geben Sie im Feld Fazilitätsgruppe den Namen der Bankfazilitätsgruppe für die Garantiebriefbuchung ein.</span><span class="sxs-lookup"><span data-stu-id="6c200-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="6c200-121">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6c200-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6c200-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c200-122">Click Save.</span></span>
6. <span data-ttu-id="6c200-123">Klicken Sie auf die Fazilitätstypregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="6c200-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="6c200-124">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6c200-124">Click New.</span></span>
8. <span data-ttu-id="6c200-125">Geben Sie im Feld Fazilitätsgruppe den Namen des Bankfazilitätstyps, der sich auf die Bankfazilitätsvereinbarung bezieht.</span><span class="sxs-lookup"><span data-stu-id="6c200-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="6c200-126">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6c200-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="6c200-127">Klicken Sie im Feld Fazilitätsgruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6c200-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6c200-128">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6c200-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6c200-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6c200-130">Wählen Sie im Feld Fazilitätsart eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="6c200-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6c200-131">Click Save.</span></span>
15. <span data-ttu-id="6c200-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c200-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="6c200-133">Bankbuchungsprofil</span><span class="sxs-lookup"><span data-stu-id="6c200-133">Bank posting profile</span></span>
1. <span data-ttu-id="6c200-134">Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankdokumentenbuchungsprofil.</span><span class="sxs-lookup"><span data-stu-id="6c200-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="6c200-135">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6c200-135">Click New.</span></span>
3. <span data-ttu-id="6c200-136">Klicken Sie im Feld "Konto-/Gruppennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6c200-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6c200-137">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6c200-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6c200-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6c200-139">Wählen Sie im Feld Buchungskonto das Hauptkonto für den Ausgleich aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="6c200-140">Wählen Sie im Feld Gebührenkonto das Konto für Ausgabenbuchungen aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="6c200-141">Wählen Sie im Feld Einschusskonto das Konto für die Einschusstransaktion aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="6c200-142">Wählen Sie im Feld Liquidationskonto das Liquidationskonto für die Garantiebriefbuchung aus.</span><span class="sxs-lookup"><span data-stu-id="6c200-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="6c200-143">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="6c200-143">Click Save.</span></span>
11. <span data-ttu-id="6c200-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c200-144">Close the page.</span></span>

