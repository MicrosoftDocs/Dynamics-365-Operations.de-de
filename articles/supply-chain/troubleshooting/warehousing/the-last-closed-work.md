---
title: Die letzte geschlossene Arbeitszeile muss ein PUT sein
description: Die letzte geschlossene Arbeitszeile muss ein PUT sein
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924374"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="cd25d-103">Die letzte geschlossene Arbeitszeile muss ein PUT sein</span><span class="sxs-lookup"><span data-stu-id="cd25d-103">The last closed work line must be a put</span></span>

<span data-ttu-id="cd25d-104">Fehlercode: WAX1285</span><span class="sxs-lookup"><span data-stu-id="cd25d-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="cd25d-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="cd25d-105">Symptoms</span></span>

<span data-ttu-id="cd25d-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="cd25d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="cd25d-107">Die letzte geschlossene Arbeitszeile muss ein PUT sein.</span><span class="sxs-lookup"><span data-stu-id="cd25d-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="cd25d-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="cd25d-108">Cause</span></span>

<span data-ttu-id="cd25d-109">Die Arbeit kann in ihrem aktuellen Status nicht storniert werden.</span><span class="sxs-lookup"><span data-stu-id="cd25d-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="cd25d-110">In der letzten Arbeitszeile ist das Feld **Arbeitsstatus** auf *Geschlossen* festgelegt, aber das Feld **Arbeitstyp** ist nicht auf *Put* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cd25d-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="cd25d-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="cd25d-111">Resolution</span></span>

<span data-ttu-id="cd25d-112">Um die Arbeit abzubrechen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="cd25d-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="cd25d-113">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="cd25d-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="cd25d-114">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="cd25d-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="cd25d-115">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd25d-115">Select **OK**.</span></span>
1. <span data-ttu-id="cd25d-116">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="cd25d-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="cd25d-117">Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="cd25d-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
