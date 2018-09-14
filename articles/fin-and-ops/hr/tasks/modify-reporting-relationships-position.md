--- 
title: "Berichtsbeziehungen für eine Position ändern"
description: "Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden."
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e779a337ff8f8e0199a60e094f4bec9eba49e701
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="c3b8e-103">Berichtsbeziehungen für eine Position ändern</span><span class="sxs-lookup"><span data-stu-id="c3b8e-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3b8e-104">Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="c3b8e-105">Die Berichtbeziehungen können für das Weiterleiten von Dokumenten durch Workflow verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="c3b8e-106">Die Prozedur zeigt auch, wie Sie den Mitarbeiter weiteren Hierarchien zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="c3b8e-107">Beispielsweise kann ein Mitarbeiter Teil eines Projektteams mit informellen Berichtsbeziehungen zu einem Projekt-Supervisor sein.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="c3b8e-108">Zusätzliche Berichtsbeziehungen können für die Position definiert werden, um verschiedene Projekt- oder Matrixszenarien zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="c3b8e-109">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c3b8e-110">Wechseln Sie zu "Personalverwaltung" > "Positionen" > "Positionen".</span><span class="sxs-lookup"><span data-stu-id="c3b8e-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="c3b8e-111">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c3b8e-112">Filtern Sie beispielsweise im Feld "Position" mit dem Wert "000091".</span><span class="sxs-lookup"><span data-stu-id="c3b8e-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="c3b8e-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c3b8e-114">Erweitern Sie die Berichte um den Abschnitt "Position".</span><span class="sxs-lookup"><span data-stu-id="c3b8e-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="c3b8e-115">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="c3b8e-116">Geben Sie im Feld "Vorgesetzter" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="c3b8e-117">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="c3b8e-117">Click Create.</span></span>
8. <span data-ttu-id="c3b8e-118">Erweitern Sie den Abschnitt 'Beziehungen'.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="c3b8e-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-119">Click Add.</span></span>
10. <span data-ttu-id="c3b8e-120">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von ''.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="c3b8e-121">Geben Sie im Feld "Hierarchiename" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="c3b8e-122">Beispiel: Projekt</span><span class="sxs-lookup"><span data-stu-id="c3b8e-122">Example: Project</span></span>  
12. <span data-ttu-id="c3b8e-123">Geben Sie im Feld "Position" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c3b8e-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="c3b8e-124">Beispiel: 000437</span><span class="sxs-lookup"><span data-stu-id="c3b8e-124">Example:  000437</span></span>
13. <span data-ttu-id="c3b8e-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c3b8e-125">Click Save.</span></span>


