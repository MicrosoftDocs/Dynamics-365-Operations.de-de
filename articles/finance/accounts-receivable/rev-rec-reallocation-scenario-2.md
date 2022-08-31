---
title: Neuzuweisung der Umsatzerkennung – Szenario 2
description: In diesem Artikel wird eine Neuzuweisung erläutert, bei der Aufträge eingegeben werden. Nachdem der erste Auftrag in Rechnung gestellt wurde, ergänzt der Kunde den Vertrag mit einem Artikel. Wird einem Vertrag ein neuer Artikel hinzugefügt wird, kann dies entweder im bestehenden Auftrag oder einem neuen Auftrag erfolgen.
author: bking
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5f8dac2991b309bb91faaa3107480ca3860af008
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348380"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Neuzuweisung der Umsatzerkennung – Szenario 2

[!include [banner](../includes/banner.md)]

In diesem Artikel wird eine Neuzuweisung erläutert, bei der Aufträge eingegeben werden. Nachdem der erste Auftrag in Rechnung gestellt wurde, ergänzt der Kunde den Vertrag mit einem Artikel. Wird einem Vertrag ein neuer Artikel hinzugefügt wird, kann dies entweder im bestehenden Auftrag oder einem neuen Auftrag erfolgen.

In diesem Fall ist die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Registerkarte **Umsatzerkennung** auf der Seite **Hauptbuchparameter** (**Umsatzerkennung \> Einrichtung \> Hauptbuchparameter**) auf **Nein** festgelegt.

[![Option „Rechnungskorrekturen auf Debitorenkonten buchen“ auf „Nein“ festgelegt.](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Für den Kunden US\_SI\_0003 wird ein Auftrag angelegt. Der Kunde kauft Installationsdienste (Artikelnummer S0001) und einen Supportplan (Artikelnummer S0008) zu einem Laptop, hat diesen aber noch nicht ausgesucht. Der Umsatzerlös für die Installationsservices wird bis zum Kaufdatum des Laptops verzögert. Der Umsatzerlös für den Supportplan wird über einen Zeitraum von zwölf Monaten verzögert und erfasst, wie durch den im Vertrag festgelegten Zeitraum festgelegt.

[![Auftragspositionen für Installationsdienst und Supportplan.](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Der Auftrag wird bestätigt. Weil bei beiden Artikeln die Umsatzerlöspreiszuteilung eingerichtet ist, wird der Umsatzerlöspreis im Zuge der Auftragsbestätigung berechnet. Den zu erfassenden Umsatzerlös können Sie auf der Seite **Umsatzerlöspreiszuteilung** anzeigen. (Wählen Sie dazu auf der Seite **Auftrag** im Aktionsbereich auf der Registerkarte **Verwalten** in der Gruppe **Umsatzerkennung** die Option **Umsatzerlöspreiszuteilung** aus.) Der Umsatzerlös für den Installationsservice wird in Höhe von 250,00 US-Dollar auf das Konto für verzögerte Umsatzerlöse gebucht. Der Umsatzerlös für den Supportplan wird in Höhe von 150,00 US-Dollar ebenso auf das Konto für verzögerte Umsatzerlöse gebucht. Die Summe der Umsatzerlöspreise muss der Summe der Positionen entsprechen, die so eingerichtet wurden, dass die Umsatzerlöspreiszuteilung erfasst wird (400,00 US-Dollar).

[![Seite mit der Umsatzerlöspreiszuteilung.](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Der Auftrag wird komplett in Rechnung gestellt. Die folgende Abbildung zeigt den Buchhaltungseintrag, der zur Rechnung gebucht wird.

[![Buchhaltungseintrag für den komplett in Rechnung gestellten Auftrag.](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Der Umsatzerlöserkennungszeitplan wird ebenfalls erstellt, aber es wird noch kein Umsatzerlös erkannt.

[![Seite „Umsatzerlöserkennungszeitplan“.](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Einige Tage später sucht sich der Kunde einen Laptop aus. Ein zweiter Auftrag wird für ihn angelegt.

[![Auftragsposition zum Laptop.](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Der zweite Auftrag wird bestätigt. Weil dieser Auftrag nur eine Position enthält, erfolgt die Umsatzerlöspreiszuteilung nicht im Zuge der Auftragsbestätigung. Sie erfolgt nur, wenn mindestens zwei eindeutige Artikel vorhanden sind und bei diesen die Umsatzerlöspreiszuteilung eingerichtet ist.

Wenn der neue Auftrag die einzige Vertragsänderung darstellt, kann die Neuzuteilung beginnen. Zum Öffnen der Seite **Preis mit neuen Auftragspositionen erneut zuteilen** wählen Sie in einem der Aufträge die Option **Preis mit neuen Auftragspositionen erneut zuteilen** aus. Alternativ wählen Sie **Umsatzerkennung \> Periodische Aufgaben \> Preis mit neuen Auftragspositionen erneut zuteilen** aus. Wählen Sie die beiden Aufträge und die entsprechenden Auftragspositionen und danach **Neuzuweisung aktualisieren** aus. In der Spalte **Neu zugewiesener Betrag** wird zu jeder Auftragsposition der neue Umsatzerlöspreis angezeigt.

[![Neue Umsatzerlöspreise auf der Seite „Preis mit neuen Auftragspositionen erneut zuteilen“.](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Anschließend wählen Sie **Erwarteter Beleg** aus, um die Buchhaltungseinträge anzuzeigen, die nur im Hauptbuch gebucht werden. Weil die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Seite **Hauptbuchparameter** auf **Nein** gesetzt ist, werden die Debitorenkonten bei Verarbeitung der Neuzuweisung nicht geändert.

[![Buchhaltungseinträge auf der Seite „Erwarteter Beleg“.](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Mit den letzten drei Positionen auf der Seite **Erwarteter Beleg** wird der ursprüngliche Buchhaltungseintrag aus der gebuchten Rechnung storniert. Die ersten vier Positionen entsprechen dem neuen Buchhaltungseintrag, der für die Rechnung gebucht wird. Dem Kunden wird keine neue Rechnung ausgestellt. Nach der Neuzuweisung schuldet der Kunde weiterhin 426,00 US-Dollar, was dem Betrag entspricht, der im neuen Buchhaltungseintrag auf die Debitorenkonten gebucht werden muss. Die Gegenbuchung zur Vorsteuer und der verzögerte Umsatzerlös entsprechen 188,69 US-Dollar + 314,48 US-Dollar + 26,00 US-Dollar = 529,17 US-Dollar. Der verzögerte Umsatzerlös hat sich aufgrund der Neuzuweisung geändert. Die Differenz von 103,17 US-Dollar wird auf das Verrechnungskonto für Teilrechnungsumsätze gebucht. Dieser Saldo wird ausgeglichen, wenn die Rechnung für den zweiten bei der Neuzuweisung berücksichtigten Auftrag gebucht wird.

Schließen Sie die Neuzuweisung mit **Verarbeiten** ab. Sie werden aufgefordert, ein Buchungsdatum einzugeben, auch wenn nichts gebucht wurde. Nach der Neuzuweisung wird auf der Seite **Umsatzerlöspreiszuteilung** zu jedem Auftrag die Preiszuweisung bei allen Artikeln in beiden Aufträgen angezeigt. Anders ausgedrückt: Die Seite **Umsatzerlöspreiszuteilung** zu den einzelnen Aufträgen enthält einen Artikel, der in diesem Auftrag nicht vorhanden ist, weil er Teil desselben Vertrags ist, jedoch in einem anderen Auftrag erfasst wurde.

> [!TIP]
> Um zu erklären, warum diese zusätzlichen Artikel angezeigt werden, können Sie das Raster mit weiteren Spalten ergänzen, wie z. B. **Neuzuweisungs-ID** und **Auftrag**.
> 
> [![Zusätzliche Spalten auf der Seite „Umsatzerlöspreiszuteilung“.](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

Bei Auftrag 00036 wurde außerdem der Umsatzerlöserkennungszeitplan entsprechend dem neuen Preis für die Neuzuweisung von Umsatzerlösen aktualisiert. Öffnen Sie in diesem Auftrag die Seite **Umsatzerkennungszeitplan**. Zuvor hatte Artikel S0008 13 Positionen (für den Artikel galt ein 12-Monats-Zeitplan). Nun sind es 39 Positionen, das heißt, die 13 ursprünglichen Zeitplanpositionen, 13 Stornierungspositionen und 13 Positionen entsprechend dem neuen Umsatzerlöspreis.

[![Aktualisierte Seite „Umsatzerlöserkennungszeitplan“ mit 39 Positionen zu Artikel S0008.](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Ferner hatte Artikel S0001 zuvor zwei Positionen. Jetzt sind es sechs.

[![Aktualisierte Seite „Umsatzerlöserkennungszeitplan“ mit sechs Positionen zu Artikel S0001.](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Bei Auswahl von **Beleg** im Auftrag 000036 wird der ursprüngliche Buchhaltungseintrag in der Rechnungserfassung angezeigt. Um im Auftrag den Stornoeintrag und den neuen Buchhaltungseintrag anzuzeigen, wählen Sie im Aktionsbereich die Option **Umsatzerlösanpassungen** und danach **Beleg** aus.

[![Auftrag 000036.](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Öffnen Sie als Nächstes die Seite **Alle Debitoren** (**Debitorenkonten \> Debitoren \> Alle Debitoren**), wählen Sie den Debitor **UNS\_SI\_0003** und danach **Buchungen** aus. Die offene Rechnung aus dem Auftrag 000036 wird angezeigt. Wenn Sie den Beleg auswählen, wird der ursprüngliche Buchhaltungseintrag angezeigt, nicht der neue Buchhaltungseintrag aus der Neuzuweisung. Der Stornoeintrag und der neue Buchhaltungseintrag können in den Debitorenkonten nicht eingesehen werden.

Der zweite Auftrag wird nun in Rechnung gestellt. Die Gesamtrechnung an den Kunden weist 1.099,00 US-Dollar + 71,44 US-Dollar Steuer und in Summe somit 1.170,44 US-Dollar aus. Die folgende Abbildung zeigt den Buchhaltungseintrag, der gebucht wird.

[![Seite „Belegbuchungen“ mit dem zu buchenden Buchhaltungseintrag.](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Weil die Summe aus Umsatzerlös und Mehrwertsteuer mehr als 1.170,44 US-Dollar beträgt, wird eine Differenz von -130,17 US-Dollar gebucht. Dieser Betrag gleicht den Saldo des Verrechnungskontos für Teilrechnungserlöse aus. Nach der Neuzuweisung wird der Saldo im neuen Buchhaltungseintrag gebucht.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
