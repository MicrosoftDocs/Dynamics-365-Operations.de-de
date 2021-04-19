---
title: Monatliche Erfassungseinträge in einem Batch erstellen
description: In diesem Thema wird erläutert, wie Sie Journaleinträge in einem Batch erstellen, um die Effizienz bei der Erfassung monatlicher Mietkosten zu steigern.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 664001dd6e9da449dec65750da53d58bd27438b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816027"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="a86b9-103">Monatliche Erfassungseinträge in einem Batch erstellen</span><span class="sxs-lookup"><span data-stu-id="a86b9-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a86b9-104">In diesem Thema wird erläutert, wie Sie Journaleinträge in einem Batch erstellen, um die Effizienz bei der Erfassung monatlicher Mietkosten zu steigern.</span><span class="sxs-lookup"><span data-stu-id="a86b9-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="a86b9-105">Mit der Stapelverarbeitung können Journaleinträge aus mehreren Zeitplänen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a86b9-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="a86b9-106">Diese Journaleinträge können Mietzahlungen, Amortisationen von Verbindlichkeiten, Amortisationen von Nutzungsrechten am Leasingobjekt und Aufwendungen für Nebenkosten beim Leasing umfassen.</span><span class="sxs-lookup"><span data-stu-id="a86b9-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="a86b9-107">Sie können die Stapelverarbeitung auch verwenden, um die erstmalige Erfassung mehrerer Mietverträge gleichzeitig durchzuführen oder Übergangsanpassungen für mehrere Mietverträge gleichzeitig zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a86b9-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="a86b9-108">Um einen Batch-Auftrag einzurichten oder Zahlungsrechnungen, Abschreibungen oder Zinsen für mehrere Mietverträge zu verarbeiten, gehen Sie zu **Anlagenleasing \> Periodisch \> Batch-Erfassungserstellung**.</span><span class="sxs-lookup"><span data-stu-id="a86b9-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="a86b9-109">Im daraufhin angezeigten Dialogfeld können Sie den Zeitplan auswählen, nach dem die Journaleinträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a86b9-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="a86b9-110">Sie können auch angeben, ob der Stapelverarbeitungsvorgang für bestimmte Entitäten, Mietvertragsgruppen oder Leasingbücher ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a86b9-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="a86b9-111">Nachfolgende Transaktionen, wie z. B. Tilgungspläne für Verbindlichkeiten, Zahlungen, Abschreibungen und Aufwendungen, werden erst gebucht, nachdem die erstmalige Erfassung für entsprechende Mietverträge gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="a86b9-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="a86b9-112">Die Journaleinträge werden erstellt, aber erst gebucht, wenn Sie den **Ausführen**-Befehl auswählen.</span><span class="sxs-lookup"><span data-stu-id="a86b9-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]