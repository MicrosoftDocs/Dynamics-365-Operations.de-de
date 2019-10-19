---
title: Einbetten von PowerApps-Apps in Dynamics 365 – Core HR
description: In diesem Thema wird erläutert, wie das Problem des aus dem Systemverwaltungsmodul verschwundenen PowerApps-Menüs gelöst wird.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008429"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>Einbetten von PowerApps-Apps in Core HR

[!include [banner](includes/banner.md)]

**Abgang**

Die Menüoption **PowerApps** ist aus dem Modul **Systemverwaltung** verschwunden.

**Ursache**

Das Design der Benutzeroberfläche (UI) wurde verändert, und Microsoft PowerApps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.

**Lösung**

Die Art und Weise, wie PowerApps jetzt eingebettet sind, hat sich geändert. PowerApps werden jetzt durch das Personalisierungsmodell hinzugefügt. Sie können PowerApps fast allen Seiten in Microsoft Dynamics 365 Talent hinzufügen.

Ausführliche Informationen zum Einbetten von PowerApps in Talent finden Sie unter [Einbetten von PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)

Jeder PowerApps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.

Die Schaltfläche **PowerApps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent. Sie können diese Schaltfläche verwenden, um eine PowerApps-App einzufügen.

Hier ist ein Beispiel.

1. Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.
2. Wählen Sie die Schaltfläche **PowerApps** und dann **PowerApp einfügen** aus.

    ![PowerApps-Schaltfläche](media/png.png)

3. Füllen Sie die Felder im Dialogfeld **Eine PowerApp einfügen** aus.

    ![Ein PowerApp-Dialogfeld einfügen](media/insert-powerapp.png)

Gehen Sie alternativ folgendermaßen vor.

1. Wählen Sie im Aktivitätsbereich der Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Dieses Formular personalisieren** aus.

    ![Gruppe „Personalisieren” in der Registerkarte „Optionen”](media/options.png)

    Die Personalisierungssymbolleiste wird angezeigt.

2. Wählen Sie auf der Symbolleiste die Option **Einfügen \> PowerApp** aus.

    ![Einfügen einer PowerApps-App mithilfe der Personalisierungssymbolleiste](media/powerapp-bar.png)
