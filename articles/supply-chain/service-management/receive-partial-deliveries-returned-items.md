---
title: Empfangen von Teillieferungen zurückgelieferter Artikel
description: Teillieferungen werden in Bezug auf Rücklieferungspositionen und nicht Rücklieferungen definiert.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf35169d8afd6e88b8ebe921514ed6d55607a4dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428450"
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