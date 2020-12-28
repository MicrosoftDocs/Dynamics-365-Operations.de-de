---
title: Ressourcenfähigkeiten definieren
description: Ressourcenfunktionen beschreiben, was betriebliche Ressourcen ausführen können.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c07d3fe1969f3baea484991e74f668eade813d78
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428403"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="eee40-103">Ressourcenfähigkeiten definieren</span><span class="sxs-lookup"><span data-stu-id="eee40-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eee40-104">Ressourcenfunktionen beschreiben, was betriebliche Ressourcen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="eee40-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="eee40-105">Während der Planung werden die Anforderungen jedes Einzelvorgangs und Arbeitsgangs mit den Funktionen der verfügbaren Ressourcen abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="eee40-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="eee40-106">Dieses Aufgabenhandbuch unterstützt Sie dabei, eine Ressourcenfunktion zu erstellen und sie einer Ressource zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="eee40-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="eee40-107">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="eee40-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="eee40-108">Erstellen einer neuen Ressourcenfunktion</span><span class="sxs-lookup"><span data-stu-id="eee40-108">Create a resource capability</span></span>
1. <span data-ttu-id="eee40-109">Wechseln Sie zu Ressourcenfunktionen.</span><span class="sxs-lookup"><span data-stu-id="eee40-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="eee40-110">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="eee40-110">Click New.</span></span>
3. <span data-ttu-id="eee40-111">Geben Sie im Feld "Funktion" die Kennung der Ressourcenfunktion ein.</span><span class="sxs-lookup"><span data-stu-id="eee40-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="eee40-112">Für einen angegebenen Arbeitsgang verwenden Sie die Funktionskennung, um anzugeben, dass Ressourcen diese Funktion aufweisen müssen, um den Arbeitsgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eee40-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="eee40-113">Geben Sie im Feld "Beschreibung" eine Beschreibung der Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="eee40-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="eee40-114">Einer Ressource eine Funktion zuweisen</span><span class="sxs-lookup"><span data-stu-id="eee40-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="eee40-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="eee40-115">Click Add.</span></span>
2. <span data-ttu-id="eee40-116">Geben Sie im Feld "Ressource" die Kennung der Ressource ein.</span><span class="sxs-lookup"><span data-stu-id="eee40-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="eee40-117">Eine Ressourcenfunktion kann einer oder mehreren Ressourcen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="eee40-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="eee40-118">Geben Sie im Feld "Ablauf" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="eee40-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="eee40-119">Sie können dieses Feld verwenden, um anzugeben, dass eine Ressource nur während einer begrenzten Zeit die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="eee40-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="eee40-120">Geben Sie im Feld "Priorität" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="eee40-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="eee40-121">Wenn Sie Einzelvorgänge und Arbeitsgänge planen, können Sie angeben, ob Ressourcen nach Priorität ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="eee40-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="eee40-122">Wenn Sie diese Wahl treffen und mehr als eine Ressource den Einzelvorgang oder den Arbeitsgang bis zum angeforderten Datum ausführen kann, wird die Ressource ausgewählt, die die niedrigste Priorität hinsichtlich der erforderlichen Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="eee40-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="eee40-123">Geben Sie im Feld "Ebene" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="eee40-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="eee40-124">Wenn Sie angeben, dass ein Einzelvorgang oder ein Arbeitsgang eine bestimmte Funktion erfordert, können Sie auch die Mindestanforderung angeben, die erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="eee40-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="eee40-125">Verwenden Sie die Funktionsebene, um Ressourcen zu unterscheiden, die den gleichen Einzelvorgang ausführen können, aber mit verschiedenen Geschwindigkeiten, Stärken, Größen, usw.</span><span class="sxs-lookup"><span data-stu-id="eee40-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

