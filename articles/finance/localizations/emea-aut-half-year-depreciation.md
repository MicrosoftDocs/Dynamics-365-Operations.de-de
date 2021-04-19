---
title: Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich
description: Dieses Thema enthält Informationen zur Abschreibung sonstiger Anschaffungen, wenn die Halbjahreskonvention für die Abschreibung von Anlagevermögen verwendet wird.
author: ShylaThompson
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBook, AssetDepreciationProfile, AssetParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272663
ms.search.region: Austria
ms.author: sndray
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 0c08cbea2b2300bd70d5dd2e19c28eed00c1e2b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839920"
---
# <a name="half-year-depreciation-on-additional-acquisitions-for-austria"></a><span data-ttu-id="17795-103">Halbjährliche Abschreibung auf sonstige Anschaffungen für Österreich</span><span class="sxs-lookup"><span data-stu-id="17795-103">Half-year depreciation on additional acquisitions for Austria</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17795-104">Dieses Thema enthält Informationen für Benutzer zur Abschreibung sonstiger Anschaffungen, wenn die Halbjahreskonvention für die Abschreibung von Anlagevermögen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17795-104">This topic provides information for users about the depreciation of additional acquisitions when the Half year convention is used for fixed asset depreciation.</span></span>

<span data-ttu-id="17795-105">Bei juristischen Personen in Österreich werden die Abschreibung für zusätzliche Anschaffungen und Anschaffungsänderungen gemäß den folgenden Regeln berechnet:</span><span class="sxs-lookup"><span data-stu-id="17795-105">In legal entities in Austria, depreciation for additional acquisitions and acquisition adjustments is calculated according to the following rules:</span></span>

-   <span data-ttu-id="17795-106">Die Anzahl der zusätzlichen Anschaffungen, die im ersten Jahr der Anschaffung gebucht werden, wird abgeschrieben ab dem Ausführungsdatum der Abschreibung (wenn eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen vor dem 30. Juni gebucht werden oder eine Anlage nach dem 1. Juli gekauft wird und zusätzliche Anschaffungen nach dem 1. Juli gebucht werden) oder ab dem 1. Juli, falls eine Anlage vor dem 30. Juni gekauft wird und zusätzliche Anschaffungen nach dem 1. Juli gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="17795-106">The number of additional acquisitions posted in the year of initial acquisition is depreciated starting from the Depreciation run date (if a Fixed asset is purchased before June 30 and additional acquisition posted before June 30 or a fixed asset is purchased after July 1 and additional acquisition posted after July 1) or from the July 1 if a fixed asset is purchased before June 30 and additional acquisition posted after July 1.</span></span>
-   <span data-ttu-id="17795-107">Die Anzahl der zusätzlichen Anschaffungen, die im Jahr nach dem ersten Jahr der Anschaffung gebucht werden, wird gemäß Halbjahreskonventionsregel beginnend am 1. Januar oder am 1. Juli des Jahres abgeschrieben, in dem die zusätzlichen Anschaffungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="17795-107">The number of additional acquisitions posted in the year later than year of initial acquisition is depreciated according to half year convention rule starting from the January 1 or the July 1 of the year where the additional acquisitions are posted.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="17795-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="17795-108">Prerequisites</span></span>

| <span data-ttu-id="17795-109">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="17795-109">Prerequisite</span></span>                      | <span data-ttu-id="17795-110">Informationen</span><span class="sxs-lookup"><span data-stu-id="17795-110">Information</span></span>                |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17795-111">Einrichten von **Abschreibungsprofilen**</span><span class="sxs-lookup"><span data-stu-id="17795-111">Set up **Depreciation profile**</span></span>       | <span data-ttu-id="17795-112">Wechseln Sie zu **Anlagen** > **Einstellungen** > **Abschreibungsprofile**.</span><span class="sxs-lookup"><span data-stu-id="17795-112">Go to **Fixed assets** > **Setup** > **Depreciation profile**.</span></span> <span data-ttu-id="17795-113">Für ein Abschreibungsprofil mit der **Abschreibungsmethode** = `Straight line life remaining` wählen Sie das Kontrollkästchen **Halbjährliche Abschreibung für sonstige Anschaffungen**.</span><span class="sxs-lookup"><span data-stu-id="17795-113">For a depreciation profile with **Depreciation method** = `Straight line life remaining`, select the **Half year depreciation on additional acquisitions** check box.</span></span> <span data-ttu-id="17795-114">Wenn diese Option aktiviert ist, wird die Abschreibungskonvention **Halbes Jahr (Startjahr)** für zusätzliche Anschaffungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="17795-114">If this option is switched on, depreciation convention **Half year (start year)** is implemented for additional acquisitions.</span></span> |
| <span data-ttu-id="17795-115">Einrichten von **Anlagenparametern**</span><span class="sxs-lookup"><span data-stu-id="17795-115">Set up **Fixed assets parameters**</span></span>    | <span data-ttu-id="17795-116">Wechseln Sie zu **Anlagen** > **Einstellungen** > **Anlagenparameter**.</span><span class="sxs-lookup"><span data-stu-id="17795-116">Go to **Fixed assets** > **Setup** > **Fixed assets parameters.**</span></span> <span data-ttu-id="17795-117">Auf der Registerkarte **Allgemeines** wählen Sie **Bestimmte Regeln zur halbjährlichen Abschreibung anwenden** und **Automatische Abschreibungsregulierungsbeträge mit Abgang erstellen**.</span><span class="sxs-lookup"><span data-stu-id="17795-117">On the **General** tab, select **Apply specific rules for half year depreciation** and **Automatically create depreciation adjustment amounts with disposal**.</span></span>                                                                                  |

## <a name="half-year-depreciation-on-additional-acquisitions-calculation"></a><span data-ttu-id="17795-118">Halbjährliche Abschreibung auf sonstige Anschaffungsberechnung</span><span class="sxs-lookup"><span data-stu-id="17795-118">Half year depreciation on additional acquisitions calculation</span></span>
<span data-ttu-id="17795-119">Wenn die Kontrollkästchen **Bestimmte Regeln zur halbjährlichen Abschreibung anwenden** und **Automatisch Abschreibungsregulierungsbeträge mit Abgang erstellen** aktiviert sind, wird der Abschreibungsregulierungsbetrag für Anlagen mit der Abschreibungsmethode `Straight line life remaining` und der Konvention **Halbjahr (Jahresanfang)** automatisch mit dem Abgang gebucht, der gemäß den Halbjahreskonventionsregeln berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="17795-119">When the **Apply specific rules for half year depreciation** and **Automatically create depreciation adjustment amounts with disposal** check boxes are marked, the depreciation adjustment amount for fixed assets with the `Straight line life remaining` depreciation method and **Half year (start of year)** convention, is posted automatically with the disposal that is calculated according to the half year convention rules.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]