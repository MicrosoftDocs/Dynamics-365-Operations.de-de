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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9e8c16724364df4dd62150056299e818470aa63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "309103"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="0485f-104">Zwischenbilanzfinanzberichte</span><span class="sxs-lookup"><span data-stu-id="0485f-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0485f-105">In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0485f-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="0485f-106">Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="0485f-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="0485f-107">Standardzwischenbilanzberichte</span><span class="sxs-lookup"><span data-stu-id="0485f-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="0485f-108">Drei Zwischenbilanzberichte sind in der Finanzberichterstellung in Microsoft Dynamics 365 for Finance and Operations verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0485f-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="0485f-109">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="0485f-109">Default report</span></span>                                 | <span data-ttu-id="0485f-110">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="0485f-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0485f-111">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="0485f-112">Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="0485f-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="0485f-113">Zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="0485f-114">Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.</span><span class="sxs-lookup"><span data-stu-id="0485f-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="0485f-115">Jährlich zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="0485f-116">Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein.</span><span class="sxs-lookup"><span data-stu-id="0485f-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="0485f-117">Bausteine</span><span class="sxs-lookup"><span data-stu-id="0485f-117">Building blocks</span></span>
<span data-ttu-id="0485f-118">Die Zwischenbilanzfinanzberichte verwenden die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="0485f-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="0485f-119">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="0485f-119">Default report</span></span>                                 | <span data-ttu-id="0485f-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-120">Row definition</span></span>          | <span data-ttu-id="0485f-121">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="0485f-122">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="0485f-123">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-123">Trial Balance - Default</span></span> | <span data-ttu-id="0485f-124">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="0485f-125">Zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="0485f-126">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-126">Trial Balance - Default</span></span> | <span data-ttu-id="0485f-127">Zusammengefasste Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="0485f-128">Jährlich zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="0485f-129">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-129">Trial Balance - Default</span></span> | <span data-ttu-id="0485f-130">Jährlich zusammengefasste Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="0485f-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="0485f-131">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-131">Row definition</span></span>

<span data-ttu-id="0485f-132">Die Zeilendefinition, Zwischenbilanz – Standard, enthält eine einzelne Zeile, die alle Hauptkonten übernimmt.</span><span class="sxs-lookup"><span data-stu-id="0485f-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="0485f-133">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0485f-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="0485f-134">Wenn Sie den Bericht anzeigen, führen Sie einen Drilldown der Einzelzeile durch, um Details zu jedem Konto zu sehen.</span><span class="sxs-lookup"><span data-stu-id="0485f-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="0485f-135">Sie können die Zeilendefinition ändern, sodass sie weitere Details umfasst.</span><span class="sxs-lookup"><span data-stu-id="0485f-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="0485f-136">Um die Zeilendefinition "Zwischenbilanz - Standard" zu ändern, sodass sie Zeilen für alle Konten umfasst, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="0485f-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="0485f-137">Klicken Sie auf **Bearbeiten** und dann auf **Zeilen aus Dimensionen einfügen**.</span><span class="sxs-lookup"><span data-stu-id="0485f-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="0485f-138">Mit dem Befehl **Zeilen aus Dimensionen einfügen** können Sie die Dimensionen auswählen, die Sie in Ihrer Zeile haben möchten.</span><span class="sxs-lookup"><span data-stu-id="0485f-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="0485f-139">Für diese Zeilendefinition werden Sie **Hauptkonto** verwenden.</span><span class="sxs-lookup"><span data-stu-id="0485f-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="0485f-140">Stellen Sie sicher, dass das **Hauptkonto** alle kaufmännischen Und-Zeichen (&) enthält, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="0485f-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="0485f-141">Die Zeilendefinition enthält nun alle Hauptkonten für Ihres juristische Standardperson.</span><span class="sxs-lookup"><span data-stu-id="0485f-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="0485f-142">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-142">Column definition</span></span>

<span data-ttu-id="0485f-143">Jeder Zwischenbilanzbericht verwendet eine andere Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="0485f-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="0485f-144">Diese Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0485f-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="0485f-145">**Ausführliche Zwischenbilanz - Standardypaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="0485f-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="0485f-146">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0485f-147">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="0485f-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="0485f-148">**ATTR (3)** – Attribute:</span><span class="sxs-lookup"><span data-stu-id="0485f-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="0485f-149">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="0485f-149">Transaction Date</span></span>
        -   <span data-ttu-id="0485f-150">Beleg</span><span class="sxs-lookup"><span data-stu-id="0485f-150">Voucher</span></span>
        -   <span data-ttu-id="0485f-151">Erfassungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0485f-151">Journal Description</span></span>
    -   <span data-ttu-id="0485f-152">**FD** - Finanzdaten, die nur Soll enthalten</span><span class="sxs-lookup"><span data-stu-id="0485f-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="0485f-153">**FD** - Finanzdaten, die nur Haben enthahlten</span><span class="sxs-lookup"><span data-stu-id="0485f-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="0485f-154">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="0485f-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="0485f-155">**Zusammengefasste Zwischenbilanz - Standardypaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="0485f-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="0485f-156">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="0485f-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="0485f-157">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0485f-158">**ATTR** – Ein Attribut:</span><span class="sxs-lookup"><span data-stu-id="0485f-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="0485f-159">Beleg</span><span class="sxs-lookup"><span data-stu-id="0485f-159">Voucher</span></span>
    -   <span data-ttu-id="0485f-160">**FD** - Die Anfangssaldoenfinanzdaten</span><span class="sxs-lookup"><span data-stu-id="0485f-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="0485f-161">**FD** - Finanzdaten, die nur Soll enthalten</span><span class="sxs-lookup"><span data-stu-id="0485f-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="0485f-162">**FD** - Finanzdaten, die nur Haben enthahlten</span><span class="sxs-lookup"><span data-stu-id="0485f-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="0485f-163">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="0485f-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="0485f-164">**CALC** – Der Abschlusssaldo</span><span class="sxs-lookup"><span data-stu-id="0485f-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="0485f-165">**Jährlich zusammengefasste Zwischenbilanz - Standard:**</span><span class="sxs-lookup"><span data-stu-id="0485f-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="0485f-166">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="0485f-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="0485f-167">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="0485f-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="0485f-168">**ATTR** – Ein Attribut</span><span class="sxs-lookup"><span data-stu-id="0485f-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="0485f-169">Beleg</span><span class="sxs-lookup"><span data-stu-id="0485f-169">Voucher</span></span>
    -   <span data-ttu-id="0485f-170">**FD** - Die Anfangssaldoenfinanzdaten für das aktuelle Jahr</span><span class="sxs-lookup"><span data-stu-id="0485f-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="0485f-171">**FD** - Finanzdaten, die nur Soll für das aktuelle Jahr enthahlten</span><span class="sxs-lookup"><span data-stu-id="0485f-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="0485f-172">**FD** - Finanzdaten, die nur haben für das aktuelle Jahr entahlten</span><span class="sxs-lookup"><span data-stu-id="0485f-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="0485f-173">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="0485f-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="0485f-174">**CALC** – Der Abschlusssaldo</span><span class="sxs-lookup"><span data-stu-id="0485f-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="0485f-175">**FD** - Finanzdaten, die nur Soll für das letzte Jahr enthahlten</span><span class="sxs-lookup"><span data-stu-id="0485f-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="0485f-176">**FD** - Finanzdaten, die nur Haben für das letzte Jahr enthalten</span><span class="sxs-lookup"><span data-stu-id="0485f-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="0485f-177">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0485f-177">Additional resources</span></span>
--------

[<span data-ttu-id="0485f-178">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="0485f-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="0485f-179">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="0485f-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="0485f-180">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="0485f-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



