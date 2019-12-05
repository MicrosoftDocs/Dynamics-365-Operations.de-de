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
# <a name="integrated-customer-master"></a>Integrierte Masterdaten von Debitoren

[!include [banner](../includes/banner.md)]

Debitorendatensätze werden typischerweise in mehreren Anwendungen verwaltet. So kann eine Verkaufsaktivität kommerzielle Debitorendatensätze über eine Verkaufsanwendung übernehmen, und E-Commerce und Einzelhandelsverkäufe können Debitorendatensätze über eine Finance and Operations-Anwendung übernehmen. Unabhängig davon, woher der Debitorendatensatz stammt, wird er im Hintergrund über Anwendungsgrenzen und Infrastrukturunterschiede hinweg integriert. Integrierte Masterdaten von Debitoren sind bei der Verarbeitung von Multimasterszenarien behilflich und bieten eine umfassende Ansicht des Debitors in der Dynamics 365-Anwendungssuite.

## <a name="customer-data-flow"></a>Debitorendatenfluss

*Debitor* ist ein gut definiertes Konzept in Anwendungen. Daher umfasst die Integration von Debitorendaten nur die Harmonisierung des Debitorenkonzepts zwischen den beiden Anwendungen. Die folgende Abbildung zeigt den Debitorendatenfluss.

![Debitorendatenfluss](media/dual-write-customer-data-flow.png)

Debitoren können in zwei Typen unterteilt werden: kommerzielle Debitoren/Unternehmensdebitoren und Verbraucher/Endbenutzer. Diese beiden Arten von Debitoren werden in Finance and Operations and Common Data Service unterschiedlich gespeichert und verarbeitet.

In Finance and Operations werden sowohl kommerzielle Debitoren/Unternehmensdebitoren als auch Verbraucher/Endbenutzer in einer einzigen Tabelle mit dem Namen **CustTable** (CustomerCustomerV3Entity) verwaltet, und sie werden basierend auf dem **Type**-Attribut klassifiziert. (Wenn **Typ** auf **Organisation** festgelegt ist, ist der Debitor ein kommerzieller Debitor/Unternehmensdebitor, und wenn **Typ** auf **Person** festgelegt ist, so ist der Debitor ein Verbraucher/Endbenutzer.) Die primären Kontaktpersoninformationen werden über die SMMContactPersonEntity-Entität verarbeitet.

In Common Data Service werden kommerzielle Debitoren/Unternehmensdebitoren in der Kontoentität verwaltet und als Debitoren identifiziert, wenn das **RelationshipType**-Attribute auf **Debitor** festgelegt ist. Sowohl Verbrauch/Endbenutzer als auch die Kontaktperson werden von der Kontaktentität dargestellt. Um eine klare Trennung zwischen einem Verbraucher/Endbenutzer und einer Kontaktperson zu haben, weist die **Kontakt**-Entität eine boolesche Markierung mit dem Namen **Verkäuflich** auf. Wenn **Verkäuflich** auf **Wahr** festgelegt ist, ist der Kontakt ein Verbraucher/Endbenutzer, und Angebote und Bestellungen können für diesen Kontakt erstellt werden. Wenn **Verkäuflich** auf **Falsch** festgelegt ist, ist der Kontakt nur eine primäre Kontaktperson eines Debitors.

Wenn ein nicht-verkäuflicher Kontakt an einem Angebot oder Bestellprozess teilnimmt, wird **Verkäuflich** auf **Wahr** festgelegt, um den Kontakt als verkäuflichen Kontakt zu kennzeichnen. Einem Kontakt, der ein verkäuflicher Kontakt wurde, bleibt ein verkäuflicher Kontakt.

## <a name="templates"></a>Vorlagen

Debitorendaten enthalten alle Informationen über den Debitor, z. B. die Debitorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil, das Rechnungsprofil und den Treuestatus. Eine Sammlung von Entitätszuordnungen arbeitet während der Interaktion der Debitorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations-Apps | Sonstige Dynamics 365-Apps         | Beschreibung
----------------------------|---------------------------------|------------
CDS-Kontakte V2             | Kontakte                        | Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.
Debitorengruppen             | msdyn_customergroups            | Diese Vorlage synchronisiert Debitorengruppeninformationen.
Zahlungsmethode für Debitoren     | msdyn_customerpaymentmethods    | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Debitoren.
Debitoren V3                | Konten                        | Diese Vorlage synchronisiert die Debitorenmasterinformationen für kommerzielle Debitoren und Geschäftsdebitoren.
Debitoren V3                | Kontakte                        | Diese Vorlage synchronisiert Debitorenmasterdaten für Kunden und Endbenutzer.
Treuekarte                | msdyn_loyaltycards              | Diese Vorlage synchronisiert Treukarteninformationen von Debitoren.
Namensaffixe                | msdyn_nameaffixes               | Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.
Zahlungstagpositionen CDS V2    | msdyn_paymentdaylines           | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.
Zahlungstage CDS            | msdyn_paymentdays               | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.
Zahlungsplanpositionen      | msdyn_paymentschedulelines      | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.
Zahlungszeitplan            | msdyn_paymentschedules          | Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.
Zahlungsbedingungen            | msdyn_paymentterms              | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.

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
