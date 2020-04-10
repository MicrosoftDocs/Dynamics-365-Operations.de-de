---
title: Einen Zinscode mit einem Bereich erstellen
description: Zinscodes können eingerichtet werden, um verschiedene Zinsbeträge auf Grundlage einen Wertebereich zu berechnen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c0c5b20ff6fff2bc62daca68c46e949a38df8d92
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140269"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="55bac-103">Einen Zinscode mit einem Bereich erstellen</span><span class="sxs-lookup"><span data-stu-id="55bac-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="55bac-104">Zinscodes können eingerichtet werden, um verschiedene Zinsbeträge auf Grundlage einen Wertebereich zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="55bac-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="55bac-105">Dieses Verfahren zeigt Ihnen, wie Sie einen Zinscode Hinzufügen und einen Bereich hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="55bac-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="55bac-106">Wechseln Sie zu "Kredit und Inkasso" > "Zinsen" > "Zinscodes einrichten".</span><span class="sxs-lookup"><span data-stu-id="55bac-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="55bac-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="55bac-107">Click New.</span></span>
3. <span data-ttu-id="55bac-108">Geben Sie im Feld "Zinscode" den Namen des Zinscodes ein.</span><span class="sxs-lookup"><span data-stu-id="55bac-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="55bac-109">Geben Sie im Feld Beschreibung eine Beschreibung für den Zinscode ein.</span><span class="sxs-lookup"><span data-stu-id="55bac-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="55bac-110">Wählen Sie "Monat" aus.</span><span class="sxs-lookup"><span data-stu-id="55bac-110">Select Month.</span></span>
6. <span data-ttu-id="55bac-111">Erweitern Sie den Abschnitt Einnahmen.</span><span class="sxs-lookup"><span data-stu-id="55bac-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="55bac-112">Erweitern Sie den Abschnitt "Einnahmen nach Währung".</span><span class="sxs-lookup"><span data-stu-id="55bac-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="55bac-113">Geben Sie im Feld "Konto für Sachkontobuchungen" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="55bac-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="55bac-114">Im Feld "Konto für Sachkontobuchungen" wählen Sie "Monate" aus.</span><span class="sxs-lookup"><span data-stu-id="55bac-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="55bac-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="55bac-115">Click Add.</span></span>
11. <span data-ttu-id="55bac-116">Geben Sie im Feld "Beschreibung" eine Beschreibung für die Währung und den Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="55bac-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="55bac-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="55bac-117">Click Save.</span></span>
13. <span data-ttu-id="55bac-118">Klicken Sie auf "Bereiche".</span><span class="sxs-lookup"><span data-stu-id="55bac-118">Click Ranges.</span></span>
14. <span data-ttu-id="55bac-119">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="55bac-119">Click New.</span></span>
15. <span data-ttu-id="55bac-120">Geben Sie den Von-Wert 0 ein und geben Sie dann die Zinsatz in Prozent pro Monat ein, der verwendet wird, um die Zinsen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="55bac-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="55bac-121">In unserem Beispiel ist das 1,5.</span><span class="sxs-lookup"><span data-stu-id="55bac-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="55bac-122">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="55bac-122">Click New.</span></span>
17. <span data-ttu-id="55bac-123">Geben Sie beim nächsten Von-Wert 4 ein. Dies ist der ersten Monat, für den Sie den neuen Zinsbetrag berechnen.</span><span class="sxs-lookup"><span data-stu-id="55bac-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="55bac-124">Geben Sie den Zinssatz pro Monat in Prozent ein, der verwendet wird, um die Zinsen zu berechnen, die in Monat 4. starten. In unserem Beispiel ist das 2.0.</span><span class="sxs-lookup"><span data-stu-id="55bac-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="55bac-125">In unserem Beispiel ist das 2,0.</span><span class="sxs-lookup"><span data-stu-id="55bac-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="55bac-126">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="55bac-126">Click New.</span></span>
20. <span data-ttu-id="55bac-127">Geben Sie beim nächsten Von-Wert 7 ein. Dies ist der nächste Monat, für den Sie den neuen Zinsbetrag berechnen.</span><span class="sxs-lookup"><span data-stu-id="55bac-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="55bac-128">Geben Sie den Zinssatz pro Monat in Prozent ein, der verwendet wird, um die Zinsen im Monat 7 zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="55bac-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="55bac-129">In unserem Beispiel ist das 2,5.</span><span class="sxs-lookup"><span data-stu-id="55bac-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="55bac-130">Klicken Sie auf "Schließen", um die Einrichtung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="55bac-130">Click Close to complete the setup.</span></span>

