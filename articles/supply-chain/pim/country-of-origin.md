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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596234"
---
# <a name="country-of-origin"></a><span data-ttu-id="d4439-105">Ursprungsland</span><span class="sxs-lookup"><span data-stu-id="d4439-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4439-106">Viele Organisationen stellen ihren Lieferanten Zertifikate aus, um sicherzustellen, dass die Produkte bestimmten Zertifizierungsstandards entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d4439-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="d4439-107">Diese Zertifikate hängen häufig vom Herkunftsland ab.</span><span class="sxs-lookup"><span data-stu-id="d4439-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="d4439-108">Mit der Herkunftslandfunktion können Sie ein Produkt mit seinem Herkunftsland verknüpfen und seine Produktzertifizierungen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d4439-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="d4439-109">Quell- und Zielländer konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d4439-109">Configure source and destination countries</span></span>

<span data-ttu-id="d4439-110">Bevor Sie ein Zertifikat für ein Produkt ausstellen, müssen Sie das Produkt mit seinem Zielland und seinem Herkunftsland verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d4439-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="d4439-111">Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Regeln für das Herkunftsland**.</span><span class="sxs-lookup"><span data-stu-id="d4439-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="d4439-112">Wählen Sie ein vorhandenes Länder-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktionsbereich aus, um ein neues Länder-Setup zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4439-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="d4439-113">Legen Sie die folgenden Werte für das ausgewählte oder neue Land fest.</span><span class="sxs-lookup"><span data-stu-id="d4439-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="d4439-114">Feld</span><span class="sxs-lookup"><span data-stu-id="d4439-114">Field</span></span> | <span data-ttu-id="d4439-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4439-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="d4439-116">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d4439-116">Item number</span></span> | <span data-ttu-id="d4439-117">Wählen Sie die Artikelnummer des Produkts aus.</span><span class="sxs-lookup"><span data-stu-id="d4439-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="d4439-118">Zielland</span><span class="sxs-lookup"><span data-stu-id="d4439-118">Destination country</span></span> | <span data-ttu-id="d4439-119">Wählen Sie das Land aus, in das Sie das Produkt liefern.</span><span class="sxs-lookup"><span data-stu-id="d4439-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="d4439-120">Ursprungsland</span><span class="sxs-lookup"><span data-stu-id="d4439-120">Origin country</span></span> | <span data-ttu-id="d4439-121">Wählen Sie das Land aus, aus dem Sie das Produkt senden.</span><span class="sxs-lookup"><span data-stu-id="d4439-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="d4439-122">Mit diesem Setup können Sie einen Stücklistenbericht (BOM-Bericht) erstellen, in dem Sie das Herkunftsland für jedes Teil angeben können, für das Quell- und Zielländer angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d4439-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="d4439-123">Dieser Bericht hilft Ihnen dabei, ein ganzheitliches Bild davon zu erhalten, woher Ihre Teile kommen und wohin sie gehen.</span><span class="sxs-lookup"><span data-stu-id="d4439-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="d4439-124">Lieferantenzertifikate nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="d4439-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="d4439-125">Sie können die Seite **Lieferantenzertifikate des Herkunftslandes** verwenden, um Zertifikate nachzuverfolgen, die Sie an Lieferanten ausstellen.</span><span class="sxs-lookup"><span data-stu-id="d4439-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="d4439-126">Sie müssen entscheiden, welche Zertifikatdokumente Sie ausstellen und wie Sie sie den Kunden melden.</span><span class="sxs-lookup"><span data-stu-id="d4439-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="d4439-127">Mit dieser Funktion können Sie Ihre Zertifikate besser nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d4439-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="d4439-128">Außerdem können Sie damit auswählen, ob die relevanten Zertifikatsnummern auf Rechnungen, Lieferscheinen und/oder Auftragsbestätigungen erscheinen.</span><span class="sxs-lookup"><span data-stu-id="d4439-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="d4439-129">Gehen Sie zum Einrichten Ihrer Zertifikatsinformationen folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d4439-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="d4439-130">Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Produktkonformität \> Herkunftsland \> Kreditorenzertifikate des Herkunftslands**.</span><span class="sxs-lookup"><span data-stu-id="d4439-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="d4439-131">Wählen Sie ein vorhandenes Zertifikat-Setup zum Bearbeiten aus oder wählen Sie **Neu** im Aktionsbereich aus, um ein neues Zertifikat-Setup zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4439-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="d4439-132">Legen Sie die folgenden Einstellungen für das ausgewählte oder neue Zertifikat fest.</span><span class="sxs-lookup"><span data-stu-id="d4439-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="d4439-133">Feld</span><span class="sxs-lookup"><span data-stu-id="d4439-133">Field</span></span> | <span data-ttu-id="d4439-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4439-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="d4439-135">Kreditorenkonto</span><span class="sxs-lookup"><span data-stu-id="d4439-135">Vendor account</span></span> | <span data-ttu-id="d4439-136">Wählen Sie den Lieferanten aus, an den Sie das Zertifikat ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="d4439-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="d4439-137">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="d4439-137">Item number</span></span> | <span data-ttu-id="d4439-138">Wählen Sie den Artikel aus, für den Sie das Zertifikat ausgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="d4439-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="d4439-139">Land/Region</span><span class="sxs-lookup"><span data-stu-id="d4439-139">Country/region</span></span> | <span data-ttu-id="d4439-140">Das Zielland oder die Zielregion, in der Sie dieses Zertifikat verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="d4439-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="d4439-141">Zertifikatnummer</span><span class="sxs-lookup"><span data-stu-id="d4439-141">Certificate number</span></span> | <span data-ttu-id="d4439-142">Geben Sie die Kennnummer des von Ihnen ausgestellten Zertifikats ein.</span><span class="sxs-lookup"><span data-stu-id="d4439-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="d4439-143">In Kraft</span><span class="sxs-lookup"><span data-stu-id="d4439-143">Effective</span></span> | <span data-ttu-id="d4439-144">Wählen Sie das erste Datum aus, an dem das aktuelle Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d4439-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="d4439-145">Ablaufdatum</span><span class="sxs-lookup"><span data-stu-id="d4439-145">Expiration</span></span> | <span data-ttu-id="d4439-146">Wählen Sie das letzte Datum aus, an dem das aktuelle Zertifikat gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d4439-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="d4439-147">Auf Rechnung drucken</span><span class="sxs-lookup"><span data-stu-id="d4439-147">Print on invoice</span></span> | <span data-ttu-id="d4439-148">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Rechnungen zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="d4439-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="d4439-149">Auf Lieferscheinen drucken</span><span class="sxs-lookup"><span data-stu-id="d4439-149">Print on packing slip</span></span> | <span data-ttu-id="d4439-150">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Lieferscheine zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="d4439-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="d4439-151">Auf Auftrag drucken</span><span class="sxs-lookup"><span data-stu-id="d4439-151">Print on sales order</span></span> | <span data-ttu-id="d4439-152">Aktivieren Sie dieses Kontrollkästchen, um die Zertifikatsnummer auf Aufträge zu drucken, die im angegebenen Datumsbereich an das angegebene Land adressiert sind.</span><span class="sxs-lookup"><span data-stu-id="d4439-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="d4439-153">Nehmen Sie das Herkunftsland in Stücklistenberichte auf</span><span class="sxs-lookup"><span data-stu-id="d4439-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="d4439-154">Wenn Sie einen Stücklistenbericht erstellen, können Sie das Herkunftsland für jeden Teil einbeziehen, für den Sie Quell- und Zielländer auf der Seite **Regeln für das Herkunftsland** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d4439-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="d4439-155">Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="d4439-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d4439-156">Wählen Sie ein Produkt aus oder erstellen Sie es, um seine Seite **Freigegebene Produktdetails** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4439-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="d4439-157">Wählen Sie im Aktionsbereich auf der Registerkarte **Techniker** in der Gruppe **Stückliste** die Option **Designer** aus.</span><span class="sxs-lookup"><span data-stu-id="d4439-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="d4439-158">Wählen Sie auf der Seite, die angezeigt wird, im Aktivitätsbereich die Option **Stückliste \> Drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="d4439-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="d4439-159">Legen Sie im Dialogfeld **Stücklistenpositionen** das Feld **Zielland** auf das Zielland fest, das Sie in Ihrem Bericht anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d4439-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="d4439-160">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4439-160">Select **OK**.</span></span>

<span data-ttu-id="d4439-161">Ein Bericht mit Informationen zum Herkunftsland jedes Teils wird generiert und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4439-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="d4439-162">Hier ist ein Beispiel des Berichts.</span><span class="sxs-lookup"><span data-stu-id="d4439-162">Here is an example of the report.</span></span>

<span data-ttu-id="d4439-163">![Herkunftslandbericht](media/country-of-origin-report.png "Herkunftslandbericht")</span><span class="sxs-lookup"><span data-stu-id="d4439-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
