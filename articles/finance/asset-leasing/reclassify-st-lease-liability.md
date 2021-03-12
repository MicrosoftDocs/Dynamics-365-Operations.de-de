---
title: Den kurzfristigen Anteil einer Leasingverbindlichkeit umgliedern
description: In diesem Thema wird erläutert, wie Sie einen monatlichen Journaleintrag erstellen, um einen Teil der Leasingverbindlichkeit als kurzfristig zu umzugliedern.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 08ca824bb4c4a02a80f2187fb5f8fe4e8b7327c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992913"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="8b810-103">Den kurzfristige Anteil der Leasingverbindlichkeit umgliedern</span><span class="sxs-lookup"><span data-stu-id="8b810-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b810-104">In diesem Thema wird erläutert, wie Sie einen monatlichen Journaleintrag erstellen, um einen Teil der Leasingverbindlichkeit als kurzfristig zu umzugliedern.</span><span class="sxs-lookup"><span data-stu-id="8b810-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="8b810-105">Wenn der im Stapelverarbeitungsvorgang ausgewählte Zeitplan **Umgliederung der kurzfristigen Leasingverbindlichkeit** ist, wird ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="8b810-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="8b810-106">Dieser Eintrag wird verwendet, um den aktuellen Teil der Leasingverbindlichkeit am letzten Tag des Monats zu buchen.</span><span class="sxs-lookup"><span data-stu-id="8b810-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="8b810-107">Gleichzeitig wird ab dem ersten Tag des nächsten Monats eine Stornobuchung gebucht.</span><span class="sxs-lookup"><span data-stu-id="8b810-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="8b810-108">Der kurzfristige Teil der Leasingverbindlichkeit wird im Tilgungsplan für Verbindlichkeiten ausgewiesen.</span><span class="sxs-lookup"><span data-stu-id="8b810-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="8b810-109">Wenn der Journaleintrag gebucht wird, wird die **Umgliederungserfassung für Verbindlichkeiten erstellt**-Spalte verfügbar, und die Erfassungs-ID wird ebenfalls in den Zeitplan eingetragen.</span><span class="sxs-lookup"><span data-stu-id="8b810-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="8b810-110">Führen Sie die folgenden Schritte aus, um den Journaleintrag für die kurzfristige Umgliederung von Verbindlichkeiten zu erstellen und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="8b810-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="8b810-111">Gehen Sie zu **Anlagenleasing \> Periodisch \> Batch-Erfassungserstellung**.</span><span class="sxs-lookup"><span data-stu-id="8b810-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="8b810-112">Wählen Sie in dem **Batch-Erfassungserstellung**-Dialogfeld im **Zeitplan auswählen**-Feld **Umgliederung der kurzfristigen Leasingverbindlichkeit** aus.</span><span class="sxs-lookup"><span data-stu-id="8b810-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="8b810-113">Wählen Sie im Feld **Leasinggruppe** eine Leasinggruppe aus.</span><span class="sxs-lookup"><span data-stu-id="8b810-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="8b810-114">Wählen Sie alternativ im **Buch-ID**-Feld die Buch-ID aus.</span><span class="sxs-lookup"><span data-stu-id="8b810-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="8b810-115">Aktivieren Sie den **Buchen**-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b810-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="8b810-116">Wenn der Eintrag erstellt, aber nicht gebucht werden soll, lassen Sie diesen Parameter alternativ deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8b810-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="8b810-117">Aktivieren Sie den **Vorschau vor dem Buchen**-Parameter, um den Eintrag anzuzeigen, bevor er gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="8b810-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="8b810-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b810-118">Select **OK**.</span></span>
