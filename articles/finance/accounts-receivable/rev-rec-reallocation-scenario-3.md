---
title: Neuzuweisung der Umsatzerkennung – Szenario 3
description: In diesem Artikel wird eine Neuzuweisung erläutert, bei der ein vorhandener und berechneter Auftrag mit einer neuen Position ergänzt wird. Wird einem Vertrag ein neuer Artikel hinzugefügt wird, kann dies entweder im bestehenden Auftrag oder einem neuen Auftrag erfolgen.
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
ms.openlocfilehash: 51646d27fe8c343c99360815d22949ffe0757979
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003353"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Neuzuweisung der Umsatzerkennung – Szenario 3

[!include [banner](../includes/banner.md)]

In diesem Artikel wird eine Neuzuweisung erläutert, bei der ein vorhandener und berechneter Auftrag mit einer neuen Position ergänzt wird. Wird einem Vertrag ein neuer Artikel hinzugefügt wird, kann dies entweder im bestehenden Auftrag oder einem neuen Auftrag erfolgen. Sie sehen auch, was passiert, wenn die Debitorenkonten bedingt durch die Neuzuweisung aktualisiert werden.

In diesem Fall ist die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Registerkarte **Umsatzerkennung** auf der Seite **Hauptbuchparameter** (**Umsatzerkennung \> Einrichtung \> Hauptbuchparameter**) auf **Ja** festgelegt.

[![Option „Rechnungskorrekturen auf Debitorenkonten buchen“ auf „Ja“ festgelegt](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Für den Kunden US\_SI\_0003 wird ein Auftrag angelegt. Der Kunde kauft einen Laptop (Artikelnummer S0012) und einen zugehörigen Supportplan (Artikelnummer S0008, „fortwährender Entwicklungsservice“). Der Umsatzerlös für den Laptop wird sofort erkannt. Der Umsatzerlös für den Supportplan wird über einen Zeitraum von zwölf Monaten verzögert und erfasst, wie durch den im Vertrag festgelegten Zeitraum festgelegt.

[![Auftragspositionen für Laptop und Supportplan](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Der Auftrag wird bestätigt. Weil bei beiden Artikeln die Umsatzerlöspreiszuteilung eingerichtet ist, wird der Umsatzerlöspreis im Zuge der Auftragsbestätigung berechnet. Den zu erfassenden Umsatzerlös können Sie auf der Seite **Umsatzerlöspreiszuteilung** anzeigen. (Wählen Sie dazu auf der Seite **Auftrag** im Aktionsbereich auf der Registerkarte **Verwalten** in der Gruppe **Umsatzerkennung** die Option **Umsatzerlöspreiszuteilung** aus.) Der Umsatzerlös für den Laptop wird in Höhe von 1.008,01 US-Dollar auf das Konto für Umsatzerlöse gebucht. Der Umsatzerlös für den Supportplan wird in Höhe von 190,99 US-Dollar auf das Konto für verzögerte Umsatzerlöse gebucht. Die Summe der Umsatzerlöspreise muss der Summe der Positionen entsprechen, die so eingerichtet wurden, dass die Umsatzerlöspreiszuteilung erfasst wird (1.199,00 US-Dollar).

[![Seite mit der Umsatzerlöspreiszuteilung](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Der Auftrag wird komplett in Rechnung gestellt. Die folgende Abbildung zeigt den Buchhaltungseintrag, der zur Rechnung gebucht wird.

[![Buchhaltungseintrag für den komplett in Rechnung gestellten Auftrag](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Außerdem wird der Umsatzerkennungszeitplan erstellt. Nach einiger Zeit wurden in zweien der Monate Umsatzerlöse für den Supportplan erkannt.

[![Seite „Umsatzerkennungszeitplan“ nach Ablauf von zwei Monaten](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Zu diesem Zeitpunkt beschließt der Kunde, Installationsservices (Artikelnummer S0001) zu ergänzen. Der Artikel wird im bestehenden Auftrag ergänzt. Der Kunde wird aufgefordert, zu bestätigen, dass er den vollständig in Rechnung gestellten Auftrag ändern möchte, und wählt **Ja** aus.

[![Auftrag nach Ergänzung der Installationsserviceposition](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Wenn außer dem neuen Artikel keine weiteren Änderungen am Auftrag mehr vorgesehen sind, kann die Neuzuteilung beginnen. Zum Öffnen der Seite **Preis mit neuen Auftragspositionen erneut zuteilen** wählen Sie im Auftrag die Option **Preis mit neuen Auftragspositionen erneut zuteilen** aus. Wählen Sie erst alle Auftragspositionen zu diesem Auftrag und dann **Neuzuteilung aktualisieren** aus. In der Spalte **Neu zugewiesener Betrag** wird zu jeder Auftragsposition der neue Umsatzerlöspreis angezeigt.

[![Neue Umsatzerlöspreise auf der Seite „Preis mit neuen Auftragspositionen erneut zuteilen“](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Rufen Sie anschließend mit **Erwarteter Beleg** die Buchhaltungseinträge auf. Weil die Option **Rechnungskorrekturen auf Debitorenkonten buchen** auf der Seite **Hauptbuchparameter** auf **Ja** festgelegt ist, werden diese Buchhaltungseinträge mittels des Kreditdokuments in das Hauptbuch gebucht, und in den Debitorenkonten wird eine neue Rechnung erstellt.

[![Buchhaltungseinträge auf der Seite „Erwarteter Beleg“](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Mit den letzten vier Positionen auf der Seite **Erwarteter Beleg** wird der ursprüngliche Buchhaltungseintrag aus der gebuchten Rechnung storniert. Die ersten fünf Positionen entsprechen den neuen Buchhaltungseinträgen, die für die Rechnung gebucht werden. Dem Kunden wird keine neue Rechnung ausgestellt. Nach der Neuzuteilung schuldet der Kunde weiterhin 1.276,94 US-Dollar, was dem Betrag entspricht, der im neuen Buchhaltungseintrag auf die Debitorenkonten gebucht werden muss. Die Gegenbuchung zur Vorsteuer und der Umsatzerlös oder der verzögerte Umsatzerlös entsprechen 995,83 US-Dollar + 188,69 US-Dollar + 77,94 US-Dollar = 1.262,46 US-Dollar. Der Umsatzerlös oder der verzögerte Umsatzerlös hat sich aufgrund der Neuzuteilung geändert. Die Differenz von -14,48 US-Dollar wird auf das Verrechnungskonto für Teilrechnungsumsätze gebucht. Dieser Saldo wird ausgeglichen, wenn die Rechnung für den neuen im Auftrag ergänzten Artikel gebucht wird.

Schließen Sie die Neuzuweisung mit **Verarbeiten** ab. Ein Buchungsdatum wird eingegeben. Nach der Neuzuteilung wird die neue Preiszuteilung aller drei Artikel auf der Seite **Umsatzerlöspreiszuteilung** angezeigt.

[![Preisneuzuteilung bei allen drei Artikeln auf der Seite „Umsatzerlöspreiszuteilung“](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Der Umsatzerkennungszeitplan wurde ebenfalls entsprechend dem neuen Preis für die Neuzuteilung von Umsatzerlösen aktualisiert. Öffnen Sie im Auftrag die Seite **Umsatzerkennungszeitplan**. Zuvor hatte Artikel S0008 13 Positionen (für den Artikel galt ein 12-Monats-Zeitplan). Nun sind es 39 Positionen, das heißt, die 13 ursprünglichen Zeitplanpositionen, 13 Stornierungspositionen und 13 Positionen entsprechend dem neuen Umsatzerlöspreis.

[![Aktualisierte Seite „Umsatzerkennungszeitplan“ mit 39 Positionen zu Artikel S0008](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Bei Auswahl von **Beleg** wird der ursprüngliche Buchhaltungseintrag in der Rechnungsjournal angezeigt. Um im Auftrag den Stornoeintrag und den neuen Buchhaltungseintrag anzuzeigen, wählen Sie im Aktionsbereich die Option **Umsatzanpassungen** und danach **Beleg** aus.

Öffnen Sie als Nächstes die Seite **Alle Debitoren** (**Debitorenkonten \> Debitoren \> Alle Debitoren**), wählen Sie den Debitor **UNS\_SI\_0003** und danach **Transaktionen** aus. Die Originalrechnung (000006), das Rückbuchungsdokument (000006-1) und die neue Rechnung (000006-2) werden auf der Seite **Debitorenbuchungen** angezeigt. Die Originalrechnung und das Rückbuchungsdokument werden gegeneinander abgerechnet und haben einen Saldo von 0 (Null). Um die Auswirkungen im Hauptbuch zu sehen, rufen Sie zu jedem Dokument den Beleg auf.

[![Originalrechnung, Rückbuchungsdokument und neue Rechnung auf der Seite „Debitorenbuchungen“](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Der Auftrag wird erneut in Zusammenhang mit dem ergänzten Artikel in Rechnung gestellt. Die Gesamtrechnung an den Kunden weist 300,00 US-Dollar + 19,50 US-Dollar Steuer und in Summe somit 319,50 US-Dollar aus. Die folgende Abbildung zeigt den Buchhaltungseintrag, der gebucht wird.

[![Seite „Belegbuchungen“ mit dem zu buchenden Buchhaltungseintrag](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Weil die Summe aus Umsatzerlös und Mehrwertsteuer mehr als 319,50 US-Dollar beträgt, wird eine Differenz von 14,48 US-Dollar gebucht. Dieser Betrag gleicht den Saldo des Verrechnungskontos für Teilrechnungserlöse aus. Dieser Saldo wurde im neuen Buchhaltungseintrag aktualisiert, der nach der Neuzuteilung gebucht wurde.
