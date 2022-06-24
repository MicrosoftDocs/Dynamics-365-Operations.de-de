---
title: Gesamttransportkosten vs. Transportverwaltung
description: Microsoft Dynamics 365 Supply Chain Management bietet zwei verschiedene Module für die Arbeit mit dem Transportwesen, Transportverwaltung (TMS) und Gesamttransportkosten. Dieser Artikel fasst die Funktionalität zusammen, die die beiden Module allgemein haben und hebt die Unterschiede zwischen ihnen hervor.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 40489ff8d8683d19a5f726546cc4c43cc3e7a05d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905920"
---
# <a name="landed-cost-vs-transportation-management"></a>Gesamttransportkosten vs. Transportverwaltung

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management stellt zwei verschiedene Module für die Arbeit mit dem Transportwesen zur Verfügung: **Transportverwaltung** (TMS) und **Gesamttransportkosten**. Dieser Artikel fasst die Funktionalität zusammen, die die beiden Module allgemein haben und hebt die Unterschiede zwischen ihnen hervor. Sie können diese Informationen nutzen, um zu entscheiden, welches Modul am besten zu Ihren Geschäftspraktiken passt. Vielleicht stellen Sie fest, dass einige Geschäftspraktiken besser mit TMS funktionieren, während andere am besten mit Gesamttransportkosten funktionieren. Je nach Ihren Geschäftsanforderungen können Sie sich dann für die ausschließliche Verwendung eines Moduls entscheiden, oder Sie können die beiden Module kombinieren.

Dieser Artikel ist keine umfassende Übersicht über alle Funktionen der beiden Module. Stattdessen werden die verfügbaren Funktionen hervorgehoben, die sich auf den Transport von Waren von einem Lieferanten zum Lagerort Ihres Unternehmens beziehen, wo sie verbraucht werden können.

## <a name="terminology-reference-data-and-reporting-differences"></a>Unterschiede in der Terminologie, den Referenzdaten und der Berichterstellung

### <a name="terminology-comparison"></a>Terminologie-Vergleich

TMS und Gesamttransportkosten verwenden unterschiedliche Begriffe für ähnliche Konzepte. Die folgende Tabelle fasst diese Begriffe und ihre Verwendung in den beiden Modulen zusammen.

| TMS-Begriff | Gesamttransportkosten-Begriff | Notizen |
|----------|------------------|-------|
| **Einlesen**<p>Eine *Ladung* ist eine Sammlung von Sendungen, die gleichzeitig auf derselben Transporteinheit (z. B. einem LKW oder einem Schiff) transportiert werden. Ladungen können entweder eingehend oder ausgehend sein.</p> | **Seereise**<p>Typischerweise ist eine *Fahrt* ein einzelnes Schiff, das auf einer einzigen *Route* fährt. Eine Fahrt kann mehrere *Transportcontainer* enthalten, und sie kann auch eingehende Aufträge von verschiedenen juristischen Entitäten Ihrer Organisation enthalten. Fahrten können nur eingehend sein.</p> | TMS verwendet auch den Begriff *Fahrtnummer*, der sich auf ein Informationsfeld bezieht, in das Sie eine Kennung eingeben können. Mit dem TMS-Feld ist jedoch keine Funktionalität verbunden, und es hat nichts mit dem Konzept der *Reise* in den Gesamttransportkosten zu tun. |
| **Route**<p>Eine *Route* ist der physische Weg eines Transports vom Ursprung zum Ziel.</p> | **Reise**<p>Eine *Reise* ist der physische Weg eines Transports vom Ursprung zum Ziel. Jede Fahrt muss einer Route zugeordnet werden.</p> | |
| **Routen-Segmente**<p>Eine Route kann mehrere *Routensegmente* haben, von denen jedes einen Schritt der Route darstellt. Eine Route kann mehrere Spediteure oder Dienste enthalten, von denen jeder als ein Routensegment betrachtet wird.</p> | **Teilstrecken**<p>Jede Fahrt kann mehrere *Abschnitte* haben, von denen jeder einen Abschnitt der Route darstellt. Ein Abschnitt kann Teil des Transports, der Zollabfertigung oder einer anderen Aktivität sein.</p> | |
| **Container**<p>Ein *Container* kann jede Art von Paket oder Verpackung sein, die von TMS verwendet wird.</p> | **Versandcontainer**<p>Ein *Schiffscontainer* ist ein buchstäblicher, physischer Transportcontainer, wie er von Containerschiffen bekannt ist.</p> | |
| **Warencodes**<p>In TMS (und an anderen Stellen im Supply Chain Management) identifizieren *Warencodes* die Arten von Waren. Sie können Zollsätze, die Handhabung von Gefahrgut usw. beeinflussen.</p> | **Warencodes**<p>In Gesamttransportkosten werden *Warencodes* auf der Ebene der juristischen Entität festgelegt. Sie werden meist für das Berichtswesen verwendet.</p> | Gesamttransportkosten können auch die Warencodes verwenden, die für TMS und andere Stellen im Supply Chain Management verwendet werden. Die Warencodes von Gesamttransportkosten werden jedoch nur von Gesamttransportkosten verwendet. |

### <a name="some-reference-data-isnt-shared"></a>Einige Referenzdaten werden nicht gemeinsam genutzt

TMS und Gesamttransportkosten teilen sich keine Referenzdaten für Entitäten wie Kalkulationen, Routen und Abschnitte. Wenn Sie beide Module verwenden, müssen Sie die nicht gemeinsam genutzten Referenzdaten neu erstellen.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Intercompany-Berichte funktionieren nicht mit Waren in Zustellung

Die folgenden Berichte funktionieren nicht in Verbindung mit der Funktion Waren in Zustellung, die Gesamttransportkosten bereitstellt:

- [Intercompany-Bericht Waren in Zustellung gesamt](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Intercompany-Bericht Waren in Zustellung gesamt](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Diese Berichte gehen davon aus, dass Waren in Transit eingelagert werden, sobald Sie einen Lieferschein ausstellen, und dass sie bei Erhalt aus dem Transit in den Bestand übernommen werden. Waren in Zustellung werden jedoch nicht auf diese Weise verarbeitet. Wenn Sie also die Funktionen für Waren in Zustellung und Intercompany zusammen verwenden, sind die Ergebnisse für diese beiden Berichte falsch.

## <a name="using-the-two-modules-together"></a>Gemeinsame Verwendung der beiden Module

Sie können TMS sowohl für eingehende als auch für ausgehende Vorgänge verwenden. Obwohl Gesamttransportkosten die meisten der grundlegenden Funktionen von TMS für eingehende Vorgänge bietet, fügt es auch einige Funktionen hinzu. Daher sollten Sie in Betracht ziehen, TMS für ausgehende Vorgänge und Gesamttransportkosten für eingehende Vorgänge zu verwenden.

Allgemein empfehlen wir Ihnen nicht, beide Module zusammen für eingehende Vorgänge zu verwenden. Sie sollten das Modul verwenden, das Ihre Anforderungen am besten erfüllt. Wenn Sie die beiden Module zusammen verwenden, dürfen Sie keine Quelldokumente zwischen ihnen austauschen. Verwenden Sie zum Beispiel nicht dieselbe Einkaufsbestellung für eine Ladung in TMS und eine Fahrt in Gesamttransportkosten. Insbesondere müssen Sie sicherstellen, dass Sie das System nicht so festlegen, dass eingehende Ladungen automatisch erstellt werden. Wenn Artikel aus Einkaufsbestellungen in einer Fahrt enthalten sind, können sie nicht als Teil einer Ladung behandelt werden.

## <a name="goods-in-transit"></a>Waren in Zustellung

Eine der wichtigsten Funktionen von Gesamttransportkosten ist die Möglichkeit, Waren in Zustellung zu verarbeiten. Mit der Bearbeitung von Waren in Zustellung können Sie das finanzielle Eigentum an versendeten Artikeln übernehmen, bevor diese physisch im Lagerort am Zielort eintreffen. Die Bearbeitung von Waren in Zustellung ist häufig für den internationalen Handel erforderlich.

### <a name="tms-goods-in-transit-features"></a>Funktionen von TMS Waren in Zustellung

TMS unterstützt derzeit keine Waren in Zustellung.

### <a name="landed-cost-goods-in-transit-features"></a>Funktionen für kalkulierte Waren in Zustellung

Die Bearbeitung von Waren im Transit ist eine primäre Funktion von Gesamttransportkosten und bietet die folgenden Funktionen:

- **Waren in Transitlagern** - Jedem Lagerort in Supply Chain Management kann ein Waren in Transitlager zugeordnet werden. Waren werden nach der Fakturierung der ursprünglichen Einkaufsbestellung in Lagerorte in Zustellung gebracht. Artikel, die dort physisch reserviert sind, sind für den Verbrauch nicht verfügbar, bis sie an ihrem physischen Lagerort eintreffen. Daher können Sie durch die Fakturierung der Einkaufsbestellung das finanzielle Eigentum an Waren übernehmen.
- **Gesamttransportkosten-Hauptbuchkonto** - Kalkulierte Kosten fügt dem Buchungsprofil für den Kauf ein spezielles Hauptbuch-Buchungskonto hinzu, um die Bearbeitung von Waren in Zustellung zu handhaben. Dieses Hauptbuchkonto für Waren im Transit fungiert als ein Konto des Typs „Waren in Rechnung gestellt, aber nicht erhalten“. Wenn die ursprüngliche Bestellung fakturiert und die Bestellung von Waren in Zustellung erstellt wird, werden die direkten Bestellkosten auf das Hauptbuchkonto für Waren in Zustellung gebucht, bis die Waren an ihrem endgültigen physischen Lagerplatz eingegangen sind.
- **Aktualisierung der Tracking-Kontrolle** - Waren in Transitbestellungen unterstützen die Funktionalität der Tracking-Kontrolle in den Gesamttransportkosten. Mit Tracking Control können Sie das erwartete Ankunftsdatum von Waren aktualisieren, während sie sich in Zustellung befinden. Tracking Control aktualisiert dann die Fahrt und die zugehörigen Zeilen der Einkaufsbestellung. Das erwartete Lieferdatum steht dann für die Produktprogrammplanung und die Logistik zur Verfügung.
- **Auslösen von Über-/Unter-Transaktionen** - Wenn eine Abweichung zwischen den erwarteten Waren auf einer Zeile der Fahrt und den tatsächlich am Lagerort eingetroffenen Waren auftritt, lösen die Gesamttransportkosten diese durch das Erstellen von Über- und/oder Unter-Transaktionen auf. Sie können diese Transaktionen dann, je nachdem, wie Sie sie verarbeiten wollen, entweder über eine Einkaufsbestellung oder eine Erfassung verwalten. Die Über- und Untertransaktionen stellen eine Verbindung zurück zur Fahrt, zur ursprünglichen Erfassung und zum neuen Umlagerungserfassung oder zur Einkaufsbestellung für die Abweichung her.
- **Gesamttransportkosten** - Gesamttransportkosten führt ein neues Quelldokument ein, das als *Gesamttransportkosten* bezeichnet wird. Mit einer Waren in Zustellung können Sie die ursprüngliche Einkaufsbestellung in Rechnung stellen, um das finanzielle Eigentum an den Artikeln zu übernehmen. Wenn die Bestellung fakturiert wird, wird das neue Quelldokument für jede Zeile der Einkaufsbestellung erstellt, die eine Kombination von Bestandsdimensionen aufweist. Die Waren werden dann physisch in ein Lagerort für Waren in Zustellung gebracht, wo sie physisch gegen die Bestellung in Zustellung reserviert werden und nicht verbraucht werden können, solange keine Bestellungen in Zustellung eingehen.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Verschiedene Gebühren und Versandkosten

Einer der wichtigsten Aspekte der Versand- und Sendungsverwaltung für Waren ist die Erfassung der Gemeinkosten, die mit den Sendungen verbunden sind. Diese Gemeinkosten sind nicht die direkten Bestandskosten, die mit einer Einkaufsbestellung und einer Lieferung oder Fahrt verbunden sind. Stattdessen handelt es sich um zusätzliche Kosten, die durch die Art der Bewegung der Waren vom Lieferanten zu Ihrem Unternehmen verursacht werden. Diese Kosten können Frachtkosten umfassen, die mit dem Versand von Waren von einem Lagerplatz zu einem anderen verbunden sind, oder Zollkosten, die mit dem Import von Waren von einem ausländischen Lieferanten verbunden sind.

Gesamttransportkosten kalkuliert diese Kosten, indem es eine neue Art von Kostenstruktur erstellt, die als *Autokalkulation* bekannt ist. TMS behandelt diese Kosten, indem es die Funktionalität der sonstigen Kosten verwendet.

### <a name="tms-charge-and-cost-features"></a>Funktionen von TMS für Gebühren und Kalkulationen

TMS verwendet diverse Gebühren, um zusätzliche Kosten für Ladungen zu verwalten, die den zugehörigen Quellbelegzeilen zugeordnet sind. Diese Zusatzkosten können entweder auf der Ebene der Zeile der Bestellung oder des Kopfes der Einkaufsbestellung festgelegt werden.

In TMS können die sonstigen Kosten nach Gewicht, Volumen oder Menge des Bestands aufgeteilt werden. Die Gebühren können durch Fracht- oder Nebenkosten aufgeteilt werden. Für die Verwendung zusätzlicher Aufteilungsmethoden in TMS ist eine weitere Entwicklung erforderlich.

### <a name="landed-cost-charge-and-cost-features"></a>Kalkulierte Kosten und Funktionen für die Kalkulation

Die kalkulierten Gesamttransportkosten stellen eine Reihe von Kostenfunktionen bereit, die zusätzliche Kosten behandeln, die mit dem Versand von Waren verbunden sind. Diese Kosten werden als Autokalkulation bezeichnet und werden zum Zeitpunkt der ersten Rechnungsstellung für den Versand unter Verwendung des geschätzten Kostenbetrags angewendet. Jede Kostenart wird in einer eigenen Buchung verwaltet. Nachdem die tatsächlichen Rechnungen für Gemeinkosten gebucht wurden, werden die geschätzten Kosten automatisch aktualisiert, um die tatsächlichen Kosten widerzuspiegeln.

Zusätzlich können die Gemeinkosten, die mit der Verschiffung der Waren verbunden sind, während der Fahrt vom Hafen aus oder zu einem beliebigen Zeitpunkt nach Erhalt der Waren in Rechnung gestellt werden. Diese Funktionalität bietet eine größere Flexibilität für den Verbrauch von Waren.

Die folgende Liste umreißt einige Konzepte für die Funktionen für Gebühren und Kosten in Gesamttransportkosten:

- **Kostenbereich** - Kosten und Gebühren können auf einer Fahrt verschiedenen Ebenen oder *Kostenbereichen* zugewiesen werden. Die Kosten können auf der Ebene der Fahrt angewendet und auf jeden Artikel der Fahrt heruntergebrochen werden. Zusätzlich können die Kalkulationen auf der Ebene des Containers, der Einkaufsbestellung, des Artikels oder des Umlagerungsauftrags angewandt werden. Jede Kalkulation kann separat über die verschiedenen Bereiche verwaltet werden und wird auf die Kosten pro Artikel heruntergebrochen.
- **Aufteilungsmethoden** - In Gesamttransportkosten stehen mehrere Aufteilungsmethoden zur Verfügung. Kalkulationen können nach Menge, Dollarbetrag, Wert, Gewicht, Volumen, Messung oder einer benutzerdefinierten volumetrischen Kennzahl umgelegt werden.
- **Abrechnung/Abweichungskontrolle** - Kosten werden in den Gesamttransportkosten als eigene Kostenart festgelegt. Für jede Kostencodeart können Sie ein Verrechnungskonto für die Kosten der geschätzten Kosten sowie Abgrenzungs- und Kaufpreisabweichungskonten für Abweichungen der geschätzten Kosten von den tatsächlichen Kosten definieren. Bei der ersten Buchung der geschätzten Kosten erfolgt eine Gutschrift auf dem Verrechnungskonto. Nach der Buchung der tatsächlichen Rechnungen werden die tatsächlichen Kostenbelastungen gebucht, und die geschätzten Kosten werden vom Verrechnungskonto abgebucht.

## <a name="matching-freight-bills-and-invoices"></a>Abgleich von Frachtbriefen und Rechnungen

### <a name="tms-bill-and-invoice-matching-features"></a>Funktionen für den Abgleich von Rechnungen und Rechnungen in TMS

TMS kann Frachtrechnungen, die geschätzte Kosten enthalten, und Rechnungen mit den tatsächlichen Kosten der Fracht abgleichen. Rechnungen können entweder elektronisch oder in Papierform empfangen werden. Die Abweichung zwischen den geschätzten Kosten und den tatsächlichen Kosten hat keinen Einfluss auf die Bewertung des Bestands.

Weitere Informationen finden Sie unter [Fracht in der Transportverwaltung abgleichen](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Funktionen für den Abgleich von kalkulierten Kosten und Rechnungen

Gesamttransportkosten können Frachtrechnungen mit geschätzten Kalkulationen abgleichen und die tatsächlichen Kalkulationen mit den geschätzten Kosten in Rechnung stellen. Zum Zeitpunkt der Rechnungsstellung befinden sich die Frachtkosten in einer Erfassung, und die geschätzten Kosten werden aus dem Verrechnungskonto ausgebucht. Zusätzlich werden die tatsächlichen Kostenbelastungen gegen die Selbstkosten des Artikels gebucht, zusammen mit den Abweichungen zwischen den geschätzten Kosten und den tatsächlichen Kosten. Dieses Verhalten ermöglicht Flexibilität bei der Rechnungsstellung.

## <a name="tracking"></a>Nachverfolgung

Eine wichtige Funktion sowohl von TMS als auch von Gesamttransportkosten ist die Möglichkeit, Waren zu verfolgen und festzustellen, wo sie sich auf der Route vom Ursprungsort bis zum endgültigen Lagerort befinden. Mit der Nachverfolgung können Sie verfolgen und aktualisieren, wo sich die Waren befinden und wann sie voraussichtlich am Lagerort zum Verbrauch eintreffen werden. Zusätzlich zum Status der Waren während ihrer Route liefern die Gesamttransportkosten erwartete und tatsächliche Daten für jeden Schritt der Route.

### <a name="tms-tracking-features"></a>TMS-Funktionen zur Verfolgung

TMS bietet begrenzte Funktionen zur Verfolgung eingehender Ladungen. Es zeigt Daten an und ermöglicht eine Integration, um die genaue Position zu finden (zum Beispiel auf der Seite **Transportstatus**).

Für jedes Routensegment können Sie geschätzte Fahrpläne und Ankunftszeiten eingeben.

### <a name="landed-cost-tracking-features"></a>Funktionen zur Verfolgung der Gesamttransportkosten

Die kalkulierten Gesamttransportkosten bieten eine Tracking-Kontrolle für jede Fahrt, vom An Hafen bis zum endgültigen Ziel. Die Verfolgungskontrolle legt den Status der Fahrt fest. Der Status gibt an, ob sich die Fahrt in Fahrt, im Zoll zur Kontrolle oder in lokaler Auslieferung auf dem Weg zum endgültigen Lagerort befindet. Der Status kann auf der Ebene der Zeile der Einkaufsbestellung, des Containers und des Kopfes der Fahrt festgelegt werden. Somit haben Sie eine granularere Kontrolle.

Zusätzlich wird jedem Schritt einer Route ein bestätigtes erwartetes Datum zugeordnet, das auf festgelegten Vorlaufzeiten basiert. Die bestätigten und erwarteten Liefertermine werden der Zeile der Einkaufsbestellung und der Waren in Zustellung hinzugefügt und können für die Produktprogrammplanung und Logistik verwendet werden. Zusätzlich zu den erwarteten Terminen können auch die tatsächlichen Termine aktualisiert werden. Die nachfolgenden Schritte einer Route werden dann entsprechend aktualisiert.

## <a name="multi-leg-journeys"></a>Reisen mit mehreren Teilstrecken

Das Routenkonzept identifiziert, wo sich die Waren im Prozess befinden und steuert den Status der Waren, während sie sich in Zustellung befinden. Waren können mehrere Abschnitte einer Route durchlaufen, und Sie können einem bestimmten Abschnitt verschiedene Kosten zuordnen. Beispiele sind die Frachtkosten für die Fahrt eines Schiffes und die lokalen Transportkosten für den Transport der Waren vom Hafen zum Zielort.

### <a name="tms-multi-leg-journey-features"></a>TMS-Funktionen für Routen mit mehreren Abschnitten

In TMS können Routen in Routensegmente unterteilt werden, um Routen mit mehreren Abschnitten darzustellen. TMS kann den einzelnen Routensegmenten Spot-Sätze und Nebenkosten zuordnen.

Weitere Informationen finden Sie unter [Planen von Güterverkehrsrouten mit mehreren Stopps](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Funktionen für kalkulierte Gesamttransportkosten bei Routen mit mehreren Abschnitten

Kalkulierte Gesamttransportkosten bieten einen Rahmen für die Beförderung von Waren vom Ausgangspunkt zum Zielort durch eine Reihe von Abschnitten, d.h. die Stopps oder Schritte einer Route. Die Abschnitte werden kombiniert, um Routenvorlagen zu erstellen, die definieren, wie Waren vom Lieferanten zu Ihrem Unternehmen gelangen.

In jedem Abschnitt einer Route können Sie außerdem den Status jeder Zeile der Einkaufsbestellung und die damit verbundenen Vorlaufzeiten definieren. Die kombinierte Vorlaufzeit für alle Abschnitte wird verwendet, um das voraussichtliche Lieferdatum zu ermitteln. Für die Anwendung von Routen mit mehreren Abschnitten ist jedoch die Verarbeitung von Waren in Zustellung erforderlich. Die Route der Waren auf einer Fahrt wird in einer Tabelle verwaltet, die spezifisch für die Gesamttransportkosten ist.

## <a name="receiving-by-container"></a>Wareneingang nach Container

Es kann wichtig sein, zu verwalten, wie Waren auf einem Schiff aufgeteilt und gelagert werden. Auf einem Schiff können Waren in einem Container oder in mehreren Containern gelagert werden. Wenn Waren empfangen werden, werden sie in Containern empfangen, und verschiedene Container auf einer Fahrt können zu verschiedenen Zeiten oder an verschiedenen Daten empfangen werden.

Sowohl TMS als auch Gesamttransportkosten bieten Funktionen für die Verwaltung des Eingangs von Waren in einem Container. TMS verwendet das Konzept der Ladungen, um die Waren, Kaufsbestellungen und Umlagerungsaufträge zu verwalten, die mit einem Transportcontainer verbunden sind. TMS unterstützt den Wareneingang auf der Basis einer Verpackungsstruktur, die durch eine Vorabliefernotiz (ASN) empfangen wird. Gesamttransportkosten kalkuliert das Konzept der Transportcontainer, um Einkaufsbestellungen zu verarbeiten und Gemeinkosten zu kontrollieren, die mit einem Container auf einem Schiff verbunden sind.

### <a name="tms-receiving-by-container-features"></a>Funktionen des TMS-Empfangs nach Containern

TMS unterstützt eingehende ASNs, alle Varianten des Wareneingangs über die Warehouse Management Mobile App und alle Methoden des Wareneingangs über den Supply Chain Management Client.

### <a name="landed-cost-receiving-by-container-features"></a>Funktionen für kalkulierte Gesamttransportkosten beim Containereingang

Zur Unterstützung des Wareneingangs nach Containern erstellt Gesamttransportkosten Transportcontainer-Datensätze und verknüpft Kaufsbestellungen mit einem bestimmten Transportcontainer unter Verwendung seiner Container-ID. Gemeinkosten können dann auf diesen Transportcontainer angewendet und aufgeschlüsselt werden, so dass sie mit den entsprechenden Einkaufsbestellungen verknüpft werden.

Container in kalkulierten Gesamttransportkosten können über eine neue Art von Quittung, die als *Wareneingangserfassung* bezeichnet wird, über Wareneingangserfassungen oder über den Empfang mit mobilen Geräten empfangen werden. Wenn Wareneingangserfassungen verwendet werden, können die Mengen aus den Zeilen der Waren in Zustellung oder der ursprünglichen Einkaufsbestellung im Behälter initialisiert werden. Gesamttransportkosten bietet zwei Arbeitstypen für den Wareneingang über die Warehouse Management Mobile App.

Kalkulierte Gesamttransportkosten bieten keinen Lieferavis für den elektronischen Empfang von Waren. Außerdem werden keine Warehouse Management Mobile App-Flows unterstützt, die Ladungsträger-, Ladungsträger- oder gemischten Ladungsträger-Eingang verarbeiten.

## <a name="rate-shopping-by-vendor"></a>Bewertung von Sätzen nach Lieferanten

Rate Shopping ermöglicht es einer Firma, einen Transportanbieter auf der Basis des niedrigsten Preises, der schnellsten Route oder einer Kombination aus beiden Überlegungen auszuwählen.

### <a name="tms-rate-shopping-features"></a>Funktionen von TMS Rate Shopping

Mit TMS können Sie Lieferanten und Routenlösungen für eingehende und ausgehende Aufträge identifizieren. So können Sie beispielsweise die schnellste Route oder den günstigsten Satz für eine Lieferung identifizieren.

TMS bietet vollständiges Rate Shopping und Frachtoptimierung über die Route Workbench, flexible Bewertungsoptionen über die Rating Engine, eine Rating Engine API für die Integration mit externen Parteien und Unterstützung für volumetrisches Gewicht.

Weitere Informationen finden Sie unter [Transportverwaltungs-Engines](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Funktionen für die Kalkulation von Gesamttransportkosten

Kalkulierte Gesamttransportkosten bieten nur begrenzte Unterstützung für das Einkaufen von Sätzen nach Anbieter. Sie können zwar Spediteurwerte eingeben, aber Gesamttransportkosten vergleicht diese nicht über mehrere Anbieter hinweg.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Einchecken/Auschecken von Fahrern mit Terminplanung

Die Funktionen zum Ein- und Auschecken von Fahrern ermöglichen es dem System, Ankünfte zu überwachen und Staus an den Ladedocks zu vermeiden.

### <a name="tms-driver-check-incheck-out-features"></a>TMS-Funktionen zum Ein- und Auschecken von Fahrern

Mit TMS können Sie *Termine* erstellen. Ein Termin stellt Ereignisse dar, die an einem Dock für den Empfang einer Kaufsbestellung, den Versand eines Auftrags oder die Bearbeitung einer eingehenden oder ausgehenden Ladung an einem bestimmten Datum und zu einer bestimmten Zeit stattfinden. Termine stellen sicher, dass Docks zum Be- und Entladen von Waren verfügbar sind, und sie helfen zu verhindern, dass mehrere Spediteure gleichzeitig an einem Lagerplatz eintreffen.

Das System unterstützt das Einchecken von Fahrern an einem bestimmten Dock-Tor.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Funktionen für das Ein- und Auschecken von Fahrern mit kalkulierten Kosten

Kalkulierte Gesamttransportkosten können Schätzungen für das Datum und die Uhrzeit, zu der ein Container geliefert wird, speichern.

## <a name="transfer-orders-and-additional-costs"></a>Umlagerungsaufträge und zusätzliche Kosten

Oft müssen Unternehmen in der Lage sein, Waren zwischen Lagerorten zu transferieren. Wenn diese Art des Transfers stattfindet, sind damit Kosten verbunden, die Sie eventuell ausweisen möchten. Bei kalkulierten Gesamttransportkosten können Umlagerungsaufträge zu einer Fahrt oder einem Schiff hinzugefügt werden, um die Bewegung von Waren von einem Lagerort oder Standort zu einem anderen zu verfolgen, die Lieferzeit und das voraussichtliche Lieferdatum abzuschätzen und die Gemeinkosten für die Umlagerung von Waren hinzuzufügen.

### <a name="tms-transfer-order-cost-features"></a>Funktionen für die Kalkulation von TMS-Umlagerungsaufträgen

TMS unterstützt die Erstellung von Frachtkosten, die mit Transfers verbunden sind. Obwohl diese Gebühren im Umlagerungsauftrag angezeigt werden können, werden die Gesamttransportkosten nicht zu den Kosten des Artikels hinzugefügt. Der Frachtabgleich wird durch die Erstellung einer Frachtrechnung unterstützt, die auf diesen Gebühren basiert. Diese Frachtrechnung wird dann mit einer Lieferantenfrachtrechnung abgeglichen.

### <a name="landed-cost-transfer-order-cost-features"></a>Funktionen für kalkulierte Gesamttransportkosten für Umlagerungsaufträge

Mit Gesamttransportkosten können Sie Umlagerungsaufträge zu einem Schiff oder einer Fahrt hinzufügen. Auf diese Weise können Sie der Fahrt Frachtkosten als Kalkulationen zum Zeitpunkt des Eingangs des Umlagerungsauftrags hinzufügen. Die Gemeinkosten können für die tatsächlichen Kosten in Rechnung gestellt werden und gegen eine Fahrt verfolgt werden, um die Kosten der verkauften Waren zu aktualisieren. Obwohl Umlagerungsaufträge in der Standardversion nicht die Verarbeitung von Waren in Zustellung verwenden, können sie zu Fahrten hinzugefügt werden. Die Gesamttransportkosten werden zu den Gesamtkosten der einzelnen Artikel addiert.