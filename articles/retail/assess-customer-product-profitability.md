---
title: Debitoren- und Produktrentabilität bewerten
description: In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblicke in die Rentabilität der Debitoren und Produkte basierend auf Ihrer Microsoft Dynamics 365 for Retail-Daten zu erhalten.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326008"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="53a42-103">Debitoren- und Produktrentabilität bewerten</span><span class="sxs-lookup"><span data-stu-id="53a42-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53a42-104">In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblicke in die Rentabilität der Debitoren und Produkte basierend auf Ihrer Microsoft Dynamics 365 for Retail-Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="53a42-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="53a42-105">Im Rahmen von Dynamics 365 for Retail können Benutzer die Rentabilität für die wichtigsten Debitoren (10 bis 100) auf unterschiedlichen Ebenen der Organisationshierarchie auf Grundlage einer der folgenden Kriterien überprüfen:</span><span class="sxs-lookup"><span data-stu-id="53a42-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="53a42-106">Verkaufsbetrag</span><span class="sxs-lookup"><span data-stu-id="53a42-106">Sales amount</span></span>
- <span data-ttu-id="53a42-107">Menge</span><span class="sxs-lookup"><span data-stu-id="53a42-107">Quantity</span></span>
- <span data-ttu-id="53a42-108">Bruttogewinnspanne</span><span class="sxs-lookup"><span data-stu-id="53a42-108">Gross profit margin</span></span>
- <span data-ttu-id="53a42-109">Gewinnspanne (Prozent)</span><span class="sxs-lookup"><span data-stu-id="53a42-109">Margin percentage</span></span>

<span data-ttu-id="53a42-110">Für diese Bewertung können Sie den vordefinierten Bericht **Wichtigste Debitoren** verwenden, den Sie an folgenden Stellen öffnen können:</span><span class="sxs-lookup"><span data-stu-id="53a42-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="53a42-111">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht 'Wichtigste Debitoren'**</span><span class="sxs-lookup"><span data-stu-id="53a42-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="53a42-112">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht 'Wichtigste Debitoren'**</span><span class="sxs-lookup"><span data-stu-id="53a42-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="53a42-113">Auf ähnliche weise können Benutzer die Rentabilität für die besten Produkte (10 bis 100) auf unterschiedlichen Ebenen der Organisationshierarchie auf Grundlage eines der folgenden Kriterien überprüfen:</span><span class="sxs-lookup"><span data-stu-id="53a42-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="53a42-114">Verkaufsbetrag</span><span class="sxs-lookup"><span data-stu-id="53a42-114">Sales amount</span></span>
- <span data-ttu-id="53a42-115">Menge</span><span class="sxs-lookup"><span data-stu-id="53a42-115">Quantity</span></span>
- <span data-ttu-id="53a42-116">Bruttogewinnspanne</span><span class="sxs-lookup"><span data-stu-id="53a42-116">Gross profit margin</span></span>
- <span data-ttu-id="53a42-117">Gewinnspanne (Prozent)</span><span class="sxs-lookup"><span data-stu-id="53a42-117">Margin percentage</span></span>

<span data-ttu-id="53a42-118">Für diese Bewertung können Sie den vordefinierten **Bericht über Top-Produkte** verwenden, den Sie an folgenden Stellen öffnen können:</span><span class="sxs-lookup"><span data-stu-id="53a42-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="53a42-119">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="53a42-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="53a42-120">**Kategorie- und Produktverwaltung**-Arbeitsbereich &gt; **Einzelhandel und Handel** &gt; **Produkte und Kategorien** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="53a42-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="53a42-121">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="53a42-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
