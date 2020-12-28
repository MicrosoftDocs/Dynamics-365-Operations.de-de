---
title: Leasingerfassungsnamen einrichten
description: In diesem Thema wird erläutert, wie Sie Namen von Leasingerfassungen definieren. Namen von Leasingerfassungen geben die Erfassungen an, in die Einträge gebucht werden, die aus dem Anlagenleasing stammen.
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
ms.openlocfilehash: e8b1b908dfd6d1d6072b6efa83f13ae5784c85c1
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443765"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="779d9-104">Leasingerfassungsnamen einrichten</span><span class="sxs-lookup"><span data-stu-id="779d9-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="779d9-105">Namen von Leasingerfassungen geben die Erfassungen an, in die Transaktionen der Anlagenleasing gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="779d9-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="779d9-106">Nur Erfassungsnamen, die dem **Anlagenleasing**-Erfassungstyp zugeordnet sind, werden in den **Erstmalige Erfassung**- und **Name der monatlichen Erfassung**-Feldern auf der **Parameter für das Anlagenleasing**-Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="779d9-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="779d9-107">Nur der **Kreditorenechnungserfassung**-Erfassungstyp kann dem **Name der Rechnungserfassung**-Feld zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="779d9-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="779d9-108">Führen Sie die folgenden Schritte aus, um die Namen der Leasingerfassung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="779d9-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="779d9-109">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="779d9-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="779d9-110">Auf der **Allgemeines**-Registerkarte im **Name der Erfassung der erstmaligen Erfassung**-Feld wählen Sie eine Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="779d9-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="779d9-111">Alle Journaleinträge der erstmaligen Erfassung werden unter diesem Erfassungsnamen gebucht.</span><span class="sxs-lookup"><span data-stu-id="779d9-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="779d9-112">Wählen Sie im Feld **Rechnungserfassungsname** eine Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="779d9-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="779d9-113">Wenn die **An den Kreditor bezahlen**-Option für das Leasingbuch auf **Ja** festgelegt ist, werden Rechnungen für Miet- und Ausgabenzahlungen unter diesem Erfassungsnamen gebucht.</span><span class="sxs-lookup"><span data-stu-id="779d9-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="779d9-114">Wählen Sie im Feld **Leasingerfassungsname** eine Erfassung aus.</span><span class="sxs-lookup"><span data-stu-id="779d9-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="779d9-115">Alle Abschreibungs-, Zins- und kurzfristigen Umgliederungseinträge werden unter diesem Erfassungsnamen gebucht.</span><span class="sxs-lookup"><span data-stu-id="779d9-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="779d9-116">Wenn die **An den Kreditor bezahlen**-Option für das Leasingbuch auf **Nein** festgelegt ist, werden Einträge für Miet- und Ausgabenzahlungen auch unter diesem Erfassungsnamen gebucht.</span><span class="sxs-lookup"><span data-stu-id="779d9-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>
