---
title: Integrierte Masterdaten von Kreditoren
description: Dieser Artikel beschreibt die Integration von Kreditor-Daten zwischen Finanz- und Betriebs-Apps und Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112194"
---
# <a name="integrated-vendor-master"></a>Integrierte Masterdaten von Kreditoren

[!include [banner](../../includes/banner.md)]



Der Begriff *Lieferant* bezieht sich auf eine Lieferantenorganisation oder einen Einzelunternehmer, der Waren oder Dienstleistungen an ein Unternehmen liefert. Der Begriff *Lieferant* ist zwar in Microsoft Dynamics 365 Supply Chain Management ein etabliertes Konzept, in Kundenbindungsapps gibt es dieses Konzept aber nicht. Sie können jedoch die Tabelle **Konto/Kontakt** zum Speichern von Lieferantendaten überladen. Die integrierten Masterdaten von Lieferanten führen ein explizites Lieferantenkonzept in Kundenbindungsapps ein. Sie können entweder das neue Lieferantendesign verwenden oder Lieferantendaten in der Tabelle **Konto/Kontakt** speichern. Duales Schreiben unterstützt beide Ansätze.

In beiden Ansätzen werden die Lieferantendaten zwischen Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, und Power Apps-Portalen integriert . In Supply Chain Management stehen die Daten für Workflows wie Bestellanforderungen und Bestellungen zur Verfügung.

## <a name="vendor-data-flow"></a>Kreditorendatenfluss

Wenn Sie Daten nicht in der Tabelle **Konto/Kontakt** in Dataverse speichern möchten, können Sie das neue Lieferantendesign verwenden.

![Kreditorendatenfluss.](media/dual-write-vendor-data-flow.png)

Wenn Sie Daten weiterhin in der Tabelle **Konto/Kontakt** speichern möchten, können Sie das erweiterte Lieferantendesign verwenden. Um das erweiterte Lieferantendesign zu verwenden, müssen Sie die Herstellerworkflows im Lösungspaket für duales Schreiben konfigurieren. Weitere Informationen finden Sie unter [Wechsel zwischen Kreditorendesigns](vendor-switch.md).

![Erweiterter Kreditorendatenfluss.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Wenn Sie Power Apps-Portale für Self-Service Verkäufer verwenden, können die Informationen des Kreditors direkt in die Finanz- und Betriebs-Apps fließen.

## <a name="templates"></a>Vorlagen

Kreditorendaten enthalten alle Informationen über den Kreditor, z. B. die Kreditorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil und das Rechnungsprofil. Eine Sammlung von Tabellenzuordnungen arbeitet während der Interaktion der Kreditorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finanz- und Betriebs-Apps | Customer Engagement-Apps     | Beschreibung
----------------------------|-----------------------------|------------
[CDS-Kontakte V2](mapping-reference.md#115) | Kontakte | Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.
[Namensaffixe](mapping-reference.md#155) | msdyn_nameaffixes | Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.
[Zahlungstagpositionen CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.
[Zahlungstage CDS](mapping-reference.md#158) | msdyn_paymentdays | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.
[Zahlungsplanpositionen](mapping-reference.md#159) | msdyn_paymentschedulelines | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.
[Zahlungszeitplan](mapping-reference.md#160) | msdyn_paymentschedules | Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.
[Zahlungsbedingungen](mapping-reference.md#161) | msdyn_paymentterms | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.
[Kreditoren V2](mapping-reference.md#202) | msdyn_vendors | Unternehmen, die eine angepasste Lösung für Kreditor verwenden, können aufgrund der Integration von Finanz- und Betriebs-Apps die Vorteile des Out-of-Box-Konzepts für Kreditor nutzen, das in Dataverse eingeführt wird.
[Kreditorengruppen](mapping-reference.md#200) | msdyn_vendorgroups | Diese Vorlage synchronisiert Lieferantengruppeninformationen.
[Kreditorzahlungsmethode](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Lieferanten.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

