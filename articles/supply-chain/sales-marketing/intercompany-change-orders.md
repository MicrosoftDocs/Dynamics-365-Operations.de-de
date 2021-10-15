---
title: Intercompany-Aufträge ändern
description: In diesem Thema wird die Funktion zum Ändern von Intercompany-Aufträgen erläutert.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1129794bf0ac6513770f8b2a0eeb7fb6154d7942
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548296"
---
# <a name="change-intercompany-orders"></a>Intercompany-Aufträge ändern

[!include [banner](../../includes/banner.md)]

Beim Ändern von Intercompany-Aufträgen oder -Bestellungen spiegelt der entsprechende Auftrag oder die Bestellung im entsprechenden Unternehmen die Änderung ebenfalls wider.

## <a name="adding-new-lines"></a>Hinzufügen von neuen Positionen

Einem Intercompany-Auftrag und einer Intercompany-Bestellung können neue Positionen hinzugefügt werden, wenn der Originalauftrag Teil der Intercompany-Auftragskette ist. Neue Positionen können auch hinzugefügt werden, wenn der Originalauftrag keine Direktlieferung ist. Wenn der Originalauftrag eine Direktlieferung ist, können dem Intercompany-Auftrag und der Bestellung nur dann neue Auftragspositionen hinzugefügt werden, wenn das Feld **Indirekte Erstellung zulassen** im Inforegister **Intercompany-Einstellungen** auf dem ursprünglichen Auftrag ausgewählt ist.

## <a name="changing-prices-and-discounts"></a>Ändern von Preisen und Rabatten

Sie können die Preise und Rabatte ändern, wenn die Kontrollkästchen **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** auf der Seite **Intercompany** aktiviert sind.

Bei einer Änderung des Stückpreises einer der vorhandenen Positionen in der Intercompany-Auftragsposition wird auch der Stückpreis auf der Intercompany-Bestellung geändert.

Wenn Sie ein Rabattfeld in der Intercompany-Auftragsposition ändern, werden die relevanten Rabattfelder in der Intercompany-Bestellung aktualisiert.

## <a name="changing-and-adding-new-charges"></a>Ändern und Hinzufügen neuer Zuschläge

Sie können die Zuschläge ändern, wenn die Kontrollkästchen **Preisbearbeitung zulassen** und **Rabattbearbeitung zulassen** auf der Seite **Intercompany** aktiviert sind.

Wenn Sie dem Intercompany-Auftragskopf und der Intercompany-Auftragsposition einen neuen Zuschlag hinzufügen, werden beide Zuschläge in die Intercompany-Bestellung kopiert. Daher weisen der Intercompany-Auftrag und die Intercompany-Bestellung den gleichen Gesamtbetrag auf. Die Zuschläge werden nie in den Originalauftrag kopiert.

## <a name="copying-a-fee"></a>Kopieren einer Gebühr

Erstellen Sie zum Kopieren einer Gebühr in den Originalauftrag die Gebühr als neue Verkaufsposition mit einem Artikel vom Typ **Service**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Ändern von Mengen und Löschen von Intercompany-Bestellpositionen und -Auftragspositionen

Sie können nur dann die Menge ändern oder eine Intercompany-Bestellposition oder -Auftragsposition löschen, wenn die Position direkt im Formular **Auftrag** oder **Bestellung** erstellt wurde. Durch diese Änderung werden entweder die Intercompany-Bestellung bzw. der Auftrag oder die Positionen zur Quelle.

## <a name="origins-of-orders-and-order-lines"></a>Ursprung von Aufträgen und Auftragspositionen

Intercompany-Aufträge und Auftragspositionen können einen von zwei Ursprüngen aufweisen:

- **Abgeleitet** – Der Auftrag wurde automatisch aus einer Intercompany-Auftragskette erstellt.
- **Quelle** – Der Auftrag wurde manuell von einem Benutzer erstellt.

Der Ursprung wird im Auftragskopf von Intercompany-Aufträgen und -Bestellungen im Feld **Ursprung** angezeigt. Dieses Feld befindet sich im Auftrag im Inforegister **Intercompany-Einstellungen** und in der Bestellung im Inforegister **Einrichtung**.

Die Ursprünge **Abgeleitet** und **Quelle** gelten nur für Intercompany-Aufträge. Das Feld **Ursprung** ist daher für alle anderen Aufträge, Bestellungen und Auftragspositionen leer. Dieses Feld ist auch im Originalauftrag leer.

## <a name="example-derived-origin"></a>Beispiel: Ursprung „Abgeleitet“

Sie erstellen einen Originalauftrag für einen externen Debitor. Dieser Auftrag enthält eine Auftragsposition. Durch diesen Originalauftrag wird eine Intercompany-Bestellung mit einer Bestellposition erstellt, durch die ein Intercompany-Auftrag mit einer Auftragsposition erstellt wird. Die Intercompany-Bestellung und die Auftragsposition werden automatisch aus dem Originalauftrag erstellt.

Der Wert des Felds **Ursprung** im Inforegister **Einrichtung** der Intercompany-Bestellung und im Inforegister **Intercompany-Einstellungen** im Auftragskopf des Intercompany-Auftrags lautet **Abgeleitet**. Der Wert des Felds **Ursprung** auf der Registerkarte **Positionsdetails** der Bestell- und Auftragspositionen lautet ebenfalls **Abgeleitet**.

Wenn eine Auftragsposition den Ursprung **Abgeleitet** aufweist, kann sie nicht direkt gelöscht werden. Die Auftragsposition kann nur in der Quelle gelöscht werden, aus der sie erstellt wurde. Nur dort kann auch die bestellte Menge geändert werden.

Sind ein Originalauftrag und eine Originalauftragsposition Teil der Intercompany-Auftragskette, können bestellte Mengen im Originalauftrag geändert und Auftragspositionen aus dem Originalauftrag gelöscht werden.

## <a name="example-source-origin"></a>Beispiel: Ursprung „Quelle“

Sie erstellen eine Bestellung für einen Intercompany-Kreditor. Die Intercompany-Bestellung und die Bestellposition haben den Ursprung **Quelle**. Daher ist diese Intercompany-Bestellung der Controller, und der automatisch erstellte Intercompany-Auftrag im Unternehmen des Kreditors hat den Status **Abgeleitet**.

Darüber hinaus können die bestellten Mengen einer in der Intercompany-Bestellung erstellen Bestellposition nicht im Intercompany-Auftrag geändert werden. Die Bestellposition kann nur aus der Intercompany-Bestellung gelöscht werden. Wird dem Intercompany-Auftrag eine neue Position hinzugefügt, dann lautet der Ursprung dieses Intercompany-Auftrags **Quelle**.

Ist ein Originalauftrag Teil der Intercompany-Auftragskette, können die Intercompany-Aufträge und Intercompany-Auftragspositionen immer aus dem Originalauftrag gesteuert werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
