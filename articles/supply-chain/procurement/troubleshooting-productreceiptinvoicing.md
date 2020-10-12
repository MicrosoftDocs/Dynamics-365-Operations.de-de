---
title: Fehlerbehebung bei Produktzugängen und Fakturierung
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Produktzugängen und Fakturierung auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834364"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Fehlerbehebung bei Produktzugängen und Fakturierung

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Produktzugängen und Fakturierung auftreten können.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Ich kann nicht mehr als eine Rechnung für eine Bestellposition mit kategorienbasierten Artikeln buchen.

Eine Menge ist obligatorisch, wenn Sie Rechnungen buchen möchten. Wenn die gesamte Menge einer Position nur für einen Teilbetrag in Rechnung gestellt wurde, können Sie den verbleibenden Betrag nicht auf einer anderen Rechnung in Rechnung stellen.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Während der Bestellbestätigung wird der Fehler „Objektreferenz nicht festgelegt“ angezeigt, oder während der Buchung der Lieferantenrechnung tritt die Ausnahme „Ausnahme wurde vom Ziel eines Aufrufs ausgelöst“ auf.

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Ich kann nicht mehrere Produktzugänge in einer einzigen Bestellung zusammenfassen.

Sie können nicht mehrere Produktzugänge in einer Bestellung zusammenfassen, wenn die verschiedenen Produktzugangspositionen unterschiedliche Abrechnungsdaten haben.

In früheren Versionen von Microsoft Dynamics 365 Supply Chain Management war in dieser Situation eine Konsolidierung zulässig. Die Praxis ist jedoch fehleranfällig. Das Abrechnungsdatum in den erstellten Bestellpositionen sollte nicht vom Abrechnungsdatum in den Produktzugangspositionen abweichen, aus denen diese Bestellpositionen erstellt wurden. (Das Abrechnungsdatum in den Bestellpositionen stimmt mit dem Abrechnungsdatum im Bestellkopf überein.) Daher ist die Konsolidierung mehrerer Produkteingänge zu einer einzigen Bestellung nicht mehr zulässig.

Das Abrechnungsdatum wird beispielsweise für Budgetreservierungen und Belastungen verwendet. Daher sollte es beim Übergang vom Produktzugang zur Bestellung beibehalten werden.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Wenn Produktzugänge storniert werden, können Transaktionen auf ein gesperrtes Sachkonto gebucht werden.

### <a name="issue-description"></a>Problembeschreibung

Wenn ein Produktzugang storniert wird, können Transaktionen auf gesperrte Sachkonten gebucht werden, obwohl die Hauptkonten gesperrt sind.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Stellen Sie auf der **Lieferantenparameter**-Seite auf der Registerkarte **Allgemeines** sicher, dass die **Produktzugang auf Sachkonto buchen**-Option auf *Ja* festgelegt ist.
1. Erstellen Sie eine Bestellung und fügen Sie eine Bestellposition mit einer Menge von *1.000* für ein Produkt hinzu.
1. Bestätigen Sie die Bestellung.
1. Buchen Sie den Produktzugang und überprüfen Sie die Gutscheine.
1. Sperren Sie die relevanten Hauptkonten *200140* und *140200*.
1. Stornieren Sie den gebuchten Produktzugang.
1. Beachten Sie, dass Transaktionen auf die gesperrten Sachkonten gebucht werden können.

### <a name="issue-resolution"></a>Problemlösung

Transaktionen können auf die gesperrten Sachkonten gebucht werden, wenn Produktbelege storniert werden, da dieses Verhalten korrekte Buchungen ermöglicht.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Eine Produktzugangs-Belegnummer wird verbraucht, auch wenn während des Produktzugangs kein Finanzbeleg generiert wird.

Wenn die **Verbindlichkeiten bei Produktzugang abgrenzen**-Option für die Artikelmodellgruppe auf *Nein* festgelegt ist, werden keine Buchungen im Hauptbuch vorgenommen. Ein physisches Ereignis wird jedoch zum Zwecke der Abrechnung in einem Nebenbuch aufgezeichnet, und für dieses Ereignis ist eine Belegnummer erforderlich. Diese Belegnummer ist die Belegnummer, auf die in den Bestandstransaktionen verwiesen wird.

Wir empfehlen Ihnen, die **Verbindlichkeiten bei Produktzugang abgrenzen**-Option auf *Ja* festzulegen, wie im folgenden Blogbeitrag beschrieben: [Sonstige Zuschläge zum Zeitpunkt des Produktzugangs buchen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Das Konto „Auf Belastungskonto im Sachkonto buchen“-Einstellung ist nicht aktiviert.

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem tritt auf, wenn eine Bestellung in Rechnung gestellt wird, wenn die **Auf Belastungskonto im Sachkonto buchen**-Option auf der **Rechnung**-Registerkarte der **Lieferantenparameter**-Seite auf *Ja* festgelegt ist.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Wechseln Sie zu **Kreditoren \> Einstellung \> Kreditorenparameter**.
1. Legen Sie auf der **Rechnung**-Registerkarte die **Auf Belastungskonto im Sachkonto buchen**-Option auf *Ja* fest.
1. Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Buchung \> Buchung**.
1. Stellen Sie auf der **Bestellung**-Registerkarte sicher, dass Sie alle Positionen in den Kaufausgaben für das Produkt gelöscht haben.
1. Wechseln Sie zu **Kreditorenkonten \> Bestellungen \> Alle Bestellungen**.
1. Erstellen einer Bestellung. Wählen Sie in dem **Lieferantenkonto**-Feld *1001 Acme Büromaterial* aus.
1. Fügen Sie eine Bestellung mit den folgenden Einstellungen hinzu:

    - **Artikelnummer:** *D0011 Laserprojektor*
    - **Standort:** *1*
    - **Lagerort:** *11*
    - **Menge** *4*

1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kauf** in der Gruppe **Aktion** auf **Bestätigen**.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Empfangen** in der Gruppe **Generieren** auf **Produktzugang**.
1. Geben Sie im **Buchen des Produktzugangs**-Dialogfeld im **Produktzugang**-Feld eine beliebige Zahl ein und wählen Sie dann **OK**.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Rechnung** in der Gruppe **Generieren** **Rechnung** aus.
1. Geben Sie im **Nummer**-Feld eine beliebige Nummer als Rechnungsnummer ein.
1. Status des Abgleichs aktualisieren und buchen.
1. Beachten Sie, dass Sie jetzt die folgende Fehlermeldung erhalten, wenn Sie eine Rechnung aus einer Bestellung erstellen: „Kontonummer für den Transaktionstyp Einkaufsausgaben für Produkt ist nicht vorhanden.“

### <a name="issue-resolution"></a>Problemlösung

Dies hängt von den Parametereinstellungen für Rechnungen und Rechnungsgruppen ab. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Buchhaltung für Einkaufskosten und Bestandsabweichungen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
