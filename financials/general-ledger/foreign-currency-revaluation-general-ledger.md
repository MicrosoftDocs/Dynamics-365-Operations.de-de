---
title: "Neubewertung der Fremdwährung für das Sachkonto"
description: "Dieses Thema enthält einen Überblick der folgenden Hauptbuchneubewertung für den der fremdwährungs-Prozess verfügbar - Dient zum Einrichten und den Vorgang ausführen, Berechnung für den Prozess und die Neubewertungsbuchungen, gegebenenfalls."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Neubewertung der Fremdwährung für das Sachkonto

Dieses Thema enthält einen Überblick der folgenden Hauptbuchneubewertung für den der fremdwährungs-Prozess verfügbar - Dient zum Einrichten und den Vorgang ausführen, Berechnung für den Prozess und die Neubewertungsbuchungen, gegebenenfalls. 

Als Teil eines Periodenende benötigen die Buchhaltungskonventionen Hauptbuchkontosalden in Fremdwährungen, um mithilfe der verschiedenen Wechselkurstypen (aktuell, historisch, durchschnittlich) neu bewertet werden zu können. Beispielsweise benötigt eine Buchhaltungskonvention Anlagen und Verbindlichkeiten, um zum aktuellen Wechselkurs,  Anlagen zum historischen Wechselkurs und GuV-Konten zum monatlichen Durchschnitt neu zu bewerten. Die Hauptbuchneubewertung der Fremdwährung kann verwendet werden, um die Bilanz und die GuV-Konten neu zu bewerten. 

> [!NOTE]
> Neubewertung der Fremdwährung wird auch im Debitoren- (AR) und im Kreditor (AP) verfügbar. Werden diese Module verwenden, sollten die ausstehende Buchungen mit der Neubewertung der Fremdwährung in diesen Modulen neu bewertet werden. Die Debitoren- Kreditoren-Neubewertung der Fremdwährung erstellt einen Buchhaltungseintrags im Hauptbuch, um den unrealisierten Gewinn oder der Verlust widerzuspiegeln und sicherzustellen, dass die untergeordneten Sachkonten mit dem Hauptbuch abgestimmt werden können. Da die Debitoren- und Kreditorenneubewertung der Fremdwährung Buchhaltungseinträge im Hauptbuch erstellen, sollten die Debitoren und Kreditorhauptkonten von der Hauptbuchneubewertung der Fremdwährung nicht berücksichtigt werden. 

Wird der Neubewertungsprozess ausgeführt, wird der Saldo für jedes Hauptkonto, das in einer Fremdwährung gebucht wird, neu bewertet. Die unrealisierten Gewinn- oder Verlusttransaktionen, die während des Neubewertungsprozesses erstellt werden, werden vom System generiert. Zwei Buchungen werden, eine für die Buchhaltungswährung und einer Sekunde für die Berichtswährung erstellt werden, falls relevant. Jeder Buchhaltungseintrags bucht den unrealisierten Gewinn oder der Verlust und das Hauptkonto, der neu bewertet wird.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Vorbereitungen, um die Neubewertung der Fremdwährung auszuführen
Bevor Sie den Neubewertungsprozess ausführen können, sind folgende Einstellungen erforderlich.

-   Auf der Seite **Hauptkonto**:
-   Wenn das Hauptkonto im Hauptbuch neu bewertet werden soll, wählen Sie **Neubewertung der Fremdwährung** aus. Wenn das Hauptkonto nicht neu bewertet wird (zum Beispiel für Debitor und Kreditor, wenn Sie in untergeordneten Sachkonten neu bewertet werden) deaktivieren Sie die Option.
-   Wenn das Hauptkonto für eine Neubewertung markiert wird, geben Sie **Wechselkurstyp** ein. Dieser Wechselkurstyp wird für die Neubewertung des Hauptkontos verwendet. Ein separates Feld **Rechnungslegungswechselkurstyp** ist für die Finanzberichterstellung verfügbar. Die zwei Felder werden nicht als synchron betrachtet und lassen es zu, dass verschiedene Wechselkurstypen für die Neubewertung und Finanzberichte verwendet werden.

-   Auf der Seite **Sachkonto**:
-   Geben Sie den **Wechselkurstyp** an. Wenn der Wechselkurstyp nicht im Hauptkonto definiert ist, wird dieser Wechselkurstyp für die Neubewertung der Fremdwährung verwendet.
-   Definieren Sie die Konten für realisierten Gewinn, realisierten Verlust, nicht realisierten Gewinn und den nicht realisierten Verlust für die Neubewertung der Währung an. Konten für realisierte Gewinne und Verluste werden verwendet, wenn Debitoren- und Kreditoren-Ausgleichstransaktionen und realisierte Gewinne und Verluste für die Neubewertung offener Transaktionen und Hauptbuch-Hauptkonten verwendet werden.

-   Auf der Seite **Währungsneubewertungskonten**:
-   Wählen Sie unterschiedliche Währungsneubewertungskonten für jede Währung und jedes Unternehmen aus. Wenn keine Konten definiert werden, werden die Konten der **Sachkonto**-Seite verwendet.

## <a name="process-foreign-currency-revaluation"></a>Eine Neubewertung der Fremdwährung verarbeiten
Nachdem die Einstellung abgeschlossen ist, können Sie die Seite **Neubewertung der Fremdwährung** verwenden, um die Transaktionen und Salden der Hauptkonten neu zu bewerten. Sie können den Prozess in die Echtzeit ausführen oder ihn planen, damit er als Stapel ausgeführt wird. 

Auf der Seite **Neubewertung der Fremdwährung** werden die Neubewertungsprozesses jedes Verlaufs angezeigt, einschließlich Datum, als der Prozess ausgeführt wurde, welche Kriterien definiert wurden, ein Link zum Beleg, der für die Neubewertung erstellt wurde und ein Datensatz, wenn eine frühere Neubewertung storniert wurde. Um den Neubewertungsprozess auszuführen, klicken Sie auf die Schaltfläche **Neubewertung der Fremdwährung**. 

Die Werte **Von Datum** und **Bis Datum** definieren das Datumsintervall für die Berechnung des Fremdwährungssaldos, der neu bewertet wird. Wenn Sie GuV-Konten neu bewerten, wird die Summe aller Transaktionen, die im Datumsintervall auftreten, neu bewertet. Wenn Sie die Bilanzkonten neu bewerten, wird das Von-Datum ignoriert. Stattdessen wird der neu zu bewertende Saldo bestimmt, indem die Zeitspanne vom Datum zu Beginn des Geschäftsjahres bis zum Enddatum genommen wird. 

** Datum des Satzes ** verwendet werden, um zu definieren für das Datum kann der Wechselkurs, Standard soll. So können Sie die Salden zwischen den Datumsbereich aus dem 1. Januar bis zum 31. Januar neu bewertet werden, sondern können den Wechselkurs, der für den 1. Februar definiert wird. 

Wählen Sie, welche Hauptkonten neu bewertet werden sollen: Alle, Bilanz oder Gewinn und Verlust. Nur Hauptkonten, die für eine Neubewertung markiert werden (auf der Hauptkontoseite) neu bewertet werden. Wenn Sie weiter einschränken möchten, schränken Sie den Bereich von Hauptkonten verwenden, die Datensätze enthalten ** ** die Registerkarte, ein, um einen Bereich von Hauptkonten oder einzelner Hauptkonten zu definieren. 

Die Neubewertung kann für mindestens eine juristische Person ausgeführt werden. Die Suche werden nur die juristischen Personen, auf die Sie Zugriff haben. Hier können die juristischen Personen aus, für die der Neubewertungsprozess ausführen möchten. 

Die Neubewertung kann für eine oder mehrere Fremdwährung ausgeführt werden. Die Suche enthält alle Währungen, die innerhalb des festgelegten Datumsbereichs gebucht wurden, die für den Typ des Hauptkontos relevant ist (Bilanz oder Gewinn und Verlust), die für die juristischen Personen, die aktiviert werden, um den neu zu bewerten. Die Buchhaltungswährung ist in der Liste enthalten, jedoch kein Artikel wird neu bewertet, wenn die Buchhaltungswährung ausgewählt wird. 

Satz ** Vorschau vor der Buchung ** ** Ja ** wenn Sie das Ergebnis der Hauptbuchneubewertung prüfen möchten. Die Vorschau im Hauptbuch zu ist der Simulation in der Debitoren- und Neubewertung der Fremdwährung verwendet. Die Simulation in "Debitoren" und " Kreditor ist ein Bericht, doch das Hauptbuch ist eine Vorschau, die gebucht werden können, und die Mitarbeiter müssen, der Neubewertungsprozess erneut auszuführen. Die Ergebnisse der Vorschau können nach Microsoft Excel exportiert werden, um den Verlauf über die Berechnung der Beträge aufzubewahren. Sie können die Stapelverarbeitung nicht verwenden, wenn Sie die Ergebnisse der Neubewertung in der Vorschau anzeigen möchten. In der Vorschau hat der Benutzer die Option, die Ergebnisse aller juristischen Personen mithilfe der Schaltfläche **Buchen** zu buchen. Liegt ein Problem mit den Ergebnissen für eine juristische Person vor, hat der Benutzer die Option, eine Teilmenge der juristischen Personen mithilfe der Schaltfläche**Juristische Personen zum Buchen auswählen** zu verwenden. 

Nachdem der Neubewertung der Fremdwährung abgeschlossen ist, wird der Datensatz erstellt, um den Serviceverlauf ausgeführtem von jedem zu verfolgen.  Ein separater Datensatz wird für jede juristische Person erstellt und Buchungsebene.

## <a name="calculate-unrealized-gainloss"></a>Berechnen von unrealisierten Gewinnen/Verlusten
Die Buchungen des unrealisierten Gewinns/Verlusts erfolgen in der Hauptbuchneubewertung und im Neubewertungsprozess von Debitoren und Kreditoren unterschiedlich. Im Modul "Debitoren" und "Kreditoren" wird die vorherige Neubewertung abgeschlossen (vorausgesetzte, die Buchung ist noch nicht ausgeglichen) und eine neue Neubewertungsbuchung wird für den unrealisierten Gewinn/Verlust basierend auf dem neuen Wechselkurs erstellt. Dies ist erforderlich, weil jede einzelne Buchung in "Debitoren" und "Kreditoren" neu bewertet werden. Im Hauptbuch wird die vorherige Neubewertung nicht storniert. Stattdessen wird eine Abschreibungsbuchung für das Delta zwischen dem Saldo des Hauptkontos, einschließlich aller früheren Neubewertungsbeträge und der neue Wert wird anhand den Wechselkurs für das Datum des Nummernkreises erstellt. 

** B ** die folgenden Salden vorhanden für Hauptkonto 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Datum**   | **Sachkonto** | **Buchungsbetrag** | **Buchhaltungsbetrag** |
| 20. Januar | 110110 (Cash)      | 500 EUR (Debit)        | 1000 USD (Debit)      |

Das Hauptkonto wird am 31. Januar neu bewertet.  Der unrealisierte Gewinn/der Verlust wird wie folgt berechnet.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Aktueller Saldo in Buchungswährung** | **Aktueller Saldo in der Buchhaltungswährung** | **Wechselkurs für Neubewertung** | **Neuer Buchhaltungswährungsbetrag** | **Unrealisierter Gewinn/Verlust**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833.33 EUR (500 x 1.666667)        | 166.67 Verlust (833.33 – 1000) |

Der nächste Buchhaltungseintrag wird erstellt.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Datum**   | **Sachkonto**       | **Soll** | **Entlastung** |
| 31. Januar | 110110 (Cash)            |           | 166.67     |
| 31. Januar | 801400 (Unrealisierter Verlust) | 166.67    |            |

Keine neuen Buchungen werden für den Monat Februar gebucht.  Das Hauptkonto wird am 28. Februar neu bewertet.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Aktueller Saldo in Buchungswährung** | **Aktueller Saldo in der Buchhaltungswährung** | **Wechselkurs für Neubewertung** | **Neuer Buchhaltungswährungsbetrag** | **Unrealisierter Gewinn/Verlust**    |
| 500 EUR                                     | 833.33 USD (1000 - 166.67)                 | 250.0000                         | 1250 USD (500 x 2.5)               | 416.67 Gewinn (1250 – 833.33) |

Der nächste Buchhaltungseintrag wird erstellt.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Datum**    | **Sachkonto**       | **Soll** | **Entlastung** |
| 28. Februar | 110110 (Cash)            | 416.67    |            |
| 28. Februar | 801600 (Unrealisierter Gewinn) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Neubewertung der Fremdwährung stornieren
Wenn Sie die Neubewertungsbuchung stornieren müssen, wählen Sie die Schaltfläche **Buchung stornieren** auf der Seite **Neubewertung der Fremdwährung** aus. Es wird eine neue Neubewertung der Fremdwährung des historischen Datensatzes erstellt, um den historischen Audit-Trail zum Zeitpunkt der Ausführung oder Stornierung zu erhalten. 

Sie können die Ergebnisse eines veralteten Auftrags der Neubewertung stornieren, jedoch müssen Sie möglicherweise eine aktuellere Neubewertung auch storniert, um die richtigen Salden für jedes neu vorkalkulierte Hauptkonto ein. Neu bewertet, werden die Rückbuchungen möglich veralteter Auftrag, da keine Möglichkeit besteht, Steuern, welcher Hauptkonten und die Häufigkeit wenn er neu bewertet werden. So kann eine Organisation hat, um alle anderen Monats Hauptkonten vierteljährlich neu bewerten, aber die Bargeldhauptkonten.


