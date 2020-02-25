---
title: Integrierte Masterdaten von Kreditoren
description: In diesem Thema wird die Integration von Lieferantendaten zwischen Finance and Operations Apps und Common Data Service beschrieben.
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
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019794"
---
# <a name="integrated-vendor-master"></a>Integrierte Masterdaten von Kreditoren

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Der Begriff *Kreditor* bezieht sich auf eine Lieferantenorganisation oder einen Einzelunternehmer, der Teil des Lieferkettenprozesses ist und der Waren an das Unternehmen liefert. Der Begriff *Lieferant* ist zwar in Finance and Operations Apps ein etabliertes Konzept, in Dynamics 365 Apps gibt es dieses Konzept aber nicht. Stattdessen überladen einige Unternehmen die Kontoentität, um sowohl Debitoreninformationen als auch Kreditoreninformationen zu speichern. Andere Unternehmen verwenden ein benutzerdefiniertes Kreditorenkonzept. Die Common Data Service-Integration unterstützt beide Entwürfe. Daher können Sie, je nach Ihrem Unternehmensszenario, einen der beiden Entwürfe aktivieren.

Durch die Integration von Lieferantendaten zwischen Finance and Operations Apps und anderen Dynamics 365-Apps können Sie für die Daten ein Multimastering ausführen. Unabhängig davon, woher die Kreditorendaten stammen, werden diese im Hintergrund über Anwendungsgrenzen und Infrastrukturunterschiede hinweg integriert. 

### <a name="vendor-data-flow"></a>Kreditorendatenfluss

Wenn Sie andere Dynamics 365-Apps für das Kreditoren-Mastering verwenden und die Kreditoreninformationen von Debitoreninformationen isolieren möchten, können Sie das neue Kreditorendesign verwenden.

![Kreditorendatenfluss](media/dual-write-vendor-data-flow.png)

Wenn Sie andere Dynamics 365-Apps für das Kreditoren-Mastering verwenden und weiterhin die Kontoentität zum Speichern der Kreditoreninformationen verwenden möchten, können Sie das neue erweiterte Kreditorendesign verwenden. In diesem Entwurf werden erweiterte Kreditordaten, z. B. das Kreditorengruppen- und das Kreditorenbuchungsprofil, in den Kreditorendetails gespeichert.

![Erweiterter Kreditorendatenfluss](media/dual-write-vendor-detail.jpg)

Die Kontaktinformationen des Kreditors ähneln den Kontaktinformationen des Debitors. Im Hintergrund werden die Informationen der Kontaktperson in den gleichen Entitäten gespeichert und aus den gleichen Entitäten abgerufen.

## <a name="templates"></a>Vorlagen

Kreditorendaten enthalten alle Informationen über den Kreditor, z. B. die Kreditorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil und das Rechnungsprofil. Eine Sammlung von Entitätszuordnungen arbeitet während der Interaktion der Kreditorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations Apps | Sonstige Dynamics 365-Apps         | Beschreibung
----------------------------|---------------------------------|------------
Kreditor V2               | Konto | Unternehmen, die die Kontoentität verwenden, um Kreditorendaten speichern, können diese weiterhin auf die gleiche Weise verwenden. Sie können auch die explizite Lieferantenfunktion nutzen, die dank der Integration von Finance and Operations Apps zur Verfügung stehen.
Kreditor V2               | Msdyn\_vendors | Unternehmen, die eine benutzerdefinierte Lösung für Lieferanten verwenden, können das vordefinierte Lieferantenkonzept nutzen, das in Common Data Service durch die Integration von Finance and Operations Apps eingeführt wird. 
Kreditorengruppen | msdyn_vendorgroups | Diese Vorlage synchronisiert Lieferantengruppeninformationen.
Kreditorzahlungsmethode | msdyn_vendorpaymentmethods | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Lieferanten.
CDS-Kontakte V2             | Kontakte                        | Die Vorlage [Kontakte](customer-mapping.md#cds-contacts-v2-to-contacts) synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Kunden und Lieferanten.
Zahlungsplanpositionen      | msdyn_paymentschedulelines      | Diese Vorlage [Zahlungsplanpositionen](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) synchronisiert die Referenzdaten für Kunden und Lieferanten.
Zahlungszeitplan            | msdyn_paymentschedules          | Die Vorlage [Zahlungspläne](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) synchronisiert die Referenzdaten für Zahlungspläne sowohl für Kunden als auch für Lieferanten.
Zahlungstagpositionen CDS V2    | msdyn_paymentdaylines           | Die Vorlage [Zahlungstagpositionen](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) synchronisiert die Referenzdaten für Zahlungstagpositionen für Kunden und Lieferanten.
Zahlungstage CDS            | msdyn_paymentdays               | Die Vorlage [Zahlungstage](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) synchronisiert die Referenzdaten für Zahlungstage sowohl für Kunden als auch für Lieferanten.
Zahlungsbedingungen            | msdyn_paymentterms              | Die Vorlage [Zahlungsbedingungen](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Kunden als auch für Lieferanten.
Namensaffixe                | msdyn_nameaffixes               | Die Vorlage [Namensaffixe](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) synchronisiert die Referenzdaten für Namensaffixe sowohl für Kunden als auch für Lieferanten.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
