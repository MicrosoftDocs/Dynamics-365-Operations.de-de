---
title: Wartungsausfallzeit
description: In diesem Thema wird Wartungsausfallzeit in Asset Management beschrieben.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918243"
---
# <a name="maintenance-downtime"></a>Wartungsausfallzeit


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Sie können Wartungsausfallzeiterfassungen für die auf einem Arbeitsauftrag ausgewählte Anlage anlegen. Dies ist hilfreich, wenn Sie Wartungsausfallzeit auf einem oder mehreren Computern im Produktionsbereich erfassen möchten. Zunächst erstellen Sie die Ursachencodes für Wartungsausfallzeit, die Sie verwenden möchten, z.B. Ausfall und geplanter Stopp. Dies geschieht in den **Ursachencodes für Wartungsausfallzeit**. Als nächstes können Sie unter **Wartungsausfallzeit** Wartungsausfallzeiterfassungen anlegen und die entsprechenden Ursachencodes hinzufügen.

## <a name="create-maintenance-downtime-reason-codes"></a>Erstellen von Ursachencodes für Wartungsausfallzeit

1. Klicken Sie auf **Anlagenverwaltungsparameter** > **Einstellungen** > **Arbeitsaufträge** > **Ursachencodes für Wartungsausfallzeit**.

2. Klicken Sie auf **Neu**.

3. Geben Sie eine Kennung im Feld **Ursachencodes für Wartungsausfallzeit** ein.

4. Geben Sie im Feld **Name** einen Namen für den Ursachencode ein.

5. Aktivieren Sie das Kontrollkästchen **KPI enthalten**, wenn der Ursachencode in den Berechnungen der Anlage-KPI-Berechnung enthalten sein soll. Im Allgemeinen sollten geplante Produktionsstopps nicht in die KPI-Berechnungen einbezogen werden, da sie die erwartete Leistung nicht beeinflussen.

6. Klicken Sie auf **Speichern**.

![Abbildung 1](media/15-work-orders.png)


Wenn Sie die von Ihnen gewünschten Ursachencodes für Wartungsausfallzeit angelegt haben, können Sie Wartungsausfallzeiterfassungen für Arbeitsaufträge und Anlagen anlegen.


## <a name="create-maintenance-downtime-registrations"></a>Erstellen von Wartungsausfallzeiterfassungen

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Wartungsausfallzeit**.

3. Klicken Sie auf **Neu**.

4. Fügen Sie das Datums- und Uhrzeitintervall für die Wartungsausfallzeitregistrierung in den Feldern **Von** und **Bis** ein.

5. Wenn Sie das Feld **Bis** leer lassen, ist die Dauer in Stunden automatisch im Feld **Dauer** eingefügt.

6. Wählen Sie im Feld **Ursachencodes für Wartungsausfallzeit** einen Ursachencode ein.

7. Wiederholen Sie die Schritte 3-6, wenn mehrere Erfassungen hinzufügen möchten.

8. Klicken Sie auf **Speichern**.


![Abbildung 2](media/16-work-orders.png)


Der Kalender, der für die Berechnung einer Wartungsausfallzeiterfassung verwendet wird, hängt von Ihrer Auswahl bei der Einrichtung von Anlagen und Parametern ab. Wenn eine Ressource auf einer Anlage im Feld **Alle Anlagen** > **Anlage** Inforegister > **Ressource** ausgewählt wird, wird der für die zugehörige Ressourcengruppe eingerichtete Kalender verwendet, wie in der folgenden Abbildung dargestellt.

![Abbildung 3](media/17-work-orders.png)


Wenn keine Ressource auf der Anlage ausgewählt ist, wird der in den **Anlagenverwaltungsparameter** ausgewählte Standardkalender verwendet, wie in der folgenden Abbildung dargestellt.

![Abbildung 4](media/18-work-orders.png)


Klicken Sie **Unternehmensanlagenverwaltung** > **Abfragen** > **Wartungsausfallzeit**, um eine Übersicht über alle Wartungsausfallzeiterfassungen anzuzeigen.

>[!NOTE]
>Alle Kalender, die im Modul **Anlagenverwaltung** verwendet werden, werden in **Organisationsverwaltung** > **Einstellungen** > **Kalender** > **Kalender** eingerichtet.

