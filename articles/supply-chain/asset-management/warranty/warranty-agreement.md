---
title: Garantievereinbarungen
description: In diesem Abschnitt werden die Garantievereinbarungen im Anlagenmanagement erläutert.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 35b5c89751d17687bd7e306094a1e4e5e144a8dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245346"
---
# <a name="warranty-agreements"></a><span data-ttu-id="e43bf-103">Garantievereinbarungen</span><span class="sxs-lookup"><span data-stu-id="e43bf-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e43bf-104">Im Anlagenmanagement können Sie Garantiebedingungen einrichten, die mit einer Anlage oder einer Anlagenart verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="e43bf-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="e43bf-105">Garantiebedingungen werden für einen bestimmten Zeitraum angelegt.</span><span class="sxs-lookup"><span data-stu-id="e43bf-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="e43bf-106">Die Garantie kann so eingerichtet werden, dass sie eine vollständige oder teilweise Deckung bietet, und Sie können Bedingungen einrichten, die sich auf Stunden, Ausgaben und Artikel beziehen.</span><span class="sxs-lookup"><span data-stu-id="e43bf-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="e43bf-107">Der erste Schritt besteht darin, alle Garantievereinbarungen mit Lieferanten zu erstellen, die Sie für Ihr Gerät haben.</span><span class="sxs-lookup"><span data-stu-id="e43bf-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="e43bf-108">Anschließend hängen Sie Garantievereinbarungen an Anlagen oder Anlagenarten an.</span><span class="sxs-lookup"><span data-stu-id="e43bf-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="e43bf-109">Gewährleistungsvereinbarungen des Lieferanten werden nur zu Informationszwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="e43bf-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="e43bf-110">Wenn die Lieferantengarantie auf eine Anlage eingerichtet ist, sehen Sie die Garantiezeit auf der Anlage.</span><span class="sxs-lookup"><span data-stu-id="e43bf-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="e43bf-111">Anlegen einer Garantievereinbarung</span><span class="sxs-lookup"><span data-stu-id="e43bf-111">Create a warranty agreement</span></span>

<span data-ttu-id="e43bf-112">Eine Garantievereinbarung kann mehrere Vertragszeilen umfassen, um die Garantie für Arbeitszeiten, Spesen und Artikel abzudecken.</span><span class="sxs-lookup"><span data-stu-id="e43bf-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="e43bf-113">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Anlagen** \> **Garantie**.</span><span class="sxs-lookup"><span data-stu-id="e43bf-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="e43bf-114">Wählen Sie **Neu**, um ein Produkt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e43bf-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="e43bf-115">Geben Sie im Feld **Garantie** eine Garantie-ID ein.</span><span class="sxs-lookup"><span data-stu-id="e43bf-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="e43bf-116">Geben Sie im Feld **Name** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="e43bf-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="e43bf-117">Im Feld **Details** FastTab zeigt das Feld **Assets** die Anzahl der aktiven Anlagen, die die Garantievereinbarung nutzen.</span><span class="sxs-lookup"><span data-stu-id="e43bf-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="e43bf-118">Im Inforegister **Garantiepositionen** führen Sie die folgenden Schritte aus, um Positionen hinzuzufügen, die in einer Garantievereinbarung enthalten sein sollten:</span><span class="sxs-lookup"><span data-stu-id="e43bf-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="e43bf-119">Wählen Sie **Zeile hinzufügen**, um der Garantie eine neue Bedingung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e43bf-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="e43bf-120">Eine fortlaufende Zeilennummer wird automatisch in das Feld **Zeile** eingetragen.</span><span class="sxs-lookup"><span data-stu-id="e43bf-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="e43bf-121">Wählen Sie im Feld **Periode** die Art der Garantiezeit aus.</span><span class="sxs-lookup"><span data-stu-id="e43bf-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="e43bf-122">Geben Sie im Feld **Intervall** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="e43bf-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="e43bf-123">Dieses Feld definiert die Anzahl der Zeiträume, für die die Garantie gültig sein soll.</span><span class="sxs-lookup"><span data-stu-id="e43bf-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="e43bf-124">Geben Sie im Feld **Prozent** den Deckungsprozentsatz für die Garantiezeile ein.</span><span class="sxs-lookup"><span data-stu-id="e43bf-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="e43bf-125">Der Prozentsatz gibt an, wie viel von Ihrem Unternehmen abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="e43bf-125">The percentage indicates how much is covered by your company.</span></span>

![Garantieseite](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]