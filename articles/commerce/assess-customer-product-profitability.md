---
title: Debitoren- und Produktrentabilität bewerten
description: In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblicke in die Rentabilität der Debitoren und Produkte basierend auf Ihrer Dynamics 365 Commerce-Daten zu erhalten.
author: ashishmsft
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 80a2f38f2b3f039b17556116d6aea738faa1db50
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797328"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="fa6ed-103">Debitoren- und Produktrentabilität bewerten</span><span class="sxs-lookup"><span data-stu-id="fa6ed-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa6ed-104">In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblicke in die Rentabilität der Debitoren und Produkte basierend auf Ihrer Dynamics 365 Commerce-Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fa6ed-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="fa6ed-105">Im Rahmen von Commerce können Benutzer die Rentabilität für die wichtigsten Debitoren (10 bis 100) auf unterschiedlichen Ebenen der Organisationshierarchie auf Grundlage einer der folgenden Kriterien überprüfen:</span><span class="sxs-lookup"><span data-stu-id="fa6ed-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="fa6ed-106">Verkaufsbetrag</span><span class="sxs-lookup"><span data-stu-id="fa6ed-106">Sales amount</span></span>
- <span data-ttu-id="fa6ed-107">Menge</span><span class="sxs-lookup"><span data-stu-id="fa6ed-107">Quantity</span></span>
- <span data-ttu-id="fa6ed-108">Bruttogewinnspanne</span><span class="sxs-lookup"><span data-stu-id="fa6ed-108">Gross profit margin</span></span>
- <span data-ttu-id="fa6ed-109">Gewinnspanne (Prozent)</span><span class="sxs-lookup"><span data-stu-id="fa6ed-109">Margin percentage</span></span>

<span data-ttu-id="fa6ed-110">Für diese Bewertung können Sie den vordefinierten Bericht **Wichtigste Debitoren** verwenden, den Sie an folgenden Stellen öffnen können:</span><span class="sxs-lookup"><span data-stu-id="fa6ed-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="fa6ed-111">**Shopverwaltung**-Arbeitsbereich &gt; **Retail and Commerce** &gt; **Kanäle** &gt; **Shopverwaltung** &gt; **Berichte** &gt; **Bericht 'Wichtigste Debitoren'**</span><span class="sxs-lookup"><span data-stu-id="fa6ed-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="fa6ed-112">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel und Handel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Wichtigste Debitoren**</span><span class="sxs-lookup"><span data-stu-id="fa6ed-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="fa6ed-113">Auf ähnliche weise können Benutzer die Rentabilität für die besten Produkte (10 bis 100) auf unterschiedlichen Ebenen der Organisationshierarchie auf Grundlage eines der folgenden Kriterien überprüfen:</span><span class="sxs-lookup"><span data-stu-id="fa6ed-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="fa6ed-114">Verkaufsbetrag</span><span class="sxs-lookup"><span data-stu-id="fa6ed-114">Sales amount</span></span>
- <span data-ttu-id="fa6ed-115">Menge</span><span class="sxs-lookup"><span data-stu-id="fa6ed-115">Quantity</span></span>
- <span data-ttu-id="fa6ed-116">Bruttogewinnspanne</span><span class="sxs-lookup"><span data-stu-id="fa6ed-116">Gross profit margin</span></span>
- <span data-ttu-id="fa6ed-117">Gewinnspanne (Prozent)</span><span class="sxs-lookup"><span data-stu-id="fa6ed-117">Margin percentage</span></span>

<span data-ttu-id="fa6ed-118">Für diese Bewertung können Sie den vordefinierten **Bericht über Top-Produkte** verwenden, den Sie an folgenden Stellen öffnen können:</span><span class="sxs-lookup"><span data-stu-id="fa6ed-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="fa6ed-119">**Shopverwaltung**-Arbeitsbereich &gt; **Retail and Commerce** &gt; **Kanäle** &gt; **Shopverwaltung** &gt; **Berichte** &gt; **Bericht „Wichtigste Produkte”**</span><span class="sxs-lookup"><span data-stu-id="fa6ed-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="fa6ed-120">**Kategorie- und Produktverwaltung**-Arbeitsbereich &gt; **Einzelhandel und Handel** &gt; **Produkte und Kategorien** &gt; **Shopverwaltung** &gt; **Berichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="fa6ed-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="fa6ed-121">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel und Handel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht über Top-Produkte**</span><span class="sxs-lookup"><span data-stu-id="fa6ed-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]