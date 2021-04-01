---
title: Einrichten eines Experiments
description: In diesem Thema wird beschrieben, wie Sie ein Experiment in einem Drittanbieterdienst einrichten.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dfd7b8cb13f4d69811b5a86b971fa1b57c75bd36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234608"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="68b1b-103">Einrichten eines Experiments</span><span class="sxs-lookup"><span data-stu-id="68b1b-103">Set up an experiment</span></span>

<span data-ttu-id="68b1b-104">Nach dem [Definieren einer Hypothese und Bestimmen, welche Erfolgsmetriken Sie verwenden möchten](experimentation-identify.md) müssen Sie Ihr Experiment im Drittanbieterdienst einrichten.</span><span class="sxs-lookup"><span data-stu-id="68b1b-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="68b1b-105">Das folgende Diagramm zeigt alle Schritte, die am Einrichten und Ausführen eines Experiments auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="68b1b-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="68b1b-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="68b1b-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="68b1b-107">[ ![User Journey zum Experimentieren – Einrichtung](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="68b1b-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="68b1b-108">Experiment im Drittanbieterdienst einrichten</span><span class="sxs-lookup"><span data-stu-id="68b1b-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="68b1b-109">Inzwischen sollten Sie Ihren Drittanbieterdienst ausgewählt haben, um Ihr Experiment auszuführen und zu überwachen, und den Experimentier-Connector eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="68b1b-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="68b1b-110">Diese Voraussetzungen sind aufgeführt unter [Experimentieren in Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="68b1b-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="68b1b-111">Befolgen Sie die Schritte, die zum Erstellen Ihres Experiments im Dienst eines Drittanbieters erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="68b1b-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="68b1b-112">Wenn der Connector ordnungsgemäß konfiguriert ist, wird die vollständige Liste der Experimente, die Sie im Drittanbieterdienst eingerichtet haben, innerhalb von ca. 5 Minuten im Commerce Site Builder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68b1b-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="68b1b-113">Erfolgsmetriken einrichten</span><span class="sxs-lookup"><span data-stu-id="68b1b-113">Set up your success metrics</span></span>
<span data-ttu-id="68b1b-114">Jedes Experiment benötigt Metriken, um die Auswirkungen der Variationen zu messen und die Hypothese zu validieren.</span><span class="sxs-lookup"><span data-stu-id="68b1b-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="68b1b-115">Führen Sie die folgenden Schritte aus, um die Berechnung von Metriken im Drittanbieterdienst mithilfe von Live-Telemetrieereignissen von Dynamics 365 Commerce zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="68b1b-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="68b1b-116">Gehen Sie zum Einrichten von Erfolgsmetriken folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="68b1b-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="68b1b-117">Wählen Sie im Commerce Site Builder im linken Navigationsbereich die Registerkarte **Seiten** aus, und wählen Sie dann die Seite aus, auf der Sie Metriken erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="68b1b-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="68b1b-118">Gehen Sie im rechten Eigenschaftenbereich der Seite oder des Moduls, die oder das Sie verfolgen möchten, zum Abschnitt **Zu verfolgende Ereignis-IDs**.</span><span class="sxs-lookup"><span data-stu-id="68b1b-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="68b1b-119">Wählen Sie **Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="68b1b-119">Select **View**.</span></span> <span data-ttu-id="68b1b-120">Eine Liste aller Ereignis-IDs wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68b1b-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="68b1b-121">Kopieren Sie das Ereignis, das Sie verfolgen möchten, und fügen Sie den Ereignisschlüssel an der angegebenen Stelle im Dienst eines Drittanbieters ein.</span><span class="sxs-lookup"><span data-stu-id="68b1b-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="68b1b-122">Wenn Sie mehr als ein Ereignis benötigen, kopieren Sie die Schlüssel einzeln.</span><span class="sxs-lookup"><span data-stu-id="68b1b-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="68b1b-123">Weitere Informationen zum Anzeigen aller verfügbaren Ereignisse und Attribute, einschließlich Seitenaufrufe und Umsatzverfolgung, finden Sie unter [Commerce-Komponentenereignisse für Diagnose und Problembehandlung](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="68b1b-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="68b1b-124">Führen Sie weitere Schritte zum Verfolgen von Metriken aus, die im Drittanbieterdienst erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="68b1b-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="68b1b-125">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="68b1b-125">Previous step</span></span>
[<span data-ttu-id="68b1b-126">Eine Hypothese identifizieren und Metriken für ein Experiment bestimmen</span><span class="sxs-lookup"><span data-stu-id="68b1b-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="68b1b-127">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="68b1b-127">Next step</span></span>
[<span data-ttu-id="68b1b-128">Ein Experiment verbinden und bearbeiten</span><span class="sxs-lookup"><span data-stu-id="68b1b-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]