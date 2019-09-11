---
title: Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten
description: In diesem Verfahren erfahren Sie, wie Sie Lagerarbeiter ermöglichen alternative Lagerplätze schnell zu finden wenn kein ausreichender Bestand am Lagerort vorhanden ist.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916757"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="f590a-103">Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten</span><span class="sxs-lookup"><span data-stu-id="f590a-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f590a-104">In diesem Verfahren erfahren Sie, wie Sie Lagerarbeiter ermöglichen alternative Lagerplätze schnell zu finden wenn kein ausreichender Bestand am Lagerort vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f590a-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="f590a-105">Es ist möglich einen automatischen Neuzuordnungsprozess zu verwenden, der Lagerplatzrichtlinien verwendet, um Waren zu erhalten, wenn sie an einem anderen Standort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f590a-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="f590a-106">Alternativ wird bei der manuellen Neuzuordnung eine Liste der Lagerplätze mit der verfügbaren Menge im mobilen Gerät angezeigt und ermöglicht dem Lagerarbeiter auszuwählen welcher Lagerplatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f590a-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="f590a-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="f590a-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="f590a-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="f590a-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="f590a-109">Arbeitsausnahmen einrichten</span><span class="sxs-lookup"><span data-stu-id="f590a-109">Set up work exceptions</span></span>
1. <span data-ttu-id="f590a-110">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Lagerverwaltung > Einrichtung > Arbeit > Arbeitsausnahmen**.</span><span class="sxs-lookup"><span data-stu-id="f590a-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="f590a-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f590a-111">Click **New**.</span></span> <span data-ttu-id="f590a-112">Es ist möglich, dass mehrere Arbeitsausnahmen mit unterschiedlichen Artikelneuzuordnungsrichtlinien zu definieren, um den Lagerarbeitern die Auswahl basierend auf den Anforderungen der Lieferung zu ermöglichen, die diese verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f590a-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="f590a-113">Geben Sie im Feld **Arbeitsausnahmencode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f590a-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="f590a-114">Geben Sie der Arbeitsausnahme einen Titel, um anzugeben, für was sie verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f590a-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="f590a-115">Beispiel: "Manuelle Entnahme".</span><span class="sxs-lookup"><span data-stu-id="f590a-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="f590a-116">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f590a-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f590a-117">Wählen Sie im Feld **Ausnahme** Typ die Option'Kurze Auswahl'.</span><span class="sxs-lookup"><span data-stu-id="f590a-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="f590a-118">Aktivieren Sie das Kontrollkästchen **Bestand anpassen**.</span><span class="sxs-lookup"><span data-stu-id="f590a-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="f590a-119">Diese Option bedeutet, dass der Lagerbestand am Entnahmelagerplatz automatisch auf 0 angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="f590a-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="f590a-120">Geben Sie im Feld **Standard-Einstellungsart Code** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f590a-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="f590a-121">In USMF können Sie beispielsweise 'Remove Res Adj Out' auswählen.</span><span class="sxs-lookup"><span data-stu-id="f590a-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="f590a-122">Wählen Sie im Feld **Einzelteilumverteilung** die Option 'Manuell'.</span><span class="sxs-lookup"><span data-stu-id="f590a-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="f590a-123">Wenn Sie "Manuell" oder "Automatisch und manuell" auswählen, muss der Lagerarbeiter für die manuelle Neuzuordnung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="f590a-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="f590a-124">Eine Arbeitskraft für die manuell Artikelneuzuordnung einrichten</span><span class="sxs-lookup"><span data-stu-id="f590a-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="f590a-125">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f590a-125">Close the page.</span></span>
2. <span data-ttu-id="f590a-126">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Lagerverwaltung > Einrichtung > Arbeiter**.</span><span class="sxs-lookup"><span data-stu-id="f590a-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="f590a-127">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="f590a-127">Click **Edit**.</span></span>
4. <span data-ttu-id="f590a-128">Wählen Sie in der Liste Arbeitskraft 24 aus.</span><span class="sxs-lookup"><span data-stu-id="f590a-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="f590a-129">Erweitern Sie die **Arbeit** fastTab.</span><span class="sxs-lookup"><span data-stu-id="f590a-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="f590a-130">Wählen Sie im Feld **Manuelle Positionsumverteilung erlauben** Ja.</span><span class="sxs-lookup"><span data-stu-id="f590a-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

