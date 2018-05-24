---
title: "Verringern der Tage für Dauerauftragsgebühren"
description: "Sie können zum Verringern der Anzahl von Tagen einer vorhandenen Dauerauftragsgebühr eine neue Buchung zum Entfernen des Zeitraums erstellen, der nicht mehr dem Intervall für die Dauerauftragsgebühr angehören soll."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c70e393c125eecef85e8711d1635250f5ff408d9
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="a68d2-103">Verringern der Tage für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="a68d2-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a68d2-104">Sie können zum Verringern der Anzahl von Tagen einer vorhandenen Dauerauftragsgebühr eine neue Buchung zum Entfernen des Zeitraums erstellen, der nicht mehr dem Intervall für die Dauerauftragsgebühr angehören soll.</span><span class="sxs-lookup"><span data-stu-id="a68d2-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="a68d2-105">Verringern der Tage für eine Dauerauftragsgebühr</span><span class="sxs-lookup"><span data-stu-id="a68d2-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="a68d2-106">Klicken Sie auf **Servicemanagement** \> **Gemeinsam** \> **Daueraufträge** \> **Alle Daueraufträge**.</span><span class="sxs-lookup"><span data-stu-id="a68d2-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="a68d2-107">Wählen Sie den Dauerauftrag aus, und klicken Sie im Aktivitätsbereich auf **Dauerauftragsgebühren**.</span><span class="sxs-lookup"><span data-stu-id="a68d2-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="a68d2-108">Wählen Sie im Feld **Dauerauftragstyp** **Minderungstage** aus.</span><span class="sxs-lookup"><span data-stu-id="a68d2-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="a68d2-109">Geben Sie mithilfe der Felder **Von Datum** und **Bis Datum** das Datumsintervall der Dauerauftragsgebühr ein, das aus der Periode für die Dauerauftragsgebühr entfernt werden soll, und klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a68d2-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="a68d2-110">Klicken Sie zum Anzeigen der erstellten Buchung im Formular **Dauerauftrag** auf  und anschließend auf **Gebührenbuchungen**.</span><span class="sxs-lookup"><span data-stu-id="a68d2-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="a68d2-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a68d2-111">Example</span></span>

<span data-ttu-id="a68d2-112">Angenommen, die Periode einer Dauerauftragsbuchung reicht vom 1. bis zu 31. Januar und soll um 10 Tage verkürzt werden. Erstellen Sie hierzu eine neue Buchung mit einer Verringerungsperiode vom 1. bis zum 10. Januar.</span><span class="sxs-lookup"><span data-stu-id="a68d2-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="a68d2-113">(Die Verringerungsperiode könnte jedoch auch vom 5. bis zum 15. Januar reichen oder einen beliebigen anderen Zeitraum von zehn Tagen umfassen).</span><span class="sxs-lookup"><span data-stu-id="a68d2-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="a68d2-114">Ist dagegen der Wert im Feld **Von Datum** für die Verringerungsperiode auf den 21. Januar festgelegt (also 31 minus 10), kann der Wert für **Bis Datum** auf ein beliebiges Datum nach dem 31 Januar festgelegt werden, und dennoch werden die 10 Tage aus der Gebührenbuchungsperiode entfernt.</span><span class="sxs-lookup"><span data-stu-id="a68d2-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="a68d2-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a68d2-115">See also</span></span>

[<span data-ttu-id="a68d2-116">Minderungstage – Beispiel</span><span class="sxs-lookup"><span data-stu-id="a68d2-116">Reduction days example</span></span>](reduction-days-example.md)

  



