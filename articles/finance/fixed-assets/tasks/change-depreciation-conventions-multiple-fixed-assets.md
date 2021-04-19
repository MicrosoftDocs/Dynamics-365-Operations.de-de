---
title: Ändern der Abschreibungskonventionen für mehrere Anlagen
description: Mithilfe dieser Aufgabe wird die Abschreibungskonvention für eine angegebene Anlagengruppe aktualisiert.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a71b24b0c2ea072aeff8c994cfdac10bc57b64c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823979"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="8a404-103">Ändern der Abschreibungskonventionen für mehrere Anlagen</span><span class="sxs-lookup"><span data-stu-id="8a404-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a404-104">Mithilfe dieser Aufgabe wird die Abschreibungskonvention für eine angegebene Anlagengruppe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8a404-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="8a404-105">Für diese Aufgabenanleitung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a404-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="8a404-106">Wechseln Sie zu "Anlagen" > "Periodische Aufgaben" > "Massenaktualisierung"</span><span class="sxs-lookup"><span data-stu-id="8a404-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="8a404-107">Klicken Sie im Feld "Abschreibungsbuch" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a404-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8a404-108">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8a404-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8a404-109">Geben Sie im Feld "Startdatum für die Inbetriebnahme" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8a404-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="8a404-110">Geben Sie im Feld "Enddatum für die Inbetriebnahme" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="8a404-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="8a404-111">Nur Anlagen, die dem ausgewählten Abschreibungsbuch zugeordnet sind und innerhalb dieses Zeitraums in Betrieb genommen wurden, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8a404-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="8a404-112">Wählen Sie im Feld "Aktuelle Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8a404-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="8a404-113">Nur Anlagen, die die aktuelle Abschreibungskonvention haben, werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8a404-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="8a404-114">Wählen Sie im Feld "Neue Abschreibungskonvention" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="8a404-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="8a404-115">Überprüfen Sie, dass der Bericht zum Drucken an das ausgewählte Ziel gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a404-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="8a404-116">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="8a404-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="8a404-117">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="8a404-117">Click Filter.</span></span>
10. <span data-ttu-id="8a404-118">Wählen Sie in der Liste die Gruppe "Anlage" aus.</span><span class="sxs-lookup"><span data-stu-id="8a404-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="8a404-119">Klicken Sie im Feld "Kriterien" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a404-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="8a404-120">Wählen Sie die gewünschte Gruppe "Anlage" aus.</span><span class="sxs-lookup"><span data-stu-id="8a404-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="8a404-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8a404-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8a404-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a404-122">Click OK.</span></span>
15. <span data-ttu-id="8a404-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8a404-123">Click OK.</span></span>
    *  <span data-ttu-id="8a404-124">Ergebnisse des Prozesses werden im "Massenaktualisierungsbericht" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8a404-124">Results of the process are shown on the Mass update report.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]