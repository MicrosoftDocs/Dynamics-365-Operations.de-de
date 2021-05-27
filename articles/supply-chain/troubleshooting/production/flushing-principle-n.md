---
title: Die Einstellungen für das Stücklisten-Bezugsprinzip in Stücklistenpositionen werden nicht berücksichtigt
description: Die Einstellungen für das Stücklisten-Bezugsprinzip in Stücklistenpositionen werden nicht berücksichtigt.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026543"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="0a25b-103">Die Einstellungen für das Stücklisten-Bezugsprinzip in Stücklistenpositionen werden nicht berücksichtigt</span><span class="sxs-lookup"><span data-stu-id="0a25b-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="0a25b-104">KB-Nummer: 4612725</span><span class="sxs-lookup"><span data-stu-id="0a25b-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="0a25b-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="0a25b-105">Symptoms</span></span>

<span data-ttu-id="0a25b-106">Dieses Problem tritt auf, wenn das Feld **Automatischer Stücklistenverbrauch** in der Registerkarte **Automatisches Update** auf der Seite **Produktionssteuerungsparameter** ist auf *Stücklisten-Bezugsprinzip* eingestellt.</span><span class="sxs-lookup"><span data-stu-id="0a25b-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="0a25b-107">Diese Einstellung gibt an, dass alle Stücklistenpositionen beim Eingang einer Bestellung automatisch verbraucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0a25b-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="0a25b-108">Wenn das Feld **Stücklisten-Bezugsprinzip** bei Stücklistenpositionen nicht explizit auf *Manuell* gesetzt ist, wäre zu erwarten, dass die Stücklistenpositionen nicht automatisch verbraucht werden.</span><span class="sxs-lookup"><span data-stu-id="0a25b-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="0a25b-109">Wenn dieses Problem auftritt, werden in Stücklistenpositionen, in denen das Feld **Stücklisten-Bezugsprinzip** auf *Manuell* gesetzt ist, jedoch automatisch verbraucht.</span><span class="sxs-lookup"><span data-stu-id="0a25b-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="0a25b-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="0a25b-110">Resolution</span></span>

<span data-ttu-id="0a25b-111">Wenn dieses Problem auftritt, sind Ihre Produktionssteuerungsparameter möglicherweise so eingerichtet, dass sie die **Stücklisten-Bezugsprinzip**-Einstellung auf Stücklistenpositionen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0a25b-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="0a25b-112">Überprüfen Sie auf der Seite **Produktionssteuerungsparameter** auf der Registerkarte **Automatisches Update** den Wert des Felds **Automatischer Stücklistenverbrauch**.</span><span class="sxs-lookup"><span data-stu-id="0a25b-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="0a25b-113">Wenn es auf *Immer* eingestellt ist, ignoriert das System die **Stücklisten-Bezugsprinzip**-Einstellung auf allen Stücklistenpositionen und leert die Positionen immer.</span><span class="sxs-lookup"><span data-stu-id="0a25b-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="0a25b-114">Damit das System **Stücklisten-Bezugsprinzip**-Einstellung respektiert, andern Sie in den Stücklistenpositionen den Wert des Felds **Automatischer Stücklistenverbrauch** auf *Stücklisten-Bezugsprinzip*.</span><span class="sxs-lookup"><span data-stu-id="0a25b-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
