---
title: Ausführen einer Debitorenrückerstattung
description: In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden. Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten.
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65ee884fb22c1a38e2d3022085fed7e3e6077d1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644536"
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
