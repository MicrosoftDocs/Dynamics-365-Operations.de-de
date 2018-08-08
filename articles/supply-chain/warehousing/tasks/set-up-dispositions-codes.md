--- 
title: Dispositionscodes einrichten
description: "Fokusse dieser Prozedur auf den Einstellungen eines Dispositionscodes, der mit einem mobilen Gerät für die Rücklieferung verwendet werden kann, die Prozess erhält."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="79450-103">Dispositionscodes einrichten</span><span class="sxs-lookup"><span data-stu-id="79450-103">Set up dispositions codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79450-104">Fokusse dieser Prozedur auf den Einstellungen eines Dispositionscodes, der mit einem mobilen Gerät für die Rücklieferung verwendet werden kann, die Prozess erhält.</span><span class="sxs-lookup"><span data-stu-id="79450-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="79450-105">Dispositionscodes sind eine Regelsammlung, die verwendet wird, wenn Artikel eingegangen sind.</span><span class="sxs-lookup"><span data-stu-id="79450-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="79450-106">Wird beispielsweise ein Arbeitsbenutzer ein mobiles Gerät verwendet, um Artikel zu erhalten, die beschädigt wurden, muss der Benutzer einen Dispositionscode für beschädigte Artikel scannen.</span><span class="sxs-lookup"><span data-stu-id="79450-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="79450-107">Der Bestandsstatus der Wareneingänge verschaffen, der Arbeitsvorlage und der Lagerplatzdirektive kann über gescannten Dispositionscode bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="79450-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="79450-108">Für die Bestellung, die Prozess und den Produktionsauftragsbericht als um Prozess erhält, ist der Verwendung von einem Dispositionscode optional.</span><span class="sxs-lookup"><span data-stu-id="79450-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="79450-109">Für den empfangenden Rückholprozess des Auftrags wenn die Artikel mithilfe eines mobilen Geräts erfasst werden, ist der Verwendung von Dispositionscode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="79450-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="79450-110">Dieses Handbuch wurde mit dem Demodatenunternehmen USMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="79450-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="79450-111">Diese Prozedur ist für die Lagerverwaltung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="79450-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="79450-112">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobile Geräte" > "Bereitstellungscodes".</span><span class="sxs-lookup"><span data-stu-id="79450-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="79450-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="79450-113">Click New.</span></span>
    * <span data-ttu-id="79450-114">Erstellen Sie einen neuen Dispositionscode, um für Debitorenrücklieferungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="79450-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="79450-115">Geben Sie im Feld "Bereitstellungscode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="79450-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="79450-116">Wählen Sie im Bestandsstatusgebiet wählen Sie einen Bestandsstatus aus, mit dem er Sperrung von Lagerbestand ausreicht.</span><span class="sxs-lookup"><span data-stu-id="79450-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="79450-117">Wählen Sie bei Verwendung von USMF "Sperrung" aus.</span><span class="sxs-lookup"><span data-stu-id="79450-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="79450-118">Sie können einen Bestandsstatus dem Dispositionscode hinzufügen, um den Standardstatus zu überschreiben, der in den Auftragspositionen lautet.</span><span class="sxs-lookup"><span data-stu-id="79450-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="79450-119">Geben Sie im Feld "Arbeitsvorlage" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="79450-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="79450-120">Optional: Wählen Sie einen Arbeitsvorlagencode aus, der mit einer Rücklieferung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="79450-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="79450-121">Wenn kein Wert angegeben, wird die Arbeitsvorlage mithilfe von Standardregeln aufgelöst, die in Ihrem System entsprechend konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="79450-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="79450-122">Eine Arbeitsvorlage ausgewählt, beschränkt die Prozesse ein, die dieser Dispositionscode mit verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="79450-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="79450-123">Wird beispielsweise ein Dispositionscode eine Arbeitsvorlage mit einem Arbeitsauftrag der Typ Bestellung hat, kann er nicht verwendet werden, um Artikel zu erfassen, die von Debitoren zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="79450-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="79450-124">Geben Sie im Feld "Rückgabe Bereitstellungscode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="79450-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="79450-125">Der Rückholdispositionscode bestimmt den Rest des Rücklieferungsprozesses für die erfassten Artikel.</span><span class="sxs-lookup"><span data-stu-id="79450-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="79450-126">In diesem Beispiel sollte der Debitor eine Gutschrift erhalten.</span><span class="sxs-lookup"><span data-stu-id="79450-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="79450-127">Hinzufügen eines Rückgabedispositionscode hinzu, der einen Aktivität Haben enthält.</span><span class="sxs-lookup"><span data-stu-id="79450-127">Add a returns disposition code that contains an action Credit.</span></span>  


