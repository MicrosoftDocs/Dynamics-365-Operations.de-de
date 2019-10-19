---
title: Hinzufügen von Finanzdimensionen zum CFO-Arbeitsbereich
description: In diesem Thema wird erläutert, wie der CFO-Arbeitsbereich Finanzdimensionen hinzufügt, sodass sie für die Sach- und Budgetberichten verwendet werden können.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3817c6688339735c7478e85786efe15bd2372c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177878"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="131ea-103">Hinzufügen von Finanzdimensionen zum CFO-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="131ea-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="131ea-104">In diesem Thema wird erläutert, wie der CFO-Arbeitsbereich Finanzdimensionen hinzufügt, sodass sie für die Sach- und Budgetberichten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="131ea-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="131ea-105">Der CFO-Arbeitsbereich hat eine Registerkarte **Überblick** und eine **Finanzen** Registerkarte. Die Berichte zu diesen zwei Registerkarten werden mit zwei Kennzahlen unterstützt: LedgerActivityMeasure und BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="131ea-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="131ea-106">Es gibt eine Beziehung zwischen diesen zwei Kennzahlen und der DimensionCombinationEntity-Entität.</span><span class="sxs-lookup"><span data-stu-id="131ea-106">There is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="131ea-107">Andernfalls können Sie Dimensionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="131ea-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="131ea-108">In Finance auf der Seite **Entitäts-Shop** aktualisieren Sie **LedgerActivityMeasure** und die Kennzahlen **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="131ea-108">In Finance, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="131ea-109">Öffnen Sie in Microsoft Visual Studio den Anwendungs-Explorer und suchen Sie **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="131ea-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="131ea-110">Unter **Ressourcen** öffnen Sie **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="131ea-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="131ea-111">Wenn die Ressource im Microsoft Power BI Desktop geöffnet wird, wählen Sie **Daten abrufen**, **SQL Server-Datenbank**, und dann **Verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="131ea-112">Geben Sie den Server mit der Berichtsdatenbank **AxDW** als Datenbank ein.</span><span class="sxs-lookup"><span data-stu-id="131ea-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="131ea-113">Wählen Sie zunächst **Direct Query** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="131ea-114">Suchen und wählen Sie **LedgerActivityMeasure \_DimensionCombination** aus und anschließend **Laden** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="131ea-115">In der Liste **Felder** benennen Sie die Tabelle **Finanzdimensionen** um, sodass sie einfach zu u identifizieren ist.</span><span class="sxs-lookup"><span data-stu-id="131ea-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="131ea-116">Wählen Sie **Verwalten Sie Beziehungen** und **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="131ea-117">Wählen Sie im ersten Feld **Hauptbuch-Aktivitäten** und **LedgerDimension** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="131ea-118">Im zweiten Feld geben Sie **LedgerActivityMeasure\_DimensionCombination** (oder **Financial dimensions** wenn Sie die Tabelle umbenannt haben).</span><span class="sxs-lookup"><span data-stu-id="131ea-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="131ea-119">Wählen Sie die Überschrift **DimensionCombinationRECID** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="131ea-120">Wählen Sie im Feld **Kardinalität** **Viele bis ein** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="131ea-121">Ändern Sie den Wert **Filterrichtung kreuzen** auf  **Einzeln**.</span><span class="sxs-lookup"><span data-stu-id="131ea-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="131ea-122">Wählen Sie **Führen Sie diese Beziehung aktiv** und **Nehmen Sie referenzielle Integrität an** aus, wählen Sie **OK** und **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="131ea-123">[![Eine Beziehung erstellen](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="131ea-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="131ea-124">In der Liste **Felder** können Sie die Tabelle sowie die verfügbaren Finanzdimensionen finden.</span><span class="sxs-lookup"><span data-stu-id="131ea-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="131ea-125">Ziehen Sie die gewünschten Finanzdimensionen in die Berichtsebenenfilter.</span><span class="sxs-lookup"><span data-stu-id="131ea-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="131ea-126">Speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="131ea-126">Save your changes.</span></span>
15. <span data-ttu-id="131ea-127">In der Entwicklungsumgebung (AOT), klicken Sie auf das Projekt mit der rechten Maustaste, und wählen Sie dann **Synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="131ea-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="131ea-128">Stellen Sie das Projekt zusammen und öffnen Sie dann die Anwendung, um die Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="131ea-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="131ea-129">[![Arbeitsabereich abgeschlossen](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="131ea-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
