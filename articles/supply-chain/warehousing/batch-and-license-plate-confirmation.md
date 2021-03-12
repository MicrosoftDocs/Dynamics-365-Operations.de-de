---
title: Chargen- und Kennzeichenbestätigung
description: In diesem Thema wird beschrieben, wie Sie Chargen- und Kennzeichenbestätigung über ein mobiles Gerät einrichten und anwenden.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97790b91d4de536b89b580c26ef1e37145f7d7c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977437"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="c5c42-103">Chargen- und Kennzeichenbestätigung</span><span class="sxs-lookup"><span data-stu-id="c5c42-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5c42-104">Chargenbestätigung ermöglicht Ihnen, zu bestätigen, dass die richtige Charge vom mobilen Gerät gewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c5c42-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="c5c42-105">Nur bei der ersten Arbeitsentnahme für Artikel aus Chargen oberhalb, wobei Charge oberhalb angibt, dass die Charge in der Suchenhierarchie höher reicht, als der Lagerplatz, müssen Sie überprüfen, dass die entnommene Charge mit der Charge auf der Arbeitsposition übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c5c42-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="c5c42-106">Kennzeichenbestätigung ermöglicht Ihnen, zu bestätigen, dass die richtige Kennzeichen vom mobilen Gerät gewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c5c42-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="c5c42-107">Wenn Arbeit aus einem Phasenlagerplatz entnommen wird, müssen Sie überprüfen dass das entnommene Kennzeichen mit dem Kennzeichen übereinstimmt, das der Arbeit zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c5c42-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="c5c42-108">Wenn die Arbeit gestartet wird, indem ein Kennzeichen gescannt wird, wird dieser Bestätigungsschritt übersprungen.</span><span class="sxs-lookup"><span data-stu-id="c5c42-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c5c42-109">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="c5c42-109">Where it applies</span></span>

<span data-ttu-id="c5c42-110">Bestätigung gilt in den folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="c5c42-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="c5c42-111">Chargenbestätigung gilt für die erste Entnahme der Arbeit für Artikel der Chargen oberhalb.</span><span class="sxs-lookup"><span data-stu-id="c5c42-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="c5c42-112">Kennzeichenbestätigung gilt für Entnahmen aus den Phasenlagerplätzen.</span><span class="sxs-lookup"><span data-stu-id="c5c42-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5c42-113">Die Wiederbeschaffung wird für die Bestätigung von Ladungsträgern nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5c42-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="c5c42-114">Beim Ausführen von Wiederbeschaffung wird kein Schritt zur Bestätigung von Ladungsträgern erstellt.</span><span class="sxs-lookup"><span data-stu-id="c5c42-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="c5c42-115">Chargen- und Kennzeichenbestätigung einrichten</span><span class="sxs-lookup"><span data-stu-id="c5c42-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="c5c42-116">Sie können Chargen- und Kennzeichenbestätigung von den Menüeinträgen des mobilen Geräts aus konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c5c42-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="c5c42-117">Geben Sie im Menüeintrag des mobilen Geräts die Einrichtung der Arbeitsbestätigung ein.</span><span class="sxs-lookup"><span data-stu-id="c5c42-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="c5c42-118">Wählen Sie die Option für Kennzeichen- oder Chargen-Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="c5c42-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="c5c42-119">Beide Optionen sind für Arbeitstypentnahmen verfügbar, bei denen keine automatische Bestätigung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c5c42-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
