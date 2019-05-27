---
title: Ändern der Abschreibungskonventionen für mehrere Anlagen
description: Mithilfe dieser Aufgabe wird die Abschreibungskonvention für eine angegebene Anlagengruppe aktualisiert.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a79b2edf64f0063253d3f2a23b0020eceb87c0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561498"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="3f599-103">Ändern der Abschreibungskonventionen für mehrere Anlagen</span><span class="sxs-lookup"><span data-stu-id="3f599-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f599-104">Mithilfe dieser Aufgabe wird die Abschreibungskonvention für eine angegebene Anlagengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f599-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="3f599-105">Für diese Aufgabenanleitung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f599-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="3f599-106">Wechseln Sie zu "Anlagen" > "Periodische Aufgaben" > "Massenaktualisierung"</span><span class="sxs-lookup"><span data-stu-id="3f599-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="3f599-107">Klicken Sie im Feld "Abschreibungsbuch" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3f599-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3f599-108">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3f599-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3f599-109">Geben Sie im Feld "Startdatum für die Inbetriebnahme" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="3f599-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="3f599-110">Geben Sie im Feld "Enddatum für die Inbetriebnahme" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="3f599-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="3f599-111">Nur Anlagen, die dem ausgewählten Abschreibungsbuch zugeordnet sind und innerhalb dieses Zeitraums in Betrieb genommen wurden, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f599-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="3f599-112">Wählen Sie im Feld "Aktuelle Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="3f599-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="3f599-113">Nur Anlagen, die die aktuelle Abschreibungskonvention haben, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f599-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="3f599-114">Wählen Sie im Feld "Neue Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="3f599-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="3f599-115">Überprüfen Sie, dass der Bericht zum Drucken an das ausgewählte Ziel gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f599-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="3f599-116">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="3f599-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="3f599-117">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="3f599-117">Click Filter.</span></span>
10. <span data-ttu-id="3f599-118">Wählen Sie in der Liste die Gruppe "Anlage" aus.</span><span class="sxs-lookup"><span data-stu-id="3f599-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="3f599-119">Klicken Sie im Feld "Kriterien" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3f599-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="3f599-120">Wählen Sie die gewünschte Gruppe "Anlage" aus.</span><span class="sxs-lookup"><span data-stu-id="3f599-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="3f599-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="3f599-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3f599-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3f599-122">Click OK.</span></span>
15. <span data-ttu-id="3f599-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3f599-123">Click OK.</span></span>
    *  <span data-ttu-id="3f599-124">Ergebnisse des Prozesses werden im "Massenaktualisierungsbericht" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f599-124">Results of the process are shown on the Mass update report.</span></span>     

