---
title: Bestellungsbuchung
description: Dieses Thema beschreibt die Registerkarte Bestellung auf der Seite Bestandsbuchungsprofile.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 4b36ab9da22da7d4f3e62bd2d2aba2a2ec80e60f
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803001"
---
# <a name="purchase-order-posting"></a>Bestellungsbuchung

Die Registerkarte **Bestellung** auf der Seite **Bestandsbuchungsprofile** dient als Steuerelement für die Buchung von Bestellungen im Hauptbuch. Zwei Hauptaktivitäten buchen das Hauptbuch für eine Bestellung: 

- Produktzugang
- Rechnung

Damit eine physische Transaktion (Produktzugang) zu einer Bestellung ins Hauptbuch gebucht werden kann, müssen die folgenden Ankreuzfelder markiert sein:

- Das Kontrollkästchen **Produktzugang im Sachkonto buchen** auf der Seite **Parameter der Bestands- und Lagerverwaltung**.
- Die Kontrollkästchen **Physikalischen Bestand buchen** und **Haftung bei Produktzugang erfassen** auf der Seite **Artikelmodellgruppen**.

Die Hauptkonten müssen auf der Seite **Bestandsbuchungsprofil** für die folgenden Buchungsarten angegeben werden:

- Nachkalkulation von Einkäufen erhaltener Materialien
- Einkaufskosten, nicht fakturiert
- Einkauf, Abgrenzung

Damit eine finanzielle Transaktion (Rechnung) für eine Bestellung im Hauptbuch gebucht werden kann, müssen die folgenden Bedingungen erfüllt sein:

- Das Kontrollkästchen **Wertmäßigen Bestand buchen** muss auf der Seite **Postenmodellgruppen** für den in der Zeile der Bestellung ausgewählten Artikel markiert sein.
- Die Hauptkonten müssen auf der Seite **Bestandsbuchungsprofil** für die folgenden Buchungsarten angegeben werden:
  - Kosten der eingekauften, fakturierten Materialien
  - Einkaufswendungen für Produkt
  - Einkaufsaufwendungen für Ausgaben
  - Rabatt (optional)

## <a name="fixed-receipt-price-posting"></a>Buchung des festen Zugangspreises

Als Alternative zur Auswahl der Option **Standardkosten** im Feld **Bestandsmodell** auf der Seite **Bestandsmodellgruppen** für einen Artikel können Sie den festen Zugangspreis als Nachkalkulation für einen Artikel verwenden. Der Hauptunterschied besteht darin, dass bei Verwendung von **Fester Zugangspreis** der aktuelle Einstandspreis für den Artikel verwendet wird, wenn der Bestandseingang gebucht wird. Für **Festgelegter Eingangspreis** gibt es keinen Prozess der Nachkalkulation; wenn eine Finanzaktualisierung gebucht wird, wird der aktuelle Einstandspreis zum Zeitpunkt der Buchung verwendet. Wenn es eine Differenz zwischen dem Einstandspreis beim Eingang und der Rechnung gibt, wird die Abweichung auf die Gewinn- und Verlustkonten für den festen Eingangspreis gebucht.

Um einen festen Eingangspreis für ein Produkt zu verwenden, müssen Sie Folgendes konfigurieren:

- Markieren Sie auf der Seite **Artikelmodellgruppen** die Ankreuzfelder **Physikalischen Bestand POSTEN** und **Fester Eingangspreis**. 
- Auf der Seite **Parameter der Bestands- und Lagerverwaltung** markieren Sie das Kontrollkästchen **Lieferschein im Sachkonto posten**.
- Geben Sie auf der Seite **Buchungsprofil Bestand** die Hauptkonten für die folgenden Buchungsarten an:
  - Fester Zugangspreis - Gewinn
  - Fester Zugangspreis - Verlust
  - Gegenkonto für festen Zugangspreis

Weitere Informationen finden Sie unter [Festgelegter Eingangspreis](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Kaufbelastungen und Bestandsabweichungsbuchungen

Wenn Sie planen, Belastungen für Käufe und Bestandsschwankungen zu berücksichtigen, gehen Sie wie folgt vor:

- Aktivieren Sie auf der Seite **Kreditorenparameter** auf der Registerkarte **Rechnung** das Kontrollkästchen **Buchen auf Sachkonto**.
- Aktivieren Sie auf der Seite **Postenmodellgruppen** für den in der Bestellzeile ausgewählten Artikel die Kontrollkästchen **Physikalischen Bestand buchen**, **Wertmäßigen Bestand buchen** und **Haftung bei Produktzugang ansetzen**.
- Auf der Seite **Beschaffungs- und Bezugsquellenfindungsparameter** markieren Sie das Ankreuzfeld **Belastungen beim Produktzugang generieren**.
- Auf der Seite **Parameter der Bestands- und Lagerverwaltung** markieren Sie das Kontrollkästchen **Lieferschein im Sachkonto posten**.

Auf der Seite **Bestandsbuchungsprofil** müssen Sie die Hauptkonten für die folgenden Buchungsarten angeben:

- Einkaufskosten, nicht fakturiert
- Einkaufswendungen für Produkt
- Bestandsveränderung

> [!NOTE]
> Die Buchungsart **Abrechnung** wird nicht verwendet, wenn der Parameter **Buchen auf Sachkonto** ausgewählt ist.

Weitere Informationen finden Sie unter [Buchen Sie auf das Konto Buchhaltungsprinzip](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Beispiel für die Konfiguration eines Buchungsprofils

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten mit beispielhaften Hauptkonten und Beschreibungen:

- Die Spalte **Clearingkonto** gibt an, dass es sich bei der Buchungsart um ein Verrechnungskonto handelt. Der auf diesem Konto gebuchte Betrag wird automatisch storniert, wenn eine spätere Transaktion gebucht wird. 
- Bei der Spalte **P/F** steht **P** für physische Buchungen und **F** für Finanzbuchungen. 
- Die Spalte **Follow** zeigt an, ob das Hauptkonto für eine bestimmte Buchungsart typischerweise mit einer anderen Buchungsart identisch ist. Der Wert in der Spalte gibt die Buchungsart an, die in der Regel verwendet wird.

> [!NOTE]
> Die Hauptkonten und Hauptkontonamen sind nur Vorschläge. Wir empfehlen<!--note from editor: Via Writing Style Guide.--> dass Sie mit Ihrem Buchhalter zusammenarbeiten, um die beste Konfiguration für Ihre Geschäftsanforderungen zu ermitteln.


| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Kosten der eingekauften, eingegangenen Materialien | 140100</br>140101 | Materialbestand</br>Materialien versendet, nicht fakturiert | Anlage | Belastung | Ja | P | Kosten der eingekauften, fakturierten Materialien | Wird verwendet, wenn ein Produktzugang für eine Bestellung gebucht wird. Die Gegenbuchung auf dem Konto sind die Ausgaben für den Kauf, die nicht in Rechnung gestellt werden. Der Betrag auf diesem Konto wird storniert, wenn eine Einkaufsrechnung gebucht wird. |
| Einkaufskosten, nicht fakturiert | 600180 | Materialeingänge | Ausgaben | Belastung | Ja | P | |Wird verwendet, wenn ein Produktzugang für eine Bestellung gebucht wird. Für den Bon werden zwei Belege erstellt, um Kaufpreisabweichungen bei der Verwendung von Standardkalkulationen zu verfolgen. Die Gegenbuchung zu dem Konto auf dem ersten Beleg ist die Abgrenzung Einkauf. Die Gegenbuchung auf dem zweiten Beleg ist die Summe der Konten Einkaufskosten für erhaltene Materialien und Kaufpreisabweichung. Die auf diesem Konto gebuchten Beträge werden storniert, wenn eine Einkaufsrechnung gebucht wird. |
| Kosten der eingekauften, fakturierten Materialien | 140100 | Materialbestand | Anlage | Belastung | Nein | Fr  |Kosten der eingekauften, eingegangenen Materialien | Wird verwendet, wenn eine Einkaufsrechnung gebucht wird. Die Gegenbuchung zu diesem Konto sind die Ausgaben für den Kauf von Produkten. Dieses Konto stellt den Bestand in Ihrer Bilanz dar. Das verwendete Konto ist in der Regel dasselbe, das auch für die Kosten der gelieferten Einheiten und die Kosten der für den Verkaufsauftrag in Rechnung gestellten Einheiten verwendet wird. |
| Einkaufswendungen für Produkt | 600180 | Materialeingang | Ausgaben | Gutschrift | Nein | Fr  | |Wird verwendet, wenn eine Einkaufsrechnung gebucht wird. Die Gegenbuchung zu diesem Konto sind die Kosten für eingekaufte Materialien, Einkauf. Dieses Konto stellt den Bestand in Ihrer Bilanz dar. |
| Festgelegter Eingangspreis Gewinn (Kauf, Festgelegter Eingangspreis Gewinn*) | 510310 | Einkaufspreisabweichung | Ausgaben | Gutschrift | Nein | Fr | Fester Zugangspreis - Verlust | Wird verwendet, wenn eine Einkaufsrechnung gebucht wird und es eine Differenz zwischen dem Rechnungspreis und den Standardkosten für den Artikel gibt. Dieses Konto wird verwendet, wenn die Differenz höher ist. Die Gegenbuchung zu diesem Konto ist die Gegenbuchung des festen Eingangspreises. |
| Fester Zugangspreis Verlust (Einkauf, fester Zugangspreis Verlust*) | 510310 | Einkaufspreisabweichung | Ausgaben | Belastung | Nein | Fr | Fester Zugangspreis - Gewinn | Wird verwendet, wenn eine Einkaufsrechnung gebucht wird und es eine Differenz zwischen dem Rechnungspreis und den Standardkosten für den Artikel gibt. Dieses Konto wird verwendet, wenn die Differenz niedriger ist. Die Gegenbuchung zu diesem Konto ist die Gegenbuchung des festen Eingangspreises. |
| Fester Zugangspreisausgleich (Einkauf, fester Zugangspreisausgleich*) | 140900 | Bestandsveränderung | Anlage | Beides | Nein | Fr  | |Wird verwendet, wenn eine Einkaufsrechnung gebucht wird und es eine Differenz zwischen dem Rechnungspreis und den Standardkosten für den Artikel gibt. Dieses Konto ist die Gegenbuchung zu den Gewinn- und Verlustkonten für feste Eingangspreise. |
| Gebühr | NA | NA | NA | NA | NA | NA | NA | Dieses Konto wird nicht mehr verwendet. Verwenden Sie stattdessen die Variante Bestand. |
| Bestandsveränderung | 600170 | Bestandsveränderung | Ausgaben | Gutschrift | Nein | Beides | | Dieses Konto wird verwendet, wenn: <ul><li>Es gibt einen Unterschied im Einheitspreis zwischen Produktzugang und Rechnung.</li><li>Belastungen werden auf den Artikel gebucht.</li><li>Indirekte Kosten wurden<!--note from editor: Edit okay?--> wird zu den gekauften Artikeln hinzugefügt. </li><li>Die Gegenbuchung zu diesem Konto ist das Konto Einkaufsausgaben, nicht fakturiert.</li></ul> |
| Einkauf, Abgrenzung | 200140 | Antizipierte Einkäufe | Passivposten | Gutschrift | Y | P | |Wird verwendet, wenn ein Produktzugang für eine Bestellung gebucht wird und die Option zur Abgrenzung von Kaufbeträgen aktiviert ist. |
| Antizipierte Mehrwertsteuer in Beleg | 250500 | Aufgelaufene Mehrwertsteuer | Passivposten | Gutschrift | Y | Beides  | |Dieses Konto wird verwendet, wenn Sie die Option **Physikalische Steuer buchen** bei den **Parametern der Bestands- und Lagerverwaltung** wählen und Sie einen Kauf mit Steuer haben. Der Betrag wird gebucht, wenn Sie die Bestellung physisch aktualisieren (Produktzugang), und storniert, wenn Sie die Bestellung finanziell buchen (Rechnung). |
| Fester Anlageneingang (Fester Anlagenabgang*) | 180100 | Sachanlagen | Anlage | Belastung | N | Beides | Beides | Dieses Konto wird verwendet, wenn Sie die Option in der Zeile für den Kauf von Anlagen wählen. Die Bestellungsintegration wurde so konfiguriert, dass die Anlage bei Produktzugang oder auf Rechnung erworben wird. Weitere Informationen zur Integration der Bestellung von Anlagen finden Sie unter [Anlagen durch Beschaffung erwerben](/fixed-assets/acquire-assets-procurement). |
| Einkaufsaufwendungen für Ausgaben | 618900 | Sonstige Ausgaben | Ausgaben | Belastung | N | Beides | |Wird verwendet, wenn ein Produktzugang oder eine Rechnung für eine Bestellung gebucht wird, bei der die Artikel nicht auf Lager sind, oder eine Beschaffungskategorie verwendet wird. |
| Vorauszahlung | 132190 | Vorausbezahlte Ausgaben | Anlage | Belastung | N | Beides | | Wird bei der Verarbeitung einer Vorauszahlungsrechnung zu einer Einkaufsrechnung verwendet. |


\*Die in Klammern angegebenen Werte stellen den Wert dar, der im Feld **Buchungsart** auf der Seite **Buchtransaktionen** verwendet wird. Sie können die **Buchungsart** auf der Seite **Buchtransaktionen** auf der Registerkarte **Allgemein** einsehen.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Anlagenbuchung mit Kaufaufträgen

Wenn Sie das Modul **Anlagevermögen** verwenden und den Kauf von Anlagegütern über Bestellungen planen, müssen Sie die Buchungsart **Anlagezugang** auf der Registerkarte **Bestellung** der Seite **Bestandsbuchungsprofil** konfigurieren. Weitere Informationen finden Sie unter [Anlagenintegration](/fixed-assets/fixed-asset-integration.md) und [Anlagen aus Kreditoren erstellen und erwerben](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Buchung von Einkaufsrechnungen mit Vorauszahlung

Wenn Sie die Funktion **Vorauszahlungsrechnung** für Bestellungen verwenden möchten, muss die Buchungsart **Vorauszahlung** auf der Registerkarte **Bestellung** auf der Seite **Bestandsbuchungsprofil** ausgewählt werden. Weitere Informationen finden Sie unter [Vorauszahlungsrechnungen vs. Vorauszahlungen](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Buchung von Bestellanforderungen und Bestellbestätigungen

Bestellanforderungen und Bestellbestätigungen können auch so konfiguriert werden, dass Vorbelastungen und Belastungen in das Hauptbuch gebucht werden. Diese Buchungen werden durch eine Buchungsdefinition gesteuert. Weitere Informationen finden Sie unter [Über Bestellungsbelastungen](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Buchung von Beschaffungskategorien

Alternativ zur Einrichtung der Bestandsbuchung für alle Artikel, eine Gruppe von Artikeln oder einen einzelnen Artikel können Sie Kategorien festlegen und die Ledgerbuchung nach Beschaffungskategorien steuern. Weitere Informationen zum Festlegen von Kategorien und deren Zuweisung zu Produkten finden Sie unter [Beispiel für die Konfiguration von Buchungsprofilen](#sample-posting-profile-configuration) weiter oben in diesem Thema.

Wenn Sie Kategorien mit Bestellungen oder Einkaufsrechnungen verwenden, muss die Kategorienhierarchie dem Typ **Beschaffungskategorienhierarchie** auf der Seite **Kategorienhierarchie-Rollenzuordnungen** zugewiesen werden.

### <a name="vendor-invoices-with-procurement-categories"></a>Lieferantenrechnungen mit Beschaffungskategorien

Wenn Ihr Unternehmen für einige Käufe Bestellungen verwendet und für andere nicht, können Sie Rechnungen, die sich nicht auf Bestellungen beziehen, auf verschiedene Weise verarbeiten. Dazu gehört die Verwendung von Erfassungen in **Kreditorenbuchhaltung** oder durch die Seite **Ausstehende Kreditor-Rechnungen**, die zur Erstellung von Rechnungen für Bestellungen verwendet wird. Wenn Sie Rechnungen für nicht auftragsbezogene Rechnungen erstellen, müssen Sie Beschaffungskategorien für jede Art von Aufwand erstellen. Sie müssen die Kategorie auf der Seite **Bestandsbuchungsprofile** dem richtigen Aufwandskonto zuordnen.

Die genaue Anzahl der Kategorien hängt von der Anzahl der Aufwandskonten ab, die Sie für die Buchung Ihrer Rechnungen verwenden. Sie benötigen mindestens eine Beschaffungskategorie für jedes Hauptkonto, dem Sie Rechnungen, die keine Bestellungen sind, in Rechnung stellen. Für ein einziges Hauptkonto können viele Kategorien verwendet werden. Dies kann für die Benutzerfreundlichkeit, die Durchsuchbarkeit und die Berichterstattung über die von Ihnen verwendeten Ausgabentypen nützlich sein.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Vorteile der Verwendung von Beschaffungskategorien für Kreditorenrechnungen

Einige Vorteile der Verwendung von Beschaffungskategorien für Kreditor Rechnungen sind:

- Konsistente Benutzererfahrung: Wenn Sie Beschaffungskategorien für alle nicht auftragsbezogenen Ausgaben konfigurieren, können Benutzer mit Hilfe der Seite **Ausstehende Rechnungen des Kreditors** auf einen Prozess für die Rechnungsstellung geschult werden.
- Verbesserte Berichterstellung: Wenn Sie Beschaffungskategorien für alle Artikel und alle nicht auftragsbezogenen Ausgaben konfigurieren, analysiert der Bericht über die Beschaffungsausgaben die Ausgaben nach Kreditor, Kategorie und mehr.
- Konsistenter Workflow: Wenn Sie **Anhängige Kreditor-Rechnungen** verwenden, um alle Rechnungen zu verarbeiten, können Sie einen konsistenten Workflow und Genehmigungsprozess erstellen, indem Sie einen einzigen Workflow verwenden.

## <a name="consignment-inventory-posting"></a>Konsignationsbestand buchen

Für Konsignationsbestände wird die gleiche Sachkonto-Buchung wie für andere gekaufte Artikel verwendet. Der Hauptunterschied besteht darin, dass beim Eingang des Bestands keine Transaktionen im Sachkonto erfasst werden. Um das Eigentum auf die Organisation zu übertragen, wenn ein **Bestandseigentumswechsel** Journal gebucht wird, wird ein Beleg erzeugt, um die Kosten des Artikels nachzukalkulieren. Weitere Informationen finden Sie unter [Unterlieferung festlegen](/supply-chain/inventory/consignment.md).
