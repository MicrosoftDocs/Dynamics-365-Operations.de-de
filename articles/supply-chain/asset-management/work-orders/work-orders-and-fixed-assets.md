---
title: Fertigungsaufträge und Abschreibungen
description: In diesem Thema werden Arbeitsaufträge und Anlagen im Anlagenmanagement erläutert.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816723"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="aafeb-103">Fertigungsaufträge und Abschreibungen</span><span class="sxs-lookup"><span data-stu-id="aafeb-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="aafeb-104">In der Anlagenbuchhaltung können Anlagen mit Anlagen verknüpft sein, und Sie können Arbeitsaufträge für diese Anlagen anlegen.</span><span class="sxs-lookup"><span data-stu-id="aafeb-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="aafeb-105">Wenn Sie diese Funktionalität nutzen, können Sie sich im Modul **Projektverwaltung und Abrechnung** und im Modul **Anlage** in Microsoft Dynamics 365 for Finance and Operations einen vollständigen Überblick über die Anlage, die zugehörigen Investitionsprojekte und die auf den Investitionsprojekten erfassten Kosten verschaffen.</span><span class="sxs-lookup"><span data-stu-id="aafeb-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="aafeb-106">Das Feld **Anlagennummer** wird auf dem Arbeitsauftragsprojekt nur festgelegt, wenn als Projektart auf dem Arbeitsauftragsprojekt der Typ **Investition** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="aafeb-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="aafeb-107">Die folgende Abbildung veranschaulicht die Beziehung zwischen einem Investitionsprojekt im Modul **Projektverwaltung und Abrechnung** und einem Arbeitsauftragseinzelvorgangsprojekt.</span><span class="sxs-lookup"><span data-stu-id="aafeb-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Abbildung 1](media/24-work-orders.png)

<span data-ttu-id="aafeb-109">Die folgende Vorgehensweise beschreibt die Beziehung zwischen Anlagen, Arbeitsaufträgen, Arbeitsauftragsprojekten und Anlagen.</span><span class="sxs-lookup"><span data-stu-id="aafeb-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="aafeb-110">Sie erstellen eine Anlage, die Sie einer Anlage zuordnen.</span><span class="sxs-lookup"><span data-stu-id="aafeb-110">You create an asset that you relate to a fixed asset.</span></span>

![Abbildung 2](media/25-work-orders.png)

2. <span data-ttu-id="aafeb-112">Wenn Sie Arbeitsauftragsarten einrichten auf der Seite **Arbeitsauftragstypen** (**Anlagenverwaltung** > **Einrichtung** > **Arbeitsaufträge** > **Arbeitsauftragstypen**), legen Sie eine Arbeitsauftragsart für die Investitionsabwicklung an.</span><span class="sxs-lookup"><span data-stu-id="aafeb-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="aafeb-113">Siehe auch [Arbeitsauftragsarten](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="aafeb-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Abbildung 3](media/26-work-orders.png)

3. <span data-ttu-id="aafeb-115">Wenn Sie Projektgruppen für Arbeitsaufträge auf der Registerkarte **Projektgruppe** der Seite **Arbeitsauftrags-Projekteinstellungen** (**Anlagenverwaltung** > **Einrichtung** > **Arbeitsaufträge** > **Projekteinrichtung**) einrichten, stellen Sie eine Beziehung zwischen der für Investitionen verwendeten Arbeitsauftragsart und der Projektgruppe her, die auf der Seite **Projektgruppen** im Modul **Projektverwaltung und -verrechnung** (**Projektverwaltung und -verrechnung** > **Einrichtung** > **Buchung** > **Projektgruppen**) erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="aafeb-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Abbildung 4](media/27-work-orders.png)

4. <span data-ttu-id="aafeb-117">Wenn Sie einen Arbeitsauftrag anlegen, der sich auf eine Anlagen bezieht, wählen Sie die Arbeitsauftragsart, die für die Abwicklung von Investitionen verwendet wird, z.B. **Investition**.</span><span class="sxs-lookup"><span data-stu-id="aafeb-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="aafeb-118">Wenn der Arbeitsauftrag angelegt wird, wird die zugehörige Arbeitsauftragsart auf der Seite **Alle Arbeitsaufträge** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aafeb-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Abbildung 5](media/28-work-orders.png)

6. <span data-ttu-id="aafeb-120">Wenn der Arbeitsauftrag erstellt wird, wird das Projekt, das dem Arbeitsauftrag zugeordnet ist, auf der Seite **Alle Projekte** im Modul **Projektverwaltung und -verrechnung** erstellt (**Projektverwaltung und -verrechnung** > **Projekte** > **Alle Projekte**).</span><span class="sxs-lookup"><span data-stu-id="aafeb-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="aafeb-121">Um projektbezogene Informationen anzuzeigen, wählen Sie den Link im Feld **Projektkennung** auf der Registerkarte **Allgemein** auf dem Inforegister **Positionsdetails** in der Detailansicht der Seite **Alle Arbeitsaufträge** im Modul **Anlagenverwaltung** aus (**Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge**).</span><span class="sxs-lookup"><span data-stu-id="aafeb-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Abbildung 6](media/29-work-orders.png)

7. <span data-ttu-id="aafeb-123">Um einen Überblick der Projekte anzuzeigen, die einer Anlage zugeordnet sind, wählen Sie **Anlagen** > **Anlagen** > **Anlagen** und dann im Feld **Anlagennummer** den Link für die Anlage aus, um die Detailansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aafeb-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="aafeb-124">Erweitern Sie den Bereich **Zugehörige Informationen** auf der rechten Seite der Seite, und wählen Sie das Inforegister **Zugeordnete Projekte** aus.</span><span class="sxs-lookup"><span data-stu-id="aafeb-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]