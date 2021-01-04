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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684738"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="8e7ee-103">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)</span><span class="sxs-lookup"><span data-stu-id="8e7ee-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e7ee-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="8e7ee-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="8e7ee-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 3: Design des Berichts)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="8e7ee-107">Sie müssen außerdem Standarddokumenttypen der elektronischen Berichterstellungsparameterseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="8e7ee-108">Standarddokumenttypen werden auch festgelegt, wenn Sie alle ER-Konfiguration herunterladen und importieren.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="8e7ee-109">Berichte ausführen</span><span class="sxs-lookup"><span data-stu-id="8e7ee-109">Run report</span></span>
1. <span data-ttu-id="8e7ee-110">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8e7ee-111">Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="8e7ee-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8e7ee-112">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell\Sachkontoerfassungsbericht".</span><span class="sxs-lookup"><span data-stu-id="8e7ee-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="8e7ee-113">Klicken Sie auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-113">Click Run.</span></span>
<span data-ttu-id="8e7ee-114">![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="8e7ee-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="8e7ee-115">Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="8e7ee-116">Um alle Dimensionen im aktuellen Unternehmen auszuwählen, geben Sie folgende Informationen ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="8e7ee-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="8e7ee-118">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="8e7ee-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="8e7ee-119">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="8e7ee-119">Click Filter.</span></span>
8. <span data-ttu-id="8e7ee-120">Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="8e7ee-121">Geben Sie im Feld "Kriterien" den Wert "00057" ein.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="8e7ee-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e7ee-122">Click OK.</span></span>
11. <span data-ttu-id="8e7ee-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8e7ee-123">Click OK.</span></span>
<span data-ttu-id="8e7ee-124">![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="8e7ee-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="8e7ee-125">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-125">Review the generated output.</span></span> <span data-ttu-id="8e7ee-126">Für jede Buchung der ausgewählten Charge werden die Finanzdimensionen aus den entsprechenden Dimensionssatz dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="8e7ee-127">Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die für diese Instanz konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="8e7ee-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run4.png)
