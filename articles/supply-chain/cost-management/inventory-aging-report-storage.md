---
title: Bestandsfälligkeitsbericht
description: In diesem Thema wird die Funktionalität beschrieben, mit der Sie einen Bericht zur Bestandsalterung ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen können.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9148a9032615222a1fdfe453488e716bacadbabc
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275578"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="585ee-103">Bestandsfälligkeitsbericht</span><span class="sxs-lookup"><span data-stu-id="585ee-103">Inventory aging report storage</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="585ee-104">In Microsoft Dynamics 365 Supply Chain Management können Sie einen Bericht **Bestandsfälligkeitsbericht** ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="585ee-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="585ee-105">Im Formular werden Spalten- und Summensalden je nach konfiguriertem Layout dynamisch angepasst.</span><span class="sxs-lookup"><span data-stu-id="585ee-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="585ee-106">Das Diagramm bietet einen visuellen Überblick, der die Filterung unterstützt und es Ihnen ermöglicht, bis in die Details zu verzweigen.</span><span class="sxs-lookup"><span data-stu-id="585ee-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="585ee-107">Zusätzlich können Sie mit einer Datenentität mit dem Namen **Bestandsfälligkeitsbericht** die Ergebnisse eines **Bestandsfälligkeitsbericht** in ein Format wie eine Microsoft Excel-Datei oder eine PDF-Datei exportieren.</span><span class="sxs-lookup"><span data-stu-id="585ee-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="585ee-108">Diese Methode zur Ausführung eines Berichts **Bestandsfälligkeitsbericht** ist hilfreich, wenn die Ausgabe viele Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="585ee-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="585ee-109">Beispielsweise enthält die Ausgabe viele Zeilen, wenn Sie 50.000 Artikel und 300 Filialen haben, die als Lager angelegt sind, und Sie die Bestandsalterung nach Artikel, Standort und Lager anfordern.</span><span class="sxs-lookup"><span data-stu-id="585ee-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="585ee-110">Aktivieren Sie die Funktion „Lagerbericht zum Bestandswert“</span><span class="sxs-lookup"><span data-stu-id="585ee-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="585ee-111">Bevor Sie diese Funktion nutzen können, müssen Sie sie auf Ihrem System aktivieren.</span><span class="sxs-lookup"><span data-stu-id="585ee-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="585ee-112">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie bei Bedarf aktivieren.</span><span class="sxs-lookup"><span data-stu-id="585ee-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="585ee-113">Hier wird die Funktion als aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="585ee-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="585ee-114">**Modul** - Kostenmanagement</span><span class="sxs-lookup"><span data-stu-id="585ee-114">**Module** - Cost management</span></span>
- <span data-ttu-id="585ee-115">**Funktionsname** – Bestandsfälligkeitsbericht</span><span class="sxs-lookup"><span data-stu-id="585ee-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="585ee-116">Bestandsfälligkeitsbericht ausführen</span><span class="sxs-lookup"><span data-stu-id="585ee-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="585ee-117">Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Bestandsalterung**.</span><span class="sxs-lookup"><span data-stu-id="585ee-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="585ee-118">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="585ee-118">Select **New**.</span></span>
1. <span data-ttu-id="585ee-119">Geben Sie im Feld **Prozesskennung - Name** einen eindeutigen Namen für den Bericht ein.</span><span class="sxs-lookup"><span data-stu-id="585ee-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="585ee-120">Wählen Sie den Bericht **Identifikation - ID** aus und filtern Sie ihn nach Ihren Wünschen.</span><span class="sxs-lookup"><span data-stu-id="585ee-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="585ee-121">Die Berichtsausführung erfolgt immer in einem Batch-Job.</span><span class="sxs-lookup"><span data-stu-id="585ee-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="585ee-122">Nach Abschluss des Batch-Jobs wird die Ausgabe auf der Seite **Bestandsalterung Berichtsspeicher** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="585ee-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="585ee-123">Um die Ausgabe als ein Formular mit einem traditionellen Rasterlayout anzuzeigen, wählen Sie **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="585ee-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="585ee-124">Um die Ausgabe als aggregiertes Diagramm anzuzeigen, wählen Sie **Diagramm anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="585ee-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="585ee-125">Das Formular enthält keine Zwischensummen, die im Berichtslayout definiert sind.</span><span class="sxs-lookup"><span data-stu-id="585ee-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="585ee-126">Mit der **Bestandsfälligkeitsbericht**-Dateneinheit können Sie die Ausgabe eines Berichts **Bestandsfälligkeitsbericht** exportieren, indem Sie einen Filter für das Feld **Prozessidentifikator - Name** auf jedes Format anwenden, das von der Datenverwaltung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="585ee-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
