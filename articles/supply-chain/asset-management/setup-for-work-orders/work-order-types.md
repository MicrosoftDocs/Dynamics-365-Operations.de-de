---
title: Arbeitsauftragstypen
description: In diesem Thema werden die Arbeitsauftragsarten im Anlagenmanagement erläutert.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 561ca87740d90590262716f0042fca6b59dafc69
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223529"
---
# <a name="work-order-types"></a><span data-ttu-id="b356a-103">Arbeitsauftragstypen</span><span class="sxs-lookup"><span data-stu-id="b356a-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b356a-104">Arbeitsauftragsarten werden zur Kategorisierung von Arbeitsaufträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b356a-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="b356a-105">Beispielsweise können Sie Arbeitsaufträge haben, die sich auf vorbeugende Instandhaltung oder korrektive Instandhaltung beziehen.</span><span class="sxs-lookup"><span data-stu-id="b356a-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="b356a-106">Ein Arbeitsauftragstyp definiert eine Zugehörigkeit zu einem Arbeitsauftrags-Lebenszyklusmodell.</span><span class="sxs-lookup"><span data-stu-id="b356a-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="b356a-107">Ein Arbeitsauftrags-Lebenszyklusmodell definiert die Arbeitsauftrags-Lebenszykluszustände, die auf einem Arbeitsauftrag festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="b356a-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="b356a-108">(Beispiele für Lebenszykluszustände von Arbeitsaufträgen sind **Erstellt**, **In Bearbeitung** und **Fertig**.)</span><span class="sxs-lookup"><span data-stu-id="b356a-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="b356a-109">Weitere Informationen über den Lebenszyklus von Arbeitsaufträgen und Projektphasen finden Sie unter [Lebenszykluszustand von Arbeitsaufträgen](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="b356a-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="b356a-110">Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Arbeitsaufträge** \> **Arbeitsauftragsarten**.</span><span class="sxs-lookup"><span data-stu-id="b356a-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="b356a-111">Wählen Sie **Neu**, um einen Arbeitsauftragstyp anzulegen.</span><span class="sxs-lookup"><span data-stu-id="b356a-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="b356a-112">Geben Sie im Feld **Arbeitsauftragsart** eine ID für die Arbeitsauftragsart ein.</span><span class="sxs-lookup"><span data-stu-id="b356a-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="b356a-113">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="b356a-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="b356a-114">Wählen Sie im Feld **Lebenszyklusmodell Arbeitsauftrag** ein Lebenszyklusmodell aus.</span><span class="sxs-lookup"><span data-stu-id="b356a-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="b356a-115">Setzen Sie die Option **Ein Wartungsarbeiter** auf **Ja**, wenn alle Arbeitsaufträge, die sich auf einen Arbeitsauftrag dieses Typs beziehen, auf denselben Wartungsarbeiter terminiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b356a-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="b356a-116">Wählen Sie im Feld **Kostenart** **Korrektur**, **Präventiv** oder **Investition**.</span><span class="sxs-lookup"><span data-stu-id="b356a-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="b356a-117">Alle Arbeitsaufträge auf einem Arbeitsauftrag müssen die gleiche Kostenart haben.</span><span class="sxs-lookup"><span data-stu-id="b356a-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="b356a-118">Setzen Sie im Abschnitt **Pflicht** die entsprechenden Optionen auf **Ja**, um festzulegen, welche fehler- oder wartungsbezogenen Informationen zu einem solchen Arbeitsauftrag hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b356a-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b356a-119">Die Optionen im Abschnitt **Pflicht** beziehen sich auf die Optionen auf der **Validieren** FastTab der **Lebenszykluszustände von Arbeitsaufträgen** Seite (**Anlagenmanagement** \> **Einrichtung** \> **Aufträge** \> **Lebenszykluszustände**).</span><span class="sxs-lookup"><span data-stu-id="b356a-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="b356a-120">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b356a-120">Select **Save**.</span></span>

![Arbeitsauftragstypen](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]