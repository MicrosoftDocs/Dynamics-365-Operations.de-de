---
title: „Zahlungstyp muss Kreditkarte sein“-Fehler auf der Auftragsseite
description: Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn nach der Auftragssynchronisierung auf der Auftragsseite eine Fehlermeldung angezeigt wird.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285631"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>„Zahlungstyp muss Kreditkarte sein“-Fehler auf der Auftragsseite

[!include [banner](../../includes/banner.md)]

Dieser Artikel enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn nach der Auftragssynchronisierung auf der Auftragsseite eine Fehlermeldung angezeigt wird.

## <a name="description"></a>Beschreibung

Wenn Sie nach der Synchronisierung eines Auftrags die Auftragsseite öffnen, wird die folgende Fehlermeldung angezeigt: „Der Zahlungstyp muss Kreditkarte sein, da die Kreditkartennummer angegeben wurde.“

![„Zahlungstyp muss Kreditkarte sein“-Fehler.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Lösung

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Zahlungstyp in der Commerce-Zentralverwaltung festlegen

1. Rufen Sie **Debitorenkonten \> Zahlungseinstellungen \> Zahlungsbedingungen** auf.
1. Wählen Sie in der linken Navigation Ihre Zahlungsbedingungen aus.
1. Vergewissern Sie sich, dass im Feld **Zahlungstyp** die Option **Kreditkarte** ausgewählt ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Onlineverkäufe und -zahlungen buchen](../tasks/posting-online-sales-payments.md)
