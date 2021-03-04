---
title: Fehlerbehebung bei Bestellungen
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestellungen auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
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
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429126"
---
# <a name="troubleshoot-purchase-orders"></a>Fehlerbehebung bei Bestellungen

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Bestellungen auftreten können.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Eine Aktion kann erst abgeschlossen werden, nachdem die Positionsnummer vollständig verteilt wurde.

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Wenn Bestellungen über die Datenverwaltung importiert werden, folgen die Bestellpositionsnummern nicht dem in den Systemparametern definierten Inkrement.

### <a name="issue-description"></a>Problembeschreibung

Standardmäßig verwenden automatisch generierte Positionsnummern für Bestellpositionen, die über die *Bestellpositionen V2*-Datenentität importiert werden nicht das in den Systemparametern angegebene Systempositionsnummerninkrement. Wenn Sie manuell eine Bestellung erstellen und Positionen über die Benutzeroberfläche hinzufügen, werden die Positionsnummern korrekt erhöht. Wenn Sie jedoch das Datenverwaltungs-Framework (DMF) verwenden, werden sie nicht korrekt inkrementiert.

Dieses Problem tritt auf, weil das System beim Importieren von Positionen über DMF die DMF-Methode zum Zuweisen verwendet, wenn in der importierten Entität noch keine Positionsnummern zugewiesen sind. Diese Methode erhöht die Positionsnummern immer um eins.

### <a name="issue-workaround"></a>Problemumgehung

Stellen Sie sicher, dass die gewünschten Positionsnummern bereits in den Feldern für Positionsnummern der Datenentität angegeben sind, wenn Sie die Bestellpositionen importieren. In diesem Fall überschreibt DMF die Positionsnummern nicht.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Eine Standardsteuergruppe und ein Standard-Skonto werden nicht vom Rechnungskonto ausgefüllt.

Wenn Sie ein vom Kundenkonto abweichendes Rechnungskonto verwenden, werden beim Erstellen einer Bestellung weder eine Standardsteuergruppe noch ein Standard-Skonto vom Rechnungskonto ausgefüllt.

Dieses Verhalten ist beabsichtigt. Die Standardwerte für die Steuergruppe, Skonti und andere Preisinformationen basieren auf dem Kundenkonto und nicht auf dem Rechnungskonto.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Während der Bestellbestätigung wird der Fehler „Objektreferenz nicht festgelegt“ angezeigt, oder während der Buchung der Lieferantenrechnung tritt die Ausnahme „Ausnahme wurde vom Ziel eines Aufrufs ausgelöst“ auf.

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Eine oder mehrere Buchhaltungsverteilungen sind entweder über- oder unterverteilt.

### <a name="issue-description"></a>Problembeschreibung

Sie erhalten folgenden Fehler: „Mindestens eine Buchhaltungsverteilungen ist entweder über- oder unterverteilt.“

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem kann aufgrund von Inkonsistenzen bei der Verteilung von Bestellungen auftreten.

So entsperren Sie dieses Problem und setzen die Bestellung auf den *Entwurf*-Zustand zurück. Gehen Sie zu **Beschaffung \> Periodische Aufgaben \> Bereinigen \> Zurücksetzen der Bestellverteilung**. Weitere Informationen finden Sie im folgenden Blog-Beitrag: [Beheben von Bestellungsverteilungsfehlern in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kann ich nur Bestellungen anzeigen, die ich erstellt habe?

Diese Funktionalität ist derzeit nicht verfügbar.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kann ich Bestand reservieren und Transaktionen mit dem registrierten Bestand einer Bestellung erstellen?

### <a name="issue-description"></a>Problembeschreibung

Auch wenn Artikel in einem *Erfasst*-Zustand auf einer Bestellung sind, können Sie den Bestand trotzdem reservieren. Mit anderen Worten, Sie können Transaktionen für den registrierten Bestand erstellen.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Erstellen einer Bestellung.
2. Registrieren Sie die Bestellposition.
3. Beachten Sie, dass Sie Reservierungen oder Transaktionen für den registrierten Bestand generieren können.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Es wird erwartet, dass die registrierten Artikel physisch im Lagerort oder im Bestand angekommen sind und daher für eine Reservierung verfügbar sind.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Bestellungen spiegeln nicht die Spracheinstellungen der juristischen Person wider.

### <a name="issue-description"></a>Problembeschreibung

Der Produktname einer Bestellung wird in der Systemsprache anstelle der Sprache angezeigt, die für die juristische Person festgelegt wurde, in der die Bestellung erstellt wurde.

### <a name="reproduce-the-issue"></a>Reproduzieren Sie das Problem

Das folgende Verfahren veranschaulicht eine Möglichkeit, das Problem zu reproduzieren.

1. Stellen Sie die Systemsprache auf *EN-US* (Amerikanisches Englisch) ein.
1. Stellen Sie sicher, dass es ein Produkt gibt, in dem die *EN-US* und *DE* (Deutschland)-Sprachen für die Übersetzung des Produktnamens gepflegt werden.
1. Ändern Sie die Sprache einer juristischen Person in *DE*.
1. In der juristischen Person, in der *DE* als Sprache festgelegt ist, erstellen Sie eine Bestellung, die das Produkt enthält.
1. Beachten Sie, dass der Produktname weiterhin in US-Englisch (der Systemsprache) angezeigt wird.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Bei Bestellungen wird das Produkt immer in der Systemsprache angezeigt. Die Bestellsprache wird verwendet, wenn ein Bestätigungsjournal erstellt wird.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>In der Liste der genehmigten Lieferanten nach Produktentitäten kann das Datum des Inkrafttretens nicht geändert werden.

### <a name="issue-description"></a>Problembeschreibung

Ein Produkt hat einen genehmigten Lieferanten, der beispielsweise ein Datum des Inkrafttretens am 11. Januar 2018 hat (*01/11/2018*) und ein Ablaufdatum von *Niemals*. Wenn Sie versuchen, das Datum des Inkrafttretens auf den 10. Januar 2018 (*01/10/2018*) oder den 12. Januar 2018 (*01/12/2018*) zu ändern, erhalten Sie folgende Fehlermeldung:

> In der Liste der genehmigten Lieferanten (PdsApproveVendorList) kann kein Datensatz erstellt werden. Der Wert 'Ablauf' muss größer oder gleich dem Wert 'Effektiv' sein.

### <a name="issue-resolution"></a>Problemlösung

Sie können nur den Zeitraum verlängern, für den der Lieferant zugelassen ist. Dabei gelten folgende Regeln:

- Um das Datum des Inkrafttretens so zu ändern, dass es vor den vorhandenen Datensätzen (Zeiträumen) des Artikelanbieters liegt, muss das Ablaufdatum des neuen Zeitraums vor allen Ablaufdaten in den vorhandenen Datensätzen liegen.
- Um das Ablaufdatum so zu ändern, dass es nach einem der vorhandenen Zeiträume liegt, muss das Datum des Inkrafttretens in jedem vorhandenen Datensatz nach dem letzten Ablaufdatum liegen.
- Um den Gesamtzeitraum zu verkürzen, für den der Lieferant zugelassen ist, müssen Sie vorhandene Datensätze löschen oder ändern. Alternativ können Sie während des Imports den **kürzen**-Umschalter verwenden. Dieser Schalter löscht alle vorhandenen Datensätze in der Tabelle für genehmigte Lieferanten nach Artikel.

Für das in der Problembeschreibung beschriebene Beispielszenario, in dem ein Datensatz das Datum des Inkrafttretens von *01/11/2018* hat und ein Ablaufdatum von *Niemals*, können Sie einen neuen Datensatz mit dem Datum des Inkrafttretens von *01/10/2018* und ein Ablaufdatum von *Niemals* importieren. Sie können den Zeitraum jedoch nicht verkürzen, sodass das Datum des Inkrafttretens über die Datenverwaltung auf *01/12/2018* aktualisiert wird. Sie müssen diese Änderung über die Benutzeroberfläche vornehmen.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a>Nachdem ich die Lieferadresse in einem Bestellkopf geändert habe, wird der Lieferungsname nicht synchronisiert.

### <a name="issue-description"></a>Problembeschreibung

Die Adresse in der Kopfzeile einer Bestellung wird auf eine Adresse aktualisiert, die keine Lieferadresse ist. Obwohl die Adresse in der Bestellung aktualisiert wird, wird der Lieferungsname nicht basierend auf der aktualisierten Adresse aktualisiert.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist beabsichtigt. Die ausgewählte Adresse muss als Lieferadresse klassifiziert werden. Andernfalls wird der Lieferungsname nicht basierend auf der ausgewählten Adresse aktualisiert.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kann ich den Benutzer finden, der eine Bestellung storniert hat?

Diese Information wird nur verfolgt, wenn die Bestellung der Änderungsverwaltung unterliegt. Wenn Sie die Änderungsverwaltung verwenden, können Sie sehen, wer die Änderung (die Stornierung) eingereicht hat und wer sie genehmigt hat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]