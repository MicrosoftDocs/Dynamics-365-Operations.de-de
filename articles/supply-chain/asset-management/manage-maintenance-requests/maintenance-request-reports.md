---
title: Wartungsanfrageberichte
description: In diesem Thema wird erläutert, wie Wartungsanfrageberichte in Asset Management erstellt werden.
author: josaw1
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f5f1860907e3cc3c4830cc385771d5924c609ea6
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847527"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="f2127-103">Wartungsanfrageberichte</span><span class="sxs-lookup"><span data-stu-id="f2127-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f2127-104">In Asset Management können Sie zwei Berichte generieren, die sich auf Wartungsanfragen beziehen.</span><span class="sxs-lookup"><span data-stu-id="f2127-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="f2127-105">Ein Bericht zeigt Details an, während der andere Bericht eine Liste bereitstellt, die für die Planung und Nachverfolgung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f2127-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="f2127-106">Erstellen eines Berichts zu Wartungsanfragedetails</span><span class="sxs-lookup"><span data-stu-id="f2127-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="f2127-107">Der Bericht **Wartungsanfragedetails** zeigt verschiedene Informationen, die sich auf Wartungsanfragen beziehen.</span><span class="sxs-lookup"><span data-stu-id="f2127-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="f2127-108">Wählen Sie **Anlagenverwaltung** \> **Berichte** \> **Wartungsanfragen** \> **Wartungsanfragedetails**.</span><span class="sxs-lookup"><span data-stu-id="f2127-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="f2127-109">Im Inforegister **Einzuschließende Datensätze** können Sie bestimmte Wartungsanfragen auswählen, die in den Bericht einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2127-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="f2127-110">Im Inforegister **Im Hintergrund ausführen** können Sie die Berichterstellung bei Bedarf als Stapelverarbeitungsauftrag einrichten.</span><span class="sxs-lookup"><span data-stu-id="f2127-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="f2127-111">Klicken Sie auf **OK**, um den Bericht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f2127-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="f2127-112">Die folgende Abbildung zeigt ein Beispiel für den Bericht **Wartungsanfragedetails**.</span><span class="sxs-lookup"><span data-stu-id="f2127-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![Abbildung 1](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="f2127-114">Erstellen eines Listenberichts zu Wartungsanfragen</span><span class="sxs-lookup"><span data-stu-id="f2127-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="f2127-115">Der Bericht **Wartungsanfragenliste** zeigt eine Liste aller Wartungsanfragen mit demselben Anfragetyp an.</span><span class="sxs-lookup"><span data-stu-id="f2127-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="f2127-116">Wählen Sie **Anlagenverwaltung** \> **Berichte** \> **Wartungsanfragen** \> **Wartungsanfragenliste**.</span><span class="sxs-lookup"><span data-stu-id="f2127-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="f2127-117">Im Inforegister **Einzuschließende Datensätze** können Sie Wartungsanfragen auswählen, die in den Bericht einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f2127-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="f2127-118">Im Inforegister **Im Hintergrund ausführen** können Sie die Berichterstellung bei Bedarf als Stapelverarbeitungsauftrag einrichten.</span><span class="sxs-lookup"><span data-stu-id="f2127-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="f2127-119">Klicken Sie auf **OK**, um den Bericht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f2127-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="f2127-120">Die folgende Abbildung zeigt ein Beispiel für den Bericht **Wartungsanfragenliste** für alle aktiven Wartungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="f2127-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![Abbildung 2](media/10-manage-maintenance-requests.png)