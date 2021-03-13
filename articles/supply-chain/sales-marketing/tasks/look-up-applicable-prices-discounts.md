---
title: Anwendbare Preise und Rabatte nachschlagen
description: Im folgenden Verfahren, wie Preis und/oder den Rabatt für ein Produkt sucht, das für einen bestimmten Debitor derzeit gültig ist, ohne einen Auftrag zu erstellen.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bd85d9cd2d7273ad6e05d794a96e4d6a8d7c526
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010771"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="0a9f4-103">Anwendbare Preise und Rabatte nachschlagen</span><span class="sxs-lookup"><span data-stu-id="0a9f4-103">Look up applicable prices and discounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a9f4-104">Im folgenden Verfahren, wie Preis und/oder den Rabatt für ein Produkt sucht, das für einen bestimmten Debitor derzeit gültig ist, ohne einen Auftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="0a9f4-105">Die Prozedurgänge durch ein besonderes Beispiel und Sie müssen im Beispiel für die Verwendung des USMF-Vorführungsunternehmens folgt, um die erforderlichen Werte auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="0a9f4-106">Suchen des gültigen Preis</span><span class="sxs-lookup"><span data-stu-id="0a9f4-106">Find the applicable price</span></span>
1. <span data-ttu-id="0a9f4-107">Wechseln Sie zu Vertrieb und Marketing > Preise und Rabatte > Preise suchen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="0a9f4-108">Klicken Sie im Feld "Debitorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0a9f4-109">Suchen Sie in der Liste den Debitor US-001 und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="0a9f4-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0a9f4-111">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "T0004" ein.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="0a9f4-112">Stellen Sie sicher, dass das Feld Menge standardmäßig auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="0a9f4-113">Wenn Sie jedoch die Größe des Auftrags bekannt, den der Debitor bewirken, für das fragliche Produkt erteilen möchten, geben Sie diesen Wert stattdessen ein.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="0a9f4-114">Diese Informationen sind von Bedeutung, wenn die Handelsvereinbarungen mit dem Debitor Mengenpausen haben, d. h. der Preis des Produkts aus der eingekauften Menge abhängt.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="0a9f4-115">Im Datumsfeld geben Sie ein Datum für, wenn der Debitor erwartet, einen Auftrag zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="0a9f4-116">Das Datum kann heute oder ab einem beliebigen Datum in der Zukunft beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="0a9f4-117">Im System wird nun den Preis zurück, der für das ausgewählte Produkt gültig ist, wenn er durch den ausgewählten Debitor für das ausgewählte Datum mit einer angegebenen Menge eingekauft wird.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="0a9f4-118">In diesem Beispiel wenn der Debitor US-001 1 Einheit des Produkts T0004 heute erworben hat, werden  350 EUR pro Einheit berechnet.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="0a9f4-119">Dieser Preis stammt aus einer Fähigkeit oder Handelsvereinbarung mit dem Debitor.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="0a9f4-120">Andere Felder auf der Seite finden Sie weitere Informationen zu den Produktpreis und die Produkt Kosten (wenn im Produktmaster eingerichtet werden) und berechnete Rentabilität.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="0a9f4-121">Wenn die Option "Ähnliche Produktvarianten anzeigen" aktiviert ist, bedeutet dies, dass es zusätzliche Handelsvereinbarungen für die Varianten des Produkts gibt.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="0a9f4-122">Klicken Sie auf das Kontrollkästchen "Ähnliche Produktvarianten anzeigen".</span><span class="sxs-lookup"><span data-stu-id="0a9f4-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="0a9f4-123">Eine Liste der Produktvarianten wird, mit Informationen zu ihrem Dimensionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="0a9f4-124">Wählen Sie in der Liste markieren Sie die Position, die Farbe Weiß darstellt.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="0a9f4-125">Hinweis, der Produktpreis ist jetzt zu dem unterscheiden, der zuvor angezeigt wird, als diese nicht pro Dimension angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="0a9f4-126">Klicken Sie auf Verkaufspreise anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-126">Click View sales prices.</span></span>
    * <span data-ttu-id="0a9f4-127">Auf der Preis (Verkauf) aller Handelsvereinbarungen anwendbar dem Produkt, einschließlich der Varianten.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="0a9f4-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="0a9f4-129">Suchen des gültigen Rabatts</span><span class="sxs-lookup"><span data-stu-id="0a9f4-129">Find the applicable discount</span></span>
<span data-ttu-id="0a9f4-130">Stellen Sie sicher, dass das Feld "Debitorenkonto" Debitornummer US-001 enthält </span><span class="sxs-lookup"><span data-stu-id="0a9f4-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="0a9f4-131">Geben Sie im Feld "Artikelnummer" die Zeichenfolge "T0012" ein.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="0a9f4-132">Stellen Sie sicher, dass das Feld Menge auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="0a9f4-133">Die folgenden Preiskalkulationsdetails, die für Produkt T0012 angezeigt werden, stammen aus einer oder mehreren Handelsvereinbarungen: Der Preis je Einheit beträgt 1,000 EUR sowie der Rabattprozentsatz ist 5.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="0a9f4-134">Legen Sie die Menge auf "20" fest.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="0a9f4-135">Die erweiterte Bestellmenge verursacht den Positionsrabatt, der dem Debitor der Änderung von 5 bis 7 Prozent angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="0a9f4-136">Der Nettobetrag wird auf dem Stückpreis, dem Rabatt und dem Gesamtpreis berechnet.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="0a9f4-137">Klicken Sie auf Positionsrabatt anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-137">Click View line discount.</span></span>
    * <span data-ttu-id="0a9f4-138">Es gibt zwei Positionsrabattvereinbarungen für Produkt T0012 und gibt einen 5-Prozent-Rabatt für eine Auftragspositionsmenge von 1 bis 10 und ein 7-Prozent-Rabatt für Bestellmengen zu 10. geliefert.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="0a9f4-139">Beachten Sie, dass die Rabatte zu einer Gruppe Produkten, in diesem Beispiel, Gruppencode 01 angewendet werden, des Produkts T0012 angehört.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="0a9f4-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0a9f4-140">Close the page.</span></span>

