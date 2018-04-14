--- 
title: Quellensteuer einrichten
description: "Die Quellensteuer ist eine Steuer für Kreditoren, bei der keine Mehrwertsteuerbuchungen entstehen."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ccaccd7b5b32431ac463925c887324a7607ae7dc
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="83650-103">Quellensteuer einrichten</span><span class="sxs-lookup"><span data-stu-id="83650-103">Set up withholding tax</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83650-104">Die Quellensteuer ist eine Steuer für Kreditoren, bei der keine Mehrwertsteuerbuchungen entstehen.</span><span class="sxs-lookup"><span data-stu-id="83650-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="83650-105">Die Quellensteuer, die für Kreditorenzahlungen berechnet wird, ist eine Verbindlichkeit.</span><span class="sxs-lookup"><span data-stu-id="83650-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="83650-106">Daher sind nur Bilanz- oder Verbindlichkeitskonten gültige Kontenarten für das Buchen der Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="83650-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="83650-107">Diese Aufgabenanleitung veranschaulicht, wie die Quellensteuer eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="83650-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="83650-108">Wechseln Sie zu "Steuer" Wechseln Sie zu Steuer > Indirekte Steuern > Quellensteuer > Quellensteuercodes.</span><span class="sxs-lookup"><span data-stu-id="83650-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="83650-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="83650-109">Click New.</span></span>
3. <span data-ttu-id="83650-110">Geben Sie im Feld "Quellensteuercode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="83650-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="83650-111">Geben Sie im Feld "Quellensteuername" den Namen des Quellensteuercodes ein.</span><span class="sxs-lookup"><span data-stu-id="83650-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="83650-112">Wählen Sie im Feld "Hauptkonto" das Hauptkonto zum Buchen der Quellensteuervebindlichkeiten aus.</span><span class="sxs-lookup"><span data-stu-id="83650-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="83650-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="83650-113">Click Save.</span></span>
7. <span data-ttu-id="83650-114">Klicken Sie auf "Werte".</span><span class="sxs-lookup"><span data-stu-id="83650-114">Click Values.</span></span>
8. <span data-ttu-id="83650-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="83650-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="83650-116">Geben Sie im Feld "Wert" einen Prozentsatz ein, der für die Berechnung der Quellensteuer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83650-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="83650-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="83650-117">Click Save.</span></span>
11. <span data-ttu-id="83650-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="83650-118">Close the page.</span></span>
12. <span data-ttu-id="83650-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="83650-119">Click Save.</span></span>
13. <span data-ttu-id="83650-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="83650-120">Close the page.</span></span>
14. <span data-ttu-id="83650-121">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Quellensteuer" > "Quellensteuerngruppen".</span><span class="sxs-lookup"><span data-stu-id="83650-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="83650-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="83650-122">Click New.</span></span>
16. <span data-ttu-id="83650-123">Geben Sie im Feld "Quellensteuergruppe" den Bezeichner der Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="83650-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="83650-124">Geben Sie im Feld "Beschreibung" den Namen Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="83650-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="83650-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="83650-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="83650-126">Wählen Sie im Feld "Quellensteuercode" den Quellensteuercode aus.</span><span class="sxs-lookup"><span data-stu-id="83650-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="83650-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="83650-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="83650-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="83650-128">Click Save.</span></span>


