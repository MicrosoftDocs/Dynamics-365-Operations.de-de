---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Finance
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127976"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="40e17-103">Entfernte oder veraltete Funktionen in Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="40e17-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40e17-104">In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="40e17-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="40e17-105">Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40e17-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="40e17-106">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="40e17-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="40e17-107">Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="40e17-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="40e17-108">Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="40e17-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="40e17-109">Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="40e17-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="40e17-110">Entfernte oder veraltete Funktionen in Finance Release 10.0.12</span><span class="sxs-lookup"><span data-stu-id="40e17-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="40e17-111">Polnische SSRS-Berichte: Ausgangssteuer, Vorsteuer, EU-Zusammenfassung des Umsatzsteuerregisters – Funktionsreferenz PL-00014</span><span class="sxs-lookup"><span data-stu-id="40e17-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="40e17-112">**Grund für veralteten Zustand/Entfernung**</span><span class="sxs-lookup"><span data-stu-id="40e17-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="40e17-113">Nicht rechtlich obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="40e17-113">Not legally required.</span></span>  |
| <span data-ttu-id="40e17-114">**Ersetzt durch eine andere Funktion?**</span><span class="sxs-lookup"><span data-stu-id="40e17-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="40e17-115">Ja (Excel-Format für Standard-Auditdatei mit Umsatzsteuererklärung – JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="40e17-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="40e17-116">**Betroffene Produktbereiche**</span><span class="sxs-lookup"><span data-stu-id="40e17-116">**Product areas affected**</span></span>         | <span data-ttu-id="40e17-117">Bewerbung</span><span class="sxs-lookup"><span data-stu-id="40e17-117">Application</span></span> |
| <span data-ttu-id="40e17-118">**Bereitstellungsoption**</span><span class="sxs-lookup"><span data-stu-id="40e17-118">**Deployment option**</span></span>              | <span data-ttu-id="40e17-119">Alle</span><span class="sxs-lookup"><span data-stu-id="40e17-119">All</span></span> |
| <span data-ttu-id="40e17-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="40e17-120">**Status**</span></span>                         | <span data-ttu-id="40e17-121">Veraltet: Bis zum 1. Juli 2021 planen wir, die SSRS-Berichte nicht mehr zu unterstützen: **Ausgangssteuerregister, Kaufsteuerregister, EU-Zusammenfassung des Umsatzsteuerregisters – Funktionsreferenz PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="40e17-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="40e17-122">Stattdessen wird ein Beispiel für ein Excel-Format für eine Standard-Auditdatei mit Umsatzsteuererklärung (JPK_VDEK) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="40e17-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="40e17-123">Entfernte oder veraltete Funktionen in Finance Release 10.0.7</span><span class="sxs-lookup"><span data-stu-id="40e17-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="40e17-124">Das Dialogfeld für die Änderung von Workflow-Anforderungen enthält nicht mehr die Dropdown-Liste für die Benutzerauswahl.</span><span class="sxs-lookup"><span data-stu-id="40e17-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="40e17-125">**Grund für veralteten Zustand/Entfernung**</span><span class="sxs-lookup"><span data-stu-id="40e17-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="40e17-126">Geändert in die Funktion mit Kontogruppenauswahl.</span><span class="sxs-lookup"><span data-stu-id="40e17-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="40e17-127">**Ersetzt durch eine andere Funktion?**</span><span class="sxs-lookup"><span data-stu-id="40e17-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="40e17-128">Ja</span><span class="sxs-lookup"><span data-stu-id="40e17-128">Yes</span></span> |
| <span data-ttu-id="40e17-129">**Betroffene Produktbereiche**</span><span class="sxs-lookup"><span data-stu-id="40e17-129">**Product areas affected**</span></span>         | <span data-ttu-id="40e17-130">Workflow</span><span class="sxs-lookup"><span data-stu-id="40e17-130">Workflow</span></span> |
| <span data-ttu-id="40e17-131">**Bereitstellungsoption**</span><span class="sxs-lookup"><span data-stu-id="40e17-131">**Deployment option**</span></span>              | <span data-ttu-id="40e17-132">Alle</span><span class="sxs-lookup"><span data-stu-id="40e17-132">All</span></span> |
| <span data-ttu-id="40e17-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="40e17-133">**Status**</span></span>                         | <span data-ttu-id="40e17-134">Veraltet: Wir planen, die chinesischen Belegtypen-Einstellungen ohne Kontogruppenauswahl bis zum 1. Dezember 2020 nicht mehr zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="40e17-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="40e17-135">Zusätzliche Details für das neue Design in [Was ist neu in 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="40e17-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="40e17-136">Frühere Ankündigungen über entfernte oder veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="40e17-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="40e17-137">Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="40e17-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
