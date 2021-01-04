---
title: Finanzberichterstellung
description: Die Finanzberichterstellung ermöglicht Finanz- und Geschäftsexperten Finanzaufstellungen zu erstellen, zu verwalten, bereitzustellen und anzuzeigen. Es bewegt sich über die traditionellen Berichtseinschränkungen hinaus, um effizient verschiedene Arten von Berichten zu entwerfen.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7da0d1aa4bb10658c66fce996e00b5714125f100
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682695"
---
# <a name="financial-reporting"></a><span data-ttu-id="83b61-104">Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="83b61-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83b61-105">Die Finanzberichterstellung für die Anwendung ermöglicht Finanz- und Geschäftsexperten Finanzaufstellungen zu erstellen, verwalten, bereitzustellen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83b61-105">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="83b61-106">Es bewegt sich über die traditionellen Berichtseinschränkungen hinaus, um effizient verschiedene Arten von Berichten zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="83b61-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="83b61-107">Die Finanzberichterstellung umfasst Dimensionsunterstützung.</span><span class="sxs-lookup"><span data-stu-id="83b61-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="83b61-108">Daher sind Kontosegmente oder Dimensionen sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="83b61-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="83b61-109">Es sind keine zusätzlichen Tools oder Konfigurationsschritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83b61-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="83b61-110">Finanzberichterstellungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="83b61-110">Financial reporting setup</span></span>
<span data-ttu-id="83b61-111">Die Seite **Rechnungslegungseinstellung** enthält eine Liste aller Finanzdimensionen im System.</span><span class="sxs-lookup"><span data-stu-id="83b61-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="83b61-112">**Hauptbuch**\>**Sachkontoeinstellung**\>**Rechnungslegungseinstellung**.</span><span class="sxs-lookup"><span data-stu-id="83b61-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="83b61-113">Die Seite **Rechnungslegungseinstellung** enthält zwei Abschnitte, die die Daten bestimmen, die Sie in der Finanzberichterstellung melden:</span><span class="sxs-lookup"><span data-stu-id="83b61-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="83b61-114">**Dimensionsregisterkarte** - Weil verschiedene Unternehmen verschiedene Dimensionen und Kontostrukturen verwenden, besteht keine Möglichkeit, den Auftrag zu bestimmen, in dem Benutzer alle enthaltenen Finanzdimensionen auf Berichten angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83b61-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="83b61-115">Mit dieser Seite können Sie den Auftrag festlegen, in dem Sie Finanzdimensionen anzeigen möchten, wenn Sie einen Bericht in der Finanzberichterstellung erstellen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="83b61-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="83b61-116">**Attributregisterkarte**, in dem Sie auswählen können, ob die Fähigkeit wünschen, **Kreditoren** und **Debitoren** als Attribut für das Filtern und Erstellen von Berichten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="83b61-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="83b61-117">Das Erstellen einer Fertigmeldung in "Kreditoren" und in " Debitoren ist nur wertvoll, wenn Sie nicht mehrere Kreditoren oder Debitoren in einem einzelnen Dokument eingeben, wenn Sie Posten buchen.</span><span class="sxs-lookup"><span data-stu-id="83b61-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="83b61-118">Kreditor und/oder Debitors werden zusätzliche Zeit der Integration hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="83b61-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="83b61-119">Finanzberichterstellungskomponenten</span><span class="sxs-lookup"><span data-stu-id="83b61-119">Financial reporting components</span></span>
<span data-ttu-id="83b61-120">Die folgenden Komponenten der Finanzberichterstellung erleichtern das Erstellen, Anzeigen und Planen von Berichten.</span><span class="sxs-lookup"><span data-stu-id="83b61-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="83b61-121">Komponente</span><span class="sxs-lookup"><span data-stu-id="83b61-121">Component</span></span>        | <span data-ttu-id="83b61-122">Funktionen</span><span class="sxs-lookup"><span data-stu-id="83b61-122">Functions</span></span> | <span data-ttu-id="83b61-123">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="83b61-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="83b61-124">Berichts-Designer</span><span class="sxs-lookup"><span data-stu-id="83b61-124">Report Designer</span></span>  | <span data-ttu-id="83b61-125">Erstellen Sie Berichtsbausteine, die kombiniert werden können, um einen Bericht zu definieren und zu generieren.</span><span class="sxs-lookup"><span data-stu-id="83b61-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="83b61-126">Der Berichts-Assistent führt weniger erfahrene Benutzer durch den Designprozess.</span><span class="sxs-lookup"><span data-stu-id="83b61-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="83b61-127">Erfahrene Benutzer können neue Berichtsbausteine erstellen oder vorhandene Bausteine den Anforderungen entsprechend ändern.</span><span class="sxs-lookup"><span data-stu-id="83b61-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="83b61-128">Berichtszeitpläne</span><span class="sxs-lookup"><span data-stu-id="83b61-128">Report schedules</span></span> | <span data-ttu-id="83b61-129">Planen Sie einen einzelnen Bericht oder eine Gruppe von Berichten so, dass sie regelmäßig generiert werden.</span><span class="sxs-lookup"><span data-stu-id="83b61-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="83b61-130">Finanzberichte generieren</span><span class="sxs-lookup"><span data-stu-id="83b61-130">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="83b61-131">Funktionen</span><span class="sxs-lookup"><span data-stu-id="83b61-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="83b61-132">Funktion</span><span class="sxs-lookup"><span data-stu-id="83b61-132">Feature</span></span></th>
<th><span data-ttu-id="83b61-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83b61-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83b61-134">Berichtsdesignflexibilität</span><span class="sxs-lookup"><span data-stu-id="83b61-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="83b61-135">Der Berichts-Designer stellt folgende Berichtsoptionen bereit, wenn Sie einen Bericht entwerfen:</span><span class="sxs-lookup"><span data-stu-id="83b61-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="83b61-136">Speichern Sie Dimensionskombinationen, und verwenden Sie die Dimensionen für weitere Berichte erneut.</span><span class="sxs-lookup"><span data-stu-id="83b61-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="83b61-137">Steuern Sie, wie Dimensionsbeschreibungen formatiert und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="83b61-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="83b61-138">Erkennen Sie Konten oder Dimensionen, die in den Berichtsbausteinen ausgelassen wurden.</span><span class="sxs-lookup"><span data-stu-id="83b61-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="83b61-139">Überschriften für rollende Prognosen formatieren.</span><span class="sxs-lookup"><span data-stu-id="83b61-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="83b61-140">Zusammenarbeit an Finanzberichten</span><span class="sxs-lookup"><span data-stu-id="83b61-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="83b61-141">Die folgenden Funktionen helfen Ihnen, die Generierung und Verteilung von Berichten zu vereinfachen:</span><span class="sxs-lookup"><span data-stu-id="83b61-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="83b61-142">Planen Sie Berichte, sodass sie täglich, wöchentlich, monatlich oder jährlich automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="83b61-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="83b61-143">Exportieren Sie ins schreibgeschützte XPS-Format, das eine bessere Dokumentensicherheit durch digitale Signaturen bietet.</span><span class="sxs-lookup"><span data-stu-id="83b61-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="83b61-144">Exportieren Sie in ein Microsoft Excel-Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="83b61-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="83b61-145">Um Berichte freizugeben, können Sie E-Mails erstellen, die Links auf die Berichte enthalten.</span><span class="sxs-lookup"><span data-stu-id="83b61-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="83b61-146">Interaktive Berichtsanzeige</span><span class="sxs-lookup"><span data-stu-id="83b61-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="83b61-147">Mit interaktiven Funktionen können Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="83b61-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="83b61-148">Ändern Sie das Berichtsdatum des Berichts, den Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="83b61-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="83b61-149">Ändern Sie die Währung des Berichts, den Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="83b61-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="83b61-150">Zeigen Sie den Berichts in einer Übersichts- oder detaillierten Ansicht an.</span><span class="sxs-lookup"><span data-stu-id="83b61-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="83b61-151">Fügen Sie Dimensionsfilter hinzu, um Berichtsinhalte auf eine bestimmte Dimension oder eine Kombination aus Dimensionen zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="83b61-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="83b61-152">Fügen Sie Attributfilter hinzu, um Berichtsinhalte auf ein bestimmtes Attribut oder eine Kombination aus Attributen zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="83b61-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="83b61-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83b61-153">Additional resources</span></span>
[<span data-ttu-id="83b61-154">Finanzberichte generieren</span><span class="sxs-lookup"><span data-stu-id="83b61-154">Generate financial reports</span></span>](generate-financial-report.md)
