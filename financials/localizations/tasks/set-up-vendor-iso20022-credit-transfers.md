--- 
title: "Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten"
description: "Diese Verfahren zeigt, wie Sie den Kreditor und dessen spezifische Bankkontoinformationen einrichten, die für ISO20022-Kreditübertragung-Dateigenerierung oder jede andere Kreditorenzahlung erforderlich sind."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.openlocfilehash: 147d8fa82bf15c984ad263cada42789038fa7371
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Kreditoren und Kreditorenbankkonten für ISO20022-Überweisungen einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Diese Verfahren zeigt, wie Sie den Kreditor und dessen spezifische Bankkontoinformationen einrichten, die für ISO20022-Kreditübertragung-Dateigenerierung oder jede andere Kreditorenzahlung erforderlich sind. 

Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DEMF.
Dies ist der vierte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.


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


