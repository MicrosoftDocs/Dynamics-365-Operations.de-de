---
title: Abschreibungsbücher einrichten
description: Bei diesem Verfahren wird ein neues Abschreibungsbuch erstellt und einer Anlagegruppe zugeordnet.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd65cb77872b3e2f74402cf8c92c8b8989cea6ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224692"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="74eea-103">Abschreibungsbücher einrichten</span><span class="sxs-lookup"><span data-stu-id="74eea-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74eea-104">Bei diesem Verfahren wird ein neues Abschreibungsbuch erstellt und einer Anlagegruppe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="74eea-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="74eea-105">Ein Abschreibungsbuch erstellen</span><span class="sxs-lookup"><span data-stu-id="74eea-105">Create a depreciation book</span></span>
1. <span data-ttu-id="74eea-106">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Abschreibungsbücher".</span><span class="sxs-lookup"><span data-stu-id="74eea-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="74eea-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="74eea-107">Click New.</span></span>
3. <span data-ttu-id="74eea-108">Geben Sie im Feld "Abschreibungsbuch" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="74eea-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="74eea-109">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="74eea-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="74eea-110">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibung berechnen".</span><span class="sxs-lookup"><span data-stu-id="74eea-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="74eea-111">Klicken Sie im Feld "Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="74eea-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="74eea-112">Suchen Sie in der Liste das gewünschte Abschreibungsprofil und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="74eea-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="74eea-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="74eea-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="74eea-114">Klicken Sie im Feld "Alternatives Abschreibungsprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="74eea-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="74eea-115">Wählen Sie in der Liste das gewünschte Abschreibungsprofil aus.</span><span class="sxs-lookup"><span data-stu-id="74eea-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="74eea-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="74eea-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="74eea-117">Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet.</span><span class="sxs-lookup"><span data-stu-id="74eea-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="74eea-118">Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="74eea-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="74eea-119">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Abschreibungsregulierungen mit Basisregulierungen erstellen".</span><span class="sxs-lookup"><span data-stu-id="74eea-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="74eea-120">Klicken Sie im Feld "Kalender" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="74eea-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="74eea-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="74eea-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="74eea-122">Das Abschreibungsbuch einer Anlagengruppe zuordnen</span><span class="sxs-lookup"><span data-stu-id="74eea-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="74eea-123">Klicken Sie auf "Anlagengruppen".</span><span class="sxs-lookup"><span data-stu-id="74eea-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="74eea-124">Klicken Sie im Feld "Anlagengruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="74eea-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="74eea-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="74eea-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="74eea-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="74eea-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="74eea-127">Wählen Sie im Feld "Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="74eea-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="74eea-128">Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="74eea-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="74eea-129">Beachten Sie, dass der Feldwert "Abschreibungszeiträume" nach der Festlegung der "Nutzungsdauer" berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="74eea-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]