---
title: Anlagenverwaltung in Anlagen integrieren
description: In diesem Thema wird erläutert, wie Sie die Module Anlagenverwaltung und Anlagevermögen integrieren, damit Sie Sachanlagen mit Wartungsanlagen verknüpfen können.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276921"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Anlagenverwaltung in Anlagen integrieren

[!include [banner](../../includes/banner.md)]

Indem Sie die Module **Anlagenverwaltung** und **Anlagevermögen** integrieren, können Sie Sachanlagen mit Wartungsanlagen verknüpfen. Benutzer von Anlagevermögen können dann ein Wartungsobjekt aus einem neuen oder vorhandenen Anlagevermögen erstellen, und Benutzer der Vermögensverwaltung können ein Wartungsobjekt einem vorhandenen Anlagevermögen zuordnen. Diese Funktion erleichtert es Benutzern von Anlagevermögen auch, die Kosten anzuzeigen, die aus Arbeitsaufträgen für zugehörige Wartungsanlagen gebucht wurden.

> [!NOTE]
> In diesem Thema bezeichnen *Wartungsanlagen* Vermögenswerte aus dem Modul **Anlagenverwaltung** und *Anlagevermögen* bezieht sich auf Vermögenswerte aus dem Modul **Anlagevermögen**.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Legen Sie einen Standardspeicherort für neue Wartungsressourcen fest, die aus dem Anlagevermögen erstellt werden (optional).

Durch diese optionale Konfiguration können Sie einen funktionalen Standardspeicherort für neue Wartungsanlagen festlegen, die aus dem Anlagevermögen erstellt werden. Normalerweise schließen Sie diese Konfiguration nur einmal ab, wenn Sie sie überhaupt abschließen.

Führen Sie zum Abschließen dieser Konfiguration die folgenden Schritte durch.

1. Wechseln Sie zu **Anlagenverwaltung \> Einstellungen \> Anlagenverwaltungsparameter**.
1. Wählen Sie auf der Registerkarte **Anlagen** im Feld **Funktionaler Standort** den Standardlagerplatz aus, der für Fertigerzeugnisse verwendet werden soll.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Arbeiten mit integrierten Wartungsanlagen und Sachanlagen

Dieser Abschnitt enthält eine Sammlung von Verfahren, die verschiedene Möglichkeiten zeigen, wie Sie mit den integrierten Funktionen Anlageverwaltung und Anlagevermögen arbeiten können.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Verknüpfen Sie ein vorhandenes Wartungsobjekt mit einem Anlagevermögen

Um ein vorhandenes Wartungsobjekt mit einem Anlagevermögen zu verknüpfen, folgen Sie den Schritten.

1. Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).
1. Wählen Sie eine Anlage aus.
1. Auf dem Inforegister **Anlage** im Feld **Anlagennummer** wählen Sie eine vorhandene Anlage aus.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Zeigen Sie die Anlage an, die einer ausgewählten Wartungsanlage zugeordnet ist

Um die Anlage anzuzeigen, die einer ausgewählten Wartungsanlage zugeordnet ist, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).
1. Wählen Sie eine Anlage aus.
1. Auf dem Inforegister **Anlage** im Feld **Anlagennummer** wählen Sie den Link aus.

    Die Seite **Anlage** für die ausgewählte Anlage wird geöffnet. (Normalerweise befindet sich diese Seite unter **Anlagen \> Anlagen \> Anlagen**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Zeigen Sie die Wartungsanlage an, die einer ausgewählten Anlage zugeordnet ist

Um die Wartungsanlage anzuzeigen, die einer ausgewählten Anlage zugeordnet ist, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.
1. Wählen Sie eine Anlage aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Ansicht** die Option **Wartungsanlage**.

    Die Seite **Wartungsanlage** für die Anlage, die einer ausgewählten Anlage zugeordnet ist, wird geöffnet. (Normalerweise befindet sich diese Seite unter **Anlagenverwaltung \> Anlagen \> Alle Anlagen** .)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Zeigen Sie Wartungskosten an, die mit einer Anlage verbunden sind

Anlagenverwaltungs-Arbeitsaufträge können für Wartungsanlagen gebucht werden, und jeder dieser Arbeitsaufträge hat normalerweise Kosten. Wenn eine Anlage einer Wartungsanlage zugeordnet ist, können Sie direkt von der Anlage aus die entsprechenden Kosten anzeigen.

Um die Wartungskosten anzuzeigen, die einer ausgewählten Anlage zugeordnet sind, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.
1. Wählen Sie eine Anlage aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Ansicht** die Option **Wartungskosten**.

    Die Seite **Wartungskosten** wird geöffnet und zeigt die damit verbundenen Kosten.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Erstellen einer neuen Wartungsanlage für eine bestehende Anlage

Um eine neue Wartungsanlage für eine Anlage zu erstellen, folgen Sie den Schritten.

1. Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.
1. Wählen Sie eine Anlage aus.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Neu** die Option **Wartungsanlage erstellen**. (Wenn diese Option nicht verfügbar ist, ist der ausgewählten Anlage möglicherweise bereits ein Wartungsobjekt zugeordnet.)
1. Beenden Sie die Erstellung der Anlage wie in [Eine Anlage erstellen](../objects/create-an-object.md) beschrieben.

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Erstellen Sie eine neue Anlage und eine neue Wartungsanlage dafür

Um eine neue Anlage zu erstellen und eine neue Wartungsanlage dafür hinzuzufügen, folgen Sie den Schritten.

1. Wechseln Sie zu **Anlagen \> Anlagen \> Anlagen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Beenden Sie die Erstellung der Anlage wie in [Anlage erstellen](../../../finance/fixed-assets/tasks/create-fixed-asset.md) beschrieben.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Anlagenverwaltung** in der Gruppe **Neu** die Option **Wartungsanlage erstellen**.
1. Beenden Sie die Erstellung der Anlage wie in [Eine Anlage erstellen](../objects/create-an-object.md) beschrieben.

### <a name="remove-the-association-between-two-assets"></a>Entfernen Sie die Zuordnung zwischen zwei Anlagen

In einigen Fällen müssen Sie möglicherweise eine Wartungsanlage von der Anlage trennen. Zum Beispiel, wenn Sie [ein neues Wartungsobjekt](#new-maintenance-from-fixed) aus einer Anlage erstellen möchten, müssen Sie zuerst eine vorhandene Zuordnung entfernen.

Um eine vorhandene Zuordnung zwischen einer Wartungsanlage und einer Anlage zu entfernen, folgen Sie den Schritten.

1. Wechseln Sie zu **Anlagenverwaltung \> Anlagen \> Alle Anlagen** (oder **Aktive Anlagen**).
1. Suchen und öffnen Sie die Anlage.
1. Auf dem Inforegister **Anlage** löschen Sie den Wert aus dem Feld **Funktionaler Standort**.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
