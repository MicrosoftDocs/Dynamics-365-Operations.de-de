---
title: „Zahlungstyp muss Kreditkarte sein“-Fehler auf der Auftragsseite
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn nach der Auftragssynchronisierung auf der Auftragsseite eine Fehlermeldung angezeigt wird.
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018409"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>„Zahlungstyp muss Kreditkarte sein“-Fehler auf der Auftragsseite

[!include [banner](../../includes/banner.md)]

Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn nach der Auftragssynchronisierung auf der Auftragsseite eine Fehlermeldung angezeigt wird.

## <a name="description"></a>Beschreibung

Wenn Sie nach der Synchronisierung eines Auftrags die Auftragsseite öffnen, wird die folgende Fehlermeldung angezeigt: „Der Zahlungstyp muss Kreditkarte sein, da die Kreditkartennummer angegeben wurde.“

![„Zahlungstyp muss Kreditkarte sein“-Fehler](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Lösung

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Zahlungstyp in der Commerce-Zentralverwaltung festlegen

1. Rufen Sie **Debitorenkonten \> Zahlungseinstellungen \> Zahlungsbedingungen** auf.
1. Wählen Sie in der linken Navigation Ihre Zahlungsbedingungen aus.
1. Vergewissern Sie sich, dass im Feld **Zahlungstyp** die Option **Kreditkarte** ausgewählt ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Onlineverkäufe und -zahlungen buchen](../tasks/posting-online-sales-payments.md)
