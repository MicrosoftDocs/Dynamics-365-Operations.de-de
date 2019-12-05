---
title: Integrierte Masterdaten von Debitoren
description: In diesem Thema wird die Integration von Debitorendaten zwischen Finance and Operations und Common Data Service beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769682"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="721b0-103">Integrierte Masterdaten von Debitoren</span><span class="sxs-lookup"><span data-stu-id="721b0-103">Integrated customer master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="721b0-104">Debitorendatensätze werden typischerweise in mehreren Anwendungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="721b0-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="721b0-105">So kann eine Verkaufsaktivität kommerzielle Debitorendatensätze über eine Verkaufsanwendung übernehmen, und E-Commerce und Einzelhandelsverkäufe können Debitorendatensätze über eine Finance and Operations-Anwendung übernehmen.</span><span class="sxs-lookup"><span data-stu-id="721b0-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="721b0-106">Unabhängig davon, woher der Debitorendatensatz stammt, wird er im Hintergrund über Anwendungsgrenzen und Infrastrukturunterschiede hinweg integriert.</span><span class="sxs-lookup"><span data-stu-id="721b0-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="721b0-107">Integrierte Masterdaten von Debitoren sind bei der Verarbeitung von Multimasterszenarien behilflich und bieten eine umfassende Ansicht des Debitors in der Dynamics 365-Anwendungssuite.</span><span class="sxs-lookup"><span data-stu-id="721b0-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="721b0-108">Debitorendatenfluss</span><span class="sxs-lookup"><span data-stu-id="721b0-108">Customer data flow</span></span>

<span data-ttu-id="721b0-109">*Debitor* ist ein gut definiertes Konzept in Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="721b0-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="721b0-110">Daher umfasst die Integration von Debitorendaten nur die Harmonisierung des Debitorenkonzepts zwischen den beiden Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="721b0-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="721b0-111">Die folgende Abbildung zeigt den Debitorendatenfluss.</span><span class="sxs-lookup"><span data-stu-id="721b0-111">The following illustration shows the customer data flow.</span></span>

![Debitorendatenfluss](media/dual-write-customer-data-flow.png)

<span data-ttu-id="721b0-113">Debitoren können in zwei Typen unterteilt werden: kommerzielle Debitoren/Unternehmensdebitoren und Verbraucher/Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="721b0-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="721b0-114">Diese beiden Arten von Debitoren werden in Finance and Operations and Common Data Service unterschiedlich gespeichert und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="721b0-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="721b0-115">In Finance and Operations werden sowohl kommerzielle Debitoren/Unternehmensdebitoren als auch Verbraucher/Endbenutzer in einer einzigen Tabelle mit dem Namen **CustTable** (CustomerCustomerV3Entity) verwaltet, und sie werden basierend auf dem **Type**-Attribut klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="721b0-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="721b0-116">(Wenn **Typ** auf **Organisation** festgelegt ist, ist der Debitor ein kommerzieller Debitor/Unternehmensdebitor, und wenn **Typ** auf **Person** festgelegt ist, so ist der Debitor ein Verbraucher/Endbenutzer.) Die primären Kontaktpersoninformationen werden über die SMMContactPersonEntity-Entität verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="721b0-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="721b0-117">In Common Data Service werden kommerzielle Debitoren/Unternehmensdebitoren in der Kontoentität verwaltet und als Debitoren identifiziert, wenn das **RelationshipType**-Attribute auf **Debitor** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="721b0-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="721b0-118">Sowohl Verbrauch/Endbenutzer als auch die Kontaktperson werden von der Kontaktentität dargestellt.</span><span class="sxs-lookup"><span data-stu-id="721b0-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="721b0-119">Um eine klare Trennung zwischen einem Verbraucher/Endbenutzer und einer Kontaktperson zu haben, weist die **Kontakt**-Entität eine boolesche Markierung mit dem Namen **Verkäuflich** auf.</span><span class="sxs-lookup"><span data-stu-id="721b0-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="721b0-120">Wenn **Verkäuflich** auf **Wahr** festgelegt ist, ist der Kontakt ein Verbraucher/Endbenutzer, und Angebote und Bestellungen können für diesen Kontakt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="721b0-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="721b0-121">Wenn **Verkäuflich** auf **Falsch** festgelegt ist, ist der Kontakt nur eine primäre Kontaktperson eines Debitors.</span><span class="sxs-lookup"><span data-stu-id="721b0-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="721b0-122">Wenn ein nicht-verkäuflicher Kontakt an einem Angebot oder Bestellprozess teilnimmt, wird **Verkäuflich** auf **Wahr** festgelegt, um den Kontakt als verkäuflichen Kontakt zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="721b0-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="721b0-123">Einem Kontakt, der ein verkäuflicher Kontakt wurde, bleibt ein verkäuflicher Kontakt.</span><span class="sxs-lookup"><span data-stu-id="721b0-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="721b0-124">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="721b0-124">Templates</span></span>

<span data-ttu-id="721b0-125">Debitorendaten enthalten alle Informationen über den Debitor, z. B. die Debitorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil, das Rechnungsprofil und den Treuestatus.</span><span class="sxs-lookup"><span data-stu-id="721b0-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="721b0-126">Eine Sammlung von Entitätszuordnungen arbeitet während der Interaktion der Debitorendaten zusammen, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="721b0-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="721b0-127">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="721b0-127">Finance and Operations apps</span></span> | <span data-ttu-id="721b0-128">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="721b0-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="721b0-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="721b0-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="721b0-130">CDS-Kontakte V2</span><span class="sxs-lookup"><span data-stu-id="721b0-130">CDS Contacts V2</span></span>             | <span data-ttu-id="721b0-131">Kontakte</span><span class="sxs-lookup"><span data-stu-id="721b0-131">contacts</span></span>                        | <span data-ttu-id="721b0-132">Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="721b0-133">Debitorengruppen</span><span class="sxs-lookup"><span data-stu-id="721b0-133">Customer groups</span></span>             | <span data-ttu-id="721b0-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="721b0-134">msdyn_customergroups</span></span>            | <span data-ttu-id="721b0-135">Diese Vorlage synchronisiert Debitorengruppeninformationen.</span><span class="sxs-lookup"><span data-stu-id="721b0-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="721b0-136">Zahlungsmethode für Debitoren</span><span class="sxs-lookup"><span data-stu-id="721b0-136">Customer payment method</span></span>     | <span data-ttu-id="721b0-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="721b0-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="721b0-138">Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Debitoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="721b0-139">Debitoren V3</span><span class="sxs-lookup"><span data-stu-id="721b0-139">Customers V3</span></span>                | <span data-ttu-id="721b0-140">Konten</span><span class="sxs-lookup"><span data-stu-id="721b0-140">accounts</span></span>                        | <span data-ttu-id="721b0-141">Diese Vorlage synchronisiert die Debitorenmasterinformationen für kommerzielle Debitoren und Geschäftsdebitoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="721b0-142">Debitoren V3</span><span class="sxs-lookup"><span data-stu-id="721b0-142">Customers V3</span></span>                | <span data-ttu-id="721b0-143">Kontakte</span><span class="sxs-lookup"><span data-stu-id="721b0-143">contacts</span></span>                        | <span data-ttu-id="721b0-144">Diese Vorlage synchronisiert Debitorenmasterdaten für Kunden und Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="721b0-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="721b0-145">Treuekarte</span><span class="sxs-lookup"><span data-stu-id="721b0-145">Loyalty card</span></span>                | <span data-ttu-id="721b0-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="721b0-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="721b0-147">Diese Vorlage synchronisiert Treukarteninformationen von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="721b0-148">Namensaffixe</span><span class="sxs-lookup"><span data-stu-id="721b0-148">Name affixes</span></span>                | <span data-ttu-id="721b0-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="721b0-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="721b0-150">Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="721b0-151">Zahlungstagpositionen CDS V2</span><span class="sxs-lookup"><span data-stu-id="721b0-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="721b0-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="721b0-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="721b0-153">Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="721b0-154">Zahlungstage CDS</span><span class="sxs-lookup"><span data-stu-id="721b0-154">Payment days CDS</span></span>            | <span data-ttu-id="721b0-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="721b0-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="721b0-156">Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="721b0-157">Zahlungsplanpositionen</span><span class="sxs-lookup"><span data-stu-id="721b0-157">Payment schedule lines</span></span>      | <span data-ttu-id="721b0-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="721b0-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="721b0-159">Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="721b0-160">Zahlungszeitplan</span><span class="sxs-lookup"><span data-stu-id="721b0-160">Payment schedule</span></span>            | <span data-ttu-id="721b0-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="721b0-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="721b0-162">Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="721b0-163">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="721b0-163">Terms of payment</span></span>            | <span data-ttu-id="721b0-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="721b0-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="721b0-165">Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="721b0-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
