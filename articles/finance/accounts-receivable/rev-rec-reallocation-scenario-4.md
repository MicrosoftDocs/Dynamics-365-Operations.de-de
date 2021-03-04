---
title: Neuzuweisung der Umsatzerkennung – Szenario 4
description: In diesem Artikel wird eine Neuzuweisung erläutert, bei der eine Position aus einem vorhandenen und teilweise in Rechnung gestellten Auftrag gelöscht wird. Unabhängig davon, ob die Position aus dem Auftrag entfernt oder in den Status „Storniert“ gesetzt wird, ist das Ergebnis identisch.
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
ms.openlocfilehash: 500c7817795448d7d9759c4ad7a1842df0a9bdc5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003279"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Neuzuweisung der Umsatzerkennung – Szenario 4

[!include [banner](../includes/banner.md)]

In diesem Artikel wird eine Neuzuweisung erläutert, bei der eine Position aus einem vorhandenen und teilweise in Rechnung gestellten Auftrag gelöscht wird. Unabhängig davon, ob die Position aus dem Auftrag entfernt oder in den Status „Storniert“ gesetzt wird, ist das Ergebnis identisch.

In diesem Fall ist die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Registerkarte **Umsatzerkennung** auf der Seite **Hauptbuchparameter** (**Umsatzerkennung \> Einrichtung \> Hauptbuchparameter**) auf **Nein** festgelegt.

[![Option „Rechnungskorrekturen auf Debitorenkonten buchen“ auf „Nein“ festgelegt](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Für den Kunden US\_SI\_0003 wird ein Auftrag angelegt. Der Kunde kauft einen Laptop (Artikelnummer S0012) mit Installationsservice (Artikelnummer S0001) und Supportplan (Artikelnummer S0008, „fortwährender Entwicklungsservice“). Der Umsatzerlös für den Laptop und den Installationsservice werden sofort erkannt. Der Umsatzerlös für den Supportplan wird über einen Zeitraum von zwölf Monaten verzögert und erfasst, wie durch den im Vertrag festgelegten Zeitraum festgelegt.

[![Auftragspositionen für Laptop, Installationsservice und Supportplan](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Der Auftrag wird bestätigt. Weil bei allen drei Positionen die Umsatzerlöspreiszuteilung eingerichtet ist, wird der Umsatzerlöspreis im Zuge der Auftragsbestätigung berechnet. Den zu erfassenden Umsatzerlös können Sie auf der Seite **Umsatzerlöspreiszuteilung** anzeigen. (Wählen Sie dazu auf der Seite **Auftrag** im Aktionsbereich auf der Registerkarte **Verwalten** in der Gruppe **Umsatzerkennung** die Option **Umsatzerlöspreiszuteilung** aus.) Der Umsatzerlös für den Laptop wird in Höhe von 995,84 US-Dollar auf das Konto für Umsatzerlöse gebucht. Der Umsatzerlös für den Installationsservice wird in Höhe von 314,47 US-Dollar ebenso auf das Konto für Umsatzerlöse gebucht. Der Umsatzerlös für den Supportplan wird in Höhe von 188,69 US-Dollar auf das Konto für verzögerte Umsatzerlöse gebucht. Die Summe der Umsatzerlöspreise muss der Summe der Positionen entsprechen, die so eingerichtet wurden, dass die Umsatzerlöspreiszuteilung erfasst wird (1.499,00 US-Dollar).

[![Seite mit der Umsatzerlöspreiszuteilung](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Dem Kunden werden Laptop und Supportplan in Rechnung gestellt, nicht jedoch der Installationsservice. Die folgende Abbildung zeigt den Buchhaltungseintrag, der zur Rechnung gebucht wird.

[![Buchhaltungseintrag für den in Rechnung gestellten Auftrag](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Mit dem Eintrag werden 1.276,94 US-Dollar auf die Debitorenkonten gebucht. Weil es sich bei dieser Rechnung aber um eine Teilrechnung handelt, entsprechen die Umsatzerlöse oder verzögerten Umsatzerlöse zuzüglich Steuer nicht dem Forderungsbetrag. Die Differenz von -14,47 US-Dollar wird auf das Verrechnungskonto für Teilrechnungsumsätze gebucht.

Außerdem wird der Umsatzerkennungszeitplan erstellt.

[![Seite „Umsatzerkennungszeitplan“ für die Teilrechnung](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Später beschließt der Kunde, doch keinen Installationsservice zu kaufen. Daher wird diese Position aus dem Auftrag gelöscht. Beachten Sie, dass der Auftrag nicht erneut bestätigt werden kann, weil im Auftrag nur die berechneten Positionen verbleiben.

[![Auftrag nach Löschung der Installationsserviceposition](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Obwohl der Auftrag nicht bestätigt werden kann, kann er neu zugewiesen werden. Zum Öffnen der Seite **Preis mit neuen Auftragspositionen erneut zuteilen** wählen Sie im Auftrag die Option **Preis mit neuen Auftragspositionen erneut zuteilen** aus. Wählen Sie erst die beiden verbleibenden Auftragspositionen und dann **Neuzuweisung aktualisieren** aus. In der Spalte **Neu zugewiesener Betrag** wird zu jeder verbleibende Auftragsposition der neue Umsatzerlöspreis angezeigt.

[![Neue Umsatzerlöspreise auf der Seite „Preis mit neuen Auftragspositionen erneut zuteilen“](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Rufen Sie anschließend mit **Erwarteter Beleg** die Buchhaltungseinträge auf.

[![Buchhaltungseinträge auf der Seite „Erwarteter Beleg“](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Mit den letzten fünf Positionen auf der Seite **Erwarteter Beleg** wird der ursprüngliche Buchhaltungseintrag aus der gebuchten Rechnung storniert. Die ersten vier Positionen entsprechen den neuen Buchhaltungseinträgen, die für die Rechnung gebucht werden. Dem Kunden wird keine neue Rechnung ausgestellt. Nach der Neuzuteilung schuldet der Kunde weiterhin 1.276,94 US-Dollar, was dem Betrag entspricht, der im neuen Buchhaltungseintrag auf die Debitorenkonten gebucht werden muss. Der neue Umsatzerlös oder der verzögerte Umsatzerlös zuzüglich Steuer entspricht 1.276,94 US-Dollar. Daher ist keine Buchung auf das Verrechnungskonto für Teilrechnungsumsätze erforderlich.

Schließen Sie die Neuzuweisung mit **Verarbeiten** ab. Ein Buchungsdatum wird eingegeben. Nach der Neuzuweisung wird die neue Preiszuteilung der beiden verbleibenden Artikel auf der Seite **Umsatzerlöspreiszuteilung** angezeigt.

[![Preisneuzuteilung bei den verbleibenden Artikeln auf der Seite „Umsatzerlöspreiszuteilung“](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Der Umsatzerkennungszeitplan wurde ebenfalls entsprechend dem neuen Preis für die Neuzuteilung von Umsatzerlösen aktualisiert. Öffnen Sie im Auftrag die Seite **Umsatzerkennungszeitplan**. Zuvor hatte Artikel S0008 13 Positionen (für den Artikel galt ein 12-Monats-Zeitplan). Nun sind es 39 Positionen, das heißt, die 13 ursprünglichen Zeitplanpositionen, 13 Stornierungspositionen und 13 Positionen entsprechend dem neuen Umsatzerlöspreis.

[![Aktualisierte Seite „Umsatzerkennungszeitplan“ mit 39 Positionen zu Artikel S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Bei Auswahl von **Beleg** wird der ursprüngliche Buchhaltungseintrag in der Rechnungsjournal angezeigt. Um im Auftrag den Stornoeintrag und den neuen Buchhaltungseintrag anzuzeigen, wählen Sie im Aktionsbereich die Option **Umsatzanpassungen** und danach **Beleg** aus.

Öffnen Sie als Nächstes die Seite **Alle Debitoren** (**Debitorenkonten \> Debitoren \> Alle Debitoren**), wählen Sie den Debitor **UNS\_SI\_0003** und danach **Transaktionen** aus. Die Originalrechnung (000008) zusammen mit dem Originalbuchhaltungseintrag steht auf der Seite **Debitorenbuchungen**. Weil die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Seite **Hauptbuchparameter** auf **Nein** gesetzt ist, wird nur das Hauptbuch aktualisiert. Dies ist der Grund, warum die stornierten und aktualisierten Buchhaltungseinträge nicht angezeigt werden. Beachten Sie, dass die in [Szenario 3](rev-rec-reallocation-scenario-3.md) erstellten Transaktionen zur Umsatzanpassung angezeigt werden.

[![Ursprünglicher Buchhaltungseintrag auf der Seite „Debitorenbuchungen“](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)
