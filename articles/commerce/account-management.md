---
title: Kontoverwaltungsseiten und Module
description: In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412485"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="a26ab-103">Kontoverwaltungsseiten und Module</span><span class="sxs-lookup"><span data-stu-id="a26ab-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a26ab-104">In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.</span><span class="sxs-lookup"><span data-stu-id="a26ab-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a26ab-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a26ab-105">Overview</span></span>

<span data-ttu-id="a26ab-106">Kundenbetreuung bezieht sich auf eine Gruppe von Seiten, die benötigt wird, um Konto-zugeordnete Benutzerinformationen in Dynamics 365 Commerce zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a26ab-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a26ab-107">Zu den Kontoverwaltungsseiten gehören die Startseite, die Benutzerprofilseite, die Benutzeradressenseite, der Bestellverlauf, die Bestelldetailseite, Treuepunkteseite und die Wunschlistenseite.</span><span class="sxs-lookup"><span data-stu-id="a26ab-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="a26ab-108">Kontenverwaltungsseite-Landingpage</span><span class="sxs-lookup"><span data-stu-id="a26ab-108">Account management landing page</span></span>

<span data-ttu-id="a26ab-109">Die Kundenbetreuungsangebotsseite verwendet die folgenden Module:</span><span class="sxs-lookup"><span data-stu-id="a26ab-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="a26ab-110">**Container** – Alle Zielseitenmodule für die Kontoverwaltung sollten sich in einem Container befinden.</span><span class="sxs-lookup"><span data-stu-id="a26ab-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="a26ab-111">**Konto-Begrüßungskachel** – Dieses Modul wird verwendet, um eine Begrüßungsmeldung auf der Kontoverwaltungsseite bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="a26ab-112">Es enthält Eigenschaften für die Überschrift.</span><span class="sxs-lookup"><span data-stu-id="a26ab-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="a26ab-113">**Generische Kachel für Konto** – Dieses Modul kann verwendet werden, um Überschriften und Links für Kontoverwaltungsseiten bereitzustellen, z. B. die Seiten „Bestellverlauf“ oder „Mein Profil“.</span><span class="sxs-lookup"><span data-stu-id="a26ab-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="a26ab-114">Mit dem allgemeinen Kachelmodul kann eine Kachel für eine beliebige Seite konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a26ab-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="a26ab-115">In Fabrikam wird dieses Modul für die Seitenlinks „Bestellverlauf“ und „Mein Profil“ auf der Zielseite der Kontoverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a26ab-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="a26ab-116">**Wunschlistenkachel für Konto** – Dieses Modul wird verwendet, um eine Übersicht der Artikel auf der Wunschliste des Debitors anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="a26ab-117">Beispielsweise kann stehen, „Sie hat 10 Artikel auf Ihrer Wunschliste.“</span><span class="sxs-lookup"><span data-stu-id="a26ab-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="a26ab-118">Es umfasst Eigenschaften für die Überschrift und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="a26ab-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="a26ab-119">Der Link „Details anzeigen“ muss konfiguriert werden, um die Wunschlistenseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="a26ab-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="a26ab-120">**Adresskachel für Konto** – Dieses Modul wird verwendet, um eine Zusammenfassung der Benutzeradressen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="a26ab-121">Beispielsweise kann stehen „Sie haben 2 Adressen Ihrem Konto hinzugefügt.“</span><span class="sxs-lookup"><span data-stu-id="a26ab-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="a26ab-122">Es umfasst Eigenschaften für die Überschrift und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="a26ab-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="a26ab-123">Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzeradressseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="a26ab-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="a26ab-124">**Loyalitätskachel für Konto** – Dieses Modul wird verwendet, um zu die Treueprogramminformationen darzustellen und zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="a26ab-125">Diese Kachel hat zwei Status: In einem Status werden Links angezeigt, über die einem Treueprogramm beigetreten werden kann, wenn der Benutzer noch kein Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="a26ab-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="a26ab-126">Der andere Status zeigt Links zum Anzeigen der Treuedetailseite an, wenn der Benutzer bereits Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="a26ab-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="a26ab-127">Zu den Eigenschaften gehören die Überschrift, der Link „Anmelden“ und der Link „Treueprogramm anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="a26ab-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="a26ab-128">Der Link „Treueprogramm anzeigen“ muss konfiguriert werden, um auf die Treueprogrammseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="a26ab-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="a26ab-129">Der Link „Anmelden“ sollte konfiguriert werden, um zu einer Seite umzuleiten, auf der der Benutzer dem Treueprogramm beitreten kann.</span><span class="sxs-lookup"><span data-stu-id="a26ab-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="a26ab-130">Bestellverlaufseite</span><span class="sxs-lookup"><span data-stu-id="a26ab-130">Order history page</span></span>

<span data-ttu-id="a26ab-131">Die Auftragsverlaufseite verwendet das Auftragsarchivierungsmodul, um alle neuen Aufträge zu zeigen, die der Benutzer erteilt hat.</span><span class="sxs-lookup"><span data-stu-id="a26ab-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="a26ab-132">Auftragsdetailseite</span><span class="sxs-lookup"><span data-stu-id="a26ab-132">Order details page</span></span>

<span data-ttu-id="a26ab-133">Die Bestelldetailseite stellt Detailinformationen zu jedem Auftrag bereit und wird über die Auftragsverlaufsseite abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="a26ab-134">Es verwendet das Bestelldetailmodul, das die Vertriebs-ID oder -Transaktions-ID erfordert, um die Auftragsdetails abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="a26ab-135">Benutzerprofilseite</span><span class="sxs-lookup"><span data-stu-id="a26ab-135">User profile page</span></span>

<span data-ttu-id="a26ab-136">Die Benutzerprofilseite zeigt die Benutzerkontodetails, beispielsweise den Benutzernamen und die E-Mail-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a26ab-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="a26ab-137">Es verwendet die Benutzerprofildetails und Benutzerprofilbearbeitungsmodule.</span><span class="sxs-lookup"><span data-stu-id="a26ab-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="a26ab-138">Obwohl die E-Mail-Adresse nicht entfernt werden kann, kann sie bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a26ab-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="a26ab-139">Auf der Benutzerprofilseite werden auch Benutzereinstellungen angezeigt, mit denen ein Benutzer bestimmte Funktionen wie die Personalisierung von Empfehlungslisten aktivieren oder deaktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="a26ab-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="a26ab-140">Adressenseite des Benutzers</span><span class="sxs-lookup"><span data-stu-id="a26ab-140">User address page</span></span>

<span data-ttu-id="a26ab-141">Die Benutzeradressenseite zeigt die Liste der Adressen, die dem Benutzerkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a26ab-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="a26ab-142">Der Benutzer stellt entweder diese Adressen für das Auschecken bereit oder fügt diese direkt dieser Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="a26ab-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="a26ab-143">Das Benutzeradressenmodul wird verwendet, um Adressen hinzuzufügen und zu bearbeiten, die primäre Adresse festzulegen und vorhandenen Adressen auf der Seite zu rendern.</span><span class="sxs-lookup"><span data-stu-id="a26ab-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="a26ab-144">Wunschlistenseite</span><span class="sxs-lookup"><span data-stu-id="a26ab-144">Wish list page</span></span>

<span data-ttu-id="a26ab-145">Die Seite Wunschliste zeigt eine Liste von Elementen, die der Kunde seiner Wunschliste hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="a26ab-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="a26ab-146">Es verwendet das Wunschlistenmodul, um Wunschlistenartikel zu rendern.</span><span class="sxs-lookup"><span data-stu-id="a26ab-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="a26ab-147">Treueseite</span><span class="sxs-lookup"><span data-stu-id="a26ab-147">Loyalty page</span></span>

<span data-ttu-id="a26ab-148">Die Treueprogrammseite ermöglicht es einem Debitor, ihre Programmdetails anzuzeigen, wenn er bereits Treueprogrammmitglied ist.</span><span class="sxs-lookup"><span data-stu-id="a26ab-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="a26ab-149">Sie können auch die Punkte anzeigen, die sie für kürzliche Transaktionen erworben haben.</span><span class="sxs-lookup"><span data-stu-id="a26ab-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="a26ab-150">Die Seite verwendet das Modul „Treuedetails“, um die Treuedetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a26ab-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="a26ab-151">Um dem Treueprogramm beizutreten, kann eine Marketingseite mit Modulen für die Registrierung von Treueprogrammen- und Treueprogrammbedingungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a26ab-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="a26ab-152">Wenn der Benutzer kein Mitglied eines Treueprogramms ist, kann der Benutzer sich mit diesen Modulen anmelden.</span><span class="sxs-lookup"><span data-stu-id="a26ab-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a26ab-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a26ab-153">Additional resources</span></span>

[<span data-ttu-id="a26ab-154">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="a26ab-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a26ab-155">Containermodul</span><span class="sxs-lookup"><span data-stu-id="a26ab-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a26ab-156">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="a26ab-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a26ab-157">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="a26ab-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a26ab-158">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="a26ab-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a26ab-159">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="a26ab-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a26ab-160">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="a26ab-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a26ab-161">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="a26ab-161">Footer module</span></span>](author-footer-module.md)
