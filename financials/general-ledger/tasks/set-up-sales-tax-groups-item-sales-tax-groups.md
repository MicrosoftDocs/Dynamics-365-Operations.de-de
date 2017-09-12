--- 
title: Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten
description: "Diese Aufgabenerfassung führt Sie Schritt für Schritt durch die Einstellungen von \"Mehrwertsteuergruppen\" und \"Artikel-Mehrwertsteuergruppen\"."
author: twheeloc
manager: AnnBe
ms.date: 11/10/2015
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
ms.openlocfilehash: 4d7f1093edcfff65fd466fa8138b1bb5203648b3
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="a1a01-103">Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten</span><span class="sxs-lookup"><span data-stu-id="a1a01-103">Set up sales tax groups and item sales tax groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1a01-104">Diese Aufgabenerfassung führt Sie Schritt für Schritt durch die Einstellungen von "Mehrwertsteuergruppen" und "Artikel-Mehrwertsteuergruppen".</span><span class="sxs-lookup"><span data-stu-id="a1a01-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="a1a01-105">Mehrwertsteuergruppen sind Gruppen von Mehrwertsteuercodes, die Debitoren und Kreditoren zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a1a01-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="a1a01-106">Sie sind auch Sachkonten für Buchungen zugeordnet, die nicht für einen bestimmten Kreditor oder Debitor gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="a1a01-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="a1a01-107">Die "Artikel-Mehrwertsteuergruppen" sind Gruppen von Mehrwertsteuercodes, die Ressourcen wie Produkte zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a1a01-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="a1a01-108">Die Mehrwertsteuer für eine bestimmte Buchung wird über die Mehrwertsteuercodes bestimmt, die in der Mehrwertsteuergruppe und in der Artikel-Mehrwertsteuergruppe der Buchung eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="a1a01-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="a1a01-109">Mehrwertsteuer kann nur berechnet werden, wenn eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe für jede Buchung ausgewählt sind, für die Mehrwertsteuer berechnet oder erfasst werden muss.</span><span class="sxs-lookup"><span data-stu-id="a1a01-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="a1a01-110">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuergruppen".</span><span class="sxs-lookup"><span data-stu-id="a1a01-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="a1a01-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a1a01-111">Click New.</span></span>
3. <span data-ttu-id="a1a01-112">Geben Sie im Feld "Mehrwertsteuergruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a1a01-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="a1a01-113">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a1a01-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a1a01-114">Schalten Sie die Erweiterung Abschnitts "Einstellungen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="a1a01-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="a1a01-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a1a01-115">Click Add.</span></span>
7. <span data-ttu-id="a1a01-116">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a1a01-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="a1a01-117">Klicken Sie im Feld "Mehrwertsteuercode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a1a01-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a1a01-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a1a01-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a1a01-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a1a01-119">Click Save.</span></span>
11. <span data-ttu-id="a1a01-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a1a01-120">Close the page.</span></span>
12. <span data-ttu-id="a1a01-121">Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Artikel-Mehrwertsteuergruppen".</span><span class="sxs-lookup"><span data-stu-id="a1a01-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="a1a01-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a1a01-122">Click New.</span></span>
14. <span data-ttu-id="a1a01-123">Geben Sie im Feld "Artikel-Mehrwertsteuergruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a1a01-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="a1a01-124">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a1a01-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="a1a01-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a1a01-125">Click Add.</span></span>
17. <span data-ttu-id="a1a01-126">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a1a01-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a1a01-127">Klicken Sie im Feld "Mehrwertsteuercode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a1a01-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="a1a01-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a1a01-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="a1a01-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a1a01-129">Click Save.</span></span>


