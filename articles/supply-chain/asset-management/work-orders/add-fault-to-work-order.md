---
title: Fehler zum Arbeitsauftrag hinzufügen
description: In diesem Thema wird beschrieben, wie Fehlererfassungen zu Arbeitsaufträgen in Asset Management hinzugefügt werden.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875677"
---
# <a name="add-fault-to-work-order"></a>Fehler zum Arbeitsauftrag hinzufügen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Sie können einem Arbeitsauftrag Fehlereinstellungen im Fehlerdesigner hinzufügen. Die Anlage, die im Arbeitsauftrag ausgewählt wird, muss Anlagentypen enthalten, mit denen ein oder mehrere Fehlerdatensätze verbunden sind. Lesen Sie mehr über die Einstellungen im Abschnitt [Fehlermanagement](../setup-for-work-orders/fault-management.md).

1. Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie in der Liste den Arbeitsauftrag aus, für den Sie eine Fehlererfassung vornehmen möchten, und klicken Sie auf **Anlagenfehler**.

3. Klicken Sie auf dem Inforegister **Symptome** auf **Position hinzufügen**. Eine laufende Fehlernummer wird automatisch im **Fehler** eingefügt.

4. Wählen Sie das zutreffende Symptom im Feld **Fehlersymptom** aus.

5. Wählen Sie **Fehlerbereich** und **Fehlertyp** aus.

6. Das Feld **Fehlerdatum** wird automatisch auf das aktuelle Datum festgelegt. Bei Bedarf können Sie ein anderes Datum auswählen.

7. Im Inforegister **Ursachen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die die Ursache des Problems beschreibt.

8. Im Inforegister **Lösungen für ausgewähltes Symptom** fügen Sie eine Position hinzu, die eine mögliche Lösung des Problems beschreibt.

9. Klicken Sie auf **Speichern**.

![Abbildung 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Anzeigen von Anlagenfehlern

In der Liste **Anlagenfehler** können Sie eine Übersicht aller Fehler erhalten, die für Anlagen erfasst werden.

Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagenfehler** > **Anlagenfehler**, um die Liste zu öffnen.


## <a name="print-asset-fault-report"></a>Anlagenfehlerberichte drucken

Auf der Listenseite **Alle Anlagen** können Sie einen Anlagenfehlerbericht drucken, der alle Fehlererfassungen sowie eine grafische Übersicht über Fehlerstatistiken anzeigt.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Anlagen** > **Alle Anlagen**.

2. Wählen Sie in der Liste **Anlagen** eine Anlage aus, für die Sie einen Fehlerbericht drucken möchten.

3. Klicken Sie auf der Registerkarte **Allgemein** > Abschnitt **Berichte** auf **Anlagenfehler**.

4. Fügen Sie eine bestimmte Periode ein, oder wählen Sie einen Fehlertyp.

5. Klicken Sie zum Drucken des Berichts auf **OK**.

>[!NOTE]
>Sie können auch einen Fehlerbericht für mehrere Anlagen oder Anlagentypen drucken, indem Sie auf **Anlagenverwaltung** > **Berichte** > **Anlagen** > **Anlagenfehler** klicken.

