---
title: Der Anmeldelink leitet zurück zu einer E-Commerce-Website
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Anmeldelink zur E-Commerce-Website zurückleitet, anstatt zur Anmeldeseite zu wechseln.
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
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585331"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="971c0-103">Der Anmeldelink leitet zurück zu einer E-Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="971c0-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="971c0-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn ein Anmeldelink zur E-Commerce-Website zurückleitet, anstatt zur Anmeldeseite zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="971c0-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="971c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="971c0-105">Description</span></span>

<span data-ttu-id="971c0-106">Nach Konfiguration eines neuen Microsoft Azure Active Directory B2C (Azure AD B2C)-Mandanten im Commerce-Website-Generator, werden Benutzer, die den **Anmelde**-Link auswählen, zur Haupt-E-Commerce-Landingpage zurückgeleitet, ohne zur Anmeldeseite zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="971c0-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="971c0-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="971c0-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="971c0-108">Sicherstellen, dass die Antwort-URL in der Azure AD B2C-Anwendung korrekt konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="971c0-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="971c0-109">Befolgen Sie diese Schritte, um sicherzustellen, dass die Antwort-URL in der Azure AD B2C-Anwendung korrekt konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="971c0-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="971c0-110">Gehen Sie zu [Azure-Portal](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="971c0-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="971c0-111">Wählen Sie die Azure AD B2C-Anwendung aus, die Sie für Ihren Website-Zugriff erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="971c0-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="971c0-112">Wählen Sie die Anwendung aus, die Sie während der Einrichtung von Azure AD B2C erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="971c0-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="971c0-113">Vergewissern Sie sich, dass die unter **Antwort-URL** befindliche Liste Einträge sowohl für die Website-Domänen-URL als auch für die von E-Commerce generierte URL enthält, wie im Beispiel in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="971c0-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C – Antwort-URL-Einträge](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="971c0-115">Sowohl die URL der Website-Domäne als auch die von E-Commerce generierte URL müssen in einem gültigen URL-Format vorliegen, das keine führenden oder nachfolgenden Schrägstriche enthält.</span><span class="sxs-lookup"><span data-stu-id="971c0-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="971c0-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="971c0-116">Additional resources</span></span>

[<span data-ttu-id="971c0-117">Registrieren einer Webanwendung in Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="971c0-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="971c0-118">B2C-Mandanten in Commerce einrichten</span><span class="sxs-lookup"><span data-stu-id="971c0-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
