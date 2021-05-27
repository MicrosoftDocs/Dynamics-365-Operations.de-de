---
title: Vorgänge für Qualitätsmängel
description: In diesem Thema wird beschrieben, wie Sie Vorgänge für Qualitätsmängel erstellen und verwenden.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022203"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="e70e9-103">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="e70e9-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e70e9-104">In diesem Thema wird beschrieben, wie Sie Vorgänge für Qualitätsmängel erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="e70e9-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="e70e9-105">Sie können die Seite **Vorgänge** verwenden, um Klassifizierungen der Arbeiten zu definieren, die für einen genehmigten Qualitätsmangel durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="e70e9-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="e70e9-106">Wenn Sie einem Qualitätsmangel einen zugehörigen Vorgang zuweisen, können Sie Details wie das zugehörige Material, die Arbeitsstunden und die Belastungen angeben, die für die Durchführung des Vorgangs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e70e9-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="e70e9-107">Anhand dieser Informationen berechnet das System eine Kalkulation für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e70e9-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="e70e9-108">Die ausführlichen Informationen sowie die vorkalkulierten Kosten dienen lediglich zu Referenzzwecken.</span><span class="sxs-lookup"><span data-stu-id="e70e9-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="e70e9-109">Die zugehörigen Arbeitsgänge für die Qualität unterscheiden sich von den Arbeitsgängen, die für einen Produktionsarbeitsplan definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e70e9-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="e70e9-110">Obwohl Sie Kosten, Zeit und die Elemente verfolgen können, die in einem Vorgang verwendet werden, der mit einem Qualitätsmangel zusammenhängt, haben die von Ihnen eingegebenen Daten nur informativen Charakter.</span><span class="sxs-lookup"><span data-stu-id="e70e9-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="e70e9-111">Es ist nicht automatisch mit dem Hauptbuch, dem untergeordneten Sachkonto oder dem Modul **Zeiterfassung** integriert.</span><span class="sxs-lookup"><span data-stu-id="e70e9-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="e70e9-112">Beispiele für Vorgänge</span><span class="sxs-lookup"><span data-stu-id="e70e9-112">Examples of operations</span></span>

<span data-ttu-id="e70e9-113">Sie arbeiten für eine produzierende Firma.</span><span class="sxs-lookup"><span data-stu-id="e70e9-113">You work for a manufacturing company.</span></span> <span data-ttu-id="e70e9-114">Ein Qualitätsmangel wurde für Elemente erstellt und genehmigt, die einen Qualitätstest nicht bestanden haben.</span><span class="sxs-lookup"><span data-stu-id="e70e9-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="e70e9-115">Eine Korrektur wurde erstellt, um anzuzeigen, dass das Problem mit einem schlechten Lager an einer Maschine zusammenhängt.</span><span class="sxs-lookup"><span data-stu-id="e70e9-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="e70e9-116">Für den Austausch des Lagers sind mehrere Schritte erforderlich, und die Verantwortung für jeden Vorgang wird nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="e70e9-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="e70e9-117">Zum Beispiel könnten die folgenden Schritte erforderlich sein:</span><span class="sxs-lookup"><span data-stu-id="e70e9-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="e70e9-118">Die Zeile wird gestoppt und die Bereinigungsroutine wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e70e9-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="e70e9-119">Wartungspersonal tauscht das Lager aus.</span><span class="sxs-lookup"><span data-stu-id="e70e9-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="e70e9-120">Qualitätssicherungspersonal inspiziert die Maschine, bevor sie wieder eingeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="e70e9-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="e70e9-121">Für dieses Beispiel können die folgenden Vorgänge erstellt werden, um die zu erledigende Arbeit darzustellen:</span><span class="sxs-lookup"><span data-stu-id="e70e9-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="e70e9-122">Stoppen Sie die Produktionslinie.</span><span class="sxs-lookup"><span data-stu-id="e70e9-122">Stop the production line.</span></span>
- <span data-ttu-id="e70e9-123">Bereinigen Sie die Produktionszeile.</span><span class="sxs-lookup"><span data-stu-id="e70e9-123">Clean out the production line.</span></span>
- <span data-ttu-id="e70e9-124">Maschinenwartung durchführen.</span><span class="sxs-lookup"><span data-stu-id="e70e9-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="e70e9-125">Inspizieren Sie die Maschine.</span><span class="sxs-lookup"><span data-stu-id="e70e9-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="e70e9-126">Erzeugen eines Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e70e9-126">Create an operation</span></span>

1. <span data-ttu-id="e70e9-127">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Vorgänge**.</span><span class="sxs-lookup"><span data-stu-id="e70e9-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="e70e9-128">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e70e9-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="e70e9-129">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="e70e9-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="e70e9-130">**Vorgang** – Geben Sie eine eindeutige ID oder einen Namen für den Vorgang ein.</span><span class="sxs-lookup"><span data-stu-id="e70e9-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="e70e9-131">**Beschreibung** – Geben Sie eine detaillierte Beschreibung des Vorgangs ein.</span><span class="sxs-lookup"><span data-stu-id="e70e9-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="e70e9-132">**Typ** – Wenn der Vorgang nur bei Qualitätsmängeln verwendet werden kann, die sich auf einen bestimmten Auftragstyp beziehen, wählen Sie den Auftragstyp (*Einkaufsbestellung* oder *Verkaufsauftrag*).</span><span class="sxs-lookup"><span data-stu-id="e70e9-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="e70e9-133">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e70e9-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e70e9-134">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e70e9-134">Additional resources</span></span>

- [<span data-ttu-id="e70e9-135">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="e70e9-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="e70e9-136">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="e70e9-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="e70e9-137">Erstellen und verarbeiten Sie Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="e70e9-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="e70e9-138">Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="e70e9-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="e70e9-139">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="e70e9-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="e70e9-140">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="e70e9-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="e70e9-141">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="e70e9-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="e70e9-142">Problemtypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="e70e9-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="e70e9-143">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="e70e9-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
