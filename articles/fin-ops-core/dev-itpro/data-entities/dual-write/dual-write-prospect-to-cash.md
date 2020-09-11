---
title: Prospect-to-cash in Dual-Write
description: Dieses Thema bietet Informationen über die Prospect-to-Cash iDual-Write.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: a2ca0ce277a062c8d525b6a3619eaf1b0114667b
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719263"
---
# <a name="prospect-to-cash-in-dual-write"></a>Prospect-to-cash in Dual-write

[!include [banner](../../includes/banner.md)]



Ein wichtiges Ziel der meisten Unternehmen ist es, Interessenten in Kunden umzuwandeln und dann eine kontinuierliche Geschäftsbeziehung mit diesen Kunden aufrechtzuerhalten. In Microsoft Dynamics 365 Apps erfolgt der Prospect-to-Cash-Prozess durch Angebots- oder Auftragsbearbeitungs-Workflows, und die Finanzzahlen werden abgestimmt und anerkannt. Durch die Integration von Prospect-to-Cash mit Dual-Write wird ein Workflow erstellt, der ein Angebot und einen Auftrag, die entweder aus Dynamics 365 Sales oder Dynamics 365 Supply Chain Management stammen, aufnimmt und das Angebot und den Auftrag in beiden Anwendungen verfügbar macht.

In den App-Schnittstellen können Sie in Echtzeit auf die Verarbeitungsstatus und Rechnungsinformationen zugreifen. So können Sie Funktionen wie Produktlagerung, Bestandsabwicklung und Erfüllung im Supply Chain Management einfacher verwalten, ohne Angebote und Aufträge neu erstellen zu müssen.

![Dual-Write-Flow in Prospect-to-Cash](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

Bevor Sie Angebote synchronisieren können, müssen Sie die folgenden Einstellungen aktualisieren.

### <a name="setup-in-sales"></a>Einrichtung in Sales

Gehen Sie in Sales zu **Einstellungen \> Verwaltung \> Systemeinstellungen \> Vertrieb** und stellen Sie sicher, dass die folgenden Einstellungen verwendet werden:

- Die Einstellung **Systempreisberechnung verwenden** ist auf **Ja** gesetzt.
- Das Feld **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.

### <a name="sites-and-warehouses"></a>Standorte und Lagerhäuser

Im Supply Chain Management sind die Felder **Site** und **Lager** für Angebots- und Auftragszeilen erforderlich. Wenn Sie den Standort und das Lager in den Standardauftragseinstellungen festlegen, werden diese Felder automatisch gesetzt, wenn Sie ein Produkt zu einer Angebots- oder Auftragszeile hinzufügen. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummernkreise für Angebote und Aufträge

Die Nummernkreise für Supply Chain Management und Sales sind nicht miteinander verbunden, wenn Angebote und Aufträge im Sales und Supply Chain Management erstellt und synchronisiert werden. Wenn ein Kundenauftrag, der in Sales angelegt wird, mit dem Supply Chain Management synchronisiert wird, hat er dieselbe Kundenauftragsnummer im Supply Chain Management. Um sicherzustellen, dass die Kundenauftragsnummer nicht doppelt vorhanden ist, müssen Sie in den beiden Anwendungen unterschiedliche Nummernfolgesysteme verwenden.

Zum Beispiel ist der Nummernkreis im Supply Chain Management **1, 2, 3, 4, 5, ...**, und der Nummernkreis in Sales ist **100, 99, 98, ...**. Wenn Sie 100 Kundenaufträge in Sales anlegen, wird letztendlich eine Auftragsnummer generiert, die bereits im Supply Chain Management existiert. Mit anderen Worten, die beiden Nummernkreise werden sich letztendlich überschneiden, wenn Kundenaufträge im Supply Chain Management und in Sales angelegt werden. Stattdessen können Sie im Supply Chain Management eine Zahlenfolge wie **F1, F2, F3, ...** und in Sales eine Zahlenfolge wie **C1, C2, C3, ...** verwenden. Diese Nummernkreise führen niemals zu doppelten Kundenauftragsnummern.

## <a name="sales-quotations"></a>Verkaufsangebote

Angebote können entweder im Vertrieb oder im Supply Chain Management erstellt werden. Wenn Sie ein Angebot in Sales erstellen, wird es in Echtzeit mit dem Supply Chain Management synchronisiert. Wenn Sie ein Angebot im Supply Chain Management erstellen, wird es in Echtzeit mit Sales synchronisiert. Beachten Sie die folgenden Punkte:

+ Sie können dem Produkt einen Rabatt auf das Angebot hinzufügen. In diesem Fall wird der Rabatt mit dem Supply Chain Management synchronisiert. Die Felder **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Supply Chain Management gesteuert. Diese Einrichtung unterstützt kein Integrations-Mapping. Stattdessen werden die Felder **Preis**, **Rabatt**, **Gebühr** und **Steuer** im Supply Chain Management gepflegt und behandelt.
+ Die Felder **Rabatt %**, **Rabatt** und **Frachtbetrag** im Angebotskopf sind schreibgeschützte Felder.
+ Die Felder **Frachtbedingungen**, **Lieferbedingungen**, **Versandmethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Felder abzubilden, müssen Sie ein Werte-Mapping einrichten, das für die Daten in den Organisationen, zwischen denen die Entität synchronisiert wird, spezifisch ist.

Wenn Sie auch die Field Service-Lösung verwenden, müssen Sie den **Angebotsanforderungspositions-Erstellungs**-Parameter erneut aktivieren. Durch erneutes Aktivieren des Parameters können Sie mit der Schnellerstellungsfunktion weiterhin Angebote erstellen.
1. Navigieren Sie zu Ihrer Dynamics 365 Sales-Anwendung.
2. Wählen Sie das Einstellungssymbol in der oberen Navigationsleiste.
3. Wählen Sie **Erweiterte Einstellungen**.
4. Wählen Sie die Option **System anpassen** aus.
5. Wählen Sie den Menüpunkt **Angebotsposition**.
6. Wechseln Sie zum Abschnitt **Datendienste** und wählen Sie das Kontrollkästchen **Schnellerstellung zulassen**.

## <a name="sales-orders"></a>Aufträge

Kundenaufträge können entweder im Vertrieb oder im Supply Chain Management angelegt werden. Wenn Sie einen Kundenauftrag in Sales anlegen, wird er in Echtzeit mit dem Supply Chain Management synchronisiert. Wenn Sie einen Kundenauftrag im Supply Chain Management anlegen, wird er ebenfalls in Echtzeit mit Sales synchronisiert. Beachten Sie die folgenden Punkte:

+ Manuell zu erfassende Produkte in Dynamics 365 Sales werden als Produktkategorien in Dynamics 365 Supply Chain Management angezeigt.
+ Rabattberechnung und Rundung:

    - Das Rabattberechnungsmodell in Sales unterscheidet sich insofern vom Modell im Bereich Supply Chain Management. In Supply Chain Management kann der endgültige Rabattbetrag in einer Sales-Position die Ergebnisse einer Kombination von Rabattbeträgen und von Rabattprozentsätzen sein. Bei der abschließenden Rabattbetrag durch die Menge für die Position geteilt wird, kann möglicherweise das Runden auftreten. Diese Rundung wird jedoch nicht berücksichtigt, wenn ein gerundeter Rabattbetrag pro Einheit mit dem Vertrieb synchronisiert wird. Um sicherzustellen, dass der volle Rabattbetrag einer Verkaufszeile im Supply Chain Management korrekt mit Sales synchronisiert wird, muss der volle Betrag synchronisiert werden, ohne durch die Zeilenmenge geteilt zu werden. Daher müssen Sie die Rabattberechnungsmethode als **Zeilenposition** im Verkauf definieren.
    - Wenn eine Kundenauftragszeile aus Sales in das Supply Chain Management synchronisiert wird, wird der volle Zeilenrabattbetrag verwendet. Da Supply Chain Management kein Feld hat, das den Rabattbetrag für vollständigen eine Position speichern kann, wird der Betrag durch die Menge dividiert und gespeichert im Feld **Positionsrabatt**. Jede Rundung, die während dieser Sparte auftritt, wird im Feld **Verkaufsgebühren** in der Verkaufszeile gespeichert.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Beispiel: Synchronisierung von Sales und Supply Chain Management

Sie haben den folgenden Kundenauftrag:

+ **Sales:** = Menge = 3, Pro-Positionsrabatt = $10.00
+ **Supply Chain Management:** Menge = 3, Zeilenrabattbetrag = DM 3,33, Verkaufsgebühr = - DM 0,01

Wenn Sie die Synchronisation vom Supply Chain Management zu Sales durchführen, erhalten Sie folgendes Ergebnis:

+ **Supply Chain Management:** Menge = 3, Zeilenrabattbetrag = DM 3,33, Verkaufsgebühr = - DM 0,01
+ **Sales:** = Menge = 3, Pro-Positionsrabatt = (3 × $3.33) + $0.01 = $10.00

## <a name="dual-write-solution-for-sales"></a>Dual-Write-Lösung für Sales

Neue Felder wurden der Entität **Bestellung** hinzugefügt und erscheinen auf der Seite. Die meisten dieser Felder erscheinen auf der Registerkarte **Integration** in Sales. Es gibt einige wenige spezielle Felder:

+ Das Feld **Bearbeitungsstatus** zeigt den Bearbeitungsstatus des Auftrags im Supply Chain Management an. Dieses Feld ist gesperrt und zeigt nur den Status des Auftrags aus dem Supply Chain Management an. Folgende Werte sind verfügbar:

    + **Aktiv** – Der Status wird nach dem Auftrag in Sales mithilfe der Schaltfläche **Aktivieren** in Sales aktiviert.
    + **Bestätigt**
    + **Geliefert**
    + **Fakturiert**
    + **Teilgeliefert**
    + **Teilweise fakturiert**
    + **Entnommen**
    + **Storniert**

    Die folgende Tabelle zeigt, wie der Verarbeitungsstatus auf den Wert **CRM-Statuscode** abgebildet wird.

    | Verarbeitungsstatus           | CRM-Statuscode    |
    |-----------------------------|--------------------|
    | Aktiv                      | Neu/Ausstellen/Behalten |
    | Bestätigt/ausgewählt            | In Bearbeitung        |
    | Teilweise geliefert         | Partiell            |
    | Geliefert                   | Vollständig           |
    | Fakturiert/Teilweise fakturiert | Fakturiert           |
    | Storniert                    | Kein Geld           |

+ Die Schaltflächen **Rechnung erstellen** und **Bestellung stornieren** auf der Seite **Verkaufsauftrag** sind in Sales ausgeblendet.
+ Der Wert **Auftragsstatus** bleibt **Aktiv**, um sicherzustellen, dass Änderungen aus dem Supply Chain Management in den Kundenauftrag in Sales fließen können. Um dieses Verhalten zu steuern, setzen Sie den Standardwert **Statecode \[Status\]** auf **Aktiv**.

## <a name="invoices"></a>Rechnungen

Verkaufsrechnungen werden im Supply Chain Management erstellt und mit Sales synchronisiert. Beachten Sie die folgenden Punkte:

+ Ein Feld **Rechnungsnummer** wurde zur Entität **Rechnung** hinzugefügt und wird auf der Seite angezeigt.
+ Die Schaltfläche **Rechnung erstellen** auf der Seite **Verkaufsauftrag** ist ausgeblendet, da die Rechnungen im Supply Chain Management erstellt und mit Sales synchronisiert werden. Die Seite **Rechnung** kann nicht bearbeitet werden, da die Rechnungen aus dem Supply Chain Management synchronisiert werden.
+ Der Wert **Verkaufsauftragsstatus** wird automatisch in **Rechnungen** geändert, wenn die zugehörige Rechnung aus dem Supply Chain Management mit Sales synchronisiert wurde. Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen. Daher kann der Besitzer des Auftrags die Rechnung anzeigen.
+ Die Felder **Frachtbedingungen**, **Lieferbedingungen** und **Liefermodus** sind nicht in den Standardzuordnungen enthalten. Um diese Felder abzubilden, müssen Sie ein Werte-Mapping einrichten, das für die Daten in den Organisationen, zwischen denen die Entität synchronisiert wird, spezifisch ist.

## <a name="templates"></a>Vorlagen

Prospect-to-Cash umfasst eine Sammlung von Kernentitätszuordnungen, die während der Dateninteraktion zusammenwirken, wie in der folgenden Tabelle dargestellt.

| Finance and Operations Apps | Modellgesteuerte Anwendungen in Dynamics 365 | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
| Verkaufsrechnungskopfzeilen V2    | Rechnungen                          |             |
| Verkaufsrechnungspositionen V2      | Rechnungsdetails                    |             |
| Auftragskopfzeilen CDS     | salesorders                       |             |
| CDS-Auftragspositionen       | salesorderdetails                 |             |
| Auftragsgrundlagencodes    | msdyn\_salesorderorigins          |             |
| CDS-Verkaufsangebotskopf  | Angebote                            |             |
| CDS-Verkaufsangebotspositionen   | quotedetails                      |             |

Hier sind die zugehörigen Kernentitätszuordnungen für Prospect-to-Cash:

+ [Debitoren V3 zu Konten](customer-mapping.md#customers-v3-to-accounts)
+ [CDS-Kontakte V2 zu Kontakten](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Debitoren V3 zu Kontakten](customer-mapping.md#customers-v3-to-contacts)
+ [Freigegebene Produkte V2 zu msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Alle Produkte zu msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Preisliste](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
