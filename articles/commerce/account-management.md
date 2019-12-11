---
title: Kontoverwaltungsseiten und Module
description: In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.
author: v-chgri
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785378"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="475cb-103">Kontoverwaltungsseiten und Module</span><span class="sxs-lookup"><span data-stu-id="475cb-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="475cb-104">In diesem Thema werden Kundenbetreuungsseiten und Module in Microsoft Dynamics 365 Commerce behandelt.</span><span class="sxs-lookup"><span data-stu-id="475cb-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="475cb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="475cb-105">Overview</span></span>

<span data-ttu-id="475cb-106">Kundenbetreuung bezieht sich auf eine Gruppe von Seiten, die benötigt wird, um Konto-zugeordnete Benutzerinformationen in Dynamics 365 Commerce zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="475cb-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="475cb-107">Zu den Kontoverwaltungsseiten gehören die Startseite, die Benutzerprofilseite, die Benutzeradressenseite, der Bestellverlauf, die Bestelldetailseite, Treuepunkteseite und die Wunschlistenseite.</span><span class="sxs-lookup"><span data-stu-id="475cb-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="475cb-108">Kontenverwaltungsseite-Landingpage</span><span class="sxs-lookup"><span data-stu-id="475cb-108">Account management landing page</span></span>

<span data-ttu-id="475cb-109">Die Kundenbetreuungsangebotsseite verwendet die folgenden Module:</span><span class="sxs-lookup"><span data-stu-id="475cb-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="475cb-110">**Inhalt-Platzierung** – Dieses Modul ist ein Containermodul, das alle Module in der Kundenbetreuungsangebotsseite enthält.</span><span class="sxs-lookup"><span data-stu-id="475cb-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="475cb-111">**Konto-Begrüßungselement** – Dieses Modul wird verwendet, um eine Begrüßungsmeldung auf der Kontoverwaltungsseite bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="475cb-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="475cb-112">Sie umfasst Eigenschaften für die Überschrift und die Kachelgröße.</span><span class="sxs-lookup"><span data-stu-id="475cb-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="475cb-113">Die Eigenschaft **Kachelgröße** definiert die Breite des Moduls im Inhaltplatzierungsmodul.</span><span class="sxs-lookup"><span data-stu-id="475cb-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="475cb-114">Die verfügbaren Werte sind von **1** bis zu **12**, wobei **12** für die volle Breite des Inhaltplatzierungscontainers steht.</span><span class="sxs-lookup"><span data-stu-id="475cb-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="475cb-115">**Kontenauftrags-Platzierungsartikel** – Dieses Modul wird verwendet, um eine Zusammenfassung der Anzahl von Aufträgen verfügbar machen, die vom Benutzer im Konto platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="475cb-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="475cb-116">Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="475cb-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="475cb-117">Der Link „Details anzeigen“  muss konfiguriert werden, um die Auftragsverlaufsseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="475cb-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="475cb-118">**Kundenprofil-Platzierungsartikel** – Dieses Modul wird verwendet, um eine Zusammenfassung des Benutzerprofils bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="475cb-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="475cb-119">Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="475cb-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="475cb-120">Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzerprofilseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="475cb-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="475cb-121">**Konto Wunschlistenartikel** – Dieses Modul wird verwendet, um eine Übersicht der Artikel auf der Wunschliste des Debitors anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="475cb-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="475cb-122">Beispielsweise kann stehen, „Sie hat 10 Artikel auf Ihrer Wunschliste.“</span><span class="sxs-lookup"><span data-stu-id="475cb-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="475cb-123">Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="475cb-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="475cb-124">Der Link „Details anzeigen“ muss konfiguriert werden, um die Wunschlistenseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="475cb-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="475cb-125">**Kundenprofil-Adressartikel** – Dieses Modul wird verwendet, um eine Zusammenfassung der Benutzeradressen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="475cb-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="475cb-126">Beispielsweise kann stehen „Sie haben 2 Adressen Ihrem Konto hinzugefügt.“</span><span class="sxs-lookup"><span data-stu-id="475cb-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="475cb-127">Sie umfasst Eigenschaften für die Überschrift, die Kachelgröße und den Link „Details anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="475cb-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="475cb-128">Der Link „Details anzeigen“ muss konfiguriert werden, um die Benutzeradressseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="475cb-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="475cb-129">**Kontoenloyalitätsartikel** – Dieses Modul wird verwendet, um zu die Treueprogramminformationen darzustellen und zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="475cb-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="475cb-130">Sie umfasst Eigenschaften für den Link für die Überschrift, die Kachelgröße und den Link „Details anzeigen“ und „Mitglied werden“.</span><span class="sxs-lookup"><span data-stu-id="475cb-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="475cb-131">Der Link „Details anzeigen“ muss konfiguriert werden, um auf die Treueprogrammseite umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="475cb-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="475cb-132">Der Link „Mitglied werden“ sollte konfiguriert werden, um zu einer Seite umzuleiten, auf der der Benutzer dem Treueprogramm beitreten kann.</span><span class="sxs-lookup"><span data-stu-id="475cb-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="475cb-133">Bestellverlaufseite</span><span class="sxs-lookup"><span data-stu-id="475cb-133">Order history page</span></span>

<span data-ttu-id="475cb-134">Die Auftragsverlaufseite verwendet das Auftragsarchivierungsmodul, um alle neuen Aufträge zu zeigen, die der Benutzer erteilt hat.</span><span class="sxs-lookup"><span data-stu-id="475cb-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="475cb-135">Auftragsdetailseite</span><span class="sxs-lookup"><span data-stu-id="475cb-135">Order details page</span></span>

<span data-ttu-id="475cb-136">Die Bestelldetailseite stellt Detailinformationen zu jedem Auftrag bereit und wird über die Auftragsverlaufsseite abgerufen.</span><span class="sxs-lookup"><span data-stu-id="475cb-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="475cb-137">Es verwendet das Bestelldetailmodul, das die Vertriebs-ID oder -Transaktions-ID erfordert, um die Auftragsdetails abzurufen.</span><span class="sxs-lookup"><span data-stu-id="475cb-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="475cb-138">Benutzerprofilseite</span><span class="sxs-lookup"><span data-stu-id="475cb-138">User profile page</span></span>

<span data-ttu-id="475cb-139">Die Benutzerprofilseite zeigt die Benutzerkontodetails, beispielsweise den Benutzername und die E-Mail-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="475cb-139">The user profile page shows user account details, such as user's name and email address.</span></span> <span data-ttu-id="475cb-140">Es verwendet das Benutzerprofilmodul.</span><span class="sxs-lookup"><span data-stu-id="475cb-140">It uses the user profile module.</span></span> <span data-ttu-id="475cb-141">Obwohl die E-Mail-Adresse nicht entfernt werden kann, kann sie bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="475cb-141">Although the email address can't be removed, it can be edited.</span></span>

### <a name="user-address-page"></a><span data-ttu-id="475cb-142">Adressenseite des Benutzers</span><span class="sxs-lookup"><span data-stu-id="475cb-142">User address page</span></span>

<span data-ttu-id="475cb-143">Die Benutzeradressenseite zeigt die Liste der Adressen, die dem Benutzerkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="475cb-143">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="475cb-144">Der Benutzer stellt entweder diese Adressen für das Auschecken bereit oder fügt diese direkt dieser Seite hinzu.</span><span class="sxs-lookup"><span data-stu-id="475cb-144">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="475cb-145">Das Benutzeradressenmodul wird verwendet, um Adressen hinzuzufügen und zu bearbeiten, die primäre Adresse festzulegen und vorhandenen Adressen auf der Seite zu rendern.</span><span class="sxs-lookup"><span data-stu-id="475cb-145">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="475cb-146">Wunschlistenseite</span><span class="sxs-lookup"><span data-stu-id="475cb-146">Wish list page</span></span>

<span data-ttu-id="475cb-147">Die Seite Wunschliste zeigt eine Liste von Elementen, die der Kunde seiner Wunschliste hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="475cb-147">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="475cb-148">Es verwendet das Wunschlistenmodul, um Wunschlistenartikel zu rendern.</span><span class="sxs-lookup"><span data-stu-id="475cb-148">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="475cb-149">Treueseite</span><span class="sxs-lookup"><span data-stu-id="475cb-149">Loyalty page</span></span>

<span data-ttu-id="475cb-150">Die Treueprogrammseite ermöglicht es einem Debitor, einem Treueprogramm beizutreten oder die Programmdetails anzuzeigen, wenn er bereits Treueprogrammmitglied ist.</span><span class="sxs-lookup"><span data-stu-id="475cb-150">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="475cb-151">Sie können auch die Punkte anzeigen, die sie für kürzliche Transaktionen erworben haben.</span><span class="sxs-lookup"><span data-stu-id="475cb-151">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="475cb-152">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="475cb-152">Additional resources</span></span>

[<span data-ttu-id="475cb-153">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="475cb-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="475cb-154">Containermodul</span><span class="sxs-lookup"><span data-stu-id="475cb-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="475cb-155">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="475cb-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="475cb-156">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="475cb-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="475cb-157">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="475cb-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="475cb-158">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="475cb-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="475cb-159">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="475cb-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="475cb-160">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="475cb-160">Footer module</span></span>](author-footer-module.md)
