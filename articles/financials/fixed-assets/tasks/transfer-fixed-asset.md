--- 
title: "Eine Anlage übertragen"
description: "In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ea0e54dad6d8a48d628fc831b3fdbe7c0f68e892
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="cd175-103">Eine Anlage übertragen</span><span class="sxs-lookup"><span data-stu-id="cd175-103">Transfer a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd175-104">In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.</span><span class="sxs-lookup"><span data-stu-id="cd175-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="cd175-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd175-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="cd175-106">Wechseln Sie zu Anlagen > Anlagen > Anlagen.</span><span class="sxs-lookup"><span data-stu-id="cd175-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="cd175-107">Suchen Sie in der Liste die zu übertragende Anlage und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="cd175-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="cd175-108">Klicken Sie im Aktivitätsbereich auf "Anlage".</span><span class="sxs-lookup"><span data-stu-id="cd175-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="cd175-109">Klicken Sie auf "Anlagen übertragen".</span><span class="sxs-lookup"><span data-stu-id="cd175-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="cd175-110">Geben Sie im Feld "Übertragungsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="cd175-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="cd175-111">Geben Sie Kommentare ein, um die Übertragung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cd175-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="cd175-112">Diese Liste zeigt alle Bücher für die Anlage an.</span><span class="sxs-lookup"><span data-stu-id="cd175-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="cd175-113">Markieren Sie die Bücher, die Sie zu einem neuen Finanzdimensionssatz übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="cd175-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="cd175-114">Diese Liste zeigt die vorhandenen Finanzdimensionswerte für das ausgewählte Buch an.</span><span class="sxs-lookup"><span data-stu-id="cd175-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="cd175-115">Wählen Sie die Finanzdimension aus, die Sie für das ausgewählte Anlagenbuch aktualisieren möchten?</span><span class="sxs-lookup"><span data-stu-id="cd175-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="cd175-116">Klicken Sie im Feld "Finanzdimensionen" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cd175-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="cd175-117">Legen Sie andere Finanzdimensionswerte entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="cd175-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="cd175-118">Alle Finanzdimensionswerte ändern sich, wenn eine Übertragung erfolgt, ob ein Wert eingegeben wurde oder das Feld leer gelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="cd175-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="cd175-119">Wenn Sie beispielsweise einen Wert für die "Unternehmenseinheit" eingegeben haben und die Finanzdimensionen für "Kostenstelle" und "Abteilung" leer gelassen haben.</span><span class="sxs-lookup"><span data-stu-id="cd175-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="cd175-120">Wenn Ihre Kontostruktur leere Werte für "Kostenstelle" und "Abteilung" zulässt, würde die Übertragung dazu führen, dass jedes Wertmodell den neuen Wert für "Unternehmenseinheit" und einen Leerwert für "Kostenstelle" und "Abteilung" hätte.</span><span class="sxs-lookup"><span data-stu-id="cd175-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="cd175-121">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cd175-121">Click Update.</span></span>
    * <span data-ttu-id="cd175-122">Sie haben die Gelegenheit, die Änderungen in der Vorschau anzeigen, bevor Sie die Übertragung abschließen.</span><span class="sxs-lookup"><span data-stu-id="cd175-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="cd175-123">Überprüfen Sie die Ergebnisse, bevor Sie die Anlagenbücher übertragen.</span><span class="sxs-lookup"><span data-stu-id="cd175-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="cd175-124">Klicken Sie auf Übertragen.</span><span class="sxs-lookup"><span data-stu-id="cd175-124">Click Transfer.</span></span>


