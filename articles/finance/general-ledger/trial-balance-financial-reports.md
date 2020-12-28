---
title: Zwischenbilanzfinanzberichte
description: In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben. Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b48510febf5a5f9f4a01728b242d9750b3c62c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443424"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="c9afc-104">Zwischenbilanzfinanzberichte</span><span class="sxs-lookup"><span data-stu-id="c9afc-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9afc-105">In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c9afc-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="c9afc-106">Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="c9afc-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="c9afc-107">Standardzwischenbilanzberichte</span><span class="sxs-lookup"><span data-stu-id="c9afc-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="c9afc-108">Drei Zwischenbilanzberichte sind in der Finanzberichterstellung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c9afc-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="c9afc-109">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="c9afc-109">Default report</span></span>                                 | <span data-ttu-id="c9afc-110">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="c9afc-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9afc-111">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="c9afc-112">Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="c9afc-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="c9afc-113">Zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="c9afc-114">Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.</span><span class="sxs-lookup"><span data-stu-id="c9afc-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="c9afc-115">Jährlich zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="c9afc-116">Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein.</span><span class="sxs-lookup"><span data-stu-id="c9afc-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="c9afc-117">Bausteine</span><span class="sxs-lookup"><span data-stu-id="c9afc-117">Building blocks</span></span>
<span data-ttu-id="c9afc-118">Die Zwischenbilanzfinanzberichte verwenden die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="c9afc-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="c9afc-119">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="c9afc-119">Default report</span></span>                                 | <span data-ttu-id="c9afc-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-120">Row definition</span></span>          | <span data-ttu-id="c9afc-121">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="c9afc-122">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="c9afc-123">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-123">Trial Balance - Default</span></span> | <span data-ttu-id="c9afc-124">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="c9afc-125">Zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="c9afc-126">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-126">Trial Balance - Default</span></span> | <span data-ttu-id="c9afc-127">Zusammengefasste Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="c9afc-128">Jährlich zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="c9afc-129">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-129">Trial Balance - Default</span></span> | <span data-ttu-id="c9afc-130">Jährlich zusammengefasste Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="c9afc-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="c9afc-131">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-131">Row definition</span></span>

<span data-ttu-id="c9afc-132">Die Zeilendefinition, Zwischenbilanz – Standard, enthält eine einzelne Zeile, die alle Hauptkonten übernimmt.</span><span class="sxs-lookup"><span data-stu-id="c9afc-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="c9afc-133">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c9afc-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="c9afc-134">Wenn Sie den Bericht anzeigen, führen Sie einen Drilldown der Einzelzeile durch, um Details zu jedem Konto zu sehen.</span><span class="sxs-lookup"><span data-stu-id="c9afc-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="c9afc-135">Sie können die Zeilendefinition ändern, sodass sie weitere Details umfasst.</span><span class="sxs-lookup"><span data-stu-id="c9afc-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="c9afc-136">Um die Zeilendefinition "Zwischenbilanz - Standard" zu ändern, sodass sie Zeilen für alle Konten umfasst, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="c9afc-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="c9afc-137">Klicken Sie auf **Bearbeiten** und dann auf **Zeilen aus Dimensionen einfügen**.</span><span class="sxs-lookup"><span data-stu-id="c9afc-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="c9afc-138">Mit dem Befehl **Zeilen aus Dimensionen einfügen** können Sie die Dimensionen auswählen, die Sie in Ihrer Zeile haben möchten.</span><span class="sxs-lookup"><span data-stu-id="c9afc-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="c9afc-139">Für diese Zeilendefinition werden Sie **Hauptkonto** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9afc-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="c9afc-140">Stellen Sie sicher, dass das **Hauptkonto** alle kaufmännischen Und-Zeichen (&) enthält, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9afc-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="c9afc-141">Die Zeilendefinition enthält nun alle Hauptkonten für Ihres juristische Standardperson.</span><span class="sxs-lookup"><span data-stu-id="c9afc-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="c9afc-142">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-142">Column definition</span></span>

<span data-ttu-id="c9afc-143">Jeder Zwischenbilanzbericht verwendet eine andere Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="c9afc-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="c9afc-144">Diese Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c9afc-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="c9afc-145">**Ausführliche Zwischenbilanz - Standardypaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="c9afc-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="c9afc-146">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c9afc-147">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="c9afc-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="c9afc-148">**ATTR (3)** – Attribute:</span><span class="sxs-lookup"><span data-stu-id="c9afc-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="c9afc-149">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="c9afc-149">Transaction Date</span></span>
        -   <span data-ttu-id="c9afc-150">Beleg</span><span class="sxs-lookup"><span data-stu-id="c9afc-150">Voucher</span></span>
        -   <span data-ttu-id="c9afc-151">Erfassungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c9afc-151">Journal Description</span></span>
    -   <span data-ttu-id="c9afc-152">**FD** - Finanzdaten, die nur Soll enthalten</span><span class="sxs-lookup"><span data-stu-id="c9afc-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="c9afc-153">**FD** - Finanzdaten, die nur Haben enthahlten</span><span class="sxs-lookup"><span data-stu-id="c9afc-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="c9afc-154">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="c9afc-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="c9afc-155">**Zusammengefasste Zwischenbilanz - Standardypaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="c9afc-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="c9afc-156">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="c9afc-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="c9afc-157">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c9afc-158">**ATTR** – Ein Attribut:</span><span class="sxs-lookup"><span data-stu-id="c9afc-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="c9afc-159">Beleg</span><span class="sxs-lookup"><span data-stu-id="c9afc-159">Voucher</span></span>
    -   <span data-ttu-id="c9afc-160">**FD** - Die Anfangssaldoenfinanzdaten</span><span class="sxs-lookup"><span data-stu-id="c9afc-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="c9afc-161">**FD** - Finanzdaten, die nur Soll enthalten</span><span class="sxs-lookup"><span data-stu-id="c9afc-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="c9afc-162">**FD** - Finanzdaten, die nur Haben enthahlten</span><span class="sxs-lookup"><span data-stu-id="c9afc-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="c9afc-163">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="c9afc-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="c9afc-164">**CALC** – Der Abschlusssaldo</span><span class="sxs-lookup"><span data-stu-id="c9afc-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="c9afc-165">**Jährlich zusammengefasste Zwischenbilanz - Standard:**</span><span class="sxs-lookup"><span data-stu-id="c9afc-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="c9afc-166">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="c9afc-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="c9afc-167">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="c9afc-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c9afc-168">**ATTR** – Ein Attribut</span><span class="sxs-lookup"><span data-stu-id="c9afc-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="c9afc-169">Beleg</span><span class="sxs-lookup"><span data-stu-id="c9afc-169">Voucher</span></span>
    -   <span data-ttu-id="c9afc-170">**FD** - Die Anfangssaldoenfinanzdaten für das aktuelle Jahr</span><span class="sxs-lookup"><span data-stu-id="c9afc-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="c9afc-171">**FD** - Finanzdaten, die nur Soll für das aktuelle Jahr enthahlten</span><span class="sxs-lookup"><span data-stu-id="c9afc-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="c9afc-172">**FD** - Finanzdaten, die nur haben für das aktuelle Jahr entahlten</span><span class="sxs-lookup"><span data-stu-id="c9afc-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="c9afc-173">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="c9afc-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="c9afc-174">**CALC** – Der Abschlusssaldo</span><span class="sxs-lookup"><span data-stu-id="c9afc-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="c9afc-175">**FD** - Finanzdaten, die nur Soll für das letzte Jahr enthahlten</span><span class="sxs-lookup"><span data-stu-id="c9afc-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="c9afc-176">**FD** - Finanzdaten, die nur Haben für das letzte Jahr enthalten</span><span class="sxs-lookup"><span data-stu-id="c9afc-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="c9afc-177">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c9afc-177">Additional resources</span></span>
--------

[<span data-ttu-id="c9afc-178">Finanzberichterstellung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="c9afc-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="c9afc-179">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="c9afc-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="c9afc-180">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="c9afc-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



