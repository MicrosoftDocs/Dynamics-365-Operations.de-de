---
title: Wartungsanfrage-Lebenszyklusstatus
description: In diesem Thema wird beschrieben, wie Wartungsanfrage-Lebenszyklusstatus in Asset Management eingerichtet werden.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c95704b944f86a1cfc0654f0ebf5bc7c79bbeec9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808687"
---
# <a name="maintenance-request-lifecycle-states"></a>Wartungsanfrage-Lebenszyklusstatus

[!include [banner](../../includes/banner.md)]

 


Wartungsanfrage-Lebenszyklusstatus definieren die Phasen, die eine Anfrage durchlaufen kann. Hierzu gehören **Erstellt**, **Aktiv** und **Beendet**. Wenn eine Wartungsanfrage in einen Arbeitsauftrag konvertiert wird, sollte der Wartungsanfrage-Lebenszyklusstatus in **Beendet** oder **Geschlossen** aktualisiert werden, um anzugeben, dass die Wartungsanfrage nicht mehr aktiv ist. Auf der Listenseite **Alle Wartungsanfragen** sehen Sie alle Wartungsanfragen unabhängig von ihrem Lebenszyklusstatus.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Wartungsanfrage-Lebenszyklusstatus einrichten

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Lebenszyklusstatus** aus.
2. Wählen Sie **Neu** aus, um einen Wartungsanfrage-Lebenszyklusstatus zu erstellen.
3. Geben Sie im Feld **Lebenszyklusstatus** eine Kennung für den Lebenszyklusstatus ein.
4. Geben Sie im Feld **Name** einen Namen ein.

    Auf dem Inforegister **Details** wird im Feld **Lebenszyklusmodelle** die Anzahl von Wartungsanfrage-Lebenszyklusmodellen angezeigt, die diesen Lebenszyklusstatus verwenden.

5. Legen Sie auf dem Inforegister **Allgemein** die Option **Aktiv** auf **Ja** fest, wenn eine Wartungsanfrage aktiv sein soll, während sie diesen Lebenszyklusstatus hat.
6. Legen Sie die Option **Tatsächliches Ende festlegen** auf **Ja** fest, wenn automatisch ein tatsächliches Enddatum und eine Uhrzeit für eine Wartungsanfrage eingegeben werden sollen, die diesen Lebenszyklusstatus hat.
7. Legen Sie die Option **Arbeitsauftrag erstellen** auf **Ja** fest, wenn ein Arbeitsauftrag aus einer Wartungsanfrage erstellt werden kann, die diesen Lebenszyklusstatus hat.
8. Legen Sie die Option **Löschen** auf **Ja** fest, wenn eine Wartungsanfrage gelöscht werden kann, während sie diesen Lebenszyklusstatus hat.
9. Im Inforegister **Aktualisieren** sind die Optionen **Eingehend** und **Ausgehend** im Bereich **Anlage** relevant, wenn Sie die Depotreparatur verwenden. Legen Sie die entsprechende Option auf **Ja** fest, wenn der Lebenszyklusstatus von Anlagen, die in einer Wartungsanfrage ausgewählt sind, automatisch zu **Eingehend** oder **Ausgehend** aktualisiert werden soll, wenn der Lebenszyklusstatus der Wartungsanfrage auf **Eingehend** oder **Ausgehend** festgelegt ist.

Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfrage-Lebenszyklusstatus**.

![Seite „Wartungsanfrage-Lebenszyklusstatus“](media/02-setup-for-requests.png)

> [!NOTE]
> Wartungsanfrage-Lebenszyklusstatus, -Lebenszyklusstatusgruppen und -typen stehen mit Arbeitsauftrag-Lebenszyklusstatus, -Lebenszyklusstatusgruppen und -typen in Zusammenhang und werden genauso wie diese verwendet. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Wartungsanfrage-Lebenszyklusmodelle einrichten

Nachdem Sie die Lebenszyklusstatus erstellt haben, die für die Wartungsanfragen erforderlich sind, können diese in Lebenszyklusstatusgruppen oder Lebenszyklusmodelle aufgeteilt werden. Wartungsanfrage-Lebenszyklusmodelle werden verwendet, um den Fluss zu erstellen, der für verschiedene Arten von Wartungsanfragen verwendet werden kann. Es sollte mindestens ein Wartungsanfrage-Lebenszyklusmodell erstellt werden.

1. Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Lebenszyklusmodelle** aus.
2. Wählen Sie **Neu** aus, um ein Wartungsanfrage-Lebenszyklusmodell zu erstellen.
3. Geben Sie im Feld **Lebenszyklusmodell** eine Kennung für das Lebenszyklusmodell ein.
4. Geben Sie im Feld **Name** einen Namen ein.

    Auf dem Inforegister **Details** wird im Feld **Lebenszyklusstatus** die Anzahl von Lebenszyklusstatus angezeigt, die in diesem Lebenszyklusmodel ausgewählt sind. Im Feld **Wartungsanfragentypen** wird die Anzahl der Wartungsanfragentypen angezeigt, die dieses Lebenszyklusmodell verwenden.

5. Wählen Sie auf dem Inforegister **Lebenszyklusstatus** die Lebenszyklusstatus aus, die in das Lebenszyklusmodell einbezogen werden sollen:

    - Um einen Lebenszyklusstatus in das Lebenszyklusmodell einzuschließen, wählen Sie ihn im Bereich **Verbleibende Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach rechts ![Nach-Rechts-Pfeil](media/03-setup-for-requests.png), um ihn in den Bereich **Ausgewählte Lebenszyklusstatus** zu verschieben.
    - Um alle verfügbaren Lebenszyklusstatus in das Lebenszyklusmodell einzuschließen, wählen Sie die Schaltfläche **Alle verfügbaren Status auswählen** ![Alle verfügbaren Status auswählen](media/04-setup-for-requests.png) aus. Alle Lebenszyklusstatus werden in den Bereich **Ausgewählte Lebenszyklusstatus** verschoben.
    - Um einen Lebenszyklusstatus aus dem Lebenszyklusmodell zu entfernen, wählen Sie ihn im Bereich **Ausgewählte Lebenszyklusstatus** aus, und klicken Sie dann auf die Schaltfläche mit dem Pfeil nach links ![Nach-Links-Pfeil](media/05-setup-for-requests.png), um ihn in den Bereich **Verbleibende Lebenszyklusstatus** zu verschieben.

6. Auf dem Inforegister **Allgemein** sind die Felder im Abschnitt **Aktualisierungen** relevant, wenn Sie die Depotreparatur verwenden.

    - Wählen Sie im Feld **Lebenszyklusstatus bei Anlagenzugang** den Anlagenlebenszyklusstatus aus, auf den Anlagen, die in einer Wartungsanfrage ausgewählt werden, automatisch aktualisiert werden sollen, wenn sie zur Depotreparatur eingehen.
    - Wählen Sie im Feld **Lebenszyklusstatus bei Anlagenauslieferung** den Lebenszyklusstatus aus, auf den Anlagen, die in einer Wartungsanfrage ausgewählt werden, automatisch aktualisiert werden sollen, wenn sie nach der Reparatur zurückgegeben werden.

Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfrage-Lebenszyklusmodelle**.

![Seite „Wartungsanfrage-Lebenszyklusmodelle“](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]