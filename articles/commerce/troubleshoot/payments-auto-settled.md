---
title: Zahlungen werden automatisch abgerechnet, bevor Aufträge fakturiert oder versendet werden
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Zahlung unmittelbar nach Auftragserteilung im Adyen-Portal abgerechnet wird, obwohl der Auftrag nicht fakturiert oder versendet wurde.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018259"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Zahlungen werden automatisch abgerechnet, bevor Aufträge fakturiert oder versendet werden

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn eine Zahlung unmittelbar nach Auftragserteilung im Adyen-Portal abgerechnet wird, obwohl der Auftrag nicht fakturiert oder versendet wurde.

## <a name="description"></a>Beschreibung

Nach Erteilung eines Auftrags wird die Zahlung sofort im Adyen-Portal abgerechnet, obwohl der Auftrag nicht fakturiert oder versendet wurde.

## <a name="resolution"></a>Lösung

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Die manuelle Erfassung für E-Commerce-Zahlungen im Adyen-Portal konfigurieren

Befolgen Sie diese Schritte, um die manuelle Erfassung für E-Commerce-Zahlungen im Adyen-Portal zu konfigurieren.

1. Melden Sie sich beim Adyen-Portal an.
1. Wählen Sie in der oberen rechten Ecke Ihr Händlerkonto für den E-Commerce-Kanal aus.
1. Wählen Sie in der oberen Navigationsleiste **Konto** und dann **Einstellungen** aus.
1. Wählen Sie im Feld **Verzögerung erfassen** die Option **Manuell** aus.

    ![„Verzögerung erfassen“-Einstellung im Adyen-Portal](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Adyen-Zahlungserfassung](https://docs.adyen.com/point-of-sale/capturing-payments)

[Zahlungskonnektor von Dynamics 365 für Adyen](../dev-itpro/adyen-connector.md)

[Adyen-Zahlungskonnektor für Dynamics 365 einrichten](https://docs.adyen.com/plugins/microsoft-dynamics)
