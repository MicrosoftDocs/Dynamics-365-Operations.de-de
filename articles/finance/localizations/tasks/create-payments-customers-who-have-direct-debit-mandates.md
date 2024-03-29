---
title: Zahlungen für einen Debitor erstellen, der Direkteinzugsmandate verwendet
description: Dieses Verfahren zeigt das Generieren einer ISO20022-Direktbelastungsdateien für einen Debitor, bei dem eine Direktbelastung konfiguriert und eine Rechnung zu bezahlen ist.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ecc28cb11b8c34a438bb47b1cfa9a37e17297e421020b32030261af95b86a49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757933"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Zahlungen für einen Debitor erstellen, der Direkteinzugsmandate verwendet

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt das Generieren einer ISO20022-Direktbelastungsdateien für einen Debitor, bei dem eine Direktbelastung konfiguriert und eine Rechnung zu bezahlen ist. Eine Rechnung zu erstellen und zu Buchen ist optional. Anstatt eine Rechnung zu bezahlende können Sie vor dem Generieren einer Zahlungsdatei eine Vollmacht in einer Erfassung auswählen, um ein Szenario mit Debitorenvorauszahlungen zu unterstützen.



Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.



Dies ist der fünfte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen. Damit diese Aufgabe ausgeführt werden kann, müssen zuvor alle vorherigen Aufgaben ausgeführt sein. Sie müssen zuerst die elektronischen Berichtskonfigurationen der Debitorenzahlungen importieren, die Zahlungmethode konfigurieren und ihr Unternehmen und die Debitoreninformationen einrichten. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Freitextrechnung mit Informationen zum Direkteinzugsmandat buchen
1. Wechseln Sie zu "Debitoren" > "Rechnungen" > "Alle Freitextrechnungen".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Debitorenkonto" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie z. B. DE-010 aus.  
4. Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.
    * Beispiel: Wählen Sie "Elektronisch" aus.  
5. Geben Sie im Feld "Direkteinzugsmandats-ID" einen Wert ein, oder wählen Sie einen Wert aus.
6. Klicken Sie auf "Position hinzufügen".
7. Geben Sie im Feld "Beschreibung" einen Wert ein.
8. Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.
9. Geben Sie im Feld "Preis je Einheit" eine Zahl ein.
10. Klicken Sie auf "Buchen".
11. Klicken Sie auf "OK".

## <a name="create-a-payment"></a>Zahlung erstellen
1. Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.
4. Klicken Sie auf "Positionen".
5. Klicken Sie auf "Zahlungsvorschlag".
6. Klicken Sie auf "Zahlungsvorschlag erstellen".
7. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
8. Klicken Sie auf "Filter".
9. In der Liste wählen Sie die Zeile für die Tabelle Debitorenbuchungen und das Zahlungsmethode-Feld aus.
    * Sie können alle beliebigen Kriterien zur Auswahl von Debitorenbuchungen anwenden, die gezahlt werden sollen. Dazu Verwenden Sie in diesem Beispiel "Elektronisch" als Zahlungsmethode, um Buchungen zu filtern.  
10. Geben Sie im Feld "Kriterien" einen Wert ein oder wählen Sie einen Wert aus.
11. Klicken Sie auf "OK".
12. Klicken Sie auf "OK".
13. Klicken Sie auf "Zahlungen erstellen".


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]