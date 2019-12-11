---
title: Generieren von Onlinekanalberichten
description: In diesem Thema wird beschrieben, wie Sie Berichte für Ihren Online-Kanal in Microsoft Dynamics 365 Retail generieren.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698049"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="549a9-103">Generieren von Onlinekanalberichten</span><span class="sxs-lookup"><span data-stu-id="549a9-103">Generate online channel reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="549a9-104">In diesem Thema wird beschrieben, wie Sie Berichte für Ihren Online-Kanal in Microsoft Dynamics 365 Retail generieren.</span><span class="sxs-lookup"><span data-stu-id="549a9-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="549a9-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="549a9-105">Overview</span></span>

<span data-ttu-id="549a9-106">Sie können in Retail mehrere Berichte erstellen und anzeigen, um die Leistung Ihres Online-Kanals zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="549a9-106">You can generate and view several reports in Retail to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="549a9-107">Bericht 'Kanalzusammenfassung'</span><span class="sxs-lookup"><span data-stu-id="549a9-107">Channel summary report</span></span>

<span data-ttu-id="549a9-108">Der Bericht **Kanalzusammenfassung** zeigt eine Zusammenfassung der folgenden Transaktionen für den ausgewählten Kanal an:</span><span class="sxs-lookup"><span data-stu-id="549a9-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="549a9-109">Verkaufstransaktionen</span><span class="sxs-lookup"><span data-stu-id="549a9-109">Sales transactions</span></span>
- <span data-ttu-id="549a9-110">Zahlungsbuchungen</span><span class="sxs-lookup"><span data-stu-id="549a9-110">Payment transactions</span></span>
- <span data-ttu-id="549a9-111">Steuerbuchungen</span><span class="sxs-lookup"><span data-stu-id="549a9-111">Tax transactions</span></span>
- <span data-ttu-id="549a9-112">Rabatttransaktionen</span><span class="sxs-lookup"><span data-stu-id="549a9-112">Discounted transactions</span></span>

<span data-ttu-id="549a9-113">Befolgen Sie diese Schritte, um den Bericht **Kanalzusammenfassung** zu generieren.</span><span class="sxs-lookup"><span data-stu-id="549a9-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-114">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Kanalzusammenfassung**.</span><span class="sxs-lookup"><span data-stu-id="549a9-114">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="549a9-115">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-116">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-117">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-118">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="549a9-119">Bericht 'Kanal Umsatz nach Jahr'</span><span class="sxs-lookup"><span data-stu-id="549a9-119">Channel sales by year report</span></span> 

<span data-ttu-id="549a9-120">Der Bericht **Kanal Umsatz nach Jahr** zeigt einen Vergleich der Verkäufe im Jahresvergleich für ein bestimmtes Geschäft.</span><span class="sxs-lookup"><span data-stu-id="549a9-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="549a9-121">Sie wählen das Jahr aus, mit dem der Umsatz verglichen werden soll, und der Bericht vergleicht den Umsatz des ausgewählten Jahres mit dem Umsatz des Vorjahres.</span><span class="sxs-lookup"><span data-stu-id="549a9-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="549a9-122">Befolgen Sie diese Schritte, um den Bericht **Kanal Umsatz nach Jahr** zu generieren.</span><span class="sxs-lookup"><span data-stu-id="549a9-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-123">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Kanal Umsatz pro Jahr**.</span><span class="sxs-lookup"><span data-stu-id="549a9-123">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="549a9-124">Geben Sie im Feld **Von Kalenderjahr** ein Jahr ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="549a9-125">Geben Sie im Feld **Bis Kalenderjahr** ein Jahr ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="549a9-126">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-127">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="549a9-128">Bericht 'Kanal Umsatz nach Stunde'</span><span class="sxs-lookup"><span data-stu-id="549a9-128">Channel sales by hour report</span></span>

<span data-ttu-id="549a9-129">Der Bericht **Kanal Umsatz nach Stunde** zeigt die Verkaufskennzahlen pro Stunde für einen ausgewählten Kanal oder eine ausgewählte Organisationseinheit an.</span><span class="sxs-lookup"><span data-stu-id="549a9-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="549a9-130">Befolgen Sie diese Schritte, um den Bericht **Kanal Umsatz nach Stunde** zu generieren.</span><span class="sxs-lookup"><span data-stu-id="549a9-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-131">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Kanal Umsatz nach Stunde**.</span><span class="sxs-lookup"><span data-stu-id="549a9-131">Go to **Retail \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="549a9-132">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-133">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-134">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-135">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="549a9-136">Bericht 'Wichtigste Debitoren'</span><span class="sxs-lookup"><span data-stu-id="549a9-136">Top customers report</span></span>

<span data-ttu-id="549a9-137">Der Bericht **Wichtigste Debitoren** zeigt die Verkaufsmetriken für die wichtigsten *N*-Kunden für einen ausgewählten Kanal oder eine Organisationseinheit an.</span><span class="sxs-lookup"><span data-stu-id="549a9-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="549a9-138">Der Wert *N* ist eine Zahl zwischen 10 und 100 und basiert auf einer benutzerdefinierten aggregierten Kennzahl.</span><span class="sxs-lookup"><span data-stu-id="549a9-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="549a9-139">Befolgen Sie diese Schritte, um den Bericht **Wichtigste Debitoren** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="549a9-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-140">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Wichtigste Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="549a9-140">Go to **Retail \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="549a9-141">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-142">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-143">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-144">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="549a9-145">Bericht über höchste Rabatte</span><span class="sxs-lookup"><span data-stu-id="549a9-145">Top discounts report</span></span>

<span data-ttu-id="549a9-146">Der Bericht **Höchste Rabatte** zeigt die Verkaufsmetriken für die wichtigsten *N*-Rabatte für einen ausgewählten Kanal oder eine Organisationseinheit an.</span><span class="sxs-lookup"><span data-stu-id="549a9-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="549a9-147">Der Wert *N* ist eine Zahl zwischen 10 und 100 und basiert auf einer benutzerdefinierten aggregierten Kennzahl.</span><span class="sxs-lookup"><span data-stu-id="549a9-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="549a9-148">Befolgen Sie diese Schritte, um den Bericht **Höchste Rabatte** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="549a9-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-149">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Höchste Rabatte**.</span><span class="sxs-lookup"><span data-stu-id="549a9-149">Go to **Retail \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="549a9-150">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-151">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-152">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-153">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="549a9-154">Bericht über Top-Produkte</span><span class="sxs-lookup"><span data-stu-id="549a9-154">Top products report</span></span>

<span data-ttu-id="549a9-155">Der Bericht **Top-Produkte** zeigt die Verkaufsmetriken für die wichtigsten *N*-Produkte für einen ausgewählten Kanal oder eine Organisationseinheit an.</span><span class="sxs-lookup"><span data-stu-id="549a9-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="549a9-156">Der Wert *N* ist eine Zahl zwischen 10 und 100 und basiert auf einer benutzerdefinierten aggregierten Kennzahl.</span><span class="sxs-lookup"><span data-stu-id="549a9-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="549a9-157">Befolgen Sie diese Schritte, um den Bericht **Top-Produkte** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="549a9-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-158">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Bericht Top-Produkte**.</span><span class="sxs-lookup"><span data-stu-id="549a9-158">Go to **Retail \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="549a9-159">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-160">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-161">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-162">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="549a9-163">Bericht 'Kategorie Verkäufe'</span><span class="sxs-lookup"><span data-stu-id="549a9-163">Category sales report</span></span>

<span data-ttu-id="549a9-164">Der Bericht **Kategorie Verkäufe** zeigt Verkaufsmetriken für einen ausgewählten Zeitraum für jeden Knoten einer Kategoriehierarchie für einen ausgewählten Kanal oder eine ausgewählte Bedieneinheit an.</span><span class="sxs-lookup"><span data-stu-id="549a9-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="549a9-165">Befolgen Sie diese Schritte, um den Bericht **Kategorie Verkäufe** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="549a9-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-166">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Berichte Kategorie Verkäufe**.</span><span class="sxs-lookup"><span data-stu-id="549a9-166">Go to **Retail \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="549a9-167">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-168">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-169">Wählen Sie im Feld **Kanal** den Online-Kanal aus.</span><span class="sxs-lookup"><span data-stu-id="549a9-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="549a9-170">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="549a9-171">Bericht 'Organisationsverkäufe'</span><span class="sxs-lookup"><span data-stu-id="549a9-171">Organization sales report</span></span>

<span data-ttu-id="549a9-172">Der Bericht **Organisationsverkäufe** zeigt die Leistung Ihrer Einzelhandelsgeschäfte nach Organisationseinheiten an.</span><span class="sxs-lookup"><span data-stu-id="549a9-172">The **Organization sales** report shows the performance of your retail stores by organization unit.</span></span> <span data-ttu-id="549a9-173">Dieser Bericht enthält die Verkaufsmenge und den Betrag nach Filiale sowie die Gewinnspanne für jede Filiale.</span><span class="sxs-lookup"><span data-stu-id="549a9-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="549a9-174">Die Organisationseinheit basiert auf der Standardberichterstattungshierarchie.</span><span class="sxs-lookup"><span data-stu-id="549a9-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="549a9-175">Befolgen Sie diese Schritte, um den Bericht **Organisationsverkäufe** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="549a9-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="549a9-176">Navigieren Sie zu **Retail \> Abfragen und Berichte \> Umsatzberichte \> Berichte Organisationsverkäufe**.</span><span class="sxs-lookup"><span data-stu-id="549a9-176">Go to **Retail \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="549a9-177">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-178">Geben Sie im Feld **Bis Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="549a9-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="549a9-179">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="549a9-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="549a9-180">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="549a9-180">Additional resources</span></span>

- [<span data-ttu-id="549a9-181">Hilferessourcen für Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="549a9-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
