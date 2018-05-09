--- 
title: "Ausführen eines Berichts, der Finanzdimensionen als Datenquelle verwendet"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fefac4db9d6fec926068483bbe8ae91a6d5d6028
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source"></a><span data-ttu-id="110c3-103">Ausführen eines Berichts, der Finanzdimensionen als Datenquelle verwendet</span><span class="sxs-lookup"><span data-stu-id="110c3-103">Run a report that uses financial dimensions as a data source</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="110c3-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Modell zur Nutzung von Finanzdimensionen als Datenquelle für ER-Berichte nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="110c3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="110c3-105">Diese Schritte können im DEMF-Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="110c3-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="110c3-106">Um diese Schritte auszuführen, müssen Sie erst die Schritte im Verfahren "ER - Finanzdimensionen als Datenquelle nutzen (Teil 3: Design des Berichts)" ausführen.</span><span class="sxs-lookup"><span data-stu-id="110c3-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="110c3-107">Sie müssen außerdem Standarddokumenttypen der elektronischen Berichterstellungsparameterseite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="110c3-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="110c3-108">Standarddokumenttypen werden auch festgelegt, wenn Sie alle ER-Konfiguration herunterladen und importieren.</span><span class="sxs-lookup"><span data-stu-id="110c3-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="110c3-109">Berichte ausführen</span><span class="sxs-lookup"><span data-stu-id="110c3-109">Run report</span></span>
1. <span data-ttu-id="110c3-110">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="110c3-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="110c3-111">Erweitern Sie in der Struktur "Finanzdimensions-Beispielmodell".</span><span class="sxs-lookup"><span data-stu-id="110c3-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="110c3-112">Wählen Sie in der Struktur "Finanzdimensions-Beispielmodell\Sachkontoerfassungsbericht".</span><span class="sxs-lookup"><span data-stu-id="110c3-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="110c3-113">Klicken Sie auf Ausführen.</span><span class="sxs-lookup"><span data-stu-id="110c3-113">Click Run.</span></span>
5. <span data-ttu-id="110c3-114">Wählen Sie im Dimensionsnamen-Feld eine Option aus oder geben Sie einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="110c3-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="110c3-115">Um alle Dimensionen im aktuellen Unternehmen auszuwählen, geben Sie Folgendes ein: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="110c3-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="110c3-116">Erweitern Sie den Abschnitt "Einzuschließende Datensätze".</span><span class="sxs-lookup"><span data-stu-id="110c3-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="110c3-117">Klicken Sie auf "Filter".</span><span class="sxs-lookup"><span data-stu-id="110c3-117">Click Filter.</span></span>
8. <span data-ttu-id="110c3-118">Wählen Sie die Zeile für die Sachkontoerfassungstabelle und das Feld Erfassungschargennummer aus.</span><span class="sxs-lookup"><span data-stu-id="110c3-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="110c3-119">Geben Sie im Feld "Kriterien" den Wert "00057" ein.</span><span class="sxs-lookup"><span data-stu-id="110c3-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="110c3-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="110c3-120">Click OK.</span></span>
11. <span data-ttu-id="110c3-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="110c3-121">Click OK.</span></span>
    * <span data-ttu-id="110c3-122">Prüfen Sie das generierte Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="110c3-122">Review the generated output.</span></span> <span data-ttu-id="110c3-123">Beachten Sie, das für jede Buchung der ausgewählten Charge, die Finanzdimensionen aus den entsprechenden Dimensionssatz dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="110c3-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="110c3-124">Führen Sie diesen Bericht aus, und wählen Sie unterschiedliche Dimensionen aus, um zu sehen, dass der Bericht nicht von der Anzahl der ausgewählten Dimensionen oder der Anzahl der Dimensionen abhängt, die für diese Dynamics 365 for Finance and Operations-Instanz konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="110c3-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


