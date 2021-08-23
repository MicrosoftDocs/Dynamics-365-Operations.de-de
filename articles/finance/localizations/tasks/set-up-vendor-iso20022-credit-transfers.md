---
title: Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten
description: Diese Verfahren zeigt, wie Sie den Kreditor und dessen spezifische Bankkontoinformationen einrichten, die für ISO20022-Kreditübertragung-Dateigenerierung oder jede andere Kreditorenzahlung erforderlich sind.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a901591f9f3d1a892c29f92e59dc96c1f172143cae6bec571da33b4a50d274
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723718"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten

[!include [banner](../../includes/banner.md)]

Diese Verfahren zeigt, wie Sie den Kreditor und dessen spezifische Bankkontoinformationen einrichten, die für ISO20022-Kreditübertragung-Dateigenerierung oder jede andere Kreditorenzahlung erforderlich sind. 

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.
Dies ist der vierte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="set-up-bank-details"></a>Bankdetails einrichten
1. Gehen Sie zu "Kreditoren" > "Händler" > "Alle Händler".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld "Kreditorenkonto" mit dem Wert "DE-001".
3. Klicken Sie auf "DE-001", um die Kreditorendetails zu öffnen.
4. Klicken Sie im Aktivitätsbereich auf "Händler".
5. Klicken Sie auf Bankkonten.
6. Klicken Sie auf "Bearbeiten".
    * Wenn kein verfügbares Bankkonto vorhanden ist, müssen Sie ein neuer Datensatz erstellen.  
7. Geben Sie im Feld "SWIFT-Code" "COBADEFFXXX" ein.
8. Geben Sie im Feld "IBAN" den Wert "DE36200400000628808808" ein.
9. Schließen Sie die Seite.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Zahlungsmethode für den Kreditor einrichten
1. Klicken Sie auf "Bearbeiten".
2. Erweitern oder reduzieren Sie den Abschnitt "Zahlung".
3. Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der Zeile "SEPA CT".
5. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]