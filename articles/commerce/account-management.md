---
title: Seiten und Module zur Kontenverwaltung
description: In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: df4959a61f1b2948c62a558523a848ff8b2fe0a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796293"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="c8349-103">Seiten und Module zur Kontenverwaltung</span><span class="sxs-lookup"><span data-stu-id="c8349-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8349-104">In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.</span><span class="sxs-lookup"><span data-stu-id="c8349-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8349-105">Kundenbetreuung bezieht sich auf eine Gruppe von Seiten, die benötigt wird, um Konto-zugeordnete Benutzerinformationen in Dynamics 365 Commerce zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c8349-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c8349-106">Zu den Kontoverwaltungsseiten gehören die Startseite, die Benutzerprofilseite, die Benutzeradressenseite, der Bestellverlauf, die Bestelldetailseite, Treuepunkteseite und die Wunschlistenseite.</span><span class="sxs-lookup"><span data-stu-id="c8349-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="c8349-107">Kontenverwaltungsseite-Landingpage</span><span class="sxs-lookup"><span data-stu-id="c8349-107">Account management landing page</span></span>

<span data-ttu-id="c8349-108">Die Kundenbetreuungsangebotsseite verwendet die folgenden Module:</span><span class="sxs-lookup"><span data-stu-id="c8349-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="c8349-109">**Container** – Alle Zielseitenmodule für die Kontoverwaltung sollten sich in einem Container befinden.</span><span class="sxs-lookup"><span data-stu-id="c8349-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="c8349-110">**Konto-Begrüßungskachel** – Dieses Modul wird verwendet, um eine Begrüßungsmeldung auf der Kontoverwaltungsseite bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8349-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="c8349-111">Es enthält Eigenschaften für die Überschrift.</span><span class="sxs-lookup"><span data-stu-id="c8349-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="c8349-112">**Generische Kachel für Konto** – Dieses Modul kann verwendet werden, um Überschriften und Links für Kontoverwaltungsseiten bereitzustellen, z. B. die Seiten „Bestellverlauf“ oder „Mein Profil“.</span><span class="sxs-lookup"><span data-stu-id="c8349-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="c8349-113">Mit dem allgemeinen Kachelmodul kann eine Kachel für eine beliebige Seite konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8349-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="c8349-114">In Fabrikam wird dieses Modul für die Seitenlinks „Bestellverlauf“ und „Mein Profil“ auf der Zielseite der Kontoverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8349-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="c8349-115">**Wunschlistenkachel für Konto** – Dieses Modul wird verwendet, um eine Übersicht der Artikel auf der Wunschliste des Debitors anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8349-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="c8349-116">Beispielsweise kann stehen, „Sie hat 10 Artikel auf Ihrer Wunschliste.“</span><span class="sxs-lookup"><span data-stu-id="c8349-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="c8349-117">Es umfasst Eigenschaften für die Überschrift und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="c8349-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="c8349-118">Der Link „Details anzeigen“ muss konfiguriert werden, um die Wunschlistenseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c8349-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="c8349-119">**Adresskachel für Konto** – Dieses Modul wird verwendet, um eine Zusammenfassung der Benutzeradressen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8349-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="c8349-120">Beispielsweise kann stehen „Sie haben 2 Adressen Ihrem Konto hinzugefügt.“</span><span class="sxs-lookup"><span data-stu-id="c8349-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="c8349-121">Es umfasst Eigenschaften für die Überschrift und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="c8349-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="c8349-122">Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzeradressseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c8349-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="c8349-123">**Loyalitätskachel für Konto** – Dieses Modul wird verwendet, um zu die Treueprogramminformationen darzustellen und zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c8349-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="c8349-124">Diese Kachel hat zwei Status: In einem Status werden Links angezeigt, über die einem Treueprogramm beigetreten werden kann, wenn der Benutzer noch kein Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="c8349-124">This tile has two states: one state shows links to join a loyalty program if the user is not a member already.</span></span> <span data-ttu-id="c8349-125">Der andere Status zeigt Links zum Anzeigen der Treuedetailseite an, wenn der Benutzer bereits Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="c8349-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="c8349-126">Zu den Eigenschaften gehören die Überschrift, der Link „Anmelden“ und der Link „Treueprogramm anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="c8349-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="c8349-127">Der Link „Treueprogramm anzeigen“ muss konfiguriert werden, um auf die Treueprogrammseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c8349-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="c8349-128">Der Link „Anmelden“ sollte konfiguriert werden, um zu einer Seite umzuleiten, auf der der Benutzer dem Treueprogramm beitreten kann.</span><span class="sxs-lookup"><span data-stu-id="c8349-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="c8349-129">Bestellverlaufseite</span><span class="sxs-lookup"><span data-stu-id="c8349-129">Order history page</span></span>

<span data-ttu-id="c8349-130">Die Auftragsverlaufseite verwendet das Auftragsarchivierungsmodul, um alle neuen Aufträge zu zeigen, die der Benutzer erteilt hat.</span><span class="sxs-lookup"><span data-stu-id="c8349-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="c8349-131">Auftragsdetailseite</span><span class="sxs-lookup"><span data-stu-id="c8349-131">Order details page</span></span>

<span data-ttu-id="c8349-132">Die Bestelldetailseite stellt Detailinformationen zu jedem Auftrag bereit und wird über die Auftragsverlaufsseite abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c8349-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="c8349-133">Es verwendet das Bestelldetailmodul, das die Vertriebs-ID oder -Transaktions-ID erfordert, um die Auftragsdetails abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8349-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="my-profile-page"></a><span data-ttu-id="c8349-134">Eigene Profilseite</span><span class="sxs-lookup"><span data-stu-id="c8349-134">My profile page</span></span>

<span data-ttu-id="c8349-135">Auf der Seite „Mein Profil“ werden die Kontoprofildetails des Benutzers mithilfe des Kontoprofilmoduls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8349-135">The My profile page shows the user's account profile details using the account profile module.</span></span> <span data-ttu-id="c8349-136">Auf der Seite werden die mit dem Benutzerkonto verknüpfte E-Mail-Adresse sowie die für das Konto eingerichteten Einstellungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8349-136">The page shows the email address associated with the user's account, as well as preferences set up for the account.</span></span> <span data-ttu-id="c8349-137">Wenn Sie benutzerdefinierte Debitorenattribute einrichten, werden diese Attribute auch in einem Abschnitt „Weitere Informationen“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c8349-137">If setting up custom customer attributes, an "Additional Information" section will also display those attributes.</span></span> <span data-ttu-id="c8349-138">Benutzer können ihren Namen, ihre Einstellungen oder weitere Informationen (falls verfügbar) bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c8349-138">Users can edit their name, preferences, or additional information (if available).</span></span>

### <a name="user-address-page"></a><span data-ttu-id="c8349-139">Adressenseite des Benutzers</span><span class="sxs-lookup"><span data-stu-id="c8349-139">User address page</span></span>

<span data-ttu-id="c8349-140">Die Benutzeradressenseite zeigt die Liste der Adressen, die dem Benutzerkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c8349-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="c8349-141">Der Benutzer stellt entweder diese Adressen für das Auschecken bereit oder fügt diese direkt dieser Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="c8349-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="c8349-142">Das Benutzeradressenmodul wird verwendet, um Adressen hinzuzufügen und zu bearbeiten, die primäre Adresse festzulegen und vorhandenen Adressen auf der Seite zu rendern.</span><span class="sxs-lookup"><span data-stu-id="c8349-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="c8349-143">Wunschlistenseite</span><span class="sxs-lookup"><span data-stu-id="c8349-143">Wish list page</span></span>

<span data-ttu-id="c8349-144">Die Seite Wunschliste zeigt eine Liste von Elementen, die der Kunde seiner Wunschliste hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="c8349-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="c8349-145">Es verwendet das Wunschlistenmodul, um Wunschlistenartikel zu rendern.</span><span class="sxs-lookup"><span data-stu-id="c8349-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="c8349-146">Treueseite</span><span class="sxs-lookup"><span data-stu-id="c8349-146">Loyalty page</span></span>

<span data-ttu-id="c8349-147">Die Treueprogrammseite ermöglicht es einem Debitor, ihre Programmdetails anzuzeigen, wenn er bereits Treueprogrammmitglied ist.</span><span class="sxs-lookup"><span data-stu-id="c8349-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="c8349-148">Sie können auch die Punkte anzeigen, die sie für kürzliche Transaktionen erworben haben.</span><span class="sxs-lookup"><span data-stu-id="c8349-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="c8349-149">Die Seite verwendet das Modul „Treuedetails“, um die Treuedetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8349-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="c8349-150">Um dem Treueprogramm beizutreten, kann eine Marketingseite mit Modulen für die Registrierung von Treueprogrammen- und Treueprogrammbedingungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8349-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="c8349-151">Wenn der Benutzer kein Mitglied eines Treueprogramms ist, kann der Benutzer sich mit diesen Modulen anmelden.</span><span class="sxs-lookup"><span data-stu-id="c8349-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8349-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c8349-152">Additional resources</span></span>

[<span data-ttu-id="c8349-153">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="c8349-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c8349-154">Containermodul</span><span class="sxs-lookup"><span data-stu-id="c8349-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c8349-155">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="c8349-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c8349-156">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="c8349-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c8349-157">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="c8349-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c8349-158">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="c8349-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c8349-159">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="c8349-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c8349-160">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="c8349-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]