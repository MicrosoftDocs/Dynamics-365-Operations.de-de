---
title: Fehlerbehebung bei Aufträgen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Aufträgen auftreten können.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824725"
---
# <a name="troubleshoot-sales-orders"></a>Fehlerbehebung bei Aufträgen

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Aufträgen auftreten können.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Die Steuerinformationen werden nicht aktualisiert, wenn ich den Standort in einem Auftragskopf ändere.

### <a name="issue-description"></a>Problembeschreibung

Wenn der Standort, das Lager oder die Lieferadresse entweder in einem Auftragskopf oder auf Positionsebene geändert wird, werden die Fallsteuerinformationen für die Positionen nicht automatisch aktualisiert.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Das Problem tritt auf, weil die Lieferadresse, der Standort und das Lager nicht auch automatisch auf Positionsebene geändert werden. Sie müssen sie manuell aktualisieren.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Wenn es zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume gibt, wird immer dieselbe Vertragsposition ausgewählt.

### <a name="issue-description"></a>Problembeschreibung

Wenn zwei Handelsvereinbarungen für denselben Zeitraum oder überlappende Zeiträume definiert sind, scheint jedes Mal, wenn Sie Auftragspositionen erstellen, die diese Artikel enthalten, dieselbe Handelsvereinbarung ausgewählt zu werden.

### <a name="issue-resolution"></a>Problemlösung

Wenn es für ein bestimmtes Datum mehr als eine Handelsvereinbarung gibt, wird immer die Handelsvereinbarung mit dem niedrigsten Preis ausgewählt. Laden Sie für weitere Informationen das folgende Whitepaper herunter: [Handelsvereinbarungen in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kann ich eine Bestellung mit einem Auftrag verknüpfen, um die Nachfrage zu befriedigen?

Sie können einer Bestellung auf Grundlage eines Auftrags erstellen. Weitere Informationen finden Sie unter [Erstellen einer Bestellung auf Grundlage eines Auftrags](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Ich kann eine Rücklieferung oder einen Auftrag nicht stornieren oder löschen.

Sie können nur Aufträge und Rücklieferungsaufträge stornieren, die sich im *Erstellt*-Zustand befinden. Weitere Informationen finden Sie unter [Stornieren einer Rücklieferung](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Wenn ich versuche, einen Auftrag zu stornieren, wird der Fehler „Reservierungen können nicht entfernt werden, da Arbeiten erstellt wurden, die auf den Reservierungen beruhen“ angezeigt.

Fehlercode: WAX4661

Wenn einem Auftrag eine Arbeit zugeordnet ist, können Sie den Auftrag erst stornieren, wenn die Arbeit storniert und entfernt wurde. Diese Anforderung gilt auch dann, wenn die mit dem Auftrag verbundene Arbeit abgeschlossen ist.

Führen Sie folgende Schritte aus, um dieses Problem zu beheben.

1. Stornieren Sie die Arbeit ab und legen Sie den Bestand wieder an den gewünschten Lagerplatz. Gehen Sie zur entsprechenden Auslastung des Auftrags und wählen Sie entweder **Entnommene Menge reduzieren** auf der Ladungsposition oder **Arbeit stornieren** im Aktionsbereich.

    Die Arbeit hat jetzt den Status *Storniert* und neue Bestandsbewegungsarbeiten werden automatisch erstellt und verarbeitet, um den Bestand wieder an den Lagerplatz zu bringen, der zum Zeitpunkt der Stornierung beschrieben wurde.

2. Löschen Sie die Auslastung. Die Lieferung wird ebenfalls gelöscht.
3. Sie sollten nun in der Lage sein, zum Auftrag zu gehen und ihn zu stornieren.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Ich kann eine Intercompany-Bestellung, die mit einem Auftrag verknüpft ist, nicht stornieren.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie versuchen, eine Intercompany-Bestellung zu stornieren, die mit einem Kundenauftrag verknüpft ist, wird möglicherweise die folgende Fehlermeldung angezeigt: „Die Menge kann nicht reduziert werden, da die verbleibende Aktualisierungsmenge das Vorzeichen ändert.“

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem wurde in Microsoft Dynamics 365 Supply Chain Management Version 10.0.13 behoben. In dieser und späteren Versionen können Sie jetzt eine Intercompany-Bestellung stornieren, die mit einem Kundenauftrag verknüpft ist.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kann ich einen in Rechnung gestellten Auftrag wiederherstellen, der gelöscht wurde?

### <a name="issue-description"></a>Problembeschreibung

Ein in Rechnung gestellter Auftrag wurde versehentlich gelöscht, und Sie möchten ihn wiederherstellen oder seine Details anzeigen.

### <a name="issue-resolution"></a>Problemlösung

Wenn der gelöschte Auftrag bereits in Rechnung gestellt wurde, gehen Sie zu **Kundenkonto \> Transaktionen \> Originaldokument \>Details anzeigen**. Suchen Sie die gesuchte Rechnung und wählen Sie sie aus, um die Details anzuzeigen. Diese Details enthalten die Auftragsreferenz. Sie sollten von der Seite auch auf die Auftragsdetails zugreifen können.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Die Frist eines Auftragskopfes kann nicht in der SalesOrderHeaderV2Entity-Datenentität gefunden werden.

Das Fristfeld existiert auf der *SalesOrderHeaderV2Entity*-Entität nicht.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Ich muss verwaiste Auftragsdatensätze löschen.

Führen Sie den periodischen Einzelvorgang *Auftragslöschung* aus, um verwaiste Auftragsdatensätze zu bereinigen, indem Sie zu einem der folgenden Orte gehen:

- Klicken Sie auf Vertrieb und Marketing \> Periodische Aufgaben \> Bereinigen \> Aufträge löschen
- Retail und Commerce \> Retail und Commerce IT \> Bereinigen \> Aufträge löschen

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Gibt es eine Möglichkeit, Provisionen für bereits gebuchte Rechnungen zu berechnen?

Supply Chain Management unterstützt derzeit die Berechnung von Provisionen für gebuchte Rechnungen nicht.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Ein Bündelartikel wird in einem Intercompany-Prozess nicht unterstützt.

Der Bündelartikel ist für die Bestellung nicht verfügbar, da Sie bei Prüfung der Auftragspositionen für den Bündelartikel feststellen werden, dass die Menge *0* (Null) und der Status *Storniert* ist. Dieses Verhalten ist beabsichtigt. Der Auftrag kauft nur die Komponenten des Bündelartikels. Der Bündelartikel selbst wird nicht gekauft.

Wenn Sie ein Bündel kaufen müssen, prüfen Sie, ob Sie es als Bündelartikel markieren müssen, da diese Funktion für Szenarien zur Umsatzrealisierung konzipiert ist. Weitere Informationen zu Bündelartikeln finden Sie unter [Bündel](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]