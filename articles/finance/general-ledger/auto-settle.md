---
title: Sachkontoabrechnungen automatisieren
description: Dieser Artikel enthält Informationen über den automatischen Sachkontoabrechnungsprozess.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708330"
---
# <a name="automate-ledger-settlements"></a>Sachkontoabrechnungen automatisieren

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 Finance Version 10.0.31 ist die Funktion  **Automatischer Sachkontoabrechnungsprozess** im Arbeitsbereich  **Funktionsverwaltung**  verfügbar. Sie können die Funktion **Automatischer Sachkontoabrechnungsprozess** nur aktivieren, wenn die Funktion **Zwischen Sachkontoabrechnung und Jahresabschluss** aktiviert wurde.

Die Hauptbuchabrechnung ist der Prozess des Abgleichs von Soll- und Haben-Transaktionen im Hauptbuch. Organisationen, die Aktivitäten zur Sachkontoabrechnung nach einem wiederkehrenden Zeitplan durchführen, können den Prozess jetzt automatisieren. Bei der automatischen Sachkontoabrechnung können eine Soll-Transaktion und eine Haben-Transaktion nur dann automatisch abgeglichen werden, wenn ihre Beträge in der Buchhaltungswährung gleich sind. Zum Beispiel kann ein Sollbetrag von $1,00 automatisch mit einem Habenbetrag von $1,00 abgeglichen werden. Ein Sollbetrag von 1,00 $ kann jedoch nicht automatisch mit zwei Gutschriften abgeglichen werden, die jeweils einen Wert von 0,50 $ haben. Ein teilweiser Abgleich von Beträgen aus Sachkonten wird nicht unterstützt.

Die Automatisierung der Sachkontoabrechnung definiert die folgenden Details:

- Wann werden Sachkontoabrechnungen ausgeführt
- Welche Kriterien werden verwendet, um die automatisch abzurechnenden Soll- und Habenbeträge abzugleichen?
- In welcher Reihenfolge die Sachkontoabrechnungen verarbeitet werden

## <a name="define-the-occurrence-of-ledger-settlements"></a>Definieren Sie das Auftreten von Sachkontoabrechnungen

Für die Automatisierung der Sachkontoabrechnung wird das Framework zur Prozessautomatisierung verwendet. Verschiedene Geschäftsprozesse verwenden dieses Framework, um die Wiederholung eines ausgewählten Prozesses zu definieren. Für Sachkontoabrechnungen gehen Sie zu  **Systemadministration \> Einrichtung \> Prozessautomatisierungen** oder **Hauptbuch \> Sachbuch Einrichtung \> Prozessautomatisierungen**.

Wählen Sie zunächst die Option **Neue Prozessautomatisierung erstellen**, und wählen Sie **Sachkontoabrechnungen**. Ein Assistent führt Sie dann durch den Prozess der Einrichtung der Automatisierung.

## <a name="general-page"></a>Allgemeine Seite

Auf der Seite **Allgemein** des Assistenten geben Sie den Namen der Sachkontoabrechnung ein, die Sie erstellen wollen. Wenn Ihre übereinstimmenden Belastungen und Gutschriften beispielsweise montags im Sachkonto verrechnet werden, geben Sie einen beschreibenden Namen ein, z.B. **Sachkontoabrechnung\_Mon**. Der von Ihnen eingegebene Name wird in der Spalte **Automatisierungsregel** auf der Seite **Sachkontoabrechnungen** angezeigt.

Die übrigen Einstellungen auf der Seite sind allgemeiner Art und definieren das Auftretensmuster für diese Version der Sachkontoabrechnungen. Wenn ein Ereignis beispielsweise für Montag vorgesehen ist, können Sie es so definieren, dass es wöchentlich ausgeführt wird, und Sie können Montag als den Wochentag auswählen, an dem es ausgeführt wird. Sie können auch einen frühen Zeitplan eingeben, z. B. 2:00 Uhr, damit die Prozessautomatisierung vor Beginn des nächsten Geschäftstages abgeschlossen ist. Wir empfehlen Ihnen, die Prozessautomatisierung so zu planen, dass sie außerhalb Ihrer normalen Arbeitszeiten durchgeführt wird. Auf diese Weise tragen Sie dazu bei, die Auswirkungen auf Ihre Mitarbeiter in der Buchhaltung während des Arbeitstages zu reduzieren.

Weitere Informationen zu den anderen Feldern auf der Seite **Allgemein** finden Sie in der Dokumentation zur Prozessautomatisierung.

## <a name="ledger-settlements-match-criteria-page"></a>Seite Sachkontoabrechnungen Abgleichskriterien

Die nächste Seite im Assistenten ist die Seite **Sachkontoabrechnungen - Abgleichskriterien** . Hier legen Sie die Hauptkonten fest, die in die Prozessautomatisierung einbezogen werden, sowie die Kriterien, die für die Ermittlung der übereinstimmenden Soll- und Habenbeträge verwendet werden.

### <a name="account-selection"></a>Kontoauswahl

Es werden die Hauptkonten angezeigt, die Sie zuvor als Sachkontoabrechnungen für die juristische Entität definiert haben. (Sie definieren Hauptkonten als Sachkontoabrechnungskonten unter **Hauptbuch \> Einrichtung des Hauptbuchs \> Parameter des Hauptbuchs \> Sachkontoabrechnungen**.)

### <a name="main-account-and-posting-layer"></a>Hauptkonto und Buchungsebene

Die Werte  **Hauptkonto** und **Buchungsebene** sind erforderliche Abgleichskriterien. Die Werte **Hauptkonto** und **Buchungsebene** der Sachkonto-Soll-Transaktion und der Sachkonto-Haben-Transaktion müssen übereinstimmen, um bei der automatischen Sachkontoabrechnung abgeglichen zu werden.

### <a name="posting-type"></a>Buchungstyp

Markieren Sie die Option **Buchungsart**, wenn die Ledger-Soll- und -Haben-Transaktionen die gleiche Buchungsart haben müssen, um bei der automatischen Sachkontoabrechnung abgeglichen zu werden.

### <a name="financial-dimensions"></a>Finanzdimensionen

Markieren Sie die Option **Finanzdimensionen**, wenn die Transaktionen des Hauptbuchs im Soll und im Haben dieselben finanziellen Dimensionen haben müssen, um bei der automatischen Sachkontoabrechnung abgeglichen zu werden. Wenn diese Option ausgewählt ist, müssen die Kriterien für die Werte der finanziellen Dimensionen in der Liste **Verfügbare finanzielle Dimensionen** ausgewählt werden. Die Liste **Verfügbare finanzielle Dimensionen** enthält nicht die Dimension des Hauptkontos, da diese automatisch als Teil der Abgleichskriterien erforderlich ist.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Anzeigen der Ergebnisse einer Sachkontoabrechnungs-Automatisierung

Nachdem die Automatisierungsserie für die Sachkontoabrechnung erstellt wurde, werden die Vorkommnisse für jede Sachkontoabrechnung in der Wochenansicht der Prozessautomatisierung angezeigt. Zusätzlich wird der Status jedes Auftretens angezeigt. Folgende Status werden verwendet:

- **Geplant** - Die Automatisierung ist geplant, aber sie wurde noch nicht ausgeführt.
- **Ausgeführt** - Die Automatisierung wird gerade ausgeführt.
- **Fehler** - Die Automatisierung wurde ausgeführt, aber es ist ein Fehler aufgetreten. Sie können die Fehler anzeigen, indem Sie die Schaltfläche **Ergebnisse anzeigen** wählen.
- **Erledigt** - Die Automatisierung wurde erfolgreich ausgeführt. Sie können die Ergebnisse der Sachkontoabrechnung auf der Seite **Sachkontoabrechnungen** einsehen.

Um die Abgleichsergebnisse zu sehen, gehen Sie zu **Hauptbuch \> Periodische Aufgaben \> Sachkontoabrechnungen**. Das Feld **Automatisierungsregel** auf der Seite **Sachkontoabrechnungen** zeigt den Namen der geplanten Aufgabe für die automatisierte Sachkontoabrechnung an, die zur Abrechnung der Transaktion verwendet wurde. Bei erfolglosen Abrechnungsversuchen wird der Wert **Automatisierungsregel** nicht aktualisiert. Wenn Sie eine Transaktion, die zuvor erfolgreich durch den Automatisierungsprozess abgerechnet wurde, manuell stornieren, wird der Wert **Automatisierungsregel** entfernt.

Das Feld **Datum der Abrechnung** für die abgeglichenen Datensätze zeigt das Datum an, an dem der Automatisierungsprozess durchgeführt wurde.

## <a name="editing-a-ledger-settlement-automation"></a>Bearbeiten einer Sachkontoabrechnungs-Automatisierung

Mit dem Framework für die Prozessautomatisierung können Sie die Serien und die Vorkommen bearbeiten, die für die Sachkontoabrechnung erstellt werden. Die Serien können entweder auf der Seite  **Prozessautomatisierung**  oder in der Wochenansicht der Prozessautomatisierung bearbeitet werden. Wenn der Manager z.B. beschließt, die Sachkontoabrechnung am Mittwoch statt am Montag durchzuführen, kann er in der Wochenansicht ein Vorkommnis suchen und **Betrachten/Bearbeiten - Serie** wählen.

Wenn Sie eine Serie bearbeiten, werden Sie aufgefordert, anzugeben, ob die Änderung für alle bestehenden Ereignisse oder nur für neue Ereignisse gelten soll. Historische Vorgänge, die bereits den Status **Abgeschlossen** haben oder mit einem  **Fehler** -Status endeten, werden nicht geändert.

Sie können auch ein neues Vorkommen hinzufügen oder ein vorhandenes Vorkommen ändern. Zum Beispiel soll die nächste Sachkontoabrechnung am Mittwoch, den 1. Januar ausgeführt werden, aber dieses Datum ist ein Feiertag. Sie können das Ereignis entweder von der Seite **Prozessautomatisierung** oder von der Wochenansicht der Prozessautomatisierung aus ändern. Es wird eine Seite geöffnet, die die Details des Zeitplans und die Abgleichskriterien anzeigt. Hier können Sie die geplante Uhrzeit und das Datum bearbeiten. Sie können auch die Abgleichskriterien bearbeiten, wenn Änderungen erforderlich sind. 

Sie können auch ein Ereignis oder eine Serie deaktivieren. Um ein Ereignis zu deaktivieren und die Verarbeitung dafür auszusetzen, markieren Sie es in der Wochenansicht der Prozessautomatisierung und wählen dann **Deaktivieren**. Sie können eine Serie auf der Seite **Prozessautomatisierung** deaktivieren.

## <a name="security-for-ledger-settlement-automation"></a>Sicherheit für die Automatisierung der Sachkontoabrechnung

Die **Serieneinstellungen für die Automatisierung von Sachkontoabrechnungen pflegen** wurde den Rollen Buchhaltungsmanager und Buchhaltungsleiter hinzugefügt, und die **Serieneinstellungen für die Automatisierung von Sachkontoabrechnungen anzeigen** wurde den Rollen Buchhalter, Buchhaltungsmanager und Buchhaltungsleiter für die Automatisierung von Sachkontoabrechnungen hinzugefügt. Diese Aufgaben sind die Standard-Sicherheitseinstellungen, können aber entsprechend den Anforderungen Ihres Unternehmens geändert werden.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Allgemeine Hauptbuch-Parameter für die Automatisierung der Sachkontoabrechnung

Das Feld **Abrechnungstypischer Saldo** gibt die Reihenfolge an, in der die automatische Sachkontoabrechnung verarbeitet wird. Um den Wert **Abrechnung typischer Saldo** festzulegen oder anzuzeigen, gehen Sie auf **Hauptbuch \> Einrichtung \> Sachkonto-Parameter** und wählen Sie die Registerkarte **Sachkontoabrechnungen**.

Wenn **Soll** ausgewählt ist, beginnt der automatische Sachkontoabrechnungsprozess auf der Sollseite und sucht nach entsprechenden Gutschriften. Wenn **Kredit** ausgewählt ist, beginnt der automatisierte Sachkontoabrechnungsprozess auf der Habenseite und sucht nach den entsprechenden Sollseiten. Diese Option sollte den typischen Saldo des Hauptkontos widerspiegeln.

## <a name="processing-a-ledger-settlement-automation"></a>Verarbeiten einer Sachkontoabrechnungs-Automatik

Wenn die Automatisierung ausgeführt wird, wählt das System die Transaktionen für die Sachkonten aus, die für die Prozessautomatisierungsserie definiert sind. Es ordnet die Transaktionen nach Datum, indem es einen Datumsbereich vom Beginn des Geschäftsjahres bis zu dem Datum verwendet, an dem die Prozessautomatisierung ausgeführt wird. Der Abgleich basiert auf den angegebenen Abgleichskriterien. Die absoluten Werte der Buchhaltungswährungsbeträge von Soll und Haben müssen übereinstimmen, damit der Abgleich erfolgt.

Während ein Hauptkonto durch eine Sachkontoabrechnungsautomatisierung verarbeitet wird, können Sie es nicht auf der Seite **Sachkontoabrechnungen** anzeigen. Sie müssen warten, bis der Automatisierungsprozess abgeschlossen ist. Wir empfehlen Ihnen, die Prozessautomatisierung so zu planen, dass sie außerhalb der Arbeitszeiten ausgeführt wird, um Konflikte zu vermeiden.

Der Automatisierungsprozess umfasst alle Transaktionen, die die Kriterien erfüllen, mit Ausnahme der Transaktionen, die auf der Seite **Sachkontoabrechnungen** manuell zur Abrechnung markiert wurden.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Stornierung von Transaktionen, die durch den Automatisierungsprozess abgerechnet werden

Sie können eine Abrechnung stornieren, die durch den automatisierten Sachkontoabrechnungsprozess durchgeführt wurde. Wenn eine Transaktion, die durch den Automatisierungsprozess abgerechnet wurde, storniert wird, wird der Wert **Automatisierungsregel** entfernt.
