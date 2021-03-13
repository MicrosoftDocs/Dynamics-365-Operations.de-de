---
title: Berichtsdefinitionen im Finanzberichtdesigner
description: Dieser Artikel enthält Informationen zu Berichtsdefinitionen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7d5531112cfb803912849af3af785b2a69a79f3d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093413"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="36295-103">Berichtsdefinitionen im Finanzberichtdesigner</span><span class="sxs-lookup"><span data-stu-id="36295-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36295-104">Dieser Artikel enthält Informationen zu Berichtsdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="36295-104">This article provides information about report definitions.</span></span> <span data-ttu-id="36295-105">Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="36295-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="36295-106">Eine Berichtsdefinition enthält auch Optionen und Einstellungen zum Anpassen eines Berichts.</span><span class="sxs-lookup"><span data-stu-id="36295-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="36295-107">Eine Berichtsdefinition ist eine Berichtskomponente (oder Baustein), die eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtstruktur-Definition verwendet, um den Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="36295-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="36295-108">Zusätzlich bietet die Berichtsdefinition Optionen und Einstellungen zum Anpassen von Berichten.</span><span class="sxs-lookup"><span data-stu-id="36295-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="36295-109">Nachdem Sie Zeilen- und Spaltendefinitionen festgelegt haben, müssen Sie diese zu einer Berichtsdefinition kombinieren.</span><span class="sxs-lookup"><span data-stu-id="36295-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="36295-110">An diesem Punkt definieren Sie auch andere Aspekte der Definitionen wie die Detailebene und das Berichtsdatum.</span><span class="sxs-lookup"><span data-stu-id="36295-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="36295-111">Sie können einen Bericht dann speichern und generieren.</span><span class="sxs-lookup"><span data-stu-id="36295-111">You can then save and generate a report.</span></span> <span data-ttu-id="36295-112">Die Finanzberichterstellung bietet die folgenden Detailebenen an:</span><span class="sxs-lookup"><span data-stu-id="36295-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="36295-113">Wertmäßig</span><span class="sxs-lookup"><span data-stu-id="36295-113">Financial</span></span>
- <span data-ttu-id="36295-114">Finanzen und Konto</span><span class="sxs-lookup"><span data-stu-id="36295-114">Financial and Account</span></span>
- <span data-ttu-id="36295-115">Finanzen, Konto und Transaktion</span><span class="sxs-lookup"><span data-stu-id="36295-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="36295-116">Abhängig von den im Microsoft Dynamics ERP-System gespeicherten Daten sind in Berichten ggf. keine Transaktionsdetails verfügbar.</span><span class="sxs-lookup"><span data-stu-id="36295-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="36295-117">Erstellen einer Berichtsdefinition</span><span class="sxs-lookup"><span data-stu-id="36295-117">Create a report definition</span></span>
1. <span data-ttu-id="36295-118">Wählen Sie im Berichts-Designer im Menü **Datei** **Neu** und dann **Berichtsdefinition**.</span><span class="sxs-lookup"><span data-stu-id="36295-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="36295-119">Geben Sie die entsprechenden Informationen auf den Registerkarten **Bericht**, **Ausgabe und Verteilung**, **Kopf- und Fußzeilen** und **Einstellungen** an.</span><span class="sxs-lookup"><span data-stu-id="36295-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="36295-120">Inhalt einer Berichtsdefinition</span><span class="sxs-lookup"><span data-stu-id="36295-120">Contents of a report definition</span></span>
<span data-ttu-id="36295-121">In der folgenden Tabelle werden die Registerkarten in einer Berichtsdefinition und die Verwendung der Informationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36295-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="36295-122">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="36295-122">Tab</span></span></th>
<th><span data-ttu-id="36295-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36295-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="36295-124">Bericht</span><span class="sxs-lookup"><span data-stu-id="36295-124">Report</span></span></td>
<td><span data-ttu-id="36295-125">Hier können Sie einen Bericht erstellen, einen neuen Bericht konfigurieren oder einen vorhandenen Bericht ändern.</span><span class="sxs-lookup"><span data-stu-id="36295-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="36295-126">Ausgabe und Verteilung</span><span class="sxs-lookup"><span data-stu-id="36295-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="36295-127">Auf dieser Registerkarte können Berichtsausgabetyp und Berichtsausgabeziel geändert werden.</span><span class="sxs-lookup"><span data-stu-id="36295-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="36295-128">Kopf- und Fußzeilen</span><span class="sxs-lookup"><span data-stu-id="36295-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="36295-129">Auf dieser Registerkarte können die Kopf- und Fußzeilen des Berichts definiert und formatiert werden.</span><span class="sxs-lookup"><span data-stu-id="36295-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="36295-130">So können Sie Text oder Bilder zur Kopf- oder der Fußzeile hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="36295-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="36295-131">Die Finanzberichterstellung unterstützt BMP-, JPG- und .png-Dateien für Bilder.</span><span class="sxs-lookup"><span data-stu-id="36295-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="36295-132">Sie können auch Autotext-Codes hinzufügen, um weitere Informationen wie einen Unternehmensnamen, Berichtsnamen oder eine Seitenzahl einzufügen.</span><span class="sxs-lookup"><span data-stu-id="36295-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="36295-133">Einstellungen</span><span class="sxs-lookup"><span data-stu-id="36295-133">Settings</span></span></td>
<td><span data-ttu-id="36295-134">Geben Sie Berichtsdefinitionseinstellungen, wie die folgenden Einstellungen, an:</span><span class="sxs-lookup"><span data-stu-id="36295-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="36295-135">Formatieren und Runden von Beträgen</span><span class="sxs-lookup"><span data-stu-id="36295-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="36295-136">Formatieren von Detailberichten</span><span class="sxs-lookup"><span data-stu-id="36295-136">Format detail reports</span></span></li>
<li><span data-ttu-id="36295-137">Formatieren von Berichtsbaumstrukturen</span><span class="sxs-lookup"><span data-stu-id="36295-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="36295-138">Generieren eines Ausnahmeberichts</span><span class="sxs-lookup"><span data-stu-id="36295-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="36295-139">Angeben der Währungskonvertierung</span><span class="sxs-lookup"><span data-stu-id="36295-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="36295-140">Teilergebnisse und das Filtern von Kontodetails</span><span class="sxs-lookup"><span data-stu-id="36295-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="36295-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="36295-141">Additional resources</span></span>

[<span data-ttu-id="36295-142">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="36295-142">Financial reporting</span></span>](financial-reporting-intro.md)
