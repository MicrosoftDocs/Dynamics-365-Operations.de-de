---
title: Lebenszyklusstatus für funktionale Standorte
description: In diesem Artikel wird beschrieben, wie funktionale Standortzustände und Lebenszyklusmodelle in Anlagenverwaltung eingerichtet werden.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae56c2b734339343b134be95abe0ce40b70c8a0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934661"
---
# <a name="functional-location-lifecycle-states"></a>Lebenszyklusstatus für funktionale Standorte

[!include [banner](../../includes/banner.md)]

 

In diesem Artikel wird beschrieben, wie funktionale Standort-Lebenszyklusstatus und Lebenszyklusmodelle in Anlagenverwaltung eingerichtet werden. Funktionale Standort-Lebenszyklusstatus definieren die Status, die funktionale Standorte durchlaufen können, zum Beispiel „erstellt“, „aktiv“ und „beendet“. Sie können alle funktionalen Standorte unabhängig von deren Lebenszyklusstatus auf der Listenseite **Alle funktionalen Standorte** anzeigen. Sie können den Status eines funktionalen Standorts ändern, indem Sie ihn auf der Listenseite **Alle funktionalen Standorte** auswählen und dann **Status des funktionalen Standorts aktualisieren** auswählen.

## <a name="set-up-functional-location-lifecycle-states"></a>Lebenszyklusstatus für funktionale Standorte einrichten

1. Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Funktionale Standorte** > **Lebenszyklusstatus** aus.
2. Wählen Sie **Neu** aus, um einen neuen funktionalen Standortstatus zu erstellen.
3. Fügen Sie die Status-ID in das Feld **Lebenszyklusstatus** ein, und geben Sie einen Namen für den funktionalen Standortstatus im Feld **Name** ein. Im Feld **Lebenszyklusmodelle** können Sie die Anzahl der funktionalen Standort-Lebenszyklusmodelle sehen, die den funktionalen Standortstatus verwenden.
4. Wählen Sie im Inforegister **Allgemein** „Ja“ für die Umschaltfläche **Aktiv** aus, wenn der funktionale Standort in diesem Status aktiv sein soll.
5. Wählen Sie auf „Ja“ für die Umschaltfläche **Anlagen erstellen** aus, wenn es möglich sein soll, automatisch eine Anlage mit dem gleichen Namen wie dem des funktionalen Standorts zu erstellen und sie in diesem Status am funktionalen Standort zu installieren.  
>[!NOTE]
>Diese Umschaltfläche bezieht sich auf das Feld **Anlagentyp** im Inforegister **Allgemein** im Formular **Funktionaler Standort** (**Anlagenverwaltung** > **Einstellungen** > **Funktionale Standorte** > **Funktionale Standorttypen**).

6. Wählen Sie „Ja“ für die Umschaltfläche **Standort umbenennen**, wenn es möglich sein soll, den Namen des funktionalen Standorts in diesem Status zu ändern.
7. Wählen Sie „Ja“ für die Umschaltfläche **Neue untergeordnete Standorte**, wenn es möglich sein soll, dem funktionalen Standort in diesem Status neue untergeordnete Standorte hinzuzufügen.
8. Wählen Sie „Ja“ für die Umschaltfläche **Anlagen installieren**, wenn es möglich sein soll, für den funktionalen Standort in diesem Status Anlagen zu installieren.
9. Wählen Sie „Ja“ für die Umschaltfläche **Funktionalen Standort löschen**, wenn es möglich sein soll, den funktionalen Standort in diesem Status zu löschen.
10. Wählen Sie einen Anlagenstatus im Feld **Lebenszyklusstatus** aus, wenn der Anlagenlebenszyklusstatus für alle Anlagen, die am funktionalen Standort installiert sind, in diesem Status automatisch aktualisiert werden soll. Beispiel: Wenn Sie einen funktionalen Standort schließen und den Lebenszyklusstatus des funktionalen Standorts auf „Beendet“ festlegen, möchten Sie den Lebenszyklusstatus der Anlagen, die am funktionalen Standort installiert sind, möglicherweise automatisch in „Nicht verwendet“ ändern.


>[!NOTE]
>Lebenszyklusstatus funktionaler Standorte, Lebenszyklusmodelle und Typen gehören zu Arbeitsauftrag-Lebenszyklusstatus, Arbeitsauftrag-Lebenzyklusmodellen und Arbeitsauftragstypen und werden auf die gleiche Weise verwendet. 

## <a name="set-up-functional-location-lifecycle-models"></a>Einrichten von Lebenszyklusmodellen für funktionale Standorte

Wenn Sie die Lebenszyklusstatus erstellt haben, die für Ihre funktionalen Standorte erforderlich sind, können diese in Gruppen eingeteilt werden. Dies erfolgt, um den Lebenszyklusmodellfluss zu erstellen, der möglicherweise für unterschiedliche Arten von funktionalen Standorten verwendet wird. Es sollte mindestens ein Lebenszyklusmodell für einen funktionalen Standort erstellt werden.

1. Wählen Sie **Anlagenverwaltung** > **Einstellungen** > **Funktionale Standorte** > **Lebenszyklusmodelle** aus.
2. Wählen Sie **Neu** aus, um ein neues Lebenszyklusmodell zu erstellen.
3. Fügen Sie die Lebenszyklusmodelle-ID in das Feld **Lebenszyklusmodell** ein, und geben Sie einen Namen für das Lebenszyklusmodell im Feld **Name** ein. In den Feldern **Funktionale Standorttypen** und **Lebenszyklusstatus** können Sie die Anzahl der funktionalen Standorttypen sehen, die das Lebenszyklusmodell verwenden, sowie die Anzahl der im Lebenszyklusmodell ausgewählten Status.
4. Wählen Sie im Inforegister **Lebenszyklusstatus** die Status aus, die in das Modell einbezogen werden sollen. Dies erfolgt, indem Sie im Abschnitt **Verbleibende Lebenszyklusstatus** auf einen Status klicken und dann auf die ![Vorwärtspfeil](media/02-setup-for-functional-locations.png)- Schaltfläche.
5. Wenn Sie alle verfügbaren Status für ein Modell auswählen möchten, klicken Sie auf die ![Alle verfügbaren Phasen auswählen](media/03-setup-for-functional-locations.png)- Schaltfläche. Alle Status werden in den Abschnitt **Ausgewählte Lebenszyklusstatus** übertragen.
6. Wenn Sie einen ausgewählten Status aus dem Modell entfernen möchten, wählen Sie den Status im Abschnitt **Ausgewählte Lebenszyklusstatus** aus, und wählen Sie dann die ![Zurück-Pfeil](media/04-setup-for-functional-locations.png)- Schaltfläche.
7. Wählen Sie **Lebenszyklusstatusaktualisierungen**, um festzulegen, welche Lebenszyklusstatus einem ausgewählten Status folgen können.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
