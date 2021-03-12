---
title: Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen
description: In diesem Thema wird beschrieben, wie Sie einen Stapelverarbeitungsauftrag einrichten, der ausgehende Transportauftragslieferungen für versandfertige Ladungen automatisch bestätigt.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996300"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="6653b-103">Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen</span><span class="sxs-lookup"><span data-stu-id="6653b-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6653b-104">In diesem Thema wird beschrieben, wie Sie einen Stapelverarbeitungsauftrag einrichten, der ausgehende Transportauftragslieferungen für versandfertige Ladungen automatisch bestätigt.</span><span class="sxs-lookup"><span data-stu-id="6653b-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="6653b-105">Der hier beschriebene Stapelverarbeitungsauftrag gilt nur für Transportauftragssendungen, nicht für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="6653b-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="6653b-106">Aktivieren Sie die Funktion Ausgehende Lieferungen bestätigen in der Funktion Stapelverarbeitungsaufträge</span><span class="sxs-lookup"><span data-stu-id="6653b-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="6653b-107">Bevor Sie diese Funktion nutzen können, müssen Sie diese auf Ihrem System aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6653b-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="6653b-108">Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6653b-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="6653b-109">Die Funktion ist aufgeführt als:</span><span class="sxs-lookup"><span data-stu-id="6653b-109">The feature is listed as:</span></span>

- <span data-ttu-id="6653b-110">**Modul** - *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="6653b-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="6653b-111">**Funktionsname** - *Ausgehende Lieferungen aus Stapelverarbeitungsaufträgen bestätigen*</span><span class="sxs-lookup"><span data-stu-id="6653b-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="6653b-112">Ausgehende Lieferungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="6653b-112">Process outbound shipments</span></span>

<span data-ttu-id="6653b-113">Um einen geplanten Stapelverarbeitungsauftrag einzurichten, um die Bestätigung für eine ausgehende Lieferung für versandfertige Ladungen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="6653b-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="6653b-114">Gehen Sie zu **Lagerortverwaltung \> Periodische Aufgaben \> Ausgehende Sendungen verarbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6653b-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="6653b-115">Das Dialogfeld **Lieferung bestätigen** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6653b-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="6653b-116">Wählen Sie auf der Seite **Einschließende Datensätze** Inforegister die Option **Filter**.</span><span class="sxs-lookup"><span data-stu-id="6653b-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="6653b-117">Das Abfrage-Editor-Dialogfeld öffnet sich.</span><span class="sxs-lookup"><span data-stu-id="6653b-117">The query editor dialog box opens.</span></span> <span data-ttu-id="6653b-118">Fügen Sie in der Registerkarte **Bereich** eine Zeile mit den folgenden Werten hinzu:</span><span class="sxs-lookup"><span data-stu-id="6653b-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="6653b-119">**Tabelle** - *Ladungen*</span><span class="sxs-lookup"><span data-stu-id="6653b-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="6653b-120">**Abgeleitete Tabelle** - *Ladungen*</span><span class="sxs-lookup"><span data-stu-id="6653b-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="6653b-121">**Feld** - *Ladungsstatus*</span><span class="sxs-lookup"><span data-stu-id="6653b-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="6653b-122">**Kriterien** - *Geladen*</span><span class="sxs-lookup"><span data-stu-id="6653b-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="6653b-123">Wählen Sie **OK**, um zum Dialogfeld **Lieferung bestätigen** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="6653b-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="6653b-124">Im Inforegister **Im Hintergrund ausführen** setzen Sie **Stapelverarbeitung** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6653b-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="6653b-125">Wählen Sie im Inforegister **Im Hintergrund ausführen** **Serie**.</span><span class="sxs-lookup"><span data-stu-id="6653b-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="6653b-126">Das Dialogfeld **Serie festlegen** öffnet sich.</span><span class="sxs-lookup"><span data-stu-id="6653b-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="6653b-127">Legen Sie den passenden Zeitplan für Ihr Unternehmen fest.</span><span class="sxs-lookup"><span data-stu-id="6653b-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="6653b-128">Wählen Sie **OK**, um zum Dialogfeld **Lieferung bestätigen** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="6653b-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="6653b-129">Wählen Sie **OK** im Dialogfeld **Lieferung bestätigen**, um den Stapelverarbeitungsauftrag der Wartestelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6653b-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="6653b-130">Weitere Informationen finden Sie unter [Stapelverarbeitung – Übersicht](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6653b-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
