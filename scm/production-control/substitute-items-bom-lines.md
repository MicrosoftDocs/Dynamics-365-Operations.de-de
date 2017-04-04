---
title: Materielle Ersetzung in der Fertigung
description: "In diesem Thema wird beschrieben, wie Materialien während des Produktionsprozesses ersetzt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 1d6f16cad4c985a5628e2589aece8e628c83ef22
ms.lasthandoff: 03/31/2017


---

# <a name="material-substitution-in-manufacturing"></a>Materielle Ersetzung in der Fertigung

In diesem Thema wird beschrieben, wie Materialien während des Produktionsprozesses ersetzt werden. 

Es gibt drei Methoden für das Ersetzen von Materialien während des Produktionsprozesses:

-   Bis zu Datum, wenn ein Material nach einem bestimmten Datum durch ein anderes ersetzt wird
-   Während des Produktprogrammplans, wenn ein Material in einer Formel mit einem anderen Material ersetzt wird, da es nicht vorrätig ist
-   Während der Produktion, wenn ein Material unerwartet nicht vorrätig ist und mit einem anderen Material ersetzt wird

## <a name="substituting-material-by-date"></a>Ersetzen des Materials nach Datum
Consider nach Szenario: Eine Maschine, dass ein Unternehmen erstellen, enthält eine Komponente, die aus dem Kreditorenkatalog in zwei Monate abläuft. Über Ablaufdatum vorwärts, bietet der Kreditor einer neuen Komponente an, die für die Komponente alte ersetzt werden kann. Das Gültigkeitsdaten Von und Bis können in Stückliste (BOM)- Positionen eingerichtet werden. In vorliegenden Beispiel richten Sie die alte Komponente so ein, dass sie abläuft, indem Sie das Ablaufdatum im Feld **Bis-Datum** eingeben. Auf der Stückliste, richten Sie die neue Ersetzungskomponente so ein, dass sie von dem Tag gültig ist, nachdem die alte Komponente abläuft. Hierfür geben Sie das Startdatum im **Von-Datum** Feld ein.

## <a name="substituting-material-by-planning"></a>Ersetzen des Materials nach Planung
Sie können Materialien bei der Planung nur dann ersetzen, wenn Sie Formeln verwenden und nicht, wenn Sie eine Stückliste verwenden. Betrachten wir das folgende Szenario: Ein Lebensmittelproduktionsunternehmen erstellt eine Soße aus einer Formel, die 20 Inhaltsstoffe hat. Ein einzelnes Element in der Formel kann durch eine von zwei anderen Zutaten ersetzt werden. Da jedoch diese beiden Inhaltsstoffe teurer als die bevorzugten Hauptzutat sind, wird Ersatz verwendet, wenn der bevorzugte Hauptzutat nicht vorrätig ist. Das Material, das ersetzt werden kann, wird mit A bezeichnet, während die beiden Materialien, die sie ersetzen können, B und C sind. Materialersatz durch Planung wird durch die Felder **Plangruppe** und **Priorität** in den Formelpositionen gesteuert. In vorliegenden Beispiel erstellen Sie Formelpositionen für die drei Materialien und ordnen die Formelpositionen mit derselben Plangruppe zu. In der Einstellungen hat die Formelposition für Material A die höchste Priorität (niedrigste Nummer), die Formelposition für Liste C besitzt die niedrigste Priorität, und die Formelposition für Material B hat eine Priorität, die zwischen der Priorität der übrigen beiden Positionen ist. Wenn Sie Bedarf für den Artikel haben, bestimmt Produktprogrammplan zuerst, ob der Bedarf für Material A abgedeckt werden kann. Wenn der Bedarf nicht abgedeckt werden kann, berücksichtigt Produktprogrammplan Materialien B und C, in Reihenfolge der Priorität. Wenn Material B verfügbar ist, wird es verwendet, nachdem ein Chargenbestellvorschlag für die Formel umgewandelt ist. Falls keines der Materialien verfügbar sind, erstellt Produktprogrammplan ein Bestellvorschlag für Material A. **Hinweis:** Wenn Sie Formelpositionen in einer Plangruppe einrichten, sollten Sie nur eine Menge für das Material angeben, das die höchste Priorität hat. Diese Menge wird verwendet, um den Bedarf aller Materialien im Plan, auch die Materialien zu berechnen, die untere Priorität haben. Sie können nicht unterschiedliche Mengen für Artikel mit niedrigerer Priorität in der Plangruppe angeben.

## <a name="substituting-material-during-production"></a>Ersetzen des Materials während der Produktion
Betrachten wir das folgende Szenario: Ein Artikel der Metallplatte ist für einen Schweißensarbeitsgang erforderlich. Während des Arbeitsgangs informiert ein Lagerarbeiter den Maschinenbediener, dass die Platte nicht vorrätig ist. Jedoch wird beschlossen, dass die Platte mit einer Platte ersetzt werden kann, die etwas stärker ist. Daher kann der Arbeitsgang abgeschlossen werden. Material kann die Stückliste für einen offenen Produktionsauftrag hinzugefügt werden. Wenn der Produktionsauftrag den **Gestartet** Status aufweist, werden Benutzer aufgefordert, den Auftrag erneut zu schätzen, wenn sie ein neues Element der Produktionsstückliste hinzufügen. Nachdem das Material hinzugefügt wurde, kann eine neue Kommissionierliste für das neue Element erstellt werden. Sie müssen das neue Material nicht der Produktionsstückliste hinzufügen. Stattdessen können Sie diese direkt auf die Produktionskommissionierliste hinzufügen. Wird anschließend die Kommissionierliste gebucht, fügt das System das Material der Produktionsstückliste hinzu.


