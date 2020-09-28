---
title: Leistung der Projektressourcenplanung
description: Dieses Thema enthält Informationen zur Verbesserung der Leistung der Ressourcenplanung für eine große Anzahl von Projekten.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760559"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="47d08-103">Leistung der Projektressourcenplanung</span><span class="sxs-lookup"><span data-stu-id="47d08-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="47d08-104">Leistungsprobleme im Zusammenhang mit der Ressourcenplanung können auftreten, wenn die Anzahl der Projekte Tausende beträgt.</span><span class="sxs-lookup"><span data-stu-id="47d08-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="47d08-105">Um die Leistung der Ressourcenplanung zu verbessern, steht eine Funktion zur Verfügung, mit der Benutzer die Zeit reduzieren können, die zum Starten des Ressourcenverfügbarkeitsformulars erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="47d08-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="47d08-106">Dies entfernt insbesondere den Rollup-Synchronisierungsprozess für die Ressourcenkapazität und verwendet die **ResProjectResource**-Tabelle, um die Ressourcensuche zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="47d08-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="47d08-107">Beachten Sie, dass die **ResRollup**-Tabelle nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47d08-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47d08-108">Bei einer Abhängigkeit vom Rollup-Synchronisierungsprozess der Ressourcenkapazität oder von der **ResProjectResource**-Tabelle verwenden Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="47d08-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="47d08-109">Aktivieren der Leistungsverbesserung bei der Ressourcenplanung</span><span class="sxs-lookup"><span data-stu-id="47d08-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="47d08-110">Führen Sie die folgenden Schritte aus, um die Leistungsverbesserung bei der Ressourcenplanung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="47d08-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="47d08-111">Wechseln Sie zu **Funktionsverwaltung** > **Alle** und suchen Sie in der Funktionsliste nach **Funktion zum Aktivieren der Leistungsverbesserung bei der Ressourcenplanung**.</span><span class="sxs-lookup"><span data-stu-id="47d08-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="47d08-112">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="47d08-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="47d08-113">Wenn Sie die Funktion in der Liste nicht finden können, wählen Sie **Auf Updates prüfen**, um die Liste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="47d08-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="47d08-114">Aktualisieren Sie Ihren Browser und wechseln Sie dann zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Projektressourcen** > **Kapazität für Kalender und Ressourcen in allen Unternehmen synchronisieren** .</span><span class="sxs-lookup"><span data-stu-id="47d08-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="47d08-115">Legen Sie **Vorhandene Kapazitätsdatensätze entfernen** auf **Ja** fest, um vorherige Daten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="47d08-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="47d08-116">Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese Option auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="47d08-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="47d08-117">wählen Sie im Feld **Periodencode** den Zeitraum aus, in dem Daten generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47d08-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="47d08-118">Wenn Sie einen Periodencode auswählen, müssen kein Start- und Enddatum definiert werden.</span><span class="sxs-lookup"><span data-stu-id="47d08-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="47d08-119">Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie bestimmte Start- und Enddaten aus, um Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="47d08-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="47d08-120">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="47d08-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="47d08-121">Dadurch werden allgemeine Daten in allen Unternehmen in Ihrer Umgebung an die **ResCalendarCapacity**-Tabelle verteilt sodass der Batch-Auftrag nur in einer juristischen Person ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="47d08-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="47d08-122">Die Daten in diesem Batch-Auftrag werden benötigt, um die Ressourcenkapazität für den zugehörigen Kalender zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="47d08-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="47d08-123">Wechseln Sie zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Projektressourcen** > **Projektressourcen in allen Unternehmen füllen** und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="47d08-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="47d08-124">Dies ist das Datenaktualisierungsskript für allgemeine Daten in den Tabellen **ResProjectResource**, **ResCalendarDateTimeRange** und **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="47d08-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="47d08-125">Werte für das **PSAPRojSchedRole.RootActivity**-Feld werden ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="47d08-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="47d08-126">Wenn dies nicht ausgeführt wird, erhalten Sie eine Warnung, wenn Sie versuchen, Ressourcenplanungsvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="47d08-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="47d08-127">Ausschalten der Leistungsverbesserung bei der Ressourcenplanung</span><span class="sxs-lookup"><span data-stu-id="47d08-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="47d08-128">Wechseln Sie zu **Funktionsverwaltung** > **Alle** und suchen Sie nach **Funktion zum Aktivieren der Leistungsverbesserung bei der Ressourcenplanung**.</span><span class="sxs-lookup"><span data-stu-id="47d08-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="47d08-129">Wählen Sie die Funktion aus und wählen Sie dann die **Deaktivieren**-Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="47d08-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="47d08-130">Aktualisieren Sie Ihren Browser.</span><span class="sxs-lookup"><span data-stu-id="47d08-130">Refresh your browser.</span></span>
4. <span data-ttu-id="47d08-131">Wechseln Sie zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Kapazitätssynchronisierung** > **Ressourcenkapazitätszusammenfassungen synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="47d08-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="47d08-132">Auf der **Synchronisation der Kapazitätszusammenfassung**-Seite, setzen Sie **Vorhandene Kapazitätsdatensätze entfernen** auf **Ja**, um vorherige Daten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="47d08-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="47d08-133">Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese Option auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="47d08-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="47d08-134">wählen Sie im Feld **Periodencode** den Zeitraum aus, in dem Daten generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47d08-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="47d08-135">Wenn Sie einen Periodencode auswählen, müssen kein Start- und Enddatum definiert werden.</span><span class="sxs-lookup"><span data-stu-id="47d08-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="47d08-136">Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie bestimmte Start- und Enddaten aus, um Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="47d08-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="47d08-137">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="47d08-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="47d08-138">Dadurch werden allgemeine Daten in allen Unternehmen in Ihrer Umgebung an die **ResRollup**-Tabelle verteilt sodass der Batch-Auftrag nur in einer juristischen Person ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="47d08-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="47d08-139">Dieser Batch-Auftrag wird für alle **Ressourcenverfügbarkeit**-Ansichten benötigt.</span><span class="sxs-lookup"><span data-stu-id="47d08-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="47d08-140">Wenn dieser Batch-Auftrag nicht ausgeführt wird, werden die **ResRollup**-Daten im laufenden Betrieb generiert, was einige Zeit dauern kann.</span><span class="sxs-lookup"><span data-stu-id="47d08-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
