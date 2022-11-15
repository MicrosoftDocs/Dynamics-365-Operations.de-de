---
title: Bedarfsgesteuerte Planung
description: Der Artikel beschreibt, wie Sie geplanter Aufträge für Artikel erzeugen, die als Entkopplungspunkte festgelegt sind.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 8ba9a6d24923b66259bc8b6cc688ec667cb000de
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740301"
---
# <a name="demand-driven-planning"></a>Bedarfsgesteuerte Planung

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Der Artikel beschreibt, wie Sie geplanter Aufträge für Artikel erzeugen, die als Entkopplungspunkte festgelegt sind.

## <a name="net-flow-and-qualified-demand"></a>Net Flow und qualifizierter Bedarf

Während der Masterplanungsphase wendet das System das Konzept des *Netto Flow* an, um den effektiven Lagerbestand auf der Grundlage des tatsächlichen Lagerbestands zuzüglich des Lagerbestands im Vorrat (bestehende Lieferaufträge, die noch nicht eingegangen sind) und abzüglich des so genannten *qualifizierten Bedarfs* (qualifizierte bevorstehende Verkäufe) zu ermitteln, wie in der folgenden Abbildung dargestellt. Wenn das System bestimmt, in welche Pufferzone ein Artikel gehört und wie hoch die Bestellmenge sein sollte, wertet es den Netto Flow aus, nicht den tatsächlichen Lagerbestand.

![Beispiel für ein Diagramm zur Berechnung des Net Flows.](media/ddmrp-net-flow-example.png "Beispiel eines Diagramms zur Berechnung des Net Flows")

Wenn ein geplanter Auftrag während eines Planungslaufs ausgeführt wird, entspricht die bestellte Menge dem maximalen Bestand abzüglich des Netto Flows. Um eine Auftragspriorität zu vergeben, verwendet das System die [prioritätsbasierte Planung](priority-based-planning.md) anstelle von Bedarfsterminen. Die bedarfsgesteuerte Materialbedarfsplanung (DDMRP) weist die Priorität eines geplanten Auftrags auf der Grundlage der bestellten Menge in Prozent des maximalen Bestands zu. In der vorigen Abbildung beträgt die bestellte Menge 53 Prozent der Höchstmenge. Die Priorität für die Wiederbeschaffung ist daher 53. (Für den Kontext ist 0 die höchste Priorität und 100 die niedrigste Priorität).

*Qualifizierter Bedarf* ist der überfällige Bedarf, plus der heutige Bedarf, plus qualifizierte Auftragsspitzen in der Zukunft. Die folgende Abbildung zeigt ein Beispiel für den Bedarf für heute (12. Juni) und die nächsten drei Tage. Mit DDMRP können Sie einen Schwellenwert für Auftragsspitzen festlegen, um einen Bedarf zu ermitteln, der über die normalen Erwartungen hinausgeht. Wenn der Schwellenwert auf 25 Stück festgelegt ist, werden zwei der in der Abbildung gezeigten zukünftigen Termine als Bestellspitzen eingestuft. Sie müssen für jedes Produkt einzeln einen Schwellenwert für Bestellspitzen festlegen, indem Sie die Seite **Artikelabdeckung** verwenden, wie in [Puffer für einen Entkopplungspunktartikel festlegen](ddmrp-buffer-profile-and-levels.md#set-up-buffers) beschrieben.

![Beispiel für eine Tabelle zur Berechnung des qualifizierten Bedarfs.](media/ddmrp-net-qualified-demand-example.png "Beispiel für ein Berechnungsdiagramm für qualifizierten Bedarf")

Vorausgesetzt, es gibt keinen überfälligen Bedarf, können Sie nun den heutigen Bedarf (18) zu den Mengen der beiden Bestellspitzen (29 und 26) addieren, um einen qualifizierten Bedarf von 73 zu erhalten. Obwohl Bedarf für den 23. Juni besteht, wird dieser nicht in die Berechnung des Netto Flows einbezogen, da DDMRP den geplanten Auftrag anders auslöst als herkömmliche Planungsdeckungsgruppen.

## <a name="generating-planned-orders-with-ddmrp"></a>Generierung geplanter Aufträge mit DDMRP

Während eines Planungslaufs erstellt das System einen neuen geplanten Auftrag, wenn der Netto Flow für einen Artikel unter den Neubestellungspunkt fällt. Wenn Sie DDMRP verwenden, führen Sie in der Regel jeden Tag einen Planungslauf durch. Daher überprüfen Sie im Wesentlichen einmal am Tag Ihren Bestand, um festzustellen, welche Artikel wiederbeschafft werden müssen.

Die folgende Abbildung zeigt ein Beispiel für eine Situation, in der Sie eine Bestellung für 18 Stück am 20. Juni, 29 Stück am 21. Juni, 26 Stück am 22. Juni und 20 Stück am 23. Juni haben. Da der Schwellenwert für Spikes auf 25 Stück festgelegt ist, sind zwei dieser Bestellungen als Spikes gekennzeichnet. Von diesem Artikel liegen 220 Stück im Lagerbestand vor.

![Planungsbeispiel 1.](media/ddmrp-planning-example-1.png "Planungsbeispiel 1")

Wenn Sie jetzt die Produktprogrammplanung ausführen, wird ein geplanter Auftrag generiert, wenn der Netto Flow unter den Neubestellungspunkt fällt (in diesem Beispiel 219 Stück).

![Planungsbeispiel 2.](media/ddmrp-planning-example-2.png "Planungsbeispiel 2")

In diesem Beispiel wird ein geplanter Auftrag für eine Menge von 130 produziert, was dem maximalen Bestand abzüglich des Netto Flows entspricht. Der geplanter Auftrag hat die Priorität 53,07, basierend auf seinem Anteil an der maximalen Menge. Da diese Werte am 20. Juni gefunden wurden, erstellt das System einen geplanter Auftrag, der auf den 20. Juni plus die entkoppelte Vorlaufzeit für den Artikel (in diesem Beispiel fünf Geschäftstage) datiert ist. Da fünf Geschäftstage eine Woche ab heute sind, ist der geplante Auftrag auf den 27. Juni datiert.

> [!NOTE]
> Die Masterplanung berechnet nur entkoppelte Artikel unter Verwendung von DDMRP. Alle anderen Artikel werden mit Hilfe der Standard-Materialbedarfsplanung (MRP) berechnet.
