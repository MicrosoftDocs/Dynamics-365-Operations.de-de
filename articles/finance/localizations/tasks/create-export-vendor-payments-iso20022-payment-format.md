---
title: Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren
description: Diese Prozedur zeigt, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei über die ISO2022 Kreditübertragung erstellen.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18c7d0b6c5c6a7f598f4b94f4dcf02df498d74cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822704"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren

[!include [banner](../../includes/banner.md)]

Dieses Thema erläutert, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei mit dem Beispiel zur ISO2022-Banküberweisung erstellen.

Dies ist der fünfte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Verwenden Sie die Demodaten DEMF, um dieses Beispiel abzuschließen.

## <a name="example"></a>Beispiel

1.    Gehen Sie zu **Kreditorenkonten > Zahlungen > Zahlungserfassung**.
2.    Klicken Sie auf **Neu**.
3.    Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.
4.    Klicken Sie auf **Positionen > Zahlungsvorschlag > Zahlungsvorschlag erstellen**.
5.    Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
6.    Klicken Sie auf **Filter**.
7.    In der Liste wählen Sie die Zeile für **Kreditorentabelle** und **Kreditorenkonto-Feld** aus.
8.    Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus. Sie können alle beliebigen Kriterien für die Auswahl von Kreditorenbuchungen anwenden. In diesem Beispiel verwenden Sie DE-001 als Kreditorenkonto.
12.    Klicken Sie auf **OK**.
13.    Klicken Sie auf **OK**.
14.    Klicken Sie auf **Zahlungen erstellen**.
15. Generieren Sie eine ISO20022-Zahlungsdatei.
    1.    Klicken Sie auf **Zahlungen generieren**.
    2.    Geben Sie im Feld **Zahlungsmethode** einen Wert ein, oder wählen Sie einen Wert aus.
    3.    Geben Sie im Feld **Dateiname** einen Wert ein. In vorliegenden Beispiel ist die generierte Datei aufgrund der EUR-Zahlung SEPA-konform. Die ISO20022-Banküberweisung und andere Kreditorenzahlungsformate können ebenfalls zum Generieren von Zahlungen in anderen Währungen verwendet werden.
    4.    Geben Sie im Feld **Bankkonto** einen Wert ein, oder wählen Sie einen Wert aus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]