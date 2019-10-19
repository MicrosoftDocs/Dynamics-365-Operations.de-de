---
title: Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben
description: In diesem Thema wird erläutert, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177973"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben

[!include [task guide banner](../../includes/task-guide-banner.md)]

In diesem Thema wird erläutert, wie das Rechnungsregister verwendet wird, um Rechnungen zu erstellen und anschließend die Genehmigungserfassung verwendet wird, um die Ausgabenkonten zu aktualisieren.

## <a name="create-and-post-and-invoice"></a>Erstellen und buchen und fakturieren
1. Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungserfassung**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie den Namen des Rechnungsregisters aus, den Sie benutzen möchten.
4. Klicken Sie auf **Positionen**, um das Register zu öffnen und Ausgabenpositionen einzugeben.
5. Wählen Sie einen Kreditor aus. Geben Sie beispielsweise `US-104` ein oder wählen Sie es aus.
6. Geben Sie im Feld **Rechnung** einen Wert ein.
7. Geben Sie im Feld **Beschreibung** einen Wert ein.
8. Geben Sie im Feld **Kredit** eine Zahl ein.
9. Wählen Sie im Feld **Genehmigt von** einen Genehmiger in der Dropdownliste aus.
10. Wählen Sie **Buchen** aus.

## <a name="approve-an-invoice"></a>Genehmigen einer Rechnung
1. Wechseln Sie im Navigationsbereich zu **Module > Kreditoren > Rechnungen > Rechnungsgenehmigung**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie den Namen der Rechnungsgenehmigungserfassung aus, den Sie benutzen möchten.
4. Klicken Sie auf **Positionen**, um eine Seite anzuzeigen, auf der Sie die Rechnungen auswählen können, die Sie genehmigen möchten.
5. Wählen Sie **Belege suchen** aus, um alle Rechnungen anzuzeigen, die zur Genehmigung bereit sind.
6. Markieren Sie die Rechnung, die Sie erstellt haben, klicken Sie **Auswählen**. Die Belege, die Sie oben ausgewählt haben, werden auf diese Liste verschoben, nachdem Sie sie auswählen.  
7. Wählen Sie **OK**.
8. Wählen Sie das Feld **Kontonummern**, um ein Ausgabenkonto der Rechnung hinzuzufügen.
9. Geben Sie eine Kontonummer ein und bewegen Sie die Tabulatortaste vom Feld weg. Geben Sie beispielsweise `600120` ein.
10. Wählen Sie **Buchen** aus.
11. Wählen Sie **Beleg** aus, um die Einträge anzuzeigen, die gebucht wurden. Das Konto "Rechnung mit ausstehender Genehmigung" wird zurückgesetzt und durch das tatsächliche Ausgabenkonto ersetzt.  

