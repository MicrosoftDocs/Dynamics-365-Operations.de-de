---
title: "Ausführen einer Debitorenrückerstattung"
description: "In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden. Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f8a46f5d961ff7629db7f9af8f3955ddfc338736
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="reimburse-customers"></a>Ausführen einer Debitorenrückerstattung

[!include[banner](../includes/banner.md)]


In diesem Thema wird erläutert, wie Rückerstattungstransaktlionen für eine Debitorengruppe erstellt werden. Wenn ein Debitor über ein Guthaben verfügt, können Sie dem Debitor den Betrag des Saldos rückerstatten. 

In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.

| Voraussetzung                                                            | Beschreibung                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Legen Sie den Mindest-Rückerstattungsbetrag für die juristische Person fest.          | Geben Sie auf der Seite **Debitorenkontenparameter** im Bereich **Allgemeines** im Feld **Mindestrückerstattung** den Mindestbetrag für die Überzahlungsrückerstattung an Debitoren ein. |
| Optional: Fügen Sie ein Kreditorenkonto für jeden Debitor hinzu, der Erstattungen erhalten kann. | Wählen Sie auf der Seite **Debitoren** auf dem Inforegister **Sonstige Details** im Feld **Kreditorenkonto** das Kreditorenkonto für den Debitor aus.                                           |

Wenn Sie Rückerstattungsbuchungen erstellen, wird eine Kreditorenrechnung für den Betrag des Saldo erstellt. Im Rahmen des Rückerstattungsprozesses wird das Saldo für das Debitorenkonto entfernt. Außerdem wird ein fälliger Saldo für das Kreditorenkonto erstellt, das dem Debitor entspricht.

1.  Führen Sie im Debitorenmodul den Prozess **Rückerstattung** aus.
2.  Führen Sie einen dieser Schritte aus:
    -   Klicken Sie zum Vornehmen einer Rückerstattung für bestimmte Debitorenkonten auf **Auswählen**, und geben Sie in der Abfrage die gewünschten Debitorenkonten an.
    -   Klicken Sie zum Vornehmen einer Rückerstattung für alle Konten auf **OK**.

    Die Habenbeträge werden auf die Kreditorenkonten der Debitoren überwiesen und als gewöhnliche Zahlungen behandelt. Ist für den Debitor kein Kreditorenkonto vorhanden, wird für diesen Debitor automatisch ein einmaliges Kreditorenkonto erstellt.
3.  Die erstellten Rückerstattungstransaktionen zeigen Sie auf der Seite **Rückerstattung** an.
4.  Im Kreditorenmodul erstellen Sie eine Zahlung für die Kreditorenrechnungen, die durch den Rückerstattungsprozess erstellt wurden.





