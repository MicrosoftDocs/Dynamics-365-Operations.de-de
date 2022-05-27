---
title: Eine Intercompany-Bestellung zur internen Verwendung erstellen und abrechnen
description: In diesem Thema wird erläutert, wie Sie eine Intercompany-Bestellung zur internen Verwendung erstellen und abrechnen.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 52b58b2dcecd5d9a83a47b425d6fb13b36c40b60
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675878"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Eine Intercompany-Bestellung zur internen Verwendung erstellen und abrechnen

[!include [banner](../../includes/banner.md)]

Sie können eine Intercompany-Bestellung für einen Intercompany-Kreditor erstellen. Damit wird automatisch ein Intercompany-Auftrag beim Intercompany-Kreditor erstellt.

![Interner Intercompany-Kaufprozess](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Eine Intercompany-Bestellung und einen entsprechenden Intercompany-Auftrag erstellen

Führen Sie diese Schritte unter „Juristische Person AAA“ aus, wie in der Abbildung dargestellt.

1. Wählen Sie **Kreditorenkonten** \> **Bestellungen** \> **Alle Bestellungen** aus.
1. Erstellen Sie auf der Seite mit der Liste **Alle Bestellungen** eine Bestellung für einen Intercompany-Kreditor. Die Feldwerte werden vom Kreditorenkonto in die Bestellung kopiert.

    Da Sie mit einem Intercompany-Kreditor arbeiten, wird ein Intercompany-Auftrag in der juristischen Person erstellt, die dem Kreditor entspricht. Die Nummer des Intercompany-Auftrags kann die gleiche wie die Nummer der Intercompany-Bestellung sein, und sie kann die Kennung der juristischen Person beinhalten. Die Anzahlstruktur, die verwendet wird, hängt von der Auswahl im Feld **Nummerierung für Verkaufsaufträge** auf der Seite **Intercompany** ab. Wenn Sie beispielsweise die Bestellung „00029\_064“ unter „Juristische Person AAA“ erstellen, lautet die Auftragsnummer unter „Juristische Person BBB“ „AAA00029\_64“.

    In einer Informationsnachricht werden Sie darüber informiert, dass eine Intercompany-Bestellung und ein Intercompany-Auftrag erstellt wurden. Die Nachricht umfasst zu Informationszwecken die Intercompany-Auftragsnummer.

1. Fügen Sie der Bestellung Positionsartikel hinzu. Die entsprechenden Positionsartikel werden automatisch dem Intercompany-Auftrag hinzugefügt. Wenn ein Artikel nicht in der anderen juristischen Person vorhanden ist, wird eine Meldung angezeigt und Sie können den Artikel nicht der Bestellung hinzufügen. Um dieses Problem zu beheben, wechseln Sie zur anderen juristischen Person und geben Sie das Produkt dieser juristischen Person frei. Der Artikel wird verfügbar sein, um den Aufträgen dieser juristischen Person hinzugefügt zu werden. Anschließend wechseln Sie wieder zur juristischen Person der Bestellung und setzen das Hinzufügen von Positionsartikeln fort.
1. Wenn Sie fertig sind, Informationen zur Bestellung einzugeben, bestätigen Sie sie.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Intercompanylieferschein und die Debitorenrechnung verarbeiten

Führen Sie diese Schritte unter „Juristische Person BBB“ aus, wie in der Abbildung dargestellt.

1. Wechseln Sie zu **Debitoren \> Aufträge \> Alle Aufträge**.
1. Wählen Sie auf der Seite mit der Liste **Alle Aufträge** den Intercompany-Auftrag aus.
1. Wählen Sie im Aktionsbereich die Registerkarte **Entnehmen und verpacken** und dann die Option **Lieferschein** aus.
1. Aktivieren Sie das Kontrollkästchen **Buchung**.
1. Wählen Sie **OK** aus. Der Lieferschein wird unter „Juristische Person BBB“ gebucht.
1. Wählen Sie auf der Seite mit der Liste **Alle Aufträge** den Intercompany-Auftrag aus.
1. Wählen Sie im Aktionsbereich die Registerkarte **Rechnung** und dann **Rechnung** aus.
1. Aktivieren Sie das Kontrollkästchen **Buchung**.
1. Wählen Sie **OK** aus.

    Die Debitorenrechnung für den Intercompany-Auftrag wird unter „Juristische Person BBB“ gebucht.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Intercompanyproduktzugang und Kreditorenrechnung verarbeiten

Führen Sie diese Schritte unter „Juristische Person AAA“ aus, wie in der Abbildung dargestellt.

1. Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.
1. Wählen Sie auf der Seite mit der Liste **Alle Bestellungen** die Intercompany-Bestellung aus.
1. Wählen Sie im Aktionsbereich **Wareneingang** und dann **Produktzugang** aus. Der Produktzugang wird erstellt. Die Produktzugangsnummer ist mit der Intercompany-Lieferscheinnummer identisch.
1. Aktivieren Sie das Kontrollkästchen **Buchung**.
1. Wählen Sie **OK** aus.
1. Wählen Sie auf der Seite mit der Liste **Alle Bestellungen** die Intercompany-Bestellung aus.
1. Wählen Sie im Aktionsbereich **Rechnung** und dann **Rechnung** aus. Die Kreditorenrechnung wird erstellt. Die Kreditorenrechnungsnummer ist mit der Intercompany-Debitorenrechnungsnummer identisch.
1. Beenden Sie die Eingabe der Kreditorenrechnung, und buchen Sie sie anschließend.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
