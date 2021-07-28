---
title: Modul Gesamttransportkosten
description: Das Modul für kalkulierte Gesamttransportkosten unterstützt Unternehmen bei der Rationalisierung eingehender Versandvorgänge, indem es dem Benutzer die vollständige finanzielle und logistische Kontrolle über importierte Fracht vom Hersteller bis zum Lagerort ermöglicht.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e646b5fed29aa4c6e67a83703a51c4a322a1918b
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338422"
---
# <a name="landed-cost-module"></a>Modul Gesamttransportkosten

[!include [banner](../../includes/banner.md)]

Das Modul **Gesamttransportkosten** hilft Unternehmen, eingehende Versandvorgänge zu rationalisieren, indem es Anwendern die vollständige finanzielle und logistische Kontrolle über importierte Fracht vom Hersteller bis zum Lagerort ermöglicht. Bei importierten Waren können die Gesamttransportkostens 40 Prozent oder mehr der Gesamtkalkulation eines jeden importierten Artikels ausmachen. Daher besteht die Herausforderung darin, genaue Schätzungen für die landed costs zu erstellen.

Unternehmen können Gesamttransportkosten verwenden, um die folgenden Aufgaben zu erledigen:

- Kalkulation der landed costs zum Zeitpunkt der Erstellung der Fahrt.
- Aufteilung der Wareneinstandspreise auf mehrere Artikel und Einkaufsbestellungen oder Umlagerungsaufträge in einer einzigen Fahrt.
- Unterstützen Sie den Transfer von Waren zwischen physischen Lagerplätzen durch Erkennen von gelandeten Kosten.
- Erfassen Sie Abgrenzungen für Waren in Zustellung.

Gesamttransportkosten liefert genaue und zeitnahe Kalkulationen für die Gemeinkosten der Waren. Gleichzeitig sorgt es für mehr finanzielle und logistische Transparenz in der erweiterten Lieferkette. Es hilft auch, die Verwaltung der Kalkulation und Kalkulationsfehler zu reduzieren.

## <a name="highlights"></a>Hervorhebungen

### <a name="voyages"></a>Seereisen

Bei den kalkulierten Gesamttransportkosten ist eine Fahrt eine eindeutige Bewegung von einem ausgehenden Lagerplatz über eine festgelegte Anzahl von Zielen in einem festgelegten Zeitraum zu einem bestimmten eingehenden Lagerplatz. Kaufbestellungen und Auftragszeilen können entweder einem einzelnen Container oder mehreren Containern für eine Fahrt hinzugefügt werden, und die Kosten werden korrekt auf die Artikelzeile zurückgerechnet. Bestellungen und Bestellzeilen können auch über juristische Entitäten hinweg für eine einzelne Fahrt hinzugefügt werden.

### <a name="item-ownership"></a>Eigentum an Artikeln

In Microsoft Dynamics 365 Supply Chain Management werden die Waren normalerweise am Lagerort empfangen und dann in Rechnung gestellt. Unter den meisten internationalen Handelsvereinbarungen übernimmt ein Unternehmen jedoch das Eigentum an den Waren ab dem Zeitpunkt, an dem sie den ursprünglichen Hafen verlassen, bevor sie physisch empfangen wurden. Gesamttransportkosten ermöglichen es Unternehmen, Waren zu fakturieren, bevor sie physisch empfangen wurden. Dieses Konzept wird als Waren in Zustellung bezeichnet. Es erstellt eine neue Art von Auftrag, um den Empfang von Waren zu verwalten, nachdem die ursprüngliche Einkaufsbestellung in Rechnung gestellt wurde.

### <a name="costs"></a>Kosten

Wenn Sie eine Fahrt in Gesamttransportkosten erstellen, können ihr automatisch Kosten hinzugefügt werden. Diese Kosten werden in Gesamttransportkosten festgelegt, und für sie stehen verschiedene Kostenoptionen und Kostengrundlagen zur Verfügung. Jede Kostenart kann für verschiedene Ebenen einer Fahrt festgelegt und über Umlageregeln, die Menge, Volumen, Gewicht, Betrag und definierte volumetrische Divisoren unterstützen, auf die Artikelebene umgelegt werden. Diese geschätzten Kosten liefern eine genaue Schätzung aller Kosten für eine Fahrt.

Die kalkulierten Gesamttransportkosten führen dann eine vorläufige Buchung/Abgrenzung der geschätzten gelandeten Kosten durch, um sicherzustellen, dass eine genaue Kalkulation der geschätzten Kosten zum Zeitpunkt der Erstellung der Fahrt bereitgestellt wird. Wenn diese automatischen Kosten in Rechnung gestellt werden, werden die geschätzten Kosten storniert und durch die tatsächlichen Kosten ersetzt, basierend auf den Kostenrechnungen.

Tatsächliche Kosten sind umgekehrte geschätzte Kosten, die zum Zeitpunkt der Kalkulation gebucht werden, indem Verrechnungskonten verwendet werden, die für jede Kostenart festgelegt werden (z.B. Zoll, Fracht und Versicherung). Diese Buchungen folgen dem Buchungsverhalten, das mit dem jeweiligen Artikel verbunden ist. Sie aktualisieren automatisch die Bestandsbuchung, unabhängig davon, ob die Buchungsart First in, First out (FIFO), Last in, First out (LIFO), gleitender gewichteter Durchschnitt oder gleitender Durchschnitt ist. Es werden alle Buchungsarten für Bestandsmodellgruppen unterstützt. Für Buchungen mit gleitendem Durchschnitt und Standardkosten stehen Einkaufspreisabweichungskonten zur Verfügung, um die Differenzen zwischen geschätzten Kosten und tatsächlichen Kosten zu buchen.

### <a name="item-and-order-tracking"></a>Artikel- und Auftragsverfolgung

Während sich eine Fahrt vom ausgehenden Lagerplatz zum endgültigen Ziellagerort bewegt, können Benutzer jeden Abschnitt oder *Etappe* ihrer Route nach Bedarf aktualisieren. Für jeden Abschnitt werden eine Vorlaufzeit und ein Versandstatus angegeben. Bestätigte Liefertermine für die Bewegung zum nächsten Abschnitt der Route werden ebenfalls identifiziert. Zusammen ergeben diese Liefertermine ein geschätztes Lieferdatum der Waren an den eingehenden Lagerort. Benutzer können diese Liefertermine ändern. In diesem Fall wird das geschätzte Lieferdatum der Waren dann automatisch aktualisiert, basierend auf den Vorlaufzeiten und Abschnitten der Route. Die Einsicht in die Waren in Zustellung nach Fahrt und Schiff ist vor dem Empfang der Waren pro Container möglich. Da die Daten in jeder Zeile der Einkaufsbestellung aktualisiert werden, haben Unternehmen mehr Kontrolle über die Logistik- und Lagerortplanung.

## <a name="landed-cost-concepts"></a>Gesamttransportkosten-Konzepte

Die folgende Tabelle fasst einige Kernkonzepte der Gesamttransportkosten zusammen.

| Konzept | Beschreibung |
|---|---|
| Seereise | Normalerweise ist eine Fahrt ein Schiff. Je nach Ihren Praktiken und Verfahren kann es sich jedoch auch um einen Lieferanten oder eine Einkaufsbestellung handeln. Es gibt keine Einschränkungen bei der Verwendung dieses Konzepts. |
| Folio | Eine Palette wird oft durch Zollbestimmungen bestimmt. Es kann aus den Waren eines Lieferanten für eine Entität/Firma pro Sendung bestehen. Die Waren in einer Palette können sich in einem Container befinden oder auf mehrere Container verteilt sein. |
| Versandcontainer | Transportcontainer speichern Zeilen der Einkaufsbestellung. Sie befinden sich eine Ebene unterhalb der Sendungsebene. Sie werden typischerweise verwendet, wenn die Kalkulation für Waren pro Container erfolgt, oder wenn der Wareneingang pro Container erfolgt. |
| Versandcontainertyp | Transportcontainer-Typen können den Preis für eine Kalkulation (z. B. Fracht) bestimmen. Sie liefern auch nützliche Versandinformationen. |
| Kostentyp | Kostenarten identifizieren Kosten, die mit Importen verbunden sind, z. B. Zoll, Fracht und Versicherung. |
| Automatische Kosten | Autokalkulationen funktionieren wie Handelsvereinbarungen. Eine Autokalkulation ist mit einer Fahrt-Ebene verknüpft. |
| Port | Häfen sind Bereiche, in denen Waren empfangen und umgeschlagen werden. |
| Schiff | Ein Schiff ist das Medium, das zum Transport von Waren verwendet wird, z. B. ein Schiff oder ein Flugzeug. |
| Waren in Zustellung | Abhängig von den Einstellungen werden die Waren in ein Lagerort in Zustellung eingelagert, nachdem eine Rechnung aktualisiert wurde. |
| Aktivität | Aktivitäten können verwendet werden, um jeden wichtigen Schritt der Route zwischen zwei Häfen zu speichern. Sie können verwendet werden, um Termine zu aktualisieren. |
| Reisevorlage | Fahrtenvorlagen sind Routen, die Waren zwischen zwei Häfen nehmen. |

Für einen Vergleich der Terminologie und Funktionen der Module **Gesamttransportkosten** und **Transportverwaltung** (TMS), siehe [Gesamttransportkosten vs. Transportverwaltung](landed-cost-vs-tms.md).
