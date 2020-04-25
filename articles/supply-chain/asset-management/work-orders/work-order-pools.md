---
title: Arbeitsauftragspools
description: In diesem Thema wird beschrieben, wie Sie mit Arbeitsauftragspools im Anlagenmanagement arbeiten.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: debff2d6ec9c9e3ba711f62ffefab0546dbd2346
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208868"
---
# <a name="work-order-pools"></a>Arbeitsauftragspools

[!include [banner](../../includes/banner.md)]


Mit Hilfe von Arbeitsauftragspools können Sie Arbeitsaufträge gruppieren, die etwas gemeinsam haben. Nachfolgend finden Sie einige Beispiele von Elementen, die Sie für Arbeitsauftragspools erstellen können:

- Arbeitsteams, z.B. Wartungspersonal A oder Wartungspersonal B  

- Fachkenntnisse, z.B. Elektriker oder Installateure  

- Physische Standorte  

- Zeitpläne, z.B. Wochen oder andere Zeiträume  

Bei Bedarf können Sie einen Arbeitsauftrag in mehrere Arbeitsauftragspools einfügen.


## <a name="create-a-work-order-pool"></a>Arbeitsauftragspool anlegen

Auf der Listenseite **Alle Auftragspools** oder **Aktive Auftragspools** können Sie sich einen Überblick über Ihre Auftragspools verschaffen und neue Pools anlegen.

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsauftragspools** > **Alle Auftragspools** oder **Aktive Auftragspools**.

2. Wählen Sie **Neu** aus.

3. Geben Sie im Feld **Pool** eine Kennung für den Arbeitsauftragspool ein.

4. Geben Sie im Feld **Name** einen Namen ein.

5. Wählen Sie **Ja** für die Option **Aktiv**, um anzuzeigen, dass der Arbeitsauftragspool aktiv ist.

6. Wählen Sie **Ja** für die Option **Arbeitsauftragsbeziehungen löschen**, wenn Sie möchten, dass Arbeitsaufträge automatisch aus dem Arbeitsauftragspool entfernt werden.

7. Wählen Sie im Feld **Lebenszykluszustand löschen** den Lebenszykluszustand des Arbeitsauftrags aus. So könnte beispielsweise der Lebenszykluszustand des Arbeitsauftrags für die Fertigstellung eines Arbeitsauftrags so eingestellt werden, dass er automatisch Beziehungen zu Arbeitsauftragspools löscht.

    Sie können sofort mit dem Hinzufügen von Arbeitsaufträgen zu Ihrem Arbeitsauftragspool beginnen.

8. Wählen Sie auf dem Inforegister **Arbeitsaufträge** **Zeile hinzufügen**.

9. Wählen Sie einen Arbeitsauftrag im Feld **Arbeitsauftrag** aus. Die Bezugsfelder werden automatisch aktualisiert.

10. Wiederholen Sie die Schritte 8 bis 9, um weitere Arbeitsaufträge hinzuzufügen.

11. Wenn die Arbeitsaufträge, die von Ihnen hinzugefügt zugefügt wurden, in einer bestimmten Reihenfolge erfolgen sollen, können Sie im Feld **Sortierreihenfolge** die Nummern **1**, **2**, **3** usw. eingeben, um diese Reihenfolge anzugeben.

12. Um eine Liste aller Arbeitsaufträge anzuzeigen, die im Arbeitsauftragspool enthalten sind, wählen Sie im Aktivitätsbereich auf dem Inforegister **Arbeitsauftragspool** in der Gruppe **Zugehörigen Arbeitsauftragspool anzeigen** **Arbeitsaufträge** aus, um die Listenseite **Alle Arbeitsaufträge** zu öffnen.

13. Um die Kapazitätsauslastung für den Wartungszeitplan, ungeplante und geplante Arbeitsaufträge zu berechnen, wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftragspool** in der Gruppe **Zugehörigen Arbeitsauftragspool anzeigen** **Kapazitätsauslastung** aus, um das Dialogfeld **Kapazitätsauslastung berechnen** zu öffnen.

14. Um die Prognosen für Artikel (Ersatzteile und andere erforderliche Artikel) zu berechnen, die mit dem Wartungszeitplan, nicht geplanten Arbeitsaufträgen und geplanten Arbeitsaufträgen verbunden sind, wählen Sie im Aktivitätsbereich auf der Registerkarte **Arbeitsauftragspool** in der Gruppe **Zugehörigen Arbeitsauftragspool anzeigen** **Artikelplanung** aus, um das Dialogfeld **Artikelprognose berechnen** zu öffnen.

15. Um eine Liste aller Bestellanforderungen anzuzeigen, die mit den Arbeitsaufträgen im Arbeitsauftragspool verbunden sind, wählen Sie im Aktivitätsbereich auf dem Inforegister **Arbeitsauftragspool** in der Gruppe **Beschaffung** **Arbeitsauftrag – Bestellanforderung** aus, um die Listenseite **Arbeitsauftrag – Bestellanforderung** zu öffnen.

16. Um eine Liste aller Bestellungen anzuzeigen, die mit den Arbeitsaufträgen im Arbeitsauftragspool verbunden sind, wählen Sie im Aktivitätsbereich auf dem Inforegister **Arbeitsauftragspool** in der Gruppe **Beschaffung** **Arbeitsauftrag – Einkauf** aus, um die Listenseite **Arbeitsauftrag – Einkauf** zu öffnen.

>[!NOTE]
>Wenn ein Arbeitsauftragspool für Ihre Arbeitsvorbereitung nicht mehr relevant ist, setzen Sie die Option **Aktiv** für diesen Pool in der Listenansicht der Seite **Arbeitsauftragspool** auf **Nein**.

Um alle Arbeitsauftragspositionen zu löschen, setzen Sie die Option **Arbeitsauftragsbeziehungen löschen** auf **Ja**. Diese Option ist hilfreich, wenn Sie beispielsweise einen leeren Pool erstellen möchten, den Sie für andere Arbeitsaufträge später verwenden können. Denken Sie daran, die Option **Arbeitsauftragsbeziehungen löschen** auf **Nein** zu setzen, wenn Sie bereit sind, den Arbeitsauftragspool zum späteren Anlegen neuer Arbeitsauftragsbeziehungen zu verwenden.

In der folgenden Abbildung wird ein Beispiel der Listenseite **Arbeitsauftragspool** angezeigt.

![Abbildung 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Arbeitsauftrag zu einem Arbeitsauftragspool hinzufügen

Wie im vorherigen Abschnitt beschrieben, können Sie beim Anlegen des Pools Arbeitsaufträge zu einem Arbeitsauftragspool hinzufügen. Sie können Arbeitsaufträge einem Arbeitsauftragspool auf der Listenseite **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** hinzufügen.

1. Wählen Sie den Arbeitsauftrag aus, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Arbeitsauftrag** in der Gruppe **Verwalten** **Arbeitsauftragspool** aus.

2. Wählen Sie den Arbeitsauftrag in der Liste aus und klicken Sie auf **Arbeitsauftragspool**.

3. Im Dialogfeld **Arbeitsauftragspool verwalten** im Feld **Hinzufügen/Entfernen** wählen Sie **Hinzufügen** aus.

4. Wählen Sie den Arbeitsauftragspool im Feld **Pool** aus.

5. Wählen Sie **OK**.

6. Um den Arbeitsauftrag zu sperren, den Sie in einer bestimmten Reihenfolge im Arbeitsauftragspool hinzugefügt haben, wählen Sie auf der Listenseite **Alle Arbeitsauftragspools** oder **Aktive Arbeitsauftragspools** den Pool aus, und wählen Sie dann **Bearbeiten**. Verwenden Sie anschließend auf der Seite **Arbeitsauftragspool** auf dem Inforegister **Arbeitsaufträge** das Feld **Sortierreihenfolge**, um die Sortierreihenfolge der Arbeitsaufträge anzupassen, die im Pool enthaltenen sind.

Wenn Sie einen Arbeitsauftrag aus einem Arbeitsauftragspool entfernen möchten, wiederholen Sie diese Schritte, aber wählen in Schritt 3 **Entfernen**.

