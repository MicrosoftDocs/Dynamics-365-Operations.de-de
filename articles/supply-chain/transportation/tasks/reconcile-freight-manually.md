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
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc4fc51955544df4d0156a4c83bcc5b5a0e13df3
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016975"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="a3de6-103">Fracht manuell abstimmen</span><span class="sxs-lookup"><span data-stu-id="a3de6-103">Reconcile freight manually</span></span>

<span data-ttu-id="a3de6-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="a3de6-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="a3de6-105">Dieses Verfahren zeigt, wie Fracht manuell abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="a3de6-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="a3de6-106">Diese Einstellung wird normalerweise von einem Transportkoordinator vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="a3de6-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="a3de6-107">Sie können diese Prozedur im Demodatunternehmen USMF verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3de6-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="a3de6-108">Eine Auslastung zur Abstimmung auswählen</span><span class="sxs-lookup"><span data-stu-id="a3de6-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="a3de6-109">Wechseln Sie zu Transportverwaltung > Planung > Ladungsplanungsworkbench.</span><span class="sxs-lookup"><span data-stu-id="a3de6-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="a3de6-110">Deaktivieren Sie das Kontrollkästchen "'Versendet' und 'Empfangen' ausblenden".</span><span class="sxs-lookup"><span data-stu-id="a3de6-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="a3de6-111">In der Liste wählen Sie die Auslastung aus, die die Auslastungskennung 00006 hat.</span><span class="sxs-lookup"><span data-stu-id="a3de6-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="a3de6-112">Erstellen einer Spediteursrechnung</span><span class="sxs-lookup"><span data-stu-id="a3de6-112">Create a carrier invoice</span></span>
<span data-ttu-id="a3de6-113">Wenn Sie Fracht manuell abstimmen und nicht automatischen Spediteursrechnungen empfangen, können Sie eine Rechnung auf Basis des Frachtbriefs erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3de6-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="a3de6-114">Klicken Sie auf "Zugehörige Informationen".</span><span class="sxs-lookup"><span data-stu-id="a3de6-114">Click Related information.</span></span>
2. <span data-ttu-id="a3de6-115">Klicken Sie auf Frachtbriefdetails.</span><span class="sxs-lookup"><span data-stu-id="a3de6-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="a3de6-116">Klicken Sie auf "Frachtbriefrechnung generieren".</span><span class="sxs-lookup"><span data-stu-id="a3de6-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="a3de6-117">Geben Sie im Feld "Rechnung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a3de6-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="a3de6-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a3de6-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="a3de6-119">Rechnung abstimmen</span><span class="sxs-lookup"><span data-stu-id="a3de6-119">Reconcile the invoice</span></span>
<span data-ttu-id="a3de6-120">Wenn Sie eine Spediteursrechnung und einen Frachtbrief abstimmen, passiert dies Position für Position.</span><span class="sxs-lookup"><span data-stu-id="a3de6-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="a3de6-121">Klicken Sie auf "Frachtbriefe und Rechnungen abgleichen".</span><span class="sxs-lookup"><span data-stu-id="a3de6-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="a3de6-122">Erweitern Sie den Abschnitt "Rechnungsdetails".</span><span class="sxs-lookup"><span data-stu-id="a3de6-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="a3de6-123">Erweitern Sie den Abschnitt "Nicht abgeglichene Frachtbriefdetails".</span><span class="sxs-lookup"><span data-stu-id="a3de6-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="a3de6-124">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="a3de6-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a3de6-125">Klicken Sie auf "Abgleichen".</span><span class="sxs-lookup"><span data-stu-id="a3de6-125">Click Match.</span></span>
6. <span data-ttu-id="a3de6-126">Erweitern Sie den Abschnitt "Abgeglichene Frachtbriefdetails".</span><span class="sxs-lookup"><span data-stu-id="a3de6-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="a3de6-127">Rechnung zur Genehmigung übermitteln</span><span class="sxs-lookup"><span data-stu-id="a3de6-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="a3de6-128">Klicken Sie auf "Zur Genehmigung senden".</span><span class="sxs-lookup"><span data-stu-id="a3de6-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="a3de6-129">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a3de6-129">Close the page.</span></span>
3. <span data-ttu-id="a3de6-130">Deaktivieren Sie das Kontrollkästchen 'Ausblenden genehmigt'.</span><span class="sxs-lookup"><span data-stu-id="a3de6-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="a3de6-131">Klicken Sie auf Kreditorenrechnungserfassungen</span><span class="sxs-lookup"><span data-stu-id="a3de6-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="a3de6-132">Klicken Sie, um dem Link im Feld "Referenzerfassungsnummer".</span><span class="sxs-lookup"><span data-stu-id="a3de6-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="a3de6-133">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="a3de6-133">Click Lines.</span></span>

