---
title: Zahlungsmethoden für Retouren ohne Beleg beschränken
description: In diesem Thema wird beschrieben, wie bestimmte Zahlungsarten für die Rückerstattung eingeschränkt werden können, wenn die Rücksendung ohne Beleg erfolgt.
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "315911"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Zahlungsmethoden für Retouren ohne Beleg beschränken

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Jeder Zahlungstyp, der von einem Einzelhändler akzeptiert wird, muss beim Einrichten des Systems konfiguriert werden. In diesem Thema wird beschrieben, wie bestimmte Zahlungsarten für die Rückerstattung eingeschränkt werden können, wenn die Rücksendung ohne Beleg erfolgt.

## <a name="set-up-payment-methods"></a>Einrichten von Zahlungsmethoden

Zum Einrichten von Zahlungsmethoden müssen die folgenden Aufgaben abgeschlossen sein.
1. Erstellen Sie die Zahlungsmethoden, die von der gesamten Organisation akzeptiert werden.
2. Einrichten von organisationsweiten Kartentypen und Kartennummern Wenn Kredit- oder Debitkarten akzeptiert werden, müssen Sie eine Zahlungsmethode für Karten und anschließend die organisationsweiten Kartentypen und Kartennummern erstellen.
3. Einrichten von Shopzahlungsmethoden. Ordnen Sie die Zahlungsmethoden den einzelnen Shops zu, und geben Sie dann für jede Zahlungsmethode shopspezifische Einstellungen ein.
4. Einrichten von Kartenzahlungsmethoden für Shops Schließen Sie für alle Zahlungsmittel vom Typ "Karte", die im Shop akzeptiert werden, die Karteneinrichtung ab.

![Einzelhandelsshop-Setup](media/NoReceiptReturns1.png "Einzelhandelsshop-Setup") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Zahlungsmethoden für Retouren ohne Beleg beschränken

Setzen Sie für jede Shop-Zahlungsmethode auf der Seite **Einzelhandelsshopleitung** unter **Retouren ohne Beleg** **Beschränkung für Rückerstattungen ohne Beleg** auf **Ja**. 

Der Standardwert des Umschalters ist **Nein**, wodurch sichergestellt wird, dass der Zahlweg für Rückerstattungen zugelassen wird. 

Wenn **Beschränkung für Rückerstattungen ohne Beleg** auf **Ja** gesetzt ist, wird die gewählte Zahlungsmethode für Rückerstattungen nicht zugelassen. 

![Zahlungsmethode im Einzelhandel](media/NoReceiptReturns3.png "Zahlungsmethode im Einzelhandel") 

> [!NOTE]
> Wenn ein Kassierer eine Zahlungsmethode auswählt, die ohne Beleg für die Rückerstattung eingeschränkt ist, wird eine Meldung angezeigt, um die zulässigen Zahlungsmethoden zu überprüfen.

![Akzeptierte Zahlungsmethoden](media/NoReceiptReturns4.png "Akzeptierte Zahlungsmethoden") 

Wenn eine Transaktion sowohl eine quittierte Rücksendung als auch eine Rücksendung ohne Beleg hat, werden die Einschränkungsbedingungen nicht durchgesetzt, da es sich bei der Transaktion um einen Rückgabe-Workflow mit Beleg handelt. 

