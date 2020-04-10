---
title: Drucker-ER-Zieltyps
description: Dieses Thema enthält Informationen zum Konfigurieren eines Druckerziels für jede ORDNER- oder DATEI-Komponente eines ER-Formats (Electronic Reporting), das zum Generieren ausgehender Dokumente in PDF- oder Microsoft Office-Formaten (Excel\Word) konfiguriert ist.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 148da191ce4ea99c237895c40ec007a1aa0cd537
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150791"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="022af-103">Druckerziel</span><span class="sxs-lookup"><span data-stu-id="022af-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="022af-104">Sie können ein generiertes Dokument direkt an einen Netzwerkdrucker senden und drucken.</span><span class="sxs-lookup"><span data-stu-id="022af-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="022af-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="022af-105">Prerequisites</span></span>

<span data-ttu-id="022af-106">Bevor Sie beginnen, müssen Sie den Dokumentweiterleitungsagenten installieren und konfigurieren und anschließend die Netzwerkdrucker registrieren.</span><span class="sxs-lookup"><span data-stu-id="022af-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="022af-107">Weitere Informationen finden Sie unter [Installieren des Dokumentweiterleitungsagenten, um Netzwerkdruck zu aktivieren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="022af-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="022af-108">Druckerziel verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="022af-108">Make the Printer destination available</span></span>

<span data-ttu-id="022af-109">Damit das **Drucker**-Ziel in der aktuellen Instanz von Microsoft Dynamics 365 Finance verfügbar ist, gehen Sie zum Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die folgenden Funktionen in dieser Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="022af-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="022af-110">Ausgehende Dokumente der elektronischen Berichterstattung aus Microsoft Office-Formaten in PDF konvertieren</span><span class="sxs-lookup"><span data-stu-id="022af-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="022af-111">Dokumentweiterleitungsagent als Ziel der elektronischen Berichterstellung für ausgehende Dokumente</span><span class="sxs-lookup"><span data-stu-id="022af-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="022af-112">[![Aktivieren der ER-Druckerzielfunktion in der Funktionsverwaltung](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="022af-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="022af-113">Anwendbarkeit</span><span class="sxs-lookup"><span data-stu-id="022af-113">Applicability</span></span>

<span data-ttu-id="022af-114">Das **Drucker**-Ziel kann nur für Dateikomponenten konfiguriert werden, die zum Generieren von Ausgaben im druckbaren PDF-Format (PDF Merger- oder PDF-Dateiformatelemente) oder Microsoft Office Excel-/Word-Format (Excel-Datei) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="022af-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="022af-115">Wenn die Ausgabe im PDF-Format erstellt wird, wird sie an einen Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="022af-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="022af-116">Wenn die Ausgabe im Microsoft Office-Format generiert wird, wird es automatisch in das PDF-Format konvertiert und dann an einen Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="022af-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="022af-117">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="022af-117">Limitations</span></span>

<span data-ttu-id="022af-118">Diese Funktion ist eine Vorschau-Funktion und unterliegt den angegebenen Nutzungsbedingungen, die in [Ergänzende Nutzungsbedingungen für Microsoft Dynamics 365-Vorschauen](https://go.microsoft.com/fwlink/?linkid=2105274) beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="022af-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="022af-119">Das **Drucker**-Ziel ist nur für Cloud-Bereitstellungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="022af-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="022af-120">Druckerziel verwenden</span><span class="sxs-lookup"><span data-stu-id="022af-120">Use the Printer destination</span></span>

1. <span data-ttu-id="022af-121">Setzen Sie die Option **Aktiviert** auf **Ja**, um ein generiertes Dokument an einen Drucker zu senden.</span><span class="sxs-lookup"><span data-stu-id="022af-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="022af-122">Im Feld **Druckername** wählen Sie den gewünschten Netzwerkdrucker aus.</span><span class="sxs-lookup"><span data-stu-id="022af-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="022af-123">Setzen Sie die Option **Im Druckarchiv speichern?** auf **Ja**, um die generierte Ausgabe im Druckarchiv zu speichern, damit sie für weitere Ausdrucke zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="022af-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="022af-124">Um später auf die archivierte Ausgabe zuzugreifen, gehen Sie zu **Organisationsverwaltung** \> **Abfragen und Berichte** \> **Berichtarchiv**.</span><span class="sxs-lookup"><span data-stu-id="022af-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="022af-125">[![Verwenden des Druckerziels](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="022af-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="022af-126">Die Option für **In PDF konvertieren** muss nicht aktiviert sein, wenn Sie das **Drucker**-Ziel konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="022af-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="022af-127">Die PDF-Konvertierung für Druckzwecke erfolgt auch dann, wenn die Option deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="022af-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="022af-128">Um eine bestimmte [Seitenausrichtung](electronic-reporting-destinations.md#SelectPdfPageOrientation) zu verwenden, wenn Sie ein ausgehendes Dokument im Excel-Format drucken, müssen Sie die Möglichkeit **In PDF konvertieren** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="022af-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="022af-129">Wenn Sie die Option **In PDF konvertieren** auf **Ja** einstellen, wird das Feld **Seitenausrichtung** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="022af-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="022af-130">In dem Feld **Seitenausrichtung** können Sie eine Seitenausrichtung auswählen.</span><span class="sxs-lookup"><span data-stu-id="022af-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="022af-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="022af-131">Additional resources</span></span>

- [<span data-ttu-id="022af-132">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="022af-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="022af-133">Zielorte für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="022af-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
