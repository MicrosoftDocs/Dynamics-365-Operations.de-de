---
title: Hybrid-Kundenaufträge
description: Ein hybrider Kundenauftrag ist einen einzelnen Auftrag, der Produkte enthält, die vom Shop des Debitors ausgeführt werden können, sowie Produkte, die verarbeitet werden oder später geliefert.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bec8389645a06a8287e51195341909ec71a8af2b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009692"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="bb126-103">Hybrid-Kundenaufträge</span><span class="sxs-lookup"><span data-stu-id="bb126-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb126-104">Ein hybrider Kundenauftrag ist einen einzelnen Auftrag, der Produkte enthält, die vom Shop des Debitors ausgeführt werden können, sowie Produkte, die verarbeitet werden oder später geliefert.</span><span class="sxs-lookup"><span data-stu-id="bb126-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="bb126-105">In Commerce können Sie festlegen, entweder alle oder ausgewählte Produkte für einen Kundenauftrag auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bb126-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="bb126-106">Die Produktgruppen, die z ausführen fakturiert werden automatisch markiert werden, nachdem der Auftrag erstellt wurde, auf ähnliche Weise diese ist identisch für einen Auftrag, die eingeschlossen werden soll, nachdem der Auftrag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bb126-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="bb126-107">Zahlbarer Betrag auf hybriden Aufträgen wird ermittelt, indem der Einzahlungsprozentsatz auf Entnahme- und Schiffsproduktgruppen mit dem Gesamtbetrag der Durchführungspositionen hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bb126-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="bb126-108">Für hybride Aufträge die Systemschalter zwischen Debitorenauftragsmodus und Abholgrosshandelmodus, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bb126-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="bb126-109">Wenn alle Produkte im Einkaufskorb auf **Lieferung ausführen** festgelegt werden, wird der Auftrag als Cash-and-carry Buchung behandelt.</span><span class="sxs-lookup"><span data-stu-id="bb126-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="bb126-110">Werden irgendwelche oder alle Positionen werden im Einkaufskorb auf entweder **Entnahme** oder **Lieferung versenden** festgelegt, wird der Auftrag als Debitorenauftragsbuchung behandelt.</span><span class="sxs-lookup"><span data-stu-id="bb126-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="bb126-111">Wenn eine Einkaufswagenposition ausgewählt und **Auswahl entnehmen**, **Auswahl senden** oder **Auswahl ausliefern** aktiviert ist, nur bestimmte Einkaufswagenposition die mit der Zahlungsbedingung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bb126-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="bb126-112">In diesem Fall wird der Ablauf des Arbeitsgangs abwärts gerichtete wie gewohnt fort.</span><span class="sxs-lookup"><span data-stu-id="bb126-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="bb126-113">Wenn **Auswahl entnehmen**, **Auswahl senden** oder **Auswahl ausliefern** aktiviert ist, ohne das eine Einkaufswagenposition aktiviert ist, die ausgewählt wird, wird geöffnet eine neue Seite, die alle Einkaufswagenpositionen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="bb126-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="bb126-114">Auf diesem Fenster können Sie mehrere Zeilen für das Festlegen der Zahlungsbedingung gleichzeitig auswählen.</span><span class="sxs-lookup"><span data-stu-id="bb126-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="bb126-115">Bei dieser Methode für die Auswahl von Zeilen verwenden, wird einer vorherigen Übermittlungsmethode, die der Position zugewiesen wurde, überschrieben.</span><span class="sxs-lookup"><span data-stu-id="bb126-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb126-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb126-116">Additional resources</span></span>

[<span data-ttu-id="bb126-117">Debitorenaufträge in Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="bb126-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)
