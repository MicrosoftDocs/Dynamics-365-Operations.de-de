---
title: Eine Hypothese identifizieren und Metriken für ein Experiment bestimmen
description: In diesem Thema wird beschrieben, wie Sie die Hypothesen und Erfolgsmetriken für ein Experiment identifizieren, das Sie auf einer E-Commerce-Website in Dynamics 365 Commerce ausführen.
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
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930202"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="cd47f-103">Eine Hypothese identifizieren und Erfolgsmetriken für ein Experiment bestimmen</span><span class="sxs-lookup"><span data-stu-id="cd47f-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="cd47f-104">Die erste Phase im Experimentierlebenszyklus umfasst das Identifizieren der Hypothese für das Experiment und das Bestimmen der Metriken, die Sie verfolgen, um den Erfolg zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="cd47f-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="cd47f-105">Das folgende Diagramm zeigt alle Schritte, die am [Einrichten und Ausführen eines Experiments](experimentation-overview.md) auf einer E-Commerce-Website in Dynamics 365 Commerce beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="cd47f-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cd47f-106">Weitere Schritte werden in separaten Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="cd47f-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="cd47f-107">[ ![User Journey zum Experimentieren – Identifizierung](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cd47f-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="cd47f-108">Eine Hypothese ist eine Aussage, bei der Sie das Ergebnis des Experiments vorhersagen.</span><span class="sxs-lookup"><span data-stu-id="cd47f-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="cd47f-109">Bei der Definition einer Hypothese spielen viele Faktoren eine Rolle, z. B. die Untersuchung des Nutzerverhaltens und der von Ihnen gesammelten Website-Daten.</span><span class="sxs-lookup"><span data-stu-id="cd47f-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="cd47f-110">Mit der Hypothese definieren Sie die Annahme oder Theorie, die Sie mit Ihrem Experiment validieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cd47f-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="cd47f-111">Ein Beispiel für eine Hypothese für Ihr Experiment könnte „*Ein Bild eines weißen T-Shirts auf meiner Homepage führt in den Sommermonaten zu einer höheren Klickrate als ein Marinepullover, da die Leute im Sommer etwas Leichtes und Helles tragen möchten*“ lauten.</span><span class="sxs-lookup"><span data-stu-id="cd47f-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="cd47f-112">In diesem Fall erstellen Sie Variationen, die ein weißes T-Shirt und einen Marinepullover enthalten, und veröffentlichen beide gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="cd47f-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="cd47f-113">Um eine Hypothese zu validieren, sollte der Erfolg oder Misserfolg eines Experiments direkt mit Benutzeraktionen verknüpft werden. Zum Beispiel, wenn der Benutzer der Website auf einen Link oder eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="cd47f-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="cd47f-114">Diese Aktionen müssen mit Ereignissen übereinstimmen, die an den Drittanbieter gemeldet werden, der das Experiment verfolgt.</span><span class="sxs-lookup"><span data-stu-id="cd47f-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="cd47f-115">Mit der Zeit wird der Prozentsatz der Benutzer, die die Aktion ausführen, als Metrik ermittelt, mit der Sie Berichte erstellen und Analysen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="cd47f-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="cd47f-116">Im Thema [Commerce-Komponentenereignisse für Diagnose und Problembehandlung](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) finden Sie alle verfügbaren Ereignisse und Attribute.</span><span class="sxs-lookup"><span data-stu-id="cd47f-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="cd47f-117">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="cd47f-117">Previous step</span></span>
[<span data-ttu-id="cd47f-118">Experimentieren in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cd47f-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="cd47f-119">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="cd47f-119">Next step</span></span>
[<span data-ttu-id="cd47f-120">Einrichten eines Experiments</span><span class="sxs-lookup"><span data-stu-id="cd47f-120">Set up an experiment</span></span>](experimentation-setup.md)
