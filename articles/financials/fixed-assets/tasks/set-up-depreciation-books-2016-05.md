---
title: Einrichten von Anlagenabschreibungsbüchern (Mai 2016)
description: Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566914"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="dcf99-103">Einrichten von Anlagenabschreibungsbüchern (Mai 2016)</span><span class="sxs-lookup"><span data-stu-id="dcf99-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dcf99-104">Diese Aufgabenanleitung erstellt ein neues Abschreibungsbuch und ordnet es einer Anlagengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="dcf99-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="dcf99-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcf99-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="dcf99-106">Ein Abschreibungsbuch erstellen</span><span class="sxs-lookup"><span data-stu-id="dcf99-106">Create a depreciation book</span></span>
1. <span data-ttu-id="dcf99-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Abschreibungsbücher".</span><span class="sxs-lookup"><span data-stu-id="dcf99-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="dcf99-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="dcf99-108">Click New.</span></span>
3. <span data-ttu-id="dcf99-109">Geben Sie im Feld "Abschreibungsbuch" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dcf99-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="dcf99-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dcf99-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dcf99-111">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibung berechnen".</span><span class="sxs-lookup"><span data-stu-id="dcf99-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="dcf99-112">Klicken Sie im Feld "Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf99-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dcf99-113">Suchen Sie in der Liste das gewünschte Abschreibungsprofil und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="dcf99-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="dcf99-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf99-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dcf99-115">Klicken Sie im Feld "Alternatives Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf99-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dcf99-116">Wählen Sie in der Liste das gewünschte Abschreibungsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="dcf99-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="dcf99-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf99-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dcf99-118">Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcf99-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="dcf99-119">Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="dcf99-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="dcf99-120">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibungsregulierungen mit Basisregulierungen erstellen".</span><span class="sxs-lookup"><span data-stu-id="dcf99-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="dcf99-121">Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf99-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dcf99-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf99-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="dcf99-123">Das Abschreibungsbuch einer Anlagengruppe zuordnen</span><span class="sxs-lookup"><span data-stu-id="dcf99-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="dcf99-124">Klicken Sie auf "Anlagengruppen".</span><span class="sxs-lookup"><span data-stu-id="dcf99-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="dcf99-125">Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf99-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="dcf99-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dcf99-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="dcf99-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf99-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dcf99-128">Wählen Sie im Feld "Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="dcf99-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="dcf99-129">Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="dcf99-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="dcf99-130">Beachten Sie, dass der Feldwert "Abschreibungszeiträume" nach der Festlegung der "Nutzungsdauer" berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="dcf99-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

