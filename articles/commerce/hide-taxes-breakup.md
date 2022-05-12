---
title: Informationen zur Steueraufteilung in Bestellzusammenfassungen ausblenden
description: In diesem Thema wird beschrieben, wie Informationen zur Steueraufschlüsselung in Bestellzusammenfassungen auf den Seiten „Warenkorb“, „Kasse“, „Bestellbestätigung“ und „Bestelldetails“ in Microsoft Dynamics 365 Commerce ausgeblendet werden.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645218"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Informationen zur Steueraufteilung in Bestellzusammenfassungen ausblenden

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie Informationen zur Steueraufschlüsselung in Bestellzusammenfassungen auf den Seiten „Warenkorb“, „Kasse“, „Bestellbestätigung“ und „Bestelldetails“ in Microsoft Dynamics 365 Commerce ausgeblendet werden.

Standardmäßig zeigt Dynamics 365 Commerce Informationen zur Steueraufschlüsselung in Bestellzusammenfassungen auf den Seiten „Warenkorb“, „Kasse“, „Bestellbestätigung“ und „Bestelldetails“. Ab der Commerce-Version 10.0.27 enthält der Commerce Site Builder eine Option, mit der Sie die Steueraufschlüsselungsinformationen in Bestellzusammenfassungen ausblenden können.

Die folgende Abbildung zeigt ein Beispiel für zwei Bestellzusammenfassungen. Die erste zeigt die Informationen zur Steueraufteilung an, die zweite blendet sie aus.

![Beispiele für Warenkörbe, in denen Informationen zur Steueraufteilung angezeigt und ausgeblendet werden.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Die Option zum Ausblenden von Steueraufteilungsinformationen in Auftragszusammenfassungen ist nur verfügbar, wenn die Option **Preise inkl. Mehrwertsteuer** für den E-Commerce-Kanal auf **Ja** festgelegt ist in der Commerce-Zentralverwaltung bei **Einzelhandel und Handel \> Kanäle \> Shops \> Alle Shops**. 
> - Standardmäßig ist die Option **Steueraufschlüsselung in Bestellzusammenfassung anzeigen** im Site Builder aktiviert.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Informationen zur Steueraufteilung in Bestellzusammenfassungen ausblenden

Führen Sie die folgenden Schritte aus, um Informationen zur Steueraufteilung in Bestellzusammenfassungen auszublenden.

1. Gehen Sie im Commerce Site Builder zu der Site, die Sie aktualisieren möchten.
1. Gehen Sie zu **Site-Einstellungen \> Erweiterungen**.
1. Deaktivieren Sie das Kontrollkästchen **Steueraufschlüsselung in Bestellzusammenfassung anzeigen**.

Um Informationen zur Steueraufteilung in Bestellzusammenfassungen anzuzeigen, aktivieren Sie das Kontrollkästchen **Steueraufschlüsselung in Bestellzusammenfassung anzeigen**.  

Die folgende Abbildung zeigt das hervorgehobene und ausgewählte Kontrollkästchen **Steueraufschlüsselung in Bestellzusammenfassung anzeigen** im Site Builder.

![Option „Steueraufschlüsselung in Bestellzusammenfassung anzeigen“ im Site Builder.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Mehrwertsteuer](/finance/general-ledger/indirect-taxes-overview)

[Mehrwertsteuer für Onlinebestellungen konfigurieren](sales-tax-config.md)

[Problembehandlung: Falsch berechnete Steuern auf Onlinebestellungen](troubleshoot/tax-miscalculated-online-order.md)
