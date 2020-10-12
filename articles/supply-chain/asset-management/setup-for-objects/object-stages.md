---
title: Anlagenlebenszyklusstatus
description: In diesem Thema werden Anlagenlebenszyklusstatus und Lebenszyklusmodelle in Asset Management erläutert.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889912"
---
# <a name="asset-lifecycle-states"></a>Anlagenlebenszyklusstatus

[!include [banner](../../includes/banner.md)]

 

In diesem Thema werden Anlagenlebenszyklusstatus und Lebenszyklusmodelle in Asset Management erläutert. Anlagenlebenszyklusstatus werden verwendet, um festzulegen, ob eine Anlage aktiv oder inaktiv ist. So können Sie zum Beispiel Anlagenlebenszyklusstatus wie **Erstellt**, **Aktiv** und **Ausgeschieden** einrichten.

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

    - Um einen Lebenszyklusstatus für das Modell zu verwenden, wählen Sie ihn im Bereich **Verbleibende Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts ![Nach-Rechts-Pfeil](media/15-setup-for-objects.png), um ihn in den Bereich **Ausgewählte Lebenszyklusstatus** zu verschieben.
    - Um alle verfügbaren Lebenszyklusstatus im Modell zu verwenden, wählen Sie die Schaltfläche **Alle verfügbaren Lebenszyklusstatus** ![Alle verfügbaren Lebenszyklusstatus](media/20-setup-for-objects.png) aus. Alle Lebenszyklusstatus werden in den Bereich **Ausgewählte Lebenszyklusstatus** verschoben.
    - Um einen Lebenszyklusstatus aus dem Modell zu entfernen, wählen Sie ihn im Bereich **Ausgewählte Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach links ![Nach-Links-Pfeil](media/16-setup-for-objects.png), um ihn in den Bereich **Verbleibende Lebenszyklusstatus** zu verschieben.

6. Wählen Sie **Lebenszyklusstatusaktualisierungen**, um festzulegen, welche Anlagenlebenszyklusstatus einem ausgewählten Lebenszyklusstatus folgen können.
7. Verwenden Sie das Inforegister **Anlagenstatus**, wenn Sie Anlagen behandelt, die Sie zwecks Reparatur erhalten. Im Abschnitt **Ein-/ausgehend** können Sie Anlagenlebenszyklusstatus auswählen, um den Workflow einer Anlage anzugeben, die Sie zwecks Reparatur erhalten. Wenn Sie Kunden oder Abteilungen Anlagenausleihen anbieten, wählen Sie im Abschnitt **Ausleihe** die Lebenszyklusstatus für Anlagenausleihen aus.
