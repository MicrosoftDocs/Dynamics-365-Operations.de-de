---
title: Garantievereinbarungen
description: In diesem Abschnitt werden die Garantievereinbarungen im Anlagenmanagement erläutert.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e9cbb9068101f3004179f338da18af0369190807
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215377"
---
# <a name="warranty-agreements"></a><span data-ttu-id="ecc69-103">Garantievereinbarungen</span><span class="sxs-lookup"><span data-stu-id="ecc69-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="ecc69-104">Im Anlagenmanagement können Sie Garantiebedingungen einrichten, die mit einer Anlage oder einer Anlagenart verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="ecc69-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="ecc69-105">Garantiebedingungen werden für einen bestimmten Zeitraum angelegt.</span><span class="sxs-lookup"><span data-stu-id="ecc69-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="ecc69-106">Die Garantie kann so eingerichtet werden, dass sie eine vollständige oder teilweise Deckung bietet, und Sie können Bedingungen einrichten, die sich auf Stunden, Ausgaben und Artikel beziehen.</span><span class="sxs-lookup"><span data-stu-id="ecc69-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="ecc69-107">Der erste Schritt besteht darin, alle Garantievereinbarungen mit Lieferanten zu erstellen, die Sie für Ihr Gerät haben.</span><span class="sxs-lookup"><span data-stu-id="ecc69-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="ecc69-108">Anschließend hängen Sie Garantievereinbarungen an Anlagen oder Anlagenarten an.</span><span class="sxs-lookup"><span data-stu-id="ecc69-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="ecc69-109">Gewährleistungsvereinbarungen des Lieferanten werden nur zu Informationszwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="ecc69-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="ecc69-110">Wenn die Lieferantengarantie auf eine Anlage eingerichtet ist, sehen Sie die Garantiezeit auf der Anlage.</span><span class="sxs-lookup"><span data-stu-id="ecc69-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="ecc69-111">Anlegen einer Garantievereinbarung</span><span class="sxs-lookup"><span data-stu-id="ecc69-111">Create a warranty agreement</span></span>

<span data-ttu-id="ecc69-112">Eine Garantievereinbarung kann mehrere Vertragszeilen umfassen, um die Garantie für Arbeitszeiten, Spesen und Artikel abzudecken.</span><span class="sxs-lookup"><span data-stu-id="ecc69-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="ecc69-113">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Anlagen** \> **Garantie**.</span><span class="sxs-lookup"><span data-stu-id="ecc69-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="ecc69-114">Wählen Sie **Neu**, um ein Produkt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ecc69-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="ecc69-115">Geben Sie im Feld **Garantie** eine Garantie-ID ein.</span><span class="sxs-lookup"><span data-stu-id="ecc69-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="ecc69-116">Geben Sie im Feld **Name** eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="ecc69-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="ecc69-117">Im Feld **Details** FastTab zeigt das Feld **Assets** die Anzahl der aktiven Anlagen, die die Garantievereinbarung nutzen.</span><span class="sxs-lookup"><span data-stu-id="ecc69-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="ecc69-118">Führen Sie auf den Seiten **Stundengarantie** und **Einzelteilgarantie** FastTabs diese Schritte aus, um Zeilen hinzuzufügen, die in eine Garantievereinbarung aufgenommen werden sollten, die sich auf Stunden oder Artikel bezieht:</span><span class="sxs-lookup"><span data-stu-id="ecc69-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="ecc69-119">Wählen Sie **Zeile hinzufügen**, um der Garantie eine neue Bedingung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ecc69-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="ecc69-120">Eine fortlaufende Zeilennummer wird automatisch in das Feld **Zeile** eingetragen.</span><span class="sxs-lookup"><span data-stu-id="ecc69-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="ecc69-121">Wählen Sie im Feld **Periode** die Art der Garantiezeit aus.</span><span class="sxs-lookup"><span data-stu-id="ecc69-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="ecc69-122">Geben Sie im Feld **Intervall** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ecc69-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="ecc69-123">Dieses Feld definiert die Anzahl der Zeiträume, für die die Garantie gültig sein soll.</span><span class="sxs-lookup"><span data-stu-id="ecc69-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="ecc69-124">Geben Sie im Feld **Prozent** den Deckungsprozentsatz für die Garantiezeile ein.</span><span class="sxs-lookup"><span data-stu-id="ecc69-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="ecc69-125">Der Prozentsatz gibt an, wie viel von Ihrem Unternehmen abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="ecc69-125">The percentage indicates how much is covered by your company.</span></span>

![Garantieseite](media/01-warranty.png)
