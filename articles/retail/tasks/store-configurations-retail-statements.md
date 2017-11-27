--- 
title: " Konfigurationen für Einzelhandelsauszüge speichern"
description: "Diese Prozedur zeigt Schritt für Schritt Konfigurationen für das Einzelhandelsgeschäft, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="d87d8-103"> Konfigurationen für Einzelhandelsauszüge speichern</span><span class="sxs-lookup"><span data-stu-id="d87d8-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d87d8-104">Diese Prozedur zeigt Schritt für Schritt Konfigurationen für das Einzelhandelsgeschäft, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="d87d8-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="d87d8-105">Finanzdimensionen in Einzelhandelsgeschäften werden in einer anderen Prozedur abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="d87d8-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="d87d8-106">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="d87d8-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d87d8-107">Navigieren Sie zu Einzelhandel und Handel > Kanäle > Einzelhandelsgeschäfte > Alle Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="d87d8-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="d87d8-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d87d8-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d87d8-109">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d87d8-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d87d8-110">Die Einstellungen im Abschnitt "Auszug/Abschluss" wirken sich auf die Auszugserstellung, -prüfung und -buchung für den Shop aus.</span><span class="sxs-lookup"><span data-stu-id="d87d8-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="d87d8-111">Öffnen Sie den Auszug/das Nachspiel.</span><span class="sxs-lookup"><span data-stu-id="d87d8-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="d87d8-112">Wählen Sie die Methode aus, die Sie verwenden möchten, um die Auszugspositionen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="d87d8-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="d87d8-113">Wählen Sie "Ja" aus, wenn nur ein Auszug pro Tag erstellt werden soll, wenn Auszüge vom Auszugserstellungsbatchauftrag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d87d8-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="d87d8-114">Das Kassensturzberechnungs-Feld definiert, ob Kassenstürze zusammen hinzugefügt werden sollen, oder ob der letzte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d87d8-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="d87d8-115">Wählen Sie das Sachkonto aus, um Rundungsdifferenzen darauf zu buchen.</span><span class="sxs-lookup"><span data-stu-id="d87d8-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="d87d8-116">Im Feld "Maximale Rundungsdifferenz" können Sie die maximal zulässige Rundungsdifferenz eingeben.</span><span class="sxs-lookup"><span data-stu-id="d87d8-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="d87d8-117">Im Buchungsfeld können Sie den maximalen gesamten Buchungsunterschied eingeben, der für einen Auszug zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="d87d8-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="d87d8-118">Im Schicht-Feld können Sie den maximalen gesamten Unterschied innerhalb einer Schicht für einen Auszug eingeben.</span><span class="sxs-lookup"><span data-stu-id="d87d8-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="d87d8-119">Im Feld "Transaktion" können Sie die maximale gesamte Differenz in einer Auszugsposition eingeben.</span><span class="sxs-lookup"><span data-stu-id="d87d8-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="d87d8-120">Im Feld "Abschlussmethode" können Sie definieren, ob Buchungen, die in einem Auszug enthalten sind, Teil einer geschlossenen Schicht sein sollen, oder ob sie beliebige Buchungen innerhalb des festgelegten Datum/Uhrzeit-Bereiches werden können.</span><span class="sxs-lookup"><span data-stu-id="d87d8-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="d87d8-121">Im Feld "Ende des Arbeitstags" können Sie eine Uhrzeit eingeben, wenn Buchungen, die nach Mitternacht auftreten, zum vorhergehenden Tag gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d87d8-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="d87d8-122">Wählen Sie "Ja" aus, wenn Buchungen, die nach Mitternacht auftreten, als Teil des vorherigen Tages gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d87d8-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="d87d8-123">Wählen Sie "Ja" aus, um Aufstellungen zu erhalten, die für jede definierte Auszugsmethode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d87d8-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="d87d8-124">Dies kann hilfreich sein, wenn die Leistung der Buchung für Shops mit hohem Buchungsvolumen verbessert werden muss, da viele kleinere Auszüge erstellt werden, die parallel verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="d87d8-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="d87d8-125">Im Feld "Standarddebitor" können Sie das Debitorenkonto auswählen, um es für Verkäufe an Laufkundschaft zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d87d8-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


