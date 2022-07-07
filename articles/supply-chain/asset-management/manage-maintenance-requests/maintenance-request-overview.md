---
title: Wartungsanfragen
description: Dieser Artikel bietet einen Überblick über die Verwaltung von Wartungsanfragen in Anlagenverwaltung.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015637"
---
# <a name="maintenance-requests"></a>Wartungsanfragen

[!include [banner](../../includes/banner.md)]

Wartungsanfragen sind Hinweise oder Erklärungen, die erstellt werden, um einen Manager oder Planer zu informieren, dass für eine Anlage möglicherweise ein Wartungs- oder Reparaturauftrag erforderlich ist, ohne dass jedoch ein Arbeitsauftrag erstellt wird. Wenn den Inhalt einer Wartungsanfrage als gültig betrachtet wird, kann ein Arbeitsauftrag auf Basis der Wartungsanfrage erstellt werden.

Wartungsanfragen können für jede Anlage in Asset Management erstellt werden. Unterschiedliche Arten von Wartungsanfragen können erstellt werden, je nachdem, wie das Unternehmen Wartungsanfragen verwendet. Nachfolgend finden Sie einige Beispiele:

- Wartungsanfragen
- Notizen
- Korrekturen oder Verbesserungen
- Investitionen
- Depotreparatur (Dieser Typ wird verwendet, wenn Sie Anlagen von einem anderen Standort erhalten, damit Sie einen Wartungs- oder Reparaturauftrag erledigen können. Anschließend geben Sie die Anlage zurück.)

## <a name="view-maintenance-requests"></a>Wartungsanfragen anzeigen

Um Wartungsanfragen anzuzeigen, wählen Sie **Anlagenverwaltung** \> **Wartungsanfragen** \> **Alle Wartungsanfragen**, **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte** aus. Jede Listenseite zeigt einige der Informationen an, die sich auf eine Wartungsanfrage bezieht.

![Wartungsanfragen anzeigen.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Verwenden Sie die Listenseite **Meine Wartungsanfragen für funktionale Standorte**, um eine Liste der Wartungsanfragen anzuzeigen, die entweder funktionalen Standorte enthalten, denen Sie als Arbeitskraft zugeordnet sind, oder Anlagen, die an funktionalen Standorten eingerichtet sind, denen Sie als Arbeitskraft zugeordnet sind. (Informationen darüber, wie Sie funktionale Standorte für Wartungsarbeiter einrichten, finden Sie unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Obwohl Informationen zu Kundenkonten in Asset Service Management (externe Wartung) verfügbar sind, sind diese nicht in Asset Management verfügbar (interne Wartung).

Um die Detailansicht eines Datensatzes zu öffnen, wählen Sie auf der Listenseite **Alle Wartungsanfragen** in der Rasteransicht eine Verknüpfung in der Spalte **Wartungsanfrage** aus.

![Details der Wartungsanfrage anzeigen.](media/02-manage-maintenance-requests.png)

Die Schaltflächen im Aktivitätsbereich sind auf Registerkarten zusammengefasst. Die folgende Tabelle beschreibt kurz die Schaltflächen, die sich auf Anlagenmanagement beziehen.

| Name der Schaltfläche                      | Beschreibung |
|----------------------------------|-------------|
| Bearbeiten                             | Dient zum Bearbeiten der ausgewählten Wartungsanfrage. |
| Neue                              | Erstellt eine neue Wartungsanfrage. |
| Löschen                           | Löscht die ausgewählte Wartungsanfrage. |
| Arbeitsauftragspool                  | Verbindet die ausgewählte Wartungsanfrage mit einem Arbeitsauftragspool. |
| Arbeitsauftrag                       | Erstellt einen Arbeitsauftrag basierend auf der ausgewählten Wartungsanfrage. |
| Anlagenfehler                      | Klicken Sie auf **Anlagenfehler**, wo Sie eine Fehlererfassung für die ausgewählte Wartungsanfrage erstellen können. |
| Arbeitsaufträge                      | Hier wird eine Liste aller Arbeitsaufträge angezeigt, die mit der ausgewählten Wartungsanfrage verbunden sind. |
| Wartungsanfragenstatus aktualisieren | Aktualisiert den Status der Wartungsanfrage. |
| Lebenszyklusstatusprotokoll              | Hiermit wird ein Protokoll angezeigt, das den Lebenszyklusstatus der ausgewählten Wartungsanfrage enthält. |
| Wartungsanfragedetails      | Dient zum Drucken eines Berichts, der Details der ausgewählten Wartungsanfrage anzeigt. |
| Anlagenausleihe senden                  | Wählen Sie eine Anlagenausleihe aus, die als temporäre Ersetzung der Anlage dienen soll, die in der ausgewählten Wartungsanfrage ausgewählt ist. |
| Anlagenausleiche zurückgeben                | Erfassen Sie die Anlagenausleihe als zurückgegeben. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]