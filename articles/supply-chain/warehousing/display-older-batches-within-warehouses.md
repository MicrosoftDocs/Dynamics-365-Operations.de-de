---
title: Anzeige von älteren Chargen am Lagerort auf einem mobilen Gerät konfigurieren
description: Dieses Thema beschreibt, wie ein mobiles Gerät eingerichtet wird, um eine Liste der Standorte anzuzeigen, die Chargen enthalten, die älter als der aktuelle Standort einer Arbeitsposition sind.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f5317f15a7c7aad53971812e4b22f9e4be79d5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251837"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="4b997-103">Anzeige von älteren Chargen am Lagerort auf einem mobilen Gerät konfigurieren</span><span class="sxs-lookup"><span data-stu-id="4b997-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b997-104">Mit der Konfiguration **Ältere Chargen im Lager anzeigen** können Sie eine Liste der Standorte anzeigen, die Chargen enthalten, die älter als der aktuelle Standort der Arbeitsposition sind.</span><span class="sxs-lookup"><span data-stu-id="4b997-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="4b997-105">Die Liste der angezeigten Standorte enthält Informationen über die älteren Chargen an dem Standort, mit Ablaufdatum und physischem Bestand jeder Charge.</span><span class="sxs-lookup"><span data-stu-id="4b997-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="4b997-106">Sie können auswählen, von einem neuen Standort auszuwählen, oder weiterhin vom aktuellen Standort auswählen.</span><span class="sxs-lookup"><span data-stu-id="4b997-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="4b997-107">Von einem neuen Standort auswählen – Wenn Sie von einem neuen Standort auswählen wollen, wird die aktuelle Arbeitsposition aktualisiert, sodass sie den neuen Standort verwendet, und die Arbeit wird mit dem neuen Standort unverändert fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4b997-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="4b997-108">Damit der neue Standort gültig ist, muss er über genügend verfügbare Menge für die gesamte Arbeitsposition verfügen.</span><span class="sxs-lookup"><span data-stu-id="4b997-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="4b997-109">Falls die erforderliche Menge nicht zur Verfügung steht, wird die Arbeitsposition nicht aktualisiert, und die Liste wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4b997-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="4b997-110">Weiter vom aktuellen Standort auswählen – Wenn Sie weiter mit dem Standort der aktuellen Arbeitsposition arbeiten wollen, werden die Mengen für die Arbeitsposition weiter von dem ursprünglichen Standort ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4b997-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="4b997-111">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="4b997-111">Where it applies</span></span>
<span data-ttu-id="4b997-112">Die Anzeige älterer Chargen im Lager ist in Menüeinträgen für mobile Geräte konfiguriert und betrifft die Auswahl von Chargen.</span><span class="sxs-lookup"><span data-stu-id="4b997-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="4b997-113">Einrichtung der Anzeige älterer Chargen im Lager</span><span class="sxs-lookup"><span data-stu-id="4b997-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="4b997-114">Die Konfiguration **Anzeige älterer Chargen im Lager** ist in Menüeinträgen für mobile Geräte verfügbar, wenn die Option **Älteste Charge auswählen** auf **Warnung** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4b997-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="4b997-115">Unter **Lagerverwaltung** > **Einrichtung** > **Mobiles Gerät** > **Menüeinträge mobiles Gerät** setzen Sie **Vorhandene Arbeit verwenden** für den Menüeintrag auf **Ja** und wählen dann **Warnung** im Feld **Älteste Charge auswählen**.</span><span class="sxs-lookup"><span data-stu-id="4b997-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]