---
title: Bestandsfälligkeitsbericht
description: In diesem Thema wird die Funktionalität beschrieben, mit der Sie einen Bericht zur Bestandsalterung ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen können.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810250"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="79b53-103">Bestandsfälligkeitsbericht</span><span class="sxs-lookup"><span data-stu-id="79b53-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="79b53-104">In Microsoft Dynamics 365 Supply Chain Management können Sie einen Bericht **Inventuralterung** ausführen und die Ausgabe als Formular und Diagramm zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="79b53-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="79b53-105">Im Formular werden Spalten- und Summensalden je nach konfiguriertem Layout dynamisch angepasst.</span><span class="sxs-lookup"><span data-stu-id="79b53-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="79b53-106">Das Diagramm bietet einen visuellen Überblick, der die Filterung unterstützt und es Ihnen ermöglicht, bis in die Details zu verzweigen.</span><span class="sxs-lookup"><span data-stu-id="79b53-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="79b53-107">Zusätzlich können Sie mit einer Datenentität mit dem Namen **Bestandsalterungsbericht** die Ergebnisse eines **Bestandsalterungsberichts** in ein Format wie eine Microsoft Excel-Datei oder eine PDF-Datei exportieren.</span><span class="sxs-lookup"><span data-stu-id="79b53-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="79b53-108">Diese Methode zur Ausführung eines Berichts **Bestandsalterung** ist hilfreich, wenn die Ausgabe viele Zeilen enthält.</span><span class="sxs-lookup"><span data-stu-id="79b53-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="79b53-109">Beispielsweise enthält die Ausgabe viele Zeilen, wenn Sie 50.000 Artikel und 300 Filialen haben, die als Lager angelegt sind, und Sie die Bestandsalterung nach Artikel, Standort und Lager anfordern.</span><span class="sxs-lookup"><span data-stu-id="79b53-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="79b53-110">Ausführen eines Berichts zur Bestandsalterung</span><span class="sxs-lookup"><span data-stu-id="79b53-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="79b53-111">Gehen Sie zu **Kostenmanagement \> Anfragen und Berichte \> Bestandsalterung**.</span><span class="sxs-lookup"><span data-stu-id="79b53-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="79b53-112">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="79b53-112">Select **New**.</span></span>
1. <span data-ttu-id="79b53-113">Geben Sie im Feld **Prozesskennung - Name** einen eindeutigen Namen für den Bericht ein.</span><span class="sxs-lookup"><span data-stu-id="79b53-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="79b53-114">Wählen Sie den Bericht **Identifikation - ID** aus und filtern Sie ihn nach Ihren Wünschen.</span><span class="sxs-lookup"><span data-stu-id="79b53-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="79b53-115">Die Berichtsausführung erfolgt immer in einem Batch-Job.</span><span class="sxs-lookup"><span data-stu-id="79b53-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="79b53-116">Nach Abschluss des Batch-Jobs wird die Ausgabe auf der Seite **Bestandsalterung Berichtsspeicher** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79b53-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="79b53-117">Um die Ausgabe als ein Formular mit einem traditionellen Rasterlayout anzuzeigen, wählen Sie **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="79b53-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="79b53-118">Um die Ausgabe als aggregiertes Diagramm anzuzeigen, wählen Sie **Diagramm anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="79b53-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="79b53-119">Das Formular enthält keine Zwischensummen, die im Berichtslayout definiert sind.</span><span class="sxs-lookup"><span data-stu-id="79b53-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="79b53-120">Mit dem Bericht **Bestandsalterung** Dateneinheit können Sie die Ausgabe eines Berichts **Bestandsalterung** exportieren, indem Sie einen Filter für das Feld **Prozessidentifikator - Name** auf jedes Format anwenden, das von der Datenverwaltung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="79b53-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
