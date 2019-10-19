---
title: Anlagengruppen einrichten
description: In diesem Abschnitt erfahren Sie, wie Sie eine neue Anlagengruppe anlegen.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186876"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="e21c6-103">Anlagengruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="e21c6-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e21c6-104">In diesem Abschnitt erfahren Sie, wie Sie eine neue Anlagengruppe anlegen.</span><span class="sxs-lookup"><span data-stu-id="e21c6-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="e21c6-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="e21c6-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="e21c6-106">Gehen Sie im Navigationsbereich zu **Module > Anlagen > Einrichtung > Anlagengruppen**.</span><span class="sxs-lookup"><span data-stu-id="e21c6-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="e21c6-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e21c6-107">Select **New**.</span></span>
3. <span data-ttu-id="e21c6-108">Geben Sie im Feld **Anlagegruppe** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e21c6-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="e21c6-109">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e21c6-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="e21c6-110">Autonummerierung der Anlage und Nummernfolgecode auf der Gruppe **Anlage** übersteuern die Einstellungen zu den Parametern der Anlage.</span><span class="sxs-lookup"><span data-stu-id="e21c6-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="e21c6-111">Sie können sie hier ändern, wenn die Anlagen in dieser Anlagengruppe eine andere Nummerierung als andere Gruppen haben.</span><span class="sxs-lookup"><span data-stu-id="e21c6-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="e21c6-112">Wählen Sie **Bücher**.</span><span class="sxs-lookup"><span data-stu-id="e21c6-112">Select **Books**.</span></span>
6. <span data-ttu-id="e21c6-113">Geben Sie im Feld **Buch** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e21c6-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="e21c6-114">Das Feld **Abschreibung berechnen** ist auf **Ja** gesetzt, so dass das Anlagenbuch in die Abschreibungsvorschläge aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="e21c6-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="e21c6-115">Wenn **Abschreibung berechnen** auf **Nein** gesetzt ist, wird die Anlage nicht automatisch abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="e21c6-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="e21c6-116">Legen Sie die Nutzungsdauer der Anlage in Jahren fest.</span><span class="sxs-lookup"><span data-stu-id="e21c6-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="e21c6-117">Beachten Sie, dass der Feldwert **Abschreibungszeiträume** nach der Einstellung der Nutzungsdauer berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e21c6-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="e21c6-118">Wählen Sie im Feld **Abschreibungskonvention** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e21c6-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="e21c6-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e21c6-119">Close the page.</span></span>

