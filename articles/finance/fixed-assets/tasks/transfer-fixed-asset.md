---
title: Eine Anlage übertragen
description: In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138048"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="eb0db-103">Eine Anlage übertragen</span><span class="sxs-lookup"><span data-stu-id="eb0db-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb0db-104">In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="eb0db-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb0db-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="eb0db-106">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="eb0db-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="eb0db-107">Suchen Sie in der Liste die zu übertragende Anlage und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="eb0db-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="eb0db-108">Klicken Sie im Aktivitätsbereich auf **Anlage**.</span><span class="sxs-lookup"><span data-stu-id="eb0db-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="eb0db-109">Klicken Sie auf **Übertragen von Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="eb0db-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="eb0db-110">Geben Sie im Feld **Übertragungsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="eb0db-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="eb0db-111">Geben Sie Kommentare ein, um die Übertragung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="eb0db-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="eb0db-112">Diese Liste zeigt alle Bücher für die Anlage an.</span><span class="sxs-lookup"><span data-stu-id="eb0db-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="eb0db-113">Markieren Sie die Bücher, die Sie zu einem neuen Finanzdimensionssatz übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="eb0db-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="eb0db-114">Diese Liste zeigt die vorhandenen Finanzdimensionswerte für das ausgewählte Buch an.</span><span class="sxs-lookup"><span data-stu-id="eb0db-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="eb0db-115">Wählen Sie die Finanzdimension aus, die Sie für das ausgewählte Anlagenbuch aktualisieren möchten?</span><span class="sxs-lookup"><span data-stu-id="eb0db-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="eb0db-116">Klicken Sie im Feld **Finanzdimensionen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="eb0db-117">Legen Sie andere Finanzdimensionswerte entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="eb0db-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="eb0db-118">Alle Finanzdimensionswerte ändern sich, wenn eine Übertragung erfolgt, ob ein Wert eingegeben wurde oder das Feld leer gelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="eb0db-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="eb0db-119">Wenn Sie beispielsweise einen Wert für die "Unternehmenseinheit" eingegeben haben und die Finanzdimensionen für "Kostenstelle" und "Abteilung" leer gelassen haben.</span><span class="sxs-lookup"><span data-stu-id="eb0db-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="eb0db-120">Wenn Ihre Kontostruktur leere Werte für "Kostenstelle" und "Abteilung" zulässt, würde die Übertragung dazu führen, dass jedes Wertmodell den neuen Wert für "Unternehmenseinheit" und einen Leerwert für "Kostenstelle" und "Abteilung" hätte.</span><span class="sxs-lookup"><span data-stu-id="eb0db-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="eb0db-121">Klicken Sie auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="eb0db-121">Click **Update**.</span></span>
    * <span data-ttu-id="eb0db-122">Sie haben die Gelegenheit, die Änderungen in der Vorschau anzeigen, bevor Sie die Übertragung abschließen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="eb0db-123">Überprüfen Sie die Ergebnisse, bevor Sie die Anlagenbücher übertragen.</span><span class="sxs-lookup"><span data-stu-id="eb0db-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="eb0db-124">Klicken Sie auf **Übertragen**.</span><span class="sxs-lookup"><span data-stu-id="eb0db-124">Click **Transfer**.</span></span>

