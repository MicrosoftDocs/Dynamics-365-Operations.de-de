---
title: Geplante Ausführung
description: In diesem Abschnitt wird die planmäßige Ausführung im Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874669"
---
# <a name="scheduled-execution"></a><span data-ttu-id="05dc7-103">Geplante Ausführung</span><span class="sxs-lookup"><span data-stu-id="05dc7-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="05dc7-104">Sie können die Service Levels für Arbeitsaufträge verwenden, um die geplante Ausführung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="05dc7-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="05dc7-105">(Weitere Informationen zu den Service Levels der Arbeitsaufträge finden Sie unter [Service Level und Beschreibung](service-level-and-description.md).) Die planmäßige Ausführung bietet Flexibilität bei der Arbeitsplanung für Instandhalter, da Sie für das Intervall, in dem ein Arbeitsauftrag abgeschlossen werden soll, detailliertere oder weniger detaillierte Anforderungen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="05dc7-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="05dc7-106">So kann beispielsweise ein Wartungsmitarbeiter, der einen Auftrag in einer Produktionsstätte schneller als erwartet erledigt, zu einem anderen nahegelegenen Auftrag wechseln, der für die aktuelle Woche geplant war, aber nicht unbedingt für den aktuellen Tag.</span><span class="sxs-lookup"><span data-stu-id="05dc7-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="05dc7-107">Dieser Ansatz ermöglicht die Optimierung der Arbeitsvorbereitung und der Auftragsabwicklung.</span><span class="sxs-lookup"><span data-stu-id="05dc7-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="05dc7-108">Die Einrichtung der geplanten Ausführung, die sich auf Arbeitsaufträge bezieht, kann generisch oder spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="05dc7-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="05dc7-109">Sie können generische Zeilen einrichten, die nicht auf bestimmte Arbeitsauftragsarten, Anlagentypen usw. beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="05dc7-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="05dc7-110">Alternativ können Sie auch geplante Ausführungspositionen erstellen, die sich auf eine bestimmte Arbeitsauftragsart, Anlagenart, Wartungsauftragsart usw. beziehen.</span><span class="sxs-lookup"><span data-stu-id="05dc7-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="05dc7-111">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Arbeitsaufträge** \> **Planausführung**.</span><span class="sxs-lookup"><span data-stu-id="05dc7-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="05dc7-112">Wählen Sie **Neu**, um eine geplante Ausführungsposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="05dc7-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="05dc7-113">Wählen Sie in den Feldern **Technischer Standort**, **Auftragsart**, **Assettyp**, **Hersteller**, **Modell**, **Wartungsauftragstyp Kategorie**, **Wartungsauftragstyp**, **Wartungsauftragstyp Variante** und **Wechseln** die gewünschten Werte aus.</span><span class="sxs-lookup"><span data-stu-id="05dc7-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="05dc7-114">Wählen Sie im Feld **Service Level** ein Service Level für Arbeitsaufträge aus.</span><span class="sxs-lookup"><span data-stu-id="05dc7-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="05dc7-115">Wenn Sie dieses Feld leer lassen, machen Sie den generischsten Typ der geplanten Ausführungslinie.</span><span class="sxs-lookup"><span data-stu-id="05dc7-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="05dc7-116">Ein Beispiel für eine generische Zeile finden Sie im ersten Satz in der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="05dc7-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="05dc7-117">Diese Position ermöglicht es, alle Arbeitsaufträge, die keinen Servicegrad für Arbeitsaufträge haben, für ein bestimmtes Datum und eine bestimmte Uhrzeit zu planen.</span><span class="sxs-lookup"><span data-stu-id="05dc7-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="05dc7-118">Wählen Sie im Feld **Geplante Ausführung** das Zeitintervall aus.</span><span class="sxs-lookup"><span data-stu-id="05dc7-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="05dc7-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="05dc7-119">Select **Save**.</span></span>

![Abbildung 1](media/20-setup-for-work-orders.png)
