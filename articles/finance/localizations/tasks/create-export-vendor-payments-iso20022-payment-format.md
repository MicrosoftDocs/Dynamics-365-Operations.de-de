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
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185818"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Kreditorenzahlungen mithilfe eines ISO20022-Zahlungsformats erstellen und exportieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Thema erläutert, wie Sie Zahlungspositionen in der Kreditorzahlungserfassung erstellen und eine Kreditorenzahlungsdatei mit dem Beispiel zur ISO2022-Banküberweisung erstellen.

Dies ist der fünfte von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen. Verwenden Sie die Demodaten DEMF, um dieses Beispiel abzuschließen.

## <a name="example"></a>Beispiel

1.  Gehen Sie zu **Kreditorenkonten > Zahlungen > Zahlungserfassung**.
2.  Klicken Sie auf **Neu**.
3.  Geben Sie im Feld **Name** einen Wert ein, oder wählen Sie einen Wert aus.
4.  Klicken Sie auf **Positionen > Zahlungsvorschlag > Zahlungsvorschlag erstellen**.
5.  Erweitern Sie den Abschnitt **Einzuschließende Datensätze**.
6.  Klicken Sie auf **Filter**.
7.  In der Liste wählen Sie die Zeile für **Kreditorentabelle** und **Kreditorenkonto-Feld** aus.
8.  Geben Sie im Feld **Kriterien** einen Wert ein, oder wählen Sie einen Wert aus. Sie können alle beliebigen Kriterien für die Auswahl von Kreditorenbuchungen anwenden. In diesem Beispiel verwenden Sie DE-001 als Kreditorenkonto.
12. Klicken Sie auf **OK**.
13. Klicken Sie auf **OK**.
14. Klicken Sie auf **Zahlungen erstellen**.
15. Generieren Sie eine ISO20022-Zahlungsdatei.
    1.  Klicken Sie auf **Zahlungen generieren**.
    2.  Geben Sie im Feld **Zahlungsmethode** einen Wert ein, oder wählen Sie einen Wert aus.
    3.  Geben Sie im Feld **Dateiname** einen Wert ein. In vorliegenden Beispiel ist die generierte Datei aufgrund der EUR-Zahlung SEPA-konform. Die ISO20022-Banküberweisung und andere Kreditorenzahlungsformate können ebenfalls zum Generieren von Zahlungen in anderen Währungen verwendet werden.
    4.  Geben Sie im Feld **Bankkonto** einen Wert ein, oder wählen Sie einen Wert aus.

