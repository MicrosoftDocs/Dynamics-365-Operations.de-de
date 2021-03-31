---
title: Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites
description: In diesem Thema wird beschrieben, wie Sie die Zahlungsmethode für Kundenkonten für B2B-E-Commerce-Websites (Business-to-Business) konfigurieren.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211200"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="63c18-103">Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites</span><span class="sxs-lookup"><span data-stu-id="63c18-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63c18-104">In diesem Thema wird beschrieben, wie Sie die Zahlungsmethode für Kundenkonten für B2B-E-Commerce-Websites (Business-to-Business) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="63c18-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="63c18-105">Einzelhändler können für die von ihnen verkauften Produkte und angebotenen Dienstleistungen verschiedene Zahlungsformen in einem E-Commerce-Kanal akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="63c18-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="63c18-106">Jeder vom Einzelhändler akzeptierte Zahlungstyp muss beim Einrichten des Systems in Microsoft Dynamics 365 Commerce konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="63c18-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="63c18-107">Die Zahlungsmethode Kundenkonto (oder „Konto“) muss auf B2B-E-Commerce-Websites unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="63c18-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="63c18-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="63c18-108">Prerequisites</span></span>

1. <span data-ttu-id="63c18-109">Fügen Sie die Zahlungsmethode „Kundenkonto“ in der Commerce-Zentralverwaltung hinzu.</span><span class="sxs-lookup"><span data-stu-id="63c18-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="63c18-110">Verknüpfen Sie die Zahlungsmethode „Kundenkonto“ mit dem E-Commerce-Kanal.</span><span class="sxs-lookup"><span data-stu-id="63c18-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="63c18-111">Stellen Sie sicher, dass **Auf Konto zulassen** für den Kunden unter **Einzelhandel und Handel \> Kunden \> Alle Kunden \> Zahlungsstandards** in der Commerce-Zentralverwaltung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63c18-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="63c18-112">Stellen Sie auch sicher, dass **Kreditlimit**-Parameter für den Kunden unter **Einzelhandel und Handel \> Kunden \> Alle Kunden \> Kredit und Inkasso** in der Commerce-Zentralverwaltung entsprechend eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="63c18-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="63c18-113">Aktivieren der Zahlungsmethode „Kundenkontos“ im Commerce-Website-Generator</span><span class="sxs-lookup"><span data-stu-id="63c18-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="63c18-114">Führen Sie folgende Schritte aus, um die Zahlungsmethode „Kundenkontos“ im Commerce-Website-Generator zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="63c18-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="63c18-115">Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.</span><span class="sxs-lookup"><span data-stu-id="63c18-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="63c18-116">Stellen Sie die **Kundenkontenzahlungen aktivieren**-Eigenschaft auf **Für B2B-Kunden aktiviert**.</span><span class="sxs-lookup"><span data-stu-id="63c18-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="63c18-117">Wählen Sie **Speichern und veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="63c18-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="63c18-118">Die neuen Seiteneinstellungen werden erst wirksam, nachdem die Datei App.settings.json aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="63c18-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="63c18-119">Weitere Informationen finden Sie unter [SDK- und Modulbibliothek-Updates](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="63c18-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="63c18-120">Aktivieren der Zahlungsmethode „Kundenkonto“ auf der Auftragsabschlussseite für die B2B-E-Commerce-Website</span><span class="sxs-lookup"><span data-stu-id="63c18-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="63c18-121">Führen Sie diese Schritte aus, um die Zahlungsmethode „Kundenkonto“ auf der Auftragsabschlussseite für die B2B-E-Commerce-Website zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="63c18-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="63c18-122">Suchen und bearbeiten Sie im Commerce-Website-Generator die Auftragsabschlussseite oder das Fragment, das das Auftragsabschlussmodul für die B2B-E-Commerce-Website enthält.</span><span class="sxs-lookup"><span data-stu-id="63c18-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="63c18-123">Wählen Sie Im **Kassenbereichcontainer**-Slot **Modul hinzufügen** aus, und fügen Sie dann ein **Kundenkontozahlung**-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="63c18-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="63c18-124">Positionieren Sie das **Kundenkontozahlung**-Modul durch Auswahl der Auslassungspunkte (**...**), und wählen Sie dann je nach Bedarf **Nach oben** oder **Nach unten**.</span><span class="sxs-lookup"><span data-stu-id="63c18-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="63c18-125">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="63c18-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="63c18-126">Bestätigen, dass die Zahlungsmethode „Kundenkonto“ aktiviert und veröffentlicht wurde</span><span class="sxs-lookup"><span data-stu-id="63c18-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="63c18-127">Führen Sie diese Schritte aus, um zu bestätigen, dass die Zahlungsmethode „Kundenkonto“ aktiviert und veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="63c18-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="63c18-128">Melden Sie sich bei der E-Commerce-Website an.</span><span class="sxs-lookup"><span data-stu-id="63c18-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="63c18-129">Fügen Sie ein Produkte zum Warenkorb hinzu.</span><span class="sxs-lookup"><span data-stu-id="63c18-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="63c18-130">Zur vorherigen Auftragsabschlussseite wechseln.</span><span class="sxs-lookup"><span data-stu-id="63c18-130">Go to the checkout page.</span></span> <span data-ttu-id="63c18-131">Sie sollten die neue **Kundenkonto**-Zahlungsmethode sehen.</span><span class="sxs-lookup"><span data-stu-id="63c18-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63c18-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="63c18-132">Additional resources</span></span>

[<span data-ttu-id="63c18-133">Eine B2B-E-Commerce-Website einrichten</span><span class="sxs-lookup"><span data-stu-id="63c18-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="63c18-134">Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen</span><span class="sxs-lookup"><span data-stu-id="63c18-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="63c18-135">Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten</span><span class="sxs-lookup"><span data-stu-id="63c18-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="63c18-136">Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites</span><span class="sxs-lookup"><span data-stu-id="63c18-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="63c18-137">SDK- und Modulbibliothekupdates</span><span class="sxs-lookup"><span data-stu-id="63c18-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]