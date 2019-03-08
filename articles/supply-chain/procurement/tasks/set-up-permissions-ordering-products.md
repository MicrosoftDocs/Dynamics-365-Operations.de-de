---
title: Berechtigungen zum Bestellen von Produkten im Auftrag einer anderen Person einrichten
description: Diese Prozedur zeigt, wie Arbeitskräften die Berechtigung erteilt wird, Bestellanforderungen im Auftrag anderer Arbeitskräfte vorzubereiten.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35688d191cef06cc15251a6e10a2e8c9afb0e08b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "314807"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="247e2-103">Berechtigungen zum Bestellen von Produkten im Auftrag einer anderen Person einrichten</span><span class="sxs-lookup"><span data-stu-id="247e2-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="247e2-104">Diese Prozedur zeigt, wie Arbeitskräften die Berechtigung erteilt wird, Bestellanforderungen im Auftrag anderer Arbeitskräfte vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="247e2-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="247e2-105">Das bedeutet, kann eine Bestellanforderung "Antragsteller" eine Bestellanforderung für eine andere  "anfordernden Person" erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="247e2-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="247e2-106">Die Prozedur zeigt auch, wie Arbeitsberechtigungen gewährt werden, um Artikel oder Services in unterschiedlichen juristischen Personen oder Organisationseinheiten zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="247e2-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="247e2-107">Normalerweise werden diese Aufgaben von einem Einkaufsleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="247e2-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="247e2-108">Sie können diese Prozedur entweder für Daten für das Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="247e2-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="247e2-109">Berechtigung erteilen, um Bestellanforderungen im Auftrag einer anderen Arbeitskraft einzugeben</span><span class="sxs-lookup"><span data-stu-id="247e2-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="247e2-110">Wechseln Sie zu Beschaffung > Einstellungen > Richtlinien > Bestellanforderungsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="247e2-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="247e2-111">Stellen Sie sicher, dass das Feld "Aktuelle Ansicht" auf "Durch Antragsteller" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="247e2-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="247e2-112">Die Liste im linken Bereich zeigt Personen an, denen die Berechtigung erteilt werden kann, Anforderungen im Auftrag anderer Personen vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="247e2-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="247e2-113">Wählen Sie die Person aus, die (dem Antragsteller) die Berechtigung erteilt.</span><span class="sxs-lookup"><span data-stu-id="247e2-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="247e2-114">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="247e2-114">Click Add.</span></span>
4. <span data-ttu-id="247e2-115">Suchen Sie die Person und wählen Sie sie aus, die als anfordernde Person hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="247e2-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="247e2-116">Die anfordernde Person ist die Person, in dessen Auftrag der Antragsteller Anforderungen erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="247e2-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="247e2-117">Wählen sie im Feld "Autorisierung" die Option "'Spezifisch" aus, wenn der Antragsteller in der Lage sein sollte, Bestellanforderungen im Auftrag der ausgewählten Arbeitskraft zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="247e2-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="247e2-118">Wählen Sie "Berichterstellung" aus, wenn der Antragsteller in der Lage sein soll, Bestellanforderungen im Auftrag aller Arbeitskräfte zu erstellen, die dieser Arbeitskraft unterstellt sind.</span><span class="sxs-lookup"><span data-stu-id="247e2-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="247e2-119">Geben Sie ein Datum im Feld "Gültig" ein.</span><span class="sxs-lookup"><span data-stu-id="247e2-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="247e2-120">Geben Sie im Feld "Ablauf" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="247e2-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="247e2-121">Antragsteller anzeigen, die die Berechtigung zum Erstellen von Bestellanforderungen für eine ausgewählte Arbeitskraft haben</span><span class="sxs-lookup"><span data-stu-id="247e2-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="247e2-122">Wählen Sie im Feld "Aktuelle Ansicht" die Option "Durch anfordernde Person" aus.</span><span class="sxs-lookup"><span data-stu-id="247e2-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="247e2-123">Diese Anzeige zeigt eine Liste von Antragstellern an, denen die Berechtigung zum Erstellen von Bestellanforderungen im Auftrag einer ausgewählten Arbeitskraft erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="247e2-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="247e2-124">Verwenden Sie den Schnellfilter, um die Arbeitskraft zu suchen, die Sie soeben als anfordernde Person hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="247e2-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="247e2-125">Wählen Sie die anfordernde Person aus.</span><span class="sxs-lookup"><span data-stu-id="247e2-125">Select the requester.</span></span>
    * <span data-ttu-id="247e2-126">Die Antragstellerliste zeigt die Personen an, die die Berechtigung haben, Artikel im Auftrag des Antragstellers zu bestellen, der im linken Bereich ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="247e2-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="247e2-127">Sie können zusätzliche Antragsteller hier hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="247e2-127">You can add additional preparers here.</span></span>   <span data-ttu-id="247e2-128">In dieser Ansicht können Sie der anfordernden Person auch die Berechtigung erteilen, Anforderungen in juristischen Personen und Organisationseinheiten zu erstellen, die nicht die primäre juristische Person oder Organisationseinheit dieser Person sind.</span><span class="sxs-lookup"><span data-stu-id="247e2-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

