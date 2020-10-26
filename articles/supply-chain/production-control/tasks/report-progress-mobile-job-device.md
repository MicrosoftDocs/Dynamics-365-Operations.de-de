---
title: Status auf einem mobilen Einzelvorgangsgerät melden
description: Dieses Verfahren zeigt Ihnen an, wie Sie den Fortschritt zu einem Produktions-Einzelvorgang im Formular Einzelvorgangsgerätregistrierung" starten und anzeigen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm, JmgRegistrationTouchReportProgress, JmgFeedbackWizard, JmgJobBundleProdFeedback
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34067902f05546b5c420feca633f77f16033ed2c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983891"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="3d26c-103">Status auf einem mobilen Einzelvorgangsgerät melden</span><span class="sxs-lookup"><span data-stu-id="3d26c-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d26c-104">Dieses Verfahren zeigt Ihnen an, wie Sie den Fortschritt zu einem Produktions-Einzelvorgang im Formular Einzelvorgangsgerätregistrierung" starten und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d26c-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="3d26c-105">Damit Sie dieses Verfahren ausführen können, muss die Rolle Systemadministator oder Maschinist zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="3d26c-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="3d26c-106">Wechseln Sie zu Produktionssteuerung > Fertigungssteuerung > Einzelvorgangslistengerät.</span><span class="sxs-lookup"><span data-stu-id="3d26c-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="3d26c-107">Wählen Sie im Feld "WorkerTextField" die Kennkarte einer Arbeitskraft aus.</span><span class="sxs-lookup"><span data-stu-id="3d26c-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="3d26c-108">Im USMF-Demodattyp ist dies "123" für Christina Portra.</span><span class="sxs-lookup"><span data-stu-id="3d26c-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="3d26c-109">Klicken sie auf "Anmelden".</span><span class="sxs-lookup"><span data-stu-id="3d26c-109">Click Log in.</span></span>
4. <span data-ttu-id="3d26c-110">Klicken Sie auf die Schaltfläche "Filter".</span><span class="sxs-lookup"><span data-stu-id="3d26c-110">Click the Filter button.</span></span>
5. <span data-ttu-id="3d26c-111">Aktivieren oder deaktivieren Sie das Kontrollkästchen "Konfigurationsfilter anwenden".</span><span class="sxs-lookup"><span data-stu-id="3d26c-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="3d26c-112">Wenn Sie einen Filter festgelegt, können Sie die Produktionseinheit 110 in USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="3d26c-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="3d26c-113">Wählen Sie im Feld "Produktionseinheit" die Ressourcengruppen aus, für deren Produktionseinzelvorgänge die Arbeitskraft arbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="3d26c-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="3d26c-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3d26c-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3d26c-115">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d26c-115">Click OK.</span></span>
9. <span data-ttu-id="3d26c-116">Klicken Sie auf die Schaltfläche "Einzelvorgang starten".</span><span class="sxs-lookup"><span data-stu-id="3d26c-116">Click the Start job button.</span></span>
10. <span data-ttu-id="3d26c-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d26c-117">Click OK.</span></span>
11. <span data-ttu-id="3d26c-118">Klicken Sie auf die Schaltfläche "Fortschritt melden".</span><span class="sxs-lookup"><span data-stu-id="3d26c-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="3d26c-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d26c-119">Click OK.</span></span>
13. <span data-ttu-id="3d26c-120">Klicken Sie auf die Schaltfläche "Nächster Einzelvorgang".</span><span class="sxs-lookup"><span data-stu-id="3d26c-120">Click the Next job button.</span></span>
14. <span data-ttu-id="3d26c-121">Klicken Sie auf die Schaltfläche "Zugewiesen", um eine Übersicht aller Produktions-Einzelvorgänge anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d26c-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="3d26c-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3d26c-122">Close the page.</span></span>
16. <span data-ttu-id="3d26c-123">Klicken Sie auf die Schaltfläche "Pause".</span><span class="sxs-lookup"><span data-stu-id="3d26c-123">Click the Break button.</span></span>
17. <span data-ttu-id="3d26c-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3d26c-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="3d26c-125">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d26c-125">Click OK.</span></span>
19. <span data-ttu-id="3d26c-126">Klicken Sie auf die Schaltfläche "Beenden".</span><span class="sxs-lookup"><span data-stu-id="3d26c-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="3d26c-127">Wählen Sie abmelden aus.</span><span class="sxs-lookup"><span data-stu-id="3d26c-127">Select to log out.</span></span>
21. <span data-ttu-id="3d26c-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d26c-128">Click OK.</span></span>
22. <span data-ttu-id="3d26c-129">Melden Sie sich im Feld "WorkerTextField" erneut an.</span><span class="sxs-lookup"><span data-stu-id="3d26c-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="3d26c-130">In den USMF-Demodaten können Sie Arbeitskraft "123" auswählen.</span><span class="sxs-lookup"><span data-stu-id="3d26c-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="3d26c-131">Klicken sie auf "Anmelden".</span><span class="sxs-lookup"><span data-stu-id="3d26c-131">Click Log in.</span></span>
24. <span data-ttu-id="3d26c-132">Klicken Sie auf "Pause stoppen".</span><span class="sxs-lookup"><span data-stu-id="3d26c-132">Click Stop break.</span></span>
25. <span data-ttu-id="3d26c-133">Klicken Sie auf die Schaltfläche "Aktivität".</span><span class="sxs-lookup"><span data-stu-id="3d26c-133">Click the Activity button.</span></span>
26. <span data-ttu-id="3d26c-134">Klicken Sie auf "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="3d26c-134">Click Cancel.</span></span>
27. <span data-ttu-id="3d26c-135">Klicken Sie auf die Schaltfläche "Beenden".</span><span class="sxs-lookup"><span data-stu-id="3d26c-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="3d26c-136">Wählen Sie "Ausstempeln" aus.</span><span class="sxs-lookup"><span data-stu-id="3d26c-136">Select to clock out.</span></span>
29. <span data-ttu-id="3d26c-137">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3d26c-137">Click OK.</span></span>
30. <span data-ttu-id="3d26c-138">Wählen Sie eine Ursache für das frühzeitige Ausstempeln.</span><span class="sxs-lookup"><span data-stu-id="3d26c-138">Select a reason why you are clocking out early.</span></span>

