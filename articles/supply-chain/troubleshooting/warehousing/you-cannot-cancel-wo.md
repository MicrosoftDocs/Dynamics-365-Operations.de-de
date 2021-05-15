---
title: Sie können keine Arbeit stornieren, die auf einem Benutzer liegt
description: Sie können keine Arbeit stornieren, die auf einem Benutzer liegt
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924400"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="6ac77-103">Sie können keine Arbeit stornieren, die auf einem Benutzer liegt</span><span class="sxs-lookup"><span data-stu-id="6ac77-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="6ac77-104">Fehlercode: WAX708</span><span class="sxs-lookup"><span data-stu-id="6ac77-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="6ac77-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="6ac77-105">Symptoms</span></span>

<span data-ttu-id="6ac77-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="6ac77-106">The system shows the following error message:</span></span>

> <span data-ttu-id="6ac77-107">Sie können keine Arbeit stornieren, die einem Benutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6ac77-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="6ac77-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="6ac77-108">Cause</span></span>

<span data-ttu-id="6ac77-109">Die Arbeit ist von einem Benutzer gesperrt und kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="6ac77-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="6ac77-110">Um dies zu bestätigen, öffnen Sie die Arbeits-ID und dann die Registerkarte **Allgemein**. Wenn die Arbeit gesperrt ist, wird das Feld **Arbeitsstatus** auf *In Bearbeitung* festgelegt und das Feld **Gesperrt durch** auf eine Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="6ac77-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ac77-111">Lösung</span><span class="sxs-lookup"><span data-stu-id="6ac77-111">Resolution</span></span>

<span data-ttu-id="6ac77-112">Um die Arbeit abzubrechen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="6ac77-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="6ac77-113">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Aufräumen \> Arbeit stornieren**.</span><span class="sxs-lookup"><span data-stu-id="6ac77-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="6ac77-114">Geben Sie im Feld **Arbeits-ID** die ID der Arbeit an, die Sie abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="6ac77-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="6ac77-115">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ac77-115">Select **OK**.</span></span>
1. <span data-ttu-id="6ac77-116">Wählen Sie **Ja**, um zu bestätigen, dass Sie die Arbeit abbrechen wollen.</span><span class="sxs-lookup"><span data-stu-id="6ac77-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="6ac77-117">Weitere Informationen finden Sie unter [Stornieren von Lagerort-Arbeiten zur Ausnahmebehandlung](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="6ac77-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
