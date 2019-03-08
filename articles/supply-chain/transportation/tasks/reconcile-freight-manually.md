---
title: Fracht manuell abstimmen
description: Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "351883"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="798ea-103">Fracht manuell abstimmen</span><span class="sxs-lookup"><span data-stu-id="798ea-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="798ea-104">Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="798ea-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="798ea-105">Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="798ea-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="798ea-106">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="798ea-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="798ea-107">Eine Auslastung zur Abstimmung auswählen</span><span class="sxs-lookup"><span data-stu-id="798ea-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="798ea-108">Wechseln Sie zu Transportverwaltung > Planung > Ladungsplanungsworkbench.</span><span class="sxs-lookup"><span data-stu-id="798ea-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="798ea-109">Deaktivieren Sie das Kontrollkästchen "'Versendet' und 'Empfangen' ausblenden".</span><span class="sxs-lookup"><span data-stu-id="798ea-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="798ea-110">In der Liste wählen Sie die Auslastung aus, die die Auslastungskennung 00006 hat.</span><span class="sxs-lookup"><span data-stu-id="798ea-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="798ea-111">Erstellen einer Spediteursrechnung</span><span class="sxs-lookup"><span data-stu-id="798ea-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="798ea-112">Wenn Sie Fracht manuell abstimmen und nicht automatischen Spediteursrechnungen empfangen, können Sie eine Rechnung auf Basis des Frachtbriefs erstellen.</span><span class="sxs-lookup"><span data-stu-id="798ea-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="798ea-113">Klicken Sie auf "Zugehörige Informationen".</span><span class="sxs-lookup"><span data-stu-id="798ea-113">Click Related information.</span></span>
2. <span data-ttu-id="798ea-114">Klicken Sie auf Frachtbriefdetails.</span><span class="sxs-lookup"><span data-stu-id="798ea-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="798ea-115">Klicken Sie auf "Frachtbriefrechnung generieren".</span><span class="sxs-lookup"><span data-stu-id="798ea-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="798ea-116">Geben Sie im Feld "Rechnung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="798ea-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="798ea-117">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="798ea-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="798ea-118">Rechnung abstimmen</span><span class="sxs-lookup"><span data-stu-id="798ea-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="798ea-119">Wenn Sie eine Spediteursrechnung und einen Frachtbrief abstimmen, passiert dies Position für Position.</span><span class="sxs-lookup"><span data-stu-id="798ea-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="798ea-120">Klicken Sie auf "Frachtbriefe und Rechnungen abgleichen".</span><span class="sxs-lookup"><span data-stu-id="798ea-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="798ea-121">Erweitern Sie den Abschnitt "Rechnungsdetails".</span><span class="sxs-lookup"><span data-stu-id="798ea-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="798ea-122">Erweitern Sie den Abschnitt "Nicht abgeglichene Frachtbriefdetails".</span><span class="sxs-lookup"><span data-stu-id="798ea-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="798ea-123">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="798ea-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="798ea-124">Klicken Sie auf "Abgleichen".</span><span class="sxs-lookup"><span data-stu-id="798ea-124">Click Match.</span></span>
6. <span data-ttu-id="798ea-125">Erweitern Sie den Abschnitt "Abgeglichene Frachtbriefdetails".</span><span class="sxs-lookup"><span data-stu-id="798ea-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="798ea-126">Rechnung zur Genehmigung übermitteln</span><span class="sxs-lookup"><span data-stu-id="798ea-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="798ea-127">Klicken Sie auf "Zur Genehmigung senden".</span><span class="sxs-lookup"><span data-stu-id="798ea-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="798ea-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="798ea-128">Close the page.</span></span>
3. <span data-ttu-id="798ea-129">Deaktivieren Sie das Kontrollkästchen 'Ausblenden genehmigt'.</span><span class="sxs-lookup"><span data-stu-id="798ea-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="798ea-130">Klicken Sie auf Kreditorenrechnungserfassungen</span><span class="sxs-lookup"><span data-stu-id="798ea-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="798ea-131">Klicken Sie, um dem Link im Feld "Referenzerfassungsnummer".</span><span class="sxs-lookup"><span data-stu-id="798ea-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="798ea-132">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="798ea-132">Click Lines.</span></span>

