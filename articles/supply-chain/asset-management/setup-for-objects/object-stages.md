---
title: Anlagenlebenszyklusstatus
description: In diesem Artikel werden Anlagenlebenszyklusstatus und Lebenszyklusmodelle in Anlagenverwaltung erläutert.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b1ff9438437e6c1ff33bab9a7ba0361029cb6d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901059"
---
# <a name="asset-lifecycle-states"></a>Anlagenlebenszyklusstatus

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel werden Anlagenlebenszyklusstatus und Lebenszyklusmodelle in Anlagenverwaltung erläutert. Anlagenlebenszyklusstatus werden verwendet, um festzulegen, ob eine Anlage aktiv oder inaktiv ist. So können Sie zum Beispiel Anlagenlebenszyklusstatus wie **Erstellt**, **Aktiv** und **Ausgeschieden** einrichten.

> [!NOTE]
> - Anforderungslebenszyklusstatus sind mit Anlagenlebenszyklusstatus verknüpft. Wenn Sie eine Anforderung in einen neuen Anforderungslebenszyklusstatus ändern, wird die Anlage, die der Anforderung zugeordnet ist, in einen neuen Anlagenlebenszyklusstatus geändert. Wenn beispielsweise der Lebenszyklusstatus einer Anforderung in **Zugang** geändert wird, wird der Lebenszyklusstaus der zugeordneten Anlage in den Lebenszyklusstatus geändert, der im Feld **Eingehender Lebenszyklusstatus** im Inforegister **Anlagenlebenszyklusstatus** der Seite **Anlagenlebenszyklusstatus-Modelle** ausgewählt ist. 


Anlagenlebenszyklusstatus können in Anlagenlebenszyklusmodellen eingerichtet werden, in denen Sie die erforderlichen Lebenszyklusstatus für unterschiedliche Arten von Anlagen definieren können. Sie richten zunächst Lebenszyklusstatus ein. Dann erstellen Sie ein Lebenszyklusmodell und wählen Lebenszyklusstatus dafür aus.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Lebenszyklusstatus** aus.
2. Wählen Sie **Neu** aus, um einen neuen Anlagenlebenszyklusstatus zu erstellen.
3. Geben Sie im Feld **Lebenszyklusstatus** eine Kennung für den Lebenszyklusstatus ein.
4. Geben Sie im Feld **Name** eine Beschreibung ein.

    Das Feld **Lebenszyklusmodelle** zeigt die Anzahl von Anlagenlebenszyklusmodellen an, die diesen Anlagenlebenszyklusstatus verwenden.

5. Legen Sie für die Option **Aktiv** den Wert **Ja** fest, wenn dieser Lebenszyklusstatus ein aktiver Lebenszyklusstatus sein soll (das heißt, wenn Arbeitsaufträge für Anlagen erstellt werden können, die in diesem Lebenszyklusstatus sind).
6. Legen Sie für die Option **Offene Kalenderpositionen löschen** den Wert **Ja** fest, wenn offene Anlagen-Kalenderpositionen, die den Anlagenlebenszyklusstatus **Erstellt** haben, gelöscht werden sollen, wenn sie in diesem Lebenszyklusstatus sind. Diese Einstellung ist hilfreich, wenn Sie alle offenen Wartungspläne bereinigen möchten, die nicht mehr für die Anlage relevant sind (die Anlage ist beispielsweise nicht mehr aktiv).

> [!NOTE]
> Anlagenlebenszyklusstatus, Anlagenlebenszyklusmodelle und Anlagentypen stehen in Beziehung. Sie werden auf die gleiche Weise wie Arbeitsauftrags-Lebenszyklusstatus, Arbeitsauftrags-Lebenszyklusmodelle und Arbeitsauftragstypen verwendet. 


Nachdem Sie die erforderlichen Anlagenlebenszyklusstatus erstellt haben, können Sie Lebenszyklusstatus in den Anlagenlebenszyklusmodellen einrichten.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Anlagen** \> **Lebenszyklusmodelle** aus.
2. Wählen Sie **Neu** aus, um ein neues Anlagenlebenszyklusmodell zu erstellen.
3. Geben Sie im Feld **Lebenszyklusmodell** eine Kennung für das Lebenszyklusmodell ein.
4. Geben Sie im Feld **Name** eine Beschreibung ein.

    Das Feld **Lebenszyklusstatus** zeigt die Anzahl der Lebenszyklusstatus an, die im Anlagenlebenszyklusmodell ausgewählt sind. Das Feld **Anlagentypen** zeigt die Anzahl von Anlagentypen an, die im Lebenszyklusmodell verwandt werden.

5. Wählen Sie auf dem Inforegister **Lebenszyklusstatus** die Anlagenlebenszyklusstatus aus, die in das Anlagenlebenszyklusmodell einbezogen werden sollen:

    - Um einen Lebenszyklusstatus für das Lebenszyklusmodell zu verwenden, wählen Sie ihn im Bereich **Verbleibende Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts ![Nach-rechts-Pfeil,](media/15-setup-for-objects.png) um ihn in den Abschnitt **Ausgewählte Lebenszyklusstatus** zu verschieben.
    - Um alle verfügbaren Lebenszyklusstatus im Modell zu verwenden, wählen Sie die Schaltfläche **Alle verfügbaren Lebenszyklusstatus** ![Alle verfügbaren Lebenszyklusstatus](media/20-setup-for-objects.png) aus. Alle Lebenszyklusstatus werden in den Bereich **Ausgewählte Lebenszyklusstatus** verschoben.
    - Um einen Lebenszyklusstatus aus dem Modell zu entfernen, wählen Sie ihn im Bereich **Ausgewählte Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach links ![Nach-links-Pfeil,](media/16-setup-for-objects.png) um ihn in den Abschnitt **Verbleibende Lebenszyklusstatus** zu verschieben.

6. Wählen Sie **Lebenszyklusstatusaktualisierungen**, um festzulegen, welche Anlagenlebenszyklusstatus einem ausgewählten Lebenszyklusstatus folgen können.
7. Verwenden Sie das Inforegister **Anlagenstatus**, wenn Sie Anlagen behandelt, die Sie zwecks Reparatur erhalten. Im Abschnitt **Ein-/ausgehend** können Sie Anlagenlebenszyklusstatus auswählen, um den Workflow einer Anlage anzugeben, die Sie zwecks Reparatur erhalten. Wenn Sie Kunden oder Abteilungen Anlagenausleihen anbieten, wählen Sie im Abschnitt **Ausleihe** die Lebenszyklusstatus für Anlagenausleihen aus.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]