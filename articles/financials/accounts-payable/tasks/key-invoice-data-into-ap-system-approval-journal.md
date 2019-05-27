---
title: Entscheidende Rechnungsdaten im Kreditorensystem mithilfe der Genehmigungserfassung
description: Diese Aufgabenanleitung zeigt Ihnen an, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550373"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Entscheidende Rechnungsdaten im Kreditorensystem mithilfe der Genehmigungserfassung

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabenanleitung zeigt Ihnen an, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.


## <a name="create-and-post-and-invoice"></a>Erstellen und buchen und fakturieren
1. Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungsregister".
2. Klicken Sie auf "Neu".
3. Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf "Positionen", um das Register zu öffnen und Ausgabenpositionen einzugeben.
6. Wählen Sie einen Kreditor aus. Geben Sie beispielsweise US-104 ein oder wählen Sie es aus.
7. Geben Sie im Feld "Rechnung" einen Wert ein.
8. Geben Sie im Feld "Beschreibung" einen Wert ein.
9. Geben Sie im Feld "Kredit" eine Zahl ein.
10. Klicken Sie im Feld "Genehmigt von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
11. Heben Sie eine genehmigende Person hervor und klicken Sie auf "Auswählen", um die genehmigende Person auszuwählen.
12. Klicken Sie auf "Buchen".
13. Schließen Sie die Seite.
14. Schließen Sie die Seite.

## <a name="approve-an-invoice"></a>Genehmigen einer Rechnung
1. Wechseln Sie zu "Kreditoren" > "Rechnungen" > "Rechnungsgenehmigung".
2. Klicken Sie auf "Neu".
3. Wählen Sie den Namen der Rechnungsgenehmigungserfassung aus, den Sie benutzen möchten.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie auf Positionen, um eine Seite anzuzeigen, auf der Sie die Rechnungen auswählen können, die Sie genehmigen möchten.
6. Wählen Sie "Belege suchen" aus, um alle Rechnungen anzuzeigen, die zur Genehmigung bereit sind.
7. Markieren Sie die Rechnung, die Sie erstellt haben.
8. Klicken Sie auf Auswählen.
    * Die Belege, die Sie oben ausgewählt haben, werden auf diese Liste verschoben, nachdem Sie sie auswählen.  
9. Klicken Sie auf "OK".
10. Klicken Sie im auf das Kontonummernfeld, um ein Ausgabenkonto der Rechnung hinzuzufügen.
11. Geben Sie eine Kontonummer ein und bewegen Sie die Tabulatortaste vom Feld weg. Geben Sie beispielsweise "600120" ein.
12. Klicken Sie auf "Buchen".
13. Klicken Sie auf "Beleg", um die Einträge anzuzeigen, die gebucht wurden.
    * Das Konto "Rechnung mit ausstehender Genehmigung" wird zurückgesetzt und durch das tatsächliche Ausgabenkonto ersetzt.  

