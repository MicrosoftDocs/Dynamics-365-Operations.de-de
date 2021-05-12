---
title: Lagerortparameter für Wellenverarbeitung
description: In diesem Thema wird beschrieben, wie Lagerortparameter für Wellenverarbeitung eingerichtet werden. Sie können Wellenverarbeitung verwenden, um Entnahmearbeit für mehrere Arbeitsaufträge in eine einzige Welle zu gruppieren.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 77513185a3323a2e78f641d25b86b2896f9f7881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838009"
---
# <a name="warehouse-parameters-for-wave-processing"></a><span data-ttu-id="a34da-104">Lagerortparameter für Wellenverarbeitung</span><span class="sxs-lookup"><span data-stu-id="a34da-104">Warehouse parameters for wave processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a34da-105">In diesem Thema wird beschrieben, wie Lagerortparameter für Wellenverarbeitung eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-105">This topic describes how to set up warehouse parameters for wave processing.</span></span> <span data-ttu-id="a34da-106">Sie können Wellenverarbeitung verwenden, um Entnahmearbeit für mehrere Arbeitsaufträge in eine einzige Welle zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="a34da-106">You can use wave processing to group picking work for multiple work orders into a single wave.</span></span>

<span data-ttu-id="a34da-107">Um die Wellenverarbeitung zu verwenden, geben Sie auf der Seite **Lagerortverwaltungsparameter** Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="a34da-107">To use wave processing, specify the following on the **Warehouse management parameters** page:</span></span>

- <span data-ttu-id="a34da-108">Ob Sie Wellen bearbeiten können, indem Sie einen Stapelverarbeitungsauftrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="a34da-108">If you can process waves by using a batch job.</span></span>
- <span data-ttu-id="a34da-109">Ob Sie Informationen in einer Protokolldatei sammeln, wenn Wellen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-109">If you collect information in a log file when waves are processed.</span></span>

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a><span data-ttu-id="a34da-110">Lagerortverwaltungsparameter für Wellenverarbeitung einrichten</span><span class="sxs-lookup"><span data-stu-id="a34da-110">Set up warehouse management parameters for wave processing</span></span>

<span data-ttu-id="a34da-111">Um Lagerortparameter für Wellenverarbeitung einzurichten, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a34da-111">To set up warehouse parameters for wave processing, follow these steps:</span></span>

1. <span data-ttu-id="a34da-112">Gehen Sie zu **Lagerortverwaltung** \> **Einstellungen** \> **Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="a34da-112">Go to **Warehouse management** \> **Setup** \> **Warehouse management parameters**.</span></span>

1. <span data-ttu-id="a34da-113">Nehmen Sie im Inforegister **Wellenverarbeitung** die folgenden Einstellungen vor:</span><span class="sxs-lookup"><span data-stu-id="a34da-113">On the **Wave processing** FastTab, make the following settings:</span></span>

    - <span data-ttu-id="a34da-114">**Wellenverarbeitungs-Stapelverarbeitungsgruppe** – Wählen Sie die Stapelverarbeitungsgruppe aus, die verwendet wird, wenn Sie Wellen verarbeiten, indem Stapelverarbeitungsaufträge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-114">**Wave processing batch group** - Select the batch group to use when you process waves by using batch jobs.</span></span> <span data-ttu-id="a34da-115">Die Stapelverarbeitungsgruppe gibt den Server an, auf dem Stapelverarbeitungsaufträge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-115">The batch group specifies the server that batch jobs will run on.</span></span>
    - <span data-ttu-id="a34da-116">**Wellen in einem Stapel verarbeiten** – Wählen Sie aus, ob Wellen automatisch mit einem Stapelverarbeitungsauftrag verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a34da-116">**Process waves in batch** - Choose whether to enable waves to be automatically processed by a batch job.</span></span> <span data-ttu-id="a34da-117">Sie müssen hier *Ja* einstellen, um eine parallele Verarbeitung verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="a34da-117">You must set this to *Yes* to use parallel processing.</span></span> <span data-ttu-id="a34da-118">Sie richten den Stapelverarbeitungsauftrag auf der Seite **Wellen verarbeiten** ein.</span><span class="sxs-lookup"><span data-stu-id="a34da-118">You set up the batch job on the **Process waves** page.</span></span> <span data-ttu-id="a34da-119">(Siehe auch den Hinweis am Ende dieser Liste.)</span><span class="sxs-lookup"><span data-stu-id="a34da-119">(See also the note at the end of this list.)</span></span>
    - <span data-ttu-id="a34da-120">**Wellenfortschrittsprotokoll erstellen** – Wählen Sie aus, ob das System immer einen Protokolldatensatz erstellen soll, wenn eine Zuteilung für einen Artikel und dessen Dimensionen beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="a34da-120">**Create wave progress log** - Choose whether the system should generate a log record every time allocation for an item and its dimensions begins and ends.</span></span> <span data-ttu-id="a34da-121">Sie sollten dieses Protokoll nur aktivieren, wenn Sie es benötigen, z. B. während des ersten Tests oder zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="a34da-121">You should only enable this log when you need it, for example, during initial testing or for troubleshooting.</span></span> <span data-ttu-id="a34da-122">Weitere Informationen finden Sie unter [Wellenzuteilung](wave-allocation-method.md).</span><span class="sxs-lookup"><span data-stu-id="a34da-122">For more information, see [Wave allocation](wave-allocation-method.md).</span></span>
    - <span data-ttu-id="a34da-123">**Protokoll für Wellenverarbeitungsverlauf erstellen** – Wählen Sie aus, ob Informationen zu einer Welle nach der Verarbeitung der Welle automatisch in einer Protokolldatei gespeichert werden sollen, auch während der parallelen Verarbeitung ausstehender Zuteilungen.</span><span class="sxs-lookup"><span data-stu-id="a34da-123">**Create wave processing history log** - Choose whether to automatically save information about a wave in a log file after the wave is processed, including during the parallel processing of pending allocations.</span></span> <span data-ttu-id="a34da-124">Normalerweise sollten Sie dies nur während der Problembehandlung aktivieren, da dies einen Mehraufwand verursacht.</span><span class="sxs-lookup"><span data-stu-id="a34da-124">Typically you should only enable this during troubleshooting because it adds extra overhead.</span></span> <span data-ttu-id="a34da-125">Um das Protokoll anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Protokoll für Wellenverarbeitungsablauf**.</span><span class="sxs-lookup"><span data-stu-id="a34da-125">To view the log, go to **Warehouse management \> Outbound waves \> Wave processing history log**.</span></span> <span data-ttu-id="a34da-126">Weitere Informationen finden Sie unter [Wellen erstellen und verarbeiten](wave-processing.md).</span><span class="sxs-lookup"><span data-stu-id="a34da-126">For more information, see [Wave creation and processing](wave-processing.md).</span></span>
    - <span data-ttu-id="a34da-127">**Containerisierungsverlaufsprotokoll** – Wählen Sie aus, ob Informationen zur Containerisierung für eine Welle nach der Verarbeitung der Welle automatisch in einer Protokolldatei gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a34da-127">**Create containerization history log** - Choose whether to automatically save information about containerization for a wave in a log file after the wave is processed.</span></span> <span data-ttu-id="a34da-128">Um das Protokoll anzuzeigen, gehen Sie zu **Lagerortverwaltung \> Verpackung und Containerisierung \> Containerisierungsverlauf**.</span><span class="sxs-lookup"><span data-stu-id="a34da-128">To view the log, go to **Warehouse management \> Packing and containerization \> Containerization history**.</span></span>
    - <span data-ttu-id="a34da-129">**Auf Sperre (ms) warten** – Geben Sie die Uhrzeit ein, in Millisekunden, die ein Zuteilungsschritt auf eine Systemressource wartet, die von einem anderen Zuteilungsschritt gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="a34da-129">**Wait for lock (ms)** - Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="a34da-130">Bei Überschreitung dieser Zeit wird, wird die Welle nicht verarbeitet und eine Fehlermeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a34da-130">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span>

1. <span data-ttu-id="a34da-131">Nehmen Sie auf dem Inforegister **An Lager freigeben** folgende Einstellung vor:</span><span class="sxs-lookup"><span data-stu-id="a34da-131">On the **Release to warehouse** FastTab, make the following setting:</span></span>

    - <span data-ttu-id="a34da-132">**Fehler zu fehlgeschlagener Stapelverarbeitung** – Wählen Sie aus, ob ein Fehler generiert werden soll, wenn eine Freigabe für eine Lagerortstapelverarbeitung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a34da-132">**Error on batch failure** - Choose whether to generate an error when a release to warehouse batch job fails.</span></span> <span data-ttu-id="a34da-133">Wenn dies aktiviert ist, enden fehlgeschlagene Aufträge mit dem Status *Fehler*.</span><span class="sxs-lookup"><span data-stu-id="a34da-133">If this is enabled, failed jobs will end with a status of *Error*.</span></span> <span data-ttu-id="a34da-134">Wenn dies deaktiviert ist, enden fehlgeschlagene Aufträge mit dem Status *Beendet*.</span><span class="sxs-lookup"><span data-stu-id="a34da-134">If this is disabled, failed jobs will end with a status of *Ended*.</span></span>

> [!NOTE]
> <span data-ttu-id="a34da-135">Auf der Wellenvorlage, die verwendet wird, um die Welle zu verarbeiten, können Sie die Einstellungen angeben, die das Wellenverarbeiten automatisieren.</span><span class="sxs-lookup"><span data-stu-id="a34da-135">On the wave template that is used to process the wave, you can specify the settings that automate wave processing.</span></span> <span data-ttu-id="a34da-136">Wenn Sie einen Zeitplan für den Batchauftrag einrichten, sollten Sie den Zeitpunkt mit den Einstellungen für Automatisieren in der Wellenvorlage koordinieren.</span><span class="sxs-lookup"><span data-stu-id="a34da-136">If you set up a schedule for the batch job, you should coordinate the timing with the settings for automation in the wave template.</span></span> <span data-ttu-id="a34da-137">Weitere Informationen finden Sie unter [Wellenvorlage erstellen](wave-templates.md).</span><span class="sxs-lookup"><span data-stu-id="a34da-137">For more information, see [Create a wave template](wave-templates.md).</span></span>
>
> <span data-ttu-id="a34da-138">Wenn Sie *Transportverwaltung* und *Erweiterte Lagerortverwaltung* verwenden, können Sie angeben, ob Ladungen konsolidiert werden, wenn Sie eine Welle verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a34da-138">If you are using *Transportation management* and *Advanced warehouse management*, you can specify whether to consolidate loads when you process a wave.</span></span> <span data-ttu-id="a34da-139">Beispielsweise ist dieses hilfreich, wenn mehrere kleinere Ladung gleichzeitig versendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a34da-139">For example, this is useful when several small loads can be shipped at the same time.</span></span> <span data-ttu-id="a34da-140">Um Ladungen zu konsolidieren, wenn Sie eine Welle verarbeiten, klicken Sie auf die Registerkarte **Ladungen** und wählen Sie das Kontrollkästchen **Ladungen während der Wellenverarbeitung konsolidieren** aus.</span><span class="sxs-lookup"><span data-stu-id="a34da-140">To consolidate loads when you process a wave, on the **Loads** tab, select the **Consolidate loads during wave processing** check box.</span></span></P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a><span data-ttu-id="a34da-141">Einrichten einer vollständigen oder teilweisen Reservierung für Produktionswellen</span><span class="sxs-lookup"><span data-stu-id="a34da-141">Set up full or partial reservation for production waves</span></span>

<span data-ttu-id="a34da-142">Bei Aufträgen und Kanbanaufträgen muss Lagerbestand reserviert werden, bevor der Auftrag an den Lagerort freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a34da-142">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="a34da-143">Andernfalls können die Artikel oder der Verteilungspositionen nicht in einer Welle verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-143">Otherwise, the items or allocation lines cannot be processed in a wave.</span></span> <span data-ttu-id="a34da-144">Einige Produktionsaufträge sind jedoch etwas flexibler.</span><span class="sxs-lookup"><span data-stu-id="a34da-144">However, production orders are slightly more flexible.</span></span> <span data-ttu-id="a34da-145">Bei Produktionsaufträgen kann Folgendes angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="a34da-145">For production orders, you can specify the following:</span></span>

- <span data-ttu-id="a34da-146">Zulassen, dass Produktionsaufträge für den Lagerort freigegeben werden, obwohl nicht alle Materialien reserviert werden können.</span><span class="sxs-lookup"><span data-stu-id="a34da-146">Allow production orders to be released to the warehouse although all materials cannot be reserved.</span></span> <span data-ttu-id="a34da-147">Wenn Sie diese Option auswählen, müssen Sie den Prozess der Freigabe für den Lagerort manuell wiederholen, wenn die zusätzlichen Materialien verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-147">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span> <span data-ttu-id="a34da-148">Dies ist beispielsweise hilfreich, wenn Sie die Materialien haben, die Sie zum Starten der Produktion benötigen, und warten können, bis die zusätzlichen Materialien verfügbar werden.</span><span class="sxs-lookup"><span data-stu-id="a34da-148">For example, this is useful if you have the materials that you need to start a production, and can wait until the additional materials become available.</span></span>
- <span data-ttu-id="a34da-149">Anfordern, dass alle Materialien reserviert werden, bevor ein Auftrag für den Lagerort freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a34da-149">Require that all materials are reserved before an order can be released to the warehouse.</span></span>

<span data-ttu-id="a34da-150">Um vollständige Reservierung anzufordern oder teilweise Reservierung zu ermöglichen, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a34da-150">To require full reservation or allow partial reservation, follow these steps:</span></span>

1. <span data-ttu-id="a34da-151">Wechseln Sie zu **Produktionssteuerung** \> **Einstellungen** \> **Produktionssteuerungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="a34da-151">Go to **Production control** \> **Setup** \> **Production control parameters**.</span></span>
1. <span data-ttu-id="a34da-152">Wählen Sie auf der Registerkarte **Allgemein** im Feld **An Lager freigeben** die Standardeinstellung aus.</span><span class="sxs-lookup"><span data-stu-id="a34da-152">On the **General** tab, in the **Release to warehouse** field, select the default setting.</span></span>