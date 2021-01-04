---
title: Integrierte Masterdaten von Debitoren
description: In diesem Thema wird die Integration von Debitorendaten zwischen Finance and Operations und Dataverse beschrieben.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685638"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="c19a6-103">Integrierte Masterdaten von Debitoren</span><span class="sxs-lookup"><span data-stu-id="c19a6-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="c19a6-104">Kundendaten können in mehr als einer Dynamics 365 Anwendung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c19a6-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="c19a6-105">Beispielsweise kann eine Kundenzeile durch Verkaufsaktivitäten in Dynamics 365 Sales (eine modellgesteuerte App in Dynamics 365) oder eine Zeile durch Einzelhandelsaktivitäten in Dynamics 365 Commerce (eine Finance and Operations-App) entstehen.</span><span class="sxs-lookup"><span data-stu-id="c19a6-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="c19a6-106">Unabhängig davon, woher die Kundendaten stammen, werden sie im Hintergrund integriert.</span><span class="sxs-lookup"><span data-stu-id="c19a6-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="c19a6-107">Der integrierte Kundenstamm bietet Ihnen die Flexibilität, Kundendaten in jeder Dynamics 365 Anwendung zu verwalten, und bietet eine umfassende Ansicht des Kunden in der gesamten Dynamics 365 Anwendungssuite.</span><span class="sxs-lookup"><span data-stu-id="c19a6-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="c19a6-108">Debitorendatenfluss</span><span class="sxs-lookup"><span data-stu-id="c19a6-108">Customer data flow</span></span>

<span data-ttu-id="c19a6-109">*Debitor* ist ein gut definiertes Konzept in Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c19a6-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="c19a6-110">Daher umfasst die Integration von Debitorendaten nur die Harmonisierung des Debitorenkonzepts zwischen den beiden Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c19a6-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="c19a6-111">Die folgende Abbildung zeigt den Debitorendatenfluss.</span><span class="sxs-lookup"><span data-stu-id="c19a6-111">The following illustration shows the customer data flow.</span></span>

![Debitorendatenfluss](media/dual-write-customer-data-flow.png)

<span data-ttu-id="c19a6-113">Debitoren können in zwei Typen unterteilt werden: kommerzielle Debitoren/Unternehmensdebitoren und Verbraucher/Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="c19a6-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="c19a6-114">Diese beiden Arten von Debitoren werden in Finance and Operations und Dataverse unterschiedlich gespeichert und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c19a6-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="c19a6-115">In Finance and Operations werden sowohl kommerzielle Debitoren/Unternehmensdebitoren als auch Verbraucher/Endbenutzer in einer einzigen Tabelle mit dem Namen **CustTable** (CustCustomerV3Entity) verwaltet, und sie werden basierend auf dem **Type**-Attribut klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="c19a6-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="c19a6-116">(Wenn **Typ** auf **Organisation** festgelegt ist, ist der Debitor ein kommerzieller Debitor/Unternehmensdebitor, und wenn **Typ** auf **Person** festgelegt ist, so ist der Debitor ein Verbraucher/Endbenutzer.) Die primären Kontaktpersoninformationen werden über die SMMContactPersonEntity-Entität verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c19a6-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="c19a6-117">In Dataverse werden kommerzielle Debitoren/Unternehmensdebitoren in der Kontoentität verwaltet und als Debitoren identifiziert, wenn das **RelationshipType**-Attribute auf **Debitor** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c19a6-117">In Dataverse, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="c19a6-118">Sowohl Verbrauch/Endbenutzer als auch die Kontaktperson werden von der Kontaktentität dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c19a6-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="c19a6-119">Um eine klare Trennung zwischen einem Verbraucher/Endbenutzer und einer Kontaktperson zu haben, weist die **Kontakt**-Entität eine boolesche Markierung mit dem Namen **Verkäuflich** auf.</span><span class="sxs-lookup"><span data-stu-id="c19a6-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="c19a6-120">Wenn **Verkäuflich** auf **Wahr** festgelegt ist, ist der Kontakt ein Verbraucher/Endbenutzer, und Angebote und Bestellungen können für diesen Kontakt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c19a6-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="c19a6-121">Wenn **Verkäuflich** auf **Falsch** festgelegt ist, ist der Kontakt nur eine primäre Kontaktperson eines Debitors.</span><span class="sxs-lookup"><span data-stu-id="c19a6-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="c19a6-122">Wenn ein nicht-verkäuflicher Kontakt an einem Angebot oder Bestellprozess teilnimmt, wird **Verkäuflich** auf **Wahr** festgelegt, um den Kontakt als verkäuflichen Kontakt zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="c19a6-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="c19a6-123">Einem Kontakt, der ein verkäuflicher Kontakt wurde, bleibt ein verkäuflicher Kontakt.</span><span class="sxs-lookup"><span data-stu-id="c19a6-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="c19a6-124">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="c19a6-124">Templates</span></span>

<span data-ttu-id="c19a6-125">Debitorendaten enthalten alle Informationen über den Debitor, z. B. die Debitorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil, das Rechnungsprofil und den Treuestatus.</span><span class="sxs-lookup"><span data-stu-id="c19a6-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="c19a6-126">Eine Sammlung von Tabellenzuordnungen arbeitet während der Interaktion der Debitorendaten zusammen, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c19a6-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="c19a6-127">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="c19a6-127">Finance and Operations apps</span></span> | <span data-ttu-id="c19a6-128">Sonstige Dynamics 365-Apps</span><span class="sxs-lookup"><span data-stu-id="c19a6-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="c19a6-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c19a6-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="c19a6-130">CDS-Kontakte V2</span><span class="sxs-lookup"><span data-stu-id="c19a6-130">CDS Contacts V2</span></span>             | <span data-ttu-id="c19a6-131">Kontakte</span><span class="sxs-lookup"><span data-stu-id="c19a6-131">contacts</span></span>                        | <span data-ttu-id="c19a6-132">Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="c19a6-133">Debitorengruppen</span><span class="sxs-lookup"><span data-stu-id="c19a6-133">Customer groups</span></span>             | <span data-ttu-id="c19a6-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="c19a6-134">msdyn_customergroups</span></span>            | <span data-ttu-id="c19a6-135">Diese Vorlage synchronisiert Debitorengruppeninformationen.</span><span class="sxs-lookup"><span data-stu-id="c19a6-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="c19a6-136">Zahlungsmethode für Debitoren</span><span class="sxs-lookup"><span data-stu-id="c19a6-136">Customer payment method</span></span>     | <span data-ttu-id="c19a6-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="c19a6-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="c19a6-138">Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Debitoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="c19a6-139">Debitoren V3</span><span class="sxs-lookup"><span data-stu-id="c19a6-139">Customers V3</span></span>                | <span data-ttu-id="c19a6-140">Konten</span><span class="sxs-lookup"><span data-stu-id="c19a6-140">accounts</span></span>                        | <span data-ttu-id="c19a6-141">Diese Vorlage synchronisiert die Debitorenmasterinformationen für kommerzielle Debitoren und Geschäftsdebitoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="c19a6-142">Debitoren V3</span><span class="sxs-lookup"><span data-stu-id="c19a6-142">Customers V3</span></span>                | <span data-ttu-id="c19a6-143">Kontakte</span><span class="sxs-lookup"><span data-stu-id="c19a6-143">contacts</span></span>                        | <span data-ttu-id="c19a6-144">Diese Vorlage synchronisiert Debitorenmasterdaten für Kunden und Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="c19a6-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="c19a6-145">Namensaffixe</span><span class="sxs-lookup"><span data-stu-id="c19a6-145">Name affixes</span></span>                | <span data-ttu-id="c19a6-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="c19a6-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="c19a6-147">Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c19a6-148">Zahlungstagpositionen CDS V2</span><span class="sxs-lookup"><span data-stu-id="c19a6-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="c19a6-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="c19a6-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="c19a6-150">Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c19a6-151">Zahlungstage CDS</span><span class="sxs-lookup"><span data-stu-id="c19a6-151">Payment days CDS</span></span>            | <span data-ttu-id="c19a6-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="c19a6-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="c19a6-153">Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c19a6-154">Zahlungsplanpositionen</span><span class="sxs-lookup"><span data-stu-id="c19a6-154">Payment schedule lines</span></span>      | <span data-ttu-id="c19a6-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="c19a6-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="c19a6-156">Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c19a6-157">Zahlungszeitplan</span><span class="sxs-lookup"><span data-stu-id="c19a6-157">Payment schedule</span></span>            | <span data-ttu-id="c19a6-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="c19a6-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="c19a6-159">Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="c19a6-160">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="c19a6-160">Terms of payment</span></span>            | <span data-ttu-id="c19a6-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="c19a6-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="c19a6-162">Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c19a6-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
