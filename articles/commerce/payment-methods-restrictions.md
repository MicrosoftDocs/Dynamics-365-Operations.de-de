---
title: Zahlungsmethoden für Retouren ohne Beleg beschränken
description: In diesem Thema wird beschrieben, wie bestimmte Zahlungsarten für die Rückerstattung eingeschränkt werden können, wenn die Rücksendung ohne Beleg erfolgt.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: dfc49e3c3132fe2687ea71e5da75fe31753d57f9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022708"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Zahlungsmethoden für Retouren ohne Beleg beschränken


[!include [banner](includes/banner.md)]

Jeder Zahlungstyp, der von einem Einzelhändler akzeptiert wird, muss beim Einrichten des Systems konfiguriert werden. In diesem Thema wird beschrieben, wie bestimmte Zahlungsarten für die Rückerstattung eingeschränkt werden können, wenn die Rücksendung ohne Beleg erfolgt.

## <a name="set-up-payment-methods"></a>Einrichten von Zahlungsmethoden

Zum Einrichten von Zahlungsmethoden müssen die folgenden Aufgaben abgeschlossen sein.
1. Erstellen Sie die Zahlungsmethoden, die von der gesamten Organisation akzeptiert werden.
2. Einrichten von organisationsweiten Kartentypen und Kartennummern Wenn Kredit- oder Debitkarten akzeptiert werden, müssen Sie eine Zahlungsmethode für Karten und anschließend die organisationsweiten Kartentypen und Kartennummern erstellen.
3. Einrichten von Shopzahlungsmethoden. Ordnen Sie die Zahlungsmethoden den einzelnen Shops zu, und geben Sie dann für jede Zahlungsmethode shopspezifische Einstellungen ein.
4. Einrichten von Kartenzahlungsmethoden für Shops Schließen Sie für alle Zahlungsmittel vom Typ "Karte", die im Shop akzeptiert werden, die Karteneinrichtung ab.

![Geschäft einrichten](media/NoReceiptReturns1.png "Retail-Setup bei Shop") 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a>Zahlungsmethoden für Retouren ohne Beleg beschränken

Setzen Sie für jede Shop-Zahlungsmethode auf der Seite **Shopverwaltung** unter **Retouren ohne Beleg** **Beschränkung für Rückerstattungen ohne Beleg** auf **Ja**. 

Der Standardwert des Umschalters ist **Nein**, wodurch sichergestellt wird, dass der Zahlweg für Rückerstattungen zugelassen wird. 

Wenn **Beschränkung für Rückerstattungen ohne Beleg** auf **Ja** gesetzt ist, wird die gewählte Zahlungsmethode für Rückerstattungen nicht zugelassen. 

![Zahlungsmethoden im Shop](media/NoReceiptReturns3.png "Retail-Zahlungsmethode in Shop") 

> [!NOTE]
> Wenn ein Kassierer eine Zahlungsmethode auswählt, die ohne Beleg für die Rückerstattung eingeschränkt ist, wird eine Meldung angezeigt, um die zulässigen Zahlungsmethoden zu überprüfen.

![Zulässige Zahlungsmethoden](media/NoReceiptReturns4.png "Zulässige Zahlungsmethoden") 

Wenn eine Transaktion sowohl eine quittierte Rücksendung als auch eine Rücksendung ohne Beleg hat, werden die Einschränkungsbedingungen nicht durchgesetzt, da es sich bei der Transaktion um einen Rückgabe-Workflow mit Beleg handelt. 

