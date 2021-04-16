---
title: Ursprungsland
description: Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen. Diese Zertifikate hängen häufig vom Herkunftsland ab. Dieses Thema enthält Informationen zur Herkunftslandfunktion, mit der Sie ein Produkt mit seinem Herkunftsland verknüpfen und die Produktzertifizierungen verfolgen können.
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: b07747752dd09f39c3a7a9a647cc3d10cc4b5cc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829545"
---
# <a name="country-of-origin"></a><span data-ttu-id="b1423-105">Ursprungsland</span><span class="sxs-lookup"><span data-stu-id="b1423-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1423-106">Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b1423-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="b1423-107">Diese Zertifikate hängen häufig vom Herkunftsland ab.</span><span class="sxs-lookup"><span data-stu-id="b1423-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="b1423-108">Mit der Herkunftslandfunktion können Sie ein Produkt mit seinem Herkunftsland verknüpfen und seine Produktzertifizierungen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="b1423-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="b1423-109">Aktivieren der Herkunftslandfunktion</span><span class="sxs-lookup"><span data-stu-id="b1423-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="b1423-110">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b1423-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b1423-111">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b1423-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b1423-112">Im Arbeitsbereich **Funktionsverwaltung** ist die Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="b1423-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b1423-113">**Modul:** *Produktinformationsverwaltung*</span><span class="sxs-lookup"><span data-stu-id="b1423-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="b1423-114">**Funktionsname:** *Funktion zur Verwaltung des Herkunftslandes*</span><span class="sxs-lookup"><span data-stu-id="b1423-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="b1423-115">Quell- und Zielländer konfigurieren</span><span class="sxs-lookup"><span data-stu-id="b1423-115">Configure source and destination countries</span></span>

<span data-ttu-id="b1423-116">Bevor Sie ein Zertifikat für ein Produkt ausstellen, müssen Sie das Produkt mit seinem Zielland und seinem Herkunftsland verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="b1423-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="b1423-117">Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Regeln für das Herkunftsland**.</span><span class="sxs-lookup"><span data-stu-id="b1423-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="b1423-118">Wählen Sie ein vorhandenes Länder-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Länder-Setup zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1423-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="b1423-119">Legen Sie die folgenden Werte für das ausgewählte oder neue Land fest.</span><span class="sxs-lookup"><span data-stu-id="b1423-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="b1423-120">Feld</span><span class="sxs-lookup"><span data-stu-id="b1423-120">Field</span></span> | <span data-ttu-id="b1423-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1423-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="b1423-122">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="b1423-122">Item number</span></span> | <span data-ttu-id="b1423-123">Wählen Sie die Artikelnummer des Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="b1423-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="b1423-124">Zielland</span><span class="sxs-lookup"><span data-stu-id="b1423-124">Destination country</span></span> | <span data-ttu-id="b1423-125">Wählen Sie das Land aus, in das Sie das Produkt liefern.</span><span class="sxs-lookup"><span data-stu-id="b1423-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="b1423-126">Ursprungsland</span><span class="sxs-lookup"><span data-stu-id="b1423-126">Origin country</span></span> | <span data-ttu-id="b1423-127">Wählen Sie das Land aus, aus dem Sie das Produkt senden.</span><span class="sxs-lookup"><span data-stu-id="b1423-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="b1423-128">Mit diesem Setup können Sie einen Stücklistenbericht (BOM-Bericht) erstellen, in dem Sie das Herkunftsland für jedes Teil angeben können, für das Quell- und Zielländer angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b1423-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="b1423-129">Dieser Bericht hilft Ihnen dabei, ein ganzheitliches Bild davon zu erhalten, woher Ihre Teile kommen und wohin sie gehen.</span><span class="sxs-lookup"><span data-stu-id="b1423-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="b1423-130">Lieferantenzertifikate nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="b1423-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="b1423-131">Sie können die Seite **Lieferantenzertifikate des Herkunftslandes** verwenden, um Zertifikate nachzuverfolgen, die Sie an Lieferanten ausstellen.</span><span class="sxs-lookup"><span data-stu-id="b1423-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="b1423-132">Sie müssen entscheiden, welche Zertifikatdokumente Sie ausstellen und wie Sie sie den Kunden melden.</span><span class="sxs-lookup"><span data-stu-id="b1423-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="b1423-133">Mit dieser Funktion können Sie Ihre Zertifikate besser nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="b1423-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="b1423-134">Außerdem können Sie damit auswählen, ob die relevanten Zertifikatsnummern auf Rechnungen, Lieferscheinen und/oder Auftragsbestätigungen erscheinen.</span><span class="sxs-lookup"><span data-stu-id="b1423-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="b1423-135">Gehen Sie zum Einrichten Ihrer Zertifikatsinformationen folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="b1423-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="b1423-136">Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Kreditorenzertifikate des Herkunftslands**.</span><span class="sxs-lookup"><span data-stu-id="b1423-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="b1423-137">Wählen Sie ein vorhandenes Zertifikat-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktivitätsbereich aus, um ein neues Zertifikat-Setup zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1423-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="b1423-138">Legen Sie die folgenden Einstellungen für das ausgewählte oder neue Zertifikat fest.</span><span class="sxs-lookup"><span data-stu-id="b1423-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="b1423-139">Feld</span><span class="sxs-lookup"><span data-stu-id="b1423-139">Field</span></span> | <span data-ttu-id="b1423-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1423-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="b1423-141">Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="b1423-141">Vendor account</span></span> | <span data-ttu-id="b1423-142">Wählen Sie den Lieferanten aus, an den Sie das Zertifikat ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="b1423-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="b1423-143">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="b1423-143">Item number</span></span> | <span data-ttu-id="b1423-144">Wählen Sie den Artikel aus, für den Sie das Zertifikat ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="b1423-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="b1423-145">Land/Region</span><span class="sxs-lookup"><span data-stu-id="b1423-145">Country/region</span></span> | <span data-ttu-id="b1423-146">Das Zielland oder die Zielregion, in der Sie dieses Zertifikat verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="b1423-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="b1423-147">Zertifikatnummer</span><span class="sxs-lookup"><span data-stu-id="b1423-147">Certificate number</span></span> | <span data-ttu-id="b1423-148">Geben Sie die Kennnummer des von Ihnen ausgestellten Zertifikats ein.</span><span class="sxs-lookup"><span data-stu-id="b1423-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="b1423-149">In Kraft</span><span class="sxs-lookup"><span data-stu-id="b1423-149">Effective</span></span> | <span data-ttu-id="b1423-150">Wählen Sie das erste Datum aus, an dem das aktuelle Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b1423-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="b1423-151">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="b1423-151">Expiration</span></span> | <span data-ttu-id="b1423-152">Wählen Sie das letzte Datum aus, an dem das aktuelle Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b1423-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="b1423-153">Auf Rechnung drucken</span><span class="sxs-lookup"><span data-stu-id="b1423-153">Print on invoice</span></span> | <span data-ttu-id="b1423-154">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Rechnungen zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="b1423-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="b1423-155">Auf Lieferscheinen drucken</span><span class="sxs-lookup"><span data-stu-id="b1423-155">Print on packing slip</span></span> | <span data-ttu-id="b1423-156">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Lieferscheine zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="b1423-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="b1423-157">Auf Auftrag drucken</span><span class="sxs-lookup"><span data-stu-id="b1423-157">Print on sales order</span></span> | <span data-ttu-id="b1423-158">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Aufträge zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="b1423-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="b1423-159">Nehmen Sie das Herkunftsland in Stücklistenberichte auf</span><span class="sxs-lookup"><span data-stu-id="b1423-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="b1423-160">Wenn Sie einen Stücklistenbericht erstellen, können Sie das Herkunftsland für jeden Teil einbeziehen, für den Sie Quell- und Zielländer auf der Seite **Regeln für das Herkunftsland** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b1423-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="b1423-161">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="b1423-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b1423-162">Wählen Sie ein Produkt aus oder erstellen Sie es, um seine Seite **Freigegebene Produktdetails** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b1423-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="b1423-163">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Techniker** in der Gruppe **Stückliste** die Option **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="b1423-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="b1423-164">Wählen Sie auf der Seite, die angezeigt wird, im Aktivitätsbereich die Option **Stückliste \> Drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="b1423-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="b1423-165">Legen Sie im Dialogfeld **Stücklistenpositionen** das Feld **Zielland** auf das Zielland fest, das Sie in Ihrem Bericht anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="b1423-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="b1423-166">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1423-166">Select **OK**.</span></span>

<span data-ttu-id="b1423-167">Ein Bericht mit Informationen zum Herkunftsland jedes Teils wird generiert und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1423-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="b1423-168">Hier ist ein Beispiel des Berichts.</span><span class="sxs-lookup"><span data-stu-id="b1423-168">Here is an example of the report.</span></span>

<span data-ttu-id="b1423-169">![Herkunftslandbericht](media/country-of-origin-report.png "Herkunftslandbericht")</span><span class="sxs-lookup"><span data-stu-id="b1423-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]