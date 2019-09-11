---
title: Wartungsprüflisten
description: In diesem Thema werden Wartungsprüflisten in Asset Management beschrieben.
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875678"
---
# <a name="maintenance-checklists"></a>Wartungsprüflisten


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Wartungsprüflisten werden für Wartungsauftragstypen erstellt und während der Arbeit an Arbeitsaufträgen verwendet. Das Ausfüllen von Wartungsprüflisten ist Teil des Abschlusses eines Arbeitsauftrags. Weitere Informationen zum Einrichten von Wartungsprüflisten für Wartungsauftragstypen im Formular **Wartungsauftragstyp-Standardwerte** finden Sie im Abschnitt [Wartungsauftragstypkategorien und Wartungsauftragstypen, Wartungsauftragstypvarianten, Wartungsauftragsbranchen und Wartungsprüflisten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

Wenn Sie mit Wartungsprüflisten an einem Arbeitsauftrag arbeiten, können Sie die vordefinierten Wartungsprüflisten ausfüllen, die sich auf Wartungsauftragstypen beziehen. Es besteht auch die Möglichkeit, weitere Wartungsprüflisten hinzuzufügen.

## <a name="fill-out-a-maintenance-checklist"></a>Ausfüllen einer Wartungsprüfliste

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag aus und klicken Sie auf **Wartungsprüfliste**.

3. In **Wartungsprüfliste für Arbeitsaufträge** finden Sie Wartungsprüflisten für alle Arbeitsauftragseinzelvorgänge. Wenn die Arbeitsauftragseinzelvorgänge unterschiedliche Wartungsauftragstypen haben, können die Wartungsprüflisten für jeden Arbeitsauftragseinzelvorgang unterschiedlich sein. Wählen Sie einen Arbeitsauftragseinzelvorgang aus, um mit der entsprechenden Wartungsprüfliste zu arbeiten. Details zu einer ausgewählten Wartungsprüflistenposition werden im Inforegister **Positionsdetails** angezeigt.

4. Schließen Sie alle Wartungsprüflistenpositionen nacheinander in der Reihenfolge ab, in der sie angezeigt werden. Eine Wartungsprüflistenposition vom Typ „Kopfzeile“ wird als Überschrift verwendet, um die folgenden Wartungsprüflistenpositionen zu gruppieren. Sie müssen keine Kopfzeile ausfüllen, aber wie bei allen Positionstypen der Wartungsprüfliste ist es auch hier möglich, der Kopfzeile einen **Hinweis** hinzuzufügen.

5. Wenn sich Anweisungen auf eine Wartungsprüflistenposition beziehen, ist das Kontrollkästchen **Anweisungen** aktiviert. Lesen Sie die Anweisungen für die ausgewählte Wartungsprüflistenposition im Inforegister **Positionsdetails** > **Anweisungen**.

6. Die Informationen, die zum Abschließen einer Wartungsprüflistenposition erforderlich sind, können je nach Typ der zugehörigen Wartungsprüfliste variieren. Sie schließen eine Wartungsprüflistenposition ab, indem Sie die Felder im Inforegister **Positionsdetails** ausfüllen. Beispielsweise fügen Sie in einer Zeile vom Typ „Text“ einen **Hinweis** hinzu, der erklärt, was das Ergebnis dieser Prüflistenposition war. In einer Position vom Typ „Messung“ fügen Sie den **Zählerwert**, den Sie am Gerät ablesen, hinzu und ebenso bei Bedarf einen **Hinweis**.

- Wenn Sie eine Wartungsprüflistenposition abgeschlossen haben, aktivieren Sie das Kontrollkästchen **Geprüft** auf der Position, um sie als abgeschlossen zu kennzeichnen. Wenn Sie eine Wartungsprüflistenposition verwerfen möchten, weil sie für den Arbeitsauftragseinzelvorgang nicht relevant ist, aktivieren Sie das Kontrollkästchen **N/V** auf der Position. Wenn eine Wartungsprüflistenposition als **Obligatorisch** markiert ist, müssen Sie sie entweder als „Geprüft“ oder „N/V“ kennzeichnen.  
- Sie können Wartungsprüflistenerfassung nur aktualisieren, wenn sich der Arbeitsauftrag im Lebenszyklusstatus [Aktiv](../setup-for-work-orders/work-order-lifecycle-states.md) befindet.  


## <a name="add-a-maintenance-checklist-line"></a>HInzufügen einer Wartungsprüflistenposition

Wartungsprüflisten werden aus der Definition des Wartungsauftragsstandards erstellt und in einen Arbeitsauftragseinzelvorgang übertragen. Bei Bedarf können Sie Wartungsprüflistenpositionen einem Arbeitsauftragseinzelvorgang hinzufügen. Manuell hinzugefügte Wartungsprüflistenpositionen erhalten den Verweis „Manuell“.

1. Wählen Sie **Wartungsprüfliste für Arbeitsaufträge** den Arbeitsauftragseinzelvorgang aus, für den Sie eine Wartungsprüfliste hinzufügen möchten.

2. Wählen Sie auf dem Inforegister **Wartungsprüflistenpositionen** eine Wartungsprüflisteposition aus und drücken Sie die Pfeiltaste auf Ihrer Tastatur, wenn Sie eine neue Position nach der ausgewählten Wartungsprüflistenposition einfügen möchten. Die nächste Nummer in der Sequenz wird automatisch in das Feld **Positionsnummer** eingefügt. Sie können auch eine Wartungsprüflistenposition auswählen und auf die Schaltfläche **Position hinzufügen** klicken, wenn Sie eine neue Position über der ausgewählten Wartungsprüflistenposition einfügen möchten.

3. Geben Sie im Feld **Name** einen Namen für die Wartungsprüflistenposition ein.

4. Im Feld **Typ** wählen Sie einen Typ für die Wartungsprüflistenposition aus. Für jeden Wartungsprüflistentyp werden die verknüpften Felder im Inforegister **Positionsdetails** angezeigt.  
  a. „Text“ wird verwendet, um eine Wartungsprüflistenposition mit einer Textbeschreibung der Vorgehensweise hinzuzufügen. Dieser Wartungsprüflistentyp kann verwendet werden, wenn Sie möchten, dass ein Mitarbeiter etwas überprüft oder inspiziert, ohne ein bestimmtes (messbares) Ergebnis zu erwarten. Fügen Sie eine Beschreibung der Vorgehensweise im Abschnitt **Anweisungen** auf dem Inforegister **Positionsdetails** ein. b. „Kopfzeile“ wird als Überschrift verwendet, um die Wartungsprüflistenpositionen zu gruppieren, die unter dem Kopf angezeigt werden. Dies ist nützlich, wenn Sie mehrere Wartungsprüflistenpositionen haben, die in bestimmte Bereiche unterteilt werden können. Geben Sie im Feld **Name** einen aussagekräftigen Namen ein.  
  c. „Vorlage“ ist nicht verfügbar, wenn Sie eine Wartungsprüflistenposition manuell auf einen Arbeitsauftragseinzelvorgang hinzufügen.  
  d. „Variabel“ wird verwendet, um ein mögliches Ergebnis in einem Bereich einer Wartungsprüflistenposition zu definieren. Die Einrichtung von Variablen der Wartungsprüfliste ist in [Wartungsauftragstypkategorien und Wartungsauftragstypen, Variationen von Wartungsaufträgen, Wartungsauftragsbranchen und Wartungsprüflisten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md). Geben Sie im Feld **Name** einen Namen zur Beschreibung der Variabel ein. Wählen Sie im Feld **Variabel** die Variabel aus. Fügen Sie eine Beschreibung der Vorgehensweise im Abschnitt **Anweisungen** auf dem Inforegister **Positionsdetails** ein.  
  e. „Messung“ wird verwendet, um eine bestimmte Messung zu erfassen. Geben Sie im Feld **Name** einen Namen für die Messung ein. Wählen Sie auf dem Inforegister **Positionsdetails** **Zähler** und **Einheit** aus. Fügen Sie eine Beschreibung dessen, was zu tun ist, in den Abschnitt **Anweisungen** ein.  

5. Wenn Sie mit dem manuellen Hinzufügen von Wartungsprüflistenpositionen fertig sind, füllen Sie die Positionen wie im vorherigen Abschnitt beschrieben aus.

>[!NOTE]
>In **Wartungsprüfliste für Arbeitsaufträge** können Sie Wartungsprüflistenpositionen mit der Referenz „Einzelvorgangstyp“ nicht löschen. Sie können nur Wartungsprüflisten mit dem Verweis „Manuell“ löschen, die Sie oder andere Wartungsarbeiter manuell angelegt haben.


![Abbildung 1](media/14-work-orders.png)

