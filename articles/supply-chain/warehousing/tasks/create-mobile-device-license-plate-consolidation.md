---
title: Menüoption für ein mobiles Gerät für die Ladungsträger-Konsolidierung erstellen
description: Diese Verfahren zeigt, wie Sie eine Menüoption des mobilen Geräts für Ladungsträgerkonsolidierungsarbeit erstellen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54457261d4f80648050845f309bcbbcc16caa629
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239013"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="3fbb5-103">Menüoption für ein mobiles Gerät für die Ladungsträger-Konsolidierung erstellen</span><span class="sxs-lookup"><span data-stu-id="3fbb5-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3fbb5-104">Diese Verfahren zeigt, wie Sie eine Menüoption des mobilen Geräts für Ladungsträgerkonsolidierungsarbeit erstellen.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="3fbb5-105">Dies ermöglicht Lagerarbeiteren das Konsolidieren von Artikeln auf Ladungsträgern mit Artikeln auf einem anderen Ladungsträger innerhalb desselben Standorts.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="3fbb5-106">Sie können dies beispielsweise nutzen, wenn aufeinander folgende Stagingschritte bei beiden Arbeitsaufträgen identisch waren, damit die Arbeit für den zusammengeführten Artikel nur einmal ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="3fbb5-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="3fbb5-108">Diese Aufgabe wird normalerweise von einem Lagerortleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="3fbb5-109">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="3fbb5-110">Wechseln Sie zu "Lagerortverwaltung" > "Einstellungen" > "Mobiles Gerät" > "Menüoptionen für mobiles Gerät".</span><span class="sxs-lookup"><span data-stu-id="3fbb5-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="3fbb5-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="3fbb5-111">Click New.</span></span>
3. <span data-ttu-id="3fbb5-112">Geben Sie im Feld "Menüoptionsname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="3fbb5-113">Geben Sie im Feld "Titel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="3fbb5-114">Wählen Sie im Feld "Modus" "Indirekt"aus.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="3fbb5-115">Wählen Sie im Feld "Aktivitätscode" "Kennzeichen konsolidieren" aus.</span><span class="sxs-lookup"><span data-stu-id="3fbb5-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]