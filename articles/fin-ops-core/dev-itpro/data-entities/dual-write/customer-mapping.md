---
title: Integrierte Masterdaten von Debitoren
description: Dieser Artikel beschreibt die Integration von Debitorendaten zwischen Finanzen und Betrieb und Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ea142aff7c8f4b442d7224325e44359129efe8a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289679"
---
# <a name="integrated-customer-master"></a>Integrierte Masterdaten von Debitoren

[!include [banner](../../includes/banner.md)]



Kundendaten können in mehr als einer Dynamics 365 Anwendung verwaltet werden. Beispielsweise kann eine Kundenzeile durch Verkaufsaktivitäten in Dynamics 365 Sales (eine Kundenbindungs-App) oder eine Zeile durch Einzelhandelsaktivitäten in Dynamics 365 Commerce (eine Finanz- und Betriebs-App) entstehen. Die Kundendaten werden im Hintergrund integriert, unabhängig davon, woher sie stammen. Der integrierte Kundenstamm bietet Ihnen die Flexibilität, Kundendaten in jeder Dynamics 365 Anwendung zu verwalten, und bietet eine umfassende Ansicht des Kunden in der gesamten Dynamics 365 Anwendungssuite.

## <a name="customer-data-flow"></a>Debitorendatenfluss

*Debitor* ist ein gut definiertes Konzept in Anwendungen. Daher umfasst die Integration von Debitorendaten nur die Harmonisierung des Debitorenkonzepts zwischen den beiden Anwendungen. Die folgende Abbildung zeigt den Debitorendatenfluss.

![Debitorendatenfluss.](media/dual-write-customer-data-flow.png)

Debitoren können in zwei Typen unterteilt werden: kommerzielle Debitoren/Unternehmensdebitoren und Verbraucher/Endbenutzer. Diese beiden Arten von Debitor werden in Finanzen und Betrieb und Dataverse unterschiedlich gespeichert und behandelt.

In Finanzen und Betrieb werden sowohl gewerbliche/organisatorische Debitor als auch Verbraucher/Endbenutzer in einer einzigen Tabelle mit dem Namen **CustTable** (CustCustomerV3Entity) verwaltet und anhand des Attributs **Type** klassifiziert. (Wenn **Typ** auf **Organisation** festgelegt ist, ist der Debitor ein kommerzieller Debitor/Unternehmensdebitor, und wenn **Typ** auf **Person** festgelegt ist, so ist der Debitor ein Verbraucher/Endbenutzer.) Die primären Kontaktpersoninformationen werden über die SMMContactPersonEntity-Tabelle verarbeitet.

In Dataverse werden kommerzielle Debitoren/Unternehmensdebitoren in der Kontotabelle verwaltet und als Debitoren identifiziert, wenn das **RelationshipType**-Attribut auf **Debitor** festgelegt ist. Sowohl Verbraucher/Endbenutzer als auch die Kontaktperson werden von der Kontakttabelle dargestellt. Um eine klare Trennung zwischen einem Verbraucher/Endbenutzer und einer Kontaktperson zu haben, weist die **Kontakt**-Tabelle eine boolesche Markierung mit dem Namen **Verkäuflich** auf. Wenn **Verkäuflich** auf **Wahr** festgelegt ist, ist der Kontakt ein Verbraucher/Endbenutzer, und Angebote und Bestellungen können für diesen Kontakt erstellt werden. Wenn **Verkäuflich** auf **Falsch** festgelegt ist, ist der Kontakt nur eine primäre Kontaktperson eines Debitors.

Wenn ein nicht-verkäuflicher Kontakt an einem Angebot oder Bestellprozess teilnimmt, wird **Verkäuflich** auf **Wahr** festgelegt, um den Kontakt als verkäuflichen Kontakt zu kennzeichnen. Einem Kontakt, der ein verkäuflicher Kontakt wurde, bleibt ein verkäuflicher Kontakt.

## <a name="templates"></a>Vorlagen

Debitorendaten enthalten alle Informationen über den Debitor, z. B. die Debitorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil, das Rechnungsprofil und den Treuestatus. Eine Sammlung von Tabellenzuordnungen arbeitet während der Interaktion der Debitorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finanz- und Betriebs-Apps | Customer Engagement-Apps         | Beschreibung
----------------------------|---------------------------------|------------
[CDS-Kontakte V2](mapping-reference.md#115) | Kontakte | Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.
[Debitorengruppen](mapping-reference.md#126) | msdyn_customergroups | Diese Vorlage synchronisiert Debitorengruppeninformationen.
[Zahlungsmethode für Debitoren](mapping-reference.md#127) | msdyn_customerpaymentmethods | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Debitoren.
[Debitoren V3](mapping-reference.md#101) | Konten | Diese Vorlage synchronisiert die Debitorenmasterinformationen für kommerzielle Debitoren und Geschäftsdebitoren.
[Debitoren V3](mapping-reference.md#116) | Kontakte | Diese Vorlage synchronisiert Debitorenmasterdaten für Kunden und Endbenutzer.
[Namensaffixe](mapping-reference.md#155) | msdyn_nameaffixes | Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.
[Zahlungstagpositionen CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.
[Zahlungstage CDS](mapping-reference.md#158) | msdyn_paymentdays | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.
[Zahlungsplanpositionen](mapping-reference.md#159) | msdyn_paymentschedulelines | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.
[Zahlungszeitplan](mapping-reference.md#160) | msdyn_paymentschedules | Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.
[Zahlungsbedingungen](mapping-reference.md#161) | msdyn_paymentterms | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

