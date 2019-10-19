---
title: Quellensteuer einrichten
description: In diesem Thema wird erläutert, wie die Quellensteuer eingerichtet wird.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185956"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="6331e-103">Quellensteuer einrichten</span><span class="sxs-lookup"><span data-stu-id="6331e-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6331e-104">In diesem Thema wird erläutert, wie die Quellensteuer eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="6331e-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="6331e-105">Die *Quellensteuer* ist eine Steuer für Kreditoren, bei der keine Mehrwertsteuerbuchungen entstehen.</span><span class="sxs-lookup"><span data-stu-id="6331e-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="6331e-106">Die Quellensteuer, die für Kreditorenzahlungen berechnet wird, ist eine Verbindlichkeit.</span><span class="sxs-lookup"><span data-stu-id="6331e-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="6331e-107">Daher sind nur Bilanz- oder Verbindlichkeitskonten gültige Kontenarten für das Buchen der Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="6331e-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="6331e-108">Diese Aufgabenanleitung veranschaulicht, wie die Quellensteuer eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="6331e-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="6331e-109">Wechseln Sie zu **Navigationsbereich > Module > Steuer > Indirekte Steuern > Quellensteuer > Quellensteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="6331e-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="6331e-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6331e-110">Select **New**.</span></span>
3. <span data-ttu-id="6331e-111">Geben Sie im Feld **Quellensteuercode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="6331e-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="6331e-112">Geben Sie im Feld **Quellensteuername** den Namen des Quellensteuercodes ein.</span><span class="sxs-lookup"><span data-stu-id="6331e-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="6331e-113">Wählen Sie im Feld **Hauptkonto** das Hauptkonto zum Buchen der Quellensteuerverbindlichkeiten aus.</span><span class="sxs-lookup"><span data-stu-id="6331e-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="6331e-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6331e-114">Select **Save**.</span></span>
7. <span data-ttu-id="6331e-115">Wählen Sie **Werte** aus, und markieren Sie den gewünschten Datensatz in der Liste.</span><span class="sxs-lookup"><span data-stu-id="6331e-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="6331e-116">Geben Sie im Feld **Wert** einen Prozentsatz ein, der für die Berechnung der Quellensteuer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6331e-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="6331e-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6331e-117">Select **Save**.</span></span>
10. <span data-ttu-id="6331e-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6331e-118">Close the page.</span></span>
11. <span data-ttu-id="6331e-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6331e-119">Select **Save**.</span></span>
12. <span data-ttu-id="6331e-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6331e-120">Close the page.</span></span>
13. <span data-ttu-id="6331e-121">Wechseln Sie zu **Navigationsbereich > Module > Steuer > Indirekte Steuern > Quellensteuer > Quellensteuergruppen**.</span><span class="sxs-lookup"><span data-stu-id="6331e-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="6331e-122">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="6331e-122">Select **New**.</span></span>
15. <span data-ttu-id="6331e-123">Geben Sie im Feld **Quellensteuergruppe** den Bezeichner der Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="6331e-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="6331e-124">Geben Sie im Feld **Beschreibung** den Namen der Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="6331e-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="6331e-125">Wählen Sie im Feld **Quellensteuercode** den Quellensteuercode aus.</span><span class="sxs-lookup"><span data-stu-id="6331e-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="6331e-126">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="6331e-126">Select **Save**.</span></span>
19. <span data-ttu-id="6331e-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6331e-127">Close the page.</span></span>

