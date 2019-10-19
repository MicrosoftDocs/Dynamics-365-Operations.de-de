---
title: Fertigungsaufträge und Abschreibungen
description: In diesem Thema werden Arbeitsaufträge und Anlagen im Anlagenmanagement erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250828"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="759c1-103">Fertigungsaufträge und Abschreibungen</span><span class="sxs-lookup"><span data-stu-id="759c1-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="759c1-104">In der Anlagenbuchhaltung können Anlagen mit Anlagen verknüpft sein, und Sie können Arbeitsaufträge für diese Anlagen anlegen.</span><span class="sxs-lookup"><span data-stu-id="759c1-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="759c1-105">Wenn Sie diese Funktionalität nutzen, können Sie sich im Modul **Projektverwaltung und Abrechnung** und im Modul **Anlage** einen vollständigen Überblick über die Anlage, die zugehörigen Investitionsprojekte und die auf den Investitionsprojekten erfassten Kosten verschaffen.</span><span class="sxs-lookup"><span data-stu-id="759c1-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="759c1-106">Das Feld **Anlagennummer** wird auf dem Arbeitsauftragsprojekt nur ausgefüllt, wenn als Projektart auf dem Arbeitsauftragsprojekt der Typ „Investition“ ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="759c1-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Abbildung 1](media/24-work-orders.png)

<span data-ttu-id="759c1-108">Die folgende Vorgehensweise beschreibt die Beziehung zwischen Anlagen, Arbeitsaufträgen, Arbeitsauftragsprojekten und Anlagen.</span><span class="sxs-lookup"><span data-stu-id="759c1-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="759c1-109">Sie legen eine Anlage an, die Sie auf eine Anlage beziehen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="759c1-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Abbildung 2](media/25-work-orders.png)

2. <span data-ttu-id="759c1-111">Wenn Sie Arbeitsauftragsarten einrichten (**Anlagenmanagement** > **Einrichtung** > **Aufträge** > **Auftragsarten**), legen Sie eine Arbeitsauftragsart für die Investitionsabwicklung an.</span><span class="sxs-lookup"><span data-stu-id="759c1-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="759c1-112">Siehe auch [Arbeitsauftragsarten](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="759c1-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Abbildung 3](media/26-work-orders.png)

3. <span data-ttu-id="759c1-114">Wenn Sie Projektgruppen für Arbeitsaufträge einrichten (**Anlagenmanagement** > **Setup** > **Arbeitsaufträge** > **Projekteinrichtung** > **Projektgruppe** Link), stellen Sie eine Beziehung zwischen der für Investitionen verwendeten Arbeitsauftragsart und der für Investitionen angelegten Projektgruppe im Modul **Projektmanagement und Rechnungswesen** her (**Projektmanagement und Rechnungswesen** > **Einrichtung** > **Buchung** > **Projektgruppen**).</span><span class="sxs-lookup"><span data-stu-id="759c1-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Abbildung 4](media/27-work-orders.png)

4. <span data-ttu-id="759c1-116">Wenn Sie einen Arbeitsauftrag anlegen, der sich auf ein Anlagenobjekt bezieht, wählen Sie die Arbeitsauftragsart, die für die Abwicklung von Investitionen verwendet wird, z.B. „Investition“.</span><span class="sxs-lookup"><span data-stu-id="759c1-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="759c1-117">Wenn der Arbeitsauftrag angelegt wird, wird die zugehörige Arbeitsauftragsart unter **Alle Arbeitsaufträge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="759c1-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Abbildung 5](media/28-work-orders.png)

6. <span data-ttu-id="759c1-119">Wenn der Arbeitsauftrag angelegt wird, wird das auf den Arbeitsauftrag bezogene Projekt in **Projektverwaltung und Abrechnung** > **Alle Projekte** angelegt.</span><span class="sxs-lookup"><span data-stu-id="759c1-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="759c1-120">Projektbezogene Informationen erhalten Sie, wenn Sie auf den Link **Projekt-ID** auf den Arbeitsauftrag klicken (in **Anlagenmanagement**, öffnen Sie den Arbeitsauftrag in der Detailansicht > **Zeilendetails** FastTab > **Allgemein** Registerkarte > **Projekt-ID** Feld).</span><span class="sxs-lookup"><span data-stu-id="759c1-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Abbildung 6](media/29-work-orders.png)

7. <span data-ttu-id="759c1-122">Unter **Abschreibung** erhalten Sie eine Übersicht über die mit einer Anlage verbundenen Projekte (**Abschreibung** > **Abschreibung** > **Abschreibung** > Klicken Sie auf die Anlage im Feld **Anlagennummer** > sehen Sie die Inhalte im Abschnitt **Verwandte Informationen** Bereich > **Verbundene Projekte**).</span><span class="sxs-lookup"><span data-stu-id="759c1-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

