---
title: Arbeit kann nicht storniert werden, weil sie blockiert ist
description: Arbeit kann nicht storniert werden, weil sie blockiert ist
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924278"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="402c7-103">Arbeit kann nicht storniert werden, weil sie blockiert ist</span><span class="sxs-lookup"><span data-stu-id="402c7-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="402c7-104">Fehlercode: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="402c7-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="402c7-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="402c7-105">Symptoms</span></span>

<span data-ttu-id="402c7-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="402c7-106">The system shows the following error message:</span></span>

> <span data-ttu-id="402c7-107">Arbeit %1 kann nicht abgebrochen werden, weil sie durch Grundtyp %2 blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="402c7-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="402c7-108">Die Arbeit muss entsperrt werden, bevor sie storniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="402c7-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="402c7-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="402c7-109">Cause</span></span>

<span data-ttu-id="402c7-110">Die Arbeit ist blockiert und kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="402c7-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="402c7-111">Auf der Seite **Arbeit**, auf der Registerkarte **Allgemein**, ist die Option **Sperrung** auf *Ja* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="402c7-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="402c7-112">Diese Einstellung gibt an, dass die Arbeit blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="402c7-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="402c7-113">Die Registerkarte **Sperrgründe** zeigt an, warum die Arbeit gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="402c7-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="402c7-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="402c7-114">Resolution</span></span>

<span data-ttu-id="402c7-115">Um die Sperrung des Werks aufzuheben, wählen Sie die Registerkarte **Sperrgründe** und führen dann einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="402c7-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="402c7-116">Wenn das Feld **Arbeitssperrungsgrund** auf *Undefinierter Grund* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeit** in der Gruppe **Arbeit** die Option **Arbeitssperre aufheben**.</span><span class="sxs-lookup"><span data-stu-id="402c7-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="402c7-117">Wenn das Feld **Arbeitssperrungsgrund** auf *Verarbeitungswelle* festgelegt ist: Wählen Sie im Aktivitätsbereich auf der Registerkarte **Zugehörige Informationen** in der Gruppe **Zugehörige Informationen** die Option **Welle**.</span><span class="sxs-lookup"><span data-stu-id="402c7-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="402c7-118">Wählen Sie dann auf der Seite **Wellen** im Aktivitätsbereich, auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Wellendaten bereinigen**.</span><span class="sxs-lookup"><span data-stu-id="402c7-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="402c7-119">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="402c7-119">Workaround</span></span>

<span data-ttu-id="402c7-120">Wenn die vorangegangenen Schritte das Problem nicht behoben haben, können Sie die Arbeit abbrechen, indem Sie diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="402c7-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="402c7-121">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="402c7-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="402c7-122">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie stornieren möchten und die derzeit einen **Arbeitsstatus**-Wert von *Offen*, *In Bearbeitung*, *Abgebrochen*, *Zusammengeführt* oder *Geschlossen* hat.</span><span class="sxs-lookup"><span data-stu-id="402c7-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="402c7-123">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="402c7-123">Select **OK**.</span></span>
1. <span data-ttu-id="402c7-124">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="402c7-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="402c7-125">Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="402c7-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
