---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)'
description: In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: a9a6f07d6c665097fabab4d3ec6d7fa5ba80b65d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406473"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="614e4-103">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)</span><span class="sxs-lookup"><span data-stu-id="614e4-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="614e4-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="614e4-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="614e4-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="614e4-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="614e4-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 3: Design des Berichts)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="614e4-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="614e4-107">Sie müssen außerdem Standarddokumenttypen der elektronischen Berichterstellungsparameterseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="614e4-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="614e4-108">Standarddokumenttypen werden auch festgelegt, wenn Sie alle ER-Konfiguration herunterladen und importieren.</span><span class="sxs-lookup"><span data-stu-id="614e4-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="614e4-109">Berichte ausführen</span><span class="sxs-lookup"><span data-stu-id="614e4-109">Run report</span></span>
1. <span data-ttu-id="614e4-110">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="614e4-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="614e4-111">Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="614e4-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="614e4-112">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell\Sachkontoerfassungsbericht".</span><span class="sxs-lookup"><span data-stu-id="614e4-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="614e4-113">Klicken Sie auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="614e4-113">Click Run.</span></span>
<span data-ttu-id="614e4-114">![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="614e4-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="614e4-115">Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="614e4-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="614e4-116">Um alle Dimensionen im aktuellen Unternehmen auszuwählen, geben Sie folgende Informationen ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="614e4-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="614e4-118">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="614e4-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="614e4-119">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="614e4-119">Click Filter.</span></span>
8. <span data-ttu-id="614e4-120">Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="614e4-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="614e4-121">Geben Sie im Feld "Kriterien" den Wert "00057" ein.</span><span class="sxs-lookup"><span data-stu-id="614e4-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="614e4-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="614e4-122">Click OK.</span></span>
11. <span data-ttu-id="614e4-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="614e4-123">Click OK.</span></span>
<span data-ttu-id="614e4-124">![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="614e4-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="614e4-125">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="614e4-125">Review the generated output.</span></span> <span data-ttu-id="614e4-126">Für jede Buchung der ausgewählten Charge werden die Finanzdimensionen aus den entsprechenden Dimensionssatz dargestellt.</span><span class="sxs-lookup"><span data-stu-id="614e4-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="614e4-127">Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die für diese Instanz konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="614e4-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run4.png)
