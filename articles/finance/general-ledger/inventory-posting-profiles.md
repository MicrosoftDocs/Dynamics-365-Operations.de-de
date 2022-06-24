---
title: Bestandbuchungsprofile
description: In diesem Artikel wird eine Übersicht der Bestandbuchungspropfile angezeigt.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901341"
---
# <a name="inventory-posting-profiles"></a>Bestandbuchungsprofile

[!include [banner](../includes/banner.md)]

Bestandbuchungsprofile steuern die Buchung von Bestandtransaktionen des untergeordnetem Sachkontos im Hauptbuch. Bestandbuchungen im untergeordneten Sachkonto können aus vielen Modulen generiert werden, einschließlich **Vertrieb und Marketing**, **Beschaffung**, **Produktionskontrolle** und mehr. Bestandbuchungen im untergeordneten Sachkonto können jedes Mal gebucht werden, wenn ein Artikel in einem Auftrag oder einer Bestellung verwendet wird. 

Zusätzliche Buchungen im untergeordneten Sachkonto können gebucht werden:
- Jedes Mal, wenn ein Dokument aktualisiert wird.
- Wenn ein Lieferschein oder eine Rechnung zum Auftrag gebucht wird.
- Wenn ein Bestellproduktbeleg oder eine Rechnung generiert wird.

Weitere Informationen finden Sie unter Bestandbuchungen im untergeordneten Sachkonto.

## <a name="inventory-transaction-overview"></a>Überischt über Bestandbuchungen

Jede Bestandbuchungen im untergeordneten Sachkonto enthält:
 - Menge 
 - Preis 
 - Website 
 - Lager 
 - Speicherort 

Bestandsbuchungen im untergeordneten Sachkonto erstellen zwei Einträge im Hauptbuch durch die physische Buchung und die finanzielle Buchung. Weitere Informationen finden Sie unter [Physische und finanzielle Aktualisierungen](/supply-chain/cost-management/physical-financial-updates.md).
Das folgende Beispiel ist eine Bestellung mit drei Positionen. Nehmen Sie für dieses Beispiel an, dass die gesamte Bestellung für einen einzelnen Standort und einen einzelnen Lagerort bestimmt ist. Jede Bestellposition hat einen einzelnen zugehörigen InventTrans-Datensatz – auch als Bestandsbuchung bekannt – und jede Position ist für eine Menge von 10. Das folgende Diagramm zeigt die Beziehung einer Bestellkopfzeile zu drei Bestellpositionen mit jeweils einem InventTrans-Datensatz.

![Beziehungsdiagramm für eine Bestellung mit drei Positionen mit jeweils einem InventTrans-Datensatz.](./media/InventTransRelationship.PNG)

Eine Menge von 5 wird auf der ersten Bestellposition empfangen. Die volle Menge für die zweite Position und keine erhaltene Menge in der dritten Position der Bestellung. Es gibt jetzt eine zweite Bestandsbuchung, die sich auf die erste Bestellposition bezieht. Die Buchung für die zweite Bestellposition wird auf **Erhalten** aktualisiert, und die dritte Transaktion bleibt unverändert. Das folgende Diagramm zeigt die Beziehung zum zusätzlichen InventTrans-Datensatz für Bestellposition 1.

![Beziehungsdiagramm für eine Bestellung mit drei Positionen. Eine Position wird teilweise empfangen und zeigt zwei InventTrans-Datensätze.](./media/InventTransRelationshipPartialReceipt.PNG)

In diesem Beispiel wird ein Beleg in das Hauptbuch gebucht; Dies ist der physische Beleg. Die Artikelmodellgruppe ist so konfiguriert, dass physischer Bestand gebucht wird, und alle Artikel verwenden dieselbe Artikelmodellgruppe. Das Bestandsbuchungsprofil verwendet einen einzelnen Satz von Hauptkonten. Es wird ein einzelner Beleg erstellt, und der InventTrans-Datensatz verknüpft sowohl InventTrans 1 als auch InventTrans 2 mit demselben Beleg.

Als Nächstes wird eine Rechnung für die Menge empfangen, die in den Positionen 1 und 2 eingegangen ist. Im Hauptbuch wird ein weiterer Beleg angelegt; das ist der Finanzbeleg. Die Artikelmodellgruppe wird zum Buchen des Finanzbestands konfiguriert. Der neue zweite Beleg bezieht sich auf InventTrans 1 und InventTrans 2.

Je nach Nachkalkulationsmodell existiert möglicherweise eine dritte Hauptbuchbuchung für Ihre Bestandbuchungen im untergeordnetem Sachkonto im Zusammenhang mit dem Abschluss und der Abrechnung des Bestands. Weitere Informationen finden Sie unter [Bestandsabschluss](/supply-chain/cost-management/inventory-close.md). Sie können die Details aller Bestandsbuchungen anzeigen, indem Sie zu **Bestandsverwaltung** > **Anfragen und Berichte** > **Buchungen** wechseln.

>[!Important]
> Die Bestandstransaktionen werden für jede eindeutige Kombination von Bestandsdimensionen und für jede Teilaktualisierung aufgeteilt. Dies wurde im vorherigen Beispiel für Teilaktualisierungen gezeigt.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Geteilter Bestand basierend auf dem Beispiel zur Bestandsdimension

Die Bestellposition 3 im Beispiel ist ein Artikel mit Seriennummer. Während des Eingangsprozesses werden zehn Seriennummern für die Bestellung registriert. Die Bestandbuchung wird in 10 Bestandbuchungen aufgeteilt. Das folgende Diagramm zeigt die Beziehung und zusätzliche Bestandsbuchungen, jede mit ihrer eigenen Seriennummer in Bezug auf Bestellposition 3.

![Beziehungsdiagramm für eine Bestellung mit drei Positionen. Eine Position wird mit Seriennummern versehen und zeigt zwei zusätzliche InventTrans-Datensätze](./media/InventTransRelationshipSerialNumber.PNG)

Wenn im obigen Beispiel jede Seriennummer auf einem einzelnen Produktbeleg eingeht, wird ein zusätzlicher Beleg erstellt. Das Feld für den physischen Beleg wird mit jeder Seriennummer verknüpft. Dasselbe gilt für die Finanzaktualisierung, wenn Sie die Bestellung fakturieren.

## <a name="inventory-transactions"></a>Bestandstransaktionen

Sie können Bestandsbuchungen auf der **Bestandsbuchungen**-Seite unter **Bestands- und Lagerverwaltung** oder **Kostenverwaltung** anzeigen. Sie können auch Bestandsbuchungen anzeigen, die sich auf eine bestimmte Ursprungsbelegposition beziehen (z. B. eine Bestellposition oder eine Aufsauftragsposition), indem Sie **Bestand** und dann **Buchungen** auswählen. 

Die **Bestandbuchungen**-Seite enthält die folgenden Felder.

| Feld            | Description                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Artikelnummer      | Die Artikelnummer, die der Buchung zugehörig ist.                                                                  |
| Physisches Datum    | Das Datum, an dem der Bestand im Lagerort ankommt, den Lagerort verlässt, in der Produktion verbraucht oder produziert wird. Geben Sie beispielsweise das Buchungsdatum auf
der Lieferscheinbuchung für einen Auftrag oder die Eingangsbuchung für eine Bestellung ein.                             |
| Finanzdatum   | Das Datum, an dem die Bestandsbuchung abgeschlossen und die Kosten im Hauptbuch erfasst werden. Beispielsweise das Buchungsdatum auf der Rechnungs- 
erstellung für eine Bestellung. Aktualisierungen des Referenzdokuments sind nicht zulässig, nachdem das Finanzdatum ausgefüllt wurde. |
| Referenz        | Gibt die Quelle der Buchung und die Art des Dokuments an, das im **Nummer**-Feld angezeigt wird. Zum Beispiel Kundenauftrag, Bestellung oder Zugang von Umlagerungsaufträgen.                                                 |
| Anzahl           | Gibt die Referenz-ID für eine Buchung an. Wenn zum Beispiel das **Referenz**-Feld den Auftrag anzeigt, gibt das **Nummer**-Feld die Auftragsnummer an.                                                       |
| Zugang (Status) | Bei Bestandsbuchungen, bei denen es sich um Quittungen handelt, zeigt dieses Feld den Status der Quittung an. Beispielsweise ist eine Bestellung eine Quittung und der Status möglicherweise **Bestellt** oder **Gekauft**.                                                            |
| Abgang (Status)   | Bei Bestandsbuchungen, bei denen es sich um Abhänge handelt, zeigt dieses Feld den Status des Abgangs an. Beispielsweise ist ein Verkaufsauftrag ein Abgang und der Status möglicherweise **Auf Bestellung** oder **Verkauft**.                         |
| Menge         | Die Menge der Bestandsbuchung. Positive Zahlen werden für Zugänge zum Bestand verwendet, während negative Zahlen für Abgänge aus dem Bestand verwendet werden.                                                                                                                          |
| Einheit             | Die Maßeinheit, in dem die Menge ausgedrückt wird.                                                                                   |
| Artikelgewichtsmenge      | Die Artikelgewichtsmenge für die Buchung. Weitere Informationen finden Sie unter [Info zu Artikeln mit Artikelgewicht](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Artikelgewichtseinheit          | Im Feld Maßeinheit für Artikelgewicht, indem die Menge für Artikelgewicht ausgedrückt wird.                                                         |
| Betrag der Kosten      | Die endgültigen Kosten der Bestandsbuchung. Dieses Feld wird ausgefüllt, wenn eine Buchung finanziell aktualisiert wird. Abhängig von der Nachkalkulationsmethode wird dieses Feld möglicherweise durch den Bestandsabschluss- und Regulierungsprozess aktualisiert.                            |

## <a name="inventory-status"></a>Bestandsstatus

Jede Bestandsbuchung hat einen Status, der entweder im Feld **Zugang** oder **Abgang** angezeigt wird. Das Feld, das verwendet wird, hängt vom Typ der Bestandbuchungen ab. Zugänge sind Buchungen, die den Bestand erhöhen. Beispielsweise eine Bestellung mit einer positiven Menge oder eine Auftragsretoure mit einer negativen Menge. Abgänge sind Bestandbuchungen, die den Bestand verringert haben. Beispielsweise ein Auftrag mit einer positiven Menge oder eine Bestellungsretoure mit einer negativen Menge.

### <a name="receipt-status"></a>Zugangsstatus

In der folgenden Tabelle wird der Status **Zugang** beschrieben.

| **Zugangsstatus** | **Beschreibung**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Bestellt            | Der Anfangsstatus jeder Bestandbuchung, die einen Eingang darstellt. Dazu gehören Bestellungen mit positiver Menge, Produktionsaufträge oder Auftragsretouren mit negativer Menge.                                                   |
| Erfasst         | Dieser Status wird verwendet, wenn ein zweistufiger Eingangsprozess vorhanden ist oder wenn die Artikelankunft verwendet wird, um anzuzeigen, dass das Produkt angekommen ist. Es wird verwendet, wenn Chargen- oder Seriennummern der Bestellung „zugewiesen“ oder registriert werden. Weitere Informationen zum Eingang finden Sie unter [Ankunftsübersicht](/supply-chain/inventory/arrival-overview.md). |
| Erhalten           | Dieser Status wird verwendet, wenn die Buchung physisch aktualisiert wird. Für eine Bestellung geschieht das, wenn der Produkteingang gebucht wird. Für eine Auftragsretoure geschieht das, wenn der Lieferschein gebucht wird.                                                                            |
| Eingekauft          | Dieser Status wird verwendet, wenn die Buchung finanziell aktualisiert wird. Für eine Bestellung oder Auftragsretoure geschieht das, wenn die Rechnung erstellt wird.                                                                                             |

### <a name="issue-status"></a>Abgangsstatus

In der folgenden Tabelle wird der Status **Abgang** beschrieben.

| **Abgangsstatus**  | **Beschreibung**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| In Auftrag          | Der Anfangsstatus jeder Bestandbuchung, die einen Abgang darstellt. Dazu gehören Aufträge mit positiver Menge, Stücklisten von Produktionsaufträgen oder Formelpositionen oder Bestellungsretouren mit negativer Menge.                                             |
| Bestellt reserviert  | Dieser Bestandsstatus zeigt an, dass Bestand für eine Bestellung reserviert ist, die erstellt, aber noch nicht physisch im Bestand eingegangen ist. Wenn das Inventar empfangen wird, wird der Status automatisch auf **Reserviert physisch** aktualisiert. Weitere Informationen zu Reservierungen finden Sie unter [Bestandsmengen reservieren](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Physisch reserviert | Dieser Status zeigt an, dass der Bestand für eine bestimmte Bestellung zugeteilt oder reserviert wurde. Wenn Bestand reserviert wird, ist er für andere Bestellungen nicht physisch verfügbar.                                 |
| Entnommen         | Dies zeigt an, dass der Bestand aus dem Lagerort kommissioniert wurde. Der Bestand befindet sich physisch noch im Lager, wurde nicht entfernt, steht aber nicht für andere Bestellungen zur Verfügung.  |
| Abgesetzt          | Dieser Status wird verwendet, wenn die Buchung physisch aktualisiert wird. Bei einem Auftrag ist dies der Zeitpunkt, an dem der Lieferschein gebucht wird; bei einer Bestellungsretoure ist dies, wenn der Wareneingang gebucht wird.                                                                      |
| Verkauft              | Dies ist der Status, der verwendet wird, wenn die Buchung finanziell aktualisiert wird. Für eine Bestellung oder einen Auftrag geschieht das, wenn die Rechnung erstellt wird.|

Weitere Informationen zu den Bestandbuchungen finden Sie unter [Details zu Bestandbuchungen](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Konfigurieren eines Bestandbuchungsprofils

Führen Sie folgende Schritte aus, um ein Bestandsbuchungsprofil zu konfigurieren:

1.  Öffnen Sie **Bestandsverwaltung** > **Einstellungen** > **Buchung** > **Buchung**.
2.  Wählen Sie die Registerkarte für den Typ der Buchung. Wählen Sie zum Beispiel **Bestellung**.
3.  Wählen Sie das Optionsfeld für den Buchungstyp aus. Wählen Sie zum Beispiel **Einkaufsaufwendungen für Ausgaben**.
4.  Wählen Sie **Neu** aus.
5.  Wählen Sie im Feld **Artikelcode** eine Option für **Tabelle**, **Gruppe**, **Alle** oder **Kategorie** aus. Um beispielsweise ein Buchungsprofil für eine bestimmte Artikelgruppe zu konfigurieren, wählen Sie **Gruppe** aus.
     - Wenn Sie **Tabelle** in Schritt 5 ausgewählt haben, wählen Sie die entsprechende Artikelnummer für das Buchungsprofil im Feld **Artikelrelation** aus.
     - Wenn Sie **Gruppe** in Schritt 5 ausgewählt haben, wählen Sie die entsprechende **Artikelgruppe** für das Buchungsprofil im Feld **Artikelrelation** aus.
     - Wenn Sie **Alle** in Schritt 5 ausgewählt haben, ist das Feld **Artikelrelation** leer.
     - Wenn Sie **Kategorie** in Schritt 5 ausgewählt haben, ist das Feld **Artikelrelation** leer. Wählen Sie im Feld **Kategorierelation** die Kategorie aus, für die das Buchungsprofil gilt.

6.  Wählen Sie im Feld **Kontocode** eine Option für **Tabelle**, **Gruppe** oder **Alle** aus. Um beispielsweise das Buchungsprofil auf alle Lieferanten anzuwenden, wählen Sie **Alle** aus.
     - Wenn Sie **Tabelle** in Schritt 5 ausgewählt haben, wählen Sie die entsprechende Lieferantennummer für das Buchungsprofil im Feld **Kontorelation** aus.
     - Wenn Sie **Gruppe** in Schritt 5 ausgewählt haben, wählen Sie die entsprechende Lieferantengruppe für das Buchungsprofil im Feld **Kontorelation** aus.
     - Wenn Sie **Alle** in Schritt 5 ausgewählt haben, ist das Feld **Kontorelation** leer.

7.  Wählen Sie eine **Mehrwertsteuergruppe** aus, um dem ausgewählten Buchungstyp eine bestimmte Steuergruppe zuzuordnen. Wenn dieses Feld leer ist, gilt der Buchungstyp für alle vorhandenen Steuergruppen. Die für Steuergruppen angegebene Buchung gilt nur für Verkaufs- und Bestellungsbuchungen.
8.  Geben die zu Kontonummer an, um den Kontotyp im Feld **Hauptkonto** zu buchen. Wenn noch keine Kontonummer für die Kontenart erstellt wurde, können Sie ein neues Konto erstellen. Sie erstellen ein neues Konto in der **Hauptkontodetails**-Seite im Hauptbuch.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Jede Registerkarte auf der **Bestandsbuchungsprofil**-Seite bezieht sich auf ein untergeordnetes Sachkonto in Dynamics 365 Supply Chain Management. Weitere Informationen finden Sie unter:
-   [Auftragsbuchung](sales-order-posting.md)
-   [Bestellungsbuchung](purchase-order-posting.md)
-   [Lagerbuchung](inventory-posting.md)
-   [Produktionssteuerungsbuchung](production-posting.md)
-   [Standardkostenabweichungsbuchung](standard-cost-variance-posting.md)
