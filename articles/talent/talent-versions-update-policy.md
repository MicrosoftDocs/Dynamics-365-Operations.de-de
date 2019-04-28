---
title: Systemanforderungen und Updaterichtlinie für Talent
description: In diesem Thema sind die Anforderungen für Dynamics 365 for Talent aufgeführt. Außerdem wird die Updaterichtlinie kurz dargestellt.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2389f00b22ec3b5284eeffb2c015533b7a3d13e0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "856300"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="0c233-104">Systemanforderungen und Updaterichtlinie für Talent</span><span class="sxs-lookup"><span data-stu-id="0c233-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c233-105">In diesem Thema sind die Anforderungen für Microsoft Dynamics 365 for Talent aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c233-105">This topic lists requirements for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="0c233-106">Außerdem wird die Updaterichtlinie kurz dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0c233-106">The update policy is outlined, as well.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="0c233-107">Unterstützte Webbrowser</span><span class="sxs-lookup"><span data-stu-id="0c233-107">Supported web browsers</span></span>

<span data-ttu-id="0c233-108">Die Microsoft Dynamics 365 for Talent Webanwendung kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="0c233-108">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="0c233-109">Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10</span><span class="sxs-lookup"><span data-stu-id="0c233-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="0c233-110">Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c233-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="0c233-111">Google Chrome (letzte öffentlich verfügbare Version)</span><span class="sxs-lookup"><span data-stu-id="0c233-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="0c233-112">Apple Safari (letzte öffentlich verfügbare Version)</span><span class="sxs-lookup"><span data-stu-id="0c233-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="0c233-113">Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers.</span><span class="sxs-lookup"><span data-stu-id="0c233-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="0c233-114">Wenn Sie Bilder aufzuzeichnen, die über die Aufgabenaufzeichnung generiert wurden, und diese in Microsoft Word-Dokumente aufnehmen, müssen Sie eine Chrome-Erweiterung installiert haben.</span><span class="sxs-lookup"><span data-stu-id="0c233-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="0c233-115">Der Workflow-Editor wird als ClickOnce-Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="0c233-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="0c233-116">Nur Microsoft Edge und Internet Explorer (auf einer unterstützten Version von Microsoft WindowsClickOnce-Bewerbungen) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0c233-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="0c233-117">Die Workflow-Editor-ClickOnce-Anwendung erfordert ein kompatibles 64-Bit-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="0c233-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="0c233-118">Um PDF-Dateien in der Vorschau anzeigen, sollten Sie moderne Browser wie Microsoft Edge verwenden (aktuellste verfügbare Version) unter Windows 10 oder Google Chrome (aktuellste verfügbare Version) unter Windows 10, 8,1, Windows 8, Windows 7 oder Google Nexus-10 Tablet.</span><span class="sxs-lookup"><span data-stu-id="0c233-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="0c233-119">Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="0c233-119">Network requirements</span></span>
> * <span data-ttu-id="0c233-120">Dynamics 365 for Talent wurde für Netzwerke mit eine Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt.</span><span class="sxs-lookup"><span data-stu-id="0c233-120">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="0c233-121">Diese Latenzzeit ist die Latenzzeit von einem Browser-Client zum Microsoft Azure-Rechenzentrum, das Dynamics 365 for Talent hostet.</span><span class="sxs-lookup"><span data-stu-id="0c233-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="0c233-122">Es wird empfohlen, dass Sie die Netzwerkwartezeit unter [[www.azurespeed.com](https://www.azurespeed.com "Azure Latenztest") testen.</span><span class="sxs-lookup"><span data-stu-id="0c233-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="0c233-123">Bandbreitenanforderungen für Dynamics 365 for Talent hängen vom Szenario ab.</span><span class="sxs-lookup"><span data-stu-id="0c233-123">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="0c233-124">In den meisten Fällen wird eine Bandbreite von mehr als 50 Kilobytes pro Sekunde (kbps) benötigt.</span><span class="sxs-lookup"><span data-stu-id="0c233-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="0c233-125">Berechnen Sie Bandbreitenanforderungen von einem Clientstandort nicht, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="0c233-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="0c233-126">Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0c233-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="0c233-127">Kunden, die sich Gedanken machen über die Bandbreitenanforderungen, sollten eine Testversion von Dynamics 365 for Talent verwenden.</span><span class="sxs-lookup"><span data-stu-id="0c233-127">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="0c233-128">Unterstützte Microsoft Office.Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0c233-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="0c233-129">Zum Ausführen von Microsoft Excel- und Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein.</span><span class="sxs-lookup"><span data-stu-id="0c233-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="0c233-130">Genauere Informationen zu Versionsanforderungen erhalten Sie unter [Fehlerbehebung bei Office-Integration](../dev-itpro/office-integration/office-integration-troubleshooting.md "Fehlerbehebung bei Office-Integration").</span><span class="sxs-lookup"><span data-stu-id="0c233-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="0c233-131">Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.</span><span class="sxs-lookup"><span data-stu-id="0c233-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="update-policy"></a><span data-ttu-id="0c233-132">Updaterichtlinie</span><span class="sxs-lookup"><span data-stu-id="0c233-132">Update policy</span></span>

<span data-ttu-id="0c233-133">Microsoft Dynamics 365 for Talent wird als Cloud-Angebot gewartet.</span><span class="sxs-lookup"><span data-stu-id="0c233-133">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="0c233-134">Aktualisierungen von Dynamics 365 for Talent sind fortlaufend und werden automatisch von Microsoft angewendet.</span><span class="sxs-lookup"><span data-stu-id="0c233-134">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="0c233-135">Aktualisierungen werden auf einen normalen Rhythmus freigegeben, Aktualisierungen erfolgen in allen Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="0c233-135">Updates are released on a regular cadence, updates will be made to all environments.</span></span>  <span data-ttu-id="0c233-136">Dynamics 365 for Talent wird entsprechend dem [Microsoft Support Lifecycle Richtlinie](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecyle") unterstützt, die einen konsistenten und voraussehbaren Leitfaden für die Produktverfügbarkeit bieten.</span><span class="sxs-lookup"><span data-stu-id="0c233-136">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
