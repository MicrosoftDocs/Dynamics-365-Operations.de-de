---
title: Inventarverfügbarkeit in dualem Schreiben
description: Dieser Artikel bietet Informationen zum Prüfen der Bestandverfügbarkeit in dualem Schreiben.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: efd175dfbe49549561bdb7d697c8bc47016f1d5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908261"
---
# <a name="inventory-availability-in-dual-write"></a>Inventarverfügbarkeit in dualem Schreiben

[!include [banner](../../includes/banner.md)]

Mithilfe der Bestandverfügbarkeit können Sie Ihr Inventar überprüfen, bevor Sie ein Produkt zu den Formularen **Zitate**, **Aufträge** oder **Rechnungen** in Microsoft Dynamics 365 Sales hinzufügen. Zum Beispiel ist die Überprüfung des Inventars und die Bestimmung eines Erfüllungstermins eine Schlüsselaufgabe in [Aussicht auf Bargeld](dual-write-prospect-to-cash.md) Prozess.

Wenn Sie nicht über genügend Bestand verfügen, können Sie einen Liefertermin basierend auf den projizierten Bestandeinnahmen und -Problemen schätzen. Sie können auch die ATP-Informationen des Produkts überprüfen, in denen Sie die ATP-Menge in dem vordefinierten Zeitrahmen finden.

## <a name="on-hand-inventory"></a>Verfügbarer Lagerbestand

In der Kopfzeile der Seiten **Angebote**, **Aufträge** und **Rechnungen** in Dynamics 365 Sales wurde eine neue Schaltfläche **Lagerbestand** hinzugefügt. Wenn Sie auf die Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen und das Produkt angeben können, für das Sie dann den Lagerbestand überprüfen möchten. Dieses Dialogfeld zeigt die gleichen Informationen wie [Lagerbestand](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Das Dialogfeld gibt die Inventarinformationen von Dynamics 365 Supply Chain Management zurück. Diese Informationen umfassen die folgenden Mengen:

- Verfügbare Menge
- Die verfügbare Menge in Reserve
- Die verfügbare Menge
- Bestellte Menge
- Die Auftragsmenge
- Reservierte bestellte Menge
- Die insgesamt verfügbare Menge

## <a name="atp-information"></a>VfZ-Informationen

In Sales wurde eine neue Schaltfläche **ATP-Informationen** wurde zu den Seite **Zitate**, **Aufträge**, und **Rechnungen** hinzugefügt. Wenn Sie auf diese Schaltfläche klicken, wird ein Dialogfeld angezeigt, in dem Sie das Unternehmen, Produkt, Lagerstandort, Lagerbestand und bestellte Menge angeben können.. Dieses Dialogfeld hat dieselben Einstellungen wie in [Bestellung vielversprechend](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Das Dialogfeld gibt die ATP-Informationen aus dem Supply Chain Management zurück. Diese Informationen umfassen die folgenden Mengen:

- VfZ-Menge
- Zugangsmenge
- Abgangsmenge
- Verfügbare Menge

## <a name="how-it-works"></a>Funktionsweise

Wenn Sie die Schaltfläche **Verfügbarer Bestand** auf der Seite **Angebote**, **Aufträge** oder **Rechnungen** auswählen, wird ein Live-Aufruf zum dualen Schreiben an die API **Verfügbarer Lagerbestand** durchgeführt. Die API berechnet den verfügbaren Lagerbestand für das jeweilige Produkt. Das Ergebnis wird in den Tabellen **InventCDSInventoryOnHandRequestEntity** und **InventCDSInventoryOnHandEntryEntity** gespeichert und dann mit dualem Schreiben in Dataverse geschrieben. Um diese Funktionalität nutzen zu können, müssen Sie die folgenden Zuordnungen für duales Schreiben ausführen. Überspringen Sie die anfängliche Synchronisierung, wenn Sie die Zuordnungen ausführen.

- Einträge zu verfügbarem CDS-Lagerbestand (msdyn_inventoryonhandentries)
- Anforderungen zu verfügbarem CDS-Lagerbestand (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Vorlagen

Die folgenden Vorlagen stehen zur Verfügung, um die Daten zu vorhandenen Lagerbestand verfügbar zu machen.

Finanz- und Betriebs-Apps | Customer Engagement-Apps     | Beschreibung
---|---|---
[Einträge für verfügbaren CDS-Bestand](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[Anfragen für verfügbaren CDS-Bestand](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
