---
title: Power Apps-Apps in Dynamics 365 Human Resources einbetten
description: In diesem Thema wird erläutert, wie das Problem des aus dem Systemverwaltungsmodul verschwundenen Microsoft Power Apps-Menüs gelöst wird.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017872"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Power Apps-Apps in Dynamics 365 Human Resources einbetten

**Abgang**

Die Menüoption **Power Apps** ist aus dem Modul **Systemverwaltung** verschwunden.

**Ursache**

Das Design der Benutzeroberfläche (UI) wurde verändert, und Microsoft Power Apps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.

**Lösung**

Die Art und Weise, wie Power Apps jetzt eingebettet ist, hat sich geändert. Power Apps wird jetzt über das Personalisierungsmodell hinzugefügt. Sie können Power Apps fast allen Seiten in Microsoft Dynamics 365 Talent hinzufügen.

Informationen zum Einbetten von Power Apps in Talent finden Sie unter [Einbetten von Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jeder Power Apps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.

Die Schaltfläche **Power Apps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent. Sie können diese Schaltfläche verwenden, um eine Apps einzufügen.

Hier ist ein Beispiel.

1. Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.
2. Wählen Sie die Schaltfläche **Power Apps** und dann **Fügen Sie eine App von Power Apps** hinzu.

    ![Power Apps-Schaltfläche](media/png.png)

3. Füllen Sie die Felder im Dialogfeld **Eine App von Power Apps** hinzufügen ausfüllen.

    ![Fügen Sie eine App aus dem Dialogfeld Power Apps hinzu](media/insert-powerapp.png)

Gehen Sie alternativ folgendermaßen vor.

1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Diese Seite personalisieren** aus.

    ![Gruppe „Personalisieren“ in der Registerkarte „Optionen”](media/options.png)

    Die Personalisierungssymbolleiste wird angezeigt.

2. Wählen Sie in der Symbolleiste **Eine App von Power Apps** hinzufügen.

    ![Eine App von Power Apps mithilfe der Personalisierungssymbolleiste hinzufügen](media/powerapp-bar.png)
