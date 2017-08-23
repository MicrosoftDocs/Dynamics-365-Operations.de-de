--- 
title: "Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten"
description: "Diese Aufgabe führt Sie durch die Einrichtung der unternehmensspezifischen Bankkontoinformationen, die zum Erstellen von Debitoren-Zahlungsdateien erforderlich sind."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 741d8ddca24e5fe083b4ddf775bb7f2d65a56fee
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Unternehmens-Bankkonten für ISO20022-Lastschriften einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Aufgabe führt Sie durch die Einrichtung der unternehmensspezifischen Bankkontoinformationen, die zum Erstellen von Debitoren-Zahlungsdateien erforderlich sind. Diese Verfahren verwendet das ISO 20022-Direktbelastungsformat als Beispiel. Andere Formate erfordern ggf. zusätzliche Einrichtungsinformationen wie die Unternehmenskennung oder die Bankleitzahl.



Diese Aufgabe wurde mit dem Demodatenunternehmen DEMF erstellt.



Dies ist die zweite von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.


## <a name="set-up-the-iban-and-swift-codes"></a>IBAN- und SWIFT -Codes einrichten
1. Wechseln Sie zu "Bargeld- und Bankverwaltung" > "Bankkonten".
2. Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "DEMF OPER" zu filtern.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Beispiel: Klicken Sie auf "DEMF OPER", um die Bankkontodetails zu öffnen.  
4. Klicken Sie auf "Bearbeiten".
5. Erweitern oder reduzieren Sie den Abschnitt "Zusätzliche Kennung".
6. Geben Sie im Feld "IBAN" einen Wert ein.
    * Geben Sie beispielsweise 'DE89370400440532013000' ein.  
7. Geben Sie im Feld "SWIFT-Code" einen Wert ein.
    * Geben Sie z. B. 'DEUTDEFF' ein.    Beachten Sie, dass die SWIFT\BIC nicht für mehrere Zahlungsformate erforderlich ist, jedoch empfohlen wird, um sie für ein Bankkonto zu erfassen.  
8. Klicken Sie auf "Speichern".

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Bankkonto für die juristische Person einrichten
1. Wechseln Sie zu Organisationsverwaltung > Organisationen > Juristische Personen.
2. Klicken Sie auf "Bearbeiten".
3. Erweitern oder reduzieren Sie den Abschnitt "Bankkontoinformationen".
4. Klicken Sie im Feld "Bankkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Beispiel: Wählen Sie das "DEMF-OPER" Bankkonto aus.  
6. Klicken Sie auf "Speichern".


