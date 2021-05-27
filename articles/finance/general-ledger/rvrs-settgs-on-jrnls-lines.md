---
title: Einstellungen für Erfassungen und Positionen stornieren
description: In diesem Thema wird erläutert, warum ein Stornoeintrag, der in einer allgemeinen Erfassung eingegeben wurde, möglicherweise nicht in der gebuchten Transaktion enthalten ist.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028564"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="46319-103">Einstellungen für Erfassungen und Positionen stornieren</span><span class="sxs-lookup"><span data-stu-id="46319-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46319-104">In diesem Thema wird erläutert, warum ein Stornoeintrag, der in einer allgemeinen Erfassung eingegeben wurde, möglicherweise nicht in der gebuchten Transaktion enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="46319-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="46319-105">Symptom</span><span class="sxs-lookup"><span data-stu-id="46319-105">Symptom</span></span>

<span data-ttu-id="46319-106">Eine allgemeine Erfassung enthält eine Stornierungsbuchung und ein Stornierungsdatum für die Erfassung.</span><span class="sxs-lookup"><span data-stu-id="46319-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="46319-107">Wenn Sie die Erfassung buchen, wird keiner der Belege storniert.</span><span class="sxs-lookup"><span data-stu-id="46319-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="46319-108">Was sind die Gründe dafür?</span><span class="sxs-lookup"><span data-stu-id="46319-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="46319-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="46319-109">Resolution</span></span>

<span data-ttu-id="46319-110">Wenn die Erfassung gebucht wird, werden beim Stornierungsvorgang nur die Einstellungen **Stornierungseintrag** und **Stornierungsdatum** im Abschnitt **Positionen** des Belegs berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="46319-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="46319-111">Dieser Ansatz ermöglicht es, in einer Erfassung einige zur Stornierung markierte sowie andere Belege einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="46319-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="46319-112">Die Werte aus der Erfassung werden nur beim Hinzufügen von *neuen* Positionen als Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="46319-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="46319-113">Änderungen an den Werten der Erfassung wirken sich nicht auf vorhandene Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="46319-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="46319-114">In diesem Beispiel wurden zuerst die Belegzeilen eingegeben.</span><span class="sxs-lookup"><span data-stu-id="46319-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="46319-115">Wenn Sie die Positionsdetails eingeben, bevor Sie die Erfassung als Stornobuchung festlegen, wird die Bezeichnung für Stornierungseintrag und -datum nicht auf vorhandene Positionen angewendet.</span><span class="sxs-lookup"><span data-stu-id="46319-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="46319-116">Durch eine Änderung des Stornierungseintrags oder des Stornierungsdatums in einer vorhandenen Position werden diese Änderungen an andere Positionen im selben Beleg weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="46319-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="46319-117">Um die Leistung zu optimieren, wird das Raster nicht aktualisiert, nachdem Änderungen an andere Positionen weitergegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="46319-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="46319-118">Sie können die aktualisierten Werte anzeigen, indem Sie das Raster aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="46319-118">You can display the updated values by refreshing the grid.</span></span>


