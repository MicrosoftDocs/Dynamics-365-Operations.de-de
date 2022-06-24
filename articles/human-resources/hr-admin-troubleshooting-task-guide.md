---
title: Aufgabenleitfäden in LCS speichern und erneut wiedergeben
description: In diesem Artikel wird erläutert, wie Aufgabenleitfäden in Microsoft Dynamics Lifecycle Services (LCS) gespeichert und dann wiedergegeben werden.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2efe48a31db533c5f22d4174cc6897f4a590cf49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875799"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Aufgabenleitfäden in LCS speichern und erneut wiedergeben


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Umgebungsdetails** 

Microsoft Dynamics 365 Human Resources, das über Microsoft Dynamics Lifecycle Services (LCS) bereitgestellt wurde

**Abgang**

Kunden möchte neue Aufgabenaufzeichnungen im LCS-Projekt speichern und dann die gespeicherten Aufgabenleitfäden wiedergeben.

**Lösung**

Folgen Sie diesen Schritten, um eine Aufgabenaufzeichnung in LCS zu speichern.

1. Melden Sie sich bei LCS an, und wählen Sie das Projekt aus.
2. Wählen Sie die Kachel **Geschäftsprozessmodellierer** aus.
3. Zeigen Sie die Seite in der „Aktualisierte BPM-Benutzeroberfläche” an.
4. Wählen Sie eine Bibliothek aus, und wählen Sie dann **Kopieren** aus.
5. Geben Sie einen Namen für das Modell des Geschäftsprozessmodellierers (BPM) an.
6. Melden Sie sich bei Human Resources von LCS an.
7. Geben Sie im Feld **Suche** den Text **Hilfe** ein. Lifecycle Services-Hilfe wird geöffnet.
8. Wählen Sie die Schaltfläche **Aktualisieren** für die Konfiguration der Lifecycle Services-Hilfe aus.

    Ihre neue BPM-Bibliothek sollte angezeigt werden und aktiv sein.

9. Schließen Sie die Seite.
10. Erstellen Sie eine Aufgabenaufzeichnung.
11. Wenn Sie fertig sind, wählen Sie **In Lifecycle Services speichern** aus.

    ![In Lifecycle Services speichern.](media/task-guides.png)

12. Wählen Sie die BPM-Bibliothek und -Knoten aus, um der Aufgabenaufzeichnung zu speichern.

Gehen Sie folgendermaßen vor, um einen Aufgabenleitfaden von LCS wiederzugeben.

1. Starten Sie die Aufgabenaufzeichnung.
2. Wählen Sie **Von LCS aus öffnen** aus.
3. Wählen Sie die Bibliothek und den BPM-Knoten aus, die den gespeicherten Aufgabenleitfaden haben.
4. Öffnen Sie den Aufgabenleitfaden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
