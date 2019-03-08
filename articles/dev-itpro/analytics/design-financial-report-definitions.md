---
title: Berichtsdefinitionen im Finanzberichtdesigner
description: Dieser Artikel enthält Informationen zu Berichtsdefinitionen. Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen. Eine Berichtsdefinition enthält auch Optionen und Einstellungen zum Anpassen eines Berichts.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 322f1cca32053224e1cd6dbaf29c098b983b5e1f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "327342"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="889f5-105">Berichtsdefinitionen im Finanzberichtdesigner</span><span class="sxs-lookup"><span data-stu-id="889f5-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="889f5-106">Dieser Artikel enthält Informationen zu Berichtsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="889f5-106">This article provides information about report definitions.</span></span> <span data-ttu-id="889f5-107">Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="889f5-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="889f5-108">Eine Berichtsdefinition enthält auch Optionen und Einstellungen zum Anpassen eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="889f5-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="889f5-109">Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="889f5-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="889f5-110">Zusätzlich bietet die Berichtsdefinition Optionen und Einstellungen zum Anpassen von Berichten.</span><span class="sxs-lookup"><span data-stu-id="889f5-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="889f5-111">Nachdem Sie Zeilen- und Spaltendefinitionen festgelegt haben, müssen Sie diese zu einer Berichtsdefinition kombinieren.</span><span class="sxs-lookup"><span data-stu-id="889f5-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="889f5-112">An diesem Punkt definieren Sie auch andere Aspekte der Definitionen wie die Detailebene und das Berichtsdatum.</span><span class="sxs-lookup"><span data-stu-id="889f5-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="889f5-113">Sie können einen Bericht dann speichern und generieren.</span><span class="sxs-lookup"><span data-stu-id="889f5-113">You can then save and generate a report.</span></span> <span data-ttu-id="889f5-114">Die Finanzberichterstellung bietet die folgenden Detailebenen an:</span><span class="sxs-lookup"><span data-stu-id="889f5-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="889f5-115">Wertmäßig</span><span class="sxs-lookup"><span data-stu-id="889f5-115">Financial</span></span>
- <span data-ttu-id="889f5-116">Finanzen und Konto</span><span class="sxs-lookup"><span data-stu-id="889f5-116">Financial and Account</span></span>
- <span data-ttu-id="889f5-117">Finanzen, Konto und Transaktion</span><span class="sxs-lookup"><span data-stu-id="889f5-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="889f5-118">Abhängig von den im Microsoft Dynamics ERP-System gespeicherten Daten sind in Berichten ggf. keine Transaktionsdetails verfügbar.</span><span class="sxs-lookup"><span data-stu-id="889f5-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="889f5-119">Erstellen einer Berichtsdefinition</span><span class="sxs-lookup"><span data-stu-id="889f5-119">Create a report definition</span></span>
1. <span data-ttu-id="889f5-120">Wählen Sie im Berichts-Designer im Menü **Datei** **Neu** und dann **Berichtsdefinition**.</span><span class="sxs-lookup"><span data-stu-id="889f5-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="889f5-121">Geben Sie die entsprechenden Informationen auf den Registerkarten **Bericht**, **Ausgabe und Verteilung**, **Kopf- und Fußzeilen** und **Einstellungen** an.</span><span class="sxs-lookup"><span data-stu-id="889f5-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="889f5-122">Inhalt einer Berichtsdefinition</span><span class="sxs-lookup"><span data-stu-id="889f5-122">Contents of a report definition</span></span>
<span data-ttu-id="889f5-123">In der folgenden Tabelle werden die Registerkarten in einer Berichtsdefinition und die Verwendung der Informationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="889f5-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="889f5-124">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="889f5-124">Tab</span></span></th>
<th><span data-ttu-id="889f5-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="889f5-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="889f5-126">Bericht</span><span class="sxs-lookup"><span data-stu-id="889f5-126">Report</span></span></td>
<td><span data-ttu-id="889f5-127">Hier können Sie einen Bericht erstellen, einen neuen Bericht konfigurieren oder einen vorhandenen Bericht ändern.</span><span class="sxs-lookup"><span data-stu-id="889f5-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="889f5-128">Ausgabe und Verteilung</span><span class="sxs-lookup"><span data-stu-id="889f5-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="889f5-129">Auf dieser Registerkarte können Berichtsausgabetyp und Berichtsausgabeziel geändert werden.</span><span class="sxs-lookup"><span data-stu-id="889f5-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="889f5-130">Kopf- und Fußzeilen</span><span class="sxs-lookup"><span data-stu-id="889f5-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="889f5-131">Auf dieser Registerkarte können die Kopf- und Fußzeilen des Berichts definiert und formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="889f5-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="889f5-132">So können Sie Text oder Bilder zur Kopf- oder der Fußzeile hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="889f5-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="889f5-133">Die Finanzberichterstellung unterstützt BMP-, JPG- und .png-Dateien für Bilder.</span><span class="sxs-lookup"><span data-stu-id="889f5-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="889f5-134">Sie können auch Autotext-Codes hinzufügen, um weitere Informationen wie einen Unternehmensnamen, Berichtsnamen oder eine Seitenzahl einzufügen.</span><span class="sxs-lookup"><span data-stu-id="889f5-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="889f5-135">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="889f5-135">Settings</span></span></td>
<td><span data-ttu-id="889f5-136">Geben Sie Berichtsdefinitionseinstellungen, wie die folgenden Einstellungen, an:</span><span class="sxs-lookup"><span data-stu-id="889f5-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="889f5-137">Formatieren und Runden von Beträgen</span><span class="sxs-lookup"><span data-stu-id="889f5-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="889f5-138">Formatieren von Detailberichten</span><span class="sxs-lookup"><span data-stu-id="889f5-138">Format detail reports</span></span></li>
<li><span data-ttu-id="889f5-139">Formatieren von Berichtsbaumstrukturen</span><span class="sxs-lookup"><span data-stu-id="889f5-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="889f5-140">Generieren eines Ausnahmeberichts</span><span class="sxs-lookup"><span data-stu-id="889f5-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="889f5-141">Angeben der Währungskonvertierung</span><span class="sxs-lookup"><span data-stu-id="889f5-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="889f5-142">Teilergebnisse und das Filtern von Kontodetails</span><span class="sxs-lookup"><span data-stu-id="889f5-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="889f5-143">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="889f5-143">Additional resources</span></span>

[<span data-ttu-id="889f5-144">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="889f5-144">Financial reporting</span></span>](financial-reporting-intro.md)
