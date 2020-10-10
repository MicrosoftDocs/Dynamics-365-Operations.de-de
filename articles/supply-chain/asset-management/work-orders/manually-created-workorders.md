---
title: Manuell erstellte Arbeitsaufträge
description: In diesem Thema wird erläutert, wie Sie im Anlagenmanagement Arbeitsaufträge manuell anlegen.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888976"
---
# <a name="manually-created-work-orders"></a>Manuell erstellte Arbeitsaufträge

[!include [banner](../../includes/banner.md)]


Sie können Arbeitsaufträge auf zwei Arten manuell anlegen:

- Auf der Seite **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** 
- Auf der Seite **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte** 

## <a name="create-work-order"></a>Arbeitsauftrag erstellen

1. Wählen Sie **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.

2. Wählen Sie **Neu** aus.

3. Im Dialogfeld **Arbeitsauftrag erstellen** wählen Sie einen Arbeitsauftragstyp im Feld **Arbeitsauftragstyp** aus.

4. Wählen Sie bei Bedarf eine **Beschreibung** aus.

5. Wählen Sie im Feld **Anlage** die Anlage aus.

>[!NOTE]
>Wenn Sie eine Anlage auswählen, sind möglicherweise drei Registerkarten im Dropdown **Anlage** verfügbar: 

- **Aktive Anlagen** – Diese Registerkarte enthält eine Liste aller Anlagen mit dem Anlagenlebenszyklusstatus „Aktiv“. 
- **Anlagenansicht** – Die Registerkarte enthält eine Strukturansicht der funktionalen Standorte und der Anlagen, die für diese Standorte installiert sind.
- **Meine Anlagen** – Diese Registerkarte enthält Anlagen, die den funktionalen Standorten zugeordnet werden, denen Sie (die am System angemeldete Arbeitskraft) möglicherweise zugewiesen werden. (Informationen zum Einrichten siehe [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).) Wenn keine funktionalen Standorte für eine Arbeitskraft unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md) eingerichtet werden, ist die Registerkarte **Meine Anlagen** nicht verfügbar. 

6. Wählen Sie im Feld **Wartungsauftragstyp** den Wartungsauftragstyp für den Wartungsauftrag aus.

7. Wählen Sie bei Bedarf **Wartungsauftragsartenvariante** und **Wechseln**.

8. Bei Bedarf können Sie den Servicegrad des Arbeitsauftrags im Feld **Service Level** ändern.

9. Wählen Sie in den entsprechenden Feldern das **erwartete Startdatum**-und das **erwartete Enddatum** aus.

10. Klicken Sie auf **OK**, um den Arbeitsauftrag zu erstellen.

11. Auf der Listenseite **Alle Arbeitsaufträge** können Sie den Arbeitsauftrag nach Bedarf bearbeiten.

Beachten Sie die folgenden Punkte:

- In der Detailansicht auf der Listenseite **Alle Arbeitsaufträge** können Sie mehrere Anlagen zu einem Arbeitsauftrag hinzufügen, indem Sie Positionen zu den Wartungsaufträgen im Inforegister **Wartungsaufträge für Arbeitsaufträge** hinzufügen. In einer Anlage können Sie nur die Wartungsauftragstypen auswählen, die für die für die Anlage ausgewählten Anlagenart definiert sind.  

- Wenn Sie einen Anlagenservicelevel oder eine Anlagenkritikalität ändern, nachdem Sie die Anlage für einen Arbeitsauftrag verwendet haben, wird der Servicelevel oder die Kritikalität für den Arbeitsauftrag nicht entsprechend aktualisiert. Weitere Informationen zu Service Levels und Kritikalitäten finden Sie unter [Asset Service Levels](../setup-for-objects/object-priorities.md) und [Asset Kritikalitätsarten](../setup-for-objects/object-criticalities.md).

- Die Kritikalität eines Arbeitsauftrags wird jedes Mal neu berechnet, wenn eine Arbeitsauftragseinzelvorgang zum Arbeitsauftrag hinzugefügt oder daraus gelöscht wird.

- In der Detailansicht **Alle Arbeitsaufträge** > Ansicht **Leiter** > Inforegister **Terminplan** können Sie in den Feldern **Verantwortliche Gruppe** oder **Verantwortlich** eine verantwortliche Wartungsgruppe oder einen verantwortlichen Wartungsarbeiter auswählen. Diese Einstellungen können geändert werden, während der Arbeitsauftrag aktiv ist. Sie können geändert werden, wenn sich der Arbeitsauftragslebenszyklusstatus ändert. Die automatische Auswahl bei der Erstellung von Arbeitsaufträgen basiert auf dem Setup auf der Seite **Zuständige Wartungsarbeitskräfte**. Wenn Sie Arbeitsaufträge hinzufügen oder entfernen, nachdem Sie einen Arbeitsauftrag angelegt haben, und das Feld **Verantwortliche Gruppe** und das Feld **Verantwortlich** bei der Aktualisierung des Arbeitsauftrags leer sind, sucht die Anlagenverwaltung nach einer möglichen Übereinstimmung für eine verantwortliche Wartungsmitarbeitergruppe oder einen verantwortlichen Wartungsmitarbeiter auf der Einrichtungsseite. Wenn das Feld **Verantwortliche Gruppe** oder das Feld **Verantwortlich** bei der Aktualisierung des Arbeitsauftrags bereits ausgefüllt ist, werden keine Änderungen vorgenommen. Weitere Informationen über verantwortliche Wartungsarbeiter und Wartungsarbeitergruppen finden Sie unter [Zuständige Wartungsarbeitskräfte](../setup-for-maintenance-requests/responsible-workers.md).

- Auf der Seite [Wartungsstatus](../controlling-and-reporting/maintenance-status.md) können Sie eine Kalkulation durchführen, um sich einen Überblick über die Auslastung der eingehenden und abgeschlossenen Arbeitsaufträge zu verschaffen.  

- In der Detailansicht der Seite **Alle Arbeitsaufträge** auf dem Inforegister **Positionsdetails**, können Sie die Felder **Breite** und **Länge** verwenden, um geografische Koordinaten für die Anlage hinzuzufügen, die für den Arbeitsauftragseinzelvorgang aktiviert ist.  


## <a name="create-related-work-order"></a>Zugehörigen Arbeitsauftrag erstellen

Sie können einen Arbeitsauftrag erstellen, der zu einem vorhandenen Arbeitsauftrag gehört. Diese Funktion ist z. B. hilfreich, wenn Sie mit primären und sekundären Arbeitsaufträgen arbeiten möchten. Ein neuer Arbeitsauftrag basiert auf einem Arbeitsauftrag aus einem bestehenden Arbeitsauftrag.

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.

2. Wählen Sie den zu erstellenden Arbeitsauftrag aus, für den ein zugehöriger Arbeitsauftrag erstellt werden soll.

3. Wählen Sie im Aktivitätsbereich, auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Neu** die Option **Zugehöriger Arbeitsauftrag**.

4. Wählen Sie im Dialogfeld **Zugehörigen Arbeitsauftrag erstellen** im Feld **Arbeitsauftragseinzelvorgang** den Arbeitsauftragseinzelvorgang aus, für den Sie einen zugehörigen Arbeitsauftrag erstellen möchten.

5. Wählen Sie im Feld **Wartungsauftragstyp** den Wartungsauftragstyp aus.

6. Wählen Sie in den Feldern **Wartungsauftragstypvariante** und **Art** nach Bedarf die Variante und Art aus, die sich auf den Wartungsauftragstyp beziehen.

7. Wenn dieser Arbeitsauftrag der erste zugehörige Arbeitsauftrag ist, der für den ausgewählten Arbeitsauftrag erstellt wurde, gehen Sie gemäß den folgenden Schritten vor:
    1. Wählen Sie die Option **Neuer Arbeitsauftrag** aus.
    2. Wählen Sie im Feld **Arbeitsauftragstyp** einen Arbeitsauftragstyp aus.
    3. Geben Sie im Feld **Beschreibung** eine Beschreibung ein.
    4. Ändern Sie bei Bedarf die Leistungsebene des Arbeitsauftrags im Feld **Leistungsebene**.
    5. Wählen Sie in den Feldern **Erwartetes Anfangsdatum** und **Erwartetes Enddatum** das erwartete Start- und Enddatum aus.
    6. Wählen Sie **OK**. Der neue zugehörige Arbeitsauftrag wird in der Listenseite **Alle Arbeitsaufträge** angezeigt.  

8. Wenn der Arbeitsauftrag, für den Sie diesen zugehörigen Arbeitsauftrag erstellen, bereits zugehörige Arbeitsaufträge hat, führen Sie die folgenden Schritte aus, um einen Arbeitsauftragseinzelvorgang einem vorhandenen zugehörigen Arbeitsauftrag hinzuzufügen:
    1. Wählen Sie die Option **Zu zugehörigem Arbeitsauftrag hinzufügen** aus.
    2. Wähle Sie im Feld **Arbeitsauftrag** den zugehörigen Arbeitsauftrag aus, dem Sie einen neuen Arbeitsauftragseinzelvorgang hinzufügen möchten.
    3. Ändern Sie bei Bedarf die Leistungsebene des Arbeitsauftrags im Feld **Leistungsebene**.
    4. Ändern Sie in den Feldern **Erwartetes Anfangsdatum** und **Erwartetes Enddatum** das erwartete Start- und Enddatum nach Bedarf.
    5. Wählen Sie **OK**. Der Arbeitsauftrag wird zu dem bestehenden zugehörigen Arbeitsauftrag hinzugefügt.

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Zugehörigen Arbeitsauftrag erstellen**.

![Abbildung 1](media/03-work-orders.png)

>[!NOTE]
>Wenn Sie eine zugehörige Arbeitsauftragsmaske unter **Anlagenverwaltungsparameter** > **Arbeitsaufträge** > **Verwandte Arbeitsauftragsmaske** eingerichtet haben, werden Arbeitsauftrags-IDs entsprechend dem Maskenaufbau erstellt. Wenn keine zugehörige Arbeitsauftragsmaske eingerichtet ist, wird die nächste verfügbare Arbeitsauftrags-ID für zugehörige Arbeitsaufträge verwendet.

## <a name="copy-a-work-order"></a>Arbeitsauftrag kopieren

Es ist möglich, schnell einen neuen Arbeitsauftrag aus einem bestehenden Arbeitsauftrag zu erstellen. Diese Art der Arbeit mit Arbeitsaufträgen unterscheidet sich von der Erstellung von Arbeitsaufträgen auf der Grundlage von [Wartungsplänen](../preventive-and-reactive-maintenance/maintenance-plans.md). Dies ist z.B. sinnvoll, wenn Sie ein Arbeitsauftrag viele Arbeitsaufträge enthält, und verschiedene Einzelvorgänge auf verschiedenen Anlagen in regelmäßigen Abständen erledigt werden sollen.

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.

2. Wählen Sie den Arbeitsauftrag aus, aus dem Sie Inhalte kopieren möchten.

3. Wählen Sie im Aktivitätsbereich > Registerkarte **Arbeitsauftrag** > Gruppe **Neu** die Option **Arbeitsauftrag kopieren**.

4. Die Einrichtung des Arbeitsauftrags aus dem ausgewählten Arbeitsauftrag wird angezeigt. Bei Bedarf können Sie einige der Felder bearbeiten.

5. Wählen Sie **OK** aus, um den neuen Arbeitsauftrag zu erstellen.

6. Auf der Listenseite **Alle Arbeitsaufträge** können Sie den Arbeitsauftrag nach Bedarf bearbeiten.

>[!NOTE]
>Wenn der neue Arbeitsauftrag erstellt wird, werden einige Informationen direkt aus dem bestehenden Arbeitsauftrag kopiert. Informationen über Planungen, Werkzeuge, Wartungsprüflisten, funktionale Standorte, Adressen und Zeitplanung werden nicht kopiert. Stattdessen werden sie über die aktuelle Einstellung in der Anlagenverwaltung initialisiert. Wenn diese Informationen zwischen dem Zeitpunkt geändert wurden, als erste Arbeitsauftrag erstellt wurde, und dem Zeitpunkt, zu dem Sie eine Kopie des Arbeitsauftrag erstellten, werden die Änderungen in den neuen Arbeitsauftrag einbezogen. Beispiele umfassen Änderungen an den Prognosen und Aktualisierungen von Wartungsprüflisten.

In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Arbeitsauftrag kopieren** angezeigt.

![Abbildung 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a>Arbeitsauftrag basierend auf einer Wartungsanforderung anlegen

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Wartungsanfragen** > **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** aus.

2. Wählen Sie die Wartungsanfrage aus, für die Sie einen Arbeitsauftrag anlegen möchten, und klicken Sie auf **Bearbeiten**.

3. Wählen Sie im Aktivitätsbereich > Registerkarte **Wartungsanfrage** > Gruppe **Neu** die Option **Arbeitsauftrag**.

4. Im Dialogfeld **Arbeitsauftrag** können Sie die Felder festlegen. Wenn in der Wartungsanfrage ein Wartungsauftrag ausgewählt wurde, können Sie beim Anlegen des Arbeitsauftrags bei Bedarf einen anderen Wartungsauftragstyp auswählen.

5. Wählen Sie **OK**. Die Nachricht informiert Sie darüber, dass ein Arbeitsauftrag erstellt wurde.

6. Wenn Sie sehen möchten, welche Arbeitsaufträge mit einer Wartungsanfrage verbunden sind, markieren Sie die Wartungsanfrage auf der Listenseite **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen**. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Wartungsanfrage** in der Gruppe **Ansicht** die Option **Arbeitsaufträge**.


In der folgenden Abbildung wird ein Beispiel des Dialogfelds **Arbeitsauftrag erstellen** angezeigt.

![Abbildung 3](media/05-work-orders.png)


>[!NOTE]
>Wenn Arbeitsaufträge automatisch erstellt werden sollen, können Sie Wartungsplanjobs planen oder festlegen, dass [Wartungspläne](../preventive-and-reactive-maintenance/maintenance-plans.md) oder [Wartungsrunden](../preventive-and-reactive-maintenance/maintenance-rounds.md) auf einer Anlage automatisch erstellt werden. Arbeitsaufträge, die aus Wartungsanfragen auf der Listenseite **Alle Wartungszeitpläne** erstellt wurden, weisen die in den Wartungsanfragen ausgewählten Wartungsauftragsarten auf.

