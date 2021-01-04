---
title: Eine Datensatzvorlage erstellen, um die Dateneingabe zu erleichtern
description: Dieses Thema zeigt, wie eine Datensatzvorlage erstellt wird, sodass Feldwerte, die oft verwendet werden, nicht explizit für jeden neuen Datensatz eingegeben werden müssen.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68d3c7dd2f042617a7e2fcc8bee05fae6a82bde9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685216"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="7ade2-103">Eine Datensatzvorlage erstellen, um die Dateneingabe zu erleichtern</span><span class="sxs-lookup"><span data-stu-id="7ade2-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ade2-104">Dieses Thema zeigt, wie eine Datensatzvorlage erstellt wird, sodass Feldwerte, die oft verwendet werden, nicht explizit für jeden neuen Datensatz eingegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7ade2-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="7ade2-105">In dieser Prozedur erstellen Sie einen neuen Datensatz für neue Laptops, die den Anlagen hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ade2-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="7ade2-106">Für diese Prozedur wird das Beispielunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ade2-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="7ade2-107">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="7ade2-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="7ade2-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7ade2-108">Select **New**.</span></span>
3. <span data-ttu-id="7ade2-109">Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7ade2-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="7ade2-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="7ade2-111">Geben Sie zum Beispiel **Laptop des potenziellen Firmenkunden** ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="7ade2-112">Geben Sie im Feld **Suchname** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="7ade2-113">Geben Sie beispielsweise **Laptop** ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="7ade2-114">Erweitern Sie den Abschnitt **Technische Informationen**.</span><span class="sxs-lookup"><span data-stu-id="7ade2-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="7ade2-115">Geben Sie in den Feldern **Hersteller**, **Modell** und **Modelljahr** jeweils Werte ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="7ade2-116">Wählen Sie im Aktivitätsbereich **Optionen** aus.</span><span class="sxs-lookup"><span data-stu-id="7ade2-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="7ade2-117">Wählen Sie **Datensatzinfo** aus.</span><span class="sxs-lookup"><span data-stu-id="7ade2-117">Select **Record info**.</span></span>
10. <span data-ttu-id="7ade2-118">Wählen Sie **Benutzervorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="7ade2-118">Select **User template**.</span></span>
11. <span data-ttu-id="7ade2-119">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="7ade2-120">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7ade2-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="7ade2-121">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ade2-121">Select **OK**.</span></span>
14. <span data-ttu-id="7ade2-122">Wählen Sie **Schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="7ade2-122">Select **Close**.</span></span>

