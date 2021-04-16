---
title: Abonnieren zum Verwenden von Bewertungen und Prüfungen
description: In diesem Thema wird erläutert, wie Sie sich für die Verwendung von Bewertungen und Prüfungen auf Ihrer Microsoft Dynamics 365 Commerce-Website anmelden.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9e3f2a17e182c0e3efc8b90380eff74f350c3278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804648"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="e6d70-103">Nutzung von Bewertungen und Prüfungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="e6d70-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6d70-104">In diesem Thema wird erläutert, wie Sie sich für die Verwendung von Bewertungen und Prüfungen auf Ihrer Microsoft Dynamics 365 Commerce-Website anmelden.</span><span class="sxs-lookup"><span data-stu-id="e6d70-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="e6d70-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e6d70-105">Overview</span></span>

<span data-ttu-id="e6d70-106">Die Bewertungs- und Prüfungslösung ist eine Omnikanal-Lösung, die Sie in Dynamics 365 Commerce zur Verfügung stellen können, indem Sie Microsoft Dynamics Lifecycle Services (LCS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6d70-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e6d70-107">LCS ist ein Verwaltungsportal, über das Einzelhändler ihre Umgebungen von der Bereitstellung bis zur Außerbetriebnahme verwalten.</span><span class="sxs-lookup"><span data-stu-id="e6d70-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="e6d70-108">Wenn Sie die Bewertungs- und Überprüfungslösung auf Ihrer Commerce-Website verwenden möchten, müssen Sie sich für Bewertungen und Überprüfungen während der Bereitstellung Ihrer E-Commerce-Website auf anmelden Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e6d70-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="e6d70-109">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="e6d70-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="e6d70-110">Führen Sie die folgenden Schritte aus, um die Verwendung von Bewertungen und Prüfungen auf Ihrer Site zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e6d70-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="e6d70-111">Befolgen Sie die Schritte in [Eine neue E-Commerce-Webseite bereitstellen](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="e6d70-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="e6d70-112">Navigieren Sie, während Sie sich noch im LCS befinden, zu **Einrichtung der Retail-Bereitstellung \> Andere Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="e6d70-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="e6d70-113">Legen Sie die Option **Bewertungs- und Prüfungsdienst aktivieren** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="e6d70-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="e6d70-114">Geben Sie im Feld **AAD-Sicherheitsgruppe für Bewertungs- und Prüfungsmoderator** die ID der Microsoft Azure Active Directory-Sicherheitsgruppe (Azure AD) ein, die Bewertungs- und Prüfungsmoderatoren enthält.</span><span class="sxs-lookup"><span data-stu-id="e6d70-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Abonnieren zum Verwenden von Bewertungen und Prüfungen](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="e6d70-116">Schließen Sie den E-Commerce-Initialisierungsprozess ab.</span><span class="sxs-lookup"><span data-stu-id="e6d70-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="e6d70-117">Wenn Sie ein bestehender Dynamics 365 Commerce Kunde sind, der bereits eine E-Commerce-Website bereitgestellt hat, ohne sich für Bewertungen und Beurteilungen entschieden zu haben, und der jetzt Bewertungen und Beurteilungen vom Dynamics 365 CommercePaket verwenden möchte, sendet bitte eine Serviceanfrage.</span><span class="sxs-lookup"><span data-stu-id="e6d70-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="e6d70-118">Informationen zum Senden einer Serviceanforderung finden Sie unter [Prozess zur Übermittlung von Serviceanfragen ](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e6d70-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e6d70-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e6d70-119">Additional resources</span></span>

[<span data-ttu-id="e6d70-120">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="e6d70-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="e6d70-121">Verwalten von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="e6d70-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="e6d70-122">Konfigurieren von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="e6d70-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="e6d70-123">Synchronisieren von Produktbewertungen in Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e6d70-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]