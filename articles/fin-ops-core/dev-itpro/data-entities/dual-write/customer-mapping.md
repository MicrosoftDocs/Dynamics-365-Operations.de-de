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
# <a name="integrated-customer-master"></a>Integrierte Masterdaten von Debitoren

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Kundendaten können in mehr als einer Dynamics 365 Anwendung verwaltet werden. Beispielsweise kann eine Kundenzeile durch Verkaufsaktivitäten in Dynamics 365 Sales (eine modellgesteuerte App in Dynamics 365) oder eine Zeile durch Einzelhandelsaktivitäten in Dynamics 365 Commerce (eine Finance and Operations-App) entstehen. Unabhängig davon, woher die Kundendaten stammen, werden sie im Hintergrund integriert. Der integrierte Kundenstamm bietet Ihnen die Flexibilität, Kundendaten in jeder Dynamics 365 Anwendung zu verwalten, und bietet eine umfassende Ansicht des Kunden in der gesamten Dynamics 365 Anwendungssuite.

## <a name="customer-data-flow"></a>Debitorendatenfluss

*Debitor* ist ein gut definiertes Konzept in Anwendungen. Daher umfasst die Integration von Debitorendaten nur die Harmonisierung des Debitorenkonzepts zwischen den beiden Anwendungen. Die folgende Abbildung zeigt den Debitorendatenfluss.

![Debitorendatenfluss](media/dual-write-customer-data-flow.png)

Debitoren können in zwei Typen unterteilt werden: kommerzielle Debitoren/Unternehmensdebitoren und Verbraucher/Endbenutzer. Diese beiden Arten von Debitoren werden in Finance and Operations und Dataverse unterschiedlich gespeichert und verarbeitet.

In Finance and Operations werden sowohl kommerzielle Debitoren/Unternehmensdebitoren als auch Verbraucher/Endbenutzer in einer einzigen Tabelle mit dem Namen **CustTable** (CustCustomerV3Entity) verwaltet, und sie werden basierend auf dem **Type**-Attribut klassifiziert. (Wenn **Typ** auf **Organisation** festgelegt ist, ist der Debitor ein kommerzieller Debitor/Unternehmensdebitor, und wenn **Typ** auf **Person** festgelegt ist, so ist der Debitor ein Verbraucher/Endbenutzer.) Die primären Kontaktpersoninformationen werden über die SMMContactPersonEntity-Entität verarbeitet.

In Dataverse werden kommerzielle Debitoren/Unternehmensdebitoren in der Kontoentität verwaltet und als Debitoren identifiziert, wenn das **RelationshipType**-Attribute auf **Debitor** festgelegt ist. Sowohl Verbrauch/Endbenutzer als auch die Kontaktperson werden von der Kontaktentität dargestellt. Um eine klare Trennung zwischen einem Verbraucher/Endbenutzer und einer Kontaktperson zu haben, weist die **Kontakt**-Entität eine boolesche Markierung mit dem Namen **Verkäuflich** auf. Wenn **Verkäuflich** auf **Wahr** festgelegt ist, ist der Kontakt ein Verbraucher/Endbenutzer, und Angebote und Bestellungen können für diesen Kontakt erstellt werden. Wenn **Verkäuflich** auf **Falsch** festgelegt ist, ist der Kontakt nur eine primäre Kontaktperson eines Debitors.

Wenn ein nicht-verkäuflicher Kontakt an einem Angebot oder Bestellprozess teilnimmt, wird **Verkäuflich** auf **Wahr** festgelegt, um den Kontakt als verkäuflichen Kontakt zu kennzeichnen. Einem Kontakt, der ein verkäuflicher Kontakt wurde, bleibt ein verkäuflicher Kontakt.

## <a name="templates"></a>Vorlagen

Debitorendaten enthalten alle Informationen über den Debitor, z. B. die Debitorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil, das Rechnungsprofil und den Treuestatus. Eine Sammlung von Tabellenzuordnungen arbeitet während der Interaktion der Debitorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations Apps | Sonstige Dynamics 365-Apps         | Beschreibung
----------------------------|---------------------------------|------------
CDS-Kontakte V2             | Kontakte                        | Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.
Debitorengruppen             | msdyn_customergroups            | Diese Vorlage synchronisiert Debitorengruppeninformationen.
Zahlungsmethode für Debitoren     | msdyn_customerpaymentmethods    | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Debitoren.
Debitoren V3                | Konten                        | Diese Vorlage synchronisiert die Debitorenmasterinformationen für kommerzielle Debitoren und Geschäftsdebitoren.
Debitoren V3                | Kontakte                        | Diese Vorlage synchronisiert Debitorenmasterdaten für Kunden und Endbenutzer.
Namensaffixe                | msdyn_nameaffixes               | Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.
Zahlungstagpositionen CDS V2    | msdyn_paymentdaylines           | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.
Zahlungstage CDS            | msdyn_paymentdays               | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.
Zahlungsplanpositionen      | msdyn_paymentschedulelines      | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.
Zahlungszeitplan            | msdyn_paymentschedules          | Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.
Zahlungsbedingungen            | msdyn_paymentterms              | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]