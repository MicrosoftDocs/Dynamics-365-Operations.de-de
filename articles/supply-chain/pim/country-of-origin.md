---
title: Ursprungsland
description: Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen. Diese Zertifikate hängen häufig vom Herkunftsland ab. Dieses Thema enthält Informationen zur Herkunftslandfunktion, mit der Sie ein Produkt mit seinem Herkunftsland verknüpfen und die Produktzertifizierungen verfolgen können.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428367"
---
# <a name="country-of-origin"></a><span data-ttu-id="2025e-105">Ursprungsland</span><span class="sxs-lookup"><span data-stu-id="2025e-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2025e-106">Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2025e-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="2025e-107">Diese Zertifikate hängen häufig vom Herkunftsland ab.</span><span class="sxs-lookup"><span data-stu-id="2025e-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="2025e-108">Mit der Herkunftslandfunktion können Sie ein Produkt mit seinem Herkunftsland verknüpfen und seine Produktzertifizierungen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="2025e-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="2025e-109">Aktivieren der Herkunftslandfunktion</span><span class="sxs-lookup"><span data-stu-id="2025e-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="2025e-110">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="2025e-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2025e-111">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2025e-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="2025e-112">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="2025e-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2025e-113">**Modul:** *Produktinformationsverwaltung*</span><span class="sxs-lookup"><span data-stu-id="2025e-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="2025e-114">**Funktionsname:** *Funktion zur Verwaltung des Herkunftslandes*</span><span class="sxs-lookup"><span data-stu-id="2025e-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="2025e-115">Quell- und Zielländer konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2025e-115">Configure source and destination countries</span></span>

<span data-ttu-id="2025e-116">Bevor Sie ein Zertifikat für ein Produkt ausstellen, müssen Sie das Produkt mit seinem Zielland und seinem Herkunftsland verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2025e-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="2025e-117">Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Regeln für das Herkunftsland**.</span><span class="sxs-lookup"><span data-stu-id="2025e-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="2025e-118">Wählen Sie ein vorhandenes Länder-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Länder-Setup zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2025e-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="2025e-119">Legen Sie die folgenden Werte für das ausgewählte oder neue Land fest.</span><span class="sxs-lookup"><span data-stu-id="2025e-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="2025e-120">Feld</span><span class="sxs-lookup"><span data-stu-id="2025e-120">Field</span></span> | <span data-ttu-id="2025e-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2025e-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2025e-122">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="2025e-122">Item number</span></span> | <span data-ttu-id="2025e-123">Wählen Sie die Artikelnummer des Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="2025e-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="2025e-124">Zielland</span><span class="sxs-lookup"><span data-stu-id="2025e-124">Destination country</span></span> | <span data-ttu-id="2025e-125">Wählen Sie das Land aus, in das Sie das Produkt liefern.</span><span class="sxs-lookup"><span data-stu-id="2025e-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="2025e-126">Ursprungsland</span><span class="sxs-lookup"><span data-stu-id="2025e-126">Origin country</span></span> | <span data-ttu-id="2025e-127">Wählen Sie das Land aus, aus dem Sie das Produkt senden.</span><span class="sxs-lookup"><span data-stu-id="2025e-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="2025e-128">Mit diesem Setup können Sie einen Stücklistenbericht (BOM-Bericht) erstellen, in dem Sie das Herkunftsland für jedes Teil angeben können, für das Quell- und Zielländer angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2025e-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="2025e-129">Dieser Bericht hilft Ihnen dabei, ein ganzheitliches Bild davon zu erhalten, woher Ihre Teile kommen und wohin sie gehen.</span><span class="sxs-lookup"><span data-stu-id="2025e-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="2025e-130">Lieferantenzertifikate nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="2025e-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="2025e-131">Sie können die Seite **Lieferantenzertifikate des Herkunftslandes** verwenden, um Zertifikate nachzuverfolgen, die Sie an Lieferanten ausstellen.</span><span class="sxs-lookup"><span data-stu-id="2025e-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="2025e-132">Sie müssen entscheiden, welche Zertifikatdokumente Sie ausstellen und wie Sie sie den Kunden melden.</span><span class="sxs-lookup"><span data-stu-id="2025e-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="2025e-133">Mit dieser Funktion können Sie Ihre Zertifikate besser nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="2025e-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="2025e-134">Außerdem können Sie damit auswählen, ob die relevanten Zertifikatsnummern auf Rechnungen, Lieferscheinen und/oder Auftragsbestätigungen erscheinen.</span><span class="sxs-lookup"><span data-stu-id="2025e-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="2025e-135">Gehen Sie zum Einrichten Ihrer Zertifikatsinformationen folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="2025e-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="2025e-136">Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Kreditorenzertifikate des Herkunftslands**.</span><span class="sxs-lookup"><span data-stu-id="2025e-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="2025e-137">Wählen Sie ein vorhandenes Zertifikat-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Zertifikat-Setup zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2025e-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="2025e-138">Legen Sie die folgenden Einstellungen für das ausgewählte oder neue Zertifikat fest.</span><span class="sxs-lookup"><span data-stu-id="2025e-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="2025e-139">Feld</span><span class="sxs-lookup"><span data-stu-id="2025e-139">Field</span></span> | <span data-ttu-id="2025e-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2025e-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="2025e-141">Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="2025e-141">Vendor account</span></span> | <span data-ttu-id="2025e-142">Wählen Sie den Lieferanten aus, an den Sie das Zertifikat ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="2025e-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="2025e-143">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="2025e-143">Item number</span></span> | <span data-ttu-id="2025e-144">Wählen Sie den Artikel aus, für den Sie das Zertifikat ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="2025e-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="2025e-145">Land/Region</span><span class="sxs-lookup"><span data-stu-id="2025e-145">Country/region</span></span> | <span data-ttu-id="2025e-146">Das Zielland oder die Zielregion, in der Sie dieses Zertifikat verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="2025e-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="2025e-147">Zertifikatnummer</span><span class="sxs-lookup"><span data-stu-id="2025e-147">Certificate number</span></span> | <span data-ttu-id="2025e-148">Geben Sie die Kennnummer des von Ihnen ausgestellten Zertifikats ein.</span><span class="sxs-lookup"><span data-stu-id="2025e-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="2025e-149">In Kraft</span><span class="sxs-lookup"><span data-stu-id="2025e-149">Effective</span></span> | <span data-ttu-id="2025e-150">Wählen Sie das erste Datum aus, an dem das aktuelle Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2025e-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="2025e-151">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="2025e-151">Expiration</span></span> | <span data-ttu-id="2025e-152">Wählen Sie das letzte Datum aus, an dem das aktuelle Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2025e-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="2025e-153">Auf Rechnung drucken</span><span class="sxs-lookup"><span data-stu-id="2025e-153">Print on invoice</span></span> | <span data-ttu-id="2025e-154">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Rechnungen zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="2025e-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="2025e-155">Auf Lieferscheinen drucken</span><span class="sxs-lookup"><span data-stu-id="2025e-155">Print on packing slip</span></span> | <span data-ttu-id="2025e-156">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Lieferscheine zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="2025e-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="2025e-157">Auf Auftrag drucken</span><span class="sxs-lookup"><span data-stu-id="2025e-157">Print on sales order</span></span> | <span data-ttu-id="2025e-158">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Aufträge zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="2025e-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="2025e-159">Nehmen Sie das Herkunftsland in Stücklistenberichte auf</span><span class="sxs-lookup"><span data-stu-id="2025e-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="2025e-160">Wenn Sie einen Stücklistenbericht erstellen, können Sie das Herkunftsland für jeden Teil einbeziehen, für den Sie Quell- und Zielländer auf der Seite **Regeln für das Herkunftsland** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2025e-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="2025e-161">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="2025e-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2025e-162">Wählen Sie ein Produkt aus oder erstellen Sie es, um seine Seite **Freigegebene Produktdetails** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2025e-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="2025e-163">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Techniker** in der Gruppe **Stückliste** die Option **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="2025e-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="2025e-164">Wählen Sie auf der Seite, die angezeigt wird, im Aktivitätsbereich die Option **Stückliste \> Drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="2025e-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="2025e-165">Legen Sie im Dialogfeld **Stücklistenpositionen** das Feld **Zielland** auf das Zielland fest, das Sie in Ihrem Bericht anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="2025e-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="2025e-166">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="2025e-166">Select **OK**.</span></span>

<span data-ttu-id="2025e-167">Ein Bericht mit Informationen zum Herkunftsland jedes Teils wird generiert und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2025e-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="2025e-168">Hier ist ein Beispiel des Berichts.</span><span class="sxs-lookup"><span data-stu-id="2025e-168">Here is an example of the report.</span></span>

<span data-ttu-id="2025e-169">![Herkunftslandbericht](media/country-of-origin-report.png "Herkunftslandbericht")</span><span class="sxs-lookup"><span data-stu-id="2025e-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
