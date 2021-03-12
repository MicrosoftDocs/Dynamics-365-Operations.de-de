---
title: Debitoren und Debitoren-Bankkonten für ISO20022-Lastschriften einrichten
description: Diese Aufgabe führt Sie durch die Einrichtung eines Debitorenbankkontos und eines Direkteinzugsmandats des Debitors, die erforderlich sind, um die ISO20022-Kreditoren-Direktbelastungszahlungsdatei zu generieren.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85c1faebe9a61ad2e708ba26c7a5f0cad15f5f8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988200"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Debitoren und Debitoren-Bankkonten für ISO20022-Lastschriften einrichten

[!include [banner](../../includes/banner.md)]

Diese Aufgabe führt Sie durch die Einrichtung eines Debitorenbankkontos und eines Direkteinzugsmandats des Debitors, die erforderlich sind, um die ISO20022-Kreditoren-Direktbelastungszahlungsdatei zu generieren. Abhängig von Debitorenzahlungsformaten, die eingerichtet sind, sind zusätzliche Informationen erforderlich, die nicht in dieser Prozedur abgedeckt werden, aber für einen Debitor oder ein Debitorenbankkonto erforderlich sind. 

Diese Aufgabe wurde mithilfe des Demodatenunternehmens DEMF mit der primären Adresse einer juristischen Person in Deutschland erstellt.



Dies ist der vierte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.


## <a name="set-up-a-customer-bank-account"></a>Einrichten eines Debitorenbankkontos
1. Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Konto" mit dem Wert "DE-010".
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Klicken Sie im Aktivitätsbereich auf "Debitor".
5. Klicken Sie auf Bankkonten.
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Bankkonto" einen Wert ein.
8. Geben Sie im Feld "Name" einen Wert ein.
    * Geben Sie beispielsweise 'EUR Bank'. ein.  
9. Geben Sie im Feld 'Bankgruppen' einen Wert ein, oder wählen Sie einen Wert aus.
10. Geben Sie im Feld "IBAN" einen Wert ein.
    * Geben Sie beispielsweise 'DE36200400000628808808' ein.  
11. Geben Sie im Feld "SWIFT-Code" einen Wert ein.
    * Geben Sie beispielsweise "COBADEFFXXX" ein.  Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.  
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.
14. Klicken Sie auf "Bearbeiten".
15. Erweitern Sie den Abschnitt "Zahlungsausfälle".
16. Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.

## <a name="add-a-direct-debit-mandate"></a>Direkteinzugsmandats-ID hinzufügen
1. Erweitern Sie den Abschnitt "Einzugsermächtigungen".
2. Klicken Sie auf Hinzufügen.
3. Geben Sie im Feld 'Kreditorenbankkonto' einen Wert ein, oder wählen Sie einen Wert aus.
    * Wählen Sie z. B. DEMF OPER. aus.  
4. Geben Sie im Feld "Unterschriftsdatum" ein Datum ein.
5. Klicken Sie auf „Ja“, um die Datumsaktualisierung zu bestätigen.
6. Geben Sie im Feld "Ort der Signatur" einen Wert ein, oder wählen Sie einen Wert aus.
7. Geben Sie im Feld "Erwartete Anzahl der Zahlungen" eine Zahl ein.
8. Klicken Sie auf "OK".
9. Klicken Sie auf "Speichern".

