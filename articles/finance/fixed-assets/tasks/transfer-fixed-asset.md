---
title: Eine Anlage übertragen
description: In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7588e0058713d7facf053aa269210fc88e5a3ff2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823883"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="3f117-103">Eine Anlage übertragen</span><span class="sxs-lookup"><span data-stu-id="3f117-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f117-104">In diesem Aufgabenleitfaden werden die Finanzdaten für ein Anlagenbuch aus einem Finanzdimensionssatz zu einem neuen Finanzdimensionssatz übertragen.</span><span class="sxs-lookup"><span data-stu-id="3f117-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="3f117-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f117-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="3f117-106">Wechseln Sie im Navigationsbereich zu **Module > Anlagen > Anlagen > Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="3f117-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="3f117-107">Suchen Sie in der Liste die zu übertragende Anlage und wählen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="3f117-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="3f117-108">Klicken Sie im Aktivitätsbereich auf **Anlage**.</span><span class="sxs-lookup"><span data-stu-id="3f117-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="3f117-109">Klicken Sie auf **Übertragen von Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="3f117-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="3f117-110">Geben Sie im Feld **Übertragungsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="3f117-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="3f117-111">Geben Sie Kommentare ein, um die Übertragung zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3f117-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="3f117-112">Diese Liste zeigt alle Bücher für die Anlage an.</span><span class="sxs-lookup"><span data-stu-id="3f117-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="3f117-113">Markieren Sie die Bücher, die Sie zu einem neuen Finanzdimensionssatz übertragen möchten.</span><span class="sxs-lookup"><span data-stu-id="3f117-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="3f117-114">Diese Liste zeigt die vorhandenen Finanzdimensionswerte für das ausgewählte Buch an.</span><span class="sxs-lookup"><span data-stu-id="3f117-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="3f117-115">Wählen Sie die Finanzdimension aus, die Sie für das ausgewählte Anlagenbuch aktualisieren möchten?</span><span class="sxs-lookup"><span data-stu-id="3f117-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="3f117-116">Klicken Sie im Feld **Finanzdimensionen** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3f117-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="3f117-117">Legen Sie andere Finanzdimensionswerte entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="3f117-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="3f117-118">Alle Finanzdimensionswerte ändern sich, wenn eine Übertragung erfolgt, ob ein Wert eingegeben wurde oder das Feld leer gelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="3f117-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="3f117-119">Wenn Sie beispielsweise einen Wert für die "Unternehmenseinheit" eingegeben haben und die Finanzdimensionen für "Kostenstelle" und "Abteilung" leer gelassen haben.</span><span class="sxs-lookup"><span data-stu-id="3f117-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="3f117-120">Wenn Ihre Kontostruktur leere Werte für "Kostenstelle" und "Abteilung" zulässt, würde die Übertragung dazu führen, dass jedes Wertmodell den neuen Wert für "Unternehmenseinheit" und einen Leerwert für "Kostenstelle" und "Abteilung" hätte.</span><span class="sxs-lookup"><span data-stu-id="3f117-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="3f117-121">Klicken Sie auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="3f117-121">Click **Update**.</span></span>
    * <span data-ttu-id="3f117-122">Sie haben die Gelegenheit, die Änderungen in der Vorschau anzeigen, bevor Sie die Übertragung abschließen.</span><span class="sxs-lookup"><span data-stu-id="3f117-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="3f117-123">Überprüfen Sie die Ergebnisse, bevor Sie die Anlagenbücher übertragen.</span><span class="sxs-lookup"><span data-stu-id="3f117-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="3f117-124">Klicken Sie auf **Übertragen**.</span><span class="sxs-lookup"><span data-stu-id="3f117-124">Click **Transfer**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]