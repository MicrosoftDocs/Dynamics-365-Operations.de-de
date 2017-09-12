---
title: "Hinzufügen von Finanzdimensionen zum CFO-Arbeitsbereich"
description: "In diesem Thema wird erläutert, wie der CFO-Arbeitsbereich Finanzdimensionen hinzufügt, sodass sie für die Sach- und Budgetberichten verwendet werden können."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: de-de
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="a72cb-103">Hinzufügen von Finanzdimensionen zum CFO-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a72cb-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a72cb-104">In diesem Thema wird erläutert, wie der CFO-Arbeitsbereich Finanzdimensionen hinzufügt, sodass sie für die Sach- und Budgetberichten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a72cb-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="a72cb-105">Der CFO-Arbeitsbereich hat eine Registerkarte **Überblick** und eine **Finanzen** Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="a72cb-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="a72cb-106">Die Berichte zu diesen zwei Registerkarten werden mit zwei Kennzahlen unterstützt: LedgerActivityMeasure und BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="a72cb-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="a72cb-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, Update Juli 2017, gibt es eine Beziehung zwischen jenen zwei Kennzahlen und der DimensionCombinationEntity-Entität.</span><span class="sxs-lookup"><span data-stu-id="a72cb-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="a72cb-108">Andernfalls können Sie Dimensionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="a72cb-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="a72cb-109">In Finance and Operations auf der Seite **Entitäts-Shop**, aktualisieren Sie **LedgerActivityMeasure** und die Kennzahlen **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="a72cb-110">In Microsoft Visual Studio, öffnen Sie den Anwendungs-Explorer und suchen **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="a72cb-111">Unter **Ressourcen** öffnen Sie **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="a72cb-112">Wenn die Ressource im Microsoft Power BI Desktop geöffnet wird, wählen Sie **Daten abrufen** **SQL Server-Datenbank** und anschließend **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="a72cb-113">Geben Sie den Server mit der Berichtsdatenbank **AxDW** als Datenbank ein.</span><span class="sxs-lookup"><span data-stu-id="a72cb-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="a72cb-114">Wählen Sie zunächst **Direct Query** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="a72cb-115">Suchen und wählen Sie **LedgerActivityMeasure \_DimensionCombination** aus und anschließend **Laden** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="a72cb-116">In der Liste **Felder** benennen Sie die Tabelle **Finanzdimensionen** um, sodass sie einfach zu u identifizieren ist.</span><span class="sxs-lookup"><span data-stu-id="a72cb-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="a72cb-117">Wählen Sie **Verwalten Sie Beziehungen** und **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="a72cb-118">Wählen Sie im ersten Feld **Hauptbuch-Aktivitäten** und **LedgerDimension** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="a72cb-119">Im zweiten Feld geben Sie **LedgerActivityMeasure\_DimensionCombination** (oder **Financial dimensions** wenn Sie die Tabelle umbenannt haben).</span><span class="sxs-lookup"><span data-stu-id="a72cb-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="a72cb-120">Wählen Sie die Überschrift **DimensionCombinationRECID** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="a72cb-121">Wählen Sie im Feld **Kardinalität** **Viele bis ein** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="a72cb-122">Ändern Sie den Wert **Filterrichtung kreuzen** auf  **Einzeln**.</span><span class="sxs-lookup"><span data-stu-id="a72cb-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="a72cb-123">Wählen Sie **Führen Sie diese Beziehung aktiv** und **Nehmen Sie referenzielle Integrität an** aus, wählen Sie **OK** und **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="a72cb-124">[![Eine Beziehung erstellen](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="a72cb-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="a72cb-125">In der Liste **Felder** können Sie die Tabelle sowie die verfügbaren Finanzdimensionen finden.</span><span class="sxs-lookup"><span data-stu-id="a72cb-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="a72cb-126">Ziehen Sie die gewünschten Finanzdimensionen in die Berichtsebenenfilter.</span><span class="sxs-lookup"><span data-stu-id="a72cb-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="a72cb-127">Speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a72cb-127">Save your changes.</span></span>
15. <span data-ttu-id="a72cb-128">In der Entwicklungsumgebung (AOT), klicken Sie auf das Projekt mit der rechten Maustaste, und wählen Sie dann **Synchronisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a72cb-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="a72cb-129">Stellen Sie das Projekt zusammen und öffnen Sie dann die Anwendung, um die Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a72cb-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="a72cb-130">[![Arbeitsabereich abgeschlossen](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="a72cb-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

