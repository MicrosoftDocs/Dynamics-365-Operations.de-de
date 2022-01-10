---
title: Geschäftstransaktionen für die Aufstellungsberechnung validieren
description: In diesem Thema wird die Funktionalität zur Überprüfung von Geschäftstransaktionen in Microsoft Dynamics 365 Commerce beschrieben.
author: analpert
ms.date: 12/15/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 008368ae32aa92682d578b75b148e0587fcc94e0
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924770"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Geschäftstransaktionen für die Aufstellungsberechnung validieren

[!include [banner](includes/banner.md)]

In diesem Thema wird die Funktionalität zur Überprüfung von Geschäftstransaktionen in Microsoft Dynamics 365 Commerce beschrieben. Im Prüfungsprozess werden Transaktionen identifiziert und markiert, die Buchungsfehler verursachen, bevor sie vom Auszugsbuchungsprozess erfasst werden.

Wenn Sie versuchen, eine Anweisung zu buchen, kann der Prüfungsprozess aufgrund inkonsistenter Daten in den Handelstransaktionstabellen fehlschlagen. Im Folgenden finden Sie einige Beispiele für Faktoren, die diese Inkonsistenzen verursachen können:

- Der Transaktionsgesamtbetrag in der Kopftabelle entspricht nicht dem Transaktionsgesamtbetrag der Positionen.
- Die in der Kopfzeilentabelle angegebene Anzahl von Elementen stimmt nicht mit der Anzahl von Elementen in der Transaktionstabelle überein.
- Die Steuern in der Kopftabelle stimmen nicht mit dem Steuerbetrag in den Positionen überein. 

Wenn inkonsistente Transaktionen durch den Aufstellungsbuchungsprozess verarbeitet werden, können die erstellten Verkaufsrechnungen und Zahlungserfassungen für ein Fehlaschlagen des gesamten Aufstellungsbuchungsprozesses sorgen. Der Prozess **Geschäftsbuchungen überprüfen** verhindert diese Probleme, indem sichergestellt wird, dass nur Transaktionen, die die Transaktionsprüfungsregeln erfüllen, an den Transaktions-Aufstellungsberechnungsprozess weitergeleitet werden.

Die folgende Abbildung zeigt die wiederkehrenden Tagesprozesse zum Hochladen von Transaktionen, Prüfen von Transaktionen, Berechnen und Buchen von Transaktionsaufstellungen sowie die Tagesendprozesse zur Berechnung und Buchung von Finanzaufstellungen.

![Abbildung mit wiederkehrenden Tagesprozessen zum Hochladen von Transaktionen, Prüfen von Transaktionen, Berechnen und Buchen von Transaktionsaufstellungen sowie Tagesendprozesse zur Berechnung und Buchung von Finanzaufstellungen.](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Transaktionsprüfungsregeln speichern

Der Stapelverarbeitungsvorgang **Geschäftsbuchungen überprüfen** prüft die Konsistenz der Handelstransaktionstabellen basierend auf folgenden Überprüfungsregeln.

> [!NOTE]
> Prüfungsregeln werden weiterhin in nachfolgenden Versionen hinzugefügt.

### <a name="transaction-header-validation-rules"></a>Transaktionskopfzeilen-Prüfungsregeln

In der folgenden Tabelle sind die Transaktionskopfzeilen-Prüfungsregeln aufgeführt, die mit den Kopfzeilen von Einzelhandelstransaktionen verglichen werden, bevor diese Transaktionen an die Aufstellungsbuchung übergeben werden.

| Titel | Beschreibung |
|-------|-------------|
| Geschäftstermin | Diese Regel überprüft, ob das Geschäftsdatum der Transaktion mit einer offenen Buchhaltungsperiode im Sachkonto verknüpft ist. |
| Währungsrundung | Diese Regel überprüft, ob die Transaktionsbeträge gemäß der Währungsrundungsregel gerundet werden. |
| Kundenkonto | Diese Regel überprüft, ob der Kunde, der in der Transaktion verwendet wird, in der Datenbank vorhanden ist. |
| Rabattbetrag | Diese Regel prüft, ob der Rabattbetrag in der Kopfzeile mit der Summe der Rabattbeträge der Positionen übereinstimmt. |
| Buchungsstatus des Steuerbelegs (Brasilien) | Diese Regel überprüft, ob der Steuerbeleg erfolgreich gebucht werden kann. |
| Bruttobetrag | Diese Regel prüft, ob der Bruttobetrag in der Transaktionskopfzeile mit dem Nettobetrag, einschließlich Steuern, der Transaktionspositionen, zuzüglich Gebühren, übereinstimmt. |
| Netto | Diese Regel prüft, ob der Nettobetrag in der Transaktionskopfzeile mit dem Nettobetrag, ausgenommen Steuern, der Transaktionspositionen, zuzüglich Gebühren, übereinstimmt. |
| Netto + Steuern | Diese Regel prüft, ob der Bruttobetrag in der Transaktionskopfzeile mit dem Nettobetrag, ausgenommen Steuern, der Transaktionspositionen, zuzüglich aller Steuern und Gebühren, übereinstimmt. |
| Artikelanzahl | Diese Regel prüft, ob die Anzahl der Artikel, die in der Transaktionskopfzeile angegeben ist, mit der Summe der Mengen in den Transaktionspositionen übereinstimmt. |
| Zahlungsbetrag | Diese Regel prüft, ob der Zahlungsbetrag in der Transaktionskopfzeile der Summe aller Zahlungstransaktionen entspricht. |
| Steuerbefreiungsberechnung | Diese Regel prüft, ob die Summe des berechneten Betrags und des steuerbefreiten Betrags der Gebührenpositionen dem ursprünglich berechneten Betrag entspricht. |
| Preise inklusive Steuern | Diese Regel prüft, ob das Flag **Steuer ist in den Preisen enthalten** in allen Transaktionskopfzeilen und Steuertransaktionen konsistent ist. |
| Transaktion ist nicht leer | Diese Regel prüft, ob die Transaktion Positionen enthält und dass mindestens eine Position nicht storniert wird. |
| Unter-/Überzahlung | Diese Regel prüft, ob die Differenz zwischen dem Bruttobetrag und dem Zahlungsbetrag nicht die maximale Unter- bzw. Überzahlungskonfiguration übersteigt. |

### <a name="transaction-line-validation-rules"></a>Transaktionspositions-Prüfungsregeln

In der folgenden Tabelle sind die Transaktionspositions-Prüfungsregeln aufgeführt, die mit den Positionsdetails von Einzelhandelstransaktionen verglichen werden, bevor diese Transaktionen an die Aufstellungsbuchung übergeben werden.

| Titel | Beschreibung |
|-------|-------------|
| Strichcode | Diese Regel prüft, ob alle Artikelstrichcodes, die in den Transaktionspositionen verwendet werden, in der Datenbank vorhanden sind. |
| Gebührenpositionen | Diese Regel prüft, ob die Summe des berechneten Betrags und des steuerbefreiten Betrags der Gebührenpositionen dem ursprünglich berechneten Betrag entspricht. |
| Geschenkkartenretouren | Diese Regel prüft, ob bei der Transaktion keine Geschenkkarten zurückgegeben werden. |
| Artikelvariante | Diese Regel prüft, ob alle Artikel und alle Varianten, die in den Transaktionspositionen verwendet werden, in der Datenbank vorhanden sind. |
| Positionsrabatt | Diese Regel prüft, ob der Positionsrabattbetrag mit der Summe der Rabatttransaktionen übereinstimmt. |
| Positionssteuer | Diese Regel prüft, ob der Positionssteuerbetrag mit der Summe der Steuertransaktionen übereinstimmt. |
| Negativer Preis | Diese Regel prüft, dass keine negativen Preise bei Transaktionspositionen verwendet werden. |
| Seriennummer gesteuert | Diese Regel prüft, ob die Seriennummer in der Transaktionsposition für Artikel vorhanden ist, die über die Seriennummer gesteuert werden. |
| Seriennummer-Lagerungsdimension | Diese Regel prüft, dass keine Seriennummer angegeben wird, wenn die Seriennummerndimension des Artikels inaktiv ist. |
| Vorzeichenwiderspruch | Diese Regel prüft, ob die Vorzeichen für die Menge und den Nettobetrag in allen Transaktionspositionen gleich sind. |
| Steuerbefreiung | Diese Regel prüft, ob die Summe des Positionsartikelpreises und des steuerbefreiten Betrags dem ursprünglichen Preis entspricht. |
| Steuergruppenzuweisung | Diese Regel prüft, ob die Kombination der Mehrwertsteuergruppe und der Artikelsteuergruppe eine gültige Steuerschnittmenge ergibt. |
| Maßeinheitenkonvertierungen | Diese Regel prüft, ob die Maßeinheit aller Positionen eine gültige Konvertierung in die Maßeinheit des Lagerbestands aufweist. |

## <a name="enable-the-store-transaction-validation-process"></a>Shop-Transaktionsprüfungsprozess aktivieren

Konfigurieren Sie den Einzelvorgang **Geschäftsbuchungen überprüfen** (**Retail und Commerce \> Retail und Commerce IT \> POS-Buchung**) so in der Commerce-Zentralverwaltung, dass er regelmäßig ausgeführt wird. Der Batchauftrag wird basierend auf der Organisationshierarchie des Shops geplant. Wir empfehlen, dass Sie diesen Stapelverarbeitungsvorgang so konfigurieren, dass er mit der gleichen Häufigkeit ausgeführt wird wie die Batchaufträge **P-Auftrag** und **Transaktionsaufstellungen stapelweise berechnen**.

## <a name="results-of-the-validation-process"></a>Ergebnisse des Überprüfungsprozesses

Die Ergebnisse des Stapelverarbeitungsvorgangs **Geschäftsbuchungen überprüfen** können bei jeder Einzelhandelstransaktion angezeigt werden. Das Feld **Überprüfungsstatus** im Transaktionsdatensatz ist auf **Erfolgreich**, **Fehler** oder **Kein** festgelegt. Im Feld **Uhrzeit der letzten Überprüfung** wird das Datum der letzten Überprüfungsausführung angezeigt.

In der folgenden Tabelle werden die einzelnen Überprüfungsstatus beschrieben.

| Überprüfungsstatus | Beschreibung |
|-------------------|-------------|
| Erfolgreich | Alle aktivierten Überprüfungsregeln wurden bestanden. |
| Fehler | Eine aktivierte Überprüfungsregel hat einen Fehler festgestellt. Sie können weitere Details zum Fehler anzeigen, indem Sie im Aktionsbereich **Überprüfungsfehler** auswählen. |
| Kein | Für den Transaktionstyp müssen keine Überprüfungsregeln angewendet werden. |

![Seite „Geschäftstransaktionen“ mit dem Feld „Überprüfungsstatus“ und der Schaltfläche „Überprüfungsfehler“.](./media/valid-checker-validation-status-errors.png)

Es werden nur Transaktionen mit einem Überprüfungsstatus von **Erfolgreich** in die Transaktionsaufstellungen übernommen. Um Transaktionen anzuzeigen, die den Status **Fehler** haben, überprüfen Sie die Kachel **Fehler bei Abholungstransaktionsprüfung** im Arbeitsbereich **Finanzdaten für Shop**.

![Kacheln im Arbeitsbereich „Finanzdaten für Shop“.](./media/valid-checker-cash-carry-validation-failures.png)

Weitere Informationen zum Beheben von Fehlern bei Abholungstransaktionsprüfungen finden Sie unter [Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen](edit-cash-trans.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
