---
title: Lagerbuchung
description: Dieses Thema erläutert die Registerkarte „Lagerbuchung“ auf der Seite „Lagerbuchungsprofil“.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783369"
---
# <a name="inventory-posting"></a>Lagerbuchung

Die Registerkarte **Bestand** auf der Seite **Lagerbuchungsprofile** wird verwendet, um zu steuern, wie Lagerbuchungen in das Hauptbuch gebucht werden. Lagerbuchungen sind Buchungen, die nicht aus Vertriebsaufträgen, Bestellungen oder Fertigungsaufträgen erstellt werden. Sie buchen die physischen und finanziellen Updates gleichzeitig automatisch für den Bestand. Eine Ausnahme sind Umlagerungsaufträge, die physische und finanzielle Updates trennen, wenn Sie Bestand versenden und erhalten.

In der folgenden Tabelle sind einige Beispiele für Lagerbuchungen dargestellt:

| Transaktionstyp | Zugang oder Abgang | Physische Buchung, Finanzbuchung oder beides | Description |
|---|---|---|---|
| Bewegung | Beides | Beides | <p>Eine Verlagerungserfassung ist ein Bestandsjournal, das Sie verwenden können, um Bestand hinzuzufügen oder zu entfernen. Es funktioniert wie eine Bestandsanpassungserfassung. Ein wichtger Unterschied ist allerdings, dass das Hauptkonto, das zur Abweichung des Eintrags führt, angegeben wird.</p><p>Die Umlagerungserfassung trägt Anfangssalden und einmalige Abrechnungssalden ein, die aufgewendet werden müssen. Beispielsweise wird dies verwendet, wenn der Bestand für eine Vertriebsprobe entnommen wird.</p><p>Wenn die Erfassung gebucht wird, geschehen die physischen und finanziellen Buchungen gleichzeitig.</p><p>Positive Mengen in den Erfassungspositionen stellen Eingänge und negative Mengen Abgänge dar.</p> |
| Lagerregulierung | Beides | Beides | Eine Bestandsanpassungserfassung wird verwendet, um Bestand hinzuzufügen oder zu entfernen. Es lässt keine Auswahl eines Abweichungskontos zu. Nur die Konten, die auf der Seite **Bestandsbuchungsprofile** angegeben sind, werden für ein Update des Hauptbuchungseintrags verwendet. |
| Umlagerung (Erfassung) | Beides | Beides | <p>Eine Umlagerungserfassung wird verwendet, um Bestand von einem Lagerort zum anderen zu verschieben (unter Verwendung von Speicherdimensionen). Sie aktualisiert die Produktinformationen bei einer Bestandsbuchung mit neuen Produkt- oder Verfolgungsdimensionen.</p><p>Eine Umlagerungserfassung erstellt eine Position für die Verschiebung eines Artikels. Diese Position hat die Felder „von“ und „zu“ für die Lagerdimensionen. Jede Position in einer Umlagerungserfassung erstellt zwei Bestandsbuchungen. Eine Buchung wird für die „von“-Bestandsdimension erstellt. Sie stellt den Abgang dar und hat eine negative Menge. Die andere Buchung wird für die „an“-Bestandsdimension erstellt. Sie stellt den Eingang dar und hat eine positive Menge.</p><p>Umlagerungserfassungen erstellen möglicherweise keinen Beleg, wenn die Verschiebung des Bestands als eine nicht-finanzielle Umbuchung betrachtet wird. Bestandsdimensionen, die sich von den „von“ oder „an“ Werten unterscheiden, werden auf der Seite **Speicherdimensionsgruppe** oder **Verfolgungsdimensionsgruppe** mit der Option **Finanzbestand** markiert. Wenn die Option **Finanzbestand** beispielsweise auf der Dimension **Lagerort** nicht markiert wird und Sie Bestand von einem Lagerort an einen anderen Lagerort am selben Standort und Lager verschieben, wird kein Beleg erstellt.</p><p>Umbuchungserfassungen unterscheiden sich von Umlagerungsaufträgen, in sofern, dass es keine Dokumente für die Verschiebung gibt. Das Update wird in einer Transaktion durch Buchung der Erfassung durchgeführt. Im Gegensatz dazu kann ein Umlagerungsauftrag Dokumente für Entnahme und Versand generieren und erfordert zwei Aktualisierungen für die Verarbeitung der Transaktion.</p> |
| Umlagerungsauftragslieferung | Problem | Beides | <p>Wenn Sie einen neuen Umlagerungsauftrag erstellen, hat jede Kombination einer Position und einer Bestanddimension zwei Bestandsbuchungen: eine für die Versendung des Umlagerungsauftrags und eine für den Eingang des Umlagerungsauftrags. Wenn Sie den Umlagerungsauftrag versenden, werden zwei Bestandsbuchungen aktualisiert und zwei zusätzliche Bestandsbuchungen für den Warentransport erstellt, also insgesamt vier Bestandsbuchungen.</p><ol><li>Die erste Bestandstransaktion wird verwendet, um den Artikel aus dem Quelllagerort und der elektronischen Adresse zu entfernen. Der Ausgabestatus dieser Transaktion ist **Verkauft**, um anzuzeigen, dass der Artikel nicht mehr am Lagerort verfügbar ist.</li><li>Die zweite Bestandstransaktion wird verwendet, um den Artikel dem Transitlagerort hinzuzufügen, das für den Lagerort ausgewählt ist, aus dem der Artikel umgelagert wird. Der Status dieser Belegtransaktion ist **Gekauft**.</li><li>Die dritte Bestandbuchung dient der Umlagerung vom Transitlagerort zum Ziellagerort. Der Status dieser Ausgabebuchung ist **Reserviert physisch**. Dieser Status stellt sicher, dass der Artikel nicht von einem anderen Prozess genutzt werden kann, während er noch unterwegs ist.</li><li>Die vierte Bestandbuchung dient dem Wareneingang im Ziellagerort. Der Status dieser Belegbuchung ist **Bestellt**.</li></ol> |
| Umlagerungsauftragsempfang | Zugang | Beides | Wenn ein Umlagerungsauftrag im Ziellagerort eingeht, wird der Bestandsstatus der Bestandsbuchung im Transitlagerort (Nummer 3 im vorherigen Beispiel) wird auf **Verkauft** aktualisiert, und der Bestandsstatus der Bestandsbuchung für den Ziellagerort wird auf **Gekauft** aktualisiert. |
| Stücklisten | Beides | Beides | Sie können eine Stücklistenerfassung (BOM) verwenden, um ein Produkt als fertig zu melden und die während des Prozesses verbrauchten Rohmaterialien zu verbrauchen, ohne einen Produktionsauftrag zu verwenden. Eine Stücklistenerfassung enthält normalerweise mindestens eine positive Zeile für das fertige Produkt und eine oder mehrere negative Zeilen für die verbrauchten Rohstoffe. Die Zeile für fertiggestellte Ware ist ein Zugang in den Bestand, während die negativen Zeilen Abgänge aus dem Bestand für die Rohmaterialien sind. Wenn Sie eine Stücklistenerfassung erstellen, ist die erste Zeile die Kopfzeile der Stückliste, und die nachfolgenden Zeilen, die hinzugefügt werden, sind die Stücklistenzeilen. |
| Bestandseigentümeränderung | Beides | Beides | Eine Bestandsbesitz-Journaländerung wird verwendet, um den Besitz des Lieferungsbestandes vom Kreditor auf die Ihre Organisation zu ändern. Erfassungen zur Änderung des Bestandsbesitzes ähneln Bestandsumbuchungserfassungen, da zwei Bestandstransaktionen mit jeder Kombination aus einer Position und einer Bestandsdimension verknüpft sind. Eine Bestandsbuchung entfernt den Bestand vom Kreditor in der **Besitz**-Dimension, und die andere fügt das Element der juristischen Person in der **Besitz**-Dimension hinzu. |
| Wareneingang | Zugang | Physisch | Eine Artikeleingangserfassung wird verwendet, um den Zugangsstatus des Bestands auf **Eingetragen** zu aktualisieren. Es wird in der Regel für den Eingang von Bestellungen und Retouren von Aufträgen verwendet. |
| Produktions-Wareneingang | Zugang | Physisch | Eine Herstellungseingangserfassung ähnelt einer Artikeleingangserfassung. Ein Produktionseingang wird verwendet, um fertige Ware aus einem Produktionsauftrag im Lagerort zu erhalten. Wenn die Erfassung gebucht wird, wird der Status der Bestandbuchung auf **Eingetragen** aktualisiert. |
| Inventur | Beides | Beides | Eine Zählerfassung wird verwendet, um die Menge der Artikel aufzuzeichnen, die für eine bestimmte Kombination von Bestandsdimensionen gezählt wurden. Bestandsbuchungen werden erstellt, wenn die Zeile der Erfassung eine Zähldifferenz aufweist. Eine Zeile mit einer höheren gezählten Menge führt zu einem Eingang in den Bestand. Eine Zeile mit einer niedrigeren gezählten Menge führt zu einem Abgang aus dem Bestand. Zeilen, in denen die gezählte Menge mit der erwarteten Menge übereinstimmt, haben keine Bestandsbuchungen. |
| Markierungen zählen | Nicht zutreffend | Nicht zutreffend | Ein Tag-Zähljournal wird verwendet, um Bestands-Tags zu verfolgen, die zugewiesen und in einer vollständigen Bestandzählung verwendet werden. Sie können die Erfassung verwenden, um einer bestimmten Kombination aus einem Artikel und einer Bestandsdimension eine Tag-Nummer zuzuweisen und den Status dieses Tags während einer vollständigen Bestandsaufnahme zu verfolgen. Tag-Zählungserfassungen erstellen keine Bestandsbuchungen. |
| Qualitätsprüfungsaufträge | Problem | Physisch | <p>Ein Qualitätsprüfungsauftrag wird verwendet, um Testergebnisse für ein bestimmtes Los im Bestand aufzuzeichnen. Jeder Qualitätsprüfungsauftrag bezieht sich auf eine bestehende Bestandsbuchung oder einen Teil einer Bestandsbuchung.</p><p>Ein Qualitätsprüfungsauftrag generiert in zwei Situationen eine neue Bestandsbuchung:</p><ul><li>Der Qualitätsprüfungsauftrag ist als **Zerstörerischer Test** auf der Registerkarte **Allgemein** gekennzeichnet.</li><li>Der Qualitätsprüfungsauftrag ist als **Quarantäne bei fehlgeschlagener Validierung** auf der Registerkarte **Allgemein** gekennzeichnet, und der Test besteht die Validierung nicht. In diesem Fall werden zwei Bestandsbuchungen erstellt. Eine Bestandsbuchung entfernt den Artikel aus der ursprünglichen Kombination aus Bestandsdimension und Lagerort, und die andere fügt dem Quarantänelagerplatz den Artikel hinzu.</li></ul> |
| Quarantäneaufträge | Beides | Beides | <p>Die Bestandsbuchungen eines Quarantäneauftrags sind wie ein Umlagerungsauftrag. Ein Quarantänelagerplatz dient der Bestandsverfolgung. Es gibt zwei Zugangsbuchungen und zwei Ausgabebuchungen.</p><p>Wenn Sie die Bestellung erstmalig erstellen, werden zwei Buchungen erstellt. Die Belegbuchung hat den Status **Bestellt** für den Quarantänelagerplatz, das mit dem Lagerplatz verknüpft ist, in dem sich der Artikel befindet. Die Ausgabebuchung hat den Status **Auf Bestellung** für den Lagerplatz, an dem der Artikel gelagert wird.</p><p>Wenn Sie den Quarantäneauftrag starten, werden zwei zusätzliche Buchungen erstellt und die vorhandenen Buchungen aktualisiert. Der Status der Eingangsbuchung für den Quarantänelagerplatz wird auf **Erhalten** aktualisiert, und der Status der Entnahmebuchung für den Lagerplatz wird auf **Abgezogen** aktualisiert.</p><p>Die beiden neuen Buchungen werden verwendet, um die eventuelle Bewegung zurück zum Lagerhaus anzuzeigen. Die Belegbuchung hat den Status **Bestellt** für das Lagerhaus, und diese Entnahmebuchung hat den Status **Reserviert physisch** für den Quarantänelagerplatz.</p><p>Wenn Sie einen Quarantäneauftrag als abgeschlossen melden, stellt dieser Vorgang die physische Aktualisierung des Quarantäneauftrags dar. Der Wareneingangsstatus im Lagerhaus wird auf **Erhalten** aktualisiert.</p><p>Wenn Sie einen Quarantäneauftrag beenden, stellt dieser Vorgang die finanzielle Aktualisierung des Quarantäneauftrags dar. Der Status der Ausgabebuchung wird auf **Verkauft** aktualisiert, und der Status der Belegbuchung wird auf **Gekauft** aktualisiert.</p><p>Alternativ können Sie den Quarantäneauftrag verwerfen. Dieser Vorgang entfernt den Artikel aus dem Bestand. Wenn Sie einen Quarantäneauftrag verwerfen, bleiben nur drei Buchungen übrig. Die Zugangsbuchung für das Lagerhaus wird entfernt und der Status der verbleibenden Zugangsbuchung wird **Gekauft** aktualisiert. Der Status der beiden Ausgabebuchungen wird auf **Verkauft** geändert. Dieser Vorgang ist eine physische und finanzielle Aktualisierung der Bestellung.</p> |

## <a name="fixed-receipt-price-posting"></a>Buchung des festen Zugangspreises

Mit dem festen Eingangspreis können Sie Standardkosten für ein Produkt verwenden. Es ist eine Alternative zur Auswahl der **Standardkosten**-Option auf der **Artikelmodellgruppe**-Seite für einen Artikel. Der Hauptunterschied bei der Verwendung eines festen Eingangspreises besteht darin, dass der derzeit konfigurierte Einstandspreis für den Artikel verwendet wird, wenn der Wareneingang im Bestand gebucht wird. Für einen festen Eingangspreis gibt es keinen Kostenneubewertungsprozess. Wenn eine Finanzaktualisierung gebucht wird, wird der aktuelle Einstandspreis zum Zeitpunkt der Buchung verwendet. Wenn sich der Einstandspreis, der beim Eingang verwendet wird, und der der Rechnung unterscheiden, wird die Abweichung auf die Gewinn- und Verlustkonten für den festen Eingangspreis gebucht.

Um optional einen Fixpreis für ein Produkt zu verwenden, müssen Sie die folgende Konfiguration durchführen:

- Aktivieren Sie das Kontrollkästchen **Physischen Bestand buchen** auf der Seite **Artikelmodellgruppe** für den in der Bestandbuchungsposition ausgewählten Artikel.
- Aktivieren Sie das Kontrollkästchen **Fester Zugangspreis** auf der Seite **Artikelmodellgruppe**.
- Geben Sie das Hauptkonto für die folgenden Buchungstypen auf der Seite **Bestandsbuchungsprofil** an.

    - Fester Zugangspreis - Gewinn
    - Fester Zugangspreis - Verlust

Weitere Informationen finden Sie unter [Fester Zugangspreis](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Buchung des Artikelgewichts

Artikelgewichtsprodukte werden häufig in Branchen wie der Lebensmittelbranche verwendet, in denen das Gewicht und/oder die Größe von Produkten leicht variieren können. Für Artikelgewichtsprodukte werden zwei Maßeinheiten verwendet: eine Lagereinheit und eine Artikelgewichtseinheit. Das Gewicht des Bestands kann bei Ankunft am Lagerort vom Gewicht des Bestands bei Entnahme aus dem Lagerort abweichen. Die Artikelgewichtproduktverarbeitung passt den Bestand an.

Bei einer Abweichung des Artikelgewichts werden die Differenzen auf die in den Feldern **Artikelgewichtsverlust** und **Artikelgewichtsgewinn** auf der **Bestandsbuchungsprofil**-Seite angegebenen Konten gebucht. Typischerweise wird in beiden Feldern dasselbe Hauptkonto angegeben.

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten und enthalten beispielhafte Hauptkonten und Beschreibungen.

- Die „Soll/Haben?“ Spalte zeigt an, ob die Transaktion typischerweise eine Soll oder Haben bucht. In manchen Fällen kann die Transaktion entweder Soll oder Haben buchen.
- Die Spalte „Verrechnungskonto“ zeigt an, dass die Buchungsart ein Verrechnungskonto ist. Mit anderen Worten: Der Betrag, der auf diesem Konto gebucht wird, wird automatisch storniert, wenn eine spätere Transaktion gebucht wird.
- Die Spalte „P/F“ zeigt die Art der Buchung an. „P“ steht für die physische Buchung und „F“ für die finanzielle Buchung.
- Die Spalte „Folgen“ zeigt an, ob das Hauptkonto für die Buchungsart in der Regel dasselbe ist wie das Hauptkonto für eine andere Buchungsart. Insbesondere gibt es den Buchungstyp an, der typischerweise für die Buchung verwendet wird.

> [!NOTE]
> Die Hauptkonten und die Namen der Hauptkonten in der Tabelle sind Vorschläge. Wir empfehlen Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um die beste Konfiguration für Ihre geschäftlichen Anforderungen zu ermitteln.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|---|---|---|---|---|---|---|---|---|
| Artikelgewicht - Verlustkonto | 510520 | Lagerregulierung | Ausgaben | | Nein | Beides | Artikelgewicht - Gewinnkonto | Dieses Konto wird verwendet, wenn Sie eine Bestandsbuchung buchen, bei der der Artikelgewichtsbetrag niedriger ist. |
| Artikelgewicht - Gewinnkonto | 510520 | Lagerregulierung | Ausgaben | | Nein | Beides | Artikelgewicht - Verlustkonto | Dieses Konto wird verwendet, wenn Sie eine Bestandsbuchung buchen, bei der der Artikelgewichtsbetrag höher ist. |

Weitere Informationen zu Artikelgewichtsprodukten finden Sie unter [Infos zu Artikeln mit Artikelgewicht](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) und [Produktverarbeitung beim Artikelgewicht mit Warehouse Management](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Umlagerungsbuchung von Bestand zu Anlagen

Die Erfassung für Bestand zu Anlage (**Anlage** \> **Erfassungen** \> **Erfassung für Bestand zu Anlage**) wird verwendet, um Artikel aus dem Bestand zu verschieben und sie in Anlagen umzuwandeln. Weitere Informationen finden Sie unter [Anlage-Integration](/fixed-assets/fixed-asset-integration.md).

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten und enthalten beispielhafte Hauptkonten und Beschreibungen.

- Die „Soll/Haben?“ Spalte zeigt an, ob die Transaktion typischerweise eine Soll oder Haben bucht. In manchen Fällen kann die Transaktion entweder Soll oder Haben buchen.
- Die Spalte „Verrechnungskonto“ zeigt an, dass die Buchungsart ein Verrechnungskonto ist. Mit anderen Worten: Der Betrag, der auf diesem Konto gebucht wird, wird automatisch storniert, wenn eine spätere Transaktion gebucht wird.
- Die Spalte „P/F“ zeigt die Art der Buchung an. „P“ steht für die physische Buchung und „F“ für die finanzielle Buchung.
- Die Spalte „Folgen“ zeigt an, ob das Hauptkonto für die Buchungsart in der Regel dasselbe ist wie das Hauptkonto für eine andere Buchungsart. Insbesondere gibt es den Buchungstyp an, der typischerweise für die Buchung verwendet wird.

> [!NOTE]
> Die Hauptkonten und die Namen der Hauptkonten in der Tabelle sind Vorschläge. Wir empfehlen Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um die beste Konfiguration für Ihre geschäftlichen Anforderungen zu ermitteln.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|---|---|---|---|---|---|---|---|---|
| Anlagenabgang | 180100 | Materielle Vermögenswerte | Anlage | Gutschrift | Nein | Beides | Nicht zutreffend | Dieses Konto wird verwendet, wenn Sie einen Bestand in die Anlageerfassung buchen, um einen Artikel aus dem Bestand zu entfernen und ihn in eine Anlage umzuwandeln. |

## <a name="moving-average-posting"></a>Buchung mit gleitendem Durchschnitt

Der gleitende Durchschnitt ist eine fortlaufende Nachkalkulation, die auf dem Durchschnittsprinzip basiert. Die Kosten für Bestandsausgaben ändern sich nicht, wenn sich die Anschaffungskosten ändern. Der Unterschied ist aktiviert und basiert auf eine proportionale Berechnung. Der verbleibende Betrag wird in Aufwand gebucht.

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten mit beispielhaften Hauptkonten und Beschreibungen.

- Die „Soll/Haben?“ Spalte zeigt an, ob die Transaktion typischerweise eine Soll oder Haben bucht. In manchen Fällen kann die Transaktion entweder Soll oder Haben buchen.
- Die Spalte „Verrechnungskonto“ zeigt an, dass die Buchungsart ein Verrechnungskonto ist. Mit anderen Worten: Der Betrag, der auf diesem Konto gebucht wird, wird automatisch storniert, wenn eine spätere Transaktion gebucht wird.
- Die Spalte „P/F“ zeigt die Art der Buchung an. „P“ steht für die physische Buchung und „F“ für die finanzielle Buchung.
- Die Spalte „Folgen“ zeigt an, ob das Hauptkonto für die Buchungsart in der Regel dasselbe ist wie das Hauptkonto für eine andere Buchungsart. Insbesondere gibt es den Buchungstyp an, der typischerweise für die Buchung verwendet wird.

> [!NOTE]
> Die Hauptkonten und die Namen der Hauptkonten in der Tabelle sind Vorschläge. Wir empfehlen Ihnen, mit Ihrem Buchhalter zusammenzuarbeiten, um die beste Konfiguration für Ihre geschäftlichen Anforderungen zu ermitteln.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|---|---|---|---|---|---|---|---|---|
| Preisdifferenz für flexiblen Durchschnitt | 510600 | Preisdifferenz bei gleitendem Durchschnitt | Ausgaben | Beides | Nein | Beides | Nicht zutreffend | Dieses Konto wird verwendet, wenn es einen Kostenunterschied zwischen dem Beleg und der Rechnung gibt. |
| Neubewertung für flexiblen Durchschnitt | 510610 | Neubewertung für flexiblen Durchschnitt | Ausgaben | Beides | Nein | Beides | Nicht zutreffend | Dieses Konto wird verwendete, wenn Sie die Kosten mit gleitendem Durchschnitt eines Produkts regulieren |

## <a name="sample-posting-profile-configuration"></a>Beispiel für die Konfiguration eines Buchungsprofils

Die folgende Tabelle zeigt Beispiele für die Standardbuchungsarten mit beispielhaften Hauptkonten und Beschreibungen.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | P/F | Folgen | Description |
|---|---|---|---|---|---|---|---|---|
| Lagerabgang | 140100 | Materialbestand | Anlage | Gutschrift | Nein | Beides | Lagerzugang | Dieses Konto wird verwendet, wenn eine gebuchte Bestandsbuchung eine Ausgabe (negative Menge) ist und nichts mit Verkäufen, Einkäufen oder der Produktion zu tun hat. Der Ausgleich zu diesem Konto ist das Bestandsausgaben-, Verlustkonto. Dieses Konto stellt in der Regel den Bestand in Ihrer Bilanz dar. |
| Bestandsaufwendungen, Verlust | 510100 | Bestand - Gewinn und Verlust | Ausgaben | Belastung | Nein | Beides | Bestandsaufwendungen, Gewinn | Dieses Konto wird verwendet, wenn eine gebuchte Bestandsbuchung eine Ausgabe (negative Menge) ist und nichts mit Verkäufen, Einkäufen oder der Produktion zu tun hat. Der Ausgleich zu diesem Konto ist das Bestandsausgabenkonto. |
| Lagerzugang | 140100 | Materialbestand | Anlage | Belastung | Nein | Beides | Lagerabgang | Dieses Konto wird verwendet, wenn eine gebuchte Bestandsbuchung ein Eingang (positive Menge) ist und nichts mit Verkäufen, Einkäufen oder der Produktion zu tun hat. Der Ausgleich zu diesem Konto ist das Bestandsausgaben-, Gewinnkonto. Dieses Konto stellt in der Regel den Bestand in Ihrer Bilanz dar. |
| Bestandsaufwendungen, Gewinn | 510100 | Bestand - Gewinn und Verlust | Ausgaben | Gutschrift | Nein | Beides | Bestandsaufwendungen, Verlust | Dieses Konto wird verwendet, wenn eine gebuchte Bestandsbuchung ein Eingang (positive Menge) ist und nichts mit Verkäufen, Einkäufen oder der Produktion zu tun hat. Der Ausgleich zu diesem Konto ist das Bestandseingangskonto. |
| Umlagerungszugang | 231500 | Einheitsbezogen Fällig | Passivposten | Belastung | Nein | Beides | | Dieses Konto wird verwendet, wenn der Bestand zwischen Bestandsdimensionen wie Standorten übertragen wird und die Kosten eines Artikels zwischen den Standorten unterschiedlich sind. |
| Umlagerungsabgang | 131500 | Einheitsbezogene Forderungen | Anlage | Gutschrift | Nein | Beides | | Dieses Konto wird verwendet, wenn der Bestand zwischen Bestandsdimensionen wie Standorten übertragen wird und die Kosten eines Artikels zwischen den Standorten unterschiedlich sind. |
