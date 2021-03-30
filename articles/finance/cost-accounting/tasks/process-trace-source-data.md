---
title: Quelldaten verarbeiten und nachverfolgen
description: Die Datenverarbeitung wird über Einzelvorgänge ausgeführt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12137c0d82109a8b757df6f6990922994d49c71a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208654"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="62342-103">Quelldaten verarbeiten und nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="62342-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62342-104">Die Datenverarbeitung wird über Einzelvorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62342-104">All data processing is run by jobs.</span></span> <span data-ttu-id="62342-105">Für jeden Einzelvorgang und Datenanbieter wird eine Erfassung zum Dokument erstellt, dass der Prozess ausgeführt wurde und die Einträge im aktuellen Einzelvorgang verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="62342-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="62342-106">Gehen Sie folgendermaßen vor, um einer Datenquelle einzurichten und die Grundlage eines bestimmten Erfassung verfolgen Kosten.</span><span class="sxs-lookup"><span data-stu-id="62342-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="62342-107">Für diese Aufzeichnung wird das USP2 Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="62342-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="62342-108">Bevor Sie diese Aufgabe abschließen, prüfen Sie, ob Sie ein Kostenrechnungssachkonto den "Erstellen "und" Kostenkontrollesteuereinheits" besetzen Aufgabenleitfäden definieren.</span><span class="sxs-lookup"><span data-stu-id="62342-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="62342-109">Wechseln Sie zu Kostenbuchhaltung > Sachkontoeinstellung > Kostenbuchhaltungs-Sachkonto .</span><span class="sxs-lookup"><span data-stu-id="62342-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="62342-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="62342-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62342-111">Wählen Sie das Kostenrechnungssachkonto aus, das Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="62342-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="62342-112">Tatsächliche Versionen anklicken.</span><span class="sxs-lookup"><span data-stu-id="62342-112">Click Actual versions.</span></span>
4. <span data-ttu-id="62342-113">Wählen Sie eine Ressource aus, und klicken Sie im Aktivitätsbereich auf .</span><span class="sxs-lookup"><span data-stu-id="62342-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="62342-114">Umlagerungserfassungseinträge im Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="62342-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="62342-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="62342-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="62342-116">Journaleinträge anklicken</span><span class="sxs-lookup"><span data-stu-id="62342-116">Click Journal entries.</span></span>
8. <span data-ttu-id="62342-117">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="62342-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="62342-118">Klicken Sie auf "Kosteneinträge".</span><span class="sxs-lookup"><span data-stu-id="62342-118">Click Cost entries.</span></span>
10. <span data-ttu-id="62342-119">Quelleneintrag anklicken.</span><span class="sxs-lookup"><span data-stu-id="62342-119">Click Source entry.</span></span>
11. <span data-ttu-id="62342-120">Wählen Sie eine Ressource aus, und klicken Sie im Aktivitätsbereich auf .</span><span class="sxs-lookup"><span data-stu-id="62342-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="62342-121">Hauptbuch anklicken.</span><span class="sxs-lookup"><span data-stu-id="62342-121">Click General ledger.</span></span>
13. <span data-ttu-id="62342-122">Geben Sie im Feld "Steuerperiode" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="62342-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="62342-123">In vorliegenden Beispiel wählen Sie Steuer 2017 Periode 9 aus.</span><span class="sxs-lookup"><span data-stu-id="62342-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="62342-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="62342-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]