---
title: Überwachen von Verkaufs- und erstellen Sie ein Leistung
description: Sie können die Verkaufs- und Margenleistung mit Dynamics 365 Retail in Echtzeit überwachen.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 46ecefdd15a3a208588aaf630571764047464cdb
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018063"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="9e706-103">Überwachen der Verkaufs- und Margenleistung</span><span class="sxs-lookup"><span data-stu-id="9e706-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9e706-104">Sie können die Verkaufs- und Margenleistung mit Dynamics 365 Retail in Echtzeit überwachen.</span><span class="sxs-lookup"><span data-stu-id="9e706-104">You can monitor sales and margin performance in real time using Dynamics 365 Retail.</span></span>

<span data-ttu-id="9e706-105">Im Rahmen von Retail können Benutzer die Verkaufs- und Margenleistung in Echtzeit auf unterschiedlichen Ebenen der Organisationshierarchie für die folgenden Dimensionen überwachen:</span><span class="sxs-lookup"><span data-stu-id="9e706-105">As part of Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="9e706-106">Produkte</span><span class="sxs-lookup"><span data-stu-id="9e706-106">Products</span></span>
- <span data-ttu-id="9e706-107">Kategorien</span><span class="sxs-lookup"><span data-stu-id="9e706-107">Categories</span></span>
- <span data-ttu-id="9e706-108">Rabatte</span><span class="sxs-lookup"><span data-stu-id="9e706-108">Discounts</span></span>
- <span data-ttu-id="9e706-109">Jahre als Zeitraum</span><span class="sxs-lookup"><span data-stu-id="9e706-109">Years as time period</span></span>
- <span data-ttu-id="9e706-110">Register/Terminals</span><span class="sxs-lookup"><span data-stu-id="9e706-110">Registers/terminals</span></span>
- <span data-ttu-id="9e706-111">Mitarbeiter/Angestellte</span><span class="sxs-lookup"><span data-stu-id="9e706-111">Staff/employees</span></span>
- <span data-ttu-id="9e706-112">Kunden</span><span class="sxs-lookup"><span data-stu-id="9e706-112">Customers</span></span>
- <span data-ttu-id="9e706-113">Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="9e706-113">Operating units</span></span>

<span data-ttu-id="9e706-114">Darüber hinaus können die Benutzer mit zwei eindeutigen Berichte mit der hierarchischen Rasterstrukturierung den Verkauf und die Gewinnspanne vom obersten Konten aus für die einzelnen untergeordneten Knoten der Kategorie in der standardmäßigen Produktkategoriehierarchie detailliert darstellen.</span><span class="sxs-lookup"><span data-stu-id="9e706-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="9e706-115">Die Benutzer können von der obersten Organisationseinheit aus einen einzelnen Kanal in der Organisationshierarchie detailliert darstellen, die als standardmäßige Organisationshierarchie für die Berichterstellungshierarchie im Einzelhandel definiert wird.</span><span class="sxs-lookup"><span data-stu-id="9e706-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="9e706-116">Sie können die Berichte über die folgenden Orten öffnen:</span><span class="sxs-lookup"><span data-stu-id="9e706-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="9e706-117">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Retail** &gt; **Channels** &gt; **Einzelhandelsshopleitung** &gt; **Berichte**</span><span class="sxs-lookup"><span data-stu-id="9e706-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9e706-118">**Kategorie- und Produktverwaltung**-Arbeitsbereich &gt; **Retail** &gt; **Produkt und Kategorien** &gt; **Einzelhandelsshopleitung** &gt; **Berichte**</span><span class="sxs-lookup"><span data-stu-id="9e706-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9e706-119">**Verwaltung von Preisen und Rabatten**-Arbeitsbereich &gt; **Retail** &gt; **Preise und Rabatte** &gt; **Einzelhandelsshopleitung** &gt; **Berichte**</span><span class="sxs-lookup"><span data-stu-id="9e706-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="9e706-120">**Abfragen und Berichte**-Abschnitt &gt; **Retail** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte**</span><span class="sxs-lookup"><span data-stu-id="9e706-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
