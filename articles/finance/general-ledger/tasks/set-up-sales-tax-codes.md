---
title: Mehrwertsteuercodes einrichten
description: In diesem Thema wird erläutert, wie Mehrwertsteuercodes in Dynamics 365 Finance eingerichtet werden.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3dad006b486f7cd6714c713a3bd83a95fdf0d2b5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443481"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="86a9e-103">Mehrwertsteuercodes einrichten</span><span class="sxs-lookup"><span data-stu-id="86a9e-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86a9e-104">In diesem Thema wird erläutert, wie Mehrwertsteuercodes eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="86a9e-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="86a9e-105">Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss.</span><span class="sxs-lookup"><span data-stu-id="86a9e-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="86a9e-106">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="86a9e-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="86a9e-107">Wechseln Sie zu **Navigationsbereich > Steuer > Indirekte Steuern > Mehrwertsteuer > Mehrwertsteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="86a9e-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="86a9e-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="86a9e-108">Select **New**.</span></span>
3. <span data-ttu-id="86a9e-109">Geben Sie im Feld **Mehrwertsteuercode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="86a9e-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="86a9e-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="86a9e-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="86a9e-111">Wählen Sie einen **Abrechnungszeitraum** aus, indem Sie die Pulldownliste öffnen, um anzugeben, welcher Mehrwertsteuerbehörde und in welchen Abständen diese Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="86a9e-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="86a9e-112">Wählen Sie eine **Sachkontobuchungsgruppe** aus, um die Hauptkonten anzugeben, um die Mehrwertsteuer im Hauptbuch zu buchen.</span><span class="sxs-lookup"><span data-stu-id="86a9e-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="86a9e-113">Erweitern Sie das Inforegister **Berechnung**.</span><span class="sxs-lookup"><span data-stu-id="86a9e-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="86a9e-114">Dieses hat mehrere Felder, die steuern, wie Mehrwertsteuerbeträge berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="86a9e-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="86a9e-115">Füllen Sie diese Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="86a9e-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="86a9e-116">Wählen Sie im **Aktivitätsbereich** oben in der Benutzeroberfläche **Mehrwertsteuercode** aus.</span><span class="sxs-lookup"><span data-stu-id="86a9e-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="86a9e-117">Wählen Sie **Werte** aus.</span><span class="sxs-lookup"><span data-stu-id="86a9e-117">Select **Values**.</span></span>
10. <span data-ttu-id="86a9e-118">Geben Sie den Wert für diesen Steuercode in der Spalte **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="86a9e-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="86a9e-119">Wenn auf dem Inforegister **Berechnung** im Feld „Ursprung“ die Option „Betrag pro Einheit“ ausgewählt ist, wird der Wert mit der Menge in der Transaktion multipliziert, um den Mehrwertsteuerbetrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="86a9e-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="86a9e-120">Wenn der Steuercode keine auf Einheiten basierte Steuer ist, ist der Wert ein Prozentsatz, der auf den "Ursprung" für diesen Steuercode angewendet wird, um den Mehrwertsteuerbetrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="86a9e-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="86a9e-121">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="86a9e-121">Select **Save**.</span></span>
12. <span data-ttu-id="86a9e-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="86a9e-122">Close the page.</span></span>
13. <span data-ttu-id="86a9e-123">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="86a9e-123">Select **Save**.</span></span>

