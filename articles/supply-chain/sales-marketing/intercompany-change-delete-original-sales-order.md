---
title: Einen ursprünglichen Intercompany-Auftrag ändern oder löschen
description: In diesem Artikel wird das Ändern und Löschen einer Funktion für ursprüngliche Aufträge erläutert.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6ff7eeb00fec7c1b9fa1dc08fa231669f728ed3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859076"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Einen ursprünglichen Intercompany-Auftrag ändern oder löschen

[!include [banner](../../includes/banner.md)]

Wenn Sie einen Auftrag ändern, werden die Änderungen automatisch sowohl mit der relevanten Intercompany-Bestellung als auch mit dem Intercompany-Auftrag synchronisiert.

> [!NOTE]
> Bestellungen für externe Kreditoren sind von diesen Änderungen ebenso wenig betroffen wie die Originalauftragspositionen in Verbindung mit Bestellpositionen für externe Kreditoren.

Die folgende Tabelle fasst die Änderungen, die Sie vornehmen können, und die erwarteten Ergebnisse zusammen.

| Vorgang | Ergebnis |
|---|---|
| Einen&nbsp;Originalauftrag&nbsp;löschen | Die zugehörige Intercompany-Bestellung und der Intercompany-Auftrag werden ebenfalls gelöscht. Wenn der Status der Auftrags **Kommissionierliste** lautet oder der Vorgang noch weiter fortgeschritten ist, kann die Auftragsposition nicht mehr gelöscht werden. |
| Eine Originalauftragsposition löschen | Die zugehörige Intercompany-Bestellposition und die Intercompany-Auftragsposition werden ebenfalls gelöscht. Wenn der Status der Auftrags **Kommissionierliste** lautet oder der Vorgang noch weiter fortgeschritten ist, kann die Auftragsposition nicht mehr gelöscht werden. |
| Einem Originalauftrag eine neue Auftragsposition hinzufügen | Die neue Auftragsposition wird sowohl in der Intercompany-Bestellung als auch im Intercompany-Auftrag erstellt. |
| Die Menge einer Originalauftragsposition ändern | Die Menge wird sowohl mit der Intercompany-Bestellposition als auch mit der Intercompany-Auftragsposition synchronisiert. Der Nettobetrag wird für alle Aufträge neu berechnet. |
| Die Option „Direktlieferung“ auf einem Originalauftrag deaktivieren | Sie können das Feld **Direktlieferung** des Originalauftrags nicht mehr ändern, wenn die Intercompany-Auftragsposition mindestens den Status **Kommissionierliste**, **Abgangsauftrag** oder **Kommissionierlistenerfassung** erreicht hat. Die Lieferadresse auf der Intercompany-Bestellung wird in die Standardlieferadresse geändert (Standardlieferadresse für Bestellung). Die Intercompany-Bestellpositionen werden ebenfalls in die Standardlieferadresse für die Positionen geändert. Beide Änderungen werden mit dem Intercompany-Auftrag und den Auftragspositionen synchronisiert. Der Liefertyp für alle Positionen auf dem Originalauftrag wird in **Kein** geändert, und das Feld wird mit den Intercompany-Bestellpositionen synchronisiert. Bestellungen für externe Kreditoren sind ebenso wenig betroffen wie die Originalauftragspositionen in Verbindung mit Bestellpositionen für externe Kreditoren. Das Lieferdatum auf der Intercompany-Bestellung und in den Bestellpositionen – und das angeforderte Wareneingangsdatum/Versanddatum auf dem Intercompany-Auftrag und in den Auftragspositionen – wird aktualisiert. |
| Die Option „Direktlieferung“ auf einem Originalauftrag aktivieren | Sie können das Feld **Direktlieferung** des Originalauftrags nicht ändern, wenn die Intercompany-Auftragsposition mindestens den Status **Kommissionierliste**, **Abgangsauftrag** oder **Kommissionierlistenerfassung** erreicht hat. Die Lieferadresse auf der Intercompany-Bestellung wird in die Lieferadresse aus dem Originalauftrag geändert und mit dem Intercompany-Auftrag synchronisiert. Der Liefertyp für alle Positionen auf dem Originalauftrag wird in **Direktlieferung** geändert, und das Feld wird mit den Intercompany-Bestellpositionen synchronisiert. Die Lieferadresse in jeder Originalauftragsposition wird sowohl mit den Intercompany-Bestellpositionen als auch mit den Intercompany-Auftragspositionen synchronisiert. Das Lieferdatum auf der Intercompany-Bestellung und in den Bestellpositionen – und das angeforderte Wareneingangsdatum/Versanddatum auf dem Intercompany-Auftrag und in den Auftragspositionen – wird aktualisiert. |
| Einen Hinweis im Kopf des Originalauftrags und in den Auftragspositionen hinzufügen | Der Hinweis wird in die Intercompany-Bestellung und in den Intercompany-Auftrag kopiert. |
| Einen Hinweis ändern oder löschen | Wenn Sie einen Hinweis ändern oder löschen, wird der entsprechende Hinweis auf der Intercompany-Bestellung und dem Intercompany-Auftrag ebenfalls geändert oder gelöscht. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
