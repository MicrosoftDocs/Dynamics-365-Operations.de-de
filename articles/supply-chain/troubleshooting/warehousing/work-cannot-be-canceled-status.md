---
title: Arbeit kann nicht storniert werden, weil sie gesperrt ist
description: Arbeit kann nicht storniert werden, weil sie gesperrt ist
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924254"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="6b3de-103">Arbeit kann nicht storniert werden, weil sie gesperrt ist</span><span class="sxs-lookup"><span data-stu-id="6b3de-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="6b3de-104">Fehlercode: WAX2190</span><span class="sxs-lookup"><span data-stu-id="6b3de-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="6b3de-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="6b3de-105">Symptoms</span></span>

<span data-ttu-id="6b3de-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="6b3de-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6b3de-107">Die Arbeit "%1" kann nicht storniert werden, weil sie den Status "%2" aufweist.</span><span class="sxs-lookup"><span data-stu-id="6b3de-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="6b3de-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="6b3de-108">Cause</span></span>

<span data-ttu-id="6b3de-109">Die Arbeit kann in ihrem aktuellen Status nicht storniert werden.</span><span class="sxs-lookup"><span data-stu-id="6b3de-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="6b3de-110">Der Work-Kopf oder die Work-Zeilen haben nicht den erwarteten **Work-Status**-Wert.</span><span class="sxs-lookup"><span data-stu-id="6b3de-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="6b3de-111">Das Feld **Arbeitsstatus** im Arbeitskopf ist nicht auf *Offen* oder *In Bearbeitung* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b3de-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="6b3de-112">Lösung</span><span class="sxs-lookup"><span data-stu-id="6b3de-112">Resolution</span></span>

<span data-ttu-id="6b3de-113">Um die Arbeit abzubrechen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6b3de-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6b3de-114">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="6b3de-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6b3de-115">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="6b3de-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6b3de-116">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b3de-116">Select **OK**.</span></span>
1. <span data-ttu-id="6b3de-117">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="6b3de-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6b3de-118">Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6b3de-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
