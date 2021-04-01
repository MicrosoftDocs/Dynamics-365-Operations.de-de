---
title: Überwachen von Verkaufs- und erstellen Sie ein Leistung
description: Sie können die Verkaufs- und Margenleistung mit Dynamics 365 Commerce in Echtzeit überwachen.
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
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4d8d6a99e0ed3f331051d504e3a1ce2bd403cc17
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251306"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="4aa29-103">Überwachen der Verkaufs- und Margenleistung</span><span class="sxs-lookup"><span data-stu-id="4aa29-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4aa29-104">Sie können die Verkaufs- und Margenleistung mit Dynamics 365 Commerce in Echtzeit überwachen.</span><span class="sxs-lookup"><span data-stu-id="4aa29-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4aa29-105">Im Rahmen von Commerce können Benutzer die Verkaufs- und Margenleistung in Echtzeit auf unterschiedlichen Ebenen der Organisationshierarchie für die folgenden Dimensionen überwachen:</span><span class="sxs-lookup"><span data-stu-id="4aa29-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="4aa29-106">Produkte</span><span class="sxs-lookup"><span data-stu-id="4aa29-106">Products</span></span>
- <span data-ttu-id="4aa29-107">Kategorien</span><span class="sxs-lookup"><span data-stu-id="4aa29-107">Categories</span></span>
- <span data-ttu-id="4aa29-108">Rabatte</span><span class="sxs-lookup"><span data-stu-id="4aa29-108">Discounts</span></span>
- <span data-ttu-id="4aa29-109">Jahre als Zeitraum</span><span class="sxs-lookup"><span data-stu-id="4aa29-109">Years as time period</span></span>
- <span data-ttu-id="4aa29-110">Register/Terminals</span><span class="sxs-lookup"><span data-stu-id="4aa29-110">Registers/terminals</span></span>
- <span data-ttu-id="4aa29-111">Mitarbeiter/Angestellte</span><span class="sxs-lookup"><span data-stu-id="4aa29-111">Staff/employees</span></span>
- <span data-ttu-id="4aa29-112">Kunden</span><span class="sxs-lookup"><span data-stu-id="4aa29-112">Customers</span></span>
- <span data-ttu-id="4aa29-113">Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="4aa29-113">Operating units</span></span>

<span data-ttu-id="4aa29-114">Darüber hinaus können die Benutzer mit zwei eindeutigen Berichten mit der hierarchischen Rasterstrukturierung den Verkauf und die Gewinnspanne vom obersten Konto aus für die einzelnen untergeordneten Knoten der Kategorie in der standardmäßigen Produktkategoriehierarchie detailliert darstellen.</span><span class="sxs-lookup"><span data-stu-id="4aa29-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="4aa29-115">Die Benutzer können von der obersten Organisationseinheit aus einen einzelnen Kanal in der Organisationshierarchie detailliert darstellen, die als standardmäßige Organisationshierarchie für die Berichterstellungshierarchie im Einzelhandel definiert wird.</span><span class="sxs-lookup"><span data-stu-id="4aa29-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="4aa29-116">Sie können die Berichte über die folgenden Orten öffnen:</span><span class="sxs-lookup"><span data-stu-id="4aa29-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="4aa29-117">**Shopverwaltung**-Arbeitsbereich &gt; **Einzelhandel und Handel** &gt; **Channels** &gt; **Shopverwaltung** &gt; **Berichte**</span><span class="sxs-lookup"><span data-stu-id="4aa29-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="4aa29-118">**Kategorie- und Produktverwaltung**-Arbeitsbereich &gt; **Einzelhandel und Handel** &gt; **Produkt und Kategorien** &gt; **Shop Verwaltung** &gt; **Berichte**</span><span class="sxs-lookup"><span data-stu-id="4aa29-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="4aa29-119">**Verwaltung von Preisen und Rabatten**-Arbeitsbereich &gt; **Einzelhandel und Handel** &gt; **Preise und Rabatte** &gt; **Shop Verwaltung** &gt; **Berichte**</span><span class="sxs-lookup"><span data-stu-id="4aa29-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="4aa29-120">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel und Handel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte**</span><span class="sxs-lookup"><span data-stu-id="4aa29-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]