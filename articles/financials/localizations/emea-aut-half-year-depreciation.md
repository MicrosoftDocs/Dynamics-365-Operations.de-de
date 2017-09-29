---
title: "Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich"
description: "Dieses Thema enthält Informationen für Benutzer von juristischen Personen in Österreich zu der Abschreibung von zusätzlichen Anschaffungen, wenn die Abschreibungskonvention für das Halbjahr für die Anlagenabschreibung verwendet wird."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBook, AssetDepreciationProfile, AssetParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272663
ms.search.region: Austria
ms.author: sndray
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 56b5529468981cd184aec26f8547753e23e33b6d
ms.contentlocale: de-de
ms.lasthandoff: 06/29/2017


---

# <a name="half-year-depreciation-on-additional-acquisitions-for-austria"></a><span data-ttu-id="ca286-103">Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich</span><span class="sxs-lookup"><span data-stu-id="ca286-103">Half-year depreciation on additional acquisitions for Austria</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ca286-104">Dieses Thema enthält Informationen für Benutzer von juristischen Personen in Österreich zu der Abschreibung von zusätzlichen Anschaffungen, wenn die Abschreibungskonvention für das Halbjahr für die Anlagenabschreibung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca286-104">This topic provides information for users in legal entities in Austria about the depreciation of additional acquisitions when the Half year convention is used for fixed asset depreciation.</span></span>

<span data-ttu-id="ca286-105">Bei juristischen Personen in Österreich werden die Abschreibung für zusätzliche Anschaffungen und Anschaffungsänderungen gemäß den folgenden Regeln berechnet:</span><span class="sxs-lookup"><span data-stu-id="ca286-105">In legal entities in Austria depreciation for additional acquisitions and acquisition adjustments is calculated according the following rules:</span></span>

-   <span data-ttu-id="ca286-106">Betrag zusätzlicher Anschaffungen, die im ersten Jahr der Anschaffung gebucht werden, wird abgeschrieben vom Abschreibungsstartdatum (wenn eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen, die vor dem 30. Juni gebucht werden oder eine Anlage, die nach dem 1. Juli gekauft wurde und zusätzliche Anschaffungen, die nach dem 1. Juli gebucht werden) oder ab dem 1. Juli, falls eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen, die nach dem 1. Juli gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ca286-106">Amount of additional acquisitions posted in the year of initial acquisition is depreciated starting from the Depreciation run date (if a Fixed asset is purchased before June 30th and additional acquisition posted before June 30th or a fixed asset is purchased after July 1st and additional acquisition posted after July 1st) or from the July 1st if a fixed asset is purchased before June 30th and additional acquisition posted after July 1st.</span></span>
-   <span data-ttu-id="ca286-107">Betrag zusätzlicher Anschaffungen, die im Jahr nach dem ersten Jahr der Anschaffung gebucht werden, wird gemäß Konventionsregel vom Halbjahr beginnend am 1. Januar oder am 1. Juli des Jahres abgeschrieben, in dem die zusätzlichen Anschaffungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ca286-107">Amount of additional acquisitions posted in the year later than year of initial acquisition is depreciated according to half year convention rule starting from the January 1st or the July 1st of the year where the additional acquisitions is posted.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ca286-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ca286-108">Prerequisites</span></span>
|                                       |                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca286-109">**Voraussetzung**</span><span class="sxs-lookup"><span data-stu-id="ca286-109">**Prerequisite**</span></span>                      | <span data-ttu-id="ca286-110">**Informationen**</span><span class="sxs-lookup"><span data-stu-id="ca286-110">**Information**</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ca286-111">Einrichten von **Abschreibungsprofilen**</span><span class="sxs-lookup"><span data-stu-id="ca286-111">Set up **Depreciation profile**</span></span>       | <span data-ttu-id="ca286-112">Öffnen Sie **Analgen** &gt; **Einrichten** &gt; **Abschreibungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="ca286-112">Open **Fixed assets** &gt; **Setup** &gt; **Depreciation profile**.</span></span> <span data-ttu-id="ca286-113">Für Abschreibungsprofile mit **Abschreibungsmethoden- = Verbleibende lineare Nutzungsdauer** markieren Sie das Kontrollkästchen **Halbjährliche Abschreibung für sonstige Anschaffungen**</span><span class="sxs-lookup"><span data-stu-id="ca286-113">For depreciation profile with **Depreciation method = Straight line life remaining**, mark check box **Half year depreciation on additional acquisitions**.</span></span> <span data-ttu-id="ca286-114">Wenn diese Option aktiviert ist, wird die Abschreibungskonvention **Halbes Jahr (Startjahr)** für zusätzliche Anschaffungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="ca286-114">If this option is switched on, depreciation convention **Half year (start year)** is implemented for additional acquisitions.</span></span> |
| <span data-ttu-id="ca286-115">Einrichten von **Anlagenparametern**</span><span class="sxs-lookup"><span data-stu-id="ca286-115">Set up **Fixed assets parameters**</span></span>    | <span data-ttu-id="ca286-116">Wechseln Sie zu **Anlagen** &gt; **Einstellungen** &gt; **Anlagenparameter.**</span><span class="sxs-lookup"><span data-stu-id="ca286-116">Open **Fixed assets** &gt; **Setup** &gt; **Fixed assets parameters.**</span></span> <span data-ttu-id="ca286-117">Auf der Registerkarte **Allgemeines** wählen Sie die folgenden Parameter:  **Wenden Sie bestimmte Regeln zur Abschreibung des Halbjahr an**, **Automatische Abschreibungsregulierungsbeträge mit Abgang erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ca286-117">On the **General** tab, select the following parameters:  **Apply specific rules for half year depreciation** , **Automatically create depreciation adjustment amounts with disposal**.</span></span>                                                                                  |

## <a name="halfyear-depreciation-on-additional-acquisitions-calculation"></a><span data-ttu-id="ca286-118">Halbjährliche Abschreibung auf sonstige Anschaffungsberechnung</span><span class="sxs-lookup"><span data-stu-id="ca286-118">Halfyear depreciation on additional acquisitions calculation</span></span>
<span data-ttu-id="ca286-119">Wenn das Kontrollkästchen **Wenden Sie bestimmte Regeln zur Abschreibung des Halbjahr an** und das Kontrollkästchen **Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen** aktiviert ist, wird der Abschreibungsregulierungsausgleichsbetrag für Anlagen mit  Abschreibungsmethode **Verbleibende lineare Nutzungsdauer)** **Halbjahr (Jahresanfang)**, die verwendet wird, automatisch mit dem Abgang gebucht, der gemäß den Konventionsregeln des Halbjahr berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ca286-119">When **Apply specific rules for half year depreciation** checkbox is marked, and **Automatically create depreciation adjustment amounts with disposal** checkbox is marked, the depreciation adjustment amount for fixed assets with **Straight line life remaining** depreciation method and **Half year (start of year)** convention used, is posted automatically with the disposal calculated according to the half year convention rules.</span></span>





