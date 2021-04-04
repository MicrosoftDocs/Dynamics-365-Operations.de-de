---
title: Drucker-ER-Zieltyps
description: In diesem Thema wird erläutert, wie für jede FOLDER- oder FILE-Komponente eines EB-Formats (elektronische Berichterstellung) ein Druckerziel konfiguriert werden kann.
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561949"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="3682f-103">Druckziel</span><span class="sxs-lookup"><span data-stu-id="3682f-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3682f-104">Sie können ein generiertes Dokument direkt an einen Netzwerkdrucker senden und drucken.</span><span class="sxs-lookup"><span data-stu-id="3682f-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3682f-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3682f-105">Prerequisites</span></span>

<span data-ttu-id="3682f-106">Bevor Sie beginnen, müssen Sie den Dokumentweiterleitungsagenten installieren und konfigurieren und anschließend die Netzwerkdrucker registrieren.</span><span class="sxs-lookup"><span data-stu-id="3682f-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="3682f-107">Weitere Informationen finden Sie unter [Installieren des Dokumentweiterleitungsagenten, um Netzwerkdruck zu aktivieren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="3682f-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="3682f-108">Druckerziel verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="3682f-108">Make the Printer destination available</span></span>

<span data-ttu-id="3682f-109">Damit das **Drucker**-Ziel in der aktuellen Instanz von Microsoft Dynamics 365 Finance verfügbar ist, gehen Sie zum Arbeitsbereich **Funktionsverwaltung**, und aktivieren Sie die folgenden Funktionen in dieser Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="3682f-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="3682f-110">Ausgehende Dokumente der elektronischen Berichterstattung aus Microsoft Office-Formaten in PDF konvertieren</span><span class="sxs-lookup"><span data-stu-id="3682f-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="3682f-111">Dokumentweiterleitungsagent als Ziel der elektronischen Berichterstellung für ausgehende Dokumente</span><span class="sxs-lookup"><span data-stu-id="3682f-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="3682f-112">[![Aktivieren der ER-Druckerzielfunktion in der Funktionsverwaltung](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="3682f-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="3682f-113">Anwendbarkeit</span><span class="sxs-lookup"><span data-stu-id="3682f-113">Applicability</span></span>

<span data-ttu-id="3682f-114">Das **Drucker**-Ziel kann nur für Dateikomponenten konfiguriert werden, die zum Generieren von Ausgaben im druckbaren PDF-Format (PDF Merger- oder PDF-Dateiformatelemente) oder Microsoft Office Excel-/Word-Format (Excel-Datei) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3682f-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="3682f-115">Wenn die Ausgabe im PDF-Format erstellt wird, wird sie an einen Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="3682f-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="3682f-116">Wenn die Ausgabe im Microsoft Office-Format generiert wird, wird es automatisch in das PDF-Format konvertiert und dann an einen Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="3682f-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="3682f-117">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3682f-117">Limitations</span></span>

<span data-ttu-id="3682f-118">Das **Drucker**-Ziel ist nur für Cloud-Bereitstellungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="3682f-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="3682f-119">Druckerziel verwenden</span><span class="sxs-lookup"><span data-stu-id="3682f-119">Use the Printer destination</span></span>

1. <span data-ttu-id="3682f-120">Setzen Sie die Option **Aktiviert** auf **Ja**, um ein generiertes Dokument an einen Drucker zu senden.</span><span class="sxs-lookup"><span data-stu-id="3682f-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="3682f-121">Im Feld **Druckername** wählen Sie den gewünschten Netzwerkdrucker aus.</span><span class="sxs-lookup"><span data-stu-id="3682f-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="3682f-122">Setzen Sie die Option **Im Druckarchiv speichern?** auf **Ja**, um die generierte Ausgabe im Druckarchiv zu speichern, damit sie für weitere Ausdrucke zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="3682f-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="3682f-123">Um später auf die archivierte Ausgabe zuzugreifen, gehen Sie zu **Organisationsverwaltung** \> **Abfragen und Berichte** \> **Berichtarchiv**.</span><span class="sxs-lookup"><span data-stu-id="3682f-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="3682f-124">[![Verwenden des Druckerziels](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="3682f-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3682f-125">Die Option für **In PDF konvertieren** muss nicht aktiviert sein, wenn Sie das **Drucker**-Ziel konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3682f-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="3682f-126">Die PDF-Konvertierung für Druckzwecke erfolgt auch dann, wenn die Option deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3682f-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="3682f-127">Um eine bestimmte [Seitenausrichtung](electronic-reporting-destinations.md#SelectPdfPageOrientation) zu verwenden, wenn Sie ein ausgehendes Dokument im Excel-Format drucken, müssen Sie die Möglichkeit **In PDF konvertieren** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3682f-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="3682f-128">Wenn Sie die Option **In PDF konvertieren** auf **Ja** einstellen, wird das Feld **Seitenausrichtung** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3682f-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="3682f-129">In dem Feld **Seitenausrichtung** können Sie eine Seitenausrichtung auswählen.</span><span class="sxs-lookup"><span data-stu-id="3682f-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3682f-130">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3682f-130">Additional resources</span></span>

- [<span data-ttu-id="3682f-131">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="3682f-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="3682f-132">Zielorte für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="3682f-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
