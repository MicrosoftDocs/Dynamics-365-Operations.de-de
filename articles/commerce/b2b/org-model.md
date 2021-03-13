---
title: Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen
description: In diesem Thema wird beschrieben, wie Sie Organisationsmodellierungshierarchien für Business-to-Business-Organisationen (B2B) erstellen.
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
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035910"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="bb5ea-103">Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen</span><span class="sxs-lookup"><span data-stu-id="bb5ea-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb5ea-104">In diesem Thema wird beschrieben, wie Sie Organisationsmodellierungshierarchien für Business-to-Business-Organisationen (B2B) in Microsoft Dynamics 365 Commerce erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bb5ea-105">In der Commerce-Zentralverwaltung werden Geschäftspartnerorganisationen durch Kunden- und Kundenhierarchie-Entitäten repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="bb5ea-106">Die Geschäftspartnerorganisation und deren Benutzer werden als Kunden dargestellt, und Kundenhierarchien werden verwendet, um diese Kunden miteinander zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="bb5ea-107">Wenn eine Geschäftspartneranfrage zum Beitritt zu einer B2B-E-Commerce-Website genehmigt wird, werden die folgenden Aktionen ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="bb5ea-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="bb5ea-108">Es werden zwei neue Kundendatensätze im System erstellt: ein **Typ: Organisation**-Kundendatensatz für die Geschäftspartnerorganisation und ein **Typ: Person**-Kundendatensatz für den Anforderer (das ist der Geschäftspartnerbenutzer, der die Anfrage eingereicht hat).</span><span class="sxs-lookup"><span data-stu-id="bb5ea-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="bb5ea-109">Unter **Kunde \> Kundenhierarchie** wird ein neuer Kundenhierarchiedatensatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="bb5ea-110">Dieser Datensatz hat die folgenden Header-Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bb5ea-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="bb5ea-111">**Kundenhierarchie-ID** – eine eindeutige ID für die Kundenhierarchie.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="bb5ea-112">Diese ID verwendet die Nummernfolge, die in den gemeinsam genutzten Commerce-Parametern in der Commerce-Zentralverwaltung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="bb5ea-113">**Name** – der Organisationsname des Geschäftspartners, wie in der Onboarding-Anfrage angegeben.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="bb5ea-114">**Zweck** – diese Eigenschaft wird auf den vordefinierten Wert **B2B-Organisation** gesetzt.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="bb5ea-115">**Organisation** – die Kunden-ID des Geschäftspartners.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="bb5ea-116">Hier sind die Details des Kundenhierarchiedatensatzes:</span><span class="sxs-lookup"><span data-stu-id="bb5ea-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="bb5ea-117">Der Kundendatensatz des Anforderers wid der Kundenhierarchie zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="bb5ea-118">Die Administratorrolle wird dem Anforderer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="bb5ea-119">Wenn der Administrator der Geschäftspartnerorganisation auf einer B2B-Website weitere Benutzer hinzufügt, wird in der Commerce-Zentralverwaltung ein neuer Kundendatensatz für jeden Benutzer erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="bb5ea-120">Dieser Kundendatensatz wird auch dem relevanten Kundenhierarchiedatensatz für den Geschäftspartner hinzugefügt und hat die Rolle eines „Benutzers“.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="bb5ea-121">In den meisten Fällen sollten die entsprechenden Eigenschaftswerte aller Kundendatensätze in einer Hierarchie übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="bb5ea-122">Da beispielsweise alle Geschäftspartnerbenutzer ähnliche Preise für Produkte erhalten sollten, sollten ihre Preisgruppe und die zugehörigen Konfigurationen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="bb5ea-123">Das System erzwingt diese Konsistenz jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="bb5ea-124">Daher sind die relevanten Benutzer der Commerce-Zentralverwaltung dafür verantwortlich, dass die Eigenschaftswerte und -konfigurationen für alle Kunden in einer bestimmten Hierarchie übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="bb5ea-125">Benutzer der Commerce-Zentralverwaltung können die Eigenschaftswerte für alle Kundendatensätze in der Hierarchie nebeneinander anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="bb5ea-126">Wählen Sie die relevanten Kundendatensatzeigenschaften aus, indem Sie die Registerkartennamen im Dropdown-Menü auswählen.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="bb5ea-127">Benutzer können die Eigenschaftswerte in dieser Ansicht direkt anzeigen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="bb5ea-128">Wenn Sie alternativ alle Werte aus dem Administrator-Kundendatensatz auf alle Benutzerkundendatensätze anwenden möchten, wählen Sie in den Details der Kundenhierarchie **Überschreiben** aus.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb5ea-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb5ea-129">Additional resources</span></span>

[<span data-ttu-id="bb5ea-130">Eine B2B-E-Commerce-Website einrichten</span><span class="sxs-lookup"><span data-stu-id="bb5ea-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="bb5ea-131">Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten</span><span class="sxs-lookup"><span data-stu-id="bb5ea-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="bb5ea-132">Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites</span><span class="sxs-lookup"><span data-stu-id="bb5ea-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="bb5ea-133">Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites</span><span class="sxs-lookup"><span data-stu-id="bb5ea-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)
