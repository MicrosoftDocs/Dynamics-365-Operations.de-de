---
title: Konventionen beim Anlagenleasing
description: Dieses Thema beschreibt die Konventionen für Leasingobjekte.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881807"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="d2074-103">Konventionen beim Anlagenleasing</span><span class="sxs-lookup"><span data-stu-id="d2074-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d2074-104">Dieses Thema beschreibt die Konventionen für Leasingobjekte.</span><span class="sxs-lookup"><span data-stu-id="d2074-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="d2074-105">Leasingkonventionen werden verwendet, um das Anfangsdatum eines Leasingbuchs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d2074-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="d2074-106">Wenn die Leasingkonvention auf **Keine** festgelegt ist, entspricht das Anfangsdatum dem Startdatum des Mietvertrags (also dem Wert des **Mietbeginn**-Feldes).</span><span class="sxs-lookup"><span data-stu-id="d2074-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="d2074-107">Wenn die Leasingkonvention auf **Voller Monat** festgelegt ist, ist das Anfangsdatum der erste Tag des Monats, in den das Startdatum des Mietvertrags fällt.</span><span class="sxs-lookup"><span data-stu-id="d2074-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="d2074-108">Das Anfangsdatum bestimmt das Startdatum des Zeitraums für die Zeitpläne zur Amortisierung von Leasingverbindlichkeiten und zur Abschreibung von Leasingobjekten.</span><span class="sxs-lookup"><span data-stu-id="d2074-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="d2074-109">Zinsaufwände und Abschreibungskosten werden am Periodenenddatum der entsprechenden Zeitpläne gebucht.</span><span class="sxs-lookup"><span data-stu-id="d2074-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="d2074-110">Die anfängliche Erfassung und der Regulierungsjournaleintrag erfolgen am Anfangsdatum.</span><span class="sxs-lookup"><span data-stu-id="d2074-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="d2074-111">Die Funktion für Leasingkonventionen muss über die Funktionsverwaltung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d2074-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="d2074-112">Suchen und wählen Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion namens **Leasingkonvention für das Anlagenleasing** aus. Wählen Sie anschließend **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d2074-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="d2074-113">Leasingkonventionen werden der Einrichtung eines Mietobjektbuchs zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d2074-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="d2074-114">Führen Sie die folgenden Schritte aus, um die Leasingkonvention anzuzeigen oder zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d2074-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="d2074-115">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Leasingbücher**.</span><span class="sxs-lookup"><span data-stu-id="d2074-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="d2074-116">Wählen Sie im Feld **Leasingkonvention** einen der folgenden Werte aus.</span><span class="sxs-lookup"><span data-stu-id="d2074-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="d2074-117">Leasingkonvention</span><span class="sxs-lookup"><span data-stu-id="d2074-117">Leasing convention</span></span> | <span data-ttu-id="d2074-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2074-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="d2074-119">Keines</span><span class="sxs-lookup"><span data-stu-id="d2074-119">None</span></span>               | <span data-ttu-id="d2074-120">Die Zeitpläne für die Amortisierung von Verbindlichkeiten und die Abschreibung von Leasingobjekten beginnen am Startdatum des Mietvertrags, da das Anfangsdatum dem Startdatum des Mietvertrags entspricht.</span><span class="sxs-lookup"><span data-stu-id="d2074-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="d2074-121">Das Enddatum ist einen Monat später.</span><span class="sxs-lookup"><span data-stu-id="d2074-121">The end date is one month later.</span></span> <span data-ttu-id="d2074-122">Diese Leasingkonvention garantiert nicht, dass die Zinsen am letzten Tag eines jeden Monats verbucht werden.</span><span class="sxs-lookup"><span data-stu-id="d2074-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="d2074-123">Ganzer Monat</span><span class="sxs-lookup"><span data-stu-id="d2074-123">Full month</span></span>         | <span data-ttu-id="d2074-124">Bei Mietverträgen mit einem Startdatum, das auf einem beliebigen Zeitpunkt während des Monats liegt, beginnen die Zeitpläne für die Amortisierung von Verbindlichkeiten sowie die Abschreibung von Leasingobjekten am ersten Tag des Monats mit der Aufwandsabgrenzung.</span><span class="sxs-lookup"><span data-stu-id="d2074-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="d2074-125">Diese Leasingkonvention gewährleistet, dass am letzten Tag eines jeden Monats für den gesamten Monat Zinsen abgegrenzt werden.</span><span class="sxs-lookup"><span data-stu-id="d2074-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="d2074-126">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d2074-126">Select **Save**.</span></span>

<span data-ttu-id="d2074-127">Wenn ein Mietvertrag erstellt wird, wird das Anfangsdatum jedes Buches automatisch basierend auf dem für den Mietvertrag eingegebenen Startdatum und der für das Buch angegebenen Leasingkonvention eingegeben.</span><span class="sxs-lookup"><span data-stu-id="d2074-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
