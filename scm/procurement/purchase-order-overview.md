---
title: "Überblick über Bestellungen"
description: "Dieser Artikel enthält allgemeine Informationen zu Bestellungen (POs) und Links zu Artikeln zu den verschiedenen Phasen die eine Bestellung durchläuft."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: aed1a411aaefeebb96c2b922afc2e3e7f82cdbb7
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-order-overview"></a>Überblick über Bestellungen

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält allgemeine Informationen zu Bestellungen (POs) und Links zu Artikeln zu den verschiedenen Phasen die eine Bestellung durchläuft.

Eine Bestellung (PO) ist ein Dokument, das eine Vereinbarung mit einem Lieferanten zum Kauf von Waren oder Dienstleistungen darstellt. Das Dokument unterstützt außerdem die Nachverfolgung von Produktzugängen, die für die Bestellung auftreten und die Buchung der Kreditorenrechnungen für die Bestellung.  

Die **Bestellungen**-Seite enthält eine Übersicht über die verfügbaren Aufträge und ermöglicht das Ändern dieser Aufträge. Wenn Sie eine Bestellung öffnen, können die **Kopfzeile**-Ansicht auswählen. Diese enthält Informationen, die für jede Bestellung nur einmal angegebenen werden (z. B. Kreditordetails). Alternativ können Sie die **Positionen** anzeigen. Dort können Sie Auftragspositionen bearbeiten. Normalerweise wechseln Sie zwischen diesen zwei Ansichten, um wie Sie PO ändern. Zuschläge sind nicht direkt auf der Seite **Bestellungen** aufgeführt, ohne dass jedoch werden auf Menüs im Auftragskopf und den Positionen zugegriffen.  

Es gibt viele Berichte, in denen Informationen zu POs, Produktzugänge und Vendorenrechnungen angezeigt werden. Diese Berichte befinden sich den Modulen **Beschaffung** und **Kreditorenkonten**.  

Die Arbeitsbereiche **Bestellungsvorbereitung** und **Bestellungszugang und Weiterverfolgung** zeigen Listen von POs in verschiedenen Zuständen an. Sie stellen zudem eine Zusammenfassung der Aktionen bereit, die ausgeführt werden müssen. der **Bestellungsvorbereitung**-Arbeitsbereich konzentriert sich auf die PO-Erstellung und -Überprüfung, die Verarbeitung der Bestellung während der Genehmigung und die Bestätigung durch den Kreditor. Der **Bestellungseingang und -Nachverfolgung** Arbeitsbereich von ist auf dem Verarbeiten des Zugangs von Waren oder Services gegen PO konzentriert. Er umfasst Listen ein, der Einblick in Belege geben, die basierend sind oder bald für die Lieferung vom Lieferanten fällig sind. Diese Arbeitsbereiche werden nicht verwendet, um zugehörige Zugangsaktivitäten für den Lagerort ausführen. Diese Aktivitäten erfolgen über Seiten in den Modulen **Bestandsverwaltung** und **Lagerortverwaltung**. Die Verarbeitung von Kreditorrechnungen sollte über den **Kreditorenrechnungseingabe**-Arbeitsbereich erfolgen. Zahlung sollten über den **Kreditorenzahlungen**-Arbeitsbereich durchgeführt werden.  

Der folgenden Artikel bieten einen Überblick über die verschiedenen Phasen, die eine Bestellung durchläuft:

-   [Bestellungserstellung](purchase-order-creation.md)
-   [Genehmigen und Bestätigen von Bestellungen](purchase-order-approval-confirmation.md)
-   [Produkteingang für Bestellungen](product-receipt-against-purchase-orders.md)
-   [Überblick der Kreditorenrechnungen](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)

## <a name="types-of-purchase-orders"></a>Typ der Bestellungen
Es gibt drei Typen von Bestellungen: Wenn Sie eine Bestellung erstellen, muss der Typ für angegeben. Sie können auf der **Beschaffungsparameter**-Seite einen Standardauftragstyp für neue Aufträge einrichten.

| Bestellungstyp        | Beschreibung                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erfassung        | Mit diesem Typ erstellen Sie einen Auftragsentwurf. Dieser Typ hat keinen Einfluss auf die Lagermengen und erzeugt keine Bestandsbuchungen. Die PO-Erfassungspositionen werden nicht in die Produktprogrammplanung einbezogen.                                                                                                       |
| Bestellung | Verwenden Sie diesen Typ, um POs zu erstellen, wenn Aufträge von einem Kreditor bestätigt sind und wenn beim Zugang verarbeitet und vor der Zahlung an den Kreditor fakturiert werden. Dieser PO-Typ ist der am häufigsten genutzt Typ.                                                                          |
| Zurückgegebener Auftrag | Er wird verwendet, wenn Sie Waren an den Kreditor zurückgeben. Diese Auftragstyp erfordert, dass Sie eine Rücksendungsnummer (RMA, Return Material Authorization) angeben, die vom Kreditor bereitgestellt wird. Sie geben die Rücksendungsnummer auf der **Allgemeines**-Registerkarte der Bestellung an. Die Auftragspositionen müssen negative Mengen haben. |

## <a name="purchase-order-statuses"></a>Bestellungsstatus
POs umfassen unterschiedliche Statusfelder, die den Status des Auftrags angeben. Diese Felder sind in der **Kopfzeilen**-Ansicht des Auftrags sichtbar. Einige sind auch in der Rasterübersicht aller Aufträge sichtbar. Das **Status**-Feld zeigt den Status für die Mengen in der Bestellung an. Folgende Werte sind verfügbar:

-   **Offener Auftrag** – Aufträge wurden erstellt und die Mengen sind bestellt.
-   **Empfangen** – Einige Mengen sind eingegangen, aber noch fakturiert.
-   **Fakturiert** - Die gesamte Menge der Bestellung wurde fakturiert. **Hinweis:** Wurde eine Bestellung *teilweise* fakturiert, gilt weder der Status **Empfangen** noch **Fakturiert**. Daher hat der Auftrag weiterhin den Status **Offener Auftrag**.
-   **Storniert** – Ein Auftrag wurde bestätigt und später storniert. Dieser Status gibt daher an, dass es keine offenen Mengen für den Auftrag gibt.

Das **Dokumentstatus**-Feld ermöglicht die schnelle Prüfung des Auftragsfortschritts über die verarbeiteten Dokumente. Es zeigt den Status des aktuell für den Auftrag abgeschlossenen Dokuments an. Folgende Werte sind verfügbar:

-   **Keine** – Kein Dokument wurde für die Bestellung verarbeitet.
-   **Einkaufsabfrage** - Eine Einkaufsabfrage wurde generiert und der Auftrag wartet auf Feedback vom Kreditor.
-   **Bestellung** – Die Bestätigung wurde für die Bestellung verarbeitet.
-   **Produktzugang** – Der Produktzugang für die Bestellung wurde verarbeitet.
-   **Rechnung** – Eine Rechnung wurde für den Auftrag gebucht.

Das **Genehmigungsstatus**-Feld wird verwendet, wenn eine Bestellung einen Überprüfungsprozess oder Workflow durchläuft. Folgende Werte sind verfügbar:

-   **Entwurf**, **Wird überprüft** und **Abgelehnt** – Diese Statuswerte werden nur bei Verwendung eines Genehmigungsworkflows für die Bestellung verwendet.
-   **Genehmigt** – Dieser Status wird Aufträgen zugewiesen, die den Genehmigungsworkflow abgeschlossen haben. Aufträge, die ohne Genehmigungsworkflow erstellt wurden, erhalten direkt den Status **Genehmigt**.
-   **In Überprüfung** – Dieser Status wird in Szenarios verwendet, bei denen eine Einkaufsabfrage an den Kreditor gesendet wird, über die der Kreditor die Bedingungen der Bestellung bestätigen kann. Dieser Status wird auch im Prozess verwendet, der über die Aktion **Bestätigungsanforderung** eingeleitet wird. Für diesen Prozess wird der Kreditor aufgefordert die Bedingungen der PO zu bestätigen, indem er sich mit Ihrem System verbindet und registriert, ob er den Auftrag bestätigt oder ablehnt.
-   **Bestätigt** – Dieser Status wird zugewiesen, nachdem die Bestellung bestätigt wurde. Normalerweise ist dieser Status der letzte Genehmigungsstatus, der die einer Bestellung zugeordnet ist.


<a name="see-also"></a>Siehe auch
--------

[Bestellungserstellung](purchase-order-creation.md)

[Genehmigen und Bestätigen von Bestellungen](purchase-order-approval-confirmation.md)

[Produkteingang für Bestellungen](product-receipt-against-purchase-orders.md)

[Überblick der Kreditorenrechnungen](/dynamics365/operations/financials/accounts-payable/vendor-invoices-overview)




