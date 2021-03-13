---
title: Auftragsrückrufe in POS
description: In diesem Thema werden die Funktionen erläutert, die für verbesserte Auftragsrückrufseiten in POS verfügbar sind.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010073"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="ac891-103">Auftragsrückrufe in POS</span><span class="sxs-lookup"><span data-stu-id="ac891-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac891-104">Der Vorgang **Auftrag zurückrufen** in der Commerce-Verkaufsstelle (POS) bietet aktualisierte Funktionen zum Suchen und Filtern von Aufträgen sowie auftragsspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="ac891-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="ac891-105">Diese Funktion ist in Commerce Version 10.0.15 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac891-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="ac891-106">Um diese Funktionalität zu aktivieren, schalten Sie die Funktion **Verbesserter Auftragsrückruf in POS** im **Funktionsverwaltung**-Arbeitsbereich in der Commerce-Zentrale ein.</span><span class="sxs-lookup"><span data-stu-id="ac891-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="ac891-107">Nachdem Sie die Funktion aktiviert haben, sollten Sie Ihre [Bildschirmlayouts](pos-screen-layouts.md) in POS aktualisieren, um einige der geänderten Funktionen zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="ac891-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="ac891-108">Mit der Konfiguration der Schaltfläche **Auftrag zurückrufen** können Organisationen den Vorgang mit einer vordefinierten Anzeige bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ac891-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Konfiguration des Schaltflächenrasters](media/recallorderbuttongrid.png)

<span data-ttu-id="ac891-110">Die Anzeigeoptionen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac891-110">The display options are as follows.</span></span>
- <span data-ttu-id="ac891-111">**Keine** – Diese Option stellt den Vorgang ohne spezifische Anzeige bereit.</span><span class="sxs-lookup"><span data-stu-id="ac891-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="ac891-112">Wenn ein Benutzer den Vorgang mit dieser Konfiguration öffnet, wird er aufgefordert, Aufträge zu suchen und zu finden oder aus einem vordefinierten Auftragsfilter auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ac891-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="ac891-113">**Zu erfüllende Aufträge** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die vom Store ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac891-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="ac891-114">Diese Aufträge sind für die Abholung im Store oder den Versand konfiguriert, und die Zeilen dieser Aufträge wurden noch nicht kommissioniert oder verpackt.</span><span class="sxs-lookup"><span data-stu-id="ac891-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="ac891-115">**Aufträge zur Abholung** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die für die Abholung im aktuellen Store des Benutzers konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="ac891-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="ac891-116">**Aufträge zum Versand** – Wenn ein Benutzer den Vorgang startet, wird automatisch eine Abfrage ausgeführt, um eine Liste der Aufträge zu durchsuchen und anzuzeigen, die für den Versand vom aktuellen Store des Benutzers konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="ac891-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="ac891-117">Beim Starten des Vorgangs **Auftrag zurückrufen** in POS, wenn das Display als **Keine** konfiguriert ist, kann ein Benutzer Aufträge auf eine der folgenden Arten suchen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="ac891-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="ac891-118">Auftrags-Barcodes scannen.</span><span class="sxs-lookup"><span data-stu-id="ac891-118">Scan order barcodes.</span></span> <span data-ttu-id="ac891-119">Dadurch werden die Felder für Auftragsnummer, Kanalreferenz und Beleg-ID nach Übereinstimmungen durchsucht.</span><span class="sxs-lookup"><span data-stu-id="ac891-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="ac891-120">Wählen Sie das Symbol **Aufträge durchsuchen** oder **Suchen und Filtern** in der AppBar aus, um mithilfe des Filtermechanismus Aufträge zu finden, die die Filterkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ac891-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="ac891-121">Wählen Sie aus einem vordefinierten Filter aus dem Dropdown-Menü **Aufträge anzeigen** (zu erfüllende Aufträge, Aufträge zur Abholung oder Aufträge zum Versand).</span><span class="sxs-lookup"><span data-stu-id="ac891-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="ac891-123">Nachdem die Suchkriterien angewendet wurden, zeigt die Anwendung eine Liste der übereinstimmenden Kundenaufträge an.</span><span class="sxs-lookup"><span data-stu-id="ac891-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="ac891-125">Ein Benutzer kann einen Auftrag in der Liste auswählen, um zusätzliche Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac891-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="ac891-126">Das Informationsfeld auf der rechten Seite des Bildschirms zeigt Einzelheiten zum ausgewählten Auftrag an, einschließlich Details zur Auftragsposition, Lieferdetails und Erfüllungsdetails.</span><span class="sxs-lookup"><span data-stu-id="ac891-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="ac891-127">In der AppBar kann ein Benutzer einen Vorgang auswählen.</span><span class="sxs-lookup"><span data-stu-id="ac891-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="ac891-128">Abhängig vom Auftragsstatus sind bestimmte Vorgänge möglicherweise nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac891-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="ac891-129">**Rückgabe** – Führt eine Rücksendung für eine oder mehrere Rechnungen aus, die sich auf den ausgewählten Kundenauftrag beziehen.</span><span class="sxs-lookup"><span data-stu-id="ac891-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="ac891-130">**Stornieren** – Stellt eine vollständige Stornierung des ausgewählten Kundenauftrags aus.</span><span class="sxs-lookup"><span data-stu-id="ac891-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="ac891-131">**Erfüllen** – Überträgt den Benutzer auf die Seite zur Auftragserfüllung, die für die ausgewählte Bestellung vorgefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="ac891-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="ac891-132">Es werden nur Auftragspositionen angezeigt, die vom Store des Benutzers für den ausgewählten Auftrag zur Erfüllung geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="ac891-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="ac891-133">**Bearbeiten** – Ermöglicht Benutzern das Vornehmen von Änderungen am ausgewählten Kundenauftrag.</span><span class="sxs-lookup"><span data-stu-id="ac891-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="ac891-134">**Abholen** – Startet den Abholungs-Flow, mit dem der Benutzer die abzuholenden Produkte auswählen kann, und erstellt die Warenabholungstransaktion.</span><span class="sxs-lookup"><span data-stu-id="ac891-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
