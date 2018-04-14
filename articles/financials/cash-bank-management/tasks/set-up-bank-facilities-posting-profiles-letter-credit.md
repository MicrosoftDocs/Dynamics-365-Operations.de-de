--- 
title: "Bankfazilitäten und Buchungsprofile für Akkreditiv einrichten"
description: "Gänge dieser Prozedur mithilfe einer Bankfazilität und Buchungsprofilen erforderlich, Kreditbrief zu verarbeiten."
author: kweekley
manager: AnnBe
ms.date: 10/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e2d80ce02f45260aa364db68692ee19d813ade54
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="65951-103">Bankfazilitäten und Buchungsprofile für Akkreditiv einrichten</span><span class="sxs-lookup"><span data-stu-id="65951-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65951-104">Gänge dieser Prozedur mithilfe einer Bankfazilität und Buchungsprofilen erforderlich, Kreditbrief zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="65951-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="65951-105">Für diese Aufgabe wird das Demo-Unternehmen "USMF" verwendet.</span><span class="sxs-lookup"><span data-stu-id="65951-105">This task uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="65951-106">Hauptbuchparameter</span><span class="sxs-lookup"><span data-stu-id="65951-106">General ledger parameter</span></span>
1. <span data-ttu-id="65951-107">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="65951-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="65951-108">Erweitern Sie den Abschnitt 'Bankdokument'.</span><span class="sxs-lookup"><span data-stu-id="65951-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="65951-109">Wählen Sie diese Option aus, um den Importkreditbrief zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="65951-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="65951-110">Wählen Sie diese Option aus, um den Exportkreditbrief zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="65951-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="65951-111">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65951-111">Click Save.</span></span>
6. <span data-ttu-id="65951-112">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65951-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="65951-113">Bankfazilität erstellen</span><span class="sxs-lookup"><span data-stu-id="65951-113">Create Bank facility</span></span>
1. <span data-ttu-id="65951-114">Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankinstitut".</span><span class="sxs-lookup"><span data-stu-id="65951-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="65951-115">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="65951-115">Click New.</span></span>
3. <span data-ttu-id="65951-116">Geben Sie im Feld Fazilitätsgruppe den Namen der Bankfazilitätsgruppe ein.</span><span class="sxs-lookup"><span data-stu-id="65951-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="65951-117">Geben Sie im Feld Beschreibung die Beschreibung der Bankfazilitätsgruppe ein.</span><span class="sxs-lookup"><span data-stu-id="65951-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="65951-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65951-118">Click Save.</span></span>
6. <span data-ttu-id="65951-119">Klicken Sie auf die Fazilitätstypregisterkarte.</span><span class="sxs-lookup"><span data-stu-id="65951-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="65951-120">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="65951-120">Click New.</span></span>
8. <span data-ttu-id="65951-121">Geben Sie im Feld Fazilitätsgruppe einen eindeutigen Code ein.</span><span class="sxs-lookup"><span data-stu-id="65951-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="65951-122">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="65951-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="65951-123">Klicken Sie im Feld Fazilitätsgruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65951-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="65951-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="65951-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="65951-125">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="65951-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="65951-126">Wählen Sie im Feld Fazilitätstyp die Art der Bankfazilität aus</span><span class="sxs-lookup"><span data-stu-id="65951-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="65951-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65951-127">Click Save.</span></span>
15. <span data-ttu-id="65951-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="65951-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="65951-129">Bankbuchungsprofil</span><span class="sxs-lookup"><span data-stu-id="65951-129">Bank posting profile</span></span>
1. <span data-ttu-id="65951-130">Gehen Sie zu Kasse und Bankverwaltung > Einstellungen > Bankdokumentenbuchungsprofil.</span><span class="sxs-lookup"><span data-stu-id="65951-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="65951-131">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="65951-131">Click New.</span></span>
3. <span data-ttu-id="65951-132">Klicken Sie im Feld "Konto-/Gruppennummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65951-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="65951-133">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="65951-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="65951-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="65951-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="65951-135">Kategorie für den Ausgleich auswählen.</span><span class="sxs-lookup"><span data-stu-id="65951-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="65951-136">Dieses Konto wird bei der Berechnung der Cashflow-Planung verwendet.</span><span class="sxs-lookup"><span data-stu-id="65951-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="65951-137">Wählen Sie im Feld Gebührenkonto das Konto für Ausgabenbuchungen aus.</span><span class="sxs-lookup"><span data-stu-id="65951-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="65951-138">Wählen Sie im Feld Einschusskonto das Konto für Einschussbuchungen aus.</span><span class="sxs-lookup"><span data-stu-id="65951-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="65951-139">Dieses Konto wird bei der Buchung der Eröffnungsmarge belastet und bei der Buchung der Zahlung entlastet.</span><span class="sxs-lookup"><span data-stu-id="65951-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="65951-140">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="65951-140">Click Save.</span></span>


