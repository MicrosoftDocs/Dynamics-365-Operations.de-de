---
title: Zeitpunkt für das Zurücksetzen eines Data Mart
description: In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, und die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093211"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="74109-103">Zeitpunkt für das Zurücksetzen eines Data Mart</span><span class="sxs-lookup"><span data-stu-id="74109-103">When to reset a data mart</span></span>

<span data-ttu-id="74109-104">Das Zurücksetzen eines Data Mart kann zeitaufwändig sein.</span><span class="sxs-lookup"><span data-stu-id="74109-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="74109-105">Abhängig von den Umständen ist diese Aktion möglicherweise nicht die passende Lösung.</span><span class="sxs-lookup"><span data-stu-id="74109-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="74109-106">In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, sowie die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="74109-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="74109-107">Wann müssen Sie einen Data Mart zurücksetzen?</span><span class="sxs-lookup"><span data-stu-id="74109-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="74109-108">Stellen Sie sich die folgenden Fragen, bevor Sie einen Data Mart zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="74109-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="74109-109">Wenn Sie eine oder mehrere Fragen mit „Ja“ beantworten, kann dies darauf hinweisen, dass Ihre Organisation vom Zurücksetzen des Data Mart profitieren kann.</span><span class="sxs-lookup"><span data-stu-id="74109-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="74109-110">Die Anwendungsdatenbank wurde wiederhergestellt, die Data-Mart-Datenbank jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="74109-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="74109-111">Ihnen werden falsche Daten für eine Buchungsperiode angezeigt, was nicht auf ein Problem mit dem Berichtsdesign zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="74109-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="74109-112">Ihnen werden falsche Daten für eine Buchungsperiode angezeigt und Datensätze werden auf der Seite **Integrationsstatus** im Berichts-Designer unter „Integrationsversuche“ aufgeführt (starten Sie den Berichts-Designer und wählen Sie **Extras > Integrationsstatus** aus).</span><span class="sxs-lookup"><span data-stu-id="74109-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="74109-113">Sie haben einen Support-Vorfall eröffnet und ein Support-Techniker hat Sie angewiesen, den Data Mart im Rahmen einer Problembehandlung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="74109-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="74109-114">Wann ist es nicht angebracht, einen Data Mart zurückzusetzen?</span><span class="sxs-lookup"><span data-stu-id="74109-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="74109-115">Unter bestimmten Umständen empfehlen wir nicht, einen Data Mart zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="74109-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="74109-116">Im Folgenden finden sind einige Beispiele für solche Umstände.</span><span class="sxs-lookup"><span data-stu-id="74109-116">These include the following.</span></span> 

- <span data-ttu-id="74109-117">Der Grund ist in diesem Thema nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="74109-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="74109-118">Es treten Leistungsprobleme im Zusammenhang mit einer Datensynchronisierung auf. Unter diesen Umständen ist das Zurücksetzen des Data Markt vermutlich nicht hilfreich.</span><span class="sxs-lookup"><span data-stu-id="74109-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="74109-119">Aus einem der folgenden Gründe kommt es zum Zurücksetzen mit einem sich wiederholenden Muster:</span><span class="sxs-lookup"><span data-stu-id="74109-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="74109-120">**Fehlende Daten** – Beseitigen Sie zunächst Probleme mit dem Berichtsdesign und dem Timing der Datensynchronisierung. Sie stellen beispielsweise fest, dass die Faktenzuordnung seit dem Buchen fehlender Daten nicht mehr ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="74109-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="74109-121">**Hängengebliebener Integrationsstatus** – Wenn die Integration langsam ist oder scheinbar hängengeblieben ist, lässt sich das Problem durch ein Zurücksetzen des Data Mart vermutlich nicht beheben.</span><span class="sxs-lookup"><span data-stu-id="74109-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="74109-122">**Versuche zum Zurücksetzen waren erfolglos** – Wenn das Zurücksetzen des Data Mart aufgrund fehlender Daten mehrmals nicht erfolgreich war, empfehlen wir, einen Support-Vorfall zu eröffnen und mit einem Support-Techniker zusammenzuarbeiten, um Ihre Situation zu analysieren, bevor Sie erneut versuchen, den Data Mart zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="74109-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="74109-123">**Veraltete Datensätze** – Veraltete Datensätze allein rechtfertigen nicht unbedingt das Zurücksetzen des Data Mart.</span><span class="sxs-lookup"><span data-stu-id="74109-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="74109-124">Bei großen Datasets kann das Zurücksetzen einige Zeit dauern. Es ist jedoch unwahrscheinlich, dass es dadurch zu einer Verbesserung kommt.</span><span class="sxs-lookup"><span data-stu-id="74109-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="74109-125">Was das Zürücksetzen des Data Mart nicht bewirkt</span><span class="sxs-lookup"><span data-stu-id="74109-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="74109-126">Das Zurücksetzen wird erst gestartet, wenn vorhandene Aufgaben abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="74109-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="74109-127">Dadurch wird sichergestellt, dass keine alten Daten eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="74109-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="74109-128">Zu diesem Zeitpunkt wird möglicherweise die folgende Meldung angezeigt: „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="74109-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="74109-129">Bitte versuchen Sie es später erneut.“</span><span class="sxs-lookup"><span data-stu-id="74109-129">Please try again later.”</span></span>
- <span data-ttu-id="74109-130">Durch das Zurücksetzen werden die Integrationsaufgaben deaktiviert und alle Data-Mart-Daten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="74109-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="74109-131">Die Integration wird erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="74109-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="74109-132">Die folgenden Punkte geben zwei Dinge an, die das Zurücksetzen eines Data Mart *nicht* bewirkt.</span><span class="sxs-lookup"><span data-stu-id="74109-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="74109-133">Berichtsentwürfe werden durch das Zurücksetzen nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="74109-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="74109-134">Unternehmensdaten oder Benutzerdaten werden beim Zurücksetzen nicht gelöscht, sofern es nicht ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="74109-134">Resets do not clear company data or user data unless selected.</span></span>
