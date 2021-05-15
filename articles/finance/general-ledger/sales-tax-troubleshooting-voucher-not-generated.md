---
title: Beleg wird nicht generiert
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die helfen können, wenn ein Beleg erzeugt werden sollte, aber nicht erzeugt wird.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947646"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="a83cc-103">Beleg wird nicht generiert</span><span class="sxs-lookup"><span data-stu-id="a83cc-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a83cc-104">Wenn ein Gutschein generiert werden soll, aber auf der Seite **Gutschein-Transaktionen** keine Gutscheine angezeigt werden, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus, um dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="a83cc-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="a83cc-105">[![Seite „Belegtransaktionen, die keine Belege haben“](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="a83cc-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="a83cc-106">Prüfen Sie die Anwendbarkeit der Steuer</span><span class="sxs-lookup"><span data-stu-id="a83cc-106">Check the tax applicability</span></span>

1. <span data-ttu-id="a83cc-107">Gehen Sie zu **Steuern** \> **Periodische Aufgaben** \> **Untergeordnete Sachkonten-Erfassungen, die noch nicht umgelagert wurden**.</span><span class="sxs-lookup"><span data-stu-id="a83cc-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="a83cc-108">Wenn ein Datensatz in der Erfassung vorhanden ist, wählen Sie ihn aus und wählen Sie dann **Jetzt übertragen**.</span><span class="sxs-lookup"><span data-stu-id="a83cc-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="a83cc-109">[![Schaltfläche „Jetzt umlagern“ auf der Seite „Noch nicht umgelagerte Journaleinträge des untergeordneten Sachkontos“](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="a83cc-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="a83cc-110">Öffnen Sie die Seite **Gutschein-Transaktionen** erneut, um zu sehen, ob der Gutschein erzeugt wurde.</span><span class="sxs-lookup"><span data-stu-id="a83cc-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="a83cc-111">Ermitteln Sie, ob eine Anpassung vorliegt</span><span class="sxs-lookup"><span data-stu-id="a83cc-111">Determine whether customization exists</span></span>

<span data-ttu-id="a83cc-112">Wenn Sie die Schritte im vorherigen Abschnitt ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a83cc-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="a83cc-113">Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.</span><span class="sxs-lookup"><span data-stu-id="a83cc-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
