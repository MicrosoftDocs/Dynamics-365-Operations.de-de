---
title: Konfigurationen für Einzelhandelsauszüge speichern
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af4321cd9d6e15c82c4eef1f1ca218b8301ebf35
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003652"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="52a1d-103">Konfigurationen für Einzelhandelsauszüge speichern</span><span class="sxs-lookup"><span data-stu-id="52a1d-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52a1d-104">Diese Prozedur zeigt Schritt für Schritt Konfigurationen für den Shop, die sich darauf auswirken, wie Commerce-Auszüge erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="52a1d-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="52a1d-105">Finanzdimensionen in Shops werden durch eine andere Prozedur abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="52a1d-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="52a1d-106">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="52a1d-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="52a1d-107">Gehen Sie im **Navigationsbereich** zu **Module > Einzelhandel und Handel > Kanäle > Geschäfte > Alle Geschäfte**.</span><span class="sxs-lookup"><span data-stu-id="52a1d-107">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="52a1d-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="52a1d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="52a1d-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="52a1d-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="52a1d-110">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="52a1d-110">Click **Edit**.</span></span>
5. <span data-ttu-id="52a1d-111">Die Einstellungen in der Registerkarte **Anweisung/Abschluss** wirken sich auf die Erstellung, Validierung und Buchung von Auszügen für die Filiale aus.</span><span class="sxs-lookup"><span data-stu-id="52a1d-111">The settings in the **Statement/closing** FastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="52a1d-112">Erweitern Sie die Registerkarte **Anweisung/Abschluss**.</span><span class="sxs-lookup"><span data-stu-id="52a1d-112">Expand the **Statement/closing** FastTab.</span></span>  
6. <span data-ttu-id="52a1d-113">Wählen Sie im Feld **Anweisgungsmethode** die Methode aus, mit der Sie die Anweisungszeilen gruppieren möchten.</span><span class="sxs-lookup"><span data-stu-id="52a1d-113">In the **Statement method** field, select the method you want to use to group the statement lines by.</span></span>  
7. <span data-ttu-id="52a1d-114">Wählen Sie „Ja“ unter **Ein Auszug pro Tag**, wenn bei der Erstellung von Auszügen aus dem Batch-Job der Auszugserstellung nur ein Auszug pro Tag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a1d-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="52a1d-115">Das Feld **Kassensturzberechnung** definiert, ob Kassensturzberechnungen addiert werden sollen oder ob die letzte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a1d-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="52a1d-116">Wählen Sie im Feld **Rundung** das Sachkonto aus, in das Rundungsdifferenzen gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52a1d-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="52a1d-117">Geben Sie im Feld **Maximale Rundungsdifferenz** die maximal zulässige Rundungsdifferenz ein.</span><span class="sxs-lookup"><span data-stu-id="52a1d-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="52a1d-118">Geben Sie im Feld **Buchung** die maximal zulässige Gesamtbuchungsdifferenz für einen Auszug ein.</span><span class="sxs-lookup"><span data-stu-id="52a1d-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="52a1d-119">Geben Sie im Feld **Shift** die maximale Gesamtdifferenz innerhalb einer Schicht in einen Auszug ein.</span><span class="sxs-lookup"><span data-stu-id="52a1d-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="52a1d-120">Geben Sie in das Feld **Transaktion** die maximale Gesamtdifferenz in einer Auszugszeile ein.</span><span class="sxs-lookup"><span data-stu-id="52a1d-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="52a1d-121">Definieren Sie im Feld **Schließmethode**, ob Transaktionen, die in einen Auszug aufgenommen werden, Teil einer geschlossenen Schicht sein sollen oder ob es sich um Transaktionen innerhalb des definierten Datums-/Zeitbereichs handeln kann.</span><span class="sxs-lookup"><span data-stu-id="52a1d-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="52a1d-122">Geben Sie im Feld **Ende des Geschäftstages** eine Uhrzeit ein, wenn Transaktionen, die nach Mitternacht stattfinden, mit dem Vortag gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52a1d-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="52a1d-123">Wählen Sie „Ja“ unter **Als Geschäftstag buchen**, wenn Transaktionen, die nach Mitternacht stattfinden, als Teil des Vortages gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52a1d-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="52a1d-124">Wählen Sie „Ja“ unter **Nach Auszugsmethode aufteilen**, um Auszüge für jede definierte Auszugsmethode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="52a1d-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="52a1d-125">Diese Aktion kann hilfreich sein, wenn die Leistung der Buchung für Shops mit hohem Buchungsvolumen verbessert werden muss, da viele kleinere Auszüge erstellt werden, die parallel verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="52a1d-125">This action can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="52a1d-126">In der Registerkarte **Allgemein** im Feld **Standardkunde** können Sie das Kundenkonto auswählen, das für den Verkauf an Laufkundschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a1d-126">In the **General** FastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

