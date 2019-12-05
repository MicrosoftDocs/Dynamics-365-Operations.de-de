---
title: Einbetten von Power Apps-Apps in Dynamics 365 – Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830208"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Einbetten von Power Apps-Apps in Dynamics 365 – Core HR

[!include [banner](includes/banner.md)]

**Abgang**

Die Menüoption **Power Apps** ist aus dem Modul **Systemverwaltung** verschwunden.

**Ursache**

Das Design der Benutzeroberfläche (UI) wurde verändert, und Microsoft Power Apps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.

**Lösung**

Die Art und Weise, wie Power Apps jetzt eingebettet ist, hat sich geändert. Power Apps wird jetzt über das Personalisierungsmodell hinzugefügt. Sie können Power Apps fast allen Seiten in Microsoft Dynamics 365 Talent hinzufügen.

Informationen zum Einbetten von Power Apps in Talent finden Sie unter [Einbetten von Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jeder Power Apps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.

Die Schaltfläche **Power Apps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent. Sie können diese Schaltfläche verwenden, um Power Apps einzufügen.

Hier ist ein Beispiel.

1. Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.
2. Wählen Sie die Schaltfläche **Power Apps** und dann **PowerApp einfügen** aus.

    ![Power Apps-Schaltfläche](media/png.png)

3. Füllen Sie die Felder im Dialogfeld **Eine PowerApp einfügen** aus.

    ![Ein PowerApp-Dialogfeld einfügen](media/insert-powerapp.png)

Gehen Sie alternativ folgendermaßen vor.

1. Wählen Sie im Aktivitätsbereich der Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Dieses Formular personalisieren** aus.

    ![Gruppe „Personalisieren” in der Registerkarte „Optionen”](media/options.png)

    Die Personalisierungssymbolleiste wird angezeigt.

2. Wählen Sie auf der Symbolleiste die Option **Einfügen \> PowerApp** aus.

    ![Einfügen einer Power Apps-App mithilfe der Personalisierungssymbolleiste](media/powerapp-bar.png)
