---
title: Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren
description: Diese Prozedur zeigt, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei über die ISO2022 Kreditübertragung erstellen.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143123"
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

