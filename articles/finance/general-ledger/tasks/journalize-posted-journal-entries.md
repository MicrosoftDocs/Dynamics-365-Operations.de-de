---
title: Gebuchte Erfassungseinträge journalisieren
description: Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443504"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="96231-103">Gebuchte Erfassungseinträge journalisieren</span><span class="sxs-lookup"><span data-stu-id="96231-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96231-104">Diese Verfahren zeigt, wie gebuchte Journaleinträge journalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="96231-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="96231-105">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="96231-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="96231-106">Wechseln Sie im **Navigationsbereich** auf **Module > Hauptbuch > Sachkonto-Einstellungen > Hauptbuchparameter**.</span><span class="sxs-lookup"><span data-stu-id="96231-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="96231-107">Das Feld **Erstellte Journale erweitern** kann auf Ja oder Nein festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="96231-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="96231-108">Bei Ja unterscheidet sich die Berichtsausgabe.</span><span class="sxs-lookup"><span data-stu-id="96231-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="96231-109">Wählen Sie aus, ob die Periode abgeschlossen werden kann, wenn der journalisierende Prozess nicht ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="96231-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="96231-110">Ist die Option auf "Ja" festgelegt ist, kann der Zeitraum nicht abgeschlossen werden, bis der Erfassungsprozess für diesen Zeitraum abgeschlossenen wurde.</span><span class="sxs-lookup"><span data-stu-id="96231-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="96231-111">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="96231-111">Close the page.</span></span>
5. <span data-ttu-id="96231-112">Wechseln Sie im **Navigationsbereich** zu **Module > Hauptbuch > Periodische Aufgaben > Journalisierung**.</span><span class="sxs-lookup"><span data-stu-id="96231-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="96231-113">Klicken Sie auf **Filter**.</span><span class="sxs-lookup"><span data-stu-id="96231-113">Click **Filter**.</span></span>
7. <span data-ttu-id="96231-114">Markieren Sie die Zeile mit den Filterkriterien, die Sie definieren möchten.</span><span class="sxs-lookup"><span data-stu-id="96231-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="96231-115">Geben Sie im Feld **Kriterien** Filterkriterien ein oder wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="96231-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="96231-116">Klicken Sie zum Schließen der Filterseite auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="96231-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="96231-117">Klicken Sie zum Starten des Journalisierungsprozesses auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="96231-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="96231-118">Ein Bericht wird generiert, nachdem der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="96231-118">A report will be generated after the process is complete.</span></span>  

