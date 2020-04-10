---
title: " Konfigurationen für Einzelhandelsauszüge speichern"
description: Diese Prozedur zeigt Schritt für Schritt Konfigurationen für den Shop, die sich darauf auswirken, wie Commerce-Auszüge erstellt und gebucht werden.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140654"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="baee8-103"> Konfigurationen für Einzelhandelsauszüge speichern</span><span class="sxs-lookup"><span data-stu-id="baee8-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="baee8-104">Diese Prozedur zeigt Schritt für Schritt Konfigurationen für den Shop, die sich darauf auswirken, wie Commerce-Auszüge erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="baee8-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="baee8-105">Finanzdimensionen in Shops werden durch eine andere Prozedur abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="baee8-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="baee8-106">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="baee8-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="baee8-107">Gehen Sie im **Navigationsbereich** zu **Module > Retail und Commerce > Kanäle > Shops > Alle Shops**.</span><span class="sxs-lookup"><span data-stu-id="baee8-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="baee8-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="baee8-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="baee8-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="baee8-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="baee8-110">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="baee8-110">Click **Edit**.</span></span>
5. <span data-ttu-id="baee8-111">Die Einstellungen in der **Auszug/Schließen** fastTab wirken sich auf die Erstellung, Validierung und Buchung von Auszügen für die Filiale aus.</span><span class="sxs-lookup"><span data-stu-id="baee8-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="baee8-112">Erweitern Sie die **Auszug/Schließen** fastTab.</span><span class="sxs-lookup"><span data-stu-id="baee8-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="baee8-113">Wählen Sie im Feld **Auszugsmethode** die Methode aus, mit der Sie die Auszugszeilen gruppieren möchten.</span><span class="sxs-lookup"><span data-stu-id="baee8-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="baee8-114">Wählen Sie „Ja“ unter **Ein Auszug pro Tag**, wenn bei der Erstellung von Auszügen aus dem Batch-Job der Auszugserstellung nur ein Auszug pro Tag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="baee8-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="baee8-115">Das Feld **Kassensturzberechnung** definiert, ob Kassensturzberechnungen addiert werden sollen oder ob die letzte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="baee8-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="baee8-116">Wählen Sie im Feld **Rundung** das Sachkonto aus, in das Rundungsdifferenzen gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="baee8-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="baee8-117">Geben Sie im Feld **Maximale Rundungsdifferenz** die maximal zulässige Rundungsdifferenz ein.</span><span class="sxs-lookup"><span data-stu-id="baee8-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="baee8-118">Geben Sie im Feld **Buchung** die maximal zulässige Gesamtbuchungsdifferenz für einen Auszug ein.</span><span class="sxs-lookup"><span data-stu-id="baee8-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="baee8-119">Geben Sie im Feld **Shift** die maximale Gesamtdifferenz innerhalb einer Schicht in einen Auszug ein.</span><span class="sxs-lookup"><span data-stu-id="baee8-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="baee8-120">Geben Sie in das Feld **Transaktion** die maximale Gesamtdifferenz in einer Auszugszeile ein.</span><span class="sxs-lookup"><span data-stu-id="baee8-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="baee8-121">Definieren Sie im Feld **Schließmethode**, ob Transaktionen, die in einen Auszug aufgenommen werden, Teil einer geschlossenen Schicht sein sollen oder ob es sich um Transaktionen innerhalb des definierten Datums-/Zeitbereichs handeln kann.</span><span class="sxs-lookup"><span data-stu-id="baee8-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="baee8-122">Geben Sie im Feld **Ende des Geschäftstages** eine Uhrzeit ein, wenn Transaktionen, die nach Mitternacht stattfinden, mit dem Vortag gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="baee8-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="baee8-123">Wählen Sie „Ja“ unter **Als Geschäftstag buchen**, wenn Transaktionen, die nach Mitternacht stattfinden, als Teil des Vortages gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="baee8-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="baee8-124">Wählen Sie „Ja“ unter **Nach Auszugsmethode aufteilen**, um Auszüge für jede definierte Auszugsmethode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="baee8-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="baee8-125">Dies kann hilfreich sein, wenn die Leistung der Buchung für Shops mit hohem Buchungsvolumen verbessert werden muss, da viele kleinere Auszüge erstellt werden, die parallel verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="baee8-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="baee8-126">Im Feld **Allgemein** fastTab, im Feld **Standardkunde** können Sie das Kundenkonto auswählen, das für den Verkauf an Laufkundschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="baee8-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

