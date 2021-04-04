---
title: Den Storefront-Zugriff während des Testens oder der Entwicklung beschränken
description: In diesem Thema wird erläutert, wie Sie beim Durchführen interner Tests oder Entwicklungen den Zugriff auf eine Microsoft Dynamics 365 Commerce-Storefront beschränken.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585343"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="c5b93-103">Den Storefront-Zugriff während des Testens oder der Entwicklung beschränken</span><span class="sxs-lookup"><span data-stu-id="c5b93-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5b93-104">In diesem Thema wird erläutert, wie Sie beim Durchführen interner Tests oder Entwicklungen den Zugriff auf eine Microsoft Dynamics 365 Commerce-Storefront beschränken.</span><span class="sxs-lookup"><span data-stu-id="c5b93-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="c5b93-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5b93-105">Description</span></span>

<span data-ttu-id="c5b93-106">Sie möchten möglicherweise bei internen Tests oder aktiven Entwicklungen den Zugriff auf Ihre Website einschränken, um zu verhindern, dass externe Benutzer auf die veröffentlichten Storefront-Seiten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c5b93-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5b93-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="c5b93-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="c5b93-108">Azure AD B2C mithilfe von Standardbenutzerflows einrichten</span><span class="sxs-lookup"><span data-stu-id="c5b93-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="c5b93-109">Informationen zum Konfigurieren von Azure Active Directory B2C (Azure AD B2C) für Ihre E-Commerce-Website siehe [Einen B2C-Mandanten in Commerce einrichten](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="c5b93-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="c5b93-110">Den Benutzerzugriff auf Storefront-Seiten beschränken und die Erstellung neuer Benutzer sperren</span><span class="sxs-lookup"><span data-stu-id="c5b93-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="c5b93-111">Befolgen Sie die folgenden Schritte, um den Benutzerzugriff auf Storefront-Seiten im Commerce-Website-Generator zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="c5b93-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c5b93-112">Rufen Sie die Website auf.</span><span class="sxs-lookup"><span data-stu-id="c5b93-112">Go to your site.</span></span>
1. <span data-ttu-id="c5b93-113">Wählen Sie unter **Seiten** die Seite aus, für die der Benutzerzugriff beschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5b93-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="c5b93-114">Wählen Sie das Modul oder den Fragmentslot und anschließend **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="c5b93-115">Wählen Sie im Eigenschaftenbereich die Option **Anmeldung erforderlich?** und anschließend **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c5b93-116">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-116">Select **Publish**.</span></span>

<span data-ttu-id="c5b93-117">Befolgen Sie diese Schritte, um die Erstellung neuer Benutzer in Azure AD zu sperren.</span><span class="sxs-lookup"><span data-stu-id="c5b93-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="c5b93-118">Gehen Sie zu [Azure-Portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="c5b93-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="c5b93-119">Wählen Sie die Azure AD B2C-Anwendung aus, die Sie für Ihren Website-Zugriff erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c5b93-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="c5b93-120">Wählen Sie im linken Navigationsbereich **Benutzerflows** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="c5b93-121">Wählen Sie oben auf der Seite **Benutzerflows** die Option **Neuer Benutzerflow** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="c5b93-122">Wählen Sie auf der Seite **Benutzerflowtyp auswählen** die Option **Vorschau** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="c5b93-123">Wählen Sie in der Mitte der Seite die Option **Anmelden v2** aus.</span><span class="sxs-lookup"><span data-stu-id="c5b93-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="c5b93-124">Befolgen Sie dann die Schritte in [Einen B2C-Mandanten in Commerce einrichten](../set-up-b2c-tenant.md), um den Flow als Standardbenutzerflow Ihrer Website für Azure AD B2C während des Testens oder der Entwicklung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c5b93-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5b93-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5b93-125">Additional resources</span></span>

[<span data-ttu-id="c5b93-126">B2C-Mandanten in Commerce einrichten</span><span class="sxs-lookup"><span data-stu-id="c5b93-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="c5b93-127">Angepasste Seiten für die Benutzeranmeldung einrichten</span><span class="sxs-lookup"><span data-stu-id="c5b93-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
