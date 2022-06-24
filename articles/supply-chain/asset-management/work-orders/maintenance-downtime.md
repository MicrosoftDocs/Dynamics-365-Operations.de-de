---
title: Wartungsausfallzeit für Arbeitsaufträge
description: Dieser Artikel beschreibt, wie Sie Wartungsausfallzeiterfassungen für die auf einem Arbeitsauftrag ausgewählte Anlage anlegen können.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a76c0ecefbb8da762ac68cbdd7bb44f68a89894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851855"
---
# <a name="maintenance-downtime-for-work-orders"></a>Wartungsausfallzeit für Arbeitsaufträge

[!include [banner](../../includes/banner.md)]


Sie können Wartungsausfallzeiterfassungen für die auf einem Arbeitsauftrag ausgewählte Anlage anlegen. Dies ist hilfreich, wenn Sie Wartungsausfallzeit auf einem oder mehreren Computern im Produktionsbereich erfassen möchten. Zunächst erstellen Sie die Ursachencodes für Wartungsausfallzeit, die Sie verwenden möchten, z. B. **Ausfall** und **Geplanter Stopp**. Dies geschieht auf der Seite **Ursachencodes für Wartungsausfallzeit**. Als Nächstes können Sie auf der Seite **Wartungsausfallzeit** Wartungsausfallzeiterfassungen anlegen und die entsprechenden Ursachencodes für Wartungsausfallzeit hinzufügen.

## <a name="create-maintenance-downtime-reason-codes"></a>Erstellen von Ursachencodes für Wartungsausfallzeit

1. Wählen Sie **Anlagenmanagement** > **Einstellungen** > **Arbeitsaufträge** > **Ursachencodes für Wartungsausfallzeit** aus.

2. Wählen Sie **Neu** aus.

3. Geben Sie im Feld **Ursachencode für Wartungsausfallzeit** eine Kennung für den Ursachencode für Wartungsausfallzeit ein.

4. Geben Sie im Feld **Name** einen Namen ein.

5. Aktivieren Sie das Kontrollkästchen **KPI enthalten**, wenn der Ursachencode in Berechnungen von Leistungskennzahlen (KPIs) für die Anlage enthalten sein soll. Im Allgemeinen sollten geplante Produktionsstopps nicht in die KPI-Berechnungen einbezogen werden, da sie die erwartete Leistung nicht beeinflussen.

6. Wählen Sie **Speichern**.

Die folgende Abbildung zeigt ein Beispiel der Seite **Ursachencodes für Wartungsausfallzeit**.

![Abbildung 1.](media/15-work-orders.png)

Wenn Sie die von Ihnen gewünschten Ursachencodes für Wartungsausfallzeit angelegt haben, können Sie Wartungsausfallzeiterfassungen für Arbeitsaufträge und Anlagen anlegen.


## <a name="create-maintenance-downtime-registrations"></a>Erstellen von Wartungsausfallzeiterfassungen

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag aus, und wählen Sie dann auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Anlage** **Wartungsausfallzeit** aus.

3. Wählen Sie **Neu** aus.

4. Definieren Sie das Datums- und Uhrzeitintervall für die Wartungsausfallzeitregistrierung in den Feldern **Von** und **Bis**.

>[!NOTE]
>Wenn Sie das Feld **Bis** leer lassen, ist die Dauer in Stunden automatisch im Feld **Dauer** eingefügt.

5. Wählen Sie im Feld **Ursachencodes für Wartungsausfallzeit** einen Ursachencode aus.

6. Wiederholen Sie die Schritte 3 bis 5, um weitere Erfassungen hinzuzufügen.

7. Wählen Sie **Speichern**.

Die folgende Abbildung zeigt das Beispiel einer Registrierung für Wartungsausfallzeit.

![Abbildung 2.](media/16-work-orders.png)

Der Kalender, der für die Berechnung einer Wartungsausfallzeiterfassung verwendet wird, hängt von Ihrer Auswahl bei der Einrichtung von Anlagen und Parametern ab. Wenn eine Ressource auf einer Anlage im Feld **Ressource** im Inforegister **Anlage** auf der Seite **Alle Anlagen** ausgewählt wird, wird der für die zugehörige Ressourcengruppe eingerichtete Kalender verwendet, wie in der folgenden Abbildung dargestellt.

![Abbildung 3.](media/17-work-orders.png)

Wenn keine Ressource auf der Anlage ausgewählt ist, wird der auf der Seite **Anlagenverwaltungsparameter** ausgewählte Standardkalender verwendet, wie in der folgenden Abbildung dargestellt.

![Abbildung 4.](media/18-work-orders.png)

Klicken Sie **Anlagenverwaltung** > **Abfragen** > **Wartungsausfallzeit**, um eine Übersicht über alle Wartungsausfallzeiterfassungen anzuzeigen.

>[!NOTE]
>Alle Kalender, die im Modul **Anlagenverwaltung** verwendet werden, werden in **Organisationsverwaltung** > **Einstellungen** > **Kalender** > **Kalender** eingerichtet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]