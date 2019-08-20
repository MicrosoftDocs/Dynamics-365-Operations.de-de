---
title: Projektkostenabgrenzung beim Empfang von Bestellungen
description: In diesem Thema wird beschrieben, wie Projektkosten von Bestellbelegen in Microsoft Dynamics 365 for Finance and Operations nachverfolgt werden können.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c1397107c179da56e8dcf4b556140dc06d8f14d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834584"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="d451c-103">Projektkostenabgrenzung beim Empfang von Bestellungen</span><span class="sxs-lookup"><span data-stu-id="d451c-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d451c-104">In diesem Thema wird beschrieben, wie Projektkosten von Bestellbelegen in Microsoft Dynamics 365 for Finance and Operations nachverfolgt werden können.</span><span class="sxs-lookup"><span data-stu-id="d451c-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="d451c-105">Rechnungen für ein Projekt werden häufig später als die Waren und Dienstleistungen geliefert, was erheblichen Auswirkungen auf Projektleistungskennzahlen (KPIs) haben kann.</span><span class="sxs-lookup"><span data-stu-id="d451c-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="d451c-106">Es wichtig, in der Lage zu sein, diese Buchungen in Projektberichten und Finanzberichten zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d451c-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="d451c-107">Das folgende Beiespielszenario illustriert dieses.</span><span class="sxs-lookup"><span data-stu-id="d451c-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="d451c-108">Contoso Consulting hat ein neues Cloudbereitstellungsprojekt gestartet.</span><span class="sxs-lookup"><span data-stu-id="d451c-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="d451c-109">Eine Bestellung wird erstellt, um einen Computer für das Projekt zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="d451c-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="d451c-110">Der Computer kostet 1500 USD und Installationsdienstleistungen kosten 150 USD.</span><span class="sxs-lookup"><span data-stu-id="d451c-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="d451c-111">Der Kreditor hat den Computer geliefert und installiert, aber die Rechnung noch nicht Contoso Consulting erreicht.</span><span class="sxs-lookup"><span data-stu-id="d451c-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="d451c-112">Der Projektmanager möchte eine Projektkostenabgrenzung von 1650 USD haben, bevor die Rechnung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d451c-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="d451c-113">Diese Kosten müssen in den Monatsendefinanzaufstellungen des Unternehmens auch angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d451c-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="d451c-114">Die antizipierten Kosten müssen auf der Finanzebene und Projektebene und für Berichtszwecke erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="d451c-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="d451c-115">In Finance and Operations kann die wertmäßige Aktualisierung des Produktzugangs für den Artikel und die Beschaffungskategorien nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="d451c-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="d451c-116">Für Artikel auf der **Kreditorenparameter** Seite wählen Sie die **Produktzugänge im Sachkonto** Option aus.</span><span class="sxs-lookup"><span data-stu-id="d451c-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="d451c-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="d451c-118">Für auf Beschaffungskategorien der **Kategorierichtlinienregel** Seite, wählen Sie **Einkauf** Richtlinien, und wählen Sie dann **Einkaufausgaben fallen auf Beleg an** für jede Beschaffungskategorie aus.</span><span class="sxs-lookup"><span data-stu-id="d451c-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="d451c-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="d451c-120">Die **Einkaufaufwendungen nicht fakturiert** und **Einkaufsabgrenzung** Konten in **Buchungseinstellungen** verwendet werden, wenn Belege, die dem Produktzugang zugeordnet sind, gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="d451c-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="d451c-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="d451c-122">Das Verwenden dieses Szenarios gleichen lassen Sie prüfen, wie Sie das Buchen eines Produktzugangs Hauptbuch und Projektinformationen auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d451c-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="d451c-123">**Schritt 1:** Erstellen und Bestätigen Sie eine neue Bestellung für das Projekt, den Einkauf eines Computers für 1500 USD und der Installations-Services für 150 USD erfasst.</span><span class="sxs-lookup"><span data-stu-id="d451c-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="d451c-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="d451c-125">Wenn die Bestellung bestätigt wurde, werden Buchungen für die zugesagten Kosten für das Projekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d451c-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="d451c-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="d451c-127">Die Buchungen für die zugesagten Kosten besitzen das **Buchungs-Ursprung** Feld auf **Bestellung** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d451c-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="d451c-128">Eine Bestellung der Informationen erstellt, bestätigend, keine Buchungen für ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="d451c-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="d451c-129">**Schritt 2:** Waren und Dienstleistungen geliefert wird ab und ein Produktzugang erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="d451c-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="d451c-130">Beim Buchen eines Produktzugangs generiert und gebucht einen Beleg auf Sachkonto.</span><span class="sxs-lookup"><span data-stu-id="d451c-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="d451c-131">Der Beleg für die Einkaufaufwendungen, das Konto und das Kreditkaufabgrenzungskonto nicht.</span><span class="sxs-lookup"><span data-stu-id="d451c-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="d451c-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d451c-133">Einen Produktzugang buchen verwendet die Buchungseinstellungen für Beschaffungskategorien und Produkte und nicht die Buchungseinstellungen für die Projektkategorien.</span><span class="sxs-lookup"><span data-stu-id="d451c-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="d451c-134">Um Finanzauswirkungen von Einkaufabgrenzungen ordnungsgemäß widerzuspiegeln, muss diese Einstellung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="d451c-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="d451c-135">Es ist möglich, Beschaffungskategorien auf die Projektkategorien auf der Seite **Beschaffungskategorie** zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d451c-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="d451c-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="d451c-137">**Schritt 3:** Standardmäßige Entwurfskreditorenrechnung erstellen</span><span class="sxs-lookup"><span data-stu-id="d451c-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="d451c-138">In Finance and Operations wirkt sich das Buchen eines Produktzugangs nicht auf die Projektinformationen aus.</span><span class="sxs-lookup"><span data-stu-id="d451c-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="d451c-139">Als Problemumgehung können Sie ein Entwurfskreditorenrechnungs-Recht erstellen, wenn Sie den Empfang von Bestellungen gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="d451c-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="d451c-140">Wechseln Sie zu **Bestellung** Seite &gt; **Rechnungsregisterkarte** &gt; **Generieren** &gt; **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="d451c-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="d451c-141">Dies erstellt ein ausstehendes Rechnungsdokument, das Projektinformationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d451c-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="d451c-142">Das Erstellen einer Entwurfskreditorenrechnung generiert ausstehende Projektbuchungen.</span><span class="sxs-lookup"><span data-stu-id="d451c-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="d451c-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="d451c-144">In der **Zugesagte Kosten** Seite werden die in Schritt 1 erstellten Datensätze geschlossen und neue Datensätze werden erstellt, damit die Zusage von der ausstehenden Kreditorenrechnung wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d451c-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="d451c-145">Die **Buchungsgrundlage** Feld für die zugesagten Kosten wird auf **Kreditorenrechnung** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d451c-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="d451c-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="d451c-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="d451c-147">Die Kreditorenrechnung wird zwar weiterhin im einem ausstehenden Status, wenn die tatsächliche Kreditorenrechnung Eingang.</span><span class="sxs-lookup"><span data-stu-id="d451c-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



