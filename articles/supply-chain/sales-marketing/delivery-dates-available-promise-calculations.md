---
title: Lieferterminzusage
description: Dieser Artikel enthält Informationen zu Lieferterminzusagen. Lieferterminzusagen ermöglichen es Ihnen, Ihren Kunden zuverlässige Lieferdaten zuzusichern und geben Ihnen Flexibilität, sodass Sie diese Daten auch einhalten können.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228265"
---
# <a name="order-promising"></a>Lieferterminzusage

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Lieferterminzusagen. Lieferterminzusagen ermöglichen es Ihnen, Ihren Kunden zuverlässige Lieferdaten zuzusichern und geben Ihnen Flexibilität, sodass Sie diese Daten auch einhalten können.

Die Lieferterminzusage berechnet die früheste Versand- und Eingangsdaten und basiert auf der Lieferdatumskontrollmethode und der Transporttage. Sie können unter den folgenden Lieferdatumkontrollmethoden auswählen:

- **Verkaufslieferzeit** – Die Verkaufslieferzeit ist die Zeit, die zwischen dem Erstellen des Auftrags und dem Versand der Artikel verstreicht. Die Berechnung des Lieferdatums basiert auf einer Standardanzahl von Tagen und berücksichtigt nicht die Verfügbarkeit am Lager, den bekannten Bedarf oder eine geplante Lieferung.
- **VfZ (verfügbar auf Zusage)** – VfZ ist die Menge eines Artikels, der verfügbar ist und einem Debitor für ein bestimmtes Datum zugesichert werden kann. Bei der VfZ-Berechnung werden nicht zugesicherter Bestand, Lieferzeiten und geplante Zu- und Abgänge berücksichtigt.
- **VfZ + Sicherheitszuschlag für Warenabgang**: Das Versanddatum entspricht dem VfZ-Datum plus dem Sicherheitszuschlag für den Artikel. Der Sicherheitszuschlag für Warenabgang ist die zur Vorbereitung der Artikel für die Lieferung erforderliche Zeit.
- **CTP (Verfügbarkeitszusage)**– Die Verfügbarkeit wird eine durch eine Auflösung berechnet. Wenn Sie die Planungsoptimierung verwenden, ist die *CTP*-Methode zur Lieferdatumskontrolle nicht zulässig und führt, wenn sie ausgewählt ist, bei Durchführung der Berechnung zu einem Fehler. Weitere Informationen dazu, wie die CTP eingerichtet und verwendet wird, finden Sie unter [Liefertermine für Aufträge mit CTP berechnen](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).
- **CTP für die Planungsoptimierung**: Verwenden Sie die CTP-Berechnung, die von der Planungsoptimierung bereitgestellt wird. Diese Option hat keinerlei Wirkung, wenn Sie das integrierte Produktprogrammplanungsmodul verwenden. Weitere Informationen dazu, wie die CTP eingerichtet und verwendet wird, finden Sie unter [Liefertermine für Aufträge mit CTP berechnen](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

> [!NOTE]
> Bei der Aktualisierung eines Verkaufsauftrags werden die Auftragszusage-Informationen nur dann aktualisiert, wenn das vorhandene Lieferterminzusagedatum nicht erfüllt werden kann, wie in den folgenden Beispielen dargestellt:
>
> - **Beispiel 1**: Das aktuelle Lieferterminzusagedatum ist der 20. Juli, aber aufgrund einer erhöhten Menge können Sie erst am 25. Juli liefern. Da das aktuelle Datum nicht mehr eingehalten werden kann, wird die Lieferterminzusage ausgelöst.
> - **Beispiel 2**: Das aktuelle Lieferterminzusagedatum ist der 20. Juli, aber aufgrund der verringerten Menge ist es nun möglich, am 15. Juli zu liefern. Da das aktuelle Datum jedoch noch erfüllt werden kann, wird die Lieferterminzusage nicht ausgelöst, und der 20. Juli bleibt die Lieferterminzusage.

## <a name="atp-calculations"></a>VfZ-Berechnungen

Die VfZ-Menge wird mithilfe der Methode „kumulierte VfZ mit Vorausplanung“ berechnet. Der wichtigste Vorteil für diese VfZ-Berechnung ist, dass sie Instanzen behandeln kann, wenn die Summe der Abgänge zwischen Zugängen größer ist als der letzte Zugang, beispielsweise, wenn es erforderlich ist, eine Menge von einem früheren Zugang zu verwenden, um eine Bedingung zu erfüllen. Die Berechnungsmethode „kumulierte VfZ mit Vorausplanung“ umfasst alle Warenausgänge, bis die kumulierte, zu empfangende Menge die abgehende Menge überschreitet. Daher wertet diese VfZ-Berechnungsmethode aus, ob einige der Mengen einer früheren Periode in einer späteren Periode verwendet werden können..

Die VfZ-Menge ist das nicht zugesicherte Lagersaldo in der ersten Periode. Sie wird normalerweise für jede Periode berechnet, in der ein Zugang geplant wird. Das Programm berechnet die VfZ-Periode in Tagen und das aktuelle Datum als erstes Datum für die VfZ-Menge. In der ersten Periode enthält VfZ den verfügbaren Bestand abzüglich der fälligen und überfälligen Debitorenaufträge.

VfZ wird anhand folgender Formel berechnet:

VfZ = VfZ für die vorherige Periode + Zugänge für die aktuelle Periode - Abgänge für die aktuelle Periode - Nettoabgangsmenge für alle künftigen Perioden bis zu der Periode, in der die Summe der Zugänge für alle künftigen Perioden bis zur (und einschließlich der) künftigen Periode größer ist als die Summe der Abgänge bis zur (und einschließlich der) künftigen Periode.

Beachten Sie, dass die ATP-Berechnung keine Informationen zum Ablaufdatum und über den ATP-Zeitrahmen hinaus enthält, den das System erwartet, wenn eine Menge zugesagt werden kann.

Sind keine weiteren Zu- oder Abgänge mehr zu berücksichtigen, entspricht die VfZ-Menge für die folgenden Daten der zuletzt berechneten VfZ-Menge.

Sind beim Ausführen der VfZ-Prüfung nicht alle für einen Artikel verwendeten Dimensionen angegeben, kann dies für die Ab- und Zugänge nachgeholt werden. In diesem Fall müssen die Zu- und Abgänge bei der VfZ-Berechnung in den vorhandenen Dimensionen zusammengefasst werden, um die Anzahl der in der VfZ-Berechnung enthaltenen Zu- und Abgangspositionen zu verringern.

Die VfZ-Menge, die angezeigt wird, ist immer größer oder gleich 0 (null). Wenn die Berechnung eine negative VfZ-Menge ergibt (was beispielsweise der Fall sein kann, wenn zuvor eine größere Menge zugesagt wurde, als verfügbar ist), wird die Menge automatisch auf 0 festgelegt.

### <a name="example"></a>Beispiel

Das Feld **VfZ - Planungszeitraum für Bedarfsaufträge (rückwärts)** steuert, wie weit rückwärts in der Zeit nach Lagerabgängen oder verzögerten Bedarfsaufträge gesucht wird. Das Feld **VfZ - Planungszeitraum für Bedarfsaufträge (rückwärts)** steuert, wie weit rückwärts in der Zeit nach Lagerabgängen oder verzögerten Bedarfsaufträge gesucht wird. Wenn beispielsweise Aufträge, die sich nur um sieben Tage verzögern, in der VfZ-Berechnung berücksichtigt werden sollen, sollten beide Felder auf festgelegt **7** werden.

Die Felder **VfZ - Zeitverschiebung für verzögerte Bedarfsaufträge** Und **VfZ - Zeitverschiebung für verzögerte Beschaffungsaufträge** steuern, ob der verzögerte Bedarf bzw. die Lieferung in der VfZ-Berechnung berücksichtigt wird. Wenn beispielsweise übermorgen die verzögerte Angebot und Nachfrage bei der VfZ-Berechnung berücksichtigt werden soll, sollten beide Felder auf **2** festgelegt werden. Ein Wert von **2** bedeutet, dass die Menge eines Artikels in einer verzögerten Bestellung, die in der VfZ-Berechnung berücksichtigt werden soll, als zwei Tage nach dem aktuellen Datum verfügbar betrachtet wird.

Im folgenden Beispiel wird **7** in die Felder **VfZ - Planungszeitraum für Bedarfsaufträge (rückwärts)** und **VfZ - Planungszeitraum für Beschaffungsaufträge (rückwärts)** eingegeben und **1** wird in die Felder **VfZ - Zeitverschiebung für verzögerte Bedarfsaufträge** Felder und **VfZ - Zeitverschiebung für verzögerte Beschaffungsaufträge** eingegeben.

Eine Bestellung für 200 Stück eines Produkts, das vor drei Tagen hätte eingehen sollen, ist noch nicht eingegangen. Aufgrund dessen wurde eine Auftragsposition für 75 Stück des gleichen Produkts, das gestern hätte versendet werden sollen, nicht versendet.

Ein Debitor ruft an und möchte 150 Stück des gleichen Produkts bestellen. Wenn Sie die Verfügbarkeit des Produkts überprüfen, stellen Sie fest, dass eine andere Bestellung für 100 Stück des Produkts vorhanden ist, die 10 Tage später geliefert wird.

Sie erstellen eine Auftragsposition für das Produkt und geben **150** als Menge ein.

Da die Methode der Lieferdatumskontrolle VfZ ist, sind die VfZ-Daten so berechnet, dass sie das früheste mögliche Versanddatum suchen. Basierend auf den Einstellungen werden die verzögerte Bestellung und der Auftrag berücksichtigt. Die sich daraus ergebende VfZ-Menge für das aktuelle Datum ist 0. Morgen, wenn die verzögerte Bestellung erwartet wird, wird die VfZ-Menge als mehr als 0 berechnet (in diesem Fall 125). Aber 10 Tagen ab nun, wenn der zusätzliche Kauf über 100 Stück erwartet wird ist, wird die VfZ-Menge mehr als 150.

Das Versanddatum wird auf 10 Tage ab jetzt festgelegt, basierend auf der VfZ-Berechnung. Daher können Sie den Debitor darüber informieren, dass die erforderliche Menge in 10 Tage geliefert werden kann.

## <a name="ctp-calculations"></a>CTP-Berechnungen

Mit der CTP-Funktionalität können Sie Ihren Kunden realistische Termine nennen, wann Sie bestimmte Waren zusichern können. Sie können für jede Verkaufsposition ein Datum angeben, das den vorhandenen Bestand, die Produktionskapazität und die Transportzeiten berücksichtigt.

CTP erweitert die ATP-Funktionalität durch Berücksichtigung von Kapazitätsinformationen. Während die VfZ nur die Materialverfügbarkeit berücksichtigt und von unendlichen Kapazitätsressourcen ausgeht, berücksichtigt die CTP sowohl die Material- als auch die Kapazitätsverfügbarkeit. Daher liefert sie ein realistischeres Bild davon, ob die Nachfrage innerhalb eines bestimmten Zeitrahmens gedeckt werden kann.

Die CTP funktioniert jedoch ein wenig anders, je nachdem, welches Produktprogrammplanungsmodul sie verwenden (Planungsoptimierung oder integriertes Modul). Die CTP für Planungsoptimierung unterstützt derzeit nur eine Teilmenge der CTP-Szenarien, die das integrierte Modul unterstützt.

Detaillierte Informationen dazu, wie die CTP für die einzelnen Module eingerichtet und verwendet wird, finden Sie unter [Liefertermine für Aufträge mit CTP berechnen](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
