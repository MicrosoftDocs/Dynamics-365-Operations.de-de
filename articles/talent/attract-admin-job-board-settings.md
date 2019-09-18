---
title: Broadbean-Integration in Microsoft Dynamics 365 for Talent - Attract aktivieren
description: In diesem Thema wird erläutert, wie Microsoft Dynamics 365 for Talent - Attract konfiguriert wird um Einzelvorgänge an externe Stellenbörsen wie Broadbean zu buchen.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2334c2bd0edccf3000f8d91651afafd4619ad0b8
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739678"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="0a406-103">Broadbean-Integration aktivieren</span><span class="sxs-lookup"><span data-stu-id="0a406-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0a406-104">Sie möchten die offenen Stellen für möglichst viele qualifizierten Kandidaten bekannt machen.</span><span class="sxs-lookup"><span data-stu-id="0a406-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="0a406-105">Stellenportale wie Broadbean helfen Ihnen dabei</span><span class="sxs-lookup"><span data-stu-id="0a406-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="0a406-106">Microsoft Dynamics 365 for Talent: Mit Attract können Sie nun Stellen auf Broadbean veröffentlichen und Microsoft ist ständig daran, neue Angebote in diesem Bereich bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0a406-106">Microsoft Dynamics 365 for Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="0a406-107">Um Stellen an externen Standorten zu buchen, müssen Sie das [Umfassende Einstellungsadd-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) haben.</span><span class="sxs-lookup"><span data-stu-id="0a406-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="0a406-108">Um Stellen bei Broadbean über Attract zu veröffentlichen, müssen Sie ein Broadbean-Abonnement haben.</span><span class="sxs-lookup"><span data-stu-id="0a406-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="0a406-109">Diese Funktion befindet sich derzeit in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="0a406-109">This feature is currently in preview.</span></span> <span data-ttu-id="0a406-110">Wenn Sie sie ausprobieren möchten, müssen Sie [sie in den Attract-Administratoreinstellungen aktivieren](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) auf.</span><span class="sxs-lookup"><span data-stu-id="0a406-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="0a406-111">Broadbean-Integration konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0a406-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="0a406-112">Bei Attract als Administrator anmelden.</span><span class="sxs-lookup"><span data-stu-id="0a406-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="0a406-113">Wählen Sie die Schaltfläche **Einstellungen** (das Rad-Symbol) in der rechten oberen Ecke der Seite aus, und wählen Sie dann **Administratorcenter**.</span><span class="sxs-lookup"><span data-stu-id="0a406-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="0a406-114">Broadbean kontaktieren und die Informationen in den Feldern **Benutzername**, **Client-ID** und **Verschlüsselungs-Token** eingeben.</span><span class="sxs-lookup"><span data-stu-id="0a406-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="0a406-115">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="0a406-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="0a406-116">Ihre Broadbean-Anmeldeinformationen sind vertraulich.</span><span class="sxs-lookup"><span data-stu-id="0a406-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="0a406-117">Daher müssen Sie diese sicher und verantwortungsvoll speichern.</span><span class="sxs-lookup"><span data-stu-id="0a406-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="0a406-118">Alle, die eine Administratorrolle in Attract haben, können diese Anmeldeinformationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a406-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="0a406-119">Microsoft und Attract sind nicht involviert beim Erstellen und Verwalten dieser Werte.</span><span class="sxs-lookup"><span data-stu-id="0a406-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="0a406-120">Es ist Ihre Verantwortung, sie in Attract auf dem neuesten Stand zu halten und mit Broabean zusammen zu arbeiten, um Probleme zu beheben, die Ihre Anmeldeinformationen umfassen.</span><span class="sxs-lookup"><span data-stu-id="0a406-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
