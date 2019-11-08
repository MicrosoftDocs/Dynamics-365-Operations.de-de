---
title: 'ER – Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten nutzen (Teil 2: Format ausführen)'
description: In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76a2df5cd7714ffda6d0563d3d9013f032db7c2
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550880"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="1c534-103">ER – Horizontal erweiterbare Bereiche zum dynamischen Hinzufügen von Spalten in Excel-Berichten nutzen (Teil 2: Format ausführen)</span><span class="sxs-lookup"><span data-stu-id="1c534-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c534-104">In den folgenden Schritten wird erläutert, wie einem Benutzer mit der Rolle Systemadministrator oder elektronischer Berichterstellungsentwickler ein Elektronische Berichterstellung-Format (ER) zur Generierung von Berichten als OPENXML-Arbeitsblätter (Excel) konfigurieren kann, in dem die erforderlichen Spalten als horizontal erweiterbare Bereiche erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="1c534-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="1c534-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1c534-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="1c534-106">Um diese Schritte auszuführen, müssen Sie die Schritte in "ER - Verwendung von horizontal erweiterbaren Bereichen zum dynamischen Hinzufügen von Spalten zu Excel-Berichten (Teil 1: Designformat)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c534-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="1c534-107">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="1c534-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="1c534-108">Erstelltes Format suchen</span><span class="sxs-lookup"><span data-stu-id="1c534-108">Find created format</span></span>
1. <span data-ttu-id="1c534-109">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="1c534-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1c534-110">Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="1c534-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1c534-111">Wählen Sie in der Strukturdarstellung "Finanzdimensionsbeispielmodell\Beispielbericht mit horizontal erweiterbaren Bereichen" aus.</span><span class="sxs-lookup"><span data-stu-id="1c534-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="1c534-112">Format für Excel-Ausgabe ausführen</span><span class="sxs-lookup"><span data-stu-id="1c534-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="1c534-113">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="1c534-113">Click Run.</span></span>
2. <span data-ttu-id="1c534-114">Geben Sie im Feld "Dimensionsnamen" "BusinessUnit;CostCenter;Department" ein.</span><span class="sxs-lookup"><span data-stu-id="1c534-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="1c534-115">Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1c534-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="1c534-116">Um alle Dimensionen für das aktuelle Unternehmen auszuwählen, geben Sie Folgendes ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="1c534-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="1c534-117">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="1c534-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="1c534-118">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="1c534-118">Click Filter.</span></span>
5. <span data-ttu-id="1c534-119">Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="1c534-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="1c534-120">Geben Sie im Feld "Kriterien" den Wert '00057..00058' ein.</span><span class="sxs-lookup"><span data-stu-id="1c534-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="1c534-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="1c534-121">00057..00058</span></span>  
7. <span data-ttu-id="1c534-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c534-122">Click OK.</span></span>
8. <span data-ttu-id="1c534-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1c534-123">Click OK.</span></span>
    * <span data-ttu-id="1c534-124">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="1c534-124">Review the generated output.</span></span> <span data-ttu-id="1c534-125">Beachten Sie, dass die neu erstellte Excel-Datei dieselbe Anzahl von Spalten enthält, die für Finanzdimensionen ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="1c534-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="1c534-126">Der in Berichtskopf in diesen Spalten enthält die Namen der Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="1c534-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="1c534-127">Die Transaktionszeilen in diesen Spalten enthalten die Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="1c534-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="1c534-128">Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die für diese Instanz konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="1c534-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

