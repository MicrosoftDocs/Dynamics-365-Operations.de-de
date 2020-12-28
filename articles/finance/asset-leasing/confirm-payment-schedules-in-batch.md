---
title: Bestätigen Sie die Zahlungspläne für Mietzahlungen in einem Batch
description: In diesem Thema wird erläutert, wie Sie mehrere Zahlungspläne in einem Batch bestätigen.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b5a90b96ac598d145e2b0697627de04731b55f59
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443777"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="c87f0-103">Bestätigen Sie die Zahlungspläne für Mietzahlungen in einem Batch</span><span class="sxs-lookup"><span data-stu-id="c87f0-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c87f0-104">In diesem Thema wird erläutert, wie Sie mehrere Zahlungspläne in einem Batch bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c87f0-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="c87f0-105">Zahlungspläne werden entweder auf einer Mietvertrag-zu-Mietvertrag-Basis oder über den Bestätigungsstapelverarbeitungsvorgang bestätigt.</span><span class="sxs-lookup"><span data-stu-id="c87f0-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="c87f0-106">Ein Journaleintrag kann nur für einen Mietvertrag gebucht werden, für den ein Zahlungsplan bestätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="c87f0-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="c87f0-107">Die Bestätigung des Zahlungsplans dient als endgültige Genehmigung der Finanzinformationen für den Mietvertrag.</span><span class="sxs-lookup"><span data-stu-id="c87f0-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="c87f0-108">Alle zukünftigen Änderungen der Finanzinformationen für den Mietvertrag, wie z. B. Zahlungen und die Laufzeit des Mietvertrags, stellen eine Mietregulierung dar und sollten auf diese Weise verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="c87f0-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="c87f0-109">Führen Sie die folgenden Schritte aus, um mehrere Zahlungspläne zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c87f0-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="c87f0-110">Gehen Sie zu **Anlagenleasing \> Periodisch \> Bestätigungs-Batch**.</span><span class="sxs-lookup"><span data-stu-id="c87f0-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="c87f0-111">Auf der **Bestätigungs-Batch**-Seite wählen Sie **Bestätigungs-Batch** aus.</span><span class="sxs-lookup"><span data-stu-id="c87f0-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="c87f0-112">Filtern Sie im angezeigten Dialogfeld nach den Büchern, die Sie bestätigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c87f0-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="c87f0-113">Um alle Bücher in einer bestimmten Leasinggruppe zu bestätigen, wählen Sie die Gruppe im **Leasinggruppe**-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="c87f0-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="c87f0-114">Um bestimmte Bücher zu bestätigen, wählen Sie die Bücher im **Buch-ID**-Feld aus.</span><span class="sxs-lookup"><span data-stu-id="c87f0-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="c87f0-115">Um alle Bücher zu bestätigen, aktivieren Sie den **Für alle Bücher**-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c87f0-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="c87f0-116">Informationen zu den neu bestätigten Büchern finden Sie auf der **Bestätigte Bücher**-Seite.</span><span class="sxs-lookup"><span data-stu-id="c87f0-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="c87f0-117">Nachdem die Zahlungspläne bestätigt wurden, können die Journaleinträge der erstmaligen Erfassung für die Mietverträge gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="c87f0-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
