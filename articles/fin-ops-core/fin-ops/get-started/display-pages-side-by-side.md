---
title: Seiten mithilfe der Funktion „In neuem Fenster öffnen“ nebeneinander anzeigen
description: In diesem Artikel wird beschrieben, wie Bildseiten parallel angezeigt werden.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ade352edf31fe895a9b9118a8ad7d5fe6c0bde
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798402"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Seiten mithilfe der Funktion „In neuem Fenster öffnen“ nebeneinander anzeigen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Bildseiten parallel angezeigt werden.

Sie möchten vielleicht mehrere Seiten nebeneinander anzeigen, um Aufgaben schnell abzuschließen. Beispielsweise möchten Sie Positionen in mehreren Erfassung prüfen oder eingeben. In der Regel müssen Sie zur Prüfung oder Eingabe von Positionen in mehrere Erfassungen zwischen der Seite, die eine Liste der Erfassungen anzeigt, und der Seite, die die Positionen für eine bestimmte Erfassung angibt, hin und her wechseln. Wenn Sie jedoch die Funktion **In neuem Fenster öffnen** aktivieren, können Sie diese parallelen Seiten anzeigen und Ihre Aufgaben schneller ausführen.

Wenn Sie die Positionen, wie im Beispiel beschrieben, anzeigen, können Sie auf das Symbol **In neuem Fenster öffnen** klicken.

[![Klicken Sie auf das Symbol „In neuem Fenster öffnen“.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Wenn Sie auf das Symbol **In neuem Fenster öffnen** klicken, öffnet sich die Positionsseite in einem neuen Popupbrowser und navigiert dann den ursprünglichen Browser zurück in der Historie zur Seite, die die Liste der Erfassungen anzeigte. Sie können nun beide Seiten nebeneinander anzeigen. Nach dem Anzeigen einer Erfassung können Sie die ausgewählte Erfassung auf der Erfassungslistenseite ändern, und die Positionsseite im Popupfenster zeigt automatisch die Positionen der neu ausgewählten Erfassung an.

[![Sie können Seiten nebeneinander anzeigen.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Das dynamische Verknüpfen und Aktualisieren geschieht aufgrund der Beziehungen, die zwischen den Daten bestehen, die diese Seiten unterstützen. Wenn das System die Beziehung zwischen den Daten nicht erkennt, aktualisiert sich das Popupfenster nicht automatisch als Reaktion auf eine Änderung im dem Fenster, von dem es erzeugt wurde.

Einige Seiten verwenden mehrere Ansichten wie die Rasteransicht, Kopfzeilenansichts- und Detailansicht. Das Symbol **In neuem Fenster öffnen** sorgt dafür, dass die gesamte Seite in einem neuen Browserfenster geöffnet wird. Daher können Sie zwei Ansichten derselben Seite nicht mithilfe der Funktion **In neuem Fenster öffnen** anzeigen. Fast all diese Seiten haben jedoch eine Navigationsliste, die Sie verwenden können, um zwischen Datensätzen zu wechseln und ähnliche Ergebnisse zu erreichen.

Vor der Verwendung der Funktion **In neuem Fenster öffnen** sollten Sie den Popupblocker des Browsers konfigurieren, um Einblendungen der URL der Website zu ermöglichen. Zum Beispiel können Sie Einblendungen von "\*.dynamics.com" ermöglichen.

Die Funktion **In neuem Fenster öffnen** ist nur verfügbar, wenn es mehr als eine Seite gibt, die im Fenster geöffnet ist. Zudem schließt sich das Popupfenster automatisch, wenn es keine offene Seiten gibt (das heißt, wenn Sie die letzte Seite in diesem Fenster schließen). Das System schließt offene Seiten auch dann, wenn Sie in einen anderen Bereich in der Anwendung navigieren. Wenn Sie geöffnete Popupfenster haben und in einen anderen Bereich in der Anwendung navigieren, werden die Popupfenster automatisch geschlossen, da die Seiten in diesen Dialogfeldern vom System geschlossen wurden.

In der oberen Leiste in den Popupfenstern werden Informationen zum Unternehmen, in dem die Seite in geöffnet wurde, angezeigt und sind schreibgeschützt. Die Popupfenster beruhen auch auf dem Hauptbrowserfenster. Wenn das Hauptfenster geschlossen oder aktualisiert wird, werden alle offenen Popupfenster schreibgeschützt. Wenn diese Situation eintritt, können Sie die Informationen zwar weiterhin in diesen Dialogfeldern anzeigen, aber nicht mit ihnen interagieren.
