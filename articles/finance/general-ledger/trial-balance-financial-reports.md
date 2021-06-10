---
title: Zwischenbilanzfinanzberichte
description: In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben. Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103657"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="ffd86-104">Zwischenbilanzfinanzberichte</span><span class="sxs-lookup"><span data-stu-id="ffd86-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffd86-105">In diesem Artikel werden die Standardberichte für Zwischenbilanzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ffd86-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="ffd86-106">Zudem werden die Bausteine beschrieben, die mit diesen Berichten zugeordnet werden und wie Sie Berichte ändern können, um diese an Ihre geschäftlichen Anforderungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="ffd86-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="ffd86-107">Standardzwischenbilanzberichte</span><span class="sxs-lookup"><span data-stu-id="ffd86-107">Default trial balance reports</span></span>

<span data-ttu-id="ffd86-108">Drei Zwischenbilanzberichte sind in der Finanzberichterstellung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ffd86-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="ffd86-109">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="ffd86-109">Default report</span></span>                                 | <span data-ttu-id="ffd86-110">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="ffd86-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd86-111">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="ffd86-112">Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="ffd86-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="ffd86-113">Zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="ffd86-114">Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.</span><span class="sxs-lookup"><span data-stu-id="ffd86-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="ffd86-115">Jährlich zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="ffd86-116">Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein.</span><span class="sxs-lookup"><span data-stu-id="ffd86-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="ffd86-117">Bausteine</span><span class="sxs-lookup"><span data-stu-id="ffd86-117">Building blocks</span></span>
<span data-ttu-id="ffd86-118">Die Zwischenbilanzfinanzberichte verwenden die folgenden Bausteine.</span><span class="sxs-lookup"><span data-stu-id="ffd86-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="ffd86-119">Standardbericht</span><span class="sxs-lookup"><span data-stu-id="ffd86-119">Default report</span></span>                                 | <span data-ttu-id="ffd86-120">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-120">Row definition</span></span>          | <span data-ttu-id="ffd86-121">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="ffd86-122">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="ffd86-123">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-123">Trial Balance - Default</span></span> | <span data-ttu-id="ffd86-124">Ausführliche Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="ffd86-125">Zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="ffd86-126">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-126">Trial Balance - Default</span></span> | <span data-ttu-id="ffd86-127">Zusammengefasste Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="ffd86-128">Jährlich zusammengefasste Zwischenbilanz – Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="ffd86-129">Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-129">Trial Balance - Default</span></span> | <span data-ttu-id="ffd86-130">Jährlich zusammengefasste Zwischenbilanz - Standard</span><span class="sxs-lookup"><span data-stu-id="ffd86-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="ffd86-131">Beim Ausführen der **Zwischenbilanz** in Financial Reporting aktivieren Sie unbedingt die Kontrollkästchen für **Zeilen ohne Beträge anzeigen** und **Berichte ohne aktive Zeilen anzeigen** auf der Registerkarte **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="ffd86-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="ffd86-132">Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-132">Row definition</span></span>

<span data-ttu-id="ffd86-133">Die Zeilendefinition, Zwischenbilanz – Standard, enthält eine einzelne Zeile, die alle Hauptkonten übernimmt.</span><span class="sxs-lookup"><span data-stu-id="ffd86-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="ffd86-134">Daher kann jeder Benutzer den Bericht erstellen, ohne Änderungen vorzunehmen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ffd86-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="ffd86-135">Wenn Sie den Bericht anzeigen, führen Sie einen Drilldown der Einzelzeile durch, um Details zu jedem Konto zu sehen.</span><span class="sxs-lookup"><span data-stu-id="ffd86-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="ffd86-136">Sie können die Zeilendefinition ändern, sodass sie weitere Details umfasst.</span><span class="sxs-lookup"><span data-stu-id="ffd86-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="ffd86-137">Um die Zeilendefinition "Zwischenbilanz - Standard" zu ändern, sodass sie Zeilen für alle Konten umfasst, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ffd86-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="ffd86-138">Klicken Sie auf **Bearbeiten** und dann auf **Zeilen aus Dimensionen einfügen**.</span><span class="sxs-lookup"><span data-stu-id="ffd86-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="ffd86-139">Mit dem Befehl **Zeilen aus Dimensionen einfügen** können Sie die Dimensionen auswählen, die Sie in Ihrer Zeile haben möchten.</span><span class="sxs-lookup"><span data-stu-id="ffd86-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="ffd86-140">Für diese Zeilendefinition werden Sie **Hauptkonto** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ffd86-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="ffd86-141">Stellen Sie sicher, dass das **Hauptkonto** alle kaufmännischen Und-Zeichen (&) enthält, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffd86-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="ffd86-142">Die Zeilendefinition enthält nun alle Hauptkonten für Ihres juristische Standardperson.</span><span class="sxs-lookup"><span data-stu-id="ffd86-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="ffd86-143">Spaltendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-143">Column definition</span></span>

<span data-ttu-id="ffd86-144">Jeder Zwischenbilanzbericht verwendet eine andere Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="ffd86-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="ffd86-145">Diese Spaltendefinitionen enthalten verschieden Spaltentypen, um verschiedene Stufen der Genauigkeit und der Finanzdaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ffd86-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="ffd86-146">**Ausführliche Zwischenbilanz - Standardypaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="ffd86-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="ffd86-147">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ffd86-148">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="ffd86-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="ffd86-149">**ATTR (3)** – Attribute:</span><span class="sxs-lookup"><span data-stu-id="ffd86-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="ffd86-150">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="ffd86-150">Transaction Date</span></span>
        -   <span data-ttu-id="ffd86-151">Beleg</span><span class="sxs-lookup"><span data-stu-id="ffd86-151">Voucher</span></span>
        -   <span data-ttu-id="ffd86-152">Erfassungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ffd86-152">Journal Description</span></span>
    -   <span data-ttu-id="ffd86-153">**FD** - Finanzdaten, die nur Soll enthalten</span><span class="sxs-lookup"><span data-stu-id="ffd86-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="ffd86-154">**FD** - Finanzdaten, die nur Haben enthahlten</span><span class="sxs-lookup"><span data-stu-id="ffd86-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="ffd86-155">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="ffd86-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="ffd86-156">**Zusammengefasste Zwischenbilanz - Standardypaltentypen:**</span><span class="sxs-lookup"><span data-stu-id="ffd86-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="ffd86-157">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="ffd86-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="ffd86-158">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ffd86-159">**ATTR** – Ein Attribut:</span><span class="sxs-lookup"><span data-stu-id="ffd86-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="ffd86-160">Beleg</span><span class="sxs-lookup"><span data-stu-id="ffd86-160">Voucher</span></span>
    -   <span data-ttu-id="ffd86-161">**FD** - Die Anfangssaldoenfinanzdaten</span><span class="sxs-lookup"><span data-stu-id="ffd86-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="ffd86-162">**FD** - Finanzdaten, die nur Soll enthalten</span><span class="sxs-lookup"><span data-stu-id="ffd86-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="ffd86-163">**FD** - Finanzdaten, die nur Haben enthahlten</span><span class="sxs-lookup"><span data-stu-id="ffd86-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="ffd86-164">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="ffd86-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="ffd86-165">**CALC** – Der Abschlusssaldo</span><span class="sxs-lookup"><span data-stu-id="ffd86-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="ffd86-166">**Jährlich zusammengefasste Zwischenbilanz - Standard:**</span><span class="sxs-lookup"><span data-stu-id="ffd86-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="ffd86-167">**ACCT** - Kontocodes</span><span class="sxs-lookup"><span data-stu-id="ffd86-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="ffd86-168">**DESC** - Die Beschreibung der Zeilendefinition</span><span class="sxs-lookup"><span data-stu-id="ffd86-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ffd86-169">**ATTR** – Ein Attribut</span><span class="sxs-lookup"><span data-stu-id="ffd86-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="ffd86-170">Beleg</span><span class="sxs-lookup"><span data-stu-id="ffd86-170">Voucher</span></span>
    -   <span data-ttu-id="ffd86-171">**FD** - Die Anfangssaldoenfinanzdaten für das aktuelle Jahr</span><span class="sxs-lookup"><span data-stu-id="ffd86-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="ffd86-172">**FD** - Finanzdaten, die nur Soll für das aktuelle Jahr enthahlten</span><span class="sxs-lookup"><span data-stu-id="ffd86-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="ffd86-173">**FD** - Finanzdaten, die nur haben für das aktuelle Jahr entahlten</span><span class="sxs-lookup"><span data-stu-id="ffd86-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="ffd86-174">**CALC** – Die Nettodifferenz</span><span class="sxs-lookup"><span data-stu-id="ffd86-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="ffd86-175">**CALC** – Der Abschlusssaldo</span><span class="sxs-lookup"><span data-stu-id="ffd86-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="ffd86-176">**FD** - Finanzdaten, die nur Soll für das letzte Jahr enthahlten</span><span class="sxs-lookup"><span data-stu-id="ffd86-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="ffd86-177">**FD** - Finanzdaten, die nur Haben für das letzte Jahr enthalten</span><span class="sxs-lookup"><span data-stu-id="ffd86-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffd86-178">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ffd86-178">Additional resources</span></span>

[<span data-ttu-id="ffd86-179">Finanzberichterstellung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="ffd86-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="ffd86-180">Finanzberichte anzeigen</span><span class="sxs-lookup"><span data-stu-id="ffd86-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="ffd86-181">Dynamics Financial Reporting-Blog</span><span class="sxs-lookup"><span data-stu-id="ffd86-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
