---
title: "Debitoren- und Produktrentabilität bewerten"
description: "In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblick zur Rentabilität der Debitoren und Produkte basierend auf Ihrer Microsoft Dynamics 365 for Retail-Daten zu erhalten."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c603c065d57f08772c3b25cab8437cb7848e5fcb
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="cef30-103">Debitoren- und Produktrentabilität bewerten</span><span class="sxs-lookup"><span data-stu-id="cef30-103">Assess customer and product profitability</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="cef30-104">In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblick zur Rentabilität der Debitoren und Produkte basierend auf Ihrer Microsoft Dynamics 365 for Retail-Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cef30-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="cef30-105">Im Rahmen von Microsoft Dynamics 365 for Retail können Benutzer die Rentabilität für die wichtigsten Debitoren (10 bis 100) auf unterschiedlichen Ebenen der Organisationshierarchie auf Grundlage eines der folgenden Kriterien überprüfen:</span><span class="sxs-lookup"><span data-stu-id="cef30-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="cef30-106">Verkaufsbetrag</span><span class="sxs-lookup"><span data-stu-id="cef30-106">Sales amount</span></span>
-   <span data-ttu-id="cef30-107">Menge</span><span class="sxs-lookup"><span data-stu-id="cef30-107">Quantity</span></span>
-   <span data-ttu-id="cef30-108">Bruttogewinnspanne</span><span class="sxs-lookup"><span data-stu-id="cef30-108">Gross profit margin</span></span>
-   <span data-ttu-id="cef30-109">Gewinnspanne (Prozent)</span><span class="sxs-lookup"><span data-stu-id="cef30-109">Margin percentage</span></span>

<span data-ttu-id="cef30-110">Für diese Bewertung können Sie den vordefinierten Bericht **Wichtigste Debitoren** verwenden, den Sie an folgenden Stellen öffnen können:</span><span class="sxs-lookup"><span data-stu-id="cef30-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="cef30-111">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht 'Wichtigste Debitoren'**</span><span class="sxs-lookup"><span data-stu-id="cef30-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="cef30-112">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht 'Wichtigste Debitoren'**</span><span class="sxs-lookup"><span data-stu-id="cef30-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="cef30-113">Auf ähnliche weise können Benutzer die Rentabilität für die besten Produkte (10 bis 100) auf unterschiedlichen Ebenen der Organisationshierarchie auf Grundlage eines der folgenden Kriterien überprüfen:</span><span class="sxs-lookup"><span data-stu-id="cef30-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="cef30-114">Verkaufsbetrag</span><span class="sxs-lookup"><span data-stu-id="cef30-114">Sales amount</span></span>
-   <span data-ttu-id="cef30-115">Menge</span><span class="sxs-lookup"><span data-stu-id="cef30-115">Quantity</span></span>
-   <span data-ttu-id="cef30-116">Bruttogewinnspanne</span><span class="sxs-lookup"><span data-stu-id="cef30-116">Gross profit margin</span></span>
-   <span data-ttu-id="cef30-117">Gewinnspanne (Prozent)</span><span class="sxs-lookup"><span data-stu-id="cef30-117">Margin percentage</span></span>

<span data-ttu-id="cef30-118">Für diese Bewertung können Sie den vordefinierten **Bericht über Top-Produkte** verwenden, den Sie an folgenden Stellen öffnen können:</span><span class="sxs-lookup"><span data-stu-id="cef30-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="cef30-119">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="cef30-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="cef30-120">**Kategorie- und Produktverwaltung**-Arbeitsbereich &gt; **Einzelhandel und Handel** &gt; **Produkte und Kategorien** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="cef30-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="cef30-121">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="cef30-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>




