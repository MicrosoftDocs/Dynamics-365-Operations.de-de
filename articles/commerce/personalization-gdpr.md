---
title: Personalisierte Empfehlungen abmelden
description: In diesem Thema wird erläutert, wie Sie Kunden davon abhalten können, personalisierte Empfehlungen in Microsoft Dynamics 365 Commerce zu erhalten.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e822d0097443d7da347c29ebfa63ad6a2d7cbf8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000636"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="9336f-103">Personalisierte Empfehlungen abmelden</span><span class="sxs-lookup"><span data-stu-id="9336f-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9336f-104">In diesem Thema wird erläutert, wie Sie Kunden davon abhalten können, personalisierte Empfehlungen in Microsoft Dynamics 365 Commerce zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9336f-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9336f-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9336f-105">Overview</span></span>

<span data-ttu-id="9336f-106">Während der Kontoerstellung werden neue Kunden automatisch eingerichtet, um personalisierte Empfehlungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9336f-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="9336f-107">Jedoch bietet Dynamics 365 Commerce Einzelhändlern verschiedene Möglichkeiten, Benutzern zu ermöglichen, diese Empfehlungen nicht zu erhalten und die Verarbeitung ihrer personenbezogenen Daten einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="9336f-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="9336f-108">Authentifizierte Benutzer, die sich gegen personalisierte Empfehlungen entscheiden, sehen keine personalisierten Listen mehr.</span><span class="sxs-lookup"><span data-stu-id="9336f-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="9336f-109">Darüber hinaus werden alle persönlichen Daten, die zur Personalisierung gesammelt werden, aus personalisierten Empfehlungsmodellen entfernt.</span><span class="sxs-lookup"><span data-stu-id="9336f-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="9336f-110">Weitere Informationen zum Empfangen personalisierter Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9336f-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="9336f-111">Möglichkeiten für Einzelhändler, ein Abmeldungs-Erlebnis zu implementieren</span><span class="sxs-lookup"><span data-stu-id="9336f-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="9336f-112">Einzelhändler haben drei Möglichkeiten, ein Abmeldungs-Erlebnis zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9336f-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="9336f-113">Deaktivierung im Namen der Benutzer</span><span class="sxs-lookup"><span data-stu-id="9336f-113">Opting out on behalf of users</span></span>

<span data-ttu-id="9336f-114">In der Kontoverwaltung im Commerce-Backoffice können sich Einzelhändler für Benutzer abmelden.</span><span class="sxs-lookup"><span data-stu-id="9336f-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="9336f-115">Suchen Sie auf der Back-Office-Startseite nach **alle Kunden**.</span><span class="sxs-lookup"><span data-stu-id="9336f-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="9336f-116">Suchen Sie nach einem Kunden und wählen Sie dann die Registerkarte **Einzelhandel**.</span><span class="sxs-lookup"><span data-stu-id="9336f-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Registerkarte für den Einzelhandel](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="9336f-118">Unter **Privatsphäre** stellen Sie die Option **Deaktivieren Sie die Personalisierung** auf **Ja** ein.</span><span class="sxs-lookup"><span data-stu-id="9336f-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Datenschutzeinstellungen](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="9336f-120">Klicken Sie auf **Speichern** und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="9336f-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="9336f-121">Erfahrung mit modulbasierter Abmeldungs-Erfahrung</span><span class="sxs-lookup"><span data-stu-id="9336f-121">Module-based opt-out experience</span></span>

<span data-ttu-id="9336f-122">Einzelhändler können authentifizierten Benutzern erlauben, sich selbst von personalisierten Empfehlungen abzumelden.</span><span class="sxs-lookup"><span data-stu-id="9336f-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="9336f-123">Fügen Sie das Benutzer-Deaktivierungsmodul zu den Profilseiten des Kundenkontos hinzu, um diese Deaktivierungsfunktion zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="9336f-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="9336f-124">Benutzerdefinierte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="9336f-124">Custom extensions</span></span>

<span data-ttu-id="9336f-125">Einzelhändler können ihre eigenen Erweiterungen erstellen, um das Abmelde-Erlebnis für Benutzer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9336f-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="9336f-126">Weitere Informationen finden Sie unter [Rufen Sie die Retail Server APIs auf](e-commerce-extensibility/call-retail-server-apis.md) und [Online-Kanal-Erweiterbarkeit](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="9336f-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="9336f-127">Erhalten Sie eine digitale Kopie der personalisierten Empfehlungsdaten für einen authentifizierten Benutzer</span><span class="sxs-lookup"><span data-stu-id="9336f-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="9336f-128">Kunden möchten möglicherweise eine digitale Kopie ihrer persönlichen Daten erhalten und auch eine exportierte Ansicht der Ergebnisse ihrer Empfehlungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9336f-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="9336f-129">Wenn ein Kunde diese Informationen anfordert, muss der Einzelhändler eine benutzerdefinierte Erweiterung erstellen, die die Retail Server-Anwendungsprogrammierschnittstelle (API) aufruft und die vollständigen Ergebnisse von der **Tipps für Sie** Liste abruft, basierend auf der Kundennummer des Kunden.</span><span class="sxs-lookup"><span data-stu-id="9336f-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="9336f-130">Die Ergebnisse können dann im CSV-Format (mit Komma getrennte Werte) exportiert und mit dem Kunden geteilt werden.</span><span class="sxs-lookup"><span data-stu-id="9336f-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="9336f-131">Das folgende Beispiel zeigt, wie ein Einzelhändler diese Aufgabe ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="9336f-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="9336f-132">Der Einzelhändler erstellt eine benutzerdefinierte Erweiterung, um persönliche Empfehlungsdaten im Namen des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9336f-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="9336f-133">Informationen zum Erstellen von Modulen, zum Klonen vorhandener Module, zum Aufrufen von Retail Server-APIs und zum Aufrufen von Datenaktionen finden Sie unter [Online-Kanal-Erweiterbarkeit ](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="9336f-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="9336f-134">Die benutzerdefinierte Nebenstelle ruft die **Empfehlungen abrufen** Kerndatenaktion ab und übergibt die erforderlichen Informationen an sie, basierend auf den Anforderungen der Liste.</span><span class="sxs-lookup"><span data-stu-id="9336f-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="9336f-135">Im Falle der **Tipps für Sie** Liste muss die Erweiterung den richtigen Listennamen und die richtige Kunden-ID an die Datenaktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="9336f-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="9336f-136">Eine Möglichkeit zum Erstellen der benutzerdefinierten Erweiterung besteht darin, das vorhandene Produktsammlungsmodul zu klonen, das zum Zurückgeben von Empfehlungsergebnissen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9336f-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="9336f-137">Durch Klonen dieses vorhandenen Moduls kann ein Einzelhändler den vorhandenen Code ändern und eine neue Schaltfläche hinzufügen, mit der die Empfehlungsergebnisse in eine CSV-Datei exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="9336f-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="9336f-138">Weitere Informationen finden Sie unter [Klonen Sie eine Modulbibliothek](e-commerce-extensibility/clone-starter-module.md) und [Produktsammelmodule](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9336f-138">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="9336f-139">Eine vollständige Ansicht der Retail Server-API-Bibliothek finden Sie unter [Retail Server-Kunden- und Verbraucher-APIs](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="9336f-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="9336f-140">Nachdem die benutzerdefinierte Erweiterung erstellt wurde, kann der Einzelhändler eine CSV-Datei mit allen Empfehlungsergebnissen exportieren, die auf der eindeutigen Kunden-ID des authentifizierten Benutzers basiert.</span><span class="sxs-lookup"><span data-stu-id="9336f-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="9336f-141">Der Einzelhändler kann die exportierte CSV-Datei mit der vollständigen personalisierten Liste der empfohlenen Produkte für den authentifizierten Benutzer freigeben.</span><span class="sxs-lookup"><span data-stu-id="9336f-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9336f-142">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9336f-142">Additional resources</span></span>

[<span data-ttu-id="9336f-143">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="9336f-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9336f-144">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="9336f-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9336f-145">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9336f-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9336f-146">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="9336f-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="9336f-147">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="9336f-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9336f-148">Produktempfehlungen in POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9336f-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9336f-149">Empfehlungen dem Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9336f-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9336f-150">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="9336f-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9336f-151">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="9336f-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9336f-152">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="9336f-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9336f-153">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="9336f-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
