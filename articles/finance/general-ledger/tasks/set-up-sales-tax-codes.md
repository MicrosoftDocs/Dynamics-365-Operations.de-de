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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f6df5ed3fc49b537845e7d418d4953c0faee5f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994539"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="0cadf-103">Mehrwertsteuercodes einrichten</span><span class="sxs-lookup"><span data-stu-id="0cadf-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cadf-104">In diesem Thema wird erläutert, wie Mehrwertsteuercodes eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="0cadf-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="0cadf-105">Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss.</span><span class="sxs-lookup"><span data-stu-id="0cadf-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="0cadf-106">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cadf-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0cadf-107">Wechseln Sie zu **Navigationsbereich > Steuer > Indirekte Steuern > Mehrwertsteuer > Mehrwertsteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="0cadf-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="0cadf-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="0cadf-108">Select **New**.</span></span>
3. <span data-ttu-id="0cadf-109">Geben Sie im Feld **Mehrwertsteuercode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0cadf-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="0cadf-110">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0cadf-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0cadf-111">Wählen Sie einen **Abrechnungszeitraum** aus, indem Sie die Pulldownliste öffnen, um anzugeben, welcher Mehrwertsteuerbehörde und in welchen Abständen diese Mehrwertsteuer gemeldet und abgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0cadf-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="0cadf-112">Wählen Sie eine **Sachkontobuchungsgruppe** aus, um die Hauptkonten anzugeben, um die Mehrwertsteuer im Hauptbuch zu buchen.</span><span class="sxs-lookup"><span data-stu-id="0cadf-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="0cadf-113">Erweitern Sie das Inforegister **Berechnung**.</span><span class="sxs-lookup"><span data-stu-id="0cadf-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="0cadf-114">Dieses hat mehrere Felder, die steuern, wie Mehrwertsteuerbeträge berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="0cadf-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="0cadf-115">Füllen Sie diese Felder nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="0cadf-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="0cadf-116">Wählen Sie im **Aktivitätsbereich** oben in der Benutzeroberfläche **Mehrwertsteuercode** aus.</span><span class="sxs-lookup"><span data-stu-id="0cadf-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="0cadf-117">Wählen Sie **Werte** aus.</span><span class="sxs-lookup"><span data-stu-id="0cadf-117">Select **Values**.</span></span>
10. <span data-ttu-id="0cadf-118">Geben Sie den Wert für diesen Steuercode in der Spalte **Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="0cadf-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="0cadf-119">Wenn auf dem Inforegister **Berechnung** im Feld „Ursprung“ die Option „Betrag pro Einheit“ ausgewählt ist, wird der Wert mit der Menge in der Transaktion multipliziert, um den Mehrwertsteuerbetrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0cadf-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="0cadf-120">Wenn der Steuercode keine auf Einheiten basierte Steuer ist, ist der Wert ein Prozentsatz, der auf den "Ursprung" für diesen Steuercode angewendet wird, um den Mehrwertsteuerbetrag zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0cadf-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="0cadf-121">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="0cadf-121">Select **Save**.</span></span>
12. <span data-ttu-id="0cadf-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0cadf-122">Close the page.</span></span>
13. <span data-ttu-id="0cadf-123">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="0cadf-123">Select **Save**.</span></span>

