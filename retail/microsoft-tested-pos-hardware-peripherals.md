---
title: "POS-Hardware und -Peripheriegeräte"
description: "Moderne Verkaufsstelle (POS) und Cloud POS können eine breite Palette von POS-Hardwareperipheriegeräten mit mehreren Schnittstellen und Bereitstellungsoptionen verwenden, um die verschiedenen Geschäftsszenarien eines Einzelhändlers zu erreichen."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 17738e794f18fddc7320b1b40ef55376fba0de24
ms.contentlocale: de-de
ms.lasthandoff: 08/30/2017

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="72db7-103">POS-Hardware und -Peripheriegeräte</span><span class="sxs-lookup"><span data-stu-id="72db7-103">POS hardware peripherals</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="72db7-104">Moderne Verkaufsstelle (POS) und Cloud POS können eine breite Palette von POS-Hardwareperipheriegeräten mit mehreren Schnittstellen und Bereitstellungsoptionen verwenden, um die verschiedenen Geschäftsszenarien eines Einzelhändlers zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="72db7-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="72db7-105">Um die maximale Auswahl von Geräten von Herstelnd Modellen zu unterstützen, verwendet POS Standardschnittstellen wie OLE für Retail POS (OPOS), Windows Gerätetreiber und Windows-POS Anwendungsprogrammierschnittstellen (APIs).</span><span class="sxs-lookup"><span data-stu-id="72db7-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="72db7-106">Im Allgemeinen arbeitet Point-of-Sale an diesen Geräten, vorausgesetzt, dass der entsprechende Treibet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="72db7-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="72db7-107">Da jedoch jeder Hersteller und jede Softwareentwicklerimplementierung von dieser Standards abweichen kann, gibt es oftmals Unterschiede in unterstützten Funktionen oder Verhalten.</span><span class="sxs-lookup"><span data-stu-id="72db7-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="72db7-108">Die folgende Liste enthält Gerätenmodelle in jede Klasse, die intern von Microsoft getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="72db7-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="72db7-109">**OPOS-Geräte**</span><span class="sxs-lookup"><span data-stu-id="72db7-109">**OPOS devices**</span></span>

-   <span data-ttu-id="72db7-110">Barcode – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="72db7-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="72db7-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="72db7-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="72db7-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="72db7-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="72db7-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="72db7-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="72db7-114">Unterschriftenauflage – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="72db7-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="72db7-115">Drucker – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="72db7-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="72db7-116">Geldlade – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="72db7-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="72db7-117">Skalieren – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="72db7-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="72db7-118">**Tastaturweiche MSR**</span><span class="sxs-lookup"><span data-stu-id="72db7-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="72db7-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="72db7-119">Magtek USB</span></span>

<span data-ttu-id="72db7-120">**Zahlungsterminal**</span><span class="sxs-lookup"><span data-stu-id="72db7-120">**Payment terminal**</span></span>

-   <span data-ttu-id="72db7-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="72db7-121">Equinox L3500</span></span>
-   <span data-ttu-id="72db7-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="72db7-122">Verifone MX925</span></span>

<span data-ttu-id="72db7-123">**Netzwerkgeräte**</span><span class="sxs-lookup"><span data-stu-id="72db7-123">**Network devices**</span></span>

-   <span data-ttu-id="72db7-124">Drucker – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="72db7-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="72db7-125">Geldlade– APG Atwood</span><span class="sxs-lookup"><span data-stu-id="72db7-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="72db7-126">Zahlungsterminal – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="72db7-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="72db7-127">**MPOS direkt nur IPC**</span><span class="sxs-lookup"><span data-stu-id="72db7-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="72db7-128">Strichcode – Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="72db7-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="72db7-129">MSR – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="72db7-129">MSR – Magtek PN - 21073075</span></span>





