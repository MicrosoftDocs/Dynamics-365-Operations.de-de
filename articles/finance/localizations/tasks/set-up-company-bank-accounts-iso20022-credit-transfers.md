---
title: Unternehmens-Bankkonten für ISO20022-Überweisungen einrichten
description: Dieses Verfahren zeigt, wie Sie die unternehmensspezifischen Bankkontoinformationen einrichten, die für die Zahlungsdateigenerierung erforderlich sind.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780769"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Unternehmens-Bankkonten für ISO20022-Überweisungen einrichten

[!include [banner](../../includes/banner.md)]

Dieses Verfahren zeigt, wie Sie die unternehmensspezifischen Bankkontoinformationen einrichten, die für die Zahlungsdateigenerierung erforderlich sind. Sie richten die Informationen ein, die erforderlich sind, um das ISO 20022-Banküberweisungsformat zu generieren. Abhängig vom Format werden möglicherweise auch andere Informationen benötigt (z. B. die Unternehmenskennung oder die Bankleitzahl). 

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.

Dies ist der zweite von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.


## <a name="set-up-iban-and-swift-code"></a>Einrichten von IBAN- und SWIFT-Code
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Bankkonten".
2. Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "DEMF OPER" zu filtern.
3. Klicken Sie auf DEMF OPER, um die Bankkontodetails zu öffnen.
4. Klicken Sie auf "Bearbeiten".
5. Erweitern Sie den Abschnitt "Zusätzliche Kennung".
6. Geben Sie im Feld "IBAN" den Wert "DE89370400440532013000" ein.
7. Geben Sie im Feld "SWIFT-Code" "DEUTDEFF" ein.
    * Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.  
8. Klicken Sie auf "Speichern".

## <a name="set-up-bank-account-for-the-legal-entity"></a>Bankkonto für die juristische Person einrichten
1. Wechseln Sie zu Organisationsverwaltung > Organisationen > Juristische Personen.
2. Klicken Sie auf "Bearbeiten".
3. Erweitern Sie den Abschnitt "Bankkontoinformationen".
4. Geben Sie im Feld 'Bankkonto' einen Wert ein, oder wählen Sie einen Wert aus.
5. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]