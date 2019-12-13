---
title: Optimieren Sie die Leistung mit automatischen Bereinigungsaufgaben
description: In diesem Thema wird erläutert, wie einige Leistungsprobleme mit Microsoft Dynamics 365 Talent behoben werden, indem Sie den Verlauf der Stapelverarbeitungsaufträge bereinigen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a053c9094151f4e12e4aadc533dd272258779540
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832581"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimieren Sie die Leistung mit automatischen Bereinigungsaufgaben

[!include [banner](includes/banner.md)]

**Abgang**

Microsoft Dynamics 365 Talent kann Leistungsprobleme aufweisen, wenn der Verlauf der Stapelverarbeitungsaufträge zu umfangreich wird.

**Ursache**

Stapelverarbeitungsaufträge, die oft ausgeführt werden, können so umfangreich werden, dass sie sich nicht mehr verwalten lassen. Dieses kann zu Leistungsproblemen führen. 

**Lösung**

Planen Sie eine automatische Aufgabe, um den Verlauf der Stapelverarbeitungsaufträge zu bereinigen. Es wird empfohlen, die Aufgabe wöchentlich auszuführen, Sie müssen jedoch möglicherweise die Bereinigung häufiger ausführen, je nach Größe Ihrer Umgebung. Die folgenden Verfahren enthalten unsere empfohlenen Einstellungen, die Sie Ihren Anforderungen entsprechend ändern können.

1. Wählen Sie in Talent **Systemverwaltung** aus.

2. Geben Sie auf der Leiste **Suchen** **Verlauf der Stapelverarbeitungsaufträge bereinigen** ein.

   ![Suche nach „Verlauf der Stapelverarbeitungsaufträge bereinigen“](media/talent-batch-history-cleanup-search-bar.png)

3. In **Historienlimit (Tage)** geben Sie **30** ein.

   ![Historienlimit auf 30 festlegen](media/talent-batch-history-cleanup-history-limit.png)

4. Wählen Sie **Im Hintergrund ausführen** und **Wiederholung** aus.

   ![Wiederholung festlegen](media/talent-batch-history-cleanup-recurrence.png)

5. Unter **Wiederholung definieren** legen Sie die Option **Startdatum** und **Startzeit** fest, um während der Arbeitszeit oder am Wochenende auszuführen, und wählen Sie dann **KEIN ENDDATUM** aus. 

   ![Startdatum und -zeit der Wiederholung definieren](media/talent-batch-history-cleanup-define-recurrence.png)

6. Wählen Sie unter **WIEDERHOLUNGSMUSTER** die Option **Tage** aus und legen Sie **NACH DEM ANGEGEBENEN INTERVALL WIEDERHOLEN** auf **7** fest.

   ![Legen Sie fest, dass die Bereinigung wöchentlich ausgeführt wird](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Wählen Sie **OK**.

8. Ändern Sie ggf. weitere Parameter unter **Im Hintergrund ausführen** und wählen Sie dann **OK** aus.

