---
title: Produktprogrammplanung mit Beschaffungsplanungen
description: Dieser Artikel beschreibt, wie Beschaffungsplanung während der Masterplanung berücksichtigt werden.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2bac9355bb1ac00f697ec459f494a64553e0eacc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740140"
---
# <a name="master-planning-with-supply-forecasts"></a>Produktprogrammplanung mit Beschaffungsplanungen

[!include [banner](../../includes/banner.md)]

Mit Beschaffungsplanungen können Sie das Angebot angeben, das Sie voraussichtlich in einem zukünftigen Zeitraum benötigen werden. In der Regel basieren Sie die Schätzung auf der Verkaufshistorie des Vorjahres und verwenden dann die Prognose für Budgetierungszwecke. Sie können Ihre Masterpläne auch so einrichten, dass Prognosen während der Planung berücksichtigt werden.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Einen Masterplan so festlegen, dass er eine Beschaffungsplanung berücksichtigt

Sie können angeben, ob jeder Hauptplan Prognosen berücksichtigen soll, wenn er ausgeführt wird. Verwenden Sie das folgende Verfahren, um Vorhersageoptionen für jeden Plan festzulegen.

1. Wechseln Sie zu **Produktprogrammplanung \> Einrichtung \> Pläne \> Produktprogrammpläne**.
1. Wählen Sie entweder einen vorhandenen Masterplan im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um ein neues Profil zu erstellen.
1. Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:

    - **Planungsmodell** – Wählen Sie das Modell aus, das die Angebots- und/oder Nachfrageprognosen enthält, die vom Masterplan berücksichtigt werden sollen.
    - **Bestandsprognose einbeziehen** – Legen Sie diese Option auf *Ja* fest, wenn der Masterplan Beschaffungsplanungen berücksichtigen soll.
    - **Bedarfsplanung einbeziehen** – Legen Sie diese Option auf *Ja* fest, wenn der Masterplan Bedarfsplanungen berücksichtigen soll. Obwohl diese Einstellung unabhängig von der Einstellung **Beschaffungsplanung einschließen** ist, gelten einige der anderen Einstellungen auf der Seite sowohl für Beschaffungsplanungen als auch für Bedarfsplanungen. Weitere Informationen zur Planung, die Bedarfsplanungen berücksichtigt, finden Sie unter [Masterplanung mit Bedarfsplanungen](demand-forecast.md).
    - **Methode zur Reduzierung des Prognosebedarfs** - Wählen Sie die Methode, die zur Reduzierung des Prognosebedarfs während der Masterplanung verwendet werden soll.

        - *Keiner* – Planungsanforderungen werden während der Hauptplanung nicht reduziert.
        - *Prozent – Planzahlenverrechnungsschlüssel* – Die Planungsanforderungen werden verringert, und zwar gemäß den vom Planzahlenverrechnungsschlüssel definierten Prozentsätzen und Zeitperioden.
        - *Transaktionen – Planzahlenverrechnungsschlüssel* – Die Planungsanforderungen werden um die Transaktion reduziert, die während der im Planzahlenverrechnungsschlüssel definierten Zeitperioden stattfinden.
        - *Transaktion – dynamische Periode* – Die Planungsanforderungen werden durch die Auftragsbuchungen verringert, die während der dynamischen Periode stattfinden. Die dynamische Periode erstreckt sich über die aktuellen Planungsdaten und endet, wenn die nächste Planung beginnt. Die *Transaktionen – dynamischer Zeitraum* Methode verwendet oder erfordert keinen Planzahlenverrechnungsschlüssel, und wenn Sie sie verwenden, gelten die folgenden Bedingungen:

            - Wenn die Planung vollständig verringert wird, wird der Planungsbedarf für die aktuelle Planung 0 (null).
            - Wenn keine zukünftige Planung vorhanden ist, wird der Planungsbedarf der letzten eingegebenen Planung verringert.
            - Planungszeiträume sind in der Berechnung der Planungsverringerung enthalten.
            - Positive Tage sind in der Berechnung der Planungsverringerung enthalten.
            - Wenn die tatsächlichen Auftragsbuchungen größer sind als der geplante Bedarf, werden die verbleibenden Buchungen nicht in die nächste Planungsperiode vorgetragen.

        > [!NOTE]
        > Die Einstellung **Methode zur Reduzierung der Planungsanforderungen** gilt auch für Bedarfsplanungen, wenn Sie sie für den Hauptplan aktiviert haben, und wirkt sich auf ähnliche Weise aus. Weitere Informationen finden Sie unter [Produktprogrammplanung mit Bedarfsprognosen](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Legen Sie Reduzierungsoptionen für Abdeckungsgruppen fest

Führen Sie die folgenden Schritte aus, um Optionen festzulegen, die steuern, wie eine Abdeckungsgruppe ihre Planungsanforderungen für Hauptpläne reduziert, die eine transaktionsbasierte Reduzierung verwenden.

1. Gehen Sie zu **Produktprogrammplanung \> Einrichten \> Pläne \> Abdeckungsgruppen**.
1. Wählen Sie entweder eine bestehende Abdeckungsgruppe im Listenbereich, oder wählen Sie **Neu** im Aktivitätsbereich, um eine neue zu erstellen.
1. Legeb Sie im Inforegister **Sonstige** im Feld **Planungswert verringern um** fest, wie Beschaffungsplanungsanforderungen für Artikel in der Abdeckungsgruppe reduziert werden sollen, für Masterpläne, wo das Feld **Methode zur Reduzierung des Planungsbedarfs** auf *Buchungen - Planzahlenverrechnungsschlüssel* oder *Buchungen - dynamische Periode* eingestellt ist. Wählen Sie einen der folgenden Werte aus:

    - *Alle Transaktionen* - Alle Transaktionen sollen die Prognose reduzieren.
    - *Aufträge* - Nur Verkaufsaufträge vom selben Typ sollen die Prognose reduzieren.

    Beispielsweise geben die Standardbestelleinstellungen für einen Artikel an, dass er produziert werden sollte. Es gibt eine Beschaffungsplanungsposition für eine Menge von 50 und eine vorhandene Bestellung für eine Menge von 20. Wenn das Feld **Planungswert verringern um** auf *Aufträge* eingestellt ist, wird ein geplanter Fertigungsauftrag für eine Menge von 50 angelegt. Wenn es auf *Alle Transaktionen* eingestellt ist, wird der geplante Fertigungsauftrag auf eine Menge von 30 reduziert.

    Diese Einstellung gilt auch für die Reduzierung der Bedarfsplanung. Weitere Informationen finden Sie unter [Produktprogrammplanung mit Bedarfsprognosen](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Eine Beschaffungsplanung für ein Produkt eingeben

Gehen Sie folgendermaßen vor, um eine Beschaffungsplanung für ein Produkt einzugeben.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie das Produkt, für das Sie eine Prognose eingeben wollen.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Plan** die Option **Beschaffungsplanung**.
1. Wählen Sie auf der Seite **Beschaffungsplanung** im Aktivitätsbereich **Neu**, um dem Raster eine Prognose hinzuzufügen.
1. Geben Sie nach Bedarf Informationen in die neue Zeile ein, um Ihre Prognose zu spezifizieren.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Einen Artikel mit Beschaffungsplanungspositionen planen

Wenn Sie einen Hauptplan ausführen, der einen Artikel enthält, für den eine Beschaffungsplanung vorhanden ist, erstellt das System eine Bestellung für die eingegebenen Lieferpositionen. Standardbestelleinstellungen für den Artikel werden respektiert. Wenn diese Standardauftragseinstellungen einen **Standardauftragstyp** Wert von *Bestellung* festlegt, und kein Kreditorenkonto in der Beschaffungsplanungsposition angegeben ist, verwendet das System den Standardlieferanten für den Artikel.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Prüfen Sie, ob ein Planauftrag ein Beschaffungsplanungsauftrag ist

Verwenden Sie das folgende Verfahren, um zu erfahren, ob ein Bestellvorschlag als Ergebnis einer Beschaffungsplanung erstellt wurde.

1. Gehen Sie zu **Produktprogrammplanung \> Gesamtplanung \> Geplante Aufträge**.
1. Öffnen Sie den geplanten Auftrag, die Sie untersuchen möchten.
1. Sehen Sie auf dem Inforegister **Allgemein** den Wert des Feldes **Beschaffungsplanung** an. Wenn der Auftrag erstellt wurde, um eine Beschaffungsplanung abzudecken, wird dieses Feld auf *Ja* gesetzt.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Beispiele der Produktprogrammplanung mit Beschaffungsplanungen

Dieser Abschnitt enthält mehrere Beispiele, die zeigen, wie sich die Beschaffungsplanung auf die Hauptplanung auswirkt.

### <a name="example-1-supply-forecast-for-an-item"></a>Beispiel 1: Beschaffungsplanung für einen Artikel

Sie haben einen Artikel, dessen Standardbestelltyp *Bestellung* und der Standardanbieter *US-002* lautet. Es hat die folgende Beschaffungsplanungsposition.

| Modell    | Datum     | Kreditorenkonto | Kreditorengruppe | Menge | Einheit | Lager | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                |              | 35       | Stck   | 1    | 11        |

Wenn Sie die Produktprogrammplanung ausführen, wird eine geplante Einkaufsbestellung für *35 ea* vom Anbieter *US-002* erstellt.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Beispiel 2: Mehrere Beschaffungsplanungpositionen mit und ohne Lieferant

Sie haben einen Artikel, dessen Standardbestelltyp *Bestellung* und der Standardanbieter *US-002* lautet. Es hat die folgende Beschaffungsplanungspositionen.

| Modell    | Datum     | Kreditorenkonto | Kreditorengruppe | Menge | Einheit | Lager | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                |              | 35       | Stck   | 1    | 11        |
| CurrentF | 10.10.22 | US-101         |              | 25       | Stck   | 1    | 11        |

In diesem Fall behandelt das System die Zeile, die keinen Lieferanten angibt, als allgemeine Prognose und geht davon aus, dass die Zeile, die einen Lieferanten angibt, von der allgemeinen Prognose abgezogen werden sollte. Daher erstellt die Produktprogrammplanung die folgenden geplanten Einkaufsbestellungen für den Artikel:

- Eine geplante Einkaufsbestellung für eine Menge von *25 Stück* vom Anbieter *US-101* (Der Lieferant und die Menge, die in der Prognoseposition angegeben sind, werden verwendet.)
- Eine geplante Einkaufsbestellung für eine Menge von *10 Stück* vom Anbieter *US-002* (Da in der anderen Prognoseposition kein Lieferant angegeben wurde, wird der Standardlieferant verwendet und die Menge dieser Prognoseposition wird um die Menge der lieferantenspezifischen Prognoseposition reduziert.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Beispiel 3: Pläne, die die Methode „Transaktionen – dynamische Periodenreduktion“ in einer einzelnen Prognoseperiode verwenden

Für Masterpläne, die *Transaktionen – dynamischer Zeitraum* als Prognosereduktionsmethode verwenden, reduziert die Produktprogrammplanung die Prognosemengen, wenn es vorhandene Transaktionen gibt, die diesen Angebotsmerkmalen entsprechen.

Sie haben beispielsweise einen Artikel, dessen Standardbestelltyp *Bestellung* lautet. Es hat die folgende Beschaffungsplanungsposition.

| Modell    | Datum     | Kreditorenkonto | Kreditorengruppe | Menge | Einheit | Lager | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | Stck   | 1    | 11        |

Da es nur eine Beschaffungsplanungsposition gibt, gibt es nur einen Prognosezeitraum.

Wenn Sie einen Hauptplan ausführen, der für die Verwendung von *Transaktionen – dynamischer Zeitraum* als Reduktionsverfahren eingerichtet ist, kann eines der folgenden Ergebnisse auftreten:

- Wenn eine Bestellung für den Lieferanten *US-101* und eine Menge von *10 Stück* vorhanden ist, und das Feld **Beschaffungsplanung** auf *Ja* eingestellt ist, erstellt die Produktprogrammplanung eine neue geplante Bestellung für die Restmenge von *10 Stück*. Die Prognoseposition wird reduziert, da der Lieferant mit der vorhandenen Bestellung übereinstimmt.
- Wenn eine Bestellung für den Lieferanten *US-102*, Site *1*, Lagerort *11*, und eine Menge von *10 Stück* vorhanden ist, und das Feld **Beschaffunsplanung** auf *Ja* eingestellt ist, erstellt die Produktprogrammplanung eine neue geplante Bestellung für die Restmenge von *25 Stück*. Die Prognoseposition kann nicht reduziert werden, da sie einen anderen Lieferanten als die vorhandene Bestellung hat.

> [!NOTE]
> Diese Situation kann bei Bestellvorschlägen auftreten, da ihnen ein Lieferant zugeordnet ist. Bei Umlagerungsaufträgen und Fertigungsaufträgen werden die Beschaffungsplanungsbeträge jedoch immer um vorhandene Aufträge reduziert, da für diese Auftragstypen kein Lieferant angegeben ist.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Beispiel 4: Pläne, die die Methode „Transaktionen – dynamische Periodenreduktion“ über mehrere Prognoseperioden hinweg verwenden

Sie haben einen Artikel, dessen Standardbestelltyp *Bestellung* lautet. Es hat die folgende Beschaffungsplanungspositionen.

| Modell    | Datum     | Kreditorenkonto | Kreditorengruppe | Menge | Einheit | Lager | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | Stck   | 1    | 11        |
| CurrentF | 15.10.22 | US-101         |              | 25       | Stck   | 1    | 11        |

In diesem Beispiel gibt es zwei Prognosezeilen, die jeweils ein anderes Datum haben. Daher legen die Daten die Grenzen der Prognosezeiträume fest. Der erste Zeitraum ist vom 10. Oktober bis 14. Oktober 2022 (10.10.22–14.10.22). Die zweite ist ab dem 15. Oktober 2022 (15.10.22).

Es gibt eine bestehende Bestellung für den Lieferanten *US-101*, eine Menge von *10 Stück*, und das Datum *12.10.22* (12. Oktober 2022). Wenn Sie einen Hauptplan ausführen, der für die Verwendung von *Transaktionen – dynamischer Zeitraum* als Reduktionsverfahren eingerichtet ist, werden folgende Aufträge erstellt:

- Ein Auftragsvorschlag über eine Menge von *15 Stück* und das Datum *10.10.22* (Die Menge wird um die vorhandene Bestellung reduziert, die auf denselben Prognosezeitraum datiert ist.)
- Ein Auftragsvorschlag über eine Menge von *25 Stück* und das Datum *15.10.22* (Die Menge ist die volle Menge der Prognose.)

### <a name="example-5-plans-that-use-no-reduction"></a>Beispiel 5: Tarife ohne Ermäßigung

Wenn Sie einen Plan ausführen, bei dem die Prognosereduktionsmethode gilt *Keiner*, erstellt die Produktprogrammplanung immer geplante Lieferungen für alle Beschaffungsplanungspositionen. Nachdem diese geplante Lieferung genehmigt wurde, werden zukünftige Auftragsvorschläge reduziert. Bestellungen reduzieren jedoch nicht die Beschaffungsplanungspositionen.

Sie haben beispielsweise einen Artikel, dessen Standardbestelltyp *Bestellung* lautet. Es hat die folgende Beschaffungsplanungsposition.

| Modell    | Datum     | Kreditorenkonto | Kreditorengruppe | Menge | Einheit | Lager | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 | US-101         |              | 25       | Stck   | 1    | 11        |

Es gibt eine bestehende Bestellung für den Lieferanten *US-101*, Site *1*, Lagerort *11*, eine Menge von *25 Stück*, und das Datum *10.10.22*. 

Wenn Sie einen Hauptplan ausführen, der für die Verwendung von *Keiner* als Reduzierungsmethode eingerichtet ist, wird eine geplante Einkaufsbestellung für den Lieferanten *US-101*, Site *1*, Lagerort *11*, eine Menge von *25 Stück*, und das Datum *10.10.22* erstellt. Mit anderen Worten, die vorhandene Bestellung wird nicht reduziert, da dies bei der prognostizierten Reduzierungsmethode *Keine* der Fall ist.

Sie bearbeiten nun die geplante Einkaufsbestellung, die nach dem letzten Planungslauf angelegt wurde, und ändern die Menge auf *15 Stück*. Genehmigen Sie dann die Bestellung. Wenn Sie das nächste Mal einen Hauptplan ausführen, wird eine geplante Einkaufsbestellung für den Lieferanten *US-101*, Site *1*, Lagerort *11*, eine Menge von *10 Stück*, und das Datum *10.10.22* erstellt. Diesmal wird die Menge reduziert, um die Menge des vorhandenen genehmigten Auftrags aus dem vorherigen Planungslauf widerzuspiegeln.

## <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Unterschiede zwischen Planungsoptimierung und veraltetem Produktprogrammplanungsmodul

Beschaffungsplanungen funktionieren jedoch ein wenig anders, je nachdem, welches Produktprogrammplanungsmodul sie verwenden (Planungsoptimierung oder das veraltete Masterplanungsmodul). In diesem Abschnitt werden die Unterschiede beschrieben.

### <a name="vendor-groups"></a>Kreditorengruppen

Wenn Sie eine prognostizierte Position hinzufügen, können Sie einen Lieferanten und eine Lieferantengruppe angeben. In der veralteten Masterplanungs-Engine werden erstellte Auftragsvorschläge nach der Kombination der Lieferanten- und Lieferantengruppenwerte gruppiert. In der Planungsoptimierung werden Auftragsvorschläge nach Lieferanten gruppiert.

Die folgende Tabelle enthält einige Beispiele für Beschaffungsplanungspositionen für einen Artikel.

| Modell    | Datum     | Kreditorenkonto | Kreditorengruppe | Menge | Einheit | Lager | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10.10.22 |                | VendorGroupA | 5        | Stck   | 1    | 11        |
| CurrentF | 10.10.22 |                | VendorGroupA | 6        | Stck   | 1    | 11        |
| CurrentF | 10.10.22 |                |              | 7        | Stck   | 1    | 11        |

Lieferant *VendorA* ist der Standardlieferant für die Kreditorengruppe *VendorGroupA*. Dies ist auch der Standardlieferant für den Artikel.

Die veraltete Masterplanungs-Engine erstellt die folgenden Aufträge:

- Eine geplante Bestellung für den Lieferanten *VendorA*, Anbietergruppe *VendorGroupA*, und eine Menge von *11*
- Eine geplante Einkaufsbestellung für den Lieferanten *VendorA* und eine Menge von *7*

Die Planungsoptimierung erstellt nur einen Auftrag:

- Eine geplante Bestellung für den Lieferanten *VendorA*, Anbietergruppe *VendorGroupA*, und eine Menge von *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Reduktion allgemeiner Prognosen durch spezifischere Prognosen

In der veralteten Hauptplanungs-Engine ist das Ergebnis unvorhersehbar, wenn einige Prognosen einen Anbieter haben, andere jedoch nicht.

In der Planungsoptimierung werden allgemeine Prognosen immer durch spezifischere Prognosen reduziert, wie das folgende Beispiel zeigt.

Die folgende Tabelle enthält einige Beispiele für Beschaffungsplanungspositionen für einen Artikel.

| Datum       | Menge | Kreditor   | Kreditorengruppe  |
|------------|----------|----------|---------------|
| 11.02.2022 | 5.00     | Vendor-A | VendorGroup-A |
| 11.02.2022 | 6,00     | Vendor-A | VendorGroup-A |
| 11.02.2022 | 15.00    |          |               |

Die allgemeine Prognose (für 15,00 Stück) wird durch die spezifischeren Prognosen (für 5,00 + 6,00 = 11,00 Stück) reduziert. Der Rest wird dem Standardlieferanten zugeordnet. Die folgende Tabelle zeigt die Auftragsvorschläge.

| Datum       | Menge | Kreditor   | Kreditorengruppe  |
|------------|----------|----------|---------------|
| 11.02.2022 | 11.00    | Vendor-A | VendorGroup-A |
| 11.02.2022 | 4.00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Beachten Sie die Standardauftragseinstellungen, wenn Auftragsvorschläge generiert werden

Jeder Artikel kann Standardbestelleinstellungen haben, wie z. B. eine Mindestbestellmenge. Die veraltete Masterplanungs-Engine ignoriert diese Einstellungen und übersetzt daher Prognosen in Auftragsvorschläge mit derselben Menge. Die Planungsoptimierung berücksichtigt diese Einstellungen, wenn Planaufträge aus Lieferprognosen generiert werden. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Aggregation von Planaufträgen durch Reduzierung um genehmigte Aufträge

Die veraltete Hauptplanungs-Engine geht davon aus, dass nur eine Bestellung die bestehende Beschaffungsplanung reduziert. Wenn also mehrere Bestellungen mit einer Beschaffungsplanungsposition übereinstimmen, wird sie nur durch die erste Bestellung reduziert. In der Planungsoptimierung wird sie durch alle Aufträge, die mit der Beschaffungsplanungsposition übereinstimmen, reduziert.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Reduzierung der Prognose nur durch passende Anbieter

Wenn das veraltete Masterplanungs-Engine eine Prognose um vorhandene freigegebene Bestellungen reduziert, stellt es nicht sicher, dass der Lieferant auf der Bestellung mit dem Lieferanten aus der Prognose übereinstimmt. Die Planungsoptimierung reduziert Prognosen nur um Bestellungen, die einen übereinstimmenden Wert im Lieferantenfeld aufweisen.

Bei Umlagerungs- und Produktionsaufträgen wird das Lieferantenfeld immer ignoriert, da es für diese Auftragsarten nicht relevant ist.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Reduzierung der Prognosen durch Transportaufträge

Wenn die Standardbestellart für einen Artikel *Umlagerung* ist, können Prognosen nur durch vorhandene geplante Umlagerungsaufträge reduziert werden. Bei Fertigungsaufträgen und Bestellungen reduzieren jedoch nur freigegebene Aufträge die Beschaffungsplanung.

Das veraltete Masterplanungs-Engine reduziert für alle Umlagerungsauftragsstatus, während die Planungsoptimierung Prognosen nur um Umlagerungsaufträge reduziert, die sich im Status *Veröffentlicht* befinden.
