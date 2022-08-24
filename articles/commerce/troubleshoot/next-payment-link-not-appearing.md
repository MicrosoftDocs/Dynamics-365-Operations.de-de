---
title: Die Option „Für meine nächste Zahlung speichern“ wird nicht angezeigt
description: Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn das Kontrollkästchen „Für meine nächste Zahlung speichern“ auf der Checkout-Seite einer E-Commerce-Website nicht unter Zahlungsmethode angezeigt wird.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287483"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Die Option „Für meine nächste Zahlung speichern“ wird nicht angezeigt

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn das Kontrollkästchen **Für meine nächste Zahlung speichern** auf der Checkout-Seite einer E-Commerce-Website nicht unter **Zahlungsmethode** angezeigt wird.

## <a name="description"></a>Beschreibung

Das Kontrollkästchen **Für meine nächste Zahlung speichern** wird nicht im Abschnitt **Zahlungsmethode** auf der Checkout-Seite einer E-Commerce-Website angezeigt.

Die folgende Abbildung zeigt ein Beispiel für eine Checkout-Seite, die das Kontrollkästchen **Für meine nächste Zahlung speichern** enthält.

![Kontrollkästchen „Für meine nächste Zahlung speichern“ im Zahlungsmodul.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Lösung

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Sicherstellen, dass der Dynamics 365 Payment Connector für Adyen in der Commerce-Zentralverwaltung korrekt konfiguriert ist

Befolgen Sie diese Schritte, um sicherzustellen, dass der Dynamics 365 Payment Connector für Adyen in der Commerce-Zentralverwaltung korrekt konfiguriert ist.

1. Rufen Sie **Retail und Commerce \> Kanäle \> Onlineshops** auf.
1. Wählen Sie den Onlineshop aus.
1. Vergewissern Sie sich, dass im Inforegister **Zahlungskonten** das Feld **Speichern von Zahlungsinformationen in E-Commerce zulassen** auf **True** gesetzt ist.

![Das Feld „Speichern von Zahlungsinformationen in E-Commerce zulassen“ in der Commerce-Zentralverwaltung.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zahlungsmodul](../payment-module.md)

[Online-Zahlungsmittel mit dem Adyen-Connector speichern](../dev-itpro/adyen-connector-listPI.md)
