---
title: Geplante Ausführung
description: In diesem Abschnitt wird die planmäßige Ausführung im Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a6d1761202697f62421bbf288c7e22efe559a986
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022406"
---
# <a name="scheduled-execution"></a><span data-ttu-id="28592-103">Geplante Ausführung</span><span class="sxs-lookup"><span data-stu-id="28592-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="28592-104">Sie können die Service Levels für Arbeitsaufträge verwenden, um die geplante Ausführung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="28592-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="28592-105">(Weitere Informationen zu den Service Levels der Arbeitsaufträge finden Sie unter [Service Level und Beschreibung](service-level-and-description.md).) Die planmäßige Ausführung bietet Flexibilität bei der Arbeitsplanung für Instandhalter, da Sie für das Intervall, in dem ein Arbeitsauftrag abgeschlossen werden soll, detailliertere oder weniger detaillierte Anforderungen einrichten können.</span><span class="sxs-lookup"><span data-stu-id="28592-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="28592-106">So kann beispielsweise ein Wartungsmitarbeiter, der einen Auftrag in einer Produktionsstätte schneller als erwartet erledigt, zu einem anderen nahegelegenen Auftrag wechseln, der für die aktuelle Woche geplant war, aber nicht unbedingt für den aktuellen Tag.</span><span class="sxs-lookup"><span data-stu-id="28592-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="28592-107">Dieser Ansatz ermöglicht die Optimierung der Arbeitsvorbereitung und der Auftragsabwicklung.</span><span class="sxs-lookup"><span data-stu-id="28592-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="28592-108">Die Einrichtung der geplanten Ausführung, die sich auf Arbeitsaufträge bezieht, kann generisch oder spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="28592-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="28592-109">Sie können generische Zeilen einrichten, die nicht auf bestimmte Arbeitsauftragsarten, Anlagentypen usw. beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="28592-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="28592-110">Alternativ können Sie auch geplante Ausführungspositionen erstellen, die sich auf eine bestimmte Arbeitsauftragsart, Anlagenart, Wartungsauftragsart usw. beziehen.</span><span class="sxs-lookup"><span data-stu-id="28592-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="28592-111">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Arbeitsaufträge** \> **Planausführung**.</span><span class="sxs-lookup"><span data-stu-id="28592-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="28592-112">Wählen Sie **Neu**, um eine geplante Ausführungsposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="28592-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="28592-113">Wählen Sie in den Feldern **Technischer Standort**, **Auftragsart**, **Assettyp**, **Hersteller**, **Modell**, **Wartungsauftragstyp Kategorie**, **Wartungsauftragstyp**, **Wartungsauftragstyp Variante** und **Wechseln** die gewünschten Werte aus.</span><span class="sxs-lookup"><span data-stu-id="28592-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="28592-114">Wählen Sie im Feld **Service Level** ein Service Level für Arbeitsaufträge aus.</span><span class="sxs-lookup"><span data-stu-id="28592-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="28592-115">Wenn Sie dieses Feld leer lassen, machen Sie den generischsten Typ der geplanten Ausführungslinie.</span><span class="sxs-lookup"><span data-stu-id="28592-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="28592-116">Ein Beispiel für eine generische Zeile finden Sie im ersten Satz in der folgenden Abbildung.</span><span class="sxs-lookup"><span data-stu-id="28592-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="28592-117">Diese Position ermöglicht es, alle Arbeitsaufträge, die keinen Servicegrad für Arbeitsaufträge haben, für ein bestimmtes Datum und eine bestimmte Uhrzeit zu planen.</span><span class="sxs-lookup"><span data-stu-id="28592-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="28592-118">Wählen Sie im Feld **Geplante Ausführung** das Zeitintervall aus.</span><span class="sxs-lookup"><span data-stu-id="28592-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="28592-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="28592-119">Select **Save**.</span></span>

![Geplante Ausführung](media/20-setup-for-work-orders.png)
