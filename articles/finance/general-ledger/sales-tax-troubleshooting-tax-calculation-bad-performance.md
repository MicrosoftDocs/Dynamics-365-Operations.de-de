---
title: Leistung der Steuerberechnung beeinflusst Transaktionen
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die sich auf die Leistung der Steuerberechnung und ihre Auswirkungen auf Transaktionen beziehen.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947647"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Leistung der Steuerberechnung beeinflusst Transaktionen

[!include [banner](../includes/banner.md)]

Manchmal ist eine Transaktion von Leistungsproblemen betroffen, die bei der Steuerberechnung auftreten. Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus.

## <a name="review-the-transaction-line-count"></a>Überprüfen Sie die Zeilenzahl der Transaktion

Ermitteln Sie, ob die Transaktion eine große Anzahl von Zeilen hat (z. B. mehr als mehrere hundert). Wenn das nicht der Fall ist, fahren Sie mit dem nächsten Abschnitt fort. Wenn die Transaktion mehrere hundert Zeilen hat, verzögern Sie die Steuerberechnung. Weitere Informationen finden Sie unter [Verzögerte Steuerberechnung für Erfassungen aktivieren](enable-delayed-tax-calculation.md). 

Als nächstes können Sie feststellen, ob eine der folgenden Bedingungen erfüllt ist:

- Es gibt Import-Transaktionen aus großen Dateien.
- Mehrere Sitzungen verarbeiten die gleiche Transaktion Steuerberechnung zur gleichen Zeit.
- Die Transaktion hat mehrere Zeilen, und die Ansichten werden in Echtzeit aktualisiert. Zum Beispiel wird das Feld **Berechneter Mehrwertsteuerbetrag** auf der Seite **Allgemeines Journal** in Echtzeit aktualisiert, wenn die Felder einer Zeile geändert werden.

   [![Feld „Berechneter Mehrwertsteuer-Betrag“ auf der Journal-Belegseite](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Wenn eine dieser Bedingungen erfüllt ist, verzögern Sie die Steuerberechnung.

## <a name="review-the-call-stack"></a>Überprüfen Sie den Call-Stack

Überprüfen Sie den Call-Stack, um festzustellen, ob die Steuerberechnung mehrfach aufgerufen wird. Wenn dies nicht der Fall ist, fahren Sie mit dem nächsten Abschnitt fort. Wenn der Call-Stack mehrfach aufgerufen wird, befolgen Sie diese Schritte, um die Steuerberechnungszeiten zu reduzieren.

1. Wenn die Erfassung die Transaktion berücksichtigt hat, verzögern Sie die Steuerberechnung. Weitere Informationen finden Sie unter [Verzögerte Steuerberechnung für Erfassungen aktivieren](enable-delayed-tax-calculation.md).
2. Wenn es sich bei der Transaktion um eine Bestellung handelt und die Anwendungsversion höher als 10.0.15 ist, können Sie die Steuerberechnung bis zur endgültigen Berechnung verzögern, indem Sie die Versionsverwaltung für **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** aktivieren.

## <a name="review-the-call-stack-timeline"></a>Überprüfen Sie die Call-Stack-Zeitleiste

Überprüfen Sie die Call-Stack-Zeitleiste, um festzustellen, ob die folgenden Probleme bestehen. Wenn dies der Fall ist, aktivieren Sie das Fluging für **TaxUncommittedDoIsolateScopeFlighting**, um das Problem zu beheben.

- Die Transaktion bewirkt, dass das System nicht mehr reagiert, bis die Sitzung beendet ist. Daher kann die Transaktion das steuerliche Ergebnis nicht berechnen. Die folgende Abbildung zeigt das Nachrichtenfeld „Sitzung beendet“, das Sie erhalten.

    [![Nachricht „Sitzung beendet“](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- Die Methoden **TaxUncommitted** benötigen mehr Zeit als andere Methoden. In der folgenden Abbildung benötigt z. B. die Methode **TaxUncommitted ::updateTaxUncommitted()** 43.347,42 Sekunden, aber andere Methoden benötigen 0,09 Sekunden.

    [![Dauer der Methode](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Anpassen und Aufruf der Steuerberechnung

Wenn Sie eine Anpassung vornehmen, rufen Sie die Steuerberechnung nicht bei der Methode **insert()** oder **update()** für jede Zeile auf. Die Steuerberechnung sollte auf Transaktionsebene aufgerufen werden.

## <a name="determine-whether-customization-exists"></a>Ermitteln Sie, ob eine Anpassung vorliegt

Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist. Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
