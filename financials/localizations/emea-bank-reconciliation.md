---
title: "Vor und Zahlungsabstimmungsüberblick für die innereuropäische"
description: "Dieses Thema bietet einen Überblick der Funktionen, die Sie verwenden können, um Zahlungsinformationen von den Banken in Formate abzustimmen, die von den europäischer Länder verwendet werden."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Vor und Zahlungsabstimmungsüberblick für die innereuropäische

Dieses Thema bietet einen Überblick der Funktionen, die Sie verwenden können, um Zahlungsinformationen von den Banken in Formate abzustimmen, die von den europäischer Länder verwendet werden.

In Microsoft Dynamics 365 für Arbeitsgänge, können Sie zum Importieren von den Banken und diese Buchungen in vorhandenen Buchungen auszugleichen. In Europa können Sie dies für die folgenden Szenarien Möglichkeiten:

-   Importieren von Bankauszügen
-   Importieren von Zahlungen.
-   Importieren von Rückgabedateien.

## <a name="bank-statements"></a>Bankauszüge
Ein *bank statement* oder *account statement* ist eine Zusammenfassung von wertmäßigen Buchungen, die über eine bestimmte Zeitperiode auf einem Konto erfolgt sind, das aus einem Unternehmen mit dem Finanzinstitut stattfindet. In Dynamics 365 für Arbeitsgänge können Sie einen Bankauszug importieren. Es ist zu importierten Bank Buchungen mit vorhandenen Buchungen sowie überprüft die wichtig Eröffnung und der Endsaldo die Bankkonten. Die folgende Liste umfasst die unterstützten europäischen Formate.

-   Erweiterte Akte Bankabstimmung Europaen-Formate. Weitere Informationen finden Sie Bankabstimmungsüberblick []( erweitert .. /cash-bank-management/advanced-bank-reconciliation-overview.md).
-   Bankauszugs-Nachrichtendateiformat ISO 20022 camt.053
-   CODA-Bankauszugsdateiformat. Weitere Informationen finden Sie emea-bel-coda-bank-statement-import.md CODA-Bankauszug [] ().

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Debitoren- und Kreditorenzahlungen Import und Rücklieferungsnachrichten
Neben einem Bankauszug Banken können bestimmte Meldungen bereitstellen und Informationen zu Debitoren und Kreditorenzahlungen enthalten, die in Dynamics 365 für Arbeitsgänge importiert werden und mit Debitoren- und Kreditorenrechnungsbuchungen abgestimmt werden können. Wenn ein Unternehmen Informationen über eingehende Debitorenzahlungsbuchungen von der Bank erhalten können Importformate muss, die verwendet werden. Bei Unternehmen, die per Banküberweisung und verwenden können Rückgabemeldungen, die erhalten, um den Status ausstehender Zahlungen zu aktualisieren, die zuvor exportiert wurden. Die Differenz zwischen Importformaten und Rücklieferungsformaten ist, dass Rücklieferungen werden hier meistens Zielgruppe, um bereits erstellter Zahlungserfassungspositionen " erstellt werden, können sie als Abbuchung oder " Banküberweisung initiiert wurden, anstatt neue Positionen zu erstellen, zu aktualisieren. Einige komplexe Importformate können auch Rückholszenarien enthalten. Das folgende Beispiel veranschaulicht, wie diese Division implementiert werden soll.

##### <a name="import-formats"></a>Importformate

-   Bankbenachrichtigungsmeldung ISO 20022 camt.054
-   Netzwerkimportformat []()- emea-nor-nets-import-format.md komplexe Funktionen für norwegische Zahlungsformate
-   ESR-Debitorenzahlungsimport
-   Importieren Sie Zahlungsformate für Schweden - BankGirot-Maximum und OCR-Formate BankGirot

##### <a name="return-formats"></a>Geben Sie die Formate zurück

-   Zahlungsstatusbericht ISO 20022 pain.002
-   (DNK) – BetalingsserviceBasis-returformat Rückgabeformat für Debitor Betalingsservice-Exportformat
-   [Importzahlungsformate für Schweden]()- emea-swe-payment-formats-import.md Bankgirot-Autogiro kehrt zurück
-   (SWE) BankGirot-Rücklieferung – Kreditorenzahlungen geben Format zurückgesetzt, das zu Bankgirot-Exportformat entspricht

