---
title: Hinzufügen der Informationen für das Debitorenkreditmanagement
description: In diesem Thema wird erläutert, wie Kreditverwaltungsinformationen für einen Debitor hinzugefügt werden.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dc734775e0ffe0388763d788a6eba90c1449ed1c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820592"
---
# <a name="add-credit-management-information-for-customers"></a>Hinzufügen der Informationen für das Debitorenkreditmanagement

[!include [banner](../includes/banner.md)]

Nachdem Sie die Parameter für das Kreditmanagement festgelegt haben, können Sie für jeden Debitor weitere Details hinzufügen. Diese Details steuern die Kreditverwaltungsprozesse und stellen zusätzliche Informationen bereit, mit deren Hilfe Mitglieder des Inkasso-Teams Debitoren verwalten können.

## <a name="customer-information"></a>Kundendaten

Sie können die Kundendaten auf dem Inforegister **Kredit und Inkasso** auf der Seite **Alle Debitoren** (**Debitorenbuchhaltung \> Debitoren \> Alle Debitoren**) hinzufügen.

1. Stellen Sie die Option **Unbegrenztes Kreditlimit** auf **Ja**, wenn der Debitor nicht durch Kreditlimitprüfungen eingeschränkt werden soll.
2. Stellen Sie die Option **Vom Kreditmanagement ausschließen** auf **Ja**, um den Kunden von allen Aktionen auszuschließen, die normalerweise während Kreditmanagementprozessen stattfinden.
3. Wählen Sie die Kreditverwaltungsgruppe für den Kunden aus.
4. Um das Kreditlimit in der Währung des Debitors zu berechnen, geben Sie im Feld **Kreditlimit in der Debitorwährung** das Kreditlimit des Debitors ein. Das Kreditlimit in der Firmenwährung wird mit den Wechselkursen umgerechnet, die durch den in den Kreditmanagementparametern ausgewählten Kreditlimit-Wechselkurstyp definiert sind.
5. Geben Sie im Feld **Datum der letzten Überprüfung** das Datum ein, an dem das Kreditlimit des Kunden zuletzt von einem Kreditmanager überprüft wurde.
6. Geben Sie im Feld **Nächstes geplantes Überprüfungsdatum** das Datum ein, an dem für den Debitor eine Kreditprüfung und -aktualisierung geplant ist.
7. Geben Sie im Feld **Zulässiges Kreditlimit** das höchste Kreditlimit ein, das dem Debitor basierend auf Ihrer Überprüfung des Kreditverlaufs dieses Debitors zugewiesen werden kann. Das zulässige Kreditlimit kann vom Kreditlimit auf dem Inforegister **Kredit und Inkasso** abweichen.
8. Geben Sie im Feld **Währung Zulässiges Kreditlimit** die Währung des zulässigen Kreditlimits ein.
9. Geben Sie im Feld **Datum Zulässiges Kreditlimit** das Datum ein, an dem das zulässige Kreditlimit erstellt wurde.
10. Geben Sie im Feld **Kreditkontostatus** den Kreditkontostatus des Debitors ein.
11. Geben Sie im Feld **Statusgrund** den Grund ein, der dem Kontostatus zugeordnet ist.
12. Stellen Sie die Option **Mit Agentur** auf **Ja**, um anzuzeigen, dass der Kunde derzeit einer Kreditagentur zugeordnet ist. Dieser Wert dient nur zu Informationszwecken. Er wird in keinem Kreditmanagementprozess verwendet.
13. Stellen Sie Option **Titel gehalten** auf **Ja**, um anzuzeigen, dass ein Titel für das Unternehmen gehalten wird. Dieser Wert dient nur zu Informationszwecken. Er wird in keinem Kreditmanagementprozess verwendet.
14. Geben Sie im Feld **Gründungsdatum** das Datum ein, an dem der Kunde seine Geschäftstätigkeit aufgenommen hat. Diese Informationen werden verwendet, wenn Risikobewertungen erstellt werden.
15. Geben Sie im Feld **Debitor seit** das Datum ein, an dem die ersten Transaktionen für den Debitor verarbeitet wurden. Diese Informationen werden verwendet, wenn Risikobewertungen erstellt werden.
16. Geben Sie Notizen ein, anhand derer das Kreditteam die Kreditwürdigkeit des Debitors weiter beurteilen kann.

Beachten Sie, dass einige der Informationen, die auf der Seite **Debitor** angezeigt werden, von einem anderen Prozess erstellt werden:

- Das Feld **Ablaufdatum für das Kreditlimit** zeigt das Datum an, an dem das Kreditlimit abläuft. Wenn Sie dieses Feld nicht festlegen, läuft das Kreditlimit des Debitors nicht ab.
- Das Feld **Datum Kreditlimit** zeigt das Datum an, an dem das Kreditlimit erstellt wurde. Dieses Feld wird aktualisiert, wenn das Kreditlimit angepasst wird.
- Temporäre Kreditlimits überschreiben das Kreditlimit eines Debitoren für einen Zeitraum. Sie werden anstelle des Kreditlimits zur Berechnung des Gesamtkreditlimits verwendet. Diese Informationen werden nur angezeigt, wenn ein Kreditlimit aktiv ist. Sie können temporäre Kreditlimits durch Kreditlimitanpassungen hinzufügen.
- Das Feld **Versicherung und Garantien** zeigt den Gesamtwert der Versicherung und Garantien an, die das Kreditlimit für den Debitor erhöhen können.
- Das Feld **Kreditlimit insgesamt** zeigt das endgültige Kreditlimit für den Debitor an. Das Gesamtkreditlimit umfasst Versicherungen und Garantien sowie temporäre Kreditlimits.

## <a name="temporary-credit-limits"></a>Temporäre Kreditlimits

Temporäre Kreditlimits überschreiben die Kreditlimits eines Debitoren für einen definierten Zeitraum. Sie können temporäre Kreditlimits durch Kreditlimitanpassungen hinzufügen. Mit Kreditlimitanpassungen können Kreditmanager die Kreditlimits und Ablaufdaten eines einzelnen Kunden, einer Kundengruppe oder aller Kunden über einen Buchungsprozess aktualisieren.

Sie können Einträge im Journal für die Kreditlimitanpassung auf der Seite **Kreditlimitanpassung** (**Kreditmanagement \> Kreditlimitanpassungen \> Kreditlimitanpassungen**) erstellen.

## <a name="create-insurance-policies-and-guarantees"></a>Versicherungspolicen und Garantien erstellen

Sie können eine oder mehrere Versicherungspolicen und Garantien für jeden Debitor erstellen. Sie können sie dann verwenden, um das Risiko zu berechnen, das Ihr Unternehmen eingeht, wenn es einem Debitor Kredite anbietet. Versicherungspolicen und Garantien können auch in das Kreditlimit für einen Debitor einbezogen werden.

Sie können Versicherungspolicen und Garantien auf der Seite **Alle Debitoren** (**Debitoren \> Debitoren \> Alle Debitoren**) erstellen. Wählen Sie einen Debitor und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Kreditmanagement** die Option **Versicherung und Garantien** aus.

> [!NOTE]
> Im folgenden Verfahren wählen Sie einen Versicherer oder Bürgen aus dem globalen Adressbuch aus. Bevor Sie mit diesem Verfahren beginnen, müssen Sie daher sicherstellen, dass die Versicherer und Bürgen dem globalen Adressbuch hinzugefügt wurden.

1. Geben Sie im Feld **Kennung** **Garantie** oder **Versicherung** ein.
2. Wählen Sie im Feld **Garantie/Versicherungstyp** eine der zuvor eingerichteten Garantie- oder Versicherungstypen aus.
3. Wählen Sie im Feld **Versicherer/Bürge** den Versicherer oder Bürgen aus dem globalen Adressbuch aus. 
4. Wenn Sie **Versicherung** im Feld **Bezeichner** ausgewählt haben, wählen Sie im Feld **Art der Versicherungsdeckung** einen der zuvor eingerichteten Deckungstypen aus. Sie können keinen Deckungstypen für eine Garantie auswählen.
5. Geben Sie im Feld **Kennung** die ID der Versicherung ein. Diese ID ist normalerweise eine Versicherungsnummer.
6. Geben Sie im Feld **Wirksam** das Startdatum der Versicherungspolice oder der Garantie ein.
7. Geben Sie im Feld **Ablauf** das Datum ein, an dem die Versicherungspolice oder die Garantie. abläuft.
8. Geben Sie im Feld **Wirksam** den Wert der Versicherungspolice oder der Garantie ein. Dieser Wert ist der volle Wert der Police.
9. Wählen Sie im Feld **Währung** die Währung des Versicherungswerts aus. 
10. Geben Sie im Feld **Kreditlimit aktualisieren** einen Prozentsatz zwischen **0** und **100** ein. Dieser Prozentsatz wird auf den Policewert angewendet, und der resultierende Betrag wird zur Erhöhung des Kreditlimits verwendet, das bei der Berechnung des Kreditlimits verwendet wird. Der berechnete Wert wird unter **Gesamtkreditlimit, Versicherung und Garantien** auf dem Inforegister **Kredit und Inkasso** auf der Seite **Debitoren** angelegt.

    Hier ist ein Beispiel:

    - Das Kreditlimit (A) beträgt 100.000.
    - Der Versicherungswert (B) beträgt 50.000.
    - Der Prozentsatz **Kreditlimit aktualisieren** (C) beträgt 50,00.
    
    In diesem Fall beträgt das effektive Kreditlimit 125.000 (= A + \[B × C \]).

11. Markieren Sie das Kontrollkästchen **In Risiko enthalten**, um das in Kreditlimitberechnungen verwendete Kreditlimit um den vollen Wert der Police zu verringern. Wenn dieses Kontrollkästchen aktiviert ist, wird der Wert berechnet, wenn der Prozentsatz **Kreditlimit aktualisieren** angegeben wird, nicht für Kreditlimitberechnungen verwendet.

    Hier ist ein Beispiel:

    - Das Kreditlimit (A) beträgt 100.000.
    - Der Versicherungswert (B) beträgt 50.000.
    - Der Prozentsatz **Kreditlimit aktualisieren** (C) beträgt 50,00.

    In diesem Fall beträgt das effektive Kreditlimit 125.000 (= A + \[B × C \]).
    
    Wenn Sie jedoch das Kontrollkästchen **In Risiko enthalten** aktivieren, wird der Wert **Kreditlimit aktualisieren** von 50.000 (= 50,00 Prozent von 100.000) entfernt, und der Risikowert beträgt 75.000 (= A + \[B × C \] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]