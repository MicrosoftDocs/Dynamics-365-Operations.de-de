---
title: Auftragsbuchung
description: Dieser Artikel enthält Informationen zur Registerkarte „Auftrag“ auf der Seite „Bestandsbuchungsprofil“.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886312"
---
# <a name="sales-order-posting"></a>Auftragsbuchung

Die Registerkarte **Auftrag** auf der Seite **Bestandsbuchungsprofile** wird verwendet, um zu steuern, wie Aufträge in das Hauptbuch gebucht werden. Für einen Auftrag werden zwei Hauptaktivitäten in das Hauptbuch gebucht: 

- Lieferschein
- Rechnung

Damit eine physische Transaktion (Lieferschein) für einen Auftrag in das Hauptbuch gebucht werden kann, müssen die folgenden Bedingungen erfüllt sein:

- Auf der Seite **Parameter für Lager- und Lagerortverwaltung** muss das Kontrollkästchen **Lieferschein auf Sachkonto buchen** aktiviert sein.
- Auf der Seite **Artikelmodellgruppe** für den in der Auftragszeile ausgewählten Artikel muss das Kontrollkästchen **Physischen Bestand auf Sachkonto buchen** aktiviert sein.
- Auf der Seite **Bestandsbuchungsprofil** müssen für folgende Buchungsarten die Hauptkonten angegeben werden:
  - Kosten der gelieferten Einheiten
  - Gelieferter Wareneinsatz

Damit eine wertmäßige Transaktion (Rechnung) für einen Auftrag in das Hauptbuch gebucht werden kann, müssen die folgenden Bedingungen erfüllt sein:

- Auf der Seite **Artikelmodellgruppe** für den in der Auftragszeile ausgewählten Artikel muss das Kontrollkästchen **Wertmäßigen Bestand auf Sachkonto buchen** aktiviert sein.
- Die Hauptkonten müssen auf der Seite **Bestandsbuchungsprofil** für folgende Buchungsarten angegeben werden:
  - Kosten der fakturierten Einheiten
  - Fakturierter Wareneinsatz
  - Umsatzerlös
  - Rabatt\*

> [!NOTE]
> Das Rabattkonto ist optional. Viele Buchhaltungsvorschriften wie GAAP und IFRS verlangen, dass Rabatte den Umsatzerlös reduzieren, und daher werden diese Konten in vielen Szenarien nicht verwendet. Wenn die örtlichen Vorschriften dies zulassen, verwenden Sie ein separates Hauptkonto, um den rabattierten Teil des Verkaufspreises zu buchen.

Um den verzögerten (geschätzten) Umsatzerlöswert in das Hauptbuch zu buchen, wenn Sie einen Lieferschein für einen Auftrag generieren, müssen die folgenden Bedingungen erfüllt sein:

- Auf der Seite **Artikelmodellgruppe** für den in der Auftragszeile ausgewählten Artikel muss das Kontrollkästchen **Physischen Bestand auf Sachkonto buchen** aktiviert sein.
- Auf der Seite **Artikelmodellgruppe** muss das Kontrollkästchen **Physischen Umsatzerlös buchen** aktiviert sein.
- Auf der Seite **Parameter für Lager- und Lagerortverwaltung** muss das Kontrollkästchen **Lieferschein auf Sachkonto buchen** aktiviert sein.
- Auf der Seite **Parameter für Lager- und Lagerortverwaltung** muss das Kontrollkästchen **Physische Verkaufssteuer buchen** aktiviert sein.
- Auf der Seite **Debitorenparameter** muss das Kontrollkästchen **Lieferschein auf Sachkonto buchen** aktiviert sein.
- Auf der Seite **Bestandsbuchungsprofil** müssen für folgende Buchungsarten die Hauptkonten angegeben werden:
  - Lieferschein-Umsatzerlös
  - Lieferschein-Umsatzerlös - Gegenkonto
  - Verzögerte Mehrwertsteuer bei Lieferung

> [!NOTE]
> Wir empfehlen generell, die Optionen **Physischen Bestand buchen** und **Lieferschein auf Sachkonto buchen** zu aktivieren. Die Aktivierung dieser Optionen kann dazu beitragen, den Monatsabschluss zu beschleunigen, da keine Abgrenzungen manuell berechnet und gebucht werden müssen. Darüber hinaus spiegeln Finanzaufstellung die gestundeten Beträge automatisch ohne manuelles Eingreifen wider.

> [!IMPORTANT]
> Die Option **Physischen Umsatzerlös buchen** wird nicht mit der Umsatzerlöserkennung verwendet. Weitere Informationen zur Umsatzerlöserkennung finden Sie unter [Übersicht über die Umsatzerlöserkennung](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Beispiel für die Konfiguration eines Buchungsprofils 

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten mit beispielhaften Hauptkonten und Beschreibungen:
 
- Die Spalte **Clearingkonto** gibt an, dass es sich bei der Buchungsart um ein Verrechnungskonto handelt. Der auf diesem Konto gebuchte Betrag wird automatisch storniert, wenn eine spätere Transaktion gebucht wird. 
- Bei der Spalte **P/F** steht **P** für physische Buchungen und **F** für Finanzbuchungen. 
- Die Spalte **Folgen** gibt an, ob das Hauptkonto für eine bestimmte Buchungsart typischerweise mit einer anderen Buchungsart identisch ist. Der Wert in der Spalte gibt die Art der Buchung an, die normalerweise verwendet wird.

> [!NOTE]
> Diese Hauptkonten und Hauptkontonamen sind nur Vorschläge. Wir empfehlen Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um die beste Konfiguration für Ihre geschäftlichen Anforderungen zu ermitteln.


| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Kosten der gelieferten Einheiten | 140100</br>140101 | Materialbestand</br>Materialien versendet, nicht fakturiert | Anlage | Gutschrift | Ja | P | Kosten der fakturierten Einheiten | Wird verwendet, wenn ein Lieferschein zum Auftrag gebucht wird. Das Gegenkonto zum Konto ist der Wareneinsatz der gelieferten Waren. Der auf diesem Konto vorhandene Betrag wird storniert, wenn eine Rechnung für einen Auftrag gebucht wird. Möglicherweise möchten Sie ein Konto für versandte, nicht in Rechnung gestellte Materialien verwenden, um den physischen Bestand darzustellen, und das Materialbestandskonto für die Finanzaktualisierung reservieren. |
| Gelieferter Wareneinsatz | 500150 | Verzögerter Wareneinsatz | Ausgaben | Belastung | Ja | P  | Wird verwendet, wenn ein Lieferschein zum Auftrag gebucht wird. Das Gegenkonto zum Konto sind die Kosten der gelieferten Einheiten. Der auf diesem Konto vorhandene Betrag wird storniert, wenn eine Rechnung für einen Auftrag gebucht wird. |
| Kosten der fakturierten Einheiten | 140100 | Materialbestand | Anlage | Gutschrift | Nein | Fr | Kosten der gelieferten Einheiten | Wird verwendet, wenn eine Rechnung zum Auftrag gebucht wird. Das Gegenkonto zum Konto ist der Wareneinsatz der fakturierten Waren. Dieses Konto stellt den Bestand in Ihrer Bilanz dar. |
| Fakturierter Wareneinsatz | 500100 | COGS-Materialien (Wareneinsatz) | Ausgaben | Belastung | Nein | Fr  | Wird verwendet, wenn eine Rechnung zum Auftrag gebucht wird. Das Gegenkonto zum Konto sind die Kosten der fakturierten Einheiten. Dieses Konto repräsentiert den COGS (Wareneinsatz) auf Ihrer G&amp;V-Aufstellung. |
| Umsatzerlös (Auftragsumsatzerlös*) | 400100 | Umsatzerlösmaterialien | Umsatzerlös | Gutschrift | Nein | Fr   | Wird verwendet, wenn eine Rechnung zum Auftrag gebucht wird. Das Gegenkonto zu diesem Konto ist das Übersichtskonto (Kundensaldo*) auf dem **Debitorenbuchungsprofil**. |
| Provision (Verkäufe, Provision*) | 602150 | Provisionsausgaben | Ausgaben | Belastung | Nein | Fr  | Wird verwendet, wenn die Provision für einen Verkauf aktiviert und berechnet und während des Rechnungsvorgangs für den Auftrag gebucht wird. Das Gegenkonto zu diesem Konto ist die zu zahlende Provision. |
| Provisionsgegenkonto (Verkauf, Provisionsgegenkonto*) | 201110 | Zahlbare Provisionen | Passivposten | Gutschrift | Ja | Fr | Wird verwendet, wenn die Provision für einen Verkauf aktiviert und berechnet und während des Rechnungsvorgangs für den Auftrag gebucht wird. Das Gegenkonto zu diesem Konto sind die Provisionsausgaben. |
| Verzögerter Umsatzerlös bei Lieferung (Verkäufe – Lieferschein-Umsatzerlös*) | 401400 | Aufgelaufene Verkäufe | Umsatzerlös | Gutschrift | Ja | P  | Wird verwendet, wenn aufgeschobene Umsatzerlöse für die Lieferung aktiviert sind, und wird gebucht, wenn Sie einen Lieferschein zum Auftrag verarbeiten. Das Gegenkonto zu diesem Konto ist das Gegenkonto für verzögerte Umsatzerlöse. Die Beträge auf diesem Konto werden automatisch storniert, wenn Sie die Auftragsrechnung buchen. |
| Gegenkonto für verzögerten Umsatzerlösaus bei Lieferung (Verkäufe – Lieferschein-Umsatzerlös, Gegenkonto)* | 130400 | Debitoren – nicht fakturiert | Anlage | Belastung | Ja | P  | Wird verwendet, wenn aufgeschobene Umsatzerlöse für die Lieferung aktiviert sind, und eine Buchung erfolgt, wenn Sie einen Lieferschein zum Auftrag verarbeiten. Das Gegenkonto zu diesem Konto sind die verzögerten Umsatzerlöse bei Lieferung. Die Beträge auf diesem Konto werden automatisch storniert, wenn Sie die Auftragsrechnung buchen. |
| Verzögerte Mehrwertsteuer bei Lieferung (Verkäufe, Lieferscheinsteuer*) | 250500 | Verzögerte Mehrwertsteuer | Passivposten | Gutschrift | Ja | P  | Wird verwendet, wenn der verzögerte Umsatzerlös für die Lieferung aktiviert ist und „Physische Verkaufssteuer buchen“ aktiviert ist. Der Steuerbetrag wird gebucht, wenn Sie einen Lieferschein zum Auftrag verarbeiten. |

\*Die in dieser Tabelle in Klammern angezeigten Werte stellen den Wert dar, der im Feld **Buchungsart** auf der Seite **Gutscheintransaktionen** verwendet wird. Sie können den **Buchungstyp** auf der Seite **Belegtransaktionen** auf der Registerkarte **Allgemein** sehen.

## <a name="sales-category-posting"></a>Verkaufskategoriebuchung

Als Alternative zum Einrichten der Bestandsbuchung für alle Artikel, eine Gruppe von Artikeln oder einen einzelnen Artikel können Sie Kategorien einrichten und die Sachkontobuchung nach Verkaufskategorien steuern. Weitere Informationen zum Einrichten einer Kategoriehierarchie und zum Zuweisen von Kategorien zu Produkten finden Sie unter [Eine Hierarchie zur Produktklassifizierung erstellen](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) und [Produkt mithilfe der Kategoriehierarchien klassifizieren](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Nachdem Sie eine Kategoriehierarchie erstellt haben, müssen Sie die Hierarchie einem oder mehreren Typen zuweisen. Um eine Kategoriehierarchie für Aufträge zu verwenden, müssen Sie die Kategorie dem Kategoriehierarchietyp „Verkauf“ zuweisen. Weitere Informationen finden Sie unter [Info zu Kategoriehierarchien](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Umsatzerlösbuchung Verkaufskategorie erstellen

Führen Sie die folgenden Schritte aus, um Sachkontobuchungen für einen Auftrag basierend auf einer Verkaufskategorie zuzuweisen:

1. Navigieren Sie zu **Lagerverwaltung** > **Einstellungen** > **Buchung** > **Buchung**.
2. Wählen Sie die Registerkarte **Verkauf** aus.
3. Wählen Sie das Optionsfeld für den Buchungstyp aus, den Sie konfigurieren möchten (z. B. **Umsatzerlös**).
4. Wählen Sie **Neu** aus.
5. Wählen Sie im Feld **Artikelcode** die Option **Kategorie** aus.
6. Wählen Sie im Feld **Kategorierelation** die Kategorie für das Buchungsprofil aus.
7. Wählen Sie im Feld **Kontocode** eine Option für **Tabelle**, **Gruppe** oder **Alle** aus. Um beispielsweise das Buchungsprofil auf alle Kunden anzuwenden, wählen Sie **Alle** aus.
   - Wenn Sie **Tabelle** in Schritt 6 ausgewählt haben, wählen Sie die entsprechende **Lieferantennummer** für das Buchungsprofil im Feld **Kontorelation** aus.
   - Wenn Sie **Gruppe** in Schritt 6 ausgewählt haben, wählen Sie die entsprechende **Lieferantengruppe** für das Buchungsprofil im Feld **Kontorelation** aus.
   - Wenn Sie **Alle** in Schritt 6 ausgewählt haben, bleibt das Feld **Kontorelation** leer.

8. Wählen Sie eine **Mehrwertsteuergruppe** aus, um dem ausgewählten Buchungstyp eine bestimmte Steuergruppe zuzuordnen. Wenn Sie dieses Feld leer lassen, gilt der Buchungstyp für alle vorhandenen Steuergruppen. Die für Steuergruppen angegebene Buchung gilt nur für Verkaufs- und Einkaufsbuchungen.

9. Geben Sie im Feld **Hauptkonto** die Kontonummer an, auf die der Kontotyp gebucht werden soll. Wählen Sie im Kontenplan eine vorhandene Kontonummer aus.
