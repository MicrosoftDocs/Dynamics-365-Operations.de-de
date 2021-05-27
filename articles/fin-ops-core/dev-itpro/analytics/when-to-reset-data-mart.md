---
title: Zeitpunkt für das Zurücksetzen eines Data Mart
description: In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, und die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988991"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="11676-103">Zeitpunkt für das Zurücksetzen eines Data Mart</span><span class="sxs-lookup"><span data-stu-id="11676-103">When to reset a data mart</span></span>

<span data-ttu-id="11676-104">Das Zurücksetzen eines Data Mart kann zeitaufwändig sein.</span><span class="sxs-lookup"><span data-stu-id="11676-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="11676-105">Abhängig von den Umständen ist diese Aktion möglicherweise nicht die passende Lösung.</span><span class="sxs-lookup"><span data-stu-id="11676-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="11676-106">In diesem Thema werden die Umstände aufgeführt, die durch das Zurücksetzen eines Data Mart verbessert werden könnten, sowie die Umstände, unter denen das Zurücksetzen Ihres Data Mart wahrscheinlich nicht hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="11676-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="11676-107">Wann muss ich einen Data Mart zurücksetzen?</span><span class="sxs-lookup"><span data-stu-id="11676-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="11676-108">Stellen Sie sich die folgenden Fragen, bevor Sie einen Data Mart zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="11676-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="11676-109">Wenn Sie eine oder mehrere Fragen mit „Ja“ beantworten, kann dies darauf hinweisen, dass Ihre Organisation vom Zurücksetzen des Data Mart profitieren kann.</span><span class="sxs-lookup"><span data-stu-id="11676-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="11676-110">Wurde die Anwendungsdatenbank wiederhergestellt?</span><span class="sxs-lookup"><span data-stu-id="11676-110">Was the application database restored?</span></span>
- <span data-ttu-id="11676-111">Wenn Sie einen Support-Vorfall eröffnet haben und ein Support-Techniker Sie angewiesen hat, den Data Mart im Rahmen einer Problembehandlung zurückzusetzen?</span><span class="sxs-lookup"><span data-stu-id="11676-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="11676-112">Wann ist es nicht angebracht, einen Data Mart zurückzusetzen?</span><span class="sxs-lookup"><span data-stu-id="11676-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="11676-113">Unter bestimmten Umständen empfehlen wir nicht, einen Data Mart zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="11676-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="11676-114">Im Folgenden finden sind einige Beispiele für solche Umstände.</span><span class="sxs-lookup"><span data-stu-id="11676-114">These include the following.</span></span> 

- <span data-ttu-id="11676-115">Bei Ihnen treten Leistungsprobleme auf, die mit einer Datensynchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="11676-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="11676-116">Aus einem der folgenden Gründe kommt es zum Zurücksetzen mit einem sich wiederholenden Muster:</span><span class="sxs-lookup"><span data-stu-id="11676-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="11676-117">**Fehlende Daten**</span><span class="sxs-lookup"><span data-stu-id="11676-117">**Missing data**</span></span> 
  - <span data-ttu-id="11676-118">**Hängengebliebener Integrationszustand**</span><span class="sxs-lookup"><span data-stu-id="11676-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="11676-119">**Veraltete Datensätze** – Veraltete Datensätze allein rechtfertigen nicht unbedingt das Zurücksetzen des Data Mart.</span><span class="sxs-lookup"><span data-stu-id="11676-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="11676-120">Bei großen Datasets kann das Zurücksetzen einige Zeit dauern. Es ist jedoch unwahrscheinlich, dass es dadurch zu einer Verbesserung kommt.</span><span class="sxs-lookup"><span data-stu-id="11676-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="11676-121">Was ist das Zurücksetzen eines Data Marts?</span><span class="sxs-lookup"><span data-stu-id="11676-121">What is a data mart reset?</span></span>
- <span data-ttu-id="11676-122">Das Zurücksetzen wird erst gestartet, wenn vorhandene Aufgaben abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="11676-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="11676-123">Dadurch wird sichergestellt, dass keine alten Daten eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="11676-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="11676-124">Zu diesem Zeitpunkt wird möglicherweise die folgende Meldung angezeigt: „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="11676-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="11676-125">Bitte versuchen Sie es später erneut.“</span><span class="sxs-lookup"><span data-stu-id="11676-125">Please try again later.”</span></span>
- <span data-ttu-id="11676-126">Durch das Zurücksetzen werden die Integrationsaufgaben deaktiviert und alle Data-Mart-Daten gelöscht.</span><span class="sxs-lookup"><span data-stu-id="11676-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="11676-127">Die Integration wird erneut aktiviert.</span><span class="sxs-lookup"><span data-stu-id="11676-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="11676-128">Verliere ich Berichte, die ich bereits erstellt habe, wenn ich den Data Mart zurücksetze?</span><span class="sxs-lookup"><span data-stu-id="11676-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="11676-129">Nein, Ihre Berichte werden in SQL-Tabellen gespeichert, die von einem Zurücksetzen des Data Mart nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="11676-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="11676-130">Wenn Sie sich Sorgen machen, von Ihnen erstellte Berichte zu verlieren, können Sie eine Sicherungskopien der Designs erstellen, die Sie nicht verlieren möchten.</span><span class="sxs-lookup"><span data-stu-id="11676-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="11676-131">Öffnen Sie dazu den Berichts-Designer und gehen Sie zu **Unternehmen > Unternehmen > Bausteine > Export**.</span><span class="sxs-lookup"><span data-stu-id="11676-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="11676-132">Müssen alle Benutzer das System verlassen, um den Data Mart zurückzusetzen?</span><span class="sxs-lookup"><span data-stu-id="11676-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="11676-133">Nein, Benutzer können während des Zurücksetzens des Data Mart weiter im System arbeiten.</span><span class="sxs-lookup"><span data-stu-id="11676-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="11676-134">Sie können jedoch erst dann auf Berichte zugreifen, die mit Financial Reporter erstellt wurden, wenn das Zurücksetzen abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="11676-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
