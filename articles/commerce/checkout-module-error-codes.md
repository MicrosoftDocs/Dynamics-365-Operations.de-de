---
title: Fehlerreferenzcodes für das Kassenmodul
description: Dieser Artikel beschreibt die Fehlerreferenzcodes des Kassenmoduls, die in benutzerseitigen Fehlermeldungen in Microsoft Dynamics 365 Commerce angezeigt werden.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709668"
---
# <a name="checkout-module-error-reference-codes"></a>Fehlerreferenzcodes für das Kassenmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dieser Artikel beschreibt die Fehlercodes des Kassenmoduls, die in benutzerseitigen Fehlermeldungen in Microsoft Dynamics 365 Commerce angezeigt werden.

Mit Dynamics 365 Commerce wurden standardisierte Fehlerreferenzen eingeführt, die in den Checkout-Fehlern des Online-Kanals enthalten sein können, die den Online-Kunden angezeigt werden. In Commerce Version 10.0.31 und später enthalten die Fehlermeldungen im Checkout-Modul Fehlercodes und zeigen dem Online-Kunden keine unnötigen Informationen an. Die Fehlercodes beziehen sich auf Fehler, die in diesem Artikel ausführlich beschrieben werden.

Je nachdem, welcher Fehler auftritt, enthält die Tabelle in diesem Artikel die folgenden Details:

- Eine Beschreibung der Bedingung, die den Fehler verursacht hat, oder zusätzliche Details
- Informationen, die in der Umgebung oder bei der Konfiguration des Zahlungskonnektors zu berücksichtigen sind
- Informationen, auf die in einem Support-Fall verwiesen werden kann, wenn zusätzliche Hilfe benötigt wird

## <a name="checkout-module-error-reference-codes"></a>Fehlerreferenzcodes für das Kassenmodul

Verwenden Sie die folgende Tabelle, um weitere Details zu den Fehlercode-Referenzen zu erhalten, die von Kunden zur Verfügung gestellt werden oder im Online Store auftreten.

| Fehlercode | Dynamics-bezogener Fehlercode | Fehlerbeschreibung |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Die Zahlung konnte nicht autorisiert werden. Die Kartentyp-ID in **TokenizedPaymentCard** fehlt, oder die angegebene Kartentyp-ID wird nicht unterstützt. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Abgelehnt. Die Zahlung konnte nicht autorisiert werden. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Die Zahlung konnte nicht autorisiert werden. Vom Kunden benötigte zusätzliche Informationen. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Fehler. Wir konnten das Ergebnis der Kartenzahlungsannahme nicht abrufen. Versuchen Sie es erneut oder wenden Sie sich an Ihren Systemadministrator. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Die Zahlung kann nicht durchgeführt werden, da die Eigenschaften des Händlers fehlen. Wenden Sie sich an Ihren Systemadministrator. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Tender Service für den Vorgang kann nicht abgerufen werden. Überprüfen Sie die Einrichtung Ihrer Zahlungsmethode für den ausgewählten Tendertyp. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Es wurde bereits eine Zahlung auf ein Kundenkonto vorgenommen und es ist nur eine Zahlung pro Transaktion zugelassen. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Das Kundenkontolimit weicht von dem fälligen Betrag ab. Versuchen Sie es mit einer anderen Zahlungsmethode oder wenden Sie sich an den Kundensupport, um Hilfe zu erhalten. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Die Zahlung für das Kundenkonto übersteigt den Gesamtbetrag für die aufgeführten Artikel. Versuchen Sie es später noch einmal oder wenden Sie sich an den Kundensupport. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Die Zahlung auf ein Kundenkonto erfordert ein eigenes Konto oder ein passendes Rechnungskonto auf einer Tenderposition. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Eine Debitorenkontozahlung kann derzeit nicht verarbeitet werden. Unterer Grenzwert überschritten. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Diesem Kunden ist es nicht erlaubt, auf Rechnung zu zahlen. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Fehler. Die Zahlung konnte nicht storniert werden. Versuchen Sie es erneut. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Bei der Verarbeitung der Zahlung ist ein Fehler aufgetreten. Versuchen Sie es später noch einmal. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Der Betrag der Treuezahlung übersteigt den Betrag, der für die in dieser Transaktion verwendete Treuekarte zugelassen ist. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Der Betrag der Rückerstattung übersteigt den Betrag, der für die in dieser Transaktion verwendete Treuekarte zugelassen ist. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Die Nummer der Treuekarte wurde nicht gefunden. Aktivieren Sie entweder die Treuekartennummer oder geben Sie eine andere Kartennummer ein, und versuchen Sie es dann erneut. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Die Treuekartennummer ist nicht verfügbar. Geben Sie eine andere Kartennummer ein, und versuchen Sie es erneut. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Mit dieser Treuekarte können für diese Transaktion keine Treuepunkte eingelöst werden. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Bei der Nummer der Geschenkkarte ist ein Fehler aufgetreten. Versuchen Sie es mit einer anderen Geschenkkarte oder wenden Sie sich an den Kundendienst, um Hilfe zu erhalten. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Der Betrag übersteigt das Guthaben auf der Geschenkkarte. Geben Sie einen anderen Betrag ein und versuchen Sie es dann erneut. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Die Buchung darf nicht mehrere Treuezahlungspositionen enthalten. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Die Zahlungsinformationen sind entweder nicht vorhanden oder falsch. Überprüfen Sie die Zahlungsinformationen und versuchen Sie es dann erneut. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | Die Bestellung kann zur Zeit nicht verarbeitet werden. Versuchen Sie es später noch einmal. |
| CCR025     | Front-End-Zeitüberschreitung für Checkout API | Der Front-End-Vorgang hat eine Zeitüberschreitung verursacht. Bestätigen Sie, ob die Bestellung in der Dynamics 365 Commerce headquarters verarbeitet wurde. |
| CCR026     | Ursprünglicher autorisierter Betrag geändert | Der Betrag der Bestellung hat sich gegenüber dem ursprünglichen, über das Gateway verarbeiteten Betrag geändert. Dies kann auf einen zeitlich begrenzten Ablauf eines Gutscheins, einer Werbeaktion oder eines Verkaufs zurückzuführen sein. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Bei der Verarbeitung einer Zahlung ist ein Fehler aufgetreten. Die Referenz, die der Cart API zur Verfügung gestellt wurde, hat eine andere Referenz als erwartet (Hinweis auf mögliche Inkonsistenzen während des Checkout-Prozesses). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Bei der versuchten Zahlungsmethode ist ein Fehler aufgetreten. Wenden Sie sich an den Support, um Ihre Kontoeinstellungen zu überprüfen oder versuchen Sie es erneut mit einer anderen Zahlungsmethode. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[FAQs zu Zahlungen](dev-itpro/payments-retail.md)

[Auschecken-Modul](add-checkout-module.md)

[Zahlungsmodul](payment-module.md)
