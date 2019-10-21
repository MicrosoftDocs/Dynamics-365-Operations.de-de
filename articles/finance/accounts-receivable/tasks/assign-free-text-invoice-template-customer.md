---
title: Einem Debitor eine Freitextrechnungsvorlage zuweisen
description: In dieser Aufgabe wird dargestellt, wie Sie eine Freitextrechnungsvorlage zu einem Debitor zuweisen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9535a4678ea0c68227a54cf3c5d1b06b116a288
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177955"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Einem Debitor eine Freitextrechnungsvorlage zuweisen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dieser Aufgabe wird dargestellt, wie Sie eine Freitextrechnungsvorlage zu einem Debitor zuweisen. Für diese Aufgabe wird das USMF-Demounternehmen verwendet und die Erfassung ist für den Benutzer bestimmt, der für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.

1. Wechseln Sie im **Navigationsbereich** zu **Module > Debitoren > Debitoren > Alle Debitoren**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie im **Aktivitätsbereich** auf **Rechnung**.
4. Klicken Sie auf **Serienrechnungen**. Mithilfe dieser Seite können Sie Debitoren Freitextrechnungsvorlagen zuweisen und angeben, wie häufig Rechnungen an den Debitor gesendet werden sollen.  
5. Klicken Sie auf **Neu**, um eine neue Vorlage zum Debitor zuzuweisen.
6. Wählen Sie im Feld **Vorlage** die Freitextrechnungsvorlage aus, die dem Debitor zugewiesen werden soll.
7. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
8. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
9. Geben Sie im Feld **Startdatum der Fakturierung** das Datum ein, an dem die erste Rechnung generiert wird.
10. Geben Sie im Abschnitt **Ende der Serie** ein wiederkehrendes Enddatum ein.  
    * Wählen Sie eine der folgenden Optionen: Kein Enddatum – Es werden so lange Rechnungen generiert, bis die Vorlage aus dem Debitorenkonto entfernt wird.
    * Enddatum der Fakturierung – Wählen Sie diese Option aus, und geben Sie das letzte Datum ein, an dem eine Rechnung generiert werden kann.  
11. Geben Sie im Feld **Maximaler kumulierter Betrag** den maximalen kumulierten Betrag ein, nach dem die Rechnungsgenerierung stoppt. Geben Sie den maximalen kumulativen Betrag ein, der unter Verwendung der ausgewählten Vorlage erreicht werden kann. Beispiel: Wenn Sie in dieses Feld den Wert 1.000,00 eingeben und monatlich eine Rechnung über jeweils 100,00 Einheiten generieren, wird nach der zehnten Rechnung keine weitere Rechnung mehr generiert.  
12. Im Abschnitt **Serienrechnungen generieren mithilfe der Standardwerte aus** wählen Sie entweder die Freitextrechnungsvorlage oder das Debitorenkonto aus. Wählen Sie aus, ob die Standardwerte für Sprache, Buchungsprofil, Mehrwertsteuergruppe, Artikel-Mehrwertsteuergruppe, Listencode, Land/Region zur Lieferadresse, Währung, Zahlungsbedingungen, Zahlungsmethode, Zahlungsspezifikation, Zahlungsplan, Skonto, Finanzdimensionen und Giro-Überweisungsbeleg anhand der Freitext-Rechnungsvorlage oder des Debitorenkontos bestimmt werden.  
13. Im Feld **Wiederholungsmuster** wählen Sie das Wiederholungsmuster aus.
    + Täglich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Tagen ein. Beispiel: Wenn Sie 15 eingeben, wird für diesen Debitor alle 15 Tage eine Rechnung generiert.
    + Wöchentlich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Wochen ein. Beispiel: Wenn Sie 2 eingeben, wird für diesen Debitor alle zwei Wochen eine Rechnung generiert.
    + Monatlich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Monaten ein. Beispiel: Wenn Sie 6 eingeben, wird für diesen Debitor alle sechs Monate eine Rechnung generiert.
    + Jährlich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Jahren ein. Beispiel: Wenn Sie 2 eingeben, wird für diesen Debitor alle zwei Jahre eine Rechnung generiert.  
14. Geben Sie im Feld **Pro** eine Zahl ein.

