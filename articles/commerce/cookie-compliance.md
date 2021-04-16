---
title: Cookie-Compliance
description: In diesem Thema werden Überlegungen zur Einhaltung von Cookies und zu den in Microsoft Dynamics 365 Commerce enthaltenen Standardrichtlinien beschrieben.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796026"
---
# <a name="cookie-compliance"></a><span data-ttu-id="6fdf9-103">Cookie-Compliance</span><span class="sxs-lookup"><span data-stu-id="6fdf9-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6fdf9-104">In diesem Thema werden Überlegungen zur Einhaltung von Cookies und zu den in Microsoft Dynamics 365 Commerce enthaltenen Standardrichtlinien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6fdf9-105">Datenschutz ist ein wichtiger Faktor, wenn Tracking-Technologien eingesetzt werden, die sich auf E-Commerce-Kunden auswirken.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="6fdf9-106">Aufgrund von Datenschutzstandards wie der allgemeinen Datenschutzverordnung (DSGVO) in der Europäischen Union (EU) müssen Richtlinien zum elektronischen Datenschutz für jede Website berücksichtigt werden, die heute aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="6fdf9-107">Da viele E-Commerce-Sites standardmäßig global zugänglich sind, ist es wichtig, dass Sie die Compliance-Standards für Ihre E-Commerce-Site überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="6fdf9-108">Weitere Informationen zu den von Microsoft verwendeten Grundprinzipien zur Cookie-Compliance finden Sie unter [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="6fdf9-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="6fdf9-109">Auf dieser Site erhalten Sie auch weitere Informationen zu Compliance- und Datenschutz-Bereichen.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="6fdf9-110">Die folgende Tabelle zeigt die aktuelle Referenzliste der von Dynamics 365 Commerce Websites platzierten Cookies.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="6fdf9-111">Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="6fdf9-111">Cookie name</span></span>                               | <span data-ttu-id="6fdf9-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="6fdf9-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="6fdf9-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="6fdf9-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="6fdf9-114">Speichern Sie Microsoft Azure Active Directory (Azure AD) Authentifizierungscookies für Single Sign-On (SSO).</span><span class="sxs-lookup"><span data-stu-id="6fdf9-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="6fdf9-115">Speichert verschlüsselte Benutzerprinzipalinformationen (Name, Nachname, E-Mail).</span><span class="sxs-lookup"><span data-stu-id="6fdf9-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="6fdf9-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="6fdf9-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="6fdf9-117">Speichern Sie die Warenkorb-ID, mit der Sie eine Liste der Produkte erhalten, die der Warenkorbinstanz hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="6fdf9-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="6fdf9-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="6fdf9-119">Nachverfolgung der Zustimmung zur Cookie-Konformität.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="6fdf9-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="6fdf9-120">ai_session</span></span>                                  | <span data-ttu-id="6fdf9-121">Erkennt, wie viele Sitzungen mit Benutzeraktivitäten bestimmte Seiten und Funktionen der App enthalten haben.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="6fdf9-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="6fdf9-122">ai_user</span></span>                                     | <span data-ttu-id="6fdf9-123">Erkennt, wie viele Personen die App und ihre Funktionen verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="6fdf9-124">Benutzer werden mit anonymen IDs gezählt.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="6fdf9-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="6fdf9-125">b2cru</span></span>                                       | <span data-ttu-id="6fdf9-126">Speichert die Umleitungs-URL dynamisch.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="6fdf9-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="6fdf9-127">JSESSIONID</span></span>                                  | <span data-ttu-id="6fdf9-128">Wird vom Zahlungsconnector Adyen zum Speichern der Benutzersitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="6fdf9-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="6fdf9-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="6fdf9-130">Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6fdf9-130">Authentication</span></span>                                               |
| <span data-ttu-id="6fdf9-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="6fdf9-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="6fdf9-132">Wird zur Aufrechterhaltung des Anforderungsstatus verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="6fdf9-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="6fdf9-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="6fdf9-134">CRSF-Token (Cross-Site Request Forgery) zum Schutz vor CRSF.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="6fdf9-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="6fdf9-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="6fdf9-136">Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="6fdf9-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="6fdf9-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="6fdf9-138">Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="6fdf9-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="6fdf9-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="6fdf9-140">Wird verwendet, um Anforderungen an die entsprechende Instanz des Produktionsauthentifizierungsservers weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="6fdf9-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="6fdf9-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="6fdf9-142">Wird zur Aufrechterhaltung der SSO-Sitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="6fdf9-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="6fdf9-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="6fdf9-144">Wird zum Verfolgen von Transaktionen verwendet (Anzahl der offenen Registerkarten, die sich bei einer B2C-Site (Business-to-Consumer) authentifizieren), einschließlich der aktuellen Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="6fdf9-145">Cookie-Zustimmung der Website-Benutzer auf einer E-Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="6fdf9-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="6fdf9-146">Wenn eine E-Commerce-Website-Funktion oder ein E-Commerce-Website-Modul ein nicht wesentliches Cookie verwendet, muss die Zustimmung eines Website-Benutzers eingeholt werden, bevor das Cookie nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="6fdf9-147">Damit Website-Benutzer auf der E-Commerce-Website eine Cookie-Einwilligung erteilen können, muss ein Website-Autor im Header-Modul der Seite ein Cookie-Einwilligungsmodul hinzufügen und konfigurieren, um sicherzustellen, dass die Einwilligung angefordert und empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="6fdf9-148">Die Zustimmung des Website-Benutzers muss gegeben werden, bevor eine Funktion oder ein Modul, das ein nicht wesentliches Cookie verwendet, auf einer Website-Seite gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6fdf9-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fdf9-149">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6fdf9-149">Additional resources</span></span>

[<span data-ttu-id="6fdf9-150">Funktionen und Leistungsspektrum der Eingabehilfe</span><span class="sxs-lookup"><span data-stu-id="6fdf9-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="6fdf9-151">Übersicht über Konformität</span><span class="sxs-lookup"><span data-stu-id="6fdf9-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="6fdf9-152">Seite mit Datenschutzrichtlinien hinzufügen</span><span class="sxs-lookup"><span data-stu-id="6fdf9-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="6fdf9-153">Benutzer-IDs ersetzen, die nachverfolgten Inhalten zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="6fdf9-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="6fdf9-154">Cookie-Zustimmungsmodul</span><span class="sxs-lookup"><span data-stu-id="6fdf9-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="6fdf9-155">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="6fdf9-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
