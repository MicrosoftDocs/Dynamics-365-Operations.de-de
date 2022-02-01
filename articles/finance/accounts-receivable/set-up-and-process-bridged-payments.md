---
title: Transferzahlungen einrichten und verarbeiten
description: Dieses Thema erklärt, wie Sie Kundentransferzahlungen einrichten und verarbeiten. Eine Transferzahlung ist eine Zahlung, die in zwei Schritten in das Hauptbuch gebucht wird.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1418e573f34fadcf0bebc7232d847ee7e9768b
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014050"
---
# <a name="set-up-and-process-bridged-payments"></a>Transferzahlungen einrichten und verarbeiten

[!include [banner](../includes/banner.md)]

Eine Transferzahlung ist eine Zahlung, die in zwei Schritten in das Hauptbuch gebucht wird. Normalerweise wird dieser Ansatz verwendet, wenn die Zahlungsmethode auf **Bank** festgelegt ist, und Sie Transaktionen erst dann auf das Bankkonto buchen müssen, wenn die Transaktion von der Bank freigegeben wurde. Sie können sie jedoch auch für ein Sachkonto verwenden. In diesem Fall verschiebt das System den Betrag bei der Verarbeitung der Transferbuchung von einem Hauptkonto auf ein anderes Hauptkonto.

Sie können Transferzahlungen entweder aus der Kreditorenbuchhaltung oder aus der Debitorenbuchhaltung erstellen. Obwohl in diesem Thema erläutert wird, wie Transferbuchungen für Debitorenkonten konfiguriert werden, sind die Schritte für Kreditorentransaktionen ähnlich.

## <a name="set-up-bridging-posting"></a>Einrichten von Transferbuchung

Um die Transferbuchung zu verwenden, müssen Sie eine oder mehrere Zahlungsmethoden einrichten, damit sie die **Transferbuchung**-Methode verwenden. Sie müssen dann ein Transferkonto auswählen.

1. Wechseln Sie zu **Debitoren &gt; Zahlungseinstellungen &gt; Zahlungsmethoden**.
2. Wählen Sie eine vorhandene Zahlungsmethode aus, für die die Transferbuchung aktiviert werden soll. Erstellen Sie alternativ eine neue Zahlungsmethode.
3. Aktivieren Sie das Kontrollkästchen **Transferbuchung**.
4. Wählen Sie im Feld **Transferkonto** das Hauptkonto aus, auf das Zahlungen gebucht werden sollen, bevor sie auf dem Bankkonto verrechnet werden.
5. Schließen Sie die Seite.

## <a name="process-and-transfer-bridging-posting"></a>Transferbuchung bearbeiten und umbuchen

Befolgen Sie diese Schritte, um Transferbuchungen zu erstellen und zu verarbeiten.

1. Gehen Sie zu **Debitorenkonten &gt; Zahlungen &gt; Kundenzahlungserfassung**.
2. Wählen Sie **Neu** aus, um eine Erfassung zu erstellen.
3. Wählen Sie im Feld **Name** einen Namen aus.
4. Fügen Sie der Erfassung für Debitorenzahlungen Position hinzu und wählen Sie die Zahlungsmethode aus, die für die Transferbuchung konfiguriert ist.
5. Erfassung buchen. Die Transaktionen werden auf das Hauptkonto gebucht, das Sie im Feld **Transferkonto** im vorherigen Verfahren ausgewählt haben.

Wenn die Transaktionen bei der Bank abgerechnet wurden und Sie die Zahlung vom Transferkonto auf das Zahlungskonto überweisen möchten, das für die Zahlungsmethode angegeben ist, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Hauptbuch &gt; Journaleinträge &gt; Allgemeine Erfassungen**.
2. Wählen Sie **Neu** aus, um eine Erfassung zu erstellen.
3. Wählen Sie im Feld **Name** einen Namen aus.
4. Wählen Sie **Positionen** aus, um die Erfassungsdetails zu öffnen.
5. Wählen Sie **Funktionen &gt; Transferbuchungen auswählen** aus.
6. Markieren Sie jede verrechnete Zahlung und wählen Sie dann **Akzeptieren** aus.
7. Erfassung buchen.
