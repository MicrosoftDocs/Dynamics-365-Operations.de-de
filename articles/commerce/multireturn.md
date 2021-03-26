---
title: Artikel über mehrere Debitorenaufträge und Rechnungen zurückgeben
description: In diesem Thema werden die Funktionen erläutert, um Rücklieferungen über mehrere Debitorenaufträgen und Rechnungen in Dynamics 365 Commerce zu ermöglichen.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251258"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="2f346-103">Artikel über mehrere Debitorenaufträge und Rechnungen zurückgeben</span><span class="sxs-lookup"><span data-stu-id="2f346-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="2f346-104">Dieser Artikel beschreibt zwei Funktionen, mit denen die Rückgabe von Debitorenaufträgen über mehrere Rechnungen optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="2f346-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="2f346-105">Rückerstattungen über mehrere Erfassungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="2f346-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="2f346-106">Diese Funktion ermöglicht mehrere verknüpfte Rückerstattungen für denselben Debitorenauftrag.</span><span class="sxs-lookup"><span data-stu-id="2f346-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="2f346-107">Wechseln Sie zum Arbeitsbereich **Funktionsverwaltung** und suchen Sie nach **Rückerstattungen über mehrere Erfassungen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="2f346-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="2f346-108">Wählen Sie **Rückerstattungen über mehrere Erfassungen aktivieren** und klicken Sie dann auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="2f346-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="2f346-109">Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren</span><span class="sxs-lookup"><span data-stu-id="2f346-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="2f346-110">Diese Funktion stellt sicher, dass bei der Retoure eines Auftrags über mehrere Rechnungen die Steuern letztendlich dem ursprünglich berechneten Steuerbetrag entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2f346-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="2f346-111">Wechseln Sie zum Arbeitsbereich **Funktionsverwaltung** und suchen Sie nach **Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="2f346-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="2f346-112">Wählen Sie **Richtige Steuerberechnung für Retouren mit Teilmengen aktivieren** aus und klicken Sie dann auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="2f346-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="2f346-113">Rücklieferungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="2f346-113">Process returns</span></span>

<span data-ttu-id="2f346-114">Nachdem diese Funktionen aktiviert und die Änderungen mit den Shops synchronisiert wurden, kann der Kassierer im Shop mehrere Aufträge für einen Debitor zur Rücklieferung auswählen.</span><span class="sxs-lookup"><span data-stu-id="2f346-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="2f346-115">Wenn die Aufträge ausgewählt werden, wird eine Liste aller retournierbaren Produkte für alle Rechnungen des Auftrags angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f346-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="2f346-116">Der Kassierer kann dann die Produkte auswählen, die retourniert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f346-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="2f346-117">Es wird ein einzelner Rücklieferungsauftrag für alle ausgewählten Produkte erstellt.</span><span class="sxs-lookup"><span data-stu-id="2f346-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="2f346-118">Wenn der Auftrag vollständig zurückgesandt wird, entspricht der an den Kunden zurückgegebene Steuerbetrag dem ursprünglich berechneten Steuerbetrag.</span><span class="sxs-lookup"><span data-stu-id="2f346-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]