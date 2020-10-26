---
title: Einrichten eines Experiments
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in einem Drittanbieterdienst einrichten.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930204"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="5fe0a-103">Einrichten eines Experiments</span><span class="sxs-lookup"><span data-stu-id="5fe0a-103">Set up an experiment</span></span>

<span data-ttu-id="5fe0a-104">Nach dem [Definieren einer Hypothese und Bestimmen, welche Erfolgsmetriken Sie verwenden möchten](experimentation-identify.md) müssen Sie Ihr Experiment im Drittanbieterdienst einrichten.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="5fe0a-105">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5fe0a-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="5fe0a-107">[ ![User Journey zum Experimentieren – Einrichtung](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="5fe0a-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="5fe0a-108">Experiment im Drittanbieterdienst einrichten</span><span class="sxs-lookup"><span data-stu-id="5fe0a-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="5fe0a-109">Inzwischen sollten Sie Ihren Drittanbieterdienst ausgewählt haben, um Ihr Experiment auszuführen und zu überwachen, und den Experimentier-Connector eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="5fe0a-110">Diese Voraussetzungen sind aufgeführt unter [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5fe0a-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="5fe0a-111">Befolgen Sie die Schritte, die zum Erstellen Ihres Experiments im Dienst eines Drittanbieters erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="5fe0a-112">Wenn der Connector ordnungsgemäß konfiguriert ist, wird die vollständige Liste der Experimente, die Sie im Drittanbieterdienst eingerichtet haben, innerhalb von ca. 5 Minuten im Site Builder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="5fe0a-113">Erfolgsmetriken einrichten</span><span class="sxs-lookup"><span data-stu-id="5fe0a-113">Set up your success metrics</span></span>
<span data-ttu-id="5fe0a-114">Jedes Experiment benötigt Metriken, um die Auswirkungen der Variationen zu messen und die Hypothese zu validieren.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="5fe0a-115">Führen Sie die folgenden Schritte aus, um die Berechnung von Metriken im Drittanbieterdienst mithilfe von Live-Telemetrieereignissen von Dynamics 365 Commerce zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="5fe0a-116">Wählen Sie im Site Builder im linken Navigationsbereich die Registerkarte **Seiten** aus, und wählen Sie dann die Seite aus, auf der Sie Metriken erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="5fe0a-117">Gehen Sie im rechten Eigenschaftenbereich der Seite oder des Moduls, die oder das Sie verfolgen möchten, zum Abschnitt **Zu verfolgende Ereignis-IDs**.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="5fe0a-118">Wählen Sie **Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-118">Select **View**.</span></span> <span data-ttu-id="5fe0a-119">Eine Liste aller Ereignis-IDs wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="5fe0a-120">Kopieren Sie das Ereignis, das Sie verfolgen möchten, und fügen Sie den Ereignisschlüssel an der angegebenen Stelle im Dienst eines Drittanbieters ein.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="5fe0a-121">Wenn Sie mehr als ein Ereignis benötigen, kopieren Sie die Schlüssel einzeln.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="5fe0a-122">Weitere Informationen zum Anzeigen aller verfügbaren Ereignisse und Attribute, einschließlich Seitenaufrufe und Umsatzverfolgung, finden Sie unter [Commerce-Komponentenereignisse für Diagnose und Problembehandlung](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="5fe0a-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="5fe0a-123">Führen Sie weitere Schritte zum Verfolgen von Metriken aus, die im Drittanbieterdienst erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5fe0a-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="5fe0a-124">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="5fe0a-124">Previous step</span></span>
[<span data-ttu-id="5fe0a-125">Eine Hypothese identifizieren und Metriken für ein Experiment bestimmen</span><span class="sxs-lookup"><span data-stu-id="5fe0a-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="5fe0a-126">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="5fe0a-126">Next step</span></span>
[<span data-ttu-id="5fe0a-127">Ein Experiment verbinden und bearbeiten</span><span class="sxs-lookup"><span data-stu-id="5fe0a-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)