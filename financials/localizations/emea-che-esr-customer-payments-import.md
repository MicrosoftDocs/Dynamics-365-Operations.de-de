---
title: "ESR-Debitorenzahlungen für Importe"
description: Unter dem folgenden Thema finden Sie Informationen zum Importieren von Debitorenzahlungen in das ESR-Forrmat.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, LedgerJournalTransCustPaym
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264584
ms.assetid: 60c429b5-1d88-4fef-be6b-b8585e0e9ee7
ms.search.region: Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f573885a71fdf449197ecea438e83d747c20a391
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="esr-customer-payments-import"></a>ESR-Debitorenzahlungen für Importe

[!include[banner](../includes/banner.md)]


Unter dem folgenden Thema finden Sie Informationen zum Importieren von Debitorenzahlungen in das ESR-Forrmat.

ESR ist ein elektronischer Schuldner-Service, der Zahlungsbelege verwendet, um Geld einzuziehen. Hierbei handelt es sich um das Standardsystem der elektronische Zahlungsmethode, das von den schweizerischen Post erstellt wird. Sie können im ESR-Format Debitorenzahlungsdateien erhalten, das Buchungen und Bankgebühren enthalten kann. Diese Funktionalität wird für importierte Debitorenbuchungen auf Grundlage von Zahlungsreferenzen vorgesehen, die ursprünglich in Microsoft Dynamics 365 for Operations generiert und auf den Zahlungsbeleg gedruckt wurden.

## <a name="generate-payment-references"></a>Zahlungsreferenzen generieren
Zahlungsreferenzen sollten auf den Zahlungsbeleg gedruckt werden, nachdem sie gebucht wurden. Sie können auch die Zahlungsreferenzen auf der Seite **Rechnungserfassung** für den ausgewählten Auftrag überprüfen. Um Zahlungsreferenzen zu generieren, müssen die folgenden Einstellungen festgelegt werden.

1.  Legen Sie die Bankkontoeinstellungen auf **ESR**, **BESR-ID** und **Bankleitzahl** fest.
2.  Legt das **Nummer Zeichen für Postgirokonto** Feld auf der **Debitorenparameter** Seite der **Sachkonto und Mehrwertsteuer** Registerkarte fest. Dies definiert, wie viele Symbole vom Debitorenkonto in der Zahlungsreferenz einbezogen werden sollen.
3.  Der Verkaufsrechnungsnummernkreis soll im richtigen Format (es sollte Symbole nicht anders als Ziffern haben und dieses sollen keine führende Null aufweisen) sein.
4.  Das Format **Orange** muss für das Debitorenkonto im Feld **Auf einer Debitorenrechnung** auf der **Rechnung und Lieferung** Registerkarte angegeben werden.

Weitere Informationen finden Sie unter [Zahlungsbericht (Giro)](emea-eur-payment-slip-report-giro.md).

## <a name="import-a-payment-file"></a>Zahlungsdatei importieren
1.  Gehen Sie zur Seite **Zahlungsjournal**
2.  Klicken Sie auf **Positionen**.
3.  Klicken Sie auf **Funktionen** &gt; **Zahlungen importieren**.
4.  Wählen Sie im Dialogfeld die Zahlungsmethode, und suchen Sie dann den Speicherort der Datei, die importiert werden soll. 
  > [!NOTE]
  >  Bevor Sie diesen Schritt ausführen können, müssen Sie die **ESR (CH)**Konfigurationen aus dem Lifecycle Services (LCS) bereits importiert haben und die ESR-Zahlungsmethode einrichten. Weitere Informationen finden Sie unter [Dateiformate für Zahlungen](emea-select-file-formats-for-the-method-of-payments.md).

Nachdem Sie die Zahlungsdatei importieren haben, werden die Zahlungserfassungspositionen für den Ausgleich mit Debitorenrechnungen anhand der Zahlungsreferenz erstellt und markiert. Wenn es Gebühren gibt, die für das Bankkonto angegeben werden, die in der Datei angezeigt werden, wie Buchungen zwischen dem Hauptkonto und dem Gebührenkonto, sind diese Gebühren der Erfassung hinzuzufügen.




