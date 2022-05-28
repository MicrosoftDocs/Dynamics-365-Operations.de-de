---
title: Eine Mehrwertsteuerzahlung erstellen
description: Bei der Einzelvorgangsprozedur zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.
author: twheeloc
ms.date: 01/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c388a8f98cd4581abe2ec13d8922e232321e4039
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735934"
---
# <a name="create-a-sales-tax-payment"></a>Eine Mehrwertsteuerzahlung erstellen

[!include [banner](../../includes/banner.md)]

Bei der Einzelvorgangsprozedur zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.

1. Wechseln Sie zu **Steuer > Erklärungen > Mehrwertsteuer > Mehrwertsteuer abrechnen und buchen**.
2. Wählen Sie im Feld **Ausgleichsperiode** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Geben Sie im Feld **Von Datum** ein Datum ein. Wenn Sie die Option **Korrekturen einbeziehen** nicht auf der Seite **Hauptbuchparameter** auswählen, kann die Abrechnung für verschiedene Versionen verarbeitet werden. **Original** ist die erste Abrechnung für ein Periodenintervall und kann nur einmal für ein Periodenintervall verarbeitet werden. Mit den neuesten Korrekturen werden Mehrwertsteuertransaktionen abgerechnet, die gebucht wurden, nachdem die Originalversion erstellt wurde.
5. Geben Sie im Feld **Transaktionsdatum** ein Datum ein.
6. Wählen Sie **OK** aus. Der Bericht **Mehrwertsteuerzahlungen** wird gedruckt, um die abgerechneten Mehrwertsteuertransaktionen in der Periode zu überprüfen.

Ab Finance-Version 10.0.24 können Sie weglassen, dass der **Mehrwertsteuerzahlungen**-Bericht direkt nach der Implementierung des periodischen Verfahrens **Mehrwertsteuer abrechnen und buchen** unter der Funktion **Separate Generierung des Mehrwertsteuer-Zahlungsberichts aus dem Mehrwertsteuerausgleich** im Arbeitsbereich **Funktionsverwaltung** generiert wird.

Wenn die Funktion aktiviert ist, wird nach Abschluss des Abrechnungsprozesses kein Mehrwertsteuerzahlungsbericht gedruckt. Stattdessen erhalten Sie die folgende Meldung: „Mehrwertsteuerausgleich und -buchung sind abgeschlossen. Der Beleg  ‚xxxx, M/T/JJJJ‘ wurde gebucht.“

Sie können weiterhin den Mehrwertsteuerzahlungsbericht manuell ausführen. Gehen Sie dazu zu **Steuer** > **Abfragen und Berichte** > **Mehrwertsteuerabfragen** > **Mehrwertsteuerzahlungen**.

## <a name="performance-consideration"></a>Leistungsüberlegung

Das Verfahren zur Zahlung der Umsatzsteuer kann lange dauern. Die wichtigsten Faktoren, die die Durchführung des Verfahrens beeinflussen, sind die Anzahl der Rechnungen im Abrechnungszeitraum und die Anzahl der Buchungen, die in den Umsatzsteuerabrechnungsbeleg gebucht werden müssen. Um die Leistung zu verbessern, können Sie einige Funktionen umgehen, die in Ihrem Prozess nicht erforderlich sind.

### <a name="enable-the-sales-tax-payment-performance-improvement-feature"></a>Fie Leistungsverbesserungsfunktion für die Mehrwertsteuerzahlung aktivieren

Die **Leistungssteigerung bei der Umsatzsteuerzahlung**-Funktion kann dazu beitragen, die Leistung des Mehrwertsteuerzahlungsverfahrens zu verbessern, indem der Buchhaltungswährungsbetrag und der Berichtswährungsbetrag auf Mehrwertsteuerzahlungsbelegzeilen, die dasselbe Hauptkonto, dieselbe Sachkontodimension und dieselbe Währung aufweisen, in einer Zeile zusammengefasst werden.

1. Wechseln Sie zu **Systemverwaltung** \> **Arbeitsbereiche** \> **Datenverwaltung**.
2. Suchen Sie auf der Registerkarte **Alle** nach **Leistungssteigerung bei der Umsatzsteuerzahlung** und wählen Sie es aus.
3. Wählen Sie **Aktivieren** aus.

### <a name="prevent-generation-of-offset-tax-transactions"></a>Die Generierung von verrechneten Steuertransaktionen verhindern

Standardmäßig bucht der Mehrwertsteuerzahlungsbeleg die Mehrwertsteuerbuchungen mit jeder Mehrwertsteuerbuchung, die im Mehrwertsteuerzahlungsverfahren abgerechnet wird. Diese verrechneten Umsatzsteuertransaktionen sind im **Umsatzsteuer-/Ledger-Abstimmung** Prüfbericht enthalten. Sie zeigen den ausstehenden Saldo der Umsatzsteuertransaktionen, die während des Zeitraums nicht beglichen wurden.

Allerdings können die aufgerechneten Umsatzsteuertransaktionen die Belastung des Umsatzsteuerzahlungsverfahrens erhöhen. Daher kann ein Flighting namens **TaxReportGenOffsetTaxTransPerRecordSetFlighting** bei Bedarf aktiviert werden. Dieses Flighting kann dazu beitragen, die Leistung der Generierung von Ausgleichssteuertransaktionen für Länder und Regionen mit Ausnahme von Thailand, Polen, Ungarn, Litauen, Malaysia, Indien, Italien, Russland, der Tschechischen Republik, Estland und Lettland zu verbessern.

> [!NOTE]
> Wenn die Steuertransaktionstabelle angepasste Felder enthält, kann das Flighting nicht aktiviert werden.

Da der **Umsatzsteuer-/Ledger-Abstimmung**-Bericht im Allgemeinen nur für interne Kontrollzwecke verwendet wird und in vielen Steuersystemen nicht erforderlich ist, können Sie sich entscheiden, keine Offset Umsatzsteuertransaktionen auf dem Umsatzsteuerzahlungsbeleg zu generieren.

1. Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuer-Abrechnungszeiträume**.
2. Wählen Sie eine Ausgleichsperiode aus.
3. Stellen Sie im Inforegister **Allgemein** die Option **Verhindern, dass Steuerverrechnungstransaktionen generiert werden** auf **Ja**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
