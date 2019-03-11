---
title: Sachkonto-Erfassungstypen
description: In diesem Thema werden die Erfassungstypen beschrieben, die Sie für Finanzerfassungen einrichten können.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fff557d20a230922b5512aea9e49aa9993a694dd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308666"
---
# <a name="ledger-journal-types"></a>Sachkonto-Erfassungstypen

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Erfassungstypen beschrieben, die Sie für Finanzerfassungen einrichten können. Verwenden Sie die Seite **Erfassungsnamen**, um Erfassungen einzurichten, die Sie für Microsoft Dynamics 365 for Finance and Operations verwenden können.

| Journaltyp                      | Zweck                       | Transaktionen auf dieser Seite eingeben                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Zuweisung                        | Erstellen Sie Zuweisungsbuchungen in einer Zuordnungserfassung. Vor der Erstellung einer Zuordnungserfassung muss die Zuordnungsregel auf der Seite **Sachkonto-Zuordnungsregel** erstellt werden.      | Zuordnungsanforderung verarbeiten             |
| Genehmigung                          | Buchen Sie Kreditorenrechnungen, die für die entsprechenden Sachkonten genehmigt wurden.  | Rechnungsgenehmigungs-Erfassung                                       |
| Bankscheck-Rückbuchung               | Stornieren eines gebuchten Schecks. Wählen Sie die Option **Überprüfungsprozess für Zahlungsrückbuchungen verwenden** auf der Seite **Bargeld- und Bankverwaltungsparameter** aus, um diesen Erfassungstyp zu verwenden.   | Scheckrückbuchungen, Zahlungsrückbuchung                   |
| Bankeinzahlungsbeleg-Stornierung    | Stornieren eines Bankeinzahlungsbelegs. Wählen Sie die Option **Überprüfungsprozess für Bankeinzahlungsbeleg-Stornierungen verwenden** auf der Seite **Bargeld- und Bankverwaltungsparameter** aus, um diesen Erfassungstyp zu verwenden.   | Bankeinzahlungsbeleg-Stornierungen            |
| Budget                            | Verarbeiten von Budgetzuteilungen. Wählen Sie die Option **Budgetzuteilung aktivieren** auf der **Hauptbuchparameter**-Seite aus, um diesen Erfassungstyp zu verwenden. Die Budgeterfassungsjournaleinträge enthalten Informationen, die auf den Sachkonten basieren, die auf der Seite **Buchungsdefinitionen** definiert werden.                                                        |                                                                |
| Debitor nimmt Wechsel an  | Erstellen von Debitorakzeptanzbuchungen für Wechsel.             | Erfassung zum Ziehen von Wechseln, Erfassung zum erneuten Ziehen von Wechseln |
| Debitoren-Bankrimesse          | Erstellen einer Wechsel-Rimessedatei, die an die Bank Ihrer Organisation gesendet werden kann. Um diesen Erfassungstyp zu verwenden, deaktivieren Sie die **Automatischer Ausgleich**-Option auf der **Debitoren** **kontenparameter**-Seite.            | Geldtransfer                                                     |
| Debitor zieht Wechsel    | Erstellen von Buchungen für vom Debitor gezogene Wechsel. Um diesen Erfassungstyp zu verwenden, deaktivieren Sie die **Wechselziehungserfassung bei der Buchung von Rechnungen automatisch erstellen und buchen**-Option auf der **Zahlungsmethoden – Debitoren**-Seite.   | Erfassung zum Ziehen von Wechseln                                  |
| Debitorenzahlung                  | Erstellen von Buchungen für Debitorenzahlungen.                             | Zahlungserfassung             |
| Debitor protestiert Wechsel | Erstellen von Buchungen für vom Debitor protestierte Wechsel.                    | Erfassung zum Protestieren von Wechseln                               |
| Debitor zieht erneut Wechsel  | Erstellen von Buchungen für vom Debitor erneut gezogene Wechsel.                     | Erfassung zum erneuten Ziehen von Wechseln                                |
| Debitor gleicht Wechsel aus  | Erstellen von Buchungen für vom Debitor ausgeglichene Wechsel.                       | Erfassung zum Ausgleich von Wechseln                                |
| Täglich                             | Erstellen der täglichen Buchungen in einer allgemeinen Erfassung.                          | Allgemeine Erfassung                                                |
| Löschung                       | Erstellen von Löschungsbuchungen für eine Löschungserfassung. Um diesen Erfassungstyp zu verwenden, wählen Sie Optionen **Für finanziellen Löschungsprozess verwenden** und **Für finanziellen Konsolidierungsprozess verwenden** auf der **Juristische Personen**-Seite aus. Sie müssen eine Sachkonto-Löschungsregel auf der Seite **Sachkonto-Löschungsregel** erstellen, bevor Sie diesen Erfassungstyp verwenden können. | Löschung                                                    |
| Anlagenbudget                | Erstellen der Anlagenbudget-Registereinträge.                                                                                                                                                                                                                                                                                                                 | Anlagenbudget                                             |
| Rechnungsbuch                  | Erfassen Sie grundlegende Informationen zu Kreditorenrechnungen.                                                                                                                                                                                                                                                                                                           | Rechnungsbuch                                               |
| Lohnzahlung              | Geben Sie Zahlungen basierend auf Lohnlohnauszügen aus. Sie können Buchungen in dieser Erfassung nicht manuell eingeben. Sie müssen Lohnauszüge generieren und dann diese Aufstellungen für Zahlung übermitteln.                                                                                                                                                              |                                                                |
| Periodisch                          | Erstellen der periodischen Buchungen für die periodische Erfassung.                                                                                                                                                                                                                                                                                                      | Periodische Erfassungen                                              |
| Anlagen buchen                 | Ausführung von Anlagenbuchungen.                                                                                                                                                                                                                                                                                                                              | Feststehende Inhaltsteile                                                   |
| Projekt - Ausgaben                | Erstellen von Projektausgabenbuchungen.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Berichtswährungsregulierung     | Erstellen von Regulierungen in der Berichtswährung für Salden aus Sachkonten.               | Erfassungen der Berichtswährungsregulierung                         |
| Statistische Buchungen            | Erstellen statistischer Buchungen.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Kreditoren-Bankrimesse            | Erstellen einer Solawechsel-Rimessedatei, die an die Bank Ihrer Organisation gesendet werden kann.                                                                                                                                                                                                                                                                      | Rimesseerfassung                                             |
| Kreditorenzahlung               | Erstellen von Buchungen für Kreditorenzahlungen.                                                                                                                                                                                                                                                                                                                    | Zahlungserfassung                                                |
| Kreditor zieht Solawechsel       | Ziehen der Kreditorensolawechsel als Zahlungsmethode. Um diesen Erfassungstyp zu verwenden, deaktivieren Sie die **Wechselziehungserfassung bei der Buchung von Rechnungen automatisch erstellen und buchen**-Option auf der **Zahlungsmethoden – Kreditoren**-Seite.                                                                                                                                          | Erfassung zum Ziehen von Solawechseln                                   |
| Kreditorenrechnungspool ohne Buchung | Erstellen der Kreditorenrechnungsbuchungen, die noch nicht auf ein temporäres Eingangskonto gebucht wurden.                                                                                                                                                                                                                                                             | Kreditorenrechnungspool ohne Buchungsdetails                  |
| Kreditorenrechnungspool               | Erstellen von Buchungen für den Kreditorenrechnungspool.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Buchung der Kreditorenrechnung          | Buchen von Kreditorenrechnungen, die in einer Erfassung sind.                                                                                                                                                                                                                                                                                                                 | Rechnungserfassung                                                |
| Kreditor zieht erneut Solawechsel     | Erneutes Ziehen eines Solawechsels, der zuvor von der Bank der Organisation eingelöst wurde.                                                                                                                                                                                                                                                                      | Erfassung zum erneuten Ziehen von Solawechseln                                 |
| Kreditor gleicht Solawechsel aus     | Erstellen von Buchungen für vom Kreditor ausgeglichene Solawechsel.                                                                                                                                                                                                                                                                                                          | Erfassung zum Ausgleich von Solawechseln                                 |





