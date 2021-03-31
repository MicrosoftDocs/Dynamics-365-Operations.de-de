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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae7b13f743336e01f17248c8d6492b31e8044ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222310"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="a280f-103">Quellensteuer einrichten</span><span class="sxs-lookup"><span data-stu-id="a280f-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a280f-104">In diesem Thema wird erläutert, wie die Quellensteuer eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="a280f-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="a280f-105">Die *Quellensteuer* ist eine Steuer für Kreditoren, bei der keine Mehrwertsteuerbuchungen entstehen.</span><span class="sxs-lookup"><span data-stu-id="a280f-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="a280f-106">Die Quellensteuer, die für Kreditorenzahlungen berechnet wird, ist eine Verbindlichkeit.</span><span class="sxs-lookup"><span data-stu-id="a280f-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="a280f-107">Daher sind nur Bilanz- oder Verbindlichkeitskonten gültige Kontenarten für das Buchen der Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="a280f-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="a280f-108">Diese Aufgabenanleitung veranschaulicht, wie die Quellensteuer eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="a280f-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="a280f-109">Wechseln Sie zu **Navigationsbereich > Module > Steuer > Indirekte Steuern > Quellensteuer > Quellensteuercodes**.</span><span class="sxs-lookup"><span data-stu-id="a280f-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="a280f-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a280f-110">Select **New**.</span></span>
3. <span data-ttu-id="a280f-111">Geben Sie im Feld **Quellensteuercode** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a280f-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="a280f-112">Geben Sie im Feld **Quellensteuername** den Namen des Quellensteuercodes ein.</span><span class="sxs-lookup"><span data-stu-id="a280f-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="a280f-113">Wählen Sie im Feld **Hauptkonto** das Hauptkonto zum Buchen der Quellensteuerverbindlichkeiten aus.</span><span class="sxs-lookup"><span data-stu-id="a280f-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="a280f-114">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a280f-114">Select **Save**.</span></span>
7. <span data-ttu-id="a280f-115">Wählen Sie **Werte** aus, und markieren Sie den gewünschten Datensatz in der Liste.</span><span class="sxs-lookup"><span data-stu-id="a280f-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="a280f-116">Geben Sie im Feld **Wert** einen Prozentsatz ein, der für die Berechnung der Quellensteuer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a280f-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="a280f-117">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a280f-117">Select **Save**.</span></span>
10. <span data-ttu-id="a280f-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a280f-118">Close the page.</span></span>
11. <span data-ttu-id="a280f-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a280f-119">Select **Save**.</span></span>
12. <span data-ttu-id="a280f-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a280f-120">Close the page.</span></span>
13. <span data-ttu-id="a280f-121">Wechseln Sie zu **Navigationsbereich > Module > Steuer > Indirekte Steuern > Quellensteuer > Quellensteuergruppen**.</span><span class="sxs-lookup"><span data-stu-id="a280f-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="a280f-122">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a280f-122">Select **New**.</span></span>
15. <span data-ttu-id="a280f-123">Geben Sie im Feld **Quellensteuergruppe** den Bezeichner der Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="a280f-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="a280f-124">Geben Sie im Feld **Beschreibung** den Namen der Quellensteuergruppe ein.</span><span class="sxs-lookup"><span data-stu-id="a280f-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="a280f-125">Wählen Sie im Feld **Quellensteuercode** den Quellensteuercode aus.</span><span class="sxs-lookup"><span data-stu-id="a280f-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="a280f-126">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a280f-126">Select **Save**.</span></span>
19. <span data-ttu-id="a280f-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a280f-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]