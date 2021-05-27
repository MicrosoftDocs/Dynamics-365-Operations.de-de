---
title: Leistung der Steuerberechnung beeinflusst Transaktionen
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die sich auf die Leistung der Steuerberechnung und ihre Auswirkungen auf Transaktionen beziehen.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020138"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="49976-103">Leistung der Steuerberechnung beeinflusst Transaktionen</span><span class="sxs-lookup"><span data-stu-id="49976-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49976-104">Manchmal ist eine Transaktion von Leistungsproblemen betroffen, die bei der Steuerberechnung auftreten.</span><span class="sxs-lookup"><span data-stu-id="49976-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="49976-105">Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="49976-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="49976-106">Überprüfen Sie die Zeilenzahl der Transaktion</span><span class="sxs-lookup"><span data-stu-id="49976-106">Review the transaction line count</span></span>

<span data-ttu-id="49976-107">Ermitteln Sie, ob die Transaktion eine große Anzahl von Zeilen hat (z. B. mehr als mehrere hundert).</span><span class="sxs-lookup"><span data-stu-id="49976-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="49976-108">Wenn das nicht der Fall ist, fahren Sie mit dem nächsten Abschnitt fort.</span><span class="sxs-lookup"><span data-stu-id="49976-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="49976-109">Wenn die Transaktion mehrere hundert Zeilen hat, verzögern Sie die Steuerberechnung.</span><span class="sxs-lookup"><span data-stu-id="49976-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="49976-110">Weitere Informationen finden Sie unter [Verzögerte Steuerberechnung für Erfassungen aktivieren](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="49976-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="49976-111">Als nächstes können Sie feststellen, ob eine der folgenden Bedingungen erfüllt ist:</span><span class="sxs-lookup"><span data-stu-id="49976-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="49976-112">Es gibt Import-Transaktionen aus großen Dateien.</span><span class="sxs-lookup"><span data-stu-id="49976-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="49976-113">Mehrere Sitzungen verarbeiten die gleiche Transaktion Steuerberechnung zur gleichen Zeit.</span><span class="sxs-lookup"><span data-stu-id="49976-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="49976-114">Die Transaktion hat mehrere Zeilen, und die Ansichten werden in Echtzeit aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="49976-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="49976-115">Zum Beispiel wird das Feld **Berechneter Mehrwertsteuerbetrag** auf der Seite **Allgemeines Journal** in Echtzeit aktualisiert, wenn die Felder einer Zeile geändert werden.</span><span class="sxs-lookup"><span data-stu-id="49976-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="49976-116">[![Feld „Berechneter Mehrwertsteuer-Betrag“ auf der Journal-Belegseite](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="49976-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="49976-117">Wenn eine dieser Bedingungen erfüllt ist, verzögern Sie die Steuerberechnung.</span><span class="sxs-lookup"><span data-stu-id="49976-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="49976-118">Überprüfen Sie den Call-Stack</span><span class="sxs-lookup"><span data-stu-id="49976-118">Review the call stack</span></span>

<span data-ttu-id="49976-119">Überprüfen Sie den Call-Stack, um festzustellen, ob die Steuerberechnung mehrfach aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="49976-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="49976-120">Wenn dies nicht der Fall ist, fahren Sie mit dem nächsten Abschnitt fort.</span><span class="sxs-lookup"><span data-stu-id="49976-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="49976-121">Wenn der Call-Stack mehrfach aufgerufen wird, befolgen Sie diese Schritte, um die Steuerberechnungszeiten zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="49976-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="49976-122">Wenn die Erfassung die Transaktion berücksichtigt hat, verzögern Sie die Steuerberechnung.</span><span class="sxs-lookup"><span data-stu-id="49976-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="49976-123">Weitere Informationen finden Sie unter [Verzögerte Steuerberechnung für Erfassungen aktivieren](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="49976-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="49976-124">Wenn es sich bei der Transaktion um eine Bestellung handelt und die Anwendungsversion höher als 10.0.15 ist, können Sie die Steuerberechnung bis zur endgültigen Berechnung verzögern, indem Sie die Versionsverwaltung für **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="49976-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="49976-125">Überprüfen Sie die Call-Stack-Zeitleiste</span><span class="sxs-lookup"><span data-stu-id="49976-125">Review the call stack timeline</span></span>

<span data-ttu-id="49976-126">Überprüfen Sie die Call-Stack-Zeitleiste, um festzustellen, ob die folgenden Probleme bestehen.</span><span class="sxs-lookup"><span data-stu-id="49976-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="49976-127">Wenn dies der Fall ist, aktivieren Sie das Fluging für **TaxUncommittedDoIsolateScopeFlighting**, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="49976-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="49976-128">Die Transaktion bewirkt, dass das System nicht mehr reagiert, bis die Sitzung beendet ist.</span><span class="sxs-lookup"><span data-stu-id="49976-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="49976-129">Daher kann die Transaktion das steuerliche Ergebnis nicht berechnen.</span><span class="sxs-lookup"><span data-stu-id="49976-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="49976-130">Die folgende Abbildung zeigt das Nachrichtenfeld „Sitzung beendet“, das Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="49976-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="49976-131">[![Nachricht „Sitzung beendet“](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="49976-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="49976-132">Die Methoden **TaxUncommitted** benötigen mehr Zeit als andere Methoden.</span><span class="sxs-lookup"><span data-stu-id="49976-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="49976-133">In der folgenden Abbildung benötigt z. B. die Methode **TaxUncommitted ::updateTaxUncommitted()** 43.347,42 Sekunden, aber andere Methoden benötigen 0,09 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="49976-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="49976-134">[![Dauer der Methode](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="49976-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="49976-135">Anpassen und Aufruf der Steuerberechnung</span><span class="sxs-lookup"><span data-stu-id="49976-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="49976-136">Wenn Sie eine Anpassung vornehmen, rufen Sie die Steuerberechnung nicht bei der Methode **insert()** oder **update()** für jede Zeile auf.</span><span class="sxs-lookup"><span data-stu-id="49976-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="49976-137">Die Steuerberechnung sollte auf Transaktionsebene aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="49976-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="49976-138">Ermitteln Sie, ob eine Anpassung vorliegt</span><span class="sxs-lookup"><span data-stu-id="49976-138">Determine whether customization exists</span></span>

<span data-ttu-id="49976-139">Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="49976-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="49976-140">Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.</span><span class="sxs-lookup"><span data-stu-id="49976-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
