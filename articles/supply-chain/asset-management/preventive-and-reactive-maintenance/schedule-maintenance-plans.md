---
title: Wartungspläne terminieren
description: In diesem Abschnitt werden die Wartungspläne im Anlagenmanagement erläutert.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c84711412d799f9d3cce02e0740ec065ef42d8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223553"
---
# <a name="schedule-maintenance-plans"></a>Wartungspläne terminieren

[!include [banner](../../includes/banner.md)]

 

Die vorbeugende Wartungsplanung erzeugt Kalendereinträge auf Anlagen, basierend auf den auf den Anlagen eingerichteten Wartungsplänen. Sie können Kalendereinträge basierend auf ausgewählten Wartungsplänen, Anlagentypen und Anlagen planen.

1. Klicken Sie auf **Anlagenmanagement** > **Periodisch** > **Präventive Wartung** > **Terminierte Wartungspläne**.

2. Sie können ein Zeitintervall in den Feldern **Periode** und **Periodenfrequenz** auswählen.

>[!NOTE]
>Die Felder **Periode** und **Periodenfrequenz** zeigen an, wie weit im Voraus Wartungseinteilungen auf der Grundlage der von Ihnen erstellten Wartungspläne (zeit- oder zählerbezogen) angelegt werden sollen. In der folgenden Abbildung werden Wartungseinteilungen (= Arbeitsauftragsvorschläge) ab dem Tagesdatum und drei Monaten erstellt.

3. Wählen Sie „Ja“ auf der Seite **Auto anlegen, wenn in der Zeile** Umschalttaste angegeben, wenn Arbeitsaufträge automatisch gemäß der Wartungsplanzeile erstellt werden sollen.

>[!NOTE]
>Wenn diese Umschalttaste auf „Ja“ gesetzt ist, ist das Kontrollkästchen *und* **Automatisch anlegen** auch in Wartungsplanzeilen in **Wartungspläne** aktiviert, Arbeitsaufträge werden auf der Grundlage der Wartungsplaneinteilungen angelegt und Wartungseinteilungen mit dem Status „Arbeitsauftrag angelegt“ werden ebenfalls angelegt. Wenn nur eine Option ausgewählt ist (**Auto anlegen, wenn in diesem Dialog in der Zeile** Umschaltfläche angegeben oder **Automatisch anlegen** im Formular **Wartungspläne**), werden nur Wartungseinteilungen mit dem Status „angelegt“ angelegt. In diesem Fall werden keine Arbeitsaufträge erstellt.

4. Es ist möglich, Kalendereinträge auf der Grundlage von Wartungsplänen (Uhrzeit oder Zähler), Anlagen, Anlagentypen, Anlagentypen, Technischen Standorte und Technischen Standortarten zu erzeugen. Klicken Sie auf die Schaltfläche **Filter** und treffen Sie bei Bedarf Ihre Auswahl.

- Bezüglich der Terminierung von Wartungsplänen auf Technischen Standorten: Wenn Sie die Einrichtung von Anlagenarten, Herstellern und Modellen zu Wartungsplänen in **Alle Technischen Standorte** > **Wartungspläne** FastTab aktualisieren, nachdem Sie Wartungspläne terminiert haben, werden bestehende Wartungsplaneinträge zu diesem Technischen Standort automatisch gelöscht. Um neue Kalendereinträge anzulegen, die dem aktualisierten Wartungsplan auf dem Technischen Standort entsprechen, müssen Sie einen neuen Wartungsplanplan für diesen Technischen Standort erstellen. Weitere Informationen zur Einrichtung von Anlagentypen, Herstellern und Modellen auf Technischen Standorte finden Sie unter [Technische Standorte anlegen](../functional-locations/create-functional-locations.md).

>*Beispiel:* Sie möchten einen Wartungsplan für einen bestimmten Technischen Standort anlegen, d.h. alle Anlagen, die auf diesem Technischen Standort zu einem bestimmten Zeitpunkt angelegt wurden, werden bei der Terminierung des Wartungsplans berücksichtigt. In diesem Fall legen Sie einen Wartungsplan an und wählen den jeweiligen Technischen Standort aus, fügen aber keine Anlagen in den Wartungsplan ein. Das Ergebnis ist, dass bei der Terminierung dieses Wartungsplans Wartungseinteilungen für alle Anlagen angelegt werden, die zu diesem Zeitpunkt mit dem Technischen Standort zusammenhängen.

- Wenn Sie Änderungen an Anlagentypen, Herstellern und Modellen in **Anlagentypen** vornehmen, betreffen diese Änderungen nur neue Anlagen, die die aktualisierte Anlagenart verwenden. Lesen Sie mehr über die Einrichtung von Anlagen-Typen unter [Anlagen-Typen](../setup-for-objects/object-types.md).  

5. Klicken Sie auf **OK**, um die Generierung von Wartungsplaneinträgen für Anlagen zu starten. Die erzeugten Einträge werden auf der Listenseite **Alle Wartungspläne** angezeigt. Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Wartungspläne terminieren**.

![Abbildung 1](media/09-preventive-maintenance.png)

- Im Dialog **Wartungspläne terminieren** können Sie Batch-Jobs auf der Seite **Ausführen im Hintergrund** FastTab einrichten, um in regelmäßigen Abständen automatisch Kalendereinträge zu erzeugen.  
- Wenn Sie vorbeugende Wartung planen, werden keine Wartungseinteilungen mit einem erwarteten Startdatum und einer erwarteten Uhrzeit vor dem Systemdatum und der Systemzeit angelegt.  

Die folgende Abbildung veranschaulicht eine zeitabhängige Wartungsplankalkulation.  

![Abbildung 2](media/10-preventive-maintenance.jpg)

Bezüglich zählerabhängiger Wartungspläne: In den folgenden Abbildungen sind zwei verschiedene Zählerregistrierungszyklen dargestellt. Sie basieren auf einem Wartungsplan für die Anlage „V0001“, der eine monatliche Laufleistung der Anlage (eines Fahrzeugs) von ca. 2.000 km erwartet.

Im ersten Beispiel werden die erwarteten 2.000 km nicht jeden Monat erreicht. Gemäß dem zählergesteuerten Wartungsplan beträgt der Schwellenwert 2.000 km, d.h. wenn Sie eine Wartungsplanterminierung durchführen, sollte bei jedem Erreichen des Schwellenwerts von 2.000 Kilometern eine Wartungseinteilung angelegt werden. In Beispiel 1 gibt es 4 Registrierungszeilen, aber die 2.000 Kilometer lange Schwelle wird nur einmal erreicht. Dies bedeutet, dass bei der Ausführung von Wartungsplänen für diese Anlage, z.B. für einen Zeitraum von 3 Monaten, nur eine Wartungseinteilung angelegt wird.

In der nächsten Abbildung werden jeden Monat 2.000 km oder mehr registriert. Daher würden drei Wartungszeilen entstehen, wenn Sie Wartungspläne für diese Anlage für einen Zeitraum von 3 Monaten terminieren. 

Die hier beschriebenen Beispiele zeigen, dass alle Zählerregistrierungen an einer Anlage einen Trend aufweisen, der die Abnutzung des Anlagenwertes beschreibt. Dieser Trend wird zum Zeitpunkt der Wartungsplanterminierung als Berechnungsgrundlage verwendet.

![Abbildung 3](media/11-preventive-maintenance.png)

![Abbildung 4](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]