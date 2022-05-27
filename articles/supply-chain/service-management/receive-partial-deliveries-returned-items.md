---
title: Empfangen von Teillieferungen zurückgelieferter Artikel
description: Teillieferungen werden in Bezug auf Rücklieferungspositionen und nicht Rücklieferungen definiert.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c0e27e3a5cb6be36a1d69190ce1b01ecada48a6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677113"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Empfangen von Teillieferungen zurückgelieferter Artikel    

[!include [banner](../includes/banner.md)]


Teillieferungen werden in Bezug auf Rücklieferungspositionen und nicht Rücklieferungen definiert.

Dies bedeutet, wenn die in einer Rücklieferungsposition angegebene volle Menge eingeht, jedoch kein Artikel aus den anderen Positionen in der Rücklieferung, dann ist die Lieferung keine Teillieferung. Um eine Teillieferung handelt es sich dagegen, wenn z. B. laut einer Rücklieferungsposition zehn Einheiten eines bestimmten Artikels zurückgeliefert werden sollen, jedoch nur vier Einheiten eingehen.

Wenn eine Rücklieferung weniger als die volle Menge einer Rücklieferungsposition enthält, können Sie die Lieferung ruhen lassen und auf den Eingang der restlichen zurückgelieferten Menge warten oder die Teillieferung erfassen und buchen.

## <a name="register-and-post-a-partial-quantity"></a>Erfassen und Buchen einer Teilmenge

1.  Nachdem Sie eine Rücklieferung für den Eingang im Formular **Wareneingangsübersicht - Lagerort: %1: Rampe %2, Erfassungsname: %3** ausgewählt haben, klicken Sie **Wareneingang starten**, um die Wareneingangserfassung zu erstellen, und klicken Sie anschließend **Erfassungen** \> **Wareneingänge aus Zugängen anzeigen**, um das Formular **Lagerplatzerfassung** zu öffnen.

2.  Wählen Sie die zu verwendende Erfassungsposition aus, und klicken Sie dann auf **Positionen**, um das Formular **Erfassungspositionen, Lagerplätze** zu öffnen.

3.  Wählen Sie die Position der Artikelnummer aus, für die nur eine Teilmenge eingegangen ist, und klicken Sie dann auf  **Funktionen** \> **Teilen**, um das Formular **Teilen** zu öffnen.

4.   **Geben Sie im Feld** die Menge für die Gesamtzahl der eingegangenen Artikel ein, und klicken Sie auf **OK**.

5.  **Wählen Sie im Formular** die Position für die eingegangene Artikelmenge aus, und klicken Sie auf **Buchen**. Die Position für die zusätzliche Menge kann nach Eingang der Artikel gebucht werden.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]