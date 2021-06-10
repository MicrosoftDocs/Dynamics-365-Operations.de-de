---
title: Berichtsbeziehungen für eine Position ändern
description: Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78410347e7e6cf67f692c7e9193419ffd87e3057
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057091"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="54cd6-103">Berichtsbeziehungen für eine Position ändern</span><span class="sxs-lookup"><span data-stu-id="54cd6-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="54cd6-104">Diese Prozedur zeigt, wie Berichtsbeziehungen für einen Mitarbeiter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="54cd6-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="54cd6-105">Die Berichtbeziehungen können für das Weiterleiten von Dokumenten durch Workflow verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54cd6-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="54cd6-106">Die Prozedur zeigt auch, wie Sie den Mitarbeiter weiteren Hierarchien zuweisen.</span><span class="sxs-lookup"><span data-stu-id="54cd6-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="54cd6-107">Beispielsweise kann ein Mitarbeiter Teil eines Projektteams mit informellen Berichtsbeziehungen zu einem Projekt-Supervisor sein.</span><span class="sxs-lookup"><span data-stu-id="54cd6-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="54cd6-108">Zusätzliche Berichtsbeziehungen können für die Position definiert werden, um verschiedene Projekt- oder Matrixszenarien zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="54cd6-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="54cd6-109">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="54cd6-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="54cd6-110">Wechseln Sie zu "Personalverwaltung" > "Positionen" > "Positionen".</span><span class="sxs-lookup"><span data-stu-id="54cd6-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="54cd6-111">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="54cd6-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="54cd6-112">Filtern Sie beispielsweise im Feld "Position" mit dem Wert "000091".</span><span class="sxs-lookup"><span data-stu-id="54cd6-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="54cd6-113">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="54cd6-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54cd6-114">Erweitern Sie die Berichte um den Abschnitt "Position".</span><span class="sxs-lookup"><span data-stu-id="54cd6-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="54cd6-115">Klicken Sie auf "Neu" zum Öffnen des Ablagedialogfeld.</span><span class="sxs-lookup"><span data-stu-id="54cd6-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="54cd6-116">Geben Sie im Feld "Vorgesetzter" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="54cd6-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="54cd6-117">Klicken Sie auf "Erstellen".</span><span class="sxs-lookup"><span data-stu-id="54cd6-117">Click Create.</span></span>
8. <span data-ttu-id="54cd6-118">Erweitern Sie den Abschnitt 'Beziehungen'.</span><span class="sxs-lookup"><span data-stu-id="54cd6-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="54cd6-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="54cd6-119">Click Add.</span></span>
10. <span data-ttu-id="54cd6-120">Aktivieren Sie das Kontrollkästchen in der Kopfzeile von ''.</span><span class="sxs-lookup"><span data-stu-id="54cd6-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="54cd6-121">Geben Sie im Feld "Hierarchiename" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="54cd6-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="54cd6-122">Beispiel: Projekt</span><span class="sxs-lookup"><span data-stu-id="54cd6-122">Example: Project</span></span>  
12. <span data-ttu-id="54cd6-123">Geben Sie im Feld "Position" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="54cd6-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="54cd6-124">Beispiel: 000437</span><span class="sxs-lookup"><span data-stu-id="54cd6-124">Example:  000437</span></span>
13. <span data-ttu-id="54cd6-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="54cd6-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]