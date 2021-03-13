---
title: 'ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)'
description: In diesem Thema wird beschrieben, wie Sie ein EB-Modell (elektronische Berichterstellung) konfigurieren, um Finanzdimensionen als Datenquelle für EB-Berichte zu verwenden. (Teil 4)
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
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092274"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="c8f21-104">ER – Verwendung von Finanzdimensionen als Datenquelle (Teil 4: Berichtsausführung)</span><span class="sxs-lookup"><span data-stu-id="c8f21-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8f21-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="c8f21-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c8f21-106">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c8f21-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c8f21-107">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren „ER - Finanzdimensionen als Datenquelle nutzen (Teil 3: Design des Berichts)“ ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8f21-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="c8f21-108">Sie müssen außerdem Standarddokumenttypen der elektronischen Berichterstellungsparameterseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c8f21-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="c8f21-109">Standarddokumenttypen werden auch festgelegt, wenn Sie alle ER-Konfiguration herunterladen und importieren.</span><span class="sxs-lookup"><span data-stu-id="c8f21-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="c8f21-110">Berichte ausführen</span><span class="sxs-lookup"><span data-stu-id="c8f21-110">Run report</span></span>
1. <span data-ttu-id="c8f21-111">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c8f21-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c8f21-112">Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="c8f21-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c8f21-113">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell\Sachkontoerfassungsbericht".</span><span class="sxs-lookup"><span data-stu-id="c8f21-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="c8f21-114">Klicken Sie auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8f21-114">Click Run.</span></span>
<span data-ttu-id="c8f21-115">![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="c8f21-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="c8f21-116">Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c8f21-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f21-117">Um alle Dimensionen im aktuellen Unternehmen auszuwählen, geben Sie folgende Informationen ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="c8f21-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="c8f21-119">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="c8f21-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c8f21-120">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="c8f21-120">Click Filter.</span></span>
8. <span data-ttu-id="c8f21-121">Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="c8f21-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="c8f21-122">Geben Sie im Feld "Kriterien" den Wert "00057" ein.</span><span class="sxs-lookup"><span data-stu-id="c8f21-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="c8f21-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8f21-123">Click OK.</span></span>
11. <span data-ttu-id="c8f21-124">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c8f21-124">Click OK.</span></span>
<span data-ttu-id="c8f21-125">![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="c8f21-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="c8f21-126">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="c8f21-126">Review the generated output.</span></span> <span data-ttu-id="c8f21-127">Für jede Buchung der ausgewählten Charge werden die Finanzdimensionen aus den entsprechenden Dimensionssatz dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c8f21-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="c8f21-128">Führen Sie diesen Bericht aus und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder aus der Anzahl der Dimensionen abhängt, die für diese Instanz konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8f21-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![ER-Konfigurationsseite](../media/er-financial-dimensions-guides-run4.png)
