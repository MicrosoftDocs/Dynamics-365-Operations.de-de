---
title: Bankauszug und Zahlungsabstimmung für die EU
description: Dieses Thema bietet einen Überblick der Funktionen, die Sie verwenden können, um Zahlungsinformationen von den Banken in Formate abzustimmen, die von den europäischer Länder verwendet werden.
author: neserovleo
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3fbdefce85fbd7aee228cdcb58f29007478c1485
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407734"
---
# <a name="bank-statement-and-payment-reconciliation-for-the-eu"></a>Bankauszug und Zahlungsabstimmung für die EU

[!include [banner](../includes/banner.md)]

Dieses Thema bietet einen Überblick der Funktionen, die Sie verwenden können, um Zahlungsinformationen von den Banken in Formate abzustimmen, die von den europäischer Länder verwendet werden. Sie können Transaktionen von Banken importieren und diese Transaktionen mit bestehenden Transaktionen ausgleichen. In Europa können Sie dies für die folgenden Szenarien tun:

-   Importieren von Bankauszügen
-   Importieren von Zahlungen
-   Importieren von Rückgabedateien

## <a name="bank-statements"></a>Bankauszüge
Ein *Bankauszug* oder ein *Kontoauszug* ist eine Zusammenfassung von wertmäßigen Buchungen, die über eine bestimmte Zeitperiode auf einem Konto erfolgt sind, das aus einem Unternehmen mit dem Finanzinstitut stattfindet. In Finance können Sie einen Bankauszug importieren. Es ist wichtig, importierte Buchungen mit vorhandenen Buchungen auszugleichen sowie den Anfangs- und den Endsaldo der Bankkonten zu überprüfen. Die folgende Liste umfasst die unterstützten europäischen Formate.

-   Erweiterte Banabstimmungen für europäische Dateiformate. Weitere Informationen finden Sie unter [Bankabstimmungsüberblick](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   Bankauszugsnachrichten-Dateiformat ISO 20022 camt.053.
-   CODA Bankauszugs-Dateiformat Weitere Informationen finden Sie unter [CODA Bankauszug](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Debitoren- und Kreditorenzahlungen Import und Rücklieferungsnachrichten
Neben einem Bankauszug können Banken bestimmte Meldungen bereitstellen, die Informationen zu Debitoren und Kreditorenzahlungen enthalten, die in Finance importiert werden und mit Debitoren- und Kreditorenrechnungsbuchungen abgestimmt werden können. Wenn ein Unternehmen Informationen über eingehende Debitorenzahlungsbuchungen von der Bank erhalten muss, können Importformate verwendet werden. Bei Unternehmen, die direkte Banküberweisung verwenden, können die Rückgabemeldungen empfangen werden, um den Status ausstehender Zahlungen zu aktualisieren, die zuvor exportiert wurden. Die Differenz zwischen Importformaten und Rücklieferungsformaten ist, dass Rücklieferungen meistens dazu dienen, bereits erstellte Zahlungserfassungspositionen zu aktualisieren (Sie können erstellt werden, wenn direkte Überweisungen ausgeführt wurden), anstatt neue Positionen zu erstellen. Einige komplexe Importformate können auch Rückholszenarien enthalten. Das folgende Beispiel veranschaulicht, wie diese Teilung implementiert werden soll.

### <a name="import-formats"></a>Importformat

-   [ISO 20022 camt.054](emea-ISO20022-file-formats.md)-Bankbenachrichtigungsmitteilung
-   [Netzwerkimportformat](emea-nor-nets-import-format.md) – komplexe Funktion für norwegische Zahlungsformate
-   [ESR-Debitorenzahlungen für Importe](emea-che-esr-customer-payments-import.md) 
-   Importieren Sie Zahlungsformate für Schweden - BankGirot-Maximum und BankGirot OCR-Formate

### <a name="return-formats"></a>Rückgabeformat

-   [ISO 20022 pain.002](emea-ISO20022-file-formats.md)-Zahlungsstatusbericht
-   (DNK) BetalingsserviceBasis-returformat – Rückgabeformat für Kunden Betalingsservice-Exportformat
-   [Importzahlungsformate für Schweden](emea-swe-payment-formats-import.md)
-   (SWE) BankGirot-Rücklieferung – Kreditorenzahlungen geben das Format zurück, das dem Bankgirot-Exportformat entspricht




[!INCLUDE[footer-include](../../includes/footer-banner.md)]