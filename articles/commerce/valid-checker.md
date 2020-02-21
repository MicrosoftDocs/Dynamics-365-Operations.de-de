---
title: Konsistenzprüfung für Einzelhandelstransaktionen
description: In diesem Thema werden die Funktionen der Konsistenzprüfung für Transaktionen in Dynamics 365 Commerce beschrieben.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3da8bdf6feb932e074680b6cb80e1b7b71f9a82b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004250"
---
# <a name="retail-transaction-consistency-checker"></a>Konsistenzprüfung für Einzelhandelstransaktionen


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

In diesem Thema werden die Funktionen der Konsistenzprüfung für Transaktionen in Microsoft Dynamics 365 Commerce beschrieben. Die Konsistenzprüfung ermittelt und isoliert inkonsistente Transaktionen, bevor sie im Aufstellungsbuchungsprozess verarbeitet werden.

Wird eine Aufstellung gebucht, kann die Buchung aufgrund der inkonsistenten Daten in den Handelstransaktionstabellen fehlschlagen. Die Datenfehler können durch unvorhergesehene Probleme in der Verkaufsstellenanwendung oder durch Fehler beim Importieren von Buchungen aus POS-Systemen von Drittanbietern auftreten. Im Folgenden sind Beispiele für diese Inkonsistenzen aufgeführt: 

- Der Transaktionsgesamtbetrag in der Kopftabelle entspricht nicht dem Transaktionsgesamtbetrag der Positionen.
- Die Positionsanzahl in der Kopftabelle entspricht nicht der Anzahl von Positionen in der Transaktionstabelle.
- Die Steuern in der Kopftabelle stimmen nicht mit dem Steuerbetrag in den Positionen überein. 

Wenn inkonsistente Transaktionen durch den Aufstellungsbuchungsprozess verarbeitet werden, werden inkonsistente Verkaufsrechnungen und Zahlungserfassungen erstellt, und der gesamte Aufstellungsbuchungsprozess schlägt anschließend fehl. Das Wiederherstellen der Aufstellungen aus einem solchen Zustand umfasst komplexe Datenkorrekturen in mehreren Transaktionstabellen. Die Konsistenzprüfung für Transaktionen verhindert solche Probleme.

Das folgende Diagramm veranschaulicht den Buchungsprozess mit Transaktionskonsistenzprüfung.

![Aufstellungsbuchungsprozess mit der Transaktionskonsistenzprüfung](./media/validchecker.png "Aufstellungsbuchungsprozess mit der Konsistenzprüfung für Einzelhandelstransaktionen")

Der Stapelverarbeitungsvorgang **Geschäftsbuchungen überprüfen** prüft die Konsistenz der Handelstransaktionstabellen in folgenden Szenarien.

- **Debitorenkonto** – Überprüft, dass das Debitorenkonto in den Transaktionstabellen in den HQ-Debitorenmasterdaten vorhanden ist.
- **Positionsanzahl** – Prüft, ob die Positionsanzahl, wie in der Tabelle in der Transaktionskopfzeile angegeben, mit der Anzahl der Positionen in den Verkaufstransaktionstabellen übereinstimmt.
- **Preis enthält Steuern**: Prüft, ob der Parameter **Preis enthält Steuern** über alle Transaktionspositionen konsistent ist.
- **Zahlungsbetrag**: Prüft, ob die Zahlungsdatensätze dem Zahlungsbetrag im Kopf entsprechen.
- **Bruttobetrag**: Prüft, ob der Bruttobetrag in der Kopfzeile mit der Summe der Nettobeträge der Positionen zuzüglich des Steuerbetrags identisch ist.
- **Nettobetrag**: Prüft, ob der Nettobetrag in der Kopfzeile mit der Summe der Nettobeträge der Positionen identisch ist.
- **Unter-/Überzahlung**: Prüft, ob die Differenz zwischen dem Bruttobetrag in der Kopfzeile und dem Zahlungsbetrag nicht die maximale Unter- bzw. Überzahlungskonfiguration übersteigt.
- **Rabattbetrag** – Prüft, ob der Rabattbetrag in den Rabatttabellen und der Rabattbetrag in den Tabellen mit den Transaktionspositionen konsistent ist und ob der Rabattbetrag aus der Kopfzeile der Summe der Rabattbeträge in den Positionen entspricht.
- **Positionsrabatt** – Prüft, ob der Positionsrabatt der Transaktionsposition der Summe aller Positionen in der Rabatttabelle entspricht, die sich auf die Transaktionsposition beziehen.
- **Geschenkkartenartikel** – Commerce unterstützt keine Rückgabe von Geschenkkartenartikeln. Allerdings kann der Wert einer Geschenkkarte bar ausgezahlt werden. Bei allen Geschenkkartenartikeln, die anstelle einer Barauszahlungsposition als Rückgabeposition verarbeitet werden, schlägt der Aufstellungsbuchungsprozess fehl. Bei der Validierung von Geschenkkartenartikeln wird sichergestellt, dass die einzigen Rückgabepositionsartikel der Geschenkkarte in den Transaktionstabellen Barauszahlungspositionen sind.
- **Negativer Preis** – Überprüft, dass es keine Transaktionspositionen mit negativen Preisen gibt.
- **Artikel und Variante**: Prüft, ob Artikel und Varianten aus den Transaktionspositionen in der Masterdatei mit Artikeln und Varianten vorhanden sind.
- **Steuerbetrag**: Prüft, ob die Steuerdatensätze den Steuerbeträgen in den Positionen entsprechen.
- **Seriennummer** - Überprüft, ob die Seriennummer in den Transaktionspositionen für Artikel vorhanden ist, die über die Seriennummer gesteuert werden.
- **Vorzeichen** - Überprüft, ob die Vorzeichen für die Menge und den Nettobetrag in allen Transaktionspositionen gleich sind.
- **Geschäftsdatum** – Prüft, ob die Finanzperioden für alle Geschäftsdaten der Transaktionen offen sind.

## <a name="set-up-the-consistency-checker"></a>Konsistenzprüfung einrichten

Konfigurieren Sie den Stapelverarbeitungsvorgang „Geschäftsbuchungen überprüfen“ unter **Retail und Commerce \> Retail und Commerce IT \> POS-Buchung**, sodass er regelmäßig ausgeführt wird. Der Batchauftrag kann basierend auf der Shoporganisationshierarchie in ähnlicher Weise wie die Funktionen zum Berechnen und Buchen im Stapel geplant werden. Es wird empfohlen, diesen Batchauftrag so zu konfigurieren, dass mehrmals am Tag ausgeführt wird, und ihn so zu planen, dass er am Ende jeder P-Auftragsausführung ausgeführt wird.

## <a name="results-of-validation-process"></a>Ergebnisse des Überprüfungsprozesses

Die Ergebnisse der Überprüfung durch den Stapelverarbeitungsvorgang werden in der entsprechenden Handelstransaktion markiert. Das Feld **Überprüfungsstatus** im Transaktionsdatensatz wird entweder auf **Erfolgreich** oder **Fehler** festgelegt und das Datum der letzten Prüfungsausführung wird im Feld **Uhrzeit der letzten Überprüfung** angezeigt.

Um eine ausführlichere Fehlerbeschreibung in Bezug auf einen Validierungsfehler zu erhalten, wählen Sie den entsprechenden Shoptransaktionsdatensatz aus und klicken auf die Schaltfläche **Überprüfungsfehler**.

Transaktionen mit Überprüfungsfehlern und noch nicht validierte Transaktionen werden nicht in Aufstellungen einbezogen. Während des Prozesses „Auszug berechnen“ werden Benutzer darüber informiert, wenn Transaktionen vorliegen, die in die Aufstellung aufgenommen hätten werden können, wo dies jedoch nicht der Fall war.

Wenn ein Überprüfungsfehler gefunden wird, können Sie ihn nur beheben, indem Sie sich an den Microsoft Support wenden. In einer zukünftigen Version werden Funktionen hinzugefügt, mit denen Benutzer die Fehler, die in der Benutzeroberfläche erfolgten, in den Datensätzen selbst beheben können. Es werden außerdem Protokollierungs- und Überwachungsfunktionen zur Nachverfolgung des Änderungsverlaufs bereitgestellt.

> [!NOTE]
> In zukünftigen Versionen werden zudem zusätzliche Validierungsregeln zur Unterstützung weiterer Szenarien hinzugefügt.
