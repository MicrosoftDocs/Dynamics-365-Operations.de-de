--- 
title: Produkte vom empfangenden Lagerort Filialen zuordnen
description: "Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung eines Crossdocks zum Vertreiben von Produkten vom empfangenden Lagerplatz einer Bestellung an einen oder viele Shops."
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c8e25007cc4a204aeaf73a2e819c129fa8fa29d
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="653d9-103">Produkte vom empfangenden Lagerort Filialen zuordnen</span><span class="sxs-lookup"><span data-stu-id="653d9-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="653d9-104">Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung und Verarbeitung eines Crossdocks zum Vertreiben von Produkten vom empfangenden Lagerplatz einer Bestellung an einen oder viele Shops.</span><span class="sxs-lookup"><span data-stu-id="653d9-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="653d9-105">Der Benutzer kann mehrere Varianten definieren und das System vorschlagen lassen, wie die Produkte vertrieben werden sollen, oder manuell eingeben, wo die Produkte vertrieben werden und wie viel an jeden Shop vertrieben wird.</span><span class="sxs-lookup"><span data-stu-id="653d9-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="653d9-106">Das Verfahren umfasst nicht die Einrichtung von Daten, die im Crossdock verwendet werden können, wie Auffüllungsregeln, Organisationshierarchien und Shopgewichte.</span><span class="sxs-lookup"><span data-stu-id="653d9-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="653d9-107">Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="653d9-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="653d9-108">Wechseln Sie zu "Alle Bestellungen".</span><span class="sxs-lookup"><span data-stu-id="653d9-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="653d9-109">Wählen Sie eine Bestellung in der Liste aus und klicken Sie auf den Link, um den Auftrag zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="653d9-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="653d9-110">Klicken Sie im Aktivitätsbereich auf "Einzelhandel".</span><span class="sxs-lookup"><span data-stu-id="653d9-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="653d9-111">Klicken Sie auf "Crossdocking".</span><span class="sxs-lookup"><span data-stu-id="653d9-111">Click Cross docking.</span></span>
5. <span data-ttu-id="653d9-112">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="653d9-112">Click Edit.</span></span>
    * <span data-ttu-id="653d9-113">Die Kategorie kann verwendet werden, um die Artikel im Abschnitt "Positionen" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="653d9-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="653d9-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="653d9-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="653d9-115">Geben Sie im Crossdockingmengenfeld einen Wert ein, um anzugeben, wie viel der Menge, die vom ausgewählten Produkt gekauft wird, vertrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="653d9-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="653d9-116">Im Feld "Zusätzliche Crossdocking-Menge" geben Sie einen Wert ein, um die Mengen angeben, die für die verfügbaren gekauften Produkte vertrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="653d9-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="653d9-117">Geben Sie im Verteilungs-Feld "Location weight" ein.</span><span class="sxs-lookup"><span data-stu-id="653d9-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="653d9-118">Sie können die anderen Typen auswählen, um verschiedene Regeln für die Verteilung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="653d9-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="653d9-119">Wählen Sie im Feld "Auffüllungshierarchie" einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="653d9-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="653d9-120">Wählen Sie "Ja" im Feld "Sortimente berücksichtigen" aus.</span><span class="sxs-lookup"><span data-stu-id="653d9-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="653d9-121">Klicken Sie auf "Mengen berechnen".</span><span class="sxs-lookup"><span data-stu-id="653d9-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="653d9-122">Klicken Sie auf "Auftrag erstellen".</span><span class="sxs-lookup"><span data-stu-id="653d9-122">Click Create order.</span></span>
14. <span data-ttu-id="653d9-123">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="653d9-123">Click Yes.</span></span>
15. <span data-ttu-id="653d9-124">Wählen Sie in der Liste einen Lagerort aus, der die Produkte empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="653d9-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="653d9-125">Klicken Sie auf "Auftrag", um die Aufträge anzuzeigen, die für den ausgewählten Lagerort erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="653d9-125">Click Order to view the orders that got created for the selected warehouse</span></span>


