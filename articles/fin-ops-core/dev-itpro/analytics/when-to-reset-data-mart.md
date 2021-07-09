---
title: Zurücksetzen von Data Marts FAQ
description: In diesem Thema finden Sie Antworten auf einige häufig gestellte Fragen zum Zurücksetzen des Data Marts.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266608"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="1d84d-103">Zurücksetzen von Data Marts FAQ</span><span class="sxs-lookup"><span data-stu-id="1d84d-103">Data mart resets FAQ</span></span>

<span data-ttu-id="1d84d-104">In diesem Thema finden Sie Antworten auf einige häufig gestellte Fragen zum Zurücksetzen des Data Marts.</span><span class="sxs-lookup"><span data-stu-id="1d84d-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="1d84d-105">Ein Zurücksetzen des Data Mart kann ein zeitaufwändiger Prozess sein und ist je nach den Umständen möglicherweise nicht die Lösung, die benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1d84d-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="1d84d-106">Daher enthält dieses Thema Informationen über Umstände, unter denen ein Data Mart-Reset hilfreich sein kann, und auch über Umstände, unter denen es unwahrscheinlich ist, dass es hilft.</span><span class="sxs-lookup"><span data-stu-id="1d84d-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="1d84d-107">Was ist das Zurücksetzen eines Data Marts?</span><span class="sxs-lookup"><span data-stu-id="1d84d-107">What is a data mart reset?</span></span>

<span data-ttu-id="1d84d-108">Bei einem Data Mart-Reset werden die Integrationsaufgaben deaktiviert, alle Data Mart-Daten gelöscht und anschließend die Integration wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1d84d-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="1d84d-109">Um sicherzustellen, dass keine alten Daten eingefügt werden, kann ein Data Mart-Reset erst dann gestartet werden, wenn bestehende Aufgaben abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="1d84d-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="1d84d-110">Wenn Sie versuchen, den Data Mart zurückzusetzen, bevor alle Aufgaben abgeschlossen sind, erhalten Sie möglicherweise eine Nachricht wie „Das Zurücksetzen des Data Mart konnte aufgrund einer aktiven Aufgabe nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1d84d-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="1d84d-111">Bitte versuchen Sie es später erneut.“</span><span class="sxs-lookup"><span data-stu-id="1d84d-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="1d84d-112">Wann muss ich ein Data Mart-Reset durchführen?</span><span class="sxs-lookup"><span data-stu-id="1d84d-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="1d84d-113">Wenn eine oder mehrere der folgenden Aussagen auf Ihre Situation zutreffen, kann Ihre Organisation von einem Data Mart-Reset profitieren:</span><span class="sxs-lookup"><span data-stu-id="1d84d-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="1d84d-114">Die Anwendungsdatenbank wurde wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="1d84d-114">The application database was restored.</span></span>
- <span data-ttu-id="1d84d-115">Sie haben ein Support-Ticket geöffnet, und ein Support-Techniker hat Sie angewiesen, den Data Mart als Teil einer Fehlerbehebung zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1d84d-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="1d84d-116">Wann ist ein Data Mart-Reset unangebracht?</span><span class="sxs-lookup"><span data-stu-id="1d84d-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="1d84d-117">Im Folgenden sind einige der Umstände aufgeführt, unter denen wir nicht empfehlen, den Data Mart zurückzusetzen:</span><span class="sxs-lookup"><span data-stu-id="1d84d-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="1d84d-118">Sie haben Leistungsprobleme, die mit der Datensynchronisierung zusammenhängen.</span><span class="sxs-lookup"><span data-stu-id="1d84d-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="1d84d-119">Sie haben ein wiederkehrendes Rücksetzungsmuster aus einem der folgenden Gründe:</span><span class="sxs-lookup"><span data-stu-id="1d84d-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="1d84d-120">**Fehlende Daten** – Wenn Sie feststellen, dass Daten fehlen, eröffnen Sie ein Support-Ticket bei Microsoft, um Ihr Berichtsformat und mögliche Probleme bei der Datensynchronisation zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1d84d-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="1d84d-121">**Hängengebliebener Integrationszustand**</span><span class="sxs-lookup"><span data-stu-id="1d84d-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="1d84d-122">**Veraltete Datensätze** – Veraltete Datensätze allein rechtfertigen nicht unbedingt einen Data Mart Reset.</span><span class="sxs-lookup"><span data-stu-id="1d84d-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="1d84d-123">Wenn Sie ein großes Dataset haben, dauert es einige Zeit, bis der Rücksetzungsprozess ausgeführt wird, aber es ist unwahrscheinlich, dass er zu einer Verbesserung führt.</span><span class="sxs-lookup"><span data-stu-id="1d84d-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="1d84d-124">Verliere ich Berichte, die ich bereits erstellt habe, wenn ich den Data Mart zurücksetze?</span><span class="sxs-lookup"><span data-stu-id="1d84d-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="1d84d-125">Nein.</span><span class="sxs-lookup"><span data-stu-id="1d84d-125">No.</span></span> <span data-ttu-id="1d84d-126">Ihre Berichte sind in SQL-Tabellen gespeichert, die von einem Data Mart-Reset nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="1d84d-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="1d84d-127">Wenn Sie befürchten, dass von Ihnen entworfene Berichte verloren gehen, können Sie die Entwürfe, die Sie nicht verlieren möchten, sichern.</span><span class="sxs-lookup"><span data-stu-id="1d84d-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="1d84d-128">Um Designs zu sichern, öffnen Sie den Report Designer und gehen Sie zu **Firma \> Firmen \> Bausteine \> Export**.</span><span class="sxs-lookup"><span data-stu-id="1d84d-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="1d84d-129">Müssen alle Benutzer das System verlassen, bevor ich den Data Mart zurücksetzen kann?</span><span class="sxs-lookup"><span data-stu-id="1d84d-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="1d84d-130">Nein.</span><span class="sxs-lookup"><span data-stu-id="1d84d-130">No.</span></span> <span data-ttu-id="1d84d-131">Die Benutzer können während eines Data Mart-Resets weiter im System arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1d84d-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="1d84d-132">Bis das Zurücksetzen abgeschlossen ist, können die Benutzer jedoch nicht auf Berichte zugreifen, die mit Financial Reporter erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1d84d-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
