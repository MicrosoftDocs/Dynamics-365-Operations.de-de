---
title: Arbeitsauftragspools
description: In diesem Thema wird beschrieben, wie Sie mit Arbeitsauftragspools im Anlagenmanagement arbeiten.
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875673"
---
# <a name="work-order-pools"></a>Arbeitsauftragspools


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Mit Hilfe von Arbeitsauftragspools können Sie Arbeitsaufträge gruppieren, die etwas gemeinsam haben. Sie können z.B. Arbeitsauftragspools anlegen für

- Arbeitsteams, z.B. Wartungspersonal A, Wartungspersonal B  

- Fachkenntnisse, z.B. Elektriker oder Installateure  

- physische Standorte  

- Zeitpläne, z.B. Wochen oder andere Zeiträume  


Bei Bedarf kann ein Arbeitsauftrag in mehreren Arbeitsauftragspools platziert werden.


## <a name="create-work-order-pool"></a>Arbeitsauftragspool anlegen

Unter **Alle Auftragspools** oder **Aktive Auftragspools** können Sie sich einen Überblick über Ihre Auftragspools verschaffen und neue Pools anlegen.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsauftragspools** > **Alle Auftragspools** oder **Aktive Auftragspools**.

2. Klicken Sie auf **Neu**.

3. Geben Sie in das Feld **Pool** eine Arbeitsauftragspool-ID und in das Feld **Name** einen Namen ein.

4. Wählen Sie „Ja“ auf der Umschalttaste **Aktiv**, um anzuzeigen, dass der Arbeitsauftragspool aktiv ist.

5. Wählen Sie „Ja“ auf der Schaltfläche **Arbeitsauftragsbeziehungen löschen**Umschalten, wenn Sie möchten, dass Arbeitsaufträge automatisch aus dem Arbeitsauftragspool entfernt werden.

6. Wählen Sie im Feld **Lebenszykluszustand löschen** den Lebenszykluszustand des Arbeitsauftrags aus. So könnte beispielsweise der Lebenszykluszustand des Arbeitsauftrags für die Fertigstellung eines Arbeitsauftrags so eingestellt werden, dass er automatisch Beziehungen zu Arbeitsauftragspools löscht.

7. Sie können sofort mit dem Hinzufügen von Arbeitsaufträgen zu Ihrem Arbeitsauftragspool beginnen. Klicken Sie auf der Seite **Arbeitsaufträge** FastTab auf **Zeile hinzufügen**.

8. Wählen Sie einen Arbeitsauftrag im Feld **Arbeitsauftrag** aus. Die Bezugsfelder werden automatisch aktualisiert.

9. Wiederholen Sie die Schritte 7-8, wenn Sie weitere Arbeitsaufträge hinzufügen möchten.

10. Im Feld **Sortierreihenfolge** können Sie angeben, ob die Arbeitsaufträge in einer bestimmten Reihenfolge ausgeführt werden sollen. Fügen Sie die Nummern 1, 2, 3 usw. ein, um eine bestimmte Reihenfolge für die ausgewählten Arbeitsaufträge anzugeben.

11. Klicken Sie auf die Schaltfläche **Arbeitsaufträge**, um eine Liste aller im Arbeitsauftragspool enthaltenen Arbeitsaufträge anzuzeigen.

12. Klicken Sie auf die Schaltfläche **Kapazitätsbelastung**, um **Kapazitätsbelastung** zu öffnen, um die Kapazitätsbelastung für Wartungsplan, nicht geplante Arbeitsaufträge und geplante Arbeitsaufträge zu berechnen und anzuzeigen.

13. Klicken Sie auf die Schaltfläche **Artikelprognose**, um **Artikelprognose** zu öffnen, um Prognosen für Artikel (Ersatzteile und andere benötigte Artikel) zu berechnen und anzuzeigen, die sich auf Wartungspläne, nicht geplante Arbeitsaufträge und geplante Arbeitsaufträge beziehen.

14. Klicken Sie auf die Schaltfläche **Bestellanforderung Arbeitsauftrag**, um die Liste **Bestellanforderung Arbeitsauftrag** zu öffnen, um eine Liste der Bestellanforderungen zu sehen, die sich auf die Arbeitsaufträge im Arbeitsauftragspool beziehen.

15. Klicken Sie auf die Schaltfläche **Arbeitsauftragsbestellung**, um die Liste **Arbeitsauftragsbestellung** zu öffnen und eine Liste der Bestellungen zu sehen, die sich auf die Arbeitsaufträge im Arbeitsauftragspool beziehen.

>[!NOTE]
>Wenn ein Arbeitsauftragspool für Ihre Arbeitsvorbereitung nicht mehr relevant ist, setzen Sie das Kontrollkästchen **Aktiv** für diesen Pool in der Listenansicht **Auftragspool** auf „Nein“.

Aktivieren Sie das Kontrollkästchen **Arbeitsauftragsbeziehungen löschen**, wenn Sie alle Arbeitsauftragszeilen löschen möchten, z.B. um einen leeren Pool zu erstellen, den Sie später für andere Arbeitsaufträge verwenden können. Denken Sie daran, das Kontrollkästchen **Arbeitsauftragsbeziehungen löschen** zu deaktivieren, wenn Sie den Arbeitsauftragspool zum späteren Anlegen neuer Arbeitsauftragsbeziehungen verwenden möchten.


![Abbildung 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Arbeitsauftrag zu einem Arbeitsauftragspool hinzufügen

Wie im obigen Abschnitt beschrieben, können Sie beim Anlegen des Vorrats Arbeitsaufträge zu einem Arbeitsauftragspool hinzufügen. Sie können einen Arbeitsauftrag auch aus einer der Listen **Alle Arbeitsaufträge** zu einem Arbeitsauftragspool hinzufügen.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag in der Liste aus und klicken Sie auf **Arbeitsauftragspool**.

3. Wählen Sie „Hinzufügen“ im Feld **Hinzufügen/Entfernen**.

4. Wählen Sie den Arbeitsauftragspool im Feld **Pool** aus.

5. Klicken Sie auf **OK**.

6. Nachdem Sie einen Arbeitsauftrag zu einem Arbeitsauftragspool hinzugefügt haben, wenn Sie den Arbeitsauftrag in einer bestimmten Reihenfolge im Pool platzieren möchten: Öffnen Sie eine der Listenseiten des Arbeitsauftragspools, wählen Sie den Pool aus und klicken Sie auf **Bearbeiten**, und passen Sie die Sortierreihenfolge der im Pool enthaltenen Arbeitsaufträge im Feld **Arbeitsauftragspool**Formular > **Arbeitsaufträge** FastTab > **Sortierauftrag** an.

Wenn Sie den ausgewählten Arbeitsauftrag aus einem Arbeitsauftragspool entfernen möchten, wählen Sie in Schritt 3 „Entfernen“.

