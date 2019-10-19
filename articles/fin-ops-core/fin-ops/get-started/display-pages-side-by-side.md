---
title: Seiten mithilfe des Symbols „In neuem Fenster öffnen” nebeneinander anzeigen
description: In diesem Artikel wird beschrieben, wie Bildseiten parallel angezeigt werden.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180690"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>Seiten mithilfe des Symbols „In neuem Fenster öffnen” nebeneinander anzeigen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Bildseiten parallel angezeigt werden.

Sie möchten vielleicht mehrere Seiten nebeneinander anzeigen, um Aufgaben schnell abzuschließen. Beispielsweise möchten Sie Positionen in mehreren Erfassung prüfen oder eingeben. In der Regel müssen Sie zu diesem Zweck zwischen der Seite, die eine Liste der Erfassungen anzeigt und der Seite, die die Positionen für eine bestimmte Erfassung angibt, hin und her wechseln. Wenn Sie jedoch die Funktion **In neuem Fenster öffnen** aktivieren, können Sie diese parallelen Seiten anzeigen und Ihre Aufgaben schneller ausführen.

Wenn Sie die Positionen, wie im Beispiel beschrieben, anzeigen, können Sie auf das Symbol **In neuem Fenster öffnen** klicken.

[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Wenn Sie auf das Symbol **In neuem Fenster öffnen** klicken, öffnet sich die Positionsseite in einem neuen Popupbrowser und navigiert dann den ursprünglichen Browser zurück in der Historie zur Seite, die die Liste der Erfassungen anzeigte. Sie können nun beide Seiten nebeneinander anzeigen. Wenn Sie die Erfassung nicht mehr angezeigt werden soll, können Sie die ausgewählte Erfassung auf der Erfassungslistenseite ändern, und die Positionsseite im Popupfenster zeigt automatisch die Positionen der neu ausgewählten Erfassung an.

[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Das dynamische Verknüpfen und Aktualisieren geschieht aufgrund der Beziehungen, die zwischen den Daten bestehen, die diese Seiten unterstützen. Wenn das System die Beziehung zwischen den Daten nicht erkennt, aktualisiert sich das Popupfenster nicht automatisch als Reaktion auf eine Änderung im dem Fenster, von dem es erzeugt wurde.

Einige Seiten verwenden mehrere Ansichten wie die Rasteransicht, Kopfzeilenansichts- und Detailansicht. Das **In neuem Fenster öffnen** Symbol sorgt dafür, dass die gesamte Seite, in einem neuen Browserfenster geöffnet wird. Daher können Sie zwei Ansichten der selben Seite nicht mithilfe der Funktion **In neuem Fenster öffnen** anzeigen. Fast all diese Seiten haben jedoch eine Navigationsliste, die Sie verwenden können, um zwischen Datensätzen zu wechseln und ähnliche Ergebnisse zu erreichen.

Vor der Verwendung der Funktion **In neuem Fenster öffnen** sollten Sie den Popupblocker des Browsers konfigurieren, um Einblendungen der URL der Website zu ermöglichen. Zum Beispiel können Sie Einblendungen von "\*.dynamics.com" ermöglichen.

Die Funktion **In neuem Fenster öffnen** ist nur verfügbar, wenn es mehr als eine Seite gibt, die im Fenster geöffnet ist. Zudem schließt sich das Popupfenster automatisch, wenn es keine offene Seiten gibt (das heißt, wenn die letzte Seite in diesem Fenster geschlossen ist). Das System schließt offene Seiten auch dann, wenn Sie in einen anderen Bereich in der Anwendung navigieren. Wenn Sie geöffnete Popupfenster haben und in einen anderen Bereich in der Anwendung navigieren, werden die Popupfenster automatisch geschlossen, da die Seiten in diesen Dialogfeldern vom System geschlossen wurden.

In der oberen Leiste in den Popupfenstern werden Informationen zum Unternehmen, in dem die Seite in geöffnet wurde, angezeigt und sind schreibgeschützt. Die Popupfenster beruhen auch auf dem Hauptbrowserfenster. Wenn das Hauptfenster geschlossen oder aktualisiert wird, werden alle offenen Popupfenster schreibgeschützt. Das bedeutet, dass die Informationen in diesen Dialogfeldern noch angezeigt werden können, aber Sie nicht in der Lage sind, mit ihnen zu interagieren.
