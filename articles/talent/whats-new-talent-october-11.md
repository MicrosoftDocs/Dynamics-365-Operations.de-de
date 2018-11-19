---
title: "Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (15. Oktober 2018)"
description: "In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind."
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 1d48bc4bad795611ce322b5f09b78886a50c415c
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-15-2018"></a><span data-ttu-id="d7a67-103">Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (15. Oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="d7a67-103">What's new or changed in Dynamics 365 for Talent Core HR (October 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d7a67-104">**Build 8.1.1056**</span><span class="sxs-lookup"><span data-stu-id="d7a67-104">**Build 8.1.1056**</span></span>

<span data-ttu-id="d7a67-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="d7a67-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="d7a67-106">Änderungen</span><span class="sxs-lookup"><span data-stu-id="d7a67-106">Changes</span></span>
<span data-ttu-id="d7a67-107">Neben verschiedenen Korrekturen wurden folgende Aktualisierungen in dieser Version vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="d7a67-107">In addition to miscellanous fixes, the following updates have been made in this release:</span></span>
- <span data-ttu-id="d7a67-108">Letzter gearbeiteter Tag legt nun fest, wenn ein Beschäftigungs- Enddatum fest.</span><span class="sxs-lookup"><span data-stu-id="d7a67-108">Last Day worked now set when hiring or setting an employment end date.</span></span>
- <span data-ttu-id="d7a67-109">US-Kompatibilitätsreferenzen wurden entfernt bei nicht US-Unternehmen (ADA, und I9).</span><span class="sxs-lookup"><span data-stu-id="d7a67-109">US compliance references removed when in non US companies (ACA, ADA, and I9).</span></span>
- <span data-ttu-id="d7a67-110">Ungültige Datumsangaben (1/1/1900) werden nun auf Analyseseiten ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="d7a67-110">Invalid dates (1/1/1900) are now hidden on analytics pages.</span></span>

## <a name="known-issue"></a><span data-ttu-id="d7a67-111">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="d7a67-111">Known issue</span></span>

<span data-ttu-id="d7a67-112">**Problem:** Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d7a67-112">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="d7a67-113">Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d7a67-113">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="d7a67-114">(Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)</span><span class="sxs-lookup"><span data-stu-id="d7a67-114">(This issue will be fixed in the next platform update.)</span></span>

