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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff5402b11cd2ccdfde2881268d9cd936947cd77e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443641"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="f1654-103">Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten</span><span class="sxs-lookup"><span data-stu-id="f1654-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1654-104">Diese Aufgabe erstellt eine Bankfazilität und ein Buchungsprofil, das benötigt wird, um einen Garantiebrief zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f1654-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="f1654-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1654-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="f1654-106">Hauptbuchparameter</span><span class="sxs-lookup"><span data-stu-id="f1654-106">General ledger parameter</span></span>
1. <span data-ttu-id="f1654-107">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="f1654-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="f1654-108">Erweitern Sie den Abschnitt 'Bankdokument'.</span><span class="sxs-lookup"><span data-stu-id="f1654-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="f1654-109">Wählen Sie diese Option aus, um den Garantiebrief zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f1654-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="f1654-110">Klicken Sie im Feld Transaktionserfassung auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f1654-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f1654-111">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f1654-112">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f1654-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f1654-113">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="f1654-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="f1654-114">Definieren Sie Nummernkreiscode für Garantiebriefnummer und Garantiebriefbuchungsreferenzen</span><span class="sxs-lookup"><span data-stu-id="f1654-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="f1654-115">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1654-115">Click Save.</span></span>
9. <span data-ttu-id="f1654-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1654-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="f1654-117">Bankfazilität erstellen</span><span class="sxs-lookup"><span data-stu-id="f1654-117">Create Bank facility</span></span>
1. <span data-ttu-id="f1654-118">Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankinstitut".</span><span class="sxs-lookup"><span data-stu-id="f1654-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="f1654-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f1654-119">Click New.</span></span>
3. <span data-ttu-id="f1654-120">Geben Sie im Feld Fazilitätsgruppe den Namen der Bankfazilitätsgruppe für die Garantiebriefbuchung ein.</span><span class="sxs-lookup"><span data-stu-id="f1654-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="f1654-121">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f1654-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f1654-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1654-122">Click Save.</span></span>
6. <span data-ttu-id="f1654-123">Klicken Sie auf die Fazilitätstypregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="f1654-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="f1654-124">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f1654-124">Click New.</span></span>
8. <span data-ttu-id="f1654-125">Geben Sie im Feld Fazilitätsgruppe den Namen des Bankfazilitätstyps, der sich auf die Bankfazilitätsvereinbarung bezieht.</span><span class="sxs-lookup"><span data-stu-id="f1654-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="f1654-126">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f1654-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f1654-127">Klicken Sie im Feld Fazilitätsgruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f1654-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f1654-128">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f1654-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f1654-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f1654-130">Wählen Sie im Feld Fazilitätsart eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="f1654-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1654-131">Click Save.</span></span>
15. <span data-ttu-id="f1654-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1654-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="f1654-133">Bankbuchungsprofil</span><span class="sxs-lookup"><span data-stu-id="f1654-133">Bank posting profile</span></span>
1. <span data-ttu-id="f1654-134">Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankdokumentenbuchungsprofil.</span><span class="sxs-lookup"><span data-stu-id="f1654-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="f1654-135">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f1654-135">Click New.</span></span>
3. <span data-ttu-id="f1654-136">Klicken Sie im Feld "Konto-/Gruppennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f1654-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f1654-137">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f1654-138">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f1654-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f1654-139">Wählen Sie im Feld Buchungskonto das Hauptkonto für den Ausgleich aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="f1654-140">Wählen Sie im Feld Gebührenkonto das Konto für Ausgabenbuchungen aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="f1654-141">Wählen Sie im Feld Einschusskonto das Konto für die Einschusstransaktion aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="f1654-142">Wählen Sie im Feld Liquidationskonto das Liquidationskonto für die Garantiebriefbuchung aus.</span><span class="sxs-lookup"><span data-stu-id="f1654-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="f1654-143">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="f1654-143">Click Save.</span></span>
11. <span data-ttu-id="f1654-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1654-144">Close the page.</span></span>

