---
title: Lieferterminzusage
description: "Dieser Artikel enthält Informationen zu Lieferterminzusagen. Lieferterminzusagen ermöglichen es Ihnen, Ihren Kunden zuverlässige Lieferdaten zuzusichern und geben Ihnen Flexibilität, sodass Sie diese Daten auch einhalten können."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8aa0a58b03ee18e42ca7770ea3e22311c1ddba67
ms.lasthandoff: 03/31/2017


---

# <a name="order-promising"></a>Lieferterminzusage

Dieser Artikel enthält Informationen zu Lieferterminzusagen. Lieferterminzusagen ermöglichen es Ihnen, Ihren Kunden zuverlässige Lieferdaten zuzusichern und geben Ihnen Flexibilität, sodass Sie diese Daten auch einhalten können.

Die Lieferterminzusage berechnet die früheste Versand- und Eingangsdaten und basiert auf der Lieferdatumskontrollmethode und der Transporttage. Sie können unter vier Lieferdatumkontrollmethoden auswählen:

-   ** Verkaufslieferzeit ** – Verkaufslieferzeit ist die Zeitspanne zwischen Erstellung des Auftrags und Versand der Artikel. Die Lieferdatums basiert auf eine Standardanzahl von Tagen und nicht berücksichtigt Verfügbarkeit des Lagers, bekannten Bedarf oder geplante Lieferung.
-   ** VfZ (verfügbar für Zusage) ** – VfZ ist die Menge eines Artikels, der verfügbar ist und zugesichert werden kann einem Debitor an einem bestimmten Datum. Bei der VfZ-Berechnung werden nicht zugesicherter Bestand, Lieferzeiten und geplante Zu- und Abgänge berücksichtigt.
-   **VfZ + Sicherheitszuschlag für Warenabgang **– Das Versanddatum entspricht dem VfZ-Datum (Verfügbar für Zusage) plus dem Sicherheitszuschlag für den Artikel. Der Sicherheitszuschlag für Warenabgang ist die zur Vorbereitung der Artikel für die Lieferung erforderliche Zeit.
-   **CTP (Verfügbarkeitszusage) **– Die Verfügbarkeit wird eine durch eine Auflösung berechnet.

## <a name="atp-calculations"></a>VfZ-Berechnungen
Die VfZ-Menge wird berechnet, indem der kumuliertes "VfZ mit Blick-voran" Methode angewendet werden. Der dieser Vorteile VfZ-Berechnungsmethode ist, dass er Fälle, in denen die Summe von Abgängen mit Eingängen mehr, ist der letzte als Zugang verfügbar ist (beispielsweise, wenn eine Menge aus einem früheren Zugriff verwendet werden muss, um eine Bedingung zu entsprechen.) Der "kumuliertes VfZ mit Berechnungsmethode Blick-voran" umfasst alle Abgänge ein, bis die kumulierte zu empfangen kumulierte Menge die Menge überschreitet, um anzuzeigen. Daher wertet diese VfZ-Berechnungsmethode aus, ob einige der Mengen einer früheren Periode in einer späteren Periode verwendet werden können..  

Die VfZ-Menge ist das nicht zugesicherte Lagersaldo in der ersten Periode. Sie wird normalerweise für jede Periode berechnet, in der ein Zugang geplant wird. Das Programm berechnet die VfZ-Periode in Tagen und das aktuelle Datum als erstes Datum für die VfZ-Menge. In der ersten Periode enthält VfZ den verfügbaren Bestand abzüglich der fälligen und überfälligen Debitorenaufträge.  

VfZ wird anhand folgender Formel berechnet:  

VfZ = VfZ für die vorherige Periode + Zugänge für die aktuelle Periode – Abgänge für die aktuelle Periode – Nettoabgangsmenge für alle künftigen Perioden bis zu der Periode, in der die Summe der Zugänge für alle künftigen Perioden, bis einschließlich zukünftiger Zeiträume, die Summe der Abgänge bis einschließlich zukünftiger Zeiträume übersteigt.  

Sind keine weiteren Zu- oder Abgänge mehr zu berücksichtigen, entspricht die VfZ-Menge für die folgenden Daten der zuletzt berechneten VfZ-Menge.  

Sind beim Ausführen der VfZ-Prüfung nicht alle für einen Artikel verwendeten Dimensionen angegeben, kann dies für die Ab- und Zugänge nachgeholt werden. In diesem Fall müssen die Zu- und Abgänge bei der VfZ-Berechnung in den vorhandenen Dimensionen zusammengefasst werden, um die Anzahl der in der VfZ-Berechnung enthaltenen Zu- und Abgangspositionen zu verringern.  

Die VfZ-Menge, die angezeigt wird, ist immer größer oder gleich 0 (null). Wenn die Berechnung eine negative VfZ-Menge ergibt,(was beispielsweise der Fall sein kann, wenn zuvor eine größere Menge zugesagt wurde als verfügbar ist), wird die Menge automatisch auf **0**festgelegt.

### <a name="example"></a>Beispiel

Das Feld **VfZ - Planungszeitraum für Bedarfsaufträge (rückwärts)** steuert, wie weit rückwärts in der Zeit nach Lagerabgängen oder verzögerten Bedarfsaufträge gesucht wird. Das Feld **VfZ - Planungszeitraum für Bedarfsaufträge (rückwärts)** steuert, wie weit rückwärts in der Zeit nach Lagerabgängen oder verzögerten Bedarfsaufträge gesucht wird. Wenn beispielsweise Aufträge, die sich nur um sieben Tage verzögern, in der VfZ-Berechnung berücksichtigt werden sollen, sollten beide Felder auf festgelegt **7** werden.  

Die Felder **VfZ - Zeitverschiebung für verzögerte Bedarfsaufträge** Und **VfZ - Zeitverschiebung für verzögerte Beschaffungsaufträge** steuern, ob der verzögerte Bedarf bzw. die Lieferung in der VfZ-Berechnung berücksichtigt wird. Wenn beispielsweise übermorgen die verzögerte Angebot und Nachfrage bei der VfZ-Berechnung berücksichtigt werden soll, sollten beide Felder auf **2** festgelegt werden. Ein Wert von **2** bedeutet, dass die Menge eines Artikels in einer verzögerten Bestellung, die in der VfZ-Berechnung berücksichtigt werden soll, als zwei Tage nach dem aktuellen Datum verfügbar betrachtet wird.  

Im folgenden Beispiel wird **7** in die Felder **VfZ - Planungszeitraum für Bedarfsaufträge (rückwärts)** und **VfZ - Planungszeitraum für Beschaffungsaufträge (rückwärts)** eingegeben und **1** wird in die Felder **VfZ - Zeitverschiebung für verzögerte Bedarfsaufträge** Felder und **VfZ - Zeitverschiebung für verzögerte Beschaffungsaufträge** eingegeben.  

Eine Bestellung für 200 Stück eines Produkts, das vor drei Tagen hätte eingehen sollen, ist noch nicht eingegangen. Aufgrund dessen wurde eine Auftragsposition für 75 Stück des gleichen Produkts, das gestern hätte versendet werden sollen, nicht versendet.  

Ein Debitor ruft an und möchte 150 Stück des gleichen Produkts bestellen. Wenn Sie die Verfügbarkeit des Produkts überprüfen, stellen Sie fest, dass eine andere Bestellung für 100 Stück des Produkts vorhanden ist, die 10 Tage später geliefert wird.  

Sie erstellen eine Auftragsposition für das Produkt und geben **150** als Menge ein.  

Da die Methode der Lieferdatumskontrolle VfZ ist, sind die VfZ-Daten so berechnet, dass sie das frühest mögliche Versanddatum suchen. Basierend auf den Einstellungen werden die verzögerte Bestellung und der Auftrag berücksichtigt, und die daraus VfZ-Menge für das aktuelle Datum 0. Morgen wenn die verzögerte Bestellung erhalten werden erwartet wird, wird die VfZ-Menge mehr als 0 %(in diesem Fall, hat diese 125 %). Allerdings 10 Tagen ab nun, wenn der Zukaufkaufauftrag für 100 Stück wird erwartet Zustellung des, wird die VfZ-Menge mehr als 150.  

Daher wird das Versanddatum an 10 Tagen ab nun, basierend die VfZ-Berechnung festgelegt. Daher können Sie den Debitor darüber informieren, dass die erforderliche Menge in 10 Tage geliefert werden kann.


