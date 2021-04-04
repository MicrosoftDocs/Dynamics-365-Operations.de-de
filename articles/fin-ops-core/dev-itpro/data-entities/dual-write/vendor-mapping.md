---
title: Integrierte Masterdaten von Kreditoren
description: In diesem Thema wird die Integration von Lieferantendaten zwischen Finance and Operations Apps und Dataverse beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 272962b58d8d654c2640a51ef2dbdcd1b05cf8c9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560312"
---
# <a name="integrated-vendor-master"></a>Integrierte Masterdaten von Kreditoren

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Der Begriff *Lieferant* bezieht sich auf eine Lieferantenorganisation oder einen Einzelunternehmer, der Waren oder Dienstleistungen an ein Unternehmen liefert. Der Begriff *Lieferant* ist zwar in Microsoft Dynamics 365 Supply Chain Management ein etabliertes Konzept, in in modellgesteuerten Apps in Dynamics 365 gibt es dieses Konzept aber nicht. Sie können jedoch die Tabelle **Konto/Kontakt** zum Speichern von Lieferantendaten überladen. Die integrierten Masterdaten von Kreditoren führen ein explizites Kreditorenkonzept in modellgesteuerten Apps in Dynamics 365 ein. Sie können entweder das neue Lieferantendesign verwenden oder Lieferantendaten in der Tabelle **Konto/Kontakt** speichern. Duales Schreiben unterstützt beide Ansätze.

In beiden Ansätzen werden die Lieferantendaten zwischen Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, und Power Apps-Portalen integriert . In Supply Chain Management stehen die Daten für Workflows wie Bestellanforderungen und Bestellungen zur Verfügung.

## <a name="vendor-data-flow"></a>Kreditorendatenfluss

Wenn Sie Daten nicht in der Tabelle **Konto/Kontakt** in Dataverse speichern möchten, können Sie das neue Lieferantendesign verwenden.

![Kreditorendatenfluss](media/dual-write-vendor-data-flow.png)

Wenn Sie Daten weiterhin in der Tabelle **Konto/Kontakt** speichern möchten, können Sie das erweiterte Lieferantendesign verwenden. Um das erweiterte Lieferantendesign zu verwenden, müssen Sie die Herstellerworkflows im Lösungspaket für duales Schreiben konfigurieren. Weitere Informationen finden Sie unter [Wechsel zwischen Kreditorendesigns](vendor-switch.md).

![Erweiterter Kreditorendatenfluss](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Wenn Sie Power Apps-Portale für Self-Service-Kreditoren verwenden, können die Kreditoreninformationen direkt an Finance and Operations-Apps weitergeleitet werden.

## <a name="templates"></a>Vorlagen

Kreditorendaten enthalten alle Informationen über den Kreditor, z. B. die Kreditorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil und das Rechnungsprofil. Eine Sammlung von Tabellenzuordnungen arbeitet während der Interaktion der Kreditorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations Apps | Sonstige Dynamics 365-Apps     | Beschreibung
----------------------------|-----------------------------|------------
Kreditor V2                   | Konto                     | Unternehmen, die die Tabelle „Konto“ verwenden, um Lieferantendaten zuspeichern, können diese weiterhin auf die gleiche Weise verwenden. Sie können auch die explizite Lieferantenfunktion nutzen, die dank der Integration von Finance and Operations Apps zur Verfügung stehen.
Kreditor V2                   | Msdyn\_vendors              | Unternehmen, die eine benutzerdefinierte Lösung für Lieferanten verwenden, können das vordefinierte Lieferantenkonzept nutzen, das in Dataverse durch die Integration von Finance and Operations Apps eingeführt wird. 
Kreditorengruppen               | msdyn\_vendorgroups         | Diese Vorlage synchronisiert Lieferantengruppeninformationen.
Kreditorzahlungsmethode       | msdyn\_vendorpaymentmethods | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Lieferanten.
CDS-Kontakte V2             | Kontakte                    | Die Vorlage [Kontakte](customer-mapping.md#cds-contacts-v2-to-contacts) synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Kunden und Lieferanten.
Zahlungsplanpositionen      | msdyn\_paymentschedulelines | Diese Vorlage [Zahlungsplanpositionen](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synchronisiert die Referenzdaten für Kunden und Lieferanten.
Zahlungsplan            | msdyn\_paymentschedules     | Die Vorlage [Zahlungspläne](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synchronisiert die Referenzdaten für Zahlungspläne sowohl für Kunden als auch für Lieferanten.
Zahlungstagpositionen CDS V2    | msdyn\_paymentdaylines      | Die Vorlage [Zahlungstagpositionen](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synchronisiert die Referenzdaten für Zahlungstagpositionen für Kunden und Lieferanten.
Zahlungstage CDS            | msdyn\_paymentdays          | Die Vorlage [Zahlungstage](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synchronisiert die Referenzdaten für Zahlungstage sowohl für Kunden als auch für Lieferanten.
Zahlungsbedingungen            | msdyn\_paymentterms         | Die Vorlage [Zahlungsbedingungen](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Kunden als auch für Lieferanten.
Namensaffixe                | msdyn\_nameaffixes          | Die Vorlage [Namensaffixe](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synchronisiert die Referenzdaten für Namensaffixe sowohl für Kunden als auch für Lieferanten.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]