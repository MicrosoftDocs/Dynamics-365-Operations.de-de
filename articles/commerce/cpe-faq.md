---
title: Dynamics 365 Commerce-Auswertungsumgebung – FAQ
description: Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Microsoft Dynamics 365 Commerce-Auswertungsumgebung.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a0c6f82432a4786f23f12122f3806c3b96a05c8f
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193593"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="83b97-103">Dynamics 365 Commerce-Evaluierungsumgebung – FAQ</span><span class="sxs-lookup"><span data-stu-id="83b97-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83b97-104">Dieses Thema enthält Antworten auf häufig gestellte Fragen zur Microsoft Dynamics 365 Commerce-Auswertungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="83b97-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="83b97-105">**Können wir die Commerce-Auswertungsumgebung als E-Commerce-Storefront für Kunden verwenden, die Retail derzeit implementieren?**</span><span class="sxs-lookup"><span data-stu-id="83b97-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="83b97-106">Nr.</span><span class="sxs-lookup"><span data-stu-id="83b97-106">No.</span></span> <span data-ttu-id="83b97-107">Die Commerce-Auswertungsumgebung dient nur zur Auswertung.</span><span class="sxs-lookup"><span data-stu-id="83b97-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="83b97-108">Wenn Sie für einen Kunden eine Umgebung benötigen, die den Einzelhandel implementiert, wenden Sie sich an Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83b97-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="83b97-109">**Kann die Commerce-Auswertungsumgebung verwendet werden, um die E-Commerce-Funktionen zusätzlich zu einer vorhandenen Anwendung/Umgebung bereitzustellen, die Retail implementiert?**</span><span class="sxs-lookup"><span data-stu-id="83b97-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="83b97-110">Nein (meistens).</span><span class="sxs-lookup"><span data-stu-id="83b97-110">No (mostly).</span></span> <span data-ttu-id="83b97-111">Die Commerce-Auswertungskomponenten sind nur für Umgebungen verfügbar, die den Konfigurationen entsprechen, die in der Anleitung zu den Voraussetzungen und der Bereitstellung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="83b97-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="83b97-112">Darüber hinaus sind die erforderlichen Basisdemodaten nicht in Umgebungen verfügbar, die mit einem Erst-Release vor 10.0.8 bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="83b97-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="83b97-113">**Welche Kosten fallen bei der Bereitstellung der Commerce-Auswertungsumgebung in Microsoft Azure über Microsoft Dynamics Lifecycle Services (LCS) an?**</span><span class="sxs-lookup"><span data-stu-id="83b97-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="83b97-114">Eine traditionelle Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce-Zentralverwaltungs-Demo-Umgebung (virtuelle Maschine \[VM\]) wird in Ihrem Azure-Abonnement gehostet.</span><span class="sxs-lookup"><span data-stu-id="83b97-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="83b97-115">Sie können den [Azure-Preisrechner](https://azure.microsoft.com/pricing/calculator/) verwenden, um die Kosten zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="83b97-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="83b97-116">Andere Komponenten wie Commerce Scale Unit, Commerce-Website-Generator und Ihre E-Commerce-Website werden als Software-as-a-Service (SaaS) verfügbar sein und von Microsoft gehostet.</span><span class="sxs-lookup"><span data-stu-id="83b97-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="83b97-117">**Welche Azure-Regionen werden derzeit in der Commerce-Auswertungsumgebung unterstützt?**</span><span class="sxs-lookup"><span data-stu-id="83b97-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="83b97-118">Die Commerce-Auswertungsumgebung kann nur in der geografischen Region Nordamerika bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="83b97-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="83b97-119">**Gibt es eine herunterladbare virtuelle Festplatte (VHD) mit der vollständigen OneBox Virtual Machine-Option (VM)?**</span><span class="sxs-lookup"><span data-stu-id="83b97-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="83b97-120">Dynamics 365 Commerce und Commerce Scale Unit sind vollständig Software as a Service (SaaS) und müssen in der Cloud gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="83b97-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="83b97-121">**Wie lange kann die Commerce-Auswertungsumgebung verwendet werden?**</span><span class="sxs-lookup"><span data-stu-id="83b97-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="83b97-122">Für die Commerce-Auswertungsumgebung gilt eine Frist von 30 Tagen ab dem Datum, an dem SaaS-Komponenten wie Commerce Scale Unit, Commerce-Website-Generator und Ihre E-Commerce-Website bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="83b97-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="83b97-123">**Kann ich das Zeitlimit für meine Commerce-Auswertungsumgebung verlängern?**</span><span class="sxs-lookup"><span data-stu-id="83b97-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="83b97-124">Die Verlängerung der Frist ist eine Ausnahme von der Norm und wird von Fall zu Fall geprüft.</span><span class="sxs-lookup"><span data-stu-id="83b97-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="83b97-125">Wenden Sie sich an Ihren Microsoft-Partner, um Unterstützung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="83b97-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83b97-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="83b97-126">Additional resources</span></span>

[<span data-ttu-id="83b97-127">Dynamics 365 Commerce-Auswertungsumgebung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="83b97-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="83b97-128">Bereitstellen einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="83b97-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="83b97-129">Konfigurieren einer Dynamics 365 Commerce-Auswertungsumgebung</span><span class="sxs-lookup"><span data-stu-id="83b97-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="83b97-130">BOPIS in einer Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="83b97-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="83b97-131">Optionale Funktionen für eine Dynamics 365 Commerce-Auswertungsumgebung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="83b97-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]