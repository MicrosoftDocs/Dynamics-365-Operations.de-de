---
title: Einbetten von PowerApps-Apps in Core HR
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, bei dem das PowerApps-Menü aus dem Systemverwaltungsmodul verschwunden ist.
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
ms.openlocfilehash: 7c0dcdd7e2f407267cf99906b4d0b317858710af
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742818"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>Einbetten von PowerApps-Apps in Core HR

[!include [banner](includes/banner.md)]

**Abgang**

Die Menüoption **PowerApps** ist aus dem Modul **Systemverwaltung** verschwunden.

**Ursache**

Das Design der Benutzeroberfläche (UI) wurde verändert, und Microsoft PowerApps ist jetzt im standardmäßigen Personalisierungsmodell enthalten.

**Auflösung**

Die Art und Weise, wie PowerApps-Apps jetzt eingebettet sind, hat sich geändert. PowerApps-Apps werden jetzt durch das Personalisierungsmodell hinzugefügt. Sie können PowerApps-Apps zu fast allen Seiten in Microsoft Dynamics 365 for Talent hinzufügen.

Ausführliche Informationen dazu, wie PowerApps-Apps in Talent eingebettet werden, finden Sie unter [PowerApps-Apps einbetten](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Jeder PowerApps-Kunde, der Apps vor der Änderung eingebettet hat, sollte auf das neue Modell aktualisiert worden sein.

Die Schaltfläche **PowerApps** befindet sich in der oberen rechten Ecke beinahe jeder Seite in Talent. Sie können diese Schaltfläche verwenden, um eine PowerApps-App einzufügen.

Hier ist ein Beispiel.

1. Wechseln Sie zu **Personalverwaltung \> Links \> Arbeitskräfte \> Mitarbeiter**.
2. Wählen Sie die Schaltfläche **PowerApps** aus, und wählen Sie dann **Eine PowerApp einfügen** aus.

    ![PowerApps-Schaltfläche](media/png.png)

3. Füllen Sie die Felder im Dialogfeld **Eine PowerApp einfügen** aus.

    ![Ein PowerApp-Dialogfeld einfügen](media/insert-powerapp.png)

Gehen Sie alternativ folgendermaßen vor.

1. Wählen Sie im Aktivitätsbereich der Seite in der Registerkarte **Optionen** in der Gruppe **Personalisieren** die Option **Dieses Formular personalisieren** aus.

    ![Gruppe „Personalisieren” in der Registerkarte „Optionen”](media/options.png)

    Die Personalisierungssymbolleiste wird angezeigt.

2. Wählen Sie auf der Symbolleiste die Option **Einfügen \> PowerApp** aus.

    ![Eine PowerApps-App mithilfe der Personalisierungssymbolleiste einfügen](media/powerapp-bar.png)
