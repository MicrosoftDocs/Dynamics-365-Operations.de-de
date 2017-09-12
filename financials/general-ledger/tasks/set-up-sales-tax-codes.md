--- 
title: Mehrwertsteuercodes einrichten
description: "Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8f1eea5e257ccb8f2e7fe900e2c8c68bdd5148f
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="35fc1-103">Mehrwertsteuercodes einrichten</span><span class="sxs-lookup"><span data-stu-id="35fc1-103">Set up sales tax codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="35fc1-104">Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss.</span><span class="sxs-lookup"><span data-stu-id="35fc1-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="35fc1-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="35fc1-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="35fc1-106">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuercodes".</span><span class="sxs-lookup"><span data-stu-id="35fc1-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="35fc1-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="35fc1-107">Click New.</span></span>
3. <span data-ttu-id="35fc1-108">Geben Sie im Feld "Mehrwertsteuercode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="35fc1-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="35fc1-109">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="35fc1-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="35fc1-110">Wählen Sie einen Abrechnungszeitraum aus, um anzugeben, welche Mehrwertsteuerbehörde und in welchen Abständen diese Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="35fc1-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="35fc1-111">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="35fc1-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="35fc1-112">Wählen Sie eine "Sachkontobuchungsgruppe" aus, um die Hauptkonten anzugeben, um die Mehrwertsteuer im Hauptbuch zu buchen.</span><span class="sxs-lookup"><span data-stu-id="35fc1-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="35fc1-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="35fc1-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="35fc1-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="35fc1-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="35fc1-115">Erweitern Sie das Inforegister "Berechnung".</span><span class="sxs-lookup"><span data-stu-id="35fc1-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="35fc1-116">Das Inforegister "Berechnung" hat mehrere Felder, die steuern, wie Mehrwertsteuerbeträge berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="35fc1-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="35fc1-117">Klicken Sie im Aktivitätsbereich auf "Mehrwertsteuercode".</span><span class="sxs-lookup"><span data-stu-id="35fc1-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="35fc1-118">Klicken Sie auf "Werte".</span><span class="sxs-lookup"><span data-stu-id="35fc1-118">Click Values.</span></span>
13. <span data-ttu-id="35fc1-119">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="35fc1-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="35fc1-120">Geben Sie den Wert für diesen Steuercode ein.</span><span class="sxs-lookup"><span data-stu-id="35fc1-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="35fc1-121">Wenn im Inforegister "Berechnung" im Feld "Ursprung" die Option "Betrag pro Einheit" ausgewählt ist, wird der Wert um die Menge in der Transaktion multipliziert, um den Mehrwertsteuerbetrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="35fc1-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="35fc1-122">Wenn der Steuercode keine auf Einheiten basierte Steuer ist, ist der Wert ein Prozentsatz, der auf den "Ursprung" für diesen Steuercode angewendet wird, um den Mehrwertsteuerbetrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="35fc1-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="35fc1-123">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="35fc1-123">Click Save.</span></span>
16. <span data-ttu-id="35fc1-124">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="35fc1-124">Close the page.</span></span>
17. <span data-ttu-id="35fc1-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="35fc1-125">Click Save.</span></span>


