---
title: Arbeit bleibt blockiert
description: Arbeit bleibt blockiert
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924129"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="5ffd0-103">Arbeit bleibt blockiert</span><span class="sxs-lookup"><span data-stu-id="5ffd0-103">Work remains blocked</span></span>

<span data-ttu-id="5ffd0-104">Fehlercode: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="5ffd0-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="5ffd0-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="5ffd0-105">Symptoms</span></span>

<span data-ttu-id="5ffd0-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="5ffd0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5ffd0-107">Arbeit %1 bleibt gesperrt, da der zugehörige Zyklus %2 den Status %3 hat.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="5ffd0-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="5ffd0-108">Cause</span></span>

<span data-ttu-id="5ffd0-109">Die Arbeit wird gerade auf einer Welle verarbeitet und kann nicht entsperrt werden, wie durch eine der folgenden Bedingungen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="5ffd0-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="5ffd0-110">Auf der Registerkarte **Sperrgründe** wird das Feld **Arbeitssperrgrund** für eine oder mehrere Zeilen auf *Verarbeitungswelle* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="5ffd0-111">Wenn Sie **Welle** in der Gruppe **Bezogene Informationen** auf der Registerkarte **Bezogene Informationen** des Aktivitätsbereichs auswählen, wird das Feld **Wellenstatus** auf *Verarbeitet* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="5ffd0-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="5ffd0-112">Resolution</span></span>

<span data-ttu-id="5ffd0-113">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Zugehörige Informationen** in der Gruppe **Zugehörige Informationen** die Option **Welle**.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="5ffd0-114">Wählen Sie dann auf der Seite **Wellen** im Aktivitätsbereich, auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Wellendaten bereinigen**.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="5ffd0-115">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="5ffd0-115">Workaround</span></span>

<span data-ttu-id="5ffd0-116">Wenn die vorangegangenen Schritte das Problem nicht behoben haben, können Sie die Arbeit abbrechen, indem Sie diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="5ffd0-117">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="5ffd0-118">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie stornieren möchten und die derzeit einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* hat.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="5ffd0-119">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-119">Select **OK**.</span></span>
1. <span data-ttu-id="5ffd0-120">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="5ffd0-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="5ffd0-121">Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="5ffd0-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
