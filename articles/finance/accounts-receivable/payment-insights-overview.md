---
title: Debitorenzahlungseinblicke (Vorschau)
description: Dieses Thema beschreibt die Fähigkeit zur Zahlungseinsicht, die dazu beiträgt, das Verständnis für die typischen Zahlungspraktiken einzelner Kunden zu verbessern und Umstände zu identifizieren, die es rechtfertigen, Inkassoprozesse früher einzuleiten, als Sie es sonst getan haben.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773962"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="7db17-103">Debitorenzahlungseinblicke (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="7db17-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7db17-104">Dieses Thema beschreibt die Fähigkeit zur Zahlungseinsicht, die dazu beiträgt, das Verständnis für die typischen Zahlungspraktiken einzelner Kunden zu verbessern und Umstände zu identifizieren, die es rechtfertigen, Inkassoprozesse früher einzuleiten, als Sie es sonst hätten tun können.</span><span class="sxs-lookup"><span data-stu-id="7db17-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="7db17-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7db17-105">Overview</span></span>

<span data-ttu-id="7db17-106">Unternehmen finden es oft schwierig, vorherzusagen, wann Kunden ihre Rechnungen bezahlen werden.</span><span class="sxs-lookup"><span data-stu-id="7db17-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="7db17-107">Dieser Mangel an Erkenntnissen führt zu weniger genauen Cashflow-Prognosen, zu zu spät einsetzenden Inkassoprozessen und zu Aufträgen, die an Kunden freigegeben werden, die möglicherweise mit ihrer Zahlung in Verzug geraten.</span><span class="sxs-lookup"><span data-stu-id="7db17-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="7db17-108">Debitorenzahlungseinblicke (Vorschau) helfen Unternehmen bei der Vorhersage, wann eine Kundenrechnung bezahlt wird, und helfen Unternehmen bei der Erstellung von Inkassostrategien, die die Wahrscheinlichkeit erhöhen, rechtzeitig bezahlt zu werden.</span><span class="sxs-lookup"><span data-stu-id="7db17-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="7db17-109">Vorhersagen</span><span class="sxs-lookup"><span data-stu-id="7db17-109">Predictions</span></span>

<span data-ttu-id="7db17-110">Zahlungsvorhersagen werden es Unternehmen ermöglichen, ihre Geschäftsprozesse zu verbessern, indem sie ihnen helfen, die Rechnungen, die wahrscheinlich verspätet bezahlt werden, leicht zu identifizieren und geeignete Maßnahmen zu ergreifen, die ihre Chancen verbessern, rechtzeitig bezahlt zu werden.</span><span class="sxs-lookup"><span data-stu-id="7db17-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="7db17-111">Mithilfe eines maschinellen Lernmodells, das historische Rechnungen, Zahlungen und Kundendaten nutzt, prognostiziert der Debitorenzahlungseinblicke (Vorschau) genauer, wann ein Kunde eine ausstehende Rechnung bezahlen wird.</span><span class="sxs-lookup"><span data-stu-id="7db17-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="7db17-112">Für jede offene Rechnung prognostiziert Debitorenzahlungseinblicke (Vorschau) drei Zahlungswahrscheinlichkeiten:</span><span class="sxs-lookup"><span data-stu-id="7db17-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="7db17-113">Wahrscheinlichkeit, dass die Zahlung pünktlich erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7db17-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="7db17-114">Wahrscheinlichkeit, dass die Zahlung verspätet erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7db17-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="7db17-115">Wahrscheinlichkeit, dass die Zahlung sehr spät erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7db17-115">Probability of payment being made very late</span></span>

<span data-ttu-id="7db17-116">Um Unternehmen dabei zu helfen, den gesamten Zahlungsbetrag zu verstehen, den sie von einem Kunden in einem der drei Bereiche On time, late und Very late erwarten können, bietet Debitorenzahlungseinblicke (Vorschau) auch eine aggregierte Ansicht der erwarteten Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="7db17-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="7db17-117">[![Aggregierte Ansicht der Zahlungsvorhersagen](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="7db17-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="7db17-118">Außerdem wird jeder Rechnung eine Zahlungswahrscheinlichkeit zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7db17-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="7db17-119">Wenn die Wahrscheinlichkeit einer rechtzeitigen Zahlung weniger als 50% beträgt, werden die Rechnungen mit einem roten Kreis markiert, um anzuzeigen, dass diese Rechnungen möglicherweise eine Inkassoaufsicht erfordern.</span><span class="sxs-lookup"><span data-stu-id="7db17-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="7db17-120">[![Liste der Zahlungswahrscheinlichkeiten](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="7db17-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="7db17-121">Debitorenzahlungseinblicke (Vorschau) bietet auch Kontextinformationen zur Erläuterung der Vorhersage, wie z.B. die wichtigsten Faktoren, die die Vorhersage beeinflusst haben, den aktuellen Geschäftsgang mit dem Kunden und Details über das historische Zahlungsverhalten des Kunden.</span><span class="sxs-lookup"><span data-stu-id="7db17-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="7db17-122">In vielen Unternehmen war der Inkassoprozess eine reaktive Tätigkeit; der Inkassoprozess beginnt erst mit der Fälligkeit der Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="7db17-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="7db17-123">Mit Debitorenzahlungseinblicke (Vorschau) können Unternehmen proaktiver mit dem Inkasso umgehen.</span><span class="sxs-lookup"><span data-stu-id="7db17-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="7db17-124">Sie müssen nicht mehr darauf warten, dass die Transaktionen fällig werden, um den Inkassoprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="7db17-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="7db17-125">Stattdessen können sie die Fähigkeit zur Zahlungsvorhersage nutzen, um festzustellen, ob proaktive Inkassi die Wahrscheinlichkeit verbessern, rechtzeitig bezahlt zu werden.</span><span class="sxs-lookup"><span data-stu-id="7db17-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="7db17-126">Die Zahlungsvorhersage liefert den Unternehmen auch die Informationen, die sie benötigen, um den frühzeitigen Beginn des Inkassoverfahrens zu rechtfertigen.</span><span class="sxs-lookup"><span data-stu-id="7db17-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="7db17-127">Methodik</span><span class="sxs-lookup"><span data-stu-id="7db17-127">Methodology</span></span>

<span data-ttu-id="7db17-128">Die Entwicklung und Bereitstellung einer KI-Lösung ist schwierig.</span><span class="sxs-lookup"><span data-stu-id="7db17-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="7db17-129">Ein Team von Datenwissenschaftlern, Fachexperten und Ingenieuren arbeitet über einen längeren Zeitraum an der Formulierung, Entwicklung, Bereitstellung und Wartung einer brauchbaren KI-Lösung.</span><span class="sxs-lookup"><span data-stu-id="7db17-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="7db17-130">Wir machen es Ihnen leicht, KI-Lösungen in Finance einzusetzen und zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="7db17-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="7db17-131">Wir bieten KI-Lösungen in Finance an, die auf Microsoft AI Builder basieren.</span><span class="sxs-lookup"><span data-stu-id="7db17-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="7db17-132">Ein Endbenutzer kann mit nur einem Klick die KI-Lösung bereitstellen und die Vorteile intelligenter Prognosen nutzen.</span><span class="sxs-lookup"><span data-stu-id="7db17-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="7db17-133">Wenn ein Unternehmen mit der Genauigkeit von Vorhersagen nicht zufrieden ist, kann ein Power-User, wiederum mit einem einzigen Klick, die Erweiterung von AI Builder aufrufen und dann die Felder auswählen oder abwählen, die zur Erstellung von Vorhersagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7db17-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="7db17-134">Sobald sie bereit sind, können sie die Änderungen trainieren und veröffentlichen, und das neu trainierte Modell wird automatisch für Prognosen zu Finance übernommen.</span><span class="sxs-lookup"><span data-stu-id="7db17-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="7db17-135">So erhalten Sie Debitorenzahlungseinblicke (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="7db17-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="7db17-136">Bitte senden Sie eine E-Mail an [Debitorenzahlungseinblicke (Vorschau)](mailto:fiap@microsoft.com), wenn Sie daran interessiert sind, die Debitorenzahlungseinblicke (Vorschau) auszuprobieren.</span><span class="sxs-lookup"><span data-stu-id="7db17-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="7db17-137">Datenschutzhinweis</span><span class="sxs-lookup"><span data-stu-id="7db17-137">Privacy Notice</span></span>

<span data-ttu-id="7db17-138">Vorschauen (1) können weniger Datenschutz- und Sicherheitsmaßnahmen anwenden als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.</span><span class="sxs-lookup"><span data-stu-id="7db17-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


