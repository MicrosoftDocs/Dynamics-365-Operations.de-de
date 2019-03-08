---
title: Produktionsaufträge erstellen
description: Durch Erstellen eines Produktionsauftrags wird für einen Artikel eine Fertigungsanforderung erstellt. Im Produktionsauftrag ist angegeben, was und wie viel produziert werden und wann die Produktion abgeschlossen sein soll. Sie enthält auch Informationen darüber, welche Materialien genommen werden müssen und welchem Prozess gefolgt werden muss, um den Artikel zu produzieren,
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "324628"
---
# <a name="create-production-orders"></a><span data-ttu-id="d67e5-105">Produktionsaufträge erstellen</span><span class="sxs-lookup"><span data-stu-id="d67e5-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d67e5-106">Durch Erstellen eines Produktionsauftrags wird für einen Artikel eine Fertigungsanforderung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d67e5-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="d67e5-107">Im Produktionsauftrag ist angegeben, was und wie viel produziert werden und wann die Produktion abgeschlossen sein soll.</span><span class="sxs-lookup"><span data-stu-id="d67e5-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="d67e5-108">Sie enthält auch Informationen darüber, welche Materialien genommen werden müssen und welchem Prozess gefolgt werden muss, um den Artikel zu produzieren,</span><span class="sxs-lookup"><span data-stu-id="d67e5-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="d67e5-109">Ein Produktionsauftrag durchläuft Phasen des Produktionslebenszyklus.</span><span class="sxs-lookup"><span data-stu-id="d67e5-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="d67e5-110">Beim Erstellen eines Auftrags erhält dieser den Status **Erstellt**.</span><span class="sxs-lookup"><span data-stu-id="d67e5-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="d67e5-111">Bei Fertigstellung eines Auftrags erhält dieser den Status **Beendet**.</span><span class="sxs-lookup"><span data-stu-id="d67e5-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="d67e5-112">Eine Parametereinstellung in jeder Phase ermöglicht dem Benutzer, jeden Schritt zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d67e5-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="d67e5-113">Die Einstellung kann für einen einzelnen Benutzer oder für alle Benutzer eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="d67e5-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="d67e5-114">Eine Produktionsstückliste und der Produktionsarbeitsplan sind die wichtigsten Entitäten des Produktionsauftrags.</span><span class="sxs-lookup"><span data-stu-id="d67e5-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="d67e5-115">Sie werden basierend auf dem ausgewählten Artikel und der Menge, die produziert wird, in den Produktionsauftrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="d67e5-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="d67e5-116">Vor Beginn des Produktionsauftrags können die Produktionsstückliste und die Route bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d67e5-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="d67e5-117">Ein Produktionsauftrag kann in den folgenden Szenarien erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="d67e5-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="d67e5-118">Erstellt durch Produktprogrammplanungslauf basierend auf Materialnachfrage.</span><span class="sxs-lookup"><span data-stu-id="d67e5-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="d67e5-119">Erstellt direkt aus einer Auftragsposition, oder wenn eine höhere Ebene des Produktionsauftrags erstellt und geschätzt wird (Lieferung mit Bedarfsverursachung).</span><span class="sxs-lookup"><span data-stu-id="d67e5-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="d67e5-120">Manuell erstellt.</span><span class="sxs-lookup"><span data-stu-id="d67e5-120">Created manually.</span></span>




