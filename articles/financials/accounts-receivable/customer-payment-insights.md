---
title: Debitorenzahlungseinblicke (Vorschau)
description: "In diesem Thema wird beschrieben, wie mithilfe von Debitorenzahlungseinblicken vorhergesagt werden kann, wann eine Rechnung bezahlt wird und wie Organisationen dabei unterstützt werden, optimierte Strategien zu erstellen, die die Wahrscheinlichkeit erhöhen, rechtzeitig bezahlt zu werden."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="customer-payment-insights-preview"></a><span data-ttu-id="30b8e-103">Debitorenzahlungseinblicke (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="30b8e-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="30b8e-104">Diese Funktion ist Teil einer gezielten Version und ist nur für Benutzer verfügbar, die sich für die Private Vorschau entschieden haben.</span><span class="sxs-lookup"><span data-stu-id="30b8e-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="30b8e-105">Diese Funktion wird in einer bevorstehenden allgemeinen Verfügbarkeitsversion einbezogen.</span><span class="sxs-lookup"><span data-stu-id="30b8e-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="30b8e-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="30b8e-106">Overview</span></span>

<span data-ttu-id="30b8e-107">Organisationen finden es oft schwierig vorherzusagen, wann Debitoren ihre Rechnungen zahlen werden.</span><span class="sxs-lookup"><span data-stu-id="30b8e-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="30b8e-108">Dieser fehlende Einblick kann neben ungenauen Cashflowprognosen und ineffektiven Inkassoprozessen dazu führen, dass Aufträge für Debitoren freigegeben werden, deren Kreditwürdigkeit in Frage steht.</span><span class="sxs-lookup"><span data-stu-id="30b8e-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="30b8e-109">Debitorenzahlungseinblicke (Vorschau) verwendet maschinelles Lernen, um vorherzusagen, wann eine Rechnung bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="30b8e-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="30b8e-110">Es bietet auch Optimierungsstrategien, die angepasst werden können, um die Wahrscheinlichkeit zu maximieren, dass Debitoren pünktlich zahlen.</span><span class="sxs-lookup"><span data-stu-id="30b8e-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="30b8e-111">Vorhersagen</span><span class="sxs-lookup"><span data-stu-id="30b8e-111">Predictions</span></span>

<span data-ttu-id="30b8e-112">Zahlungsvorhersagen ermöglichen es Organisationen, ihre Geschäftsprozesse zu verbessern, indem sie bei Folgenden unterstützen:</span><span class="sxs-lookup"><span data-stu-id="30b8e-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="30b8e-113">Rechnungen einfach identifizieren, bei denen eine späte Zahlung vorhergesagt wird.</span><span class="sxs-lookup"><span data-stu-id="30b8e-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="30b8e-114">Geeignete Maßnahmen ergreifen, um die Chancen einer rechtzeitigen Zahlung zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="30b8e-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="30b8e-115">Debitorenzahlungseinblicke (Vorschau) verwendet maschinelles Lernen, um vorherzusagen, wann eine Rechnung bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="30b8e-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="30b8e-116">Es werden Verlaufsdaten zu Rechnung, Zahlung und Debitor verwendet, um ein Modell für maschinelles Lernen zu erstellen, mit dem vorhergesagt werden kann, wann eine Rechnung bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="30b8e-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="30b8e-117">Für jede offene Rechnung prognostiziert Debitorenzahlungseinblicke (Vorschau) drei Zahlungswahrscheinlichkeiten:</span><span class="sxs-lookup"><span data-stu-id="30b8e-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="30b8e-118">Wahrscheinlichkeit einer pünktlichen Zahlung (innerhalb des Rechnungsfälligkeitsdatums).</span><span class="sxs-lookup"><span data-stu-id="30b8e-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="30b8e-119">Wahrscheinlichkeit einer Zahlung innerhalb von 30 Tagen gemäß dem Rechnungsfälligkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="30b8e-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="30b8e-120">Wahrscheinlichkeit einer Zahlung später als 30 Tagen nach dem Rechnungsfälligkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="30b8e-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="30b8e-121">Die Wahrscheinlichkeit von Zahlungen kann im Vorhersageabschnitt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="30b8e-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="30b8e-122">[![Zahlungsvorhersagen](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="30b8e-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="30b8e-123">Jeder Rechnung wird auch eine ausschlaggebende Wahrscheinlichkeit hinsichtlich der Zahlung zugewiesen. Dies geschieht mithilfe einer der drei vorhergesagten Zahlungswahrscheinlichkeitsszenarien, die oben definiert sind.</span><span class="sxs-lookup"><span data-stu-id="30b8e-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="30b8e-124">Das Szenario mit der höchsten Zahlungswahrscheinlichkeit ist das ausschlaggebende Szenario.</span><span class="sxs-lookup"><span data-stu-id="30b8e-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="30b8e-125">Nehmen wir beispielsweise an, dass bei einer Rechnung die Vorhersage eine 71-prozentige Wahrscheinlichkeit anzeigt, dass die Rechnung rechtzeitig bezahlt wird, eine 13-prozentige Wahrscheinlichkeit, dass die Rechnung innerhalb von 30 Tagen nach dem Fälligkeitsdatum bezahlt wird und eine 16-prozentige Wahrscheinlichkeit, dass die Rechnung über 30 Tage nach dem Fälligkeitsdatum bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="30b8e-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="30b8e-126">Die höchste Wahrscheinlichkeit zeigt an, dass sich die Rechnung im Szenario rechtzeitiger Zahlung befindet. Somit wird die Rechnung mit der Wahrscheinlichkeit einer rechtzeitigen Zahlung markiert.</span><span class="sxs-lookup"><span data-stu-id="30b8e-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="30b8e-127">[![Zahlungsvorhersagen](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="30b8e-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="30b8e-128">Optimierungsstrategien</span><span class="sxs-lookup"><span data-stu-id="30b8e-128">Optimization strategies</span></span>

<span data-ttu-id="30b8e-129">Neben Zahlungsvorhersagen, können die Debitorenzahlungseinblicke (Vorschau) Optimierungsstrategien verwenden, um die Wahrscheinlichkeit einer rechtzeitigen Zahlung zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="30b8e-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="30b8e-130">Dies ermöglicht es Organisationen, „What If”-Analysen durchzuführen, indem Benutzer die Möglichkeit haben, Rechnungs- und Debitorenparameter zu ändern und dann die entsprechende Wirkung auf die Wahrscheinlichkeit zu vergleichen, rechtzeitig die Zahlung der Rechnung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="30b8e-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="30b8e-131">Beispielsweise möchte eine Organisation unter Umständen die Auswirkung der Aktualisierung des Skontos bei Rechnungen auf die Wahrscheinlichkeit einer rechtzeitigen Zahlung bewerten.</span><span class="sxs-lookup"><span data-stu-id="30b8e-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="30b8e-132">Wenn die Rechnungen optimiert werden, um den neuen Rabatt zu verwenden, können die Benutzer die Auswirkungen der Anwendung des Rabatts auf die Wahrscheinlichkeit überprüfen, Zahlungen für diese Rechnungen pünktlich zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="30b8e-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="30b8e-133">Wenn die Kosten der Anwendung des Rabatts minimal sind im Vergleich zum Vorteil, die Zahlung rechtzeitig zu beziehen, entscheidet sich die Organisation möglicherweise dafür, den ausgewählten Rabatt auf alle zukünftigen offenen Aufträge anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="30b8e-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="30b8e-134">Aktuell ist nur ein Rabatt als Optimierungsstrategie für Debitorenzahlungseinblicke (Vorschau) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30b8e-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="30b8e-135">[![Optimierte Vorhersagen](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="30b8e-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="30b8e-136">Wie beziehe ich Debitorenzahlungseinblicke (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="30b8e-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="30b8e-137">Wenn Sie daran interessiert sind, Debitorenzahlungseinblicke (Vorschau) auszuprobieren, senden Sie eine E-Mail an [Finance Insights-Vorschauversionsteam](mailto:fiap@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="30b8e-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="30b8e-138">Datenschutzerklärung</span><span class="sxs-lookup"><span data-stu-id="30b8e-138">Privacy Statement</span></span>

<span data-ttu-id="30b8e-139">Vorschauversionen speichern Debitorendaten in den USA.</span><span class="sxs-lookup"><span data-stu-id="30b8e-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="30b8e-140">Darüber hinaus verwenden Vorschauen (1) möglicherweise weniger Datenschutz- und Sicherheitsmaßnamen als der Dynamics 365 for Finance and Operations-Service, (2) sie sind nicht in der Vereinbarung zum Servicelevel für diesen Service enthalten, (3) sie sollten nicht dazu verwendet werden, personenbezogene Daten oder andere Daten zu verwenden, die rechtlichen oder gesetzlich vorgeschriebenen Konformitätsanforderungen unterliegen und (4) es besteht ein eingeschränkter Support.</span><span class="sxs-lookup"><span data-stu-id="30b8e-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>

