---
title: Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten
description: Diese Aufgabenerfassung führt Sie Schritt für Schritt durch die Einstellungen von "Mehrwertsteuergruppen" und "Artikel-Mehrwertsteuergruppen".
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24210129f7595c6544234c20915f4003bf0e1eb8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984696"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="a519c-103">Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="a519c-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a519c-104">Diese Aufgabenerfassung führt Sie Schritt für Schritt durch die Einstellungen von "Mehrwertsteuergruppen" und "Artikel-Mehrwertsteuergruppen".</span><span class="sxs-lookup"><span data-stu-id="a519c-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="a519c-105">Mehrwertsteuergruppen sind Gruppen von Mehrwertsteuercodes, die Debitoren und Kreditoren zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a519c-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="a519c-106">Sie sind auch Sachkonten für Buchungen zugeordnet, die nicht für einen bestimmten Kreditor oder Debitor gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a519c-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="a519c-107">Die "Artikel-Mehrwertsteuergruppen" sind Gruppen von Mehrwertsteuercodes, die Ressourcen wie Produkte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a519c-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="a519c-108">Die Mehrwertsteuer für eine bestimmte Buchung wird über die Mehrwertsteuercodes bestimmt, die in der Mehrwertsteuergruppe und in der Artikel-Mehrwertsteuergruppe der Buchung eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="a519c-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="a519c-109">Mehrwertsteuer kann nur berechnet werden, wenn eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe für jede Buchung ausgewählt sind, für die Mehrwertsteuer berechnet oder erfasst werden muss.</span><span class="sxs-lookup"><span data-stu-id="a519c-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="a519c-110">Gehen Sie zu **Navigationsbereich > Module > Steuern > Indirekte Steuern > Umsatzsteuer > Umsatzsteuer > Umsatzsteuerkennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="a519c-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="a519c-111">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="a519c-111">Click **New**.</span></span>
3. <span data-ttu-id="a519c-112">Geben Sie im Feld **Umsatzsteuerkennzeichen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a519c-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="a519c-113">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a519c-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a519c-114">Schaltet die Erweiterung des Abschnitts **Setup** um.</span><span class="sxs-lookup"><span data-stu-id="a519c-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="a519c-115">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a519c-115">Click **Add**.</span></span>
7. <span data-ttu-id="a519c-116">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a519c-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a519c-117">Klicken Sie im Feld **Verkaufssteuerkennzeichen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a519c-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a519c-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a519c-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a519c-119">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a519c-119">Click **Save**.</span></span>
11. <span data-ttu-id="a519c-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a519c-120">Close the page.</span></span>
12. <span data-ttu-id="a519c-121">Gehen Sie zu **Steuern > Indirekte Steuern > Umsatzsteuer > Artikel Umsatzsteuerkennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="a519c-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="a519c-122">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="a519c-122">Click **New**.</span></span>
14. <span data-ttu-id="a519c-123">Geben Sie im Feld **Position Umsatzsteuerkennzeichen** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a519c-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="a519c-124">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a519c-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="a519c-125">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a519c-125">Click **Add**.</span></span>
17. <span data-ttu-id="a519c-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a519c-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a519c-127">Klicken Sie im Feld **Verkaufssteuerkennzeichen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a519c-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="a519c-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a519c-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="a519c-129">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a519c-129">Click **Save**.</span></span>

