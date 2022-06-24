---
title: Materielle Ersetzung in der Fertigung
description: In diesem Artikel wird beschrieben, wie Materialien während des Produktionsprozesses ersetzt werden.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c2e6c9cc8ed85c8c60539b37fb6c51c96bc2872
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855977"
---
# <a name="material-substitution-in-manufacturing"></a>Materielle Ersetzung in der Fertigung

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Materialien während des Produktionsprozesses ersetzt werden. 

Es gibt drei Methoden für das Ersetzen von Materialien während des Produktionsprozesses:

-   Bis zu Datum, wenn ein Material nach einem bestimmten Datum durch ein anderes ersetzt wird
-   Während des Produktprogrammplans, wenn ein Material in einer Formel mit einem anderen Material ersetzt wird, da es nicht vorrätig ist
-   Während der Produktion, wenn ein Material unerwartet nicht vorrätig ist und mit einem anderen Material ersetzt wird

## <a name="substituting-material-by-date"></a>Ersetzen des Materials nach Datum
Stellen Sie sich folgendes Szenario vor: Eine Maschine, die von einem Unternehmen hergestellt wird, enthält eine Komponente, die in zweit Monaten aus dem Lieferantenkatalog gestrichen wird. Ab dem Ablaufdatum bietet der Lieferant eine neue Komponente an, die die alte ersetzen kann. Das Gültigkeitsdaten Von und Bis können in Stückliste (BOM)- Positionen eingerichtet werden. In vorliegenden Beispiel richten Sie die alte Komponente so ein, dass sie abläuft, indem Sie das Ablaufdatum im Feld **Bis-Datum** eingeben. Auf der Stückliste, richten Sie die neue Ersetzungskomponente so ein, dass sie von dem Tag gültig ist, nachdem die alte Komponente abläuft. Hierfür geben Sie das Startdatum im **Von-Datum** Feld ein.

## <a name="substituting-material-by-planning"></a>Ersetzen des Materials nach Planung
Sie können Materialien bei der Planung nur dann ersetzen, wenn Sie Formeln verwenden und nicht, wenn Sie eine Stückliste verwenden. Betrachten wir das folgende Szenario: Ein Lebensmittelproduktionsunternehmen erstellt eine Soße aus einer Formel, die 20 Inhaltsstoffe hat. Ein einzelnes Element in der Formel kann durch eine von zwei anderen Zutaten ersetzt werden. Da jedoch diese beiden Inhaltsstoffe teurer als die bevorzugten Hauptzutat sind, wird Ersatz verwendet, wenn der bevorzugte Hauptzutat nicht vorrätig ist. Das Material, das ersetzt werden kann, wird mit A bezeichnet, während die beiden Materialien, die sie ersetzen können, B und C sind. Materialersatz durch Planung wird durch die Felder **Plangruppe** und **Priorität** in den Formelpositionen gesteuert. In vorliegenden Beispiel erstellen Sie Formelpositionen für die drei Materialien und ordnen die Formelpositionen mit derselben Plangruppe zu. In der Einstellungen hat die Formelposition für Material A die höchste Priorität (niedrigste Nummer), die Formelposition für Liste C besitzt die niedrigste Priorität, und die Formelposition für Material B hat eine Priorität, die zwischen der Priorität der übrigen beiden Positionen ist. Wenn Sie Bedarf für den Artikel haben, bestimmt Produktprogrammplan zuerst, ob der Bedarf für Material A abgedeckt werden kann. Wenn der Bedarf nicht abgedeckt werden kann, berücksichtigt Produktprogrammplan Materialien B und C, in Reihenfolge der Priorität. Wenn Material B verfügbar ist, wird es verwendet, nachdem ein Chargenbestellvorschlag für die Formel umgewandelt ist. Falls keines der Materialien verfügbar sind, erstellt Produktprogrammplan ein Bestellvorschlag für Material A. **Hinweis:** Wenn Sie Formelpositionen in einer Plangruppe einrichten, sollten Sie nur eine Menge für das Material angeben, das die höchste Priorität hat. Diese Menge wird verwendet, um den Bedarf aller Materialien im Plan, auch die Materialien zu berechnen, die untere Priorität haben. Sie können nicht unterschiedliche Mengen für Artikel mit niedrigerer Priorität in der Plangruppe angeben.

## <a name="substituting-material-during-production"></a>Ersetzen des Materials während der Produktion
Betrachten wir das folgende Szenario: Ein Artikel der Metallplatte ist für einen Schweißensarbeitsgang erforderlich. Während des Arbeitsgangs informiert ein Lagerarbeiter den Maschinenbediener, dass die Platte nicht vorrätig ist. Jedoch wird beschlossen, dass die Platte mit einer Platte ersetzt werden kann, die etwas stärker ist. Daher kann der Arbeitsgang abgeschlossen werden. Material kann die Stückliste für einen offenen Produktionsauftrag hinzugefügt werden. Wenn der Produktionsauftrag den **Gestartet** Status aufweist, werden Benutzer aufgefordert, den Auftrag erneut zu schätzen, wenn sie ein neues Element der Produktionsstückliste hinzufügen. Nachdem das Material hinzugefügt wurde, kann eine neue Kommissionierliste für das neue Element erstellt werden. Sie müssen das neue Material nicht der Produktionsstückliste hinzufügen. Stattdessen können Sie diese direkt auf die Produktionskommissionierliste hinzufügen. Wird anschließend die Kommissionierliste gebucht, fügt das System das Material der Produktionsstückliste hinzu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]