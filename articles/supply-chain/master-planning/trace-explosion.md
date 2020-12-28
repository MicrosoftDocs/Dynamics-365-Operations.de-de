---
title: Verwenden der Ablaufverfolgung für die Auflösung
description: In diesem Artikel wird beschrieben, wie Sie die Funktion Nachverfolgung verwenden können, um die Ursachen hinter dem Ergebnis einer Auftragsauflösung zu untersuchen.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e777d69c9da8a19c186bca3ca591e59af232f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428477"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="ebe54-103">Verwenden der Ablaufverfolgung für die Auflösung</span><span class="sxs-lookup"><span data-stu-id="ebe54-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebe54-104">In diesem Artikel wird beschrieben, wie Sie die Funktion Nachverfolgung verwenden können, um die Ursachen hinter dem Ergebnis einer Auftragsauflösung zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="ebe54-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="ebe54-105">Wenn Sie Ablaufverfolgung aktivieren, können Sie Informationen zu Faktoren anzeigen, die dem Ergebnis der Auflösung eines bestimmten Auftrags beitrugen.</span><span class="sxs-lookup"><span data-stu-id="ebe54-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="ebe54-106">Nachfolgend finden Sie Beispiele dafür, wie die Ablaufverfolgungsinformationen verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="ebe54-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="ebe54-107">Hier können Sie Zuordnungen zwischen den Aktivitäten zu Bestellvorschlägen anzeigen, um die Lieferkette und die Lagerreservierungen zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="ebe54-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="ebe54-108">Hier können Sie Zuordnungen zu den Aufträgen anzeigen, die bereits genehmigt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebe54-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="ebe54-109">Sie können abgeleitete Anforderungen schwerpunktmäßig automatisch umwandeln, und dann die Aufträge genauer priorisieren.</span><span class="sxs-lookup"><span data-stu-id="ebe54-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="ebe54-110">Simulieren Sie Planungsergebnisse, um zu bestimmen, ob die Planungsparameter optimal sind.</span><span class="sxs-lookup"><span data-stu-id="ebe54-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="ebe54-111">Stellen Sie fest, wie Informationen wie Produktionsdatumsangaben, Mengen und Prioritäten für einen Auftrag bestimmt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebe54-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="ebe54-112">Sie können Details zu Verfügbarkeit und Aktivitäten für einen ausgewählten Auftrag anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ebe54-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="ebe54-113">Auf der Seite **Auflösung** sind auf der Registerkarte **Erklärung** im oberen Bereich Nachverfolgungsinformationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ebe54-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="ebe54-114">Ablaufverfolgung tritt auf, wenn Sie einen Auftrag auflösen.</span><span class="sxs-lookup"><span data-stu-id="ebe54-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="ebe54-115">Um die Verfolgung für den Bestellvorschlag zu starten, klicken Sie auf **Aktualisieren** und wählen Sie dann das Kontrollkästchen **Nachverfolgung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="ebe54-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="ebe54-116">Sie können das Feld **Text suchen** verwenden, um den Datensatz für spezifische Informationen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ebe54-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="ebe54-117">Suchergebnisse werden in der Struktur hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="ebe54-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ebe54-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ebe54-118">Additional resources</span></span>
--------

[<span data-ttu-id="ebe54-119">Hauptpläne – Übersicht</span><span class="sxs-lookup"><span data-stu-id="ebe54-119">Master plans overview</span></span>](master-plans.md)



