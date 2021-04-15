---
title: Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten
description: In diesem Thema erfahren Sie, wie Sie Lagerarbeitern ermöglichen, alternative Lagerplätze schnell zu finden, wenn kein ausreichender Bestand am Lagerort vorhanden ist.
author: ShylaThompson
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90aeb860dc95a348b000a0f994fadc5cc9aea7e6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814415"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="3f5ad-103">Artikelneuzuordnung für Entnahme mit unzureichender Menge einrichten</span><span class="sxs-lookup"><span data-stu-id="3f5ad-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f5ad-104">In diesem Verfahren erfahren Sie, wie Sie Lagerarbeitern ermöglichen, alternative Lagerplätze schnell zu finden, wenn kein ausreichender Bestand am Lagerort vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="3f5ad-105">Der Neuzuordnungsprozess wird von einer **Arbeitsausnahme** gesteuert und vom **Arbeiter** des Lagerorts verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="3f5ad-106">Es ist möglich, automatische, manuelle oder beide Neuzuordnungsprozesse zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="3f5ad-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="3f5ad-107">Automatische Neuzuordnung – Lagerplatzrichtlinien werden verwendet, um festzustellen, ob die Waren an einem anderen Lagerplatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="3f5ad-108">Wenn möglich, wird die Arbeit aktualisiert und der Lagerbenutzer wird zum alternativen Lagerplatz geleitet.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="3f5ad-109">Manuelle Neuzuordnung – Ermöglicht dem Lagerbenutzer die Auswahl aus einem oder mehreren Lagerplätzen mit nicht reservierten Warenmengen.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="3f5ad-110">Automatisch und manuell – Wenn das System keine automatische Neuzuordnung durchführen kann und Lagerplätze mit nicht reservierten Mengen verfügbar sind, wird der Benutzer aufgefordert, einen Lagerplatz auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="3f5ad-111">Arbeitsausnahmen einrichten</span><span class="sxs-lookup"><span data-stu-id="3f5ad-111">Set up work exceptions</span></span>
<span data-ttu-id="3f5ad-112">Es ist möglich, dass mehrere Arbeitsausnahmen mit unterschiedlichen Artikelneuzuordnungsrichtlinien zu definieren, um den Lagerarbeitern die Auswahl basierend auf den Anforderungen der Lieferung zu ermöglichen, die diese verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="3f5ad-113">Das Demodatenunternehmen USMF wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="3f5ad-114">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Lagerverwaltung > Einrichtung > Arbeit > Arbeitsausnahmen**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="3f5ad-115">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-115">Click **New**</span></span> 
3. <span data-ttu-id="3f5ad-116">Geben Sie im Feld **Arbeitsausnahmencode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="3f5ad-117">Dies ist der Titel dieser Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-117">This will be the title of this exception .</span></span> <span data-ttu-id="3f5ad-118">Beispiel: "Manuelle Entnahme".</span><span class="sxs-lookup"><span data-stu-id="3f5ad-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="3f5ad-119">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="3f5ad-120">Dies ist eine kurze Beschreibung der Verwendung dieser Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="3f5ad-121">Zum Beispiel: Kurze Entnahme – Artikel nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="3f5ad-122">Wählen Sie im Feldtyp **Ausnahme** die Option **Kurze Entnahme** aus.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="3f5ad-123">Aktivieren Sie das Kontrollkästchen **Bestand anpassen**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="3f5ad-124">Wenn es aktiviert ist, wird der Lagerbestand am Kurzentnahmelagerplatz automatisch auf 0 angepasst.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="3f5ad-125">Geben Sie im Feld **Standard-Einstellungsart Code** einen Wert ein oder wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="3f5ad-126">In USMF können Sie beispielsweise **Remove Res Adj Out** auswählen. Jeder Anpassungstypcode enthält vier Merkmale: Name, Beschreibung, Bestandserfassungsname und **Reservierungen entfernen**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="3f5ad-127">Wenn die Option **Reservierungen entfernen** aktiviert ist, werden die Reservierungen der Kurzentnahmebestellposition entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="3f5ad-128">Wählen Sie im Feld **Artikelneuzuordnung** einen Wert aus, zum Beispiel „Manuell“.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="3f5ad-129">Wenn Sie "Manuell" oder "Automatisch und manuell" auswählen, muss der Lagerarbeiter für die manuelle Neuzuordnung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="3f5ad-130">Eine Arbeitskraft für die manuell Artikelneuzuordnung einrichten</span><span class="sxs-lookup"><span data-stu-id="3f5ad-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="3f5ad-131">Das Demodatenunternehmen USMF wurde verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="3f5ad-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-132">Close the page.</span></span>
2. <span data-ttu-id="3f5ad-133">Gehen Sie im Navigationsbereich **Navigationsbereich** zu **Lagerverwaltung > Einrichtung > Arbeiter**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="3f5ad-134">Klicken Sie auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-134">Click **Edit**.</span></span>
4. <span data-ttu-id="3f5ad-135">Wählen Sie in der Liste die Arbeitskraft aus.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-135">In the list, select worker.</span></span> <span data-ttu-id="3f5ad-136">Zum Beispiel Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="3f5ad-137">Erweitern Sie das Inforegister **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="3f5ad-138">Wählen Sie in der Liste eine **Benutzer-ID** aus.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="3f5ad-139">Beispiel: 24.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-139">For example, 24.</span></span>
7. <span data-ttu-id="3f5ad-140">Erweitern Sie das Inforegister **Arbeit**.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="3f5ad-141">Wählen Sie **Ja** im Feld **Manuelle Artikelneuzuordnung zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]