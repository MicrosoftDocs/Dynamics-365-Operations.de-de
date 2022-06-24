---
title: Ausführen einer Debitorenrückerstattung
description: In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 892b089edb16ba560f588c086d37faafdf16958d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891781"
---
# <a name="reimburse-customers"></a>Ausführen einer Debitorenrückerstattung

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden. Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten. 

In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.

| Voraussetzung                                                            | Beschreibung |
|-------------------------------------------------------------------------|-------------|
| Legen Sie den Mindest-Rückerstattungsbetrag für die juristische Person fest.          | Geben Sie auf der Seite **Debitorenkontenparameter** im Bereich **Allgemeines** im Feld **Mindestrückerstattung** den Mindestbetrag für die Überzahlungsrückerstattung an Debitoren ein. |
| Optional: Fügen Sie ein Kreditorenkonto für jeden Debitor hinzu, der Erstattungen erhalten kann. | Wählen Sie auf der Seite **Debitoren** auf dem Inforegister **Sonstige Details** im Feld **Kreditorenkonto** das Kreditorenkonto für den Debitor aus. |

Wenn Sie Rückerstattungsbuchungen erstellen, wird eine Kreditorenrechnung für den Betrag des Saldo erstellt. Im Rahmen des Rückerstattungsprozesses wird das Saldo für das Debitorenkonto entfernt. Außerdem wird ein fälliger Saldo für das Kreditorenkonto erstellt, das dem Debitor entspricht.

1. Führen Sie in der Debitorenbuchhaltung den **Rückerstattung**-Prozess (**Debitoren \> Periodische Aufgaben \> Rückerstattung**) aus.
2. Um alle Transaktionen unabhängig von den Hauptbuchdimensionen zu gruppieren, legen Sie die **Debitor zusammenfassen** Option auf **Ja** fest. Um nur Transaktionen mit ähnlichen Sachkontodimensionen zu gruppieren, setzen Sie die Option auf **Nein**.
3. Wählen Sie **Debitoren mit ausstehenden Habentransaktionen einschließen** aus, um Debitoren auszuwählen, deren Abbuchungsbeträge nicht abgewickelt wurden.
4. Um bestimmte Debitorenkonten zu erstatten, wählen Sie auf dem Inforegister **Einzuschließende Datensätze** die Option **Filtern** aus, und geben Sie dann die Debitorenkonten in der Abfrage an.

    Die Habenbeträge werden auf die Kreditorenkonten der Debitoren überwiesen und als gewöhnliche Zahlungen behandelt. Ist für den Debitor kein Kreditorenkonto vorhanden, wird für diesen Debitor automatisch ein einmaliges Kreditorenkonto erstellt.

5. Um die erstellten Erstattungstransaktionen anzuzeigen, verwenden Sie den Bericht **Rückerstattung** (**Debitoren \> Anfragen und Berichte \> Erstattungsbericht**).
6. Im Kreditorenmodul erstellen Sie eine Zahlung für die Kreditorenrechnungen, die durch den Rückerstattungsprozess erstellt wurden. Informationen zum Bezahlen von Kreditoren finden Sie unter [Übersicht über Kreditorenzahlungen](../accounts-payable/Vendor-payments-workspace.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
