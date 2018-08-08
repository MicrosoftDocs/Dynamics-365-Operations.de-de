--- 
title: "Abschreibungsbücher einrichten "
description: Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c4660cd31ef0cd80a2f73eeeb01523e34510ca38
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="set-up-depreciation-books"></a><span data-ttu-id="0b39b-103">Abschreibungsbücher einrichten </span><span class="sxs-lookup"><span data-stu-id="0b39b-103">Set up depreciation books</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b39b-104">Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="0b39b-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="0b39b-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b39b-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="0b39b-106">Ein Abschreibungsbuch erstellen</span><span class="sxs-lookup"><span data-stu-id="0b39b-106">Create a depreciation book</span></span>
1. <span data-ttu-id="0b39b-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Abschreibungsbücher".</span><span class="sxs-lookup"><span data-stu-id="0b39b-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="0b39b-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0b39b-108">Click New.</span></span>
3. <span data-ttu-id="0b39b-109">Geben Sie im Feld "Abschreibungsbuch" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0b39b-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="0b39b-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0b39b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b39b-111">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibung berechnen".</span><span class="sxs-lookup"><span data-stu-id="0b39b-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="0b39b-112">Klicken Sie im Feld "Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0b39b-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0b39b-113">Suchen Sie in der Liste das gewünschte Abschreibungsprofil und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="0b39b-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="0b39b-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b39b-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0b39b-115">Klicken Sie im Feld "Alternatives Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0b39b-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0b39b-116">Wählen Sie in der Liste das gewünschte Abschreibungsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="0b39b-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="0b39b-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b39b-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0b39b-118">Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b39b-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0b39b-119">Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="0b39b-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="0b39b-120">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibungsregulierungen mit Basisregulierungen erstellen".</span><span class="sxs-lookup"><span data-stu-id="0b39b-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="0b39b-121">Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0b39b-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0b39b-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b39b-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="0b39b-123">Das Abschreibungsbuch einer Anlagengruppe zuordnen</span><span class="sxs-lookup"><span data-stu-id="0b39b-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="0b39b-124">Klicken Sie auf "Anlagengruppen".</span><span class="sxs-lookup"><span data-stu-id="0b39b-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0b39b-125">Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0b39b-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0b39b-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0b39b-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0b39b-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0b39b-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0b39b-128">Wählen Sie im Feld "Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="0b39b-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="0b39b-129">Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0b39b-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0b39b-130">Beachten Sie, dass der Feldwert "Abschreibungszeiträume" nach der Festlegung der "Nutzungsdauer" berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0b39b-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


