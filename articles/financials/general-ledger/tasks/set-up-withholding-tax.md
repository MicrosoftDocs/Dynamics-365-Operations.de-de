---
title: Quellensteuer einrichten
description: Die Quellensteuer ist eine Steuer für Kreditoren, bei der keine Mehrwertsteuerbuchungen entstehen.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 382b6332665af2491563960a75d498a4f007aba8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337232"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="c9308-103">Quellensteuer einrichten</span><span class="sxs-lookup"><span data-stu-id="c9308-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9308-104">Die Quellensteuer ist eine Steuer für Kreditoren, bei der keine Mehrwertsteuerbuchungen entstehen.</span><span class="sxs-lookup"><span data-stu-id="c9308-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="c9308-105">Die Quellensteuer, die für Kreditorenzahlungen berechnet wird, ist eine Verbindlichkeit.</span><span class="sxs-lookup"><span data-stu-id="c9308-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="c9308-106">Daher sind nur Bilanz- oder Verbindlichkeitskonten gültige Kontenarten für das Buchen der Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="c9308-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="c9308-107">Diese Aufgabenanleitung veranschaulicht, wie die Quellensteuer eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="c9308-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="c9308-108">Wechseln Sie zu "Steuer" Wechseln Sie zu Steuer > Indirekte Steuern > Quellensteuer > Quellensteuercodes.</span><span class="sxs-lookup"><span data-stu-id="c9308-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="c9308-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c9308-109">Click New.</span></span>
3. <span data-ttu-id="c9308-110">Geben Sie im Feld "Quellensteuercode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c9308-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="c9308-111">Geben Sie im Feld "Quellensteuername" den Namen des Quellensteuercodes ein.</span><span class="sxs-lookup"><span data-stu-id="c9308-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="c9308-112">Wählen Sie im Feld "Hauptkonto" das Hauptkonto zum Buchen der Quellensteuervebindlichkeiten aus.</span><span class="sxs-lookup"><span data-stu-id="c9308-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="c9308-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c9308-113">Click Save.</span></span>
7. <span data-ttu-id="c9308-114">Klicken Sie auf "Werte".</span><span class="sxs-lookup"><span data-stu-id="c9308-114">Click Values.</span></span>
8. <span data-ttu-id="c9308-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c9308-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c9308-116">Geben Sie im Feld "Wert" einen Prozentsatz ein, der für die Berechnung der Quellensteuer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9308-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="c9308-117">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c9308-117">Click Save.</span></span>
11. <span data-ttu-id="c9308-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c9308-118">Close the page.</span></span>
12. <span data-ttu-id="c9308-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c9308-119">Click Save.</span></span>
13. <span data-ttu-id="c9308-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c9308-120">Close the page.</span></span>
14. <span data-ttu-id="c9308-121">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Quellensteuer" > "Quellensteuerngruppen".</span><span class="sxs-lookup"><span data-stu-id="c9308-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="c9308-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c9308-122">Click New.</span></span>
16. <span data-ttu-id="c9308-123">Geben Sie im Feld "Quellensteuergruppe" den Bezeichner der Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="c9308-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="c9308-124">Geben Sie im Feld "Beschreibung" den Namen Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="c9308-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="c9308-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c9308-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="c9308-126">Wählen Sie im Feld "Quellensteuercode" den Quellensteuercode aus.</span><span class="sxs-lookup"><span data-stu-id="c9308-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="c9308-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="c9308-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="c9308-128">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c9308-128">Click Save.</span></span>

