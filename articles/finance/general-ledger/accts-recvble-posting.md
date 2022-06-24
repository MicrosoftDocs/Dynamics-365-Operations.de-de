---
title: Debitorenkontobuchung
description: Dieser Artikel erklärt, wie Buchungen in der Debitorenbuchhaltung konfiguriert werden, und enthält Beispiele für Buchungskonfigurationen.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 492bbd31cae08a93cd68e5ce120d02a62141241b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874573"
---
# <a name="accounts-receivable-posting"></a>Debitorenbuchung

[!include [banner](../includes/banner.md)]

Das primäre Buchungsprofil für das Modul **Debitoren** ist das Buchungsprofil des Debitors. Dieses Buchungsprofil bestimmt das Sammelkonto, das verwendet wird, wenn die Salden der Debitoren im Hauptbuch gebucht werden. Ein Sammelkonto ist ein Hauptkonto. Es wird auch als Inzahlungnahme-Konto für Debitoren bezeichnet.

Weitere Informationen finden Sie unter [Debitorenbuchungsprofile](../accounts-receivable/customer-posting-profiles.md).

In Debitoren sind neben dem Buchungsprofil des Debitors mehrere Buchungskonfigurationen verfügbar. Die folgenden Abschnitte enthalten mehr Informationen zu diesen anderen Buchungskonfigurationen.

## <a name="posting-accounts-for-methods-of-payment"></a>Buchungskonten für Zahlungsarten

Zahlungsmethoden definieren, wie eine Zahlung im Hauptbuch gebucht wird. Sie steuern auch das Verhalten der Zahlungsausgabe. Normalerweise wird für jede Zahlungsart, die Ihr Unternehmen akzeptiert (z.B. Bargeld, Scheck, Kreditkarte, Zahlungsanweisung und Überweisung), eine Zahlungsmethode erstellt.

Die Felder im Abschnitt **Buchung** auf dem Inforegister **Allgemein** steuern, wie eine Zahlung im Hauptbuch gebucht wird. Sie müssen zuerst einen Wert im Feld **Kontotyp** auswählen. Der ausgewählte Kontotyp steuert das Verhalten des **Zahlungskonto**-Felds. Wir empfehlen **Bank** im **Kontotyp** Feld und dann das Bankkonto im **Zahlungskonto**-Feld auszuwählen. Der Vorteil dieses Ansatzes besteht darin, dass das System die Zahlung auf das untergeordnete Sachkonto der Bank bucht, was die Abstimmung und andere bargeldbezogene Prozesse unterstützt. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils, wenn Sie das **Bargeld- und Bankmanagement**-Modul verwenden.

| Buchungstyp | Kontotyp | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Bank | Bank | Bank von Contoso | Bankkonto, das mit einer Analge verknüpft ist | Gutschrift | Nein | Geben Sie für jede Zahlungsmethode das Hauptkonto im **Zahlungskonto**-Feld ein. |

Wenn Sie nicht vorhaben, Cash- und Bankmanagement zu verwenden, sollten Sie im Feld **Kontotyp** die Option **Sachkonto** wählen und dann im Feld **Zahlungskonto** das Hauptkonto auswählen. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils, wenn Sie nicht mit Cash and Bank Management arbeiten.

| Buchungstyp | Kontotyp | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Unternehmen | Unternehmen | 100100: Bank von Contoso | Anlage | Gutschrift | Nein | Geben Sie für jede Zahlungsmethode das Hauptkonto im **Zahlungskonto**-Feld ein. |

## <a name="bridging-accounts"></a>Transferkonten

Die Transferbuchung ist ein zweistufiger Prozess, der verwendet wird, wenn Zahlungen gebucht werden. Es handelt sich um eine optionale Funktion, die beispielsweise bei Bankkonten mit Nullsaldo verwendet werden kann. Er kann dazu beitragen, einen reibungsloseren und zeitnaheren Bankabstimmungsprozess zu gewährleisten. Im ersten Schritt wird eine Zahlung auf ein temporäres Konto (das Transferkonto) gebucht. Im zweiten Schritt wird die gebuchte Buchung storniert und auf das Bankkonto gebucht, wenn die Zahlung von der Bank verrechnet wird. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils für die Transferbuchung.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Erstellte Journale | 130725 | Nicht verrechnetes Bargeld | Passivposten | Belastung | Ja | Geben Sie für jede Zahlungsmethode das Hauptkonto im **Transferkonto**-Feld ein. |

Weitere Informationen finden Sie unter [Transferzahlungen einrichten und verarbeiten](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Buchungskonten für Debitor-Skonti

Wenn Ihr Unternehmen Kunden Skonti als Gegenleistung für eine schnelle Zahlung anbietet, müssen Sie Skontocodes konfigurieren und angeben, wie die Skonti im Hauptbuch gebucht werden sollen. Für die Angabe des Hauptkontos, über das ein Debitorenskonto gebucht wird, stehen mehrere Möglichkeiten zur Verfügung.

Weitere Informationen finden Sie unter [Skonti](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Buchungskonten für Zahlungsgebühren

Mit den Zahlungsgebühren können Sie automatisch eine Gebühr zu einer Zahlung des Debitors hinzufügen, wenn eine Reihe von Bedingungen erfüllt ist. Zahlungsgebühren können dem Debitor in Rechnung gestellt oder als Aufwand auf Ihrem Bankkonto verbucht werden. Im Folgenden finden Sie einige Beispiele hierfür:

- Sie berechnen Debitor 3 Prozent der Zahlungssumme, wenn sie mit einer Kreditkarte bezahlen.
- Ihre Bank berechnet Ihnen $1,00 für jede Überweisung, die Sie verarbeiten, und die Überweisungsgebühr wird als Aufwand verbucht.

Wenn Sie bei der Konfiguration einer Debitorenzahlungsgebühr das Feld **Gebühr** auf **Kunde** festlegen, ist das Feld **Hauptkonto** nicht mehr verfügbar und das System verwendet das Kundenbuchungsprofil, um die Gebühr zu buchen. Wenn Sie das **Belastung**-Feld auf **Sachkonto** festlegen, müssen Sie das **Hauptkonto**-Feld auf das Hauptkonto festlegen, wo die Zahlungsgebühr gebucht wird. Dieses Hauptkonto ist in der Regel ein Ausgabenkonto. Die folgende Tabelle zeigt ein Beispiel für die Konfiguration des Buchungsprofils für die Zahlungsgebührbuchung.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Erstellte Journale | 618190 | Bankgebührausgaben | Ausgaben | Belastung | Nein |  Wenn **Sachkonto** im Feld **Gebühr** ausgewählt ist, wählen Sie dieses Konto im Feld **Hauptkonto** für die Zahlungsgebühr aus. |

Weitere Informationen finden Sie unter [Zahlungsgebühren von Kreditoren erstellen](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Buchungskonten für Belastungen Codes

Wenn Sie neben den Zeilen auch die Verkaufsbeträge verfolgen müssen, können Sie Lasten-Codes verwenden. So können Sie beispielsweise Ihren Debitor mit Fracht- und Bearbeitungsgebühren belasten, oder Sie können einige Fracht- und Bearbeitungsgebühren intern ausgeben. Sie können angeben, ob diese Beträge in Ausgabenkonten gebucht oder ob den Kosten der Artikel hinzugefügt werden sollen.

Sie können Belastungscodes für Debitoren und Kreditorenkonten erstellen. Wenn Sie einen Belastungscode konfigurieren, müssen Sie die Buchung definieren. Die Buchung steuert sowohl das Sollkonto als auch das Habenkonto. Für jede von Ihnen erstellte Abgabenordnung können Sie die verwendete Buchungsart auswählen. In der folgenden Tabelle finden Sie typische Beispiele für Belastungen für Debitoren.

| Buchungstyp | Hauptkontobeispiel | Hauptkonto-Namenbeispiel | Kontotyp | Soll/Haben? | Clearingkonto | Description |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Zahlungsgebühr | 411400 | Umsatz - Gebühren | Umsatzerlös | Gutschrift | Nein | **Beispiel für unzureichende Deckung:** Soll Debitor/Kreditor und Haben Sachkonto |
| Auftrag, Fracht | 403500 | Umsatz - Fracht | Umsatzerlös | Gutschrift | Nein | **Beispiel für eine Fracht, die einem Debitor in Rechnung gestellt wird:** Debit Customer/Vendor und Credit Sachkonto |
| Rückvergütung\* | 403200 | Rabatt | Umsatzerlös | Belastung | Nein | **Beispiel für einen Kundenrabatt:** Debitor Sachkonto und Kredit Kunde/Lieferant |

\* Beim Rabattbeispiel wird die Buchung nur verwendet, wenn ein Belastungscode zu einem Bestellkopf oder einer Position hinzugefügt wird. Die erweiterte Rabattfunktion, die in Microsoft Dynamics 365 Supply Chain Management verfügbar ist, bietet mehr Kontrolle und Automatisierung von Rabatten. Weitere Informationen finden Sie unter [Kundennachlässe](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Die vorstehende Tabelle zeigt drei typische Beispiele für Buchungstypen, die für Belastungscodes verwendet werden können. Sie sollte als Richtlinie und Beispiel verwendet werden. Sie bietet keine umfassende Liste aller möglichen Kombinationen oder Buchungstypen, die verwendet werden können.

Weitere Informationen finden Sie unter [Belastungscodes erstellen](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Buchungskonten für Provisionen

Sie können das System optional so konfigurieren, dass es die Provisionen für einen Vertriebsmitarbeiter oder eine Gruppe von Vertriebsmitarbeitern für einen bestimmten Verkaufsauftrag berechnet. Wenn Sie diese Funktion aktivieren, müssen Sie das Buchungskonto konfigurieren, das für die Berechnung der Provision verwendet wird. Diese Konfiguration wird auf der Seite **Kommissionsbuchung** im Modul **Vertrieb und Marketing** vorgenommen.

Weitere Informationen finden Sie unter [Regeln für Verkaufsprovisionen festlegen](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
