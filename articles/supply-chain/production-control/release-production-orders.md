---
title: Freigeben von Produktionsaufträgen
description: Ein freigegebener Produktionsauftrag ist ein Auftrag, der für die Produktion autorisiert wurde. Der Begriff "Freigegeben" wird verwendet, um einen Status im Lebenszyklus eines Produktionsauftrags zu beschreiben, in dem der Produktionsauftrag für die Ausführung im Fertigungsbereich und für Lagerortprozesse verfügbar ist.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 242c3526e82e7d475f516bdbff8854fa0bf12079
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986603"
---
# <a name="release-production-orders"></a><span data-ttu-id="946f7-104">Freigeben von Produktionsaufträgen</span><span class="sxs-lookup"><span data-stu-id="946f7-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="946f7-105">Ein freigegebener Produktionsauftrag ist ein Auftrag, der für die Produktion autorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="946f7-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="946f7-106">Der Begriff "Freigegeben" wird verwendet, um einen Status im Lebenszyklus eines Produktionsauftrags zu beschreiben, in dem der Produktionsauftrag für die Ausführung im Fertigungsbereich und für Lagerortprozesse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="946f7-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="946f7-107">Merkmale des Status "Freigegeben"</span><span class="sxs-lookup"><span data-stu-id="946f7-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="946f7-108">Der Status **Freigegeben** ist ein Status im Lebenszyklus eines Produktionsauftrags.</span><span class="sxs-lookup"><span data-stu-id="946f7-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="946f7-109">Produktionsaufträge, die sich im Status **Freigegeben** befinden, sind für die Ausführung im Fertigungsbereich und für Lagerortprozesse verfügbar.</span><span class="sxs-lookup"><span data-stu-id="946f7-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="946f7-110">Der Status **Freigegeben** weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="946f7-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="946f7-111">Ein Produktionsauftrag kann in den Status **Freigegeben** geändert werden, entweder aus dem Produktionsauftrag oder mithilfe eines Stapelverarbeitungsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="946f7-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="946f7-112">Der Produktionsauftrag kann auch aus geplanten Produktionsaufträgen automatisch aktualisiert werden, die umgewandelt werden, indem Sie das Feld **Sofortanlagezeitraum** auf der Seite **Produktprogrammplan** verwenden.</span><span class="sxs-lookup"><span data-stu-id="946f7-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="946f7-113">Der Status **Freigegeben** ist das Signal für die Bediener im Fertigungsbereich (Bediener), die Ausführung der Produktionseinzelvorgänge im Fertigungsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="946f7-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="946f7-114">Produktionsunterlagen, wie Arbeitsplanlisten, Arbeitspläne und Listen zu Einzelvorgängen enthalten Informationen zu Produktionseinzelvorgängen und können ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="946f7-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="946f7-115">Für Materialien, die physisch reserviert werden, wird Lagerortarbeit generiert, um Materialien für den Produktionsauftrag zu entnehmen.</span><span class="sxs-lookup"><span data-stu-id="946f7-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="946f7-116">Freigeben von Einzelvorgängen für die Fertigung</span><span class="sxs-lookup"><span data-stu-id="946f7-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="946f7-117">Nachdem ein Produktionsauftrag freigegeben ist, werden Produktionseinzelvorgänge, die dem Auftrag zugeordnet sind, angezeigt und sind zur Registrierung bereit.</span><span class="sxs-lookup"><span data-stu-id="946f7-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="946f7-118">Die Operatoren Einzelvorgangserfassungen können, z.B. Start und stoppt Abschluss, entweder auf der **Einzelvorgangslistenterminal** Seite vornehmen oder die **Einzelvorgangslistengerät** Seite.</span><span class="sxs-lookup"><span data-stu-id="946f7-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="946f7-119">Die erfasste Zeit und die Menge werden automatisch aus den Erfassungsseiten auf Produktionserfassungen übertragen, die verbrauchte Zeit und Menge zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="946f7-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="946f7-120">Arbeitsplanlisten</span><span class="sxs-lookup"><span data-stu-id="946f7-120">Route cards</span></span>
<span data-ttu-id="946f7-121">Eine Arbeitsplanliste bietet einen Überblick über die Informationen aus den Einstellungen der Arbeitspläne und Arbeitsgänge sowie aus der Grob- und Feinterminierung.</span><span class="sxs-lookup"><span data-stu-id="946f7-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="946f7-122">Arbeitsplan-Einzelvorgänge</span><span class="sxs-lookup"><span data-stu-id="946f7-122">Route jobs</span></span>
<span data-ttu-id="946f7-123">Ein Arbeitsplan führt alle Einzelvorgänge eines Arbeitsgangs detailliert auf und enthält Rüstzeit, Bearbeitungszeit, Wartezeit und Transportzeiten.</span><span class="sxs-lookup"><span data-stu-id="946f7-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="946f7-124">Ein Arbeitsgang, wie etwa ein Anstrich, erfordert möglicherweise bestimmte Einzelvorgänge, wie Einrichtungszeit, Ausführungszeit für den Anstrichprozess und Wartezeit für das Trocknen.</span><span class="sxs-lookup"><span data-stu-id="946f7-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="946f7-125">Einzelvorgangslisten</span><span class="sxs-lookup"><span data-stu-id="946f7-125">Job cards</span></span>
<span data-ttu-id="946f7-126">In einer Einzelvorgangsliste werden die jeweiligen Einzelvorgangsnummern eines bestimmten Arbeitsgangs aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="946f7-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="946f7-127">Ein Einzelvorgang wird auf jeder Seite dargestellt.</span><span class="sxs-lookup"><span data-stu-id="946f7-127">One job appears on each page.</span></span> <span data-ttu-id="946f7-128">Die in einer Einzelvorgangsliste enthaltenen Einzelvorgänge sowie deren geschätzte Zeiten stammen aus den Einstellungen für den Arbeitsplan sowie aus den Einstellungen für den Arbeitsgang.</span><span class="sxs-lookup"><span data-stu-id="946f7-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="946f7-129">Von einer Einzelvorgangsliste können Sie die **Produktionserfassungspositionen**, Seite **Einzelvorgangslisten** öffnen.</span><span class="sxs-lookup"><span data-stu-id="946f7-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="946f7-130">Für die Ausführung betrieblicher Ressourcen zuständige Personen haben die Möglichkeit zum Eingeben von Rückmeldungen bezüglich des Produktionsprozesses.</span><span class="sxs-lookup"><span data-stu-id="946f7-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="946f7-131">Zu diesem Zweck stehen Felder für Verbrauchsstatistiken sowie für Informationen wie Ausschussmengen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="946f7-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="946f7-132">Lagerortarbeit für Rohmaterialentnahme</span><span class="sxs-lookup"><span data-stu-id="946f7-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="946f7-133">Arbeit für Rohmaterialentnahme wird während der Freigabe generiert.</span><span class="sxs-lookup"><span data-stu-id="946f7-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="946f7-134">Vorgang wird nur für die Menge von Materialien generiert, die physisch für den Produktionsauftrag reserviert war, bevor der Auftrag verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="946f7-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="946f7-135">Die folgende Einrichtung muss, um Lagerortarbeit für Rohmaterialentnahme zu generieren:</span><span class="sxs-lookup"><span data-stu-id="946f7-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="946f7-136">Eine Lagerplatzrichtlinie für die Rohmaterialentnahme, die bestimmt, an welchem Lagerort-Lagerplatz die Materialien zu entnehmen sind</span><span class="sxs-lookup"><span data-stu-id="946f7-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="946f7-137">Eine Wellenvorlage für Rohmaterialen, in denen Richtlinien für die Ausführung der Lagerortarbeit konfiguriert werden</span><span class="sxs-lookup"><span data-stu-id="946f7-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="946f7-138">Ein Lagerplatz für den Produktionswareneingang, der bestimmt, wo Materialien eingelagert werden</span><span class="sxs-lookup"><span data-stu-id="946f7-138">A production input location that determines where materials are put</span></span>




