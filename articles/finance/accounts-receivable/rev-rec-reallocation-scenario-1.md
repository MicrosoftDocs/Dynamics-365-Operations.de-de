---
title: Neuzuweisung der Umsatzerkennung – Szenario 1
description: In diesem Artikel wird eine Neuzuweisung erläutert, bei der zwei Aufträge eingegeben, aber nur bestätigt werden. Liegen mehr als zwei Aufträge mit dem Status „Bestätigt“ vor, ist das Ergebnis ähnlich.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a0add2d4bc01127c1f359736398123a6a3df9fe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969651"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Neuzuweisung der Umsatzerkennung – Szenario 1

[!include [banner](../includes/banner.md)]

In diesem Artikel wird eine Neuzuweisung erläutert, bei der zwei Aufträge eingegeben, aber nur bestätigt werden. Liegen mehr als zwei Aufträge mit dem Status „Bestätigt“ vor, ist das Ergebnis ähnlich.

In diesem Fall ist die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Registerkarte **Umsatzerkennung** auf der Seite **Hauptbuchparameter** (**Umsatzerkennung \> Einrichtung \> Hauptbuchparameter**) auf **Nein** festgelegt.

[![Option „Rechnungskorrekturen auf Debitorenkonten buchen“ auf „Nein“ festgelegt](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Für den Kunden US\_SI\_0003 wird ein Auftrag angelegt. Der Kunde kauft einen Laptop (Artikelnummer S0012) und einen zugehörigen Supportplan (Artikelnummer S0008, „fortwährender Entwicklungsservice“). Der Umsatzerlös für den Laptop wird sofort erkannt (es gibt keinen Umsatzerkennungszeitplan). Der Umsatzerlös für den Supportplan wird über einen Zeitraum von zwölf Monaten verzögert und erfasst, wie durch den im Vertrag festgelegten Zeitraum festgelegt.

[![Auftragspositionen für Laptop und Supportplan](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Der Auftrag wird bestätigt. Weil bei beiden Artikeln die Umsatzerlöspreiszuteilung eingerichtet ist, wird der Umsatzerlöspreis im Zuge der Auftragsbestätigung berechnet. Den zu erfassenden Umsatzerlös können Sie auf der Seite **Umsatzerlöspreiszuteilung** anzeigen. (Wählen Sie dazu auf der Seite **Auftrag** im Aktionsbereich auf der Registerkarte **Verwalten** in der Gruppe **Umsatzerkennung** die Option **Umsatzerlöspreiszuteilung** aus.) Der Umsatzerlös für den Laptop wird in Höhe von 1.008,01 US-Dollar auf das Konto für Umsatzerlöse gebucht. Der Umsatzerlös für den Supportplan wird in Höhe von 190,99 US-Dollar auf das Konto für verzögerte Umsatzerlöse gebucht. Die Summe der Umsatzerlöspreise muss der Summe der Positionen entsprechen, die so eingerichtet wurden, dass die Umsatzerlöspreiszuteilung erfasst wird (1.199,00 US-Dollar).

[![Seite mit der Umsatzerlöspreiszuteilung](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Zum Zeitpunkt des Verkaufs wünschte der Kunde keinen Installationsservice (Artikelnummer S0001), änderte seine Meinung aber später. Daher wird für ihn ein zweiter Auftrag eingegeben.

[![Auftragsposition über Installationsservice](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Der zweite Auftrag wird bestätigt. Weil dieser Auftrag nur eine Position enthält, erfolgt die Umsatzerlöspreiszuteilung nicht im Zuge der Auftragsbestätigung. Sie erfolgt nur, wenn mindestens zwei eindeutige Artikel vorhanden sind und bei diesen die Umsatzerlöspreiszuteilung eingerichtet ist.

Wenn der neue Auftrag die einzige Vertragsänderung darstellt, kann die Neuzuteilung beginnen. Zum Öffnen der Seite **Preis mit neuen Auftragspositionen erneut zuteilen** wählen Sie in einem der Aufträge die Option **Preis mit neuen Auftragspositionen erneut zuteilen** aus. Alternativ wählen Sie **Umsatzerkennung \> Periodische Aufgaben \> Preis mit neuen Auftragspositionen erneut zuteilen** aus. Wählen Sie die beiden Aufträge und die entsprechenden Auftragspositionen und danach **Neuzuweisung aktualisieren** aus. In der Spalte **Neu zugewiesener Betrag** wird zu jeder Auftragsposition der neue Umsatzerlöspreis angezeigt.

[![Neue Umsatzerlöspreise auf der Seite „Preis mit neuen Auftragspositionen erneut zuteilen“](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Bei Auswahl von **Erwarteter Beleg** wird nichts angezeigt, weil keine Rechnungen gebucht wurden.

Schließen Sie die Neuzuweisung mit **Verarbeiten** ab. Sie werden aufgefordert, ein Buchungsdatum einzugeben, auch wenn nichts gebucht wurde. Nach der Neuzuweisung wird auf der Seite **Umsatzerlöspreiszuteilung** zu jedem Auftrag die Preiszuweisung bei allen Artikeln in beiden Aufträgen angezeigt. Anders ausgedrückt: Die Seite **Umsatzerlöspreiszuteilung** zu den einzelnen Aufträgen enthält einen Artikel, der in diesem Auftrag nicht vorhanden ist, weil er Teil desselben Vertrags ist, jedoch in einem anderen Auftrag erfasst wurde.

> [!TIP]
> Um zu erklären, warum diese zusätzlichen Artikel angezeigt werden, können Sie das Raster mit weiteren Spalten ergänzen, wie z. B. **Neuzuweisungs-ID** und **Auftrag**.
> 
> [![Zusätzliche Spalten auf der Seite „Umsatzerlöspreiszuteilung“](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)
