---
title: Dashboard für die Nutzungsverwaltung
description: In diesem Thema wird erläutert, wie Sie das Dashboard für die Nutzungsverwaltung verwenden, um die Nutzung des Dienstes für die elektronische Rechnungsstellung zu überwachen und konform zu bleiben.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130505"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="22681-103">Dashboard für die Nutzungsverwaltung</span><span class="sxs-lookup"><span data-stu-id="22681-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22681-104">Das Dashboard für die **Nutzungsverwaltung** hilft Ihnen bei der Überwachung der Nutzung des elektronischen Rechnungsstellungsdienstes und hilft somit Ihrem Unternehmen, die monatlichen Nutzungsbedingungen einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="22681-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="22681-105">Die Compliance wird durch die Berechnung des Einreichungsvolumens und den Vergleich mit dem erfassten Einreichungsvolumen festgestellt, um Abweichungen zwischen dem erfassten Volumen und dem verbrauchten Volumen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="22681-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="22681-106">Das Dashboard enthält die folgenden Indikatoren:</span><span class="sxs-lookup"><span data-stu-id="22681-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="22681-107">Ein Kostenindikator, den Sie verwenden können, um den Verbrauch für Lizenzierungs-Compliance-Zwecke zu überwachen:</span><span class="sxs-lookup"><span data-stu-id="22681-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="22681-108">Verbrauch pro Monat (Export)</span><span class="sxs-lookup"><span data-stu-id="22681-108">Usage per month (export)</span></span>

- <span data-ttu-id="22681-109">Drei Betriebsindikatoren, die Sie verwenden können, um die Nutzung des elektronischen Rechnungsstellungsdienstes für Verwaltungszwecke zu verfolgen:</span><span class="sxs-lookup"><span data-stu-id="22681-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="22681-110">Verbrauch nach Funktion</span><span class="sxs-lookup"><span data-stu-id="22681-110">Usage by feature</span></span>
    - <span data-ttu-id="22681-111">Verbrauch nach Umgebung</span><span class="sxs-lookup"><span data-stu-id="22681-111">Usage by environment</span></span>
    - <span data-ttu-id="22681-112">Verbrauch pro Monat (Import)</span><span class="sxs-lookup"><span data-stu-id="22681-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="22681-113">Messbereich</span><span class="sxs-lookup"><span data-stu-id="22681-113">Measurement scope</span></span>

- <span data-ttu-id="22681-114">Maßeinheit:</span><span class="sxs-lookup"><span data-stu-id="22681-114">Unit of measure:</span></span> 

    <span data-ttu-id="22681-115">Das **Nutzungsverwaltung**-Dashboard zählt die Einreichung von Geschäftsdokumenten und importierten elektronischen Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="22681-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="22681-116">Organisation:</span><span class="sxs-lookup"><span data-stu-id="22681-116">Organization:</span></span> 

    <span data-ttu-id="22681-117">Die Zählung wird nach der Mandanten-ID Ihrer Organisation zusammengefasst, unabhängig von der Anzahl der Instanzen von Microsoft Dynamics 365 Finance oder Dynamics 365 Supply Chain Management, oder die Anzahl der juristischen Personen, für die der Dienst für die elektronische Rechnungsstellung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="22681-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="22681-118">Indikator: Verbrauch pro Monat (Export)</span><span class="sxs-lookup"><span data-stu-id="22681-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="22681-119">Dieses Kennzeichen liefert Details zu den elektronischen Rechnungen, die Ihre Organisation während eines definierten Zeitraums ausstellt.</span><span class="sxs-lookup"><span data-stu-id="22681-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="22681-120">Bereich</span><span class="sxs-lookup"><span data-stu-id="22681-120">Scope</span></span>
- <span data-ttu-id="22681-121">Die Anzahl der Geschäftsdokumente, die von Finance and Supply Chain Management an den Dienst für die elektronische Rechnungsstellung gesendet werden, unabhängig von der Anzahl der Zeilen, die diese Geschäftsdokumente enthalten.</span><span class="sxs-lookup"><span data-stu-id="22681-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="22681-122">Die Anzahl der eingereichten Geschäftsdokumente, die erfolgreich vom elektronischen Rechnungsdienst verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="22681-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="22681-123">Ein Dokument gilt als erfolgreich verarbeitet, wenn der Aktionsfluss, der in der Funktionseinrichtung definiert ist, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="22681-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="22681-124">Wenn eine elektronische Rechnung an einen externen Webdienst gesendet wird, erfolgt die Zählung unabhängig von den Ergebnissen der Webdienst-Verarbeitung (akzeptiert, abgelehnt oder Schemavalidierungsfehler).</span><span class="sxs-lookup"><span data-stu-id="22681-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="22681-125">Wenn der Webdienst die Anfrage des elektronischen Rechnungsdienstes erhalten und darauf geantwortet hat, gilt die Einreichung als gültige Zählung.</span><span class="sxs-lookup"><span data-stu-id="22681-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="22681-126">**Ausnahme:** Geschäftsdokumente werden nicht gezählt, wenn sie von Finance and Supply Chain Management erneut an den Dienst für die elektronische Rechnungstellung übermittelt werden, beispielsweise in Szenarien, in denen eine erneute Übermittlung desselben Geschäftsdokuments erforderlich ist, um den Status der elektronischen Rechnung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="22681-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="22681-127">Zum Beispiel wird die Ausstellung einer brasilianischen elektronischen Rechnung (Steuerdokument) als gültig gezählt, aber die Stornierungsanfrage dafür wird nicht gezählt.</span><span class="sxs-lookup"><span data-stu-id="22681-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="22681-128">Herstellkostenkalkulation</span><span class="sxs-lookup"><span data-stu-id="22681-128">Calculation</span></span>

<span data-ttu-id="22681-129">Die Berechnung des Saldos wird wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="22681-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="22681-130">Guthaben = Kostenlos + Gekauft – Gebraucht</span><span class="sxs-lookup"><span data-stu-id="22681-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="22681-131">Wobei:</span><span class="sxs-lookup"><span data-stu-id="22681-131">Where:</span></span>

- <span data-ttu-id="22681-132">Frei:</span><span class="sxs-lookup"><span data-stu-id="22681-132">Free:</span></span>
  
    <span data-ttu-id="22681-133">Ein kostenloser Umfang an Geschäftsunterlagen, den der Kunde pro Monat einreichen kann.</span><span class="sxs-lookup"><span data-stu-id="22681-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="22681-134">Es enthält ein Paket von 100 Geschäftsdokumenten, die an den elektronischen Rechnungsdienst übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="22681-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="22681-135">Das freie Volumen ist nicht kumulativ und das verbleibende Guthaben wird nicht auf den nächsten Zeitraum übertragen.</span><span class="sxs-lookup"><span data-stu-id="22681-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="22681-136">Eingekauft:</span><span class="sxs-lookup"><span data-stu-id="22681-136">Purchased:</span></span>
  
    <span data-ttu-id="22681-137">Ein Paket von 1.000 Geschäftsdokumenten, die an den elektronischen Rechnungsdienst übermittelt werden können.</span><span class="sxs-lookup"><span data-stu-id="22681-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="22681-138">Dieses Paket muss monatlich für Ihre Organisation erworben werden.</span><span class="sxs-lookup"><span data-stu-id="22681-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="22681-139">Das gekaufte Volumen ist nicht kumulativ und das verbleibende Guthaben wird nicht auf den nächsten Zeitraum übertragen.</span><span class="sxs-lookup"><span data-stu-id="22681-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="22681-140">Verwendet:</span><span class="sxs-lookup"><span data-stu-id="22681-140">Used:</span></span> 

    <span data-ttu-id="22681-141">Die Anzahl der Übermittlungen von Geschäftsdokumenten an den elektronischen Rechnungsstellungsdienst nach definierten Kriterien.</span><span class="sxs-lookup"><span data-stu-id="22681-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="22681-142">Wenn Ihre Organisation plant, das monatliche Volumen von 100 kostenlosen Übermittlungen zu überschreiten, kaufen Sie das Spitzenvolumen, um sicherzustellen, dass Sie die Microsoft-Lizenzierungsrichtlinie für den elektronischen Rechnungsdienst einhalten.</span><span class="sxs-lookup"><span data-stu-id="22681-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="22681-143">Derzeit muss das gekaufte Volumen je nach Erwerbsdatum in mehreren Paketen von 1.000 Einreichungen manuell eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="22681-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="22681-144">Indikator: Nutzung nach Funktion</span><span class="sxs-lookup"><span data-stu-id="22681-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="22681-145">Dieser Indikator zeigt die Nutzung elektronischer Rechnungsfunktionen für die Ausstellung elektronischer Rechnungen während eines definierten Zeitraums an.</span><span class="sxs-lookup"><span data-stu-id="22681-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="22681-146">Kalkulation:</span><span class="sxs-lookup"><span data-stu-id="22681-146">Calculation:</span></span>
  
    <span data-ttu-id="22681-147">Verwendet = Die Anzahl, wie oft jede elektronische Rechnungsstellungsfunktion während der Übermittlung von Geschäftsdokumenten an den elektronischen Rechnungsstellungsdienst verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="22681-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="22681-148">Indikator: Nutzung nach Umgebung</span><span class="sxs-lookup"><span data-stu-id="22681-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="22681-149">Dieser Indikator zeigt die Nutzung von Service-Umgebungen für die elektronische Rechnungsstellung während eines definierten Zeitraums an.</span><span class="sxs-lookup"><span data-stu-id="22681-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="22681-150">Kalkulation:</span><span class="sxs-lookup"><span data-stu-id="22681-150">Calculation:</span></span>
    
    <span data-ttu-id="22681-151">Verwendet = Die Anzahl, wie oft jedeService-Umgebung für die elektronische Rechnungsstellung während der Übermittlung von Geschäftsdokumenten an den elektronischen Rechnungsstellungsdienst verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="22681-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="22681-152">Indikator: Verbrauch pro Monat (Import)</span><span class="sxs-lookup"><span data-stu-id="22681-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="22681-153">Dieser Indikator zeigt das Importvolumen elektronischer Rechnungen durch den Dienst für die elektronische Rechnungserstellung in Finance und Supply Chain Management während eines definierten Zeitraums an.</span><span class="sxs-lookup"><span data-stu-id="22681-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="22681-154">Bereich:</span><span class="sxs-lookup"><span data-stu-id="22681-154">Scope:</span></span>

    <span data-ttu-id="22681-155">Elektronische Rechnungen, die in Finance and Supply Chain Management importiert werden, unabhängig von der Anzahl der Zeilen, die diese elektronischen Rechnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="22681-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="22681-156">Kalkulation:</span><span class="sxs-lookup"><span data-stu-id="22681-156">Calculation:</span></span>

    <span data-ttu-id="22681-157">Eingegangen = Die Anzahl importierter elektronischer Rechnungen in Finance and Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="22681-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="22681-158">Funktionen</span><span class="sxs-lookup"><span data-stu-id="22681-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="22681-159">Kaufen</span><span class="sxs-lookup"><span data-stu-id="22681-159">Purchase</span></span>

<span data-ttu-id="22681-160">Wählen Sie auf der Registerkarte **Verbrauch pro Monat (Export)** die Option **Kauf**, um die Anzahl der erworbenen Einreichungen manuell zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="22681-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="22681-161">Wählen Sie für ein bestimmtes Datum **Neu** und geben Sie die Anzahl der **Pakete** ein, die an diesem Tag erworben wurden.</span><span class="sxs-lookup"><span data-stu-id="22681-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="22681-162">Die **Menge** wird folgendermaßen berechnet:</span><span class="sxs-lookup"><span data-stu-id="22681-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="22681-163">Menge = Pakete \* 1.000</span><span class="sxs-lookup"><span data-stu-id="22681-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="22681-164">Das berechnete **Menge** spiegelt sich in der **Gekauft** vom Indikator **Verbrauch pro Monat (Export)**.</span><span class="sxs-lookup"><span data-stu-id="22681-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="22681-165">Buchen</span><span class="sxs-lookup"><span data-stu-id="22681-165">Update</span></span>

<span data-ttu-id="22681-166">Wählen Sie im Aktivitätsbereich **Aktualisieren**, um die Berechnung zu aktualisieren und die auf der Seite und im Diagramm angezeigten Daten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="22681-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="22681-167">Verlaufsdaten zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="22681-167">Reset history data</span></span>

<span data-ttu-id="22681-168">Wählen Sie im Aktivitätsbereich **Verlaufsdaten zurücksetzen**, um die Datenbank zu aktualisieren, aus der die Indikatoren berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="22681-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="22681-169">Das **Nutzungsverwaltung**-Dashboard zeigt keine Geldbeträge an.</span><span class="sxs-lookup"><span data-stu-id="22681-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="22681-170">Stattdessen wird nur das Volumen der gezählten Einreichungen und importierten Dokumente angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22681-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
