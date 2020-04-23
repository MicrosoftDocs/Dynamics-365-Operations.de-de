---
title: Fracht manuell abstimmen
description: Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a0ff9aa1070272dd2cee357fb4fc001ffff8df1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206172"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="c2c2f-103">Fracht manuell abstimmen</span><span class="sxs-lookup"><span data-stu-id="c2c2f-103">Reconcile freight manually</span></span>

<span data-ttu-id="c2c2f-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="c2c2f-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="c2c2f-105">Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="c2c2f-106">Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="c2c2f-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="c2c2f-108">Eine Auslastung zur Abstimmung auswählen</span><span class="sxs-lookup"><span data-stu-id="c2c2f-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="c2c2f-109">Wechseln Sie zu Transportverwaltung > Planung > Ladungsplanungsworkbench.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="c2c2f-110">Deaktivieren Sie das Kontrollkästchen "'Versendet' und 'Empfangen' ausblenden".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="c2c2f-111">In der Liste wählen Sie die Auslastung aus, die die Auslastungskennung 00006 hat.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="c2c2f-112">Erstellen einer Spediteursrechnung</span><span class="sxs-lookup"><span data-stu-id="c2c2f-112">Create a carrier invoice</span></span>
<span data-ttu-id="c2c2f-113">Wenn Sie Fracht manuell abstimmen und nicht automatischen Spediteursrechnungen empfangen, können Sie eine Rechnung auf Basis des Frachtbriefs erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="c2c2f-114">Klicken Sie auf "Zugehörige Informationen".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-114">Click Related information.</span></span>
2. <span data-ttu-id="c2c2f-115">Klicken Sie auf Frachtbriefdetails.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="c2c2f-116">Klicken Sie auf "Frachtbriefrechnung generieren".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="c2c2f-117">Geben Sie im Feld "Rechnung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="c2c2f-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="c2c2f-119">Rechnung abstimmen</span><span class="sxs-lookup"><span data-stu-id="c2c2f-119">Reconcile the invoice</span></span>
<span data-ttu-id="c2c2f-120">Wenn Sie eine Spediteursrechnung und einen Frachtbrief abstimmen, passiert dies Position für Position.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="c2c2f-121">Klicken Sie auf "Frachtbriefe und Rechnungen abgleichen".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="c2c2f-122">Erweitern Sie den Abschnitt "Rechnungsdetails".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="c2c2f-123">Erweitern Sie den Abschnitt "Nicht abgeglichene Frachtbriefdetails".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="c2c2f-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="c2c2f-125">Klicken Sie auf "Abgleichen".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-125">Click Match.</span></span>
6. <span data-ttu-id="c2c2f-126">Erweitern Sie den Abschnitt "Abgeglichene Frachtbriefdetails".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="c2c2f-127">Rechnung zur Genehmigung übermitteln</span><span class="sxs-lookup"><span data-stu-id="c2c2f-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="c2c2f-128">Klicken Sie auf "Zur Genehmigung senden".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="c2c2f-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-129">Close the page.</span></span>
3. <span data-ttu-id="c2c2f-130">Deaktivieren Sie das Kontrollkästchen 'Ausblenden genehmigt'.</span><span class="sxs-lookup"><span data-stu-id="c2c2f-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="c2c2f-131">Klicken Sie auf Kreditorenrechnungserfassungen</span><span class="sxs-lookup"><span data-stu-id="c2c2f-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="c2c2f-132">Klicken Sie, um dem Link im Feld "Referenzerfassungsnummer".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="c2c2f-133">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="c2c2f-133">Click Lines.</span></span>

