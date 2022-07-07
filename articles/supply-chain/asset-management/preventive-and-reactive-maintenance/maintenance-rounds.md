---
title: Wartungsdurchgänge
description: In diesem Artikel werden Wartungsdurchgänge im Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 519431d84652e45dcd45aefbbaaa2a0e2afe6349
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016506"
---
# <a name="maintenance-rounds"></a>Wartungsdurchgänge

[!include [banner](../../includes/banner.md)]

 

In **Asset Management** können Sie für verschiedene Anlagen Wartungsdurchgänge anlegen, bei denen Sie eine ähnliche Aufgabe in regelmäßigen Abständen durchführen müssen. Zum Beispiel Schmierarbeiten oder Sicherheitsprüfungen, die an mehreren Maschinen innerhalb derselben Zeiträume durchgeführt werden müssen. Der erste Schritt ist die Erstellung eines Wartungsdurchgangs, der Anlagen einbezieht, die die gleiche Form von Wartungsarbeiten erfordern. Als nächstes planen Sie die Wartungsdurchgänge ein. Wenn Sie den Wartungsdurchgangsplan erstellt haben, sehen Sie alle Auftragsdatensätze, die sich auf die Runde beziehen, in **Alle Wartungszeitpläne**- und **Offene Wartungszeitpläne-Positionen**.

>[!NOTE]
>Wartungsdurchgänge können auch auf funktionaler Standorten eingerichtet werden, die zum Zeitpunkt der Erstellung des durchgangsbasierten Arbeitsauftrags auf den funktionalem Standort installierten Anlagen abgeschlossen werden sollen. Weitere Informationen zum Einrichten von Wartungsdurchgängen auf funktionalen Standorten finden Sie unter [Erstellen von funktionalen Standorten](../functional-locations/create-functional-locations.md).

## <a name="set-up-a-maintenance-round"></a>Einrichten eines Wartungsdurchgangs

1. Klicken Sie auf **Anlagenverwaltung** > **Einstellungen** > **Vorbeugende Wartung** > **Wartungsdurchgänge**.

2. Klicken Sie auf **Neu**, um einen neuen Wartungsdurchgang zu erstellen.

3. Fügen Sie im Feld **Wartungsdurchgang** eine Kennung ein und im Feld **Name** einen Namen für den Wartungsdurchgang.

4. Wählen Sie im Feld **Startdatum** ein Startdatum für den Durchgang aus.

5. n den Feldern **Innerhalb von Tagen beenden** und **Innerhalb von Stunden beenden** können Sie das erwartete Enddatum in Tagen oder Stunden eingeben. Das erwartete Enddatum wird relativ zum erwarteten Startdatum berechnet, das beim Anlegen von Wartungszeitplanpositionen berechnet wird. Sie können beispielsweise „7“ in das Feld **Innerhalb von Tagen beenden** einfügen, um anzugeben, dass der betreffende Auftrag innerhalb einer Woche nach dem Startdatum abgeschlossen sein soll.

6. Wählen Sie „Ja“ auf der Umschaltfläche **Automatisch einrichten**, wenn Arbeitsaufträge automatisch aus Wartungszeitplanpositionen erstellt werden sollen, die aus diesem Wartungsdurchgang angelegt werden.

7. Wählen Sie im Feld **Arbeitsauftragstyp** den Arbeitsauftragstyp aus, der für Arbeitsaufträge verwendet werden soll, die aus diesem Wartungsdurchgang angelegt wurden.

8. Wählen Sie im Feld **Servicelevel** den Servicelevel des Arbeitsauftrags aus, der für Arbeitsaufträge verwendet werden soll, die aus diesem Wartungsdurchgang angelegt wurden.

9. Klicken Sie auf dem Inforegister **Anlagenpositionen** auf **Hinzufügen**, um eine Anlage zum Wartungsdurchgang hinzuzufügen.

10. Im Feld **Positionsnummer** wird automatisch eine Positionsnummer eingefügt, um die Reihenfolge der Anlagen im Wartungsdurchgang anzuzeigen.

11. Wählen Sie im Feld **Anlage** die Anlage aus.

12. Wählen Sie im Feld **Wartungsauftragstyp** den Wartungsauftragstyp für die Anlage aus.

13. Bei Bedarf wählen Sie **Wartungsauftragstypvariante** und **Branche** bezogen auf die Wartungsauftragsart.

14. Wählen Sie im Feld **Periodentyp** die Wiederholung (Tag, Woche, etc.) aus.

15. Geben Sie im Feld **Periodenhäufigkeit** die Anzahl der Wiederholungen für den Wartungsdurchgang ein. Beispiel: Wenn Sie im Feld **Periodentyp** „Tag“ gewählt haben und in diesem Feld die Zahl „7“ eingeben, werden bei der Planung der vorbeugenden Wartung einmal pro Woche neue Wartungsdurchgangspositionen angelegt.

16. Wählen Sie im Feld **Startdatum** ein Startdatum für die Anlage, die in den Wartungsdurchgang aufgenommen werden soll. Dieses Datum kann von dem im Wartungsdurchgang festgelegten Startdatum abweichen.

17. Wiederholen Sie die Schritte 9-16, um dem Wartungsdurchgang weitere Anlagen hinzuzufügen.

18. Klicken Sie auf dem Inforegister **Funktionaler Standort-Positionen** auf **Hinzufügen**, um einen funktionalen Standort zum Wartungsdurchgang hinzuzufügen. Siehe Beschreibung der zugehörigen Felder oben. Es stehen Ihnen die gleichen Felder zur Verfügung wie beim Erstellen einer Anlagenposition, aber Sie können bei Bedarf auch **Hersteller** und **Modell** für einen funktionalen Standort auswählen. Wenn Sie nur einen funktionalen Standort in einer Zeile auswählen, aber keine Auswahl in **Anlagentyp**, **Hersteller**, **Modell**, **Wartungsauftragstyp**, **Wartungsauftragstypvariante** und **Branche** treffen, werden alle Anlagen, die zum Zeitpunkt der Wartungsplanung mit diesem funktionalen Standort zusammenhängen, in den Wartungsdurchgang aufgenommen.

19. Klicken Sie im Inforegister **Pools** auf **Hinzufügen**, um einen Arbeitsauftragspool auszuwählen, der in den Wartungsdurchgang aufgenommen werden soll. Einige Arbeitsauftragspools können mit einem Wartungsdurchgang verbunden werden.

20. Speichern Sie Ihre Einstellungen.

>[!NOTE]
>Die Felder **Anlagen** und **Positionen** in der Gruppe **Details** auf dem Inforegister **Kopfzeile** zeigen die Gesamtzahl der Anlagen und Positionen, die sich auf den ausgewählten Wartungsdurchgang beziehen.

Die folgende Abbildung zeigt das Beispiel einer Wartungsdurchführung mit drei Anlagen.

![Abbildung 1.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Wartungsdurchgänge terminieren

Wenn Sie einen Wartungsdurchgang eingerichtet haben, führen Sie einen Zeitplanauftrag aus, um alle mit dem Wartungsdurchgang verbundenen Aufträge einzuplanen.

1. Klicken Sie auf die Schaltfläche **Anlagenverwaltung** > **Periodisch** > **Vorbeugende Wartung** > **Wartungsdurchgänge planen** oder **Anlagenverwaltung** > **Wartungszeitplan** > **Gesamter Wartungszeitplan** oder **Wartungszeitplanpositionen öffnen** oder **Wartungszeitplanpools öffnen** > Wartungszeitplanposition in der Liste auswählen > **Wartungsdurchgänge**.

2. Wählen Sie im Feld **Periode** den Periodentyp, der für den Terminierungsauftrag verwendet werden soll.

3. Geben Sie im Feld **Periodenhäufigkeit** die Anzahl der Perioden ein, die in den Terminierungsauftrag aufgenommen werden sollen. Der Beginn der Terminierung ist das aktuelle Datum.

4. Wählen Sie „Ja“ auf der Umschaltfläche **Automatisch einrichten**, wenn ein Arbeitsauftrag auf der Grundlage eines Wartungsdurchgangs automatisch erstellt werden soll.

>[!NOTE]
>Wenn diese Umschaltfläche auf „Ja“ gesetzt ist und die Umschaltfläche **Automatisch einrichten** auch im Wartungsdurchgang im Formular **Wartungsdurchgänge** auf „Ja“ gesetzt ist, werden Arbeitsaufträge auf der Grundlage der Wartungsdurchgangspositionen angelegt und Wartungszeitplanpositionen mit dem Status „Arbeitsauftrag angelegt“ ebenfalls erstellt. Wenn nur eine der Umschaltflächen **Automatisch einrichten** auf „Ja“ gesetzt ist, in diesem Dropdownmenü oder in **Wartungsdurchgängen**, werden nur Wartungszeitplanpositionen mit dem Status „Erstellt“ angelegt. In diesem Fall werden keine Arbeitsaufträge erstellt.

5. Bei Bedarf können Sie bestimmte Durchgänge oder ein anderes Startdatum für den Zeitplanauftrag auswählen. Klicken Sie **Filtern** und fügen Sie die einzubeziehenden Durchgänge hinzu.

6. Klicken Sie auf **OK**.

7. Sie können nun die Wartungsdurchgangsaufträge in **Anlagenverwaltung** > **Wartungszeitplan** > **Alle Wartungszeitpläne** oder **Wartungszeitplanpositionen öffnen** sehen. Wenn die terminierten Durchgänge an einen Arbeitsauftragspool angeschlossen sind, sehen Sie auch Wartungszeitplanpositionen in **Wartungszeitplanpools öffnen**. Wartungszeitplanpositionen, die aus einem Durchgang angelegt wurden, haben den Referenztyp „Wartungsdurchgänge“.

Die zwei folgenden Abbildungen zeigen einen Zeitplaneinzelvorgang im Dialog **Wartungszeitplan anzeigen** und die Wartungsplanpositionen, die in **Alle Wartungszeitpläne** erstellt werden, die auf diesem Zeitplaneinzelvorgang basieren.

![Abbildung 2.](media/14-preventive-maintenance.png)

![Abbildung 3.](media/15-preventive-maintenance.png)

- Wenn Arbeitsaufträge für Anlagen, die unter eine Lieferantengarantie fallen, manuell erstellt werden, erscheint ein Dialogfenster, um den Benutzer auf die Garantie aufmerksam zu machen Die Erstellung des Arbeitsauftrags kann dann abgebrochen werden. Bei Arbeitsaufträgen, die automatisch angelegt werden, entfällt die Prüfung auf eine Garantiebeziehung.  
- Sie können einen Batchauftrag auf dem Inforegister **Im Hintergrund ausführen** einrichten, um Durchgänge in regelmäßigen Abständen einzuplanen.  
- Wenn ein Durchgang in mehreren Arbeitsauftragspools enthalten ist (siehe [Arbeitsauftragspools](../work-orders/work-order-pools.md)), wird für jeden Pool ein Datensatz in **Wartungszeitplanpools öffnen** angezeigt. Dies erfolgt, um die Filtermöglichkeiten für Arbeitsauftragspools zu optimieren.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]