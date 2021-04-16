---
title: Fehler zum Arbeitsauftrag hinzufügen
description: In diesem Thema wird beschrieben, wie Fehlererfassungen zu Arbeitsaufträgen in Asset Management hinzugefügt werden.
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
ms.openlocfilehash: 0a79986e3b477865bc1816a1d28c1b7094ae3974
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809805"
---
# <a name="add-fault-to-work-order"></a>Fügen Sie Fehler zum Arbeitsauftrag hinzu

[!include [banner](../../includes/banner.md)]



Sie können einem Arbeitsauftrag Fehler hinzufügen, die im Fehlerdesigner eingerichtet wurden. Mit den Anlagetypen, die für die Anlage verwendet werden, die im Arbeitsauftrag ausgewählt ist, müssen ein oder mehrere Fehlerdatensätze verbunden sein. Weitere Informationen zum Einrichten finden Sie unter [Fehlermanagement](../setup-for-work-orders/fault-management.md).

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.

2. Wählen Sie den Arbeitsauftrag aus, für den Sie eine Fehlererfassung durchführen möchten, und wählen Sie dann im Aktivitätsbereich auf der **Arbeitsauftrag**-Registerkarte in der **Anlage**-Gruppe **Anlagenfehler** aus.

3. Wählen Sie auf dem Inforegister **Symptome** die Option **Position hinzufügen** aus. Eine laufende Fehlernummer wird automatisch im **Fehler** eingegeben.

4. Wählen Sie das zutreffende Symptom im Feld **Fehlersymptom** aus.

5. Wählen Sie in den Feldern **Fehlerbereich** und **Fehlertyp** die entsprechenden Werte aus.

6. Das Feld **Fehlerdatum** wird automatisch auf das aktuelle Datum festgelegt. Sie können bei Bedarf ein anderes Datum auswählen.

7. Im Inforegister **Ursachen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die die Ursache des Problems beschreibt.

8. Im Inforegister **Lösungen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die eine mögliche Lösung des Problems beschreibt.

9. Wählen Sie **Speichern**.

Die folgende Abbildung zeigt das Beispiel einer Fehlererfassung.

![Abbildung 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Anzeigen von Anlagenfehlern

In der Liste **Anlagenfehler** können Sie eine Übersicht aller Fehler erhalten, die für Anlagen erfasst werden.

Auf der Listenseite **Anlagenfehler** können Sie eine Übersicht aller Fehler erhalten, die für Anlagen erfasst wurden. Wählen Sie **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehler** aus, um die Seite zu öffnen.


## <a name="print-asset-fault-report"></a>Anlagenfehlerberichte drucken

Auf der Listenseite **Alle Anlagen** können Sie einen Anlagenfehlerbericht drucken, der alle Fehlererfassungen sowie eine grafische Übersicht über Fehlerstatistiken anzeigt.

1. Wählen Sie **Anlagenverwaltung** > **Allgemeines** > **Anlagen** > **Alle Anlagen**.

2. Wählen Sie die Anlage aus, für die Sie den Fehlerbericht drucken möchten.

3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Allgemein** in der Gruppe **Berichte** **Anlagenfehler** aus.

4. Geben Sie eine bestimmte Periode ein, oder wählen Sie einen Fehlertyp aus.

5. Wählen Sie zum Drucken des Berichts **OK** aus.

>[!NOTE]
>Sie können auch einen Fehlerbericht für mehrere Anlagen oder Anlagentypen drucken, indem Sie **Anlagenverwaltung** > **Berichte** > **Anlagen** > **Anlagenfehler** auswählen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]