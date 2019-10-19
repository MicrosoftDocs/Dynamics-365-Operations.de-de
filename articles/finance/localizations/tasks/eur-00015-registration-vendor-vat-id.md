---
title: EUR-00015 Registrierung der Kreditor-MwSt.-Kennung
description: Dieses Verfahren zeigt, wie Sie MwSt. -Erfassungkennungen und einer Steuerbefreiungsnummer zu einem Kreditorenkonto hinzufügen.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68475c96e7c85cc5a4c540441a4b1f3752ecf0bd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175103"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="b18fa-103">EUR-00015 Registrierung der Kreditor-MwSt.-Kennung</span><span class="sxs-lookup"><span data-stu-id="b18fa-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b18fa-104">Dieses Verfahren zeigt, wie Sie MwSt. -Erfassungkennungen und einer Steuerbefreiungsnummer zu einem Kreditorenkonto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b18fa-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="b18fa-105">Dieser Vorgang ist nur für juristische Personen und Debitoren identisch.</span><span class="sxs-lookup"><span data-stu-id="b18fa-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="b18fa-106">Vor der Ausführung dieses Schritts müssen Sie MwSt.-IDs einrichten.</span><span class="sxs-lookup"><span data-stu-id="b18fa-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="b18fa-107">Diese Prozedur gilt für alle europäischen Länder/Regionen.</span><span class="sxs-lookup"><span data-stu-id="b18fa-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="b18fa-108">Diese Prozedur wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Deutschland erstellt.</span><span class="sxs-lookup"><span data-stu-id="b18fa-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="b18fa-109">Diese Vorgehensweise ist für einen Datenverwaltungsadministrator, Kreditor-Manager oder einen Debitor-Manager vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b18fa-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="b18fa-110">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b18fa-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="b18fa-111">Gehen Sie zu "Kreditoren" > "Händler" > "Alle Händler".</span><span class="sxs-lookup"><span data-stu-id="b18fa-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="b18fa-112">Wählen Sie in der Liste den Kreditor US-01001 aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="b18fa-113">Klicken Sie auf Registrierungskennungen</span><span class="sxs-lookup"><span data-stu-id="b18fa-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="b18fa-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b18fa-114">Click Add.</span></span>
5. <span data-ttu-id="b18fa-115">Wählen Sie "MwSt.-ID" aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-115">Select VAT ID.</span></span>
6. <span data-ttu-id="b18fa-116">Geben Sie im Feld "Registrierungsnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b18fa-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="b18fa-117">Geben Sie eine Mehrwertsteuernummer in Deutschland für den ausgewählten Kreditor an.</span><span class="sxs-lookup"><span data-stu-id="b18fa-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="b18fa-118">Die Kennung muss mit dem angegebenen Format des Erfassungstyps übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b18fa-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="b18fa-119">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="b18fa-119">Click the General tab.</span></span>
8. <span data-ttu-id="b18fa-120">Geben Sie ein Datum im Feld "Gültig" ein.</span><span class="sxs-lookup"><span data-stu-id="b18fa-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="b18fa-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b18fa-121">Click Save.</span></span>
10. <span data-ttu-id="b18fa-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b18fa-122">Click New.</span></span>
11. <span data-ttu-id="b18fa-123">Geben Sie im Feld "Name oder Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b18fa-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="b18fa-124">Geben Sie beispielsweise "ITA" ein.</span><span class="sxs-lookup"><span data-stu-id="b18fa-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="b18fa-125">Wählen Sie im Feld Name/Region einen Wert aus oder geben Sie ihn ein«».</span><span class="sxs-lookup"><span data-stu-id="b18fa-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="b18fa-126">Wählen Sie z. B. ITA aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="b18fa-127">Wählen Sie "Ja" im Feld "Primär für Land".</span><span class="sxs-lookup"><span data-stu-id="b18fa-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="b18fa-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b18fa-128">Click Save.</span></span>
15. <span data-ttu-id="b18fa-129">Klicken Sie auf die Registerkarte "Überblick".</span><span class="sxs-lookup"><span data-stu-id="b18fa-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="b18fa-130">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b18fa-130">Click Add.</span></span>
17. <span data-ttu-id="b18fa-131">Geben Sie im Feld "Registrierungstyp" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="b18fa-132">Wählen Sie z. B. "MwSt.-ID" aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="b18fa-133">Geben Sie im Feld "Registrierungsnummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b18fa-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="b18fa-134">Geben Sie z. B. eine italienische MwSt. -ID ein.</span><span class="sxs-lookup"><span data-stu-id="b18fa-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="b18fa-135">Die Kennung muss das gleiche Format wie der Erfassungstyp haben.</span><span class="sxs-lookup"><span data-stu-id="b18fa-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="b18fa-136">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b18fa-136">Click Save.</span></span>
20. <span data-ttu-id="b18fa-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b18fa-137">Close the page.</span></span>
21. <span data-ttu-id="b18fa-138">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b18fa-139">Wählen Sie z. B. DE-01001 aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="b18fa-140">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b18fa-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="b18fa-141">Erweitern Sie den Rechnungs- und Lieferungsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="b18fa-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="b18fa-142">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b18fa-142">Click Edit.</span></span>
25. <span data-ttu-id="b18fa-143">Geben Sie im Feld "Umsatzsteuernummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="b18fa-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="b18fa-144">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b18fa-144">Click Save.</span></span>

