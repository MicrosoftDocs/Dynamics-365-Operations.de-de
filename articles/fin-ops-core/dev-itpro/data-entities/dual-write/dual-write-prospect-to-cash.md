---
title: Prospect-to-cash in Dual-Write
description: Dieses Thema bietet Informationen über die Prospect-to-Cash iDual-Write.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 7c53bcd1084d89b59d0f6b2674a85d7c3481a9bf
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781790"
---
# <a name="prospect-to-cash-in-dual-write"></a>Prospect-to-cash in Dual-write

[!include [banner](../../includes/banner.md)]

Ein wichtiges Ziel der meisten Unternehmen ist es, Interessenten in Kunden umzuwandeln und dann eine kontinuierliche Geschäftsbeziehung mit diesen Kunden aufrechtzuerhalten. In Microsoft Dynamics 365 Apps erfolgt der Prospect-to-Cash-Prozess durch Angebots- oder Auftragsbearbeitungs-Workflows, und die Finanzzahlen werden abgestimmt und anerkannt. Durch die Integration von Prospect-to-Cash mit Dual-Write wird ein Workflow erstellt, der ein Angebot und einen Auftrag, die entweder aus Dynamics 365 Sales oder Dynamics 365 Supply Chain Management stammen, aufnimmt und das Angebot und den Auftrag in beiden Anwendungen verfügbar macht.

In den App-Schnittstellen können Sie in Echtzeit auf die Verarbeitungsstatus und Rechnungsinformationen zugreifen. So können Sie Funktionen wie Produktlagerung, Bestandsabwicklung und Erfüllung im Supply Chain Management einfacher verwalten, ohne Angebote und Aufträge neu erstellen zu müssen.

![Dual-Write-Flow in Prospect-to-Cash.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Informationen zur Kunden- und Kontaktintegration finden Sie unter [Integrierte Masterdaten von Debitoren](customer-mapping.md). Informationen zur Produktintegration finden Sie unter [Einheitliche Produktumgebung](product-mapping.md).

> [!NOTE]
> In Dynamics 365 Sales beziehen sich sowohl Interessent als auch Kunde auf einen Datensatz in der Tabelle **Konto**, in der die Spalte **RelationshipType** entweder **Interessent** oder **Kunde** ist. Wenn Ihre Geschäftslogik einen **Konto**-Qualifizierungsprozess enthält, bei dem der Datensatz **Konto** erstellt und zuerst als Interessent und dann als Kunde qualifiziert wird, wird dieser Datensatz nur mit der Finance and Operations-App synchronisiert, wenn es ein Kunde ist (`RelationshipType=Customer`). Wenn Sie möchten, dass die Zeile **Konto** als Interessent synchronisiert wird, benötigen Sie eine benutzerdefinierte Zuordnung, um die Interessentendaten zu integrieren.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

Bevor Sie Angebote synchronisieren können, müssen Sie die folgenden Einstellungen aktualisieren.

### <a name="setup-in-sales"></a>Einrichtung in Sales

Gehen Sie in Sales zu **Einstellungen \> Verwaltung \> Systemeinstellungen \> Vertrieb** und stellen Sie sicher, dass die folgenden Einstellungen verwendet werden:

- Die Option **Systempreisberechnungssystem verwenden** wird auf **Ja** festgelegt.
- Die Spalte **Rabattberechnungsmethode** wird auf **Positionsartikel** festgelegt.

### <a name="sites-and-warehouses"></a>Standorte und Lagerhäuser

Im Supply Chain Management sind die Spalten **Standort** und **Lager** für Angebots- und Auftragspositionen erforderlich. Wenn Sie den Standort und das Lager in den Standardauftragseinstellungen festlegen, werden diese Spalten automatisch gesetzt, wenn Sie ein Produkt zu einer Angebots- oder Auftragsposition hinzufügen. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummernkreise für Angebote und Aufträge

Die Nummernkreise für Supply Chain Management und Sales sind nicht miteinander verbunden, wenn Angebote und Aufträge im Sales und Supply Chain Management erstellt und synchronisiert werden. Wenn ein Kundenauftrag, der in Sales angelegt wird, mit dem Supply Chain Management synchronisiert wird, hat er dieselbe Kundenauftragsnummer im Supply Chain Management. Um sicherzustellen, dass die Kundenauftragsnummer nicht doppelt vorhanden ist, müssen Sie in den beiden Anwendungen unterschiedliche Nummernfolgesysteme verwenden.

Zum Beispiel ist der Nummernkreis im Supply Chain Management **1, 2, 3, 4, 5, ...**, und der Nummernkreis in Sales ist **100, 99, 98, ...**. Wenn Sie 100 Kundenaufträge in Sales anlegen, wird letztendlich eine Auftragsnummer generiert, die bereits im Supply Chain Management existiert. Mit anderen Worten, die beiden Nummernkreise werden sich letztendlich überschneiden, wenn Kundenaufträge im Supply Chain Management und in Sales angelegt werden. Stattdessen können Sie im Supply Chain Management eine Zahlenfolge wie **F1, F2, F3, ...** und in Sales eine Zahlenfolge wie **C1, C2, C3, ...** verwenden. Diese Nummernkreise führen niemals zu doppelten Kundenauftragsnummern.

## <a name="sales-quotations"></a>Verkaufsangebote

Angebote können entweder im Vertrieb oder im Supply Chain Management erstellt werden. Wenn Sie ein Angebot in Sales erstellen, wird es in Echtzeit mit dem Supply Chain Management synchronisiert. Wenn Sie ein Angebot im Supply Chain Management erstellen, wird es in Echtzeit mit Sales synchronisiert. Beachten Sie die folgenden Punkte:

+ Sie können dem Produkt einen Rabatt auf das Angebot hinzufügen. In diesem Fall wird der Rabatt mit dem Supply Chain Management synchronisiert. Die Spalten **Rabatt**, **Belastungen** und **Steuer** in der Kopfzeile werden durch komplizierte Einstellungen in Supply Chain Management gesteuert. Diese Einrichtung unterstützt kein Integrations-Mapping. Stattdessen werden die Spalten **Preis**, **Rabatt**, **Gebühr** und **Steuer** in Supply Chain Management verwaltet.
+ Die Spalten **Rabatt %**, **Rabatt** und **Frachtbetrag** im Angebotskopf sind schreibgeschützte Spalten.
+ Die Spalten **Frachtkonditionen**, **Lieferbedingungen**, **Versandmethode** und **Liefermodus** sind nicht Teil der Standardzuordnungen. Um diese Spalten zuzuordnen, müssen Sie eine Wertzuordnung, die für die Daten in den Organisationen, zwischen denen die Tabelle synchronisiert wird, spezifisch ist.

Wenn Sie auch die Field Service-Lösung verwenden, müssen Sie den **Angebotsanforderungspositions-Erstellungs**-Parameter erneut aktivieren. Durch erneutes Aktivieren des Parameters können Sie mit der Schnellerstellungsfunktion weiterhin Angebotspositionen erstellen.

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
    - Wenn eine Kundenauftragszeile aus Sales in das Supply Chain Management synchronisiert wird, wird der volle Zeilenrabattbetrag verwendet. Da Supply Chain Management keine Spalte hat, die den vollständigen Rabattbetrag für eine Position speichern kann, wird der Betrag durch die Menge dividiert und in der Spalte **Positionsrabatt** gespeichert. Jede Rundung, die während dieser Division auftritt, wird in der Spalte **Verkaufsgebühren** in der Verkaufsposition gespeichert.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Beispiel: Synchronisierung von Sales und Supply Chain Management

Sie haben den folgenden Kundenauftrag:

+ **Sales:** = Menge = 3, Pro-Positionsrabatt = $10.00
+ **Supply Chain Management:** Menge = 3, Zeilenrabattbetrag = DM 3,33, Verkaufsgebühr = - DM 0,01

Wenn Sie die Synchronisation vom Supply Chain Management zu Sales durchführen, erhalten Sie folgendes Ergebnis:

+ **Supply Chain Management:** Menge = 3, Zeilenrabattbetrag = DM 3,33, Verkaufsgebühr = - DM 0,01
+ **Sales:** = Menge = 3, Pro-Positionsrabatt = (3 × $3.33) + $0.01 = $10.00

## <a name="dual-write-solution-for-sales"></a>Dual-Write-Lösung für Sales

Neue Spalten wurden der Tabelle **Bestellung** hinzugefügt und erscheinen auf der Seite. Die meisten dieser Spalten erscheinen auf der Registerkarte **Integration** in Sales. Weitere Informationen zur Zuordnung der Statusspalten finden Sie unter [Zuordnung für die Kundenauftragsstatusspalten einrichten](sales-status-map.md).

+ Die Schaltflächen **Rechnung erstellen** und **Bestellung stornieren** auf der Seite **Verkaufsauftrag** sind in Sales ausgeblendet.
+ Der Wert **Auftragsstatus** bleibt **Aktiv**, um sicherzustellen, dass Änderungen aus dem Supply Chain Management in den Kundenauftrag in Sales fließen können. Um dieses Verhalten zu steuern, setzen Sie den Standardwert **Statecode \[Status\]** auf **Aktiv**.

## <a name="invoices"></a>Rechnungen

Verkaufsrechnungen werden im Supply Chain Management erstellt und mit Sales synchronisiert. Beachten Sie die folgenden Punkte:

+ Eine Spalte **Rechnungsnummer** wurde zur Tabelle **Rechnung** hinzugefügt und wird auf der Seite angezeigt.
+ Die Schaltfläche **Rechnung erstellen** auf der Seite **Verkaufsauftrag** ist ausgeblendet, da die Rechnungen im Supply Chain Management erstellt und mit Sales synchronisiert werden. Die Seite **Rechnung** kann nicht bearbeitet werden, da die Rechnungen aus dem Supply Chain Management synchronisiert werden.
+ Der Wert **Verkaufsauftragsstatus** wird automatisch in **Rechnungen** geändert, wenn die zugehörige Rechnung aus dem Supply Chain Management mit Sales synchronisiert wurde. Darüber hinaus wird der Eigentümer des Auftrags, aufgrund dessen die Rechnung erstellt wurde, als Eigentümer der Rechnung zugewiesen. Daher kann der Besitzer des Auftrags die Rechnung anzeigen.
+ Die Spalten **Frachtkonditionen**, **Lieferbedingungen** und **Liefermodus** sind nicht in den Standardzuordnungen enthalten. Um diese Spalten zuzuordnen, müssen Sie eine Wertzuordnung, die für die Daten in den Organisationen, zwischen denen die Tabelle synchronisiert wird, spezifisch ist.

## <a name="templates"></a>Vorlagen

Prospect-to-Cash umfasst eine Sammlung von Kerntabellenzuordnungen, die während der Dateninteraktion zusammenwirken, wie in der folgenden Tabelle dargestellt.

| Finance and Operations Apps | Customer Engagement-Apps | Beschreibung |
|-----------------------------|-----------------------------------|-------------|
[Alle Produkte](mapping-reference.md#138) | msdyn_globalproducts | |
[Debitoren V3](mapping-reference.md#101) | Konten | |
[Debitoren V3](mapping-reference.md#116) | Kontakte | |
[Kontakte V2](mapping-reference.md#221) | msdyn_contactforparties | |
[Auftragskopfzeilen CDS](mapping-reference.md#217) | salesorders | |
[CDS-Auftragspositionen](mapping-reference.md#216) | salesorderdetails | |
[CDS-Verkaufsangebotskopf](mapping-reference.md#215) | Angebote | |
[CDS-Verkaufsangebotspositionen](mapping-reference.md#214) | quotedetails | |
[Freigegebene Produkte V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Verkaufsrechnungskopfzeilen V2](mapping-reference.md#118) | Rechnungen | Die Tabelle „Verkaufsrechnungskopfzeilen V2“ in der Finance and Operations-App enthält Rechnungen für Aufträge und Freitextrechnungen. Ein Filter wird in Dataverse für duales Schreiben angewendet, der alle Freitext-Rechnungsdokumente herausfiltert. |
[Verkaufsrechnungspositionen V2](mapping-reference.md#117) | Rechnungsdetails | |
[Auftragsgrundlagencodes](mapping-reference.md#186) | msdyn_salesorderorigins | |

Informationen zu Preislisten finden Sie unter [Einheitliche Produktumgebung](product-mapping.md).

## <a name="limitations"></a>Einschränkungen

- Rücklieferungen werden nicht unterstützt.
- Gutschriften werden nicht unterstützt.
- Für die Stammdaten müssen Finanzdimensionen festgelegt werden, z. B. Debitor und Kreditor. Wenn ein Kunde zu einem Angebot oder Auftrag hinzugefügt wird, fließen die mit dem Kundendatensatz verknüpften Finanzdimensionen automatisch in den Auftrag ein. Derzeit enthält duales Schreiben keine Daten zu Finanzdimensionen für Stammdaten.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
