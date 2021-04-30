---
title: Systemanforderungen
description: Dieser Artikel beschreibt die Anforderungen für Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a4266ee942f504ffa2f355959af8e3076984d83
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892298"
---
# <a name="system-requirements"></a><span data-ttu-id="b025b-103">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="b025b-103">System requirements</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b025b-104">Dieser Artikel beschreibt die Anforderungen für Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b025b-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b025b-105">Es werden auch die Länder und Regionen beschrieben, in denen Human Resources verfügbar ist, außerdem werden Informationen zu Sprachen und zur Lokalisierung für Human Resourcessdaten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b025b-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="b025b-106">Unterstützte Webbrowser</span><span class="sxs-lookup"><span data-stu-id="b025b-106">Supported web browsers</span></span>

<span data-ttu-id="b025b-107">Human Resources kann in den folgenden Webbrowsern ausgeführt werden, die auf den angegebenen Betriebssysteme ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b025b-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="b025b-108">Microsoft Edge (letzte öffentlich verfügbare Version) unter Windows 10</span><span class="sxs-lookup"><span data-stu-id="b025b-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="b025b-109">Internet Explorer 11 unter Windows 10, Windows 8.1 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="b025b-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="b025b-110">Google Chrome (letzte öffentlich verfügbare Version)</span><span class="sxs-lookup"><span data-stu-id="b025b-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="b025b-111">Apple Safari (letzte öffentlich verfügbare Version)</span><span class="sxs-lookup"><span data-stu-id="b025b-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="b025b-112">Um die neueste Version für jeden Webbrowser zu suchen, wechseln Sie zur Website des Softwareherstellers.</span><span class="sxs-lookup"><span data-stu-id="b025b-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="b025b-113">Wenn Sie Bilder aufzuzeichnen, die über die Aufgabenaufzeichnung generiert wurden, und diese in Microsoft Word-Dokumente aufnehmen, müssen Sie eine Chrome-Erweiterung installiert haben.</span><span class="sxs-lookup"><span data-stu-id="b025b-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="b025b-114">Der Workflow-Editor wird als ClickOnce-Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="b025b-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="b025b-115">Nur Microsoft Edge und Internet Explorer (auf einer unterstützten Version von Microsoft WindowsClickOnce-Bewerbungen) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b025b-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="b025b-116">Die Workflow-Editor-ClickOnce-Anwendung erfordert ein kompatibles 64-Bit-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="b025b-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="b025b-117">Um PDF-Dateien in der Vorschau anzeigen, sollten Sie moderne Browser wie Microsoft Edge verwenden (aktuellste verfügbare Version) unter Windows 10 oder Google Chrome (aktuellste verfügbare Version) unter Windows 10, 8,1, Windows 8, Windows 7 oder Google Nexus-10 Tablet.</span><span class="sxs-lookup"><span data-stu-id="b025b-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="b025b-118">Netzwerkanforderungen</span><span class="sxs-lookup"><span data-stu-id="b025b-118">Network requirements</span></span>
> * <span data-ttu-id="b025b-119">Human Resources wurde für Netzwerke mit eine Latenzzeit von 250-300 Millisekunden (ms) oder weniger entwickelt.</span><span class="sxs-lookup"><span data-stu-id="b025b-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="b025b-120">Diese Latenzzeit ist die Latenzzeit von einem Browser-Client zum Microsoft Azure-Rechenzentrum, das Human Resources hostet.</span><span class="sxs-lookup"><span data-stu-id="b025b-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="b025b-121">Wir empfehlen, die Netzwerklatenz unter [www.azurespeed.com](https://www.azurespeed.com "Azure Latenztest") zu testen.</span><span class="sxs-lookup"><span data-stu-id="b025b-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="b025b-122">Bandbreitenanforderungen für Human Resources hängen vom Szenario ab.</span><span class="sxs-lookup"><span data-stu-id="b025b-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="b025b-123">In den meisten Fällen wird eine Bandbreite von mehr als 50 Kilobytes pro Sekunde (kbps) benötigt.</span><span class="sxs-lookup"><span data-stu-id="b025b-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="b025b-124">Berechnen Sie Bandbreitenanforderungen von einem Clientstandort nicht, indem Sie die Anzahl der Benutzer mit den Mindestbandbreitenanforderungen multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="b025b-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="b025b-125">Die gleichzeitige Nutzung eines bestimmten Standorts ist schwierig zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b025b-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="b025b-126">Kunden, die sich Gedanken machen über die Bandbreitenanforderungen, sollten eine Testversion von Human Resources verwenden.</span><span class="sxs-lookup"><span data-stu-id="b025b-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="b025b-127">Unterstützte Microsoft Office.Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b025b-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="b025b-128">Zum Ausführen von Microsoft Excel- und Word-Add-Ins muss Microsoft Office 2016 für Windows oder Mac installiert sein.</span><span class="sxs-lookup"><span data-stu-id="b025b-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="b025b-129">Weitere Informationen zu den Versionsanforderungen finden Sie unter [Fehlerbehebung bei der Office-Integration](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Fehlerbehebung bei der Office Integration").</span><span class="sxs-lookup"><span data-stu-id="b025b-129">For more details about version requirements, see [Office integration troubleshooting](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="b025b-130">Um Dokumente anzuzeigen, die über die Funktionen für einen Export nach Excel oder einen Export nach Word erzeugt wurden, muss Microsoft Office 2007 oder höher installiert sein.</span><span class="sxs-lookup"><span data-stu-id="b025b-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="b025b-131">Regionale Verfügbarkeit, Sprachen und Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="b025b-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="b025b-132">Sie können eine PDF-Datei der Länder, Regionen der und der von Human Resources unterstützten Sprachen unter [Internationale Verfügbarkeit von Microsoft Dynamics 365](/dynamics365/get-started/availability) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b025b-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="b025b-133">Auch wenn die Benutzeroberfläche in andere Sprachen lokalisiert ist, werden alle Benutzerdaten in der Sprache gespeichert, in der sie eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="b025b-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="b025b-134">Sie können E-Mails und Vorlagen in anderen Sprachen erstellen, aber Daten wie Planungsinformationen sind derzeit nur auf Englisch verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b025b-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="b025b-135">Wenn Sie Entwickler sind, der an dem Erstellen länder- oder regionsspezifischer Anpassungen interessiert ist, oder an der Erstellung einer Lösung für ein Land oder eine Region, die derzeit nicht von Microsoft unterstützt wird, finden weitere Informationen unter [Globalisierung](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="b025b-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]