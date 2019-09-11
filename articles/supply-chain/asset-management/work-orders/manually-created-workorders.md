---
title: Manuell erstellte Arbeitsaufträge
description: In diesem Thema wird erläutert, wie Sie im Anlagenmanagement Arbeitsaufträge manuell anlegen.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875671"
---
# <a name="manually-created-work-orders"></a>Manuell erstellte Arbeitsaufträge

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Sie können Arbeitsaufträge auf zwei Arten manuell anlegen:

- in **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**  
- in **Alle Wartungsanforderungen** oder **Aktive Wartungsanforderungen** oder **Meine Wartungsanforderungen für Technische Standorte**.  

## <a name="create-work-order"></a>Arbeitsauftrag erstellen

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Klicken Sie auf die Schaltfläche **Neu**.

3. Wählen Sie in der Dropdown-Liste **Arbeitsauftrag erstellen** einen Arbeitsauftragstyp aus.

4. Wählen Sie bei Bedarf eine Beschreibung aus.

5. Wählen Sie die Anlage für den Arbeitsauftrag sowie eine Wartungsauftragsart aus.

>[!NOTE]
>Wenn Sie eine Anlage auswählen, stehen Ihnen möglicherweise drei Registerkarten zur Verfügung: Die Registerkarte **Meine Anlagen** enthält Anlagen, die sich auf die Technischen Standorte beziehen, denen Sie (der im System angemeldete Mitarbeiter) zugeordnet werden können (eingerichtet unter [Wartungsarbeiter und Arbeitsgruppen](../setup-for-objects/workers-and-worker-groups.md)). Wenn in [Wartungsarbeiter und Arbeitsgruppen](../setup-for-objects/workers-and-worker-groups.md) keine Technischen Standorte für einen Mitarbeiter eingerichtet sind, ist die Registerkarte **Meine Anlagen** nicht sichtbar. Die Registerkarte **Aktive Anlagen** enthält eine Liste aller Anlagen mit dem Anlagenlebenszyklusstatus „Aktiv“. Die Registerkarte **Anlagenansicht** enthält eine Strukturansicht der funktionalen Standorte und Anlagen, die für diese Standorte installiert sind.

6. Wählen Sie bei Bedarf **Wartungsauftragsartenvariante** und **Wechseln**.

7. Bei Bedarf können Sie den Servicegrad des Arbeitsauftrags im Feld **Service Level** ändern.

8. Wählen Sie in den entsprechenden Feldern das erwartete Start- und Enddatum aus.

9. Klicken Sie auf **OK**, um einen neuen Arbeitsauftrag zu erstellen.

10. Bearbeiten Sie den Arbeitsauftrag bei Bedarf unter **Alle Arbeitsaufträge**.

- Unter **Alle Arbeitsaufträge** können Sie in der Detailansicht mehrere Anlagen zu einem Arbeitsauftrag hinzufügen, indem Sie Zeilen zu den Wartungsaufträgen **Arbeitsauftrag** FastTab hinzufügen. Auf einer Anlage können Sie nur die Wartungsjobtypen auswählen, die auf der für die Anlage ausgewählten Anlagenart definiert sind.  
- Wenn Sie einen Anlagenservicegrad oder einen Kritisch-Wert geändert haben, nachdem Sie sie für einen Arbeitsauftrag verwendet haben (siehe [Anlagen-Service-Level](../setup-for-objects/object-priorities.md) und [Anlagenkritiken](../setup-for-objects/object-criticalities.md)), wird der Servicegrad oder die Kritizität auf dem Arbeitsauftrag nicht entsprechend aktualisiert.
- Der kritische Wert eines Arbeitsauftrags wird jedes Mal neu berechnet, wenn eine Arbeitsauftragszeile auf dem Arbeitsauftrag hinzugefügt oder gelöscht wird.
- Unter **Alle Arbeitsaufträge** Detailansicht > **Leiter** Ansicht > **Terminplan** FastTab können Sie in den Feldern **Verantwortliche Gruppe** oder **Verantwortliche** eine verantwortliche Wartungsgruppe oder einen verantwortlichen Instandhalter auswählen. Diese Einstellungen können geändert werden, solange der Arbeitsauftrag aktiv ist, z.B. wenn sich der Lebenszykluszustand des Arbeitsauftrags ändert. Die automatische Auswahl bei der Erstellung von Arbeitsaufträgen basiert auf dem Setup in **Verantwortliche Wartungsmitarbeiter**. Wenn Sie Arbeitsaufträge hinzufügen oder entfernen, nachdem Sie einen Arbeitsauftrag angelegt haben, und das Feld **Verantwortliche Gruppe** und das Feld **Verantwortliche** bei der Aktualisierung des Arbeitsauftrags leer sind, sucht die Anlagenverwaltung nach einer möglichen Übereinstimmung im Setup-Formular für eine verantwortliche Wartungsmitarbeitergruppe oder einen verantwortlichen Wartungsmitarbeiter. Wenn das Feld **Verantwortliche Gruppe** oder das Feld **Verantwortlicher** bei der Aktualisierung des Arbeitsauftrags bereits ausgefüllt ist, werden keine Änderungen vorgenommen. 

- Unter **Wartungsstatus** können Sie eine Kalkulation durchführen, um sich einen Überblick über die Auslastung der eingehenden und abgeschlossenen Arbeitsaufträge zu verschaffen.  

- Verwenden Sie auf der **Zeilendetails** FastTab die Felder **Breite** und **Länge**, um geografische Koordinaten für die im Arbeitsauftrag ausgewählte Anlage hinzuzufügen.  

## <a name="create-related-work-order"></a>Zugehörigen Arbeitsauftrag erstellen

Sie können einen zugehörigen Arbeitsauftrag zu einem bestehenden Arbeitsauftrag anlegen, wenn Sie z.B. mit primären und sekundären Arbeitsaufträgen arbeiten möchten. Ein neuer Arbeitsauftrag basiert auf einem Arbeitsauftrag aus einem bestehenden Arbeitsauftrag.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag aus, für den Sie einen zugehörigen Arbeitsauftrag erstellen möchten.

3. Klicken Sie auf **Verwandter Arbeitsauftrag**.

4. Wählen Sie im Dropdown-Menü **Verwandter Arbeitsauftrag erstellen** im Feld **Verwandter Arbeitsauftrag** den Arbeitsauftrag aus, für den Sie einen entsprechenden Arbeitsauftrag erstellen möchten.

5. Wählen Sie im Feld **Wartungsauftragsart** eine Wartungsauftragsart und ggf. eine zugehörige Variante der Wartungsauftragsart aus und handeln Sie in den Feldern **Wartungsauftragsart Variante** und **Wechseln**.

6. Wenn dies der erste zugehörige Arbeitsauftrag ist, den Sie erstellen, klicken Sie auf den Auswahlknopf **Neuer Arbeitsauftrag**.

7. Wählen Sie in den entsprechenden Feldern einen **Arbeitsauftragstyp** und eine **Beschreibung**.

8. Ändern Sie bei Bedarf den Servicegrad des Arbeitsauftrags im Feld **Servegrad**.

9. Fügen Sie die erwarteten Start- und Enddaten in die entsprechenden Felder ein.

10. Klicken Sie auf **OK**. Der neue zugehörige Arbeitsauftrag wird in der Liste **Alle Arbeitsaufträge** angezeigt.

11. Wenn Sie einen zugehörigen Arbeitsauftrag auf einem Arbeitsauftrag anlegen, der bereits zugehörige Arbeitsaufträge hat, können Sie den Arbeitsauftrag zu einem bereits zugehörigen Arbeitsauftrag hinzufügen. Dies geschieht durch Anklicken des Optionsschalters **Zu zugehörigem Arbeitsauftrag hinzufügen** in Schritt 6. Dann wählen Sie den zugehörigen Arbeitsauftrag aus, dem Sie einen neuen Arbeitsauftrag hinzufügen möchten. Bearbeiten Sie bei Bedarf die Felder **Service Level**, **Erwarteter Start** und **Erwartetes Ende** und klicken Sie auf **OK**. Der Arbeitsauftrag wird zu dem bestehenden zugehörigen Arbeitsauftrag hinzugefügt.


![Abbildung 1](media/03-work-orders.png)

**Hinweis:** Wenn Sie eine zugehörige Arbeitsauftragsmaske in **Anlagenmanagementparameter** > **Arbeitsaufträge**Link > **Verwandte Arbeitsauftragsmaske** eingerichtet haben, werden Arbeitsauftrags-IDs entsprechend dem Maskenaufbau erstellt. Wenn keine zugehörige Arbeitsauftragsmaske eingerichtet ist, wird die nächste verfügbare Arbeitsauftrags-ID für zugehörige Arbeitsaufträge verwendet.

## <a name="copy-work-order"></a>Arbeitsauftrag kopieren

Es ist möglich, schnell einen neuen Arbeitsauftrag aus einem bestehenden Arbeitsauftrag zu erstellen. Diese Art der Arbeit mit Arbeitsaufträgen unterscheidet sich von der Erstellung von Arbeitsaufträgen auf der Grundlage von Wartungsplänen. Dies ist z.B. sinnvoll, wenn Sie einen Arbeitsauftrag haben, der viele Arbeitsaufträge mit verschiedenen Aufträgen auf verschiedenen Anlagen enthält, die in regelmäßigen Abständen erledigt werden sollen.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag aus, aus dem Sie Inhalte kopieren möchten.

3. Klicken Sie auf **Arbeitsauftrag kopieren**. Die Einrichtung des Arbeitsauftrags aus dem ausgewählten Arbeitsauftrag wird angezeigt. Bei Bedarf können Sie einige der Felder bearbeiten.

4. Klicken Sie auf **OK**, um den neuen Arbeitsauftrag zu erstellen.

5. Bearbeiten Sie den Arbeitsauftrag bei Bedarf unter **Alle Arbeitsaufträge**.

>[!NOTE]
>Wenn der neue Arbeitsauftrag erstellt wird, werden einige Informationen direkt aus dem bestehenden Arbeitsauftrag kopiert. Informationen zu Prognosen, Tools, Wartungschecklisten, Technischen Standorten, Adressen und Terminierung werden nicht kopiert, sondern aus dem aktuellen Setup im Anlagenmanagement initialisiert. Das bedeutet, dass, wenn Änderungen an diesen Daten vom Zeitpunkt der Erstellung des ersten Arbeitsauftrags bis zum Zeitpunkt der Erstellung einer Kopie des Arbeitsauftrags vorgenommen wurden, diese Änderungen in den neuen Arbeitsauftrag aufgenommen werden, den Sie angelegt haben. Beispiele sind Änderungen in den Prognosen oder aktualisierte Wartungschecklisten.


![Abbildung 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a>Arbeitsauftrag basierend auf einer Wartungsanforderung anlegen

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Wartungsanforderungen** > **Alle Wartungsanforderungen** oder **Aktive Wartungsanforderungen**.

2. Wählen Sie die Wartungsanforderung aus, für die Sie einen Arbeitsauftrag anlegen möchten, und klicken Sie auf **Bearbeiten**.

3. Klicken Sie unter **Alle Anfragen** auf **Arbeitsauftrag**.

4. Füllen Sie das Dropdown-Menü **Arbeitsauftrag** aus. Wenn in der Wartungsanforderung ein Wartungsauftrag ausgewählt wurde, können Sie beim Anlegen des Arbeitsauftrags bei Bedarf einen anderen Wartungsauftragstyp auswählen.

5. Klicken Sie auf **OK**. Sie erhalten eine Meldung, die Sie darüber informiert, dass der Arbeitsauftrag angelegt wurde.

6. Wenn Sie sehen möchten, welche Arbeitsaufträge mit einer Wartungsanforderung verbunden sind, markieren Sie die Wartungsanforderung in den Listen **Alle Wartungsanforderungen** oder **Aktive Wartungsanforderungen** und klicken Sie auf die Schaltfläche **Arbeitsaufträge**.


![Abbildung 3](media/05-work-orders.png)


>[!NOTE]
>Arbeitsaufträge können auch automatisch erstellt werden, indem Wartungsplanjobs eingeplant werden, oder indem Wartungspläne oder Wartungsrunden auf einer Anlage „automatisch erstellt“ werden. Arbeitsaufträge, die aus Wartungsanforderungen in **Wartungsplan** erstellt wurden, werden mit den in den Wartungsanforderungen ausgewählten Wartungsauftragsarten erstellt.

