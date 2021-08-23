---
title: Integrierte Masterdaten von Kreditoren
description: In diesem Thema wird die Integration von Lieferantendaten zwischen Finance and Operations Apps und Dataverse beschrieben.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0f3e4a2267dd80c0631f9d09e12907dd9a6b517b503b1c549d28c95b0789cab0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747540"
---
# <a name="integrated-vendor-master"></a>Integrierte Masterdaten von Kreditoren

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Der Begriff *Lieferant* bezieht sich auf eine Lieferantenorganisation oder einen Einzelunternehmer, der Waren oder Dienstleistungen an ein Unternehmen liefert. Der Begriff *Lieferant* ist zwar in Microsoft Dynamics 365 Supply Chain Management ein etabliertes Konzept, in Kundenbindungsapps gibt es dieses Konzept aber nicht. Sie können jedoch die Tabelle **Konto/Kontakt** zum Speichern von Lieferantendaten überladen. Die integrierten Masterdaten von Lieferanten führen ein explizites Lieferantenkonzept in Kundenbindungsapps ein. Sie können entweder das neue Lieferantendesign verwenden oder Lieferantendaten in der Tabelle **Konto/Kontakt** speichern. Duales Schreiben unterstützt beide Ansätze.

In beiden Ansätzen werden die Lieferantendaten zwischen Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, und Power Apps-Portalen integriert . In Supply Chain Management stehen die Daten für Workflows wie Bestellanforderungen und Bestellungen zur Verfügung.

## <a name="vendor-data-flow"></a>Kreditorendatenfluss

Wenn Sie Daten nicht in der Tabelle **Konto/Kontakt** in Dataverse speichern möchten, können Sie das neue Lieferantendesign verwenden.

![Kreditorendatenfluss.](media/dual-write-vendor-data-flow.png)

Wenn Sie Daten weiterhin in der Tabelle **Konto/Kontakt** speichern möchten, können Sie das erweiterte Lieferantendesign verwenden. Um das erweiterte Lieferantendesign zu verwenden, müssen Sie die Herstellerworkflows im Lösungspaket für duales Schreiben konfigurieren. Weitere Informationen finden Sie unter [Wechsel zwischen Kreditorendesigns](vendor-switch.md).

![Erweiterter Kreditorendatenfluss.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Wenn Sie Power Apps-Portale für Self-Service-Kreditoren verwenden, können die Kreditoreninformationen direkt an Finance and Operations-Apps weitergeleitet werden.

## <a name="templates"></a>Vorlagen

Kreditorendaten enthalten alle Informationen über den Kreditor, z. B. die Kreditorengruppe, Adressen, Kontaktinformationen, das Zahlungsprofil und das Rechnungsprofil. Eine Sammlung von Tabellenzuordnungen arbeitet während der Interaktion der Kreditorendaten zusammen, wie in der folgenden Tabelle dargestellt.

Finance and Operations-Apps | Customer Engagement-Apps     | Beschreibung
----------------------------|-----------------------------|------------
[CDS-Kontakte V2](mapping-reference.md#115) | Kontakte | Diese Vorlage synchronisiert alle primären, sekundären und tertiären Kontaktinformationen für Debitoren und Kreditoren.
[Namensaffixe](mapping-reference.md#155) | msdyn_nameaffixes | Diese Vorlage synchronisiert die Referenzdaten für Namensaffixe sowohl für Debitoren als auch für Kreditoren.
[Zahlungstagpositionen CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstagpositionen sowohl für Debitoren als auch für Kreditoren.
[Zahlungstage CDS](mapping-reference.md#158) | msdyn_paymentdays | Diese Vorlage synchronisiert die Referenzdaten für Zahlungstage sowohl für Debitoren als auch für Kreditoren.
[Zahlungsplanpositionen](mapping-reference.md#159) | msdyn_paymentschedulelines | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsplanpositionen sowohl für Debitoren als auch für Kreditoren.
[Zahlungszeitplan](mapping-reference.md#160) | msdyn_paymentschedules | Diese Vorlage synchronisiert die Referenzdaten für Zahlungspläne sowohl für Debitoren als auch für Kreditoren.
[Zahlungsbedingungen](mapping-reference.md#161) | msdyn_paymentterms | Diese Vorlage synchronisiert die Referenzdaten für Zahlungsbedingungen sowohl für Debitoren als auch für Kreditoren.
[Kreditoren V2](mapping-reference.md#202) | msdyn_vendors | Unternehmen, die eine benutzerdefinierte Lösung für Lieferanten verwenden, können das vordefinierte Lieferantenkonzept nutzen, das in Dataverse durch die Integration von Finance and Operations Apps eingeführt wird.
[Kreditorengruppen](mapping-reference.md#200) | msdyn_vendorgroups | Diese Vorlage synchronisiert Lieferantengruppeninformationen.
[Kreditorzahlungsmethode](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Diese Vorlage synchronisiert Informationen zu den Zahlungsmethoden für Lieferanten.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
