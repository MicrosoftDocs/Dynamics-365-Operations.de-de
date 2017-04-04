---
title: ESR-Debitorenzahlungsimport
description: "Dieses Thema enthält Informationen zum Importieren von Debitorenzahlungen in ESR-Format."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f7fd20ef0c78bc781f0ef9f17fc612723906ac78
ms.openlocfilehash: 87643da8ef213f72740370a52d500d9f6fb2fcf2
ms.lasthandoff: 03/31/2017


---

# <a name="esr-customer-payments-import"></a>ESR-Debitorenzahlungsimport

Dieses Thema enthält Informationen zum Importieren von Debitorenzahlungen in ESR-Format.

ESR ist ein elektronischer Schuldner-Service, Zahlungsbelege der verwendet, um Geld erfasst. Hierbei handelt es sich um das Standardsystem der elektronische Zahlungsmethode, das von den schweizerischen Buchen erstellt wird. Sie können im ESR-Format Debitorenzahlungsdateien erhalten, das Buchungen und Bankgebühren enthalten kann. Diese Funktionalität wird für importierte Debitorenbuchungen auf Grundlage Zahlungsreferenzen vorgesehen, die ursprünglich in Microsoft Dynamics 365 für Arbeitsgänge generiert wurden und auf den Zahlungsbeleg gedruckt.

## <a name="generate-payment-references"></a>Generieren Sie Zahlungsreferenzen
Zahlungsreferenzen sollten auf den Zahlungsbeleg gedruckt werden, nachdem sie gebucht wurde. Sie können auf die Zahlungsreferenzen ** Rechnungserfassung ** Seite für den ausgewählten Auftrag auch überprüfen. Um Zahlungsreferenzen zu generieren, müssen die folgenden Einstellungen festgelegt werden.

1.  Legen Sie die Bankkontoeinstellungen auf ** ESR **, BESR-ID ** ** fest und Bankleitzahl ** **.
2.  Legt das ** Nummer Zeichen für Postgirokonto ** Feld auf der ** Debitorenparameter ** Seite der ** Sachkonto und Mehrwertsteuer ** Registerkarte fest. Dies definiert, wie viele Symbole vom Debitorenkonto in der Zahlungsreferenz einbezogen werden sollen.
3.  Der Verkaufsrechnungsnummernkreis soll im richtigen Format (es sollte Symbole nicht anders als Ziffern haben und dieses nicht enthalten soll führende null) sein.
4.  ** Orange ** Das Format muss für das Debitorenkonto im Feld ** auf einer Debitorenrechnung ** ** Feld auf der Rechnung und Lieferung ** Registerkarte angegeben werden.

Weitere Informationen finden Sie Zahlungsbelegbericht Giro ([])(emea-eur-payment-slip-report-giro.md).

## <a name="import-a-payment-file"></a>Importieren einer Zahlungsdatei
1.  Zur ** Zahlungserfassung ** Seite
2.  Klicken Sie auf **Positionen**.
3.  ** Auf Funktionen ** &gt; ** Importzahlungen **.
4.  Wählen Sie im Dialogfeld die Zahlungsmethode, und suchen Sie dann zum Speicherort der Datei aus, die importiert werden sollen. 
  > [!NOTE]
  >  Bevor Sie diesen Schritt ausführen können, müssen Sie die CH) (Einzahlungsschein ** ** Konfigurationen aus den Lebenszyklus-Dienstleistungen (LCS) bereits importiert haben und die ESR-Zahlungsmethode einrichten. Weitere Informationen finden Sie [Dateiformate für Methode von Zahlungen emea-select-file-formats-for-the-method-of-payments.md] ().

Nachdem die Zahlungsdatei importieren, werden für Zahlungserfassungspositionen Ausgleich mit Debitorenrechnungen anhand die Zahlungsreferenz erstellt und markiert. Wenn vorhanden) Gebühren gibt, die für das Bankkonto angegeben werden, die in der Datei, wie Buchungen zwischen dem und dem Hauptkonto Gebührenkonto angezeigt werden, sind diese Gebühren der Erfassung hinzugefügt.


