---
title: Bestandsmengen reservieren
description: In diesem Artikel werden die verschiedenen Optionen beschrieben, die für die Reservierung von Bestand verfügbar sind.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c0e283189998473469164398fa6f43c8e8825e
ms.sourcegitcommit: 3a882de1f1c27654a8e92ebc1999c75678cc9a53
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/27/2022
ms.locfileid: "9201865"
---
# <a name="reserve-inventory-quantities"></a>Bestandsmengen reservieren

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die verschiedenen Optionen beschrieben, die für die Reservierung von Bestand verfügbar sind.

Lagermengen können für einen bestimmten Auftrag automatisch reserviert werden. Das heißt, dass der reservierte Lagerbestand nicht für andere Aufträge aus dem Lagerort entnommen werden kann, es sei denn, die gesamte Lagerreservierung oder ein Teil davon wird storniert.

Für das Reservieren von Lagerbestand gibt es mehrere Gründe:
-   "Zuerst bestellt, zuerst geliefert", was bedeutet, dass Kunden verfügbare Artikel in der gleichen Reihenfolge erhalten, in der die Aufträge platziert werden.
-   Ein Mangel an Artikeln aufgrund von langen oder ungewissen Lieferzeiten des Lieferanten. Sie möchten die Lieferung an bestimmte Kunden oder die Lieferung bestimmter Aufträge ggf. mit den ersten verfügbaren Artikeln sicherstellen.
-   Bestimmte Kunden oder bestimmte Auftragstypen haben im Hinblick auf die Lieferung oberste Priorität.
-   Artikel mit Serien- oder Chargennummern. Sie können bestimmte Artikel markieren, die im Rahmen bestimmter Aufträge geliefert werden oder wurden.
-   Speziell bestellte Artikel werden für bestimmte Aufträge reserviert.
-   Produktionsaufträge. Sie können z. B. Artikel markieren, die für bestimmte Aufträge hergestellt und angepasst wurden.

Der Lagerbestand kann automatisch reserviert werden, wenn eine neue Auftragsposition erstellt wird, oder er wird manuell für die individuellen Aufträge reserviert. Es ist auch möglich, Bestand in verschiedenen Stufen in einem Produktionsprozess zu reservieren. Nur gelagerte Produkte können reserviert werden. Leistungen können nicht reserviert werden, da es keinen Lagerbestand gibt. Sowohl der physische als auch der bestellte, aber noch nicht eingegangene Lagerbestand kann reserviert werden. Wenn eine größere Menge reserviert wird, als im verfügbaren Lagerbestand vorhanden ist, wird eine Warnung angezeigt, dass das Reservieren einer so großen Menge nicht möglich ist. Sie können die Menge dann trotzdem reservieren oder die bestellte Menge ändern. Die Menge kann entweder reserviert oder geändert werden. Wenn mehr Artikel reserviert werden, als verfügbar sind, wird der Mangel das nächste Mal abgedeckt, wenn Artikel für die Lieferung verfügbar sind.

## <a name="inventory-reservation-policies"></a>Bestandsreservierungsrichtlinien
Bestandreservierungsrichtlinien werden auf den Seiten **Lagersteuerungsgruppen** und **Parameter für Lager- und Lagerortverwaltung**  und der Seite **Produktionsparameter** festgelegt.
### <a name="policies-on-the-item-model-groups-page"></a>Richtlinien auf der Artikelmodellgruppenseite

Der Abschnitt **Bestandrichtlinie** enthält die folgenden Reservierungsrichtlinien.

| &nbsp;                  | &nbsp;                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reservierungsrichtlinie**  | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO-datumsgesteuert    | Wenn Sie im Formular die Option **FIFO-datumsgesteuert** aktivieren, wird die Lagerreservierung über ein Sortierdatum nach dem FIFO-Prinzip gesteuert. Chargen sind basierend auf dem frühesten Wareneingangsdatum nach dem Prinzip "first in, first out" (FIFO) reserviert.                                                                                                                                                                                                                                                                       |
| Rückwärts ab Versanddatum | Diese Option ist nur verfügbar, wenn Sie die Option **FIFO datumsgesteuert** ausgewählt haben. Wenn Sie zusätzlich das Kontrollkästchen **Rückwärts ab Versanddatum** aktivieren, erfolgt die Lagerreservierung rückwärts ab dem gewünschten Lieferdatum unter Verwendung des LIFO-Prinzips (last in, first out). Sind vor dem Versanddatum keine Zugänge zu verzeichnen, wird eine FIFO-Reservierung vorgenommen.                                                                                                                                                                                                           |
| Artikelverkaufsreservierung  | Bestimmt, ob die Artikelreservierung manuell oder automatisch erfolgt. Wenn eine Reservierung automatisch erfolgt, wird der Bestand reserviert, wenn Auftragspositionen erstellt werden. Es ist möglich, Reservierungen auf der Artikelnummerenebene für Stücklisten **Automatisch** oder für die einzelnen Elemente einer Stückliste **Auflösung** zu machen. Der Standardwert wird aus den für **Artikelvertriebsreservierung** **Debitorparametern** übernommen werden. Auf dieser Seite wird der Wert im Reservierungsfeld im **Abschnitt** **Vertriebsstandardwerte** in der Registerkarte **Allgemeines** festgelegt. |
| Auswahl derselben Charge    | Mit der Reservierung derselben Charge können Sie Bestand für eine Auftragsposition aus einer einzelnen Lagercharge reservieren. Wenn Sie diese Option verwenden möchten, müssen Sie die Option **Bedarf konsolidieren** auch auf **Ja** festlegen. Darüber hinaus gibt es weitere Einstellungen, die die für die Lagerdimensionsgruppe und Rückverfolgungsangabengruppe erforderlich sind. Weitere Informationen finden Sie unter [Die gleiche Charge für einen Kundenauftrag](../sales-marketing/reserve-same-batch-sales-order.md) reservieren.                                                          |
| Bedarf konsolidieren | Diese Option ist mit der Option **Auswahl derselben Charge** ähnlich und konsolidiert den Bestand, der für Auftragspositionen reserviert ist, in einer einzelnen Anforderung.                                                                                                                                                                                                                                                                                                                                                                                      |
| FEFO-datumsgesteuert    | Mit dieser Option können Sie den Chargen reservieren, die nahe dem Ablaufdatum oder dem Mindesthaltbarkeitsdatum sind. Zudem müssen Sie das Feld **Kommissionierungskriterien** einrichten, um entweder **Ablaufdatum oder** **Mindesthaltbarkeitsdatum** auszuwählen.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Beispiel für "FIFO-Datumsgesteuert" und "Rückwärts ab Versanddatum"

In diesem Beispiel besteht der verfügbare Lagerbestand für Artikelnummer A für drei verschiedene Chargennummern.

| Artikelnummer | Chargennummer | Menge | Datum             |
|-------------|--------------|----------|------------------|
| A:           | 1.000         | 5        | 2. Februar 2016 |
| A:           | 1001         | 3        | 1. Januar 2016  |
| A:           | 1002         | 7        | 3. März 2016    |

Für einen Auftrag, der automatisch reserviert und am 4. April 2016 geliefert werden soll, wird folgende Charge reserviert:
-   Wenn sowohl das Kontrollkästchen **FIFO-Datumsgeteuert** und **Rückwärts vom Versanddatum** aktiviert ist, wird die Charge 1000 reserviert, weil es sich dabei um die Charge handelt, deren Zugangsdatum dem Auftragslieferdatum am nächsten liegt.
-   Wenn das Kontrollkästchen **FIFO-Datumsgesteuert** aktiviert und das Kontrollkästchen **Rückwärts ab Versanddatum** deaktiviert ist, wird die Charge 1001 reserviert, weil es sich dabei um die Charge mit dem frühesten Eingangsdatum handelt (FIFO).
-   Wenn sowohl das Kontrollkästchen **FIFO-Datumsgesteuert** und **Rückwärts ab Versanddatum** aktiviert sind, wird die Charge 1002 reserviert, weil es sich dabei um die Charge handelt, deren Zugangsdatum dem Versanddatum am nächsten liegt.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Richtlinien auf der Seite„Parameter für Lager- und Lagerortverwaltung“ anzeigen

Es gibt zwei Möglichkeiten, die Reservierungen auf der Seite **Parameter für Lager- und Lagerortverwaltung** zugeordnet werden:
-   Mit der Option **Bestellte Artikel reservieren** in der Registerkarte **Allgemein** können Sie Artikelzugänge reservieren, die gegenüber Artikelabgängen in den Bereichen Debitoren, Projektverwaltung und Buchhaltung sowie Produktionssteuerung bestellt wurden. Wenn Sie diese Option deaktivieren, können Sie nur Artikel reservieren, die physisch eingegangen sind. Wenn ein bestimmter Artikel so eingerichtet wurde, dass er einen negativen Bestand akzeptiert, ist dieses Feld nicht relevant.
-   Die Option **Artikel automatisch reservieren** auf der Registerkarte **Umlagerung** legt die Standardeinstellung fest, wenn Artikel für Umlagerungsaufträge automatisch reserviert werden. Die Standardeinstellung kann auf einzelnen Umlagerungsaufträge überschrieben werden.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Bestandreservierungsrichtlinien auf der Produktionsparameterseite

Der Wert des Feldes **Reservierung** auf der Registerkarte **Allgemeines** auf der Seite **Produktionsparameter** ist abhängig vom Standardpunkt im Produktionsprozess, für den Lagerbestand reserviert werden soll. So kann zum Beispiel Bestand reserviert werden, wenn Arbeit eingeplant wird oder wenn Arbeit gestartet wird.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
