---
title: Abonnieren zum Verwenden von Bewertungen und Prüfungen
description: In diesem Thema wird erläutert, wie Sie sich für die Verwendung von Bewertungen und Prüfungen auf Ihrer Microsoft Dynamics 365 Commerce-Site anmelden.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697979"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="c1dc4-103">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="c1dc4-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c1dc4-104">In diesem Thema wird erläutert, wie Sie sich für die Verwendung von Bewertungen und Prüfungen auf Ihrer Microsoft Dynamics 365 Commerce-Site anmelden.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="c1dc4-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="c1dc4-105">Overview</span></span>

<span data-ttu-id="c1dc4-106">Die Bewertungs- und Prüfungslösung ist eine Mehrkanal-Lösung, die Sie in Dynamics 365 Commerce zur Verfügung stellen können, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c1dc4-107">LCS ist ein Verwaltungsportal, über das Einzelhändler ihre Umgebungen von der Bereitstellung bis zur Außerbetriebnahme verwalten.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="c1dc4-108">Wenn Sie die Bewertungs- und Prüfungslösung auf Ihrer Commerce-Website verwenden möchten, müssen Sie sich zuerst anmelden.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="c1dc4-109">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="c1dc4-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="c1dc4-110">Führen Sie die folgenden Schritte aus, um die Verwendung von Bewertungen und Prüfungen auf Ihrer Site zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="c1dc4-111">Befolgen Sie die Schritte in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="c1dc4-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="c1dc4-112">Navigieren Sie, während Sie sich noch im LCS befinden, zu **Einrichtung der Retail-Bereitstellung \> Andere Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="c1dc4-113">Legen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="c1dc4-114">Geben Sie im Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ID der Microsoft Azure Active Directory-Sicherheitsgruppe (Azure AD) ein, die Bewertungs- und Prüfungsmoderatoren enthält.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Abonnieren zum Verwenden von Bewertungen und Prüfungen](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="c1dc4-116">Schließen Sie den E-Commerce-Initialisierungsprozess ab.</span><span class="sxs-lookup"><span data-stu-id="c1dc4-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1dc4-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c1dc4-117">Additional resources</span></span>

[<span data-ttu-id="c1dc4-118">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="c1dc4-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c1dc4-119">Verwalten von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="c1dc4-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="c1dc4-120">Konfigurieren von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="c1dc4-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="c1dc4-121">Synchronisieren von Produktbewertungen in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="c1dc4-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
