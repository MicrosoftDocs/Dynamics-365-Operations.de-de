---
title: Einführung in funktionale Standorte
description: Dieses Thema bietet einen Überblick über funktionale Standorte in Asset Management.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea318d750f1ef18f270fa246ab54ecb63aa790
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888834"
---
# <a name="introduction-to-functional-locations"></a>Einführung in funktionale Standorte

[!include [banner](../../includes/banner.md)]

 

Dieses Thema bietet einen Überblick über funktionale Standorte in Asset Management. Funktionale Standorte sind Elementen einer technischen Struktur, wie die Funktionseinheiten in einem System. Funktionale Standorte werden hierarchisch erstellt, und Sie installieren Anlagen für sie. Das Einrichten von funktionalen Standorten in Ihrem Unternehmen hängt von den Anforderungen des Unternehmens ab.

Nachfolgend sind einige Beispiele für die Verwendung von funktionalen Standorten aufgeführt:

- **Funktional** – Die funktionalen Standorte können benutzerorientiert sein und verwendet werden, um Anlagen zu verwalten, die ein ähnliches Verhalten haben.
- **Prozessbezogen** – Die funktionalen Standorte können Workflow-orientiert sein.
- **Räumlich** – Die funktionalen Standorte können geografische Standorte darstellen.

Jeder funktionale Standort wird in Asset Management eigenständig verwaltet. Nachfolgend sind einige der wichtigsten Funktionen von funktionalen Standorten aufgeführt:

- Einrichten von Spezifikationen für funktionale Standorte.
- Einrichten von Anlagenspezifikationsanforderungen.
- Einrichten von Wartungssequenzen für die vorbeugende und reagierende Wartung.
- Verwalten von installierten Anlagen.
- Nachverfolgen von aktiven Anfragen und Arbeitsaufträge, die sich auf installierte Anlagen beziehen.
- Nachverfolgen von Fehlern, die für Anlagen erfasst wurden.
- Nachverfolgen von Wartungskosten für Anlagen, die zu einem funktionalen Standort gehören, zu jedem beliebigen Zeitpunkt.

Funktionale Standorte ermöglichten das Nachverfolgen von Anlagen in Bezug auf Anfragen, Arbeitsaufträge, Fehlererfassungen, Bedingungsbewertungen, Produktionsstoperfassungen und Anlagenzählererfassungen.

> [!NOTE]
> Auch wenn eine Anlage während ihrer Lebensdauer an verschiedenen funktionalen Standorten installiert wird, können die Kosten jedem Standort zugeordnet werden. Dies bedeutet, dass sich Anlagenkosten immer auf den funktionalen Standort beziehen, an dem die Anlage zu einem bestimmten Zeitpunkt installiert war.

Funktionale Standorte sind **nicht** flexibel. Daher können Sie nach dem Einrichten eine funktionalen Standorthierarchie die Standorte darin nicht mehr verschieben. 

Nachdem Sie eine funktionale Standorthierarchie erstellt haben, besteht der nächste Schritt darin, Anlagen an ihm zu installieren. Weitere Informationen finden Sie unter [Anlagen an funktionalen Standorten installieren](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Alle funktionalen Standorte

Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Funktionale Standorte** \> **Alle funktionalen Standorte**, um die Listenseite **Aktive funktionale Standorte** zu öffnen. Auf dieser Seite werden alle funktionalen Standorte und einige der Informationen angezeigt, die sich auf die einzelnen Standorte beziehen. Um nur aktive funktionale Standorte anzuzeigen, wählen Sie **Aktive funktionale Standorte** aus. Um nur die funktionalen Standorte anzuzeigen, denen Sie als Bearbeiter zugeordnet sind, wählen Sie **Meine aktiven funktionalen Standorte** aus. (Diese Beziehung wird auf der Seite **Arbeitskräfte** festgelegt. Weitere Informationen finden Sie unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).)

Wählen Sie auf der Listenseite **Alle funktionalen Standorte** eine Verknüpfung in der Spalte **Funktionaler Standort** aus, um die Details für den ausgewählten Datensatz anzuzeigen. Um den funktionalen Standort zu bearbeiten, wählen Sie die Schaltfläche **Bearbeiten**. Die Detailansicht zeigt detaillierte Informationen an, die sich auf den Standort beziehen. Sie enthält auch den Bereich **Zugehörige Informationen** auf der rechten Seite. Dieser Bereich zeigt die Hierarchie des funktionalen Standorts an. Sie können den Bereich **Zugehörige Informationen** erweitern bzw. reduzieren.

Die Schaltflächen im Aktivitätsbereich sind auf Registerkarten zusammengefasst. Die folgende Tabelle beschreibt kurz die Schaltflächen, die sich auf Anlagenmanagement beziehen.

| Name der Schaltfläche                         | Beschreibung                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Bearbeiten                                | Zwischen Anzeigemodus und Bearbeitungsmodus der Seite wechseln.                                                                                         |
| Neue                                 | Neuen funktionalen Standort erstellen.                                                                                                            |
| Löschen                              | Ausgewählten funktionalen Standort löschen.                                                                                                     |
| Umbenennen                              | Ausgewählten funktionalen Standort umbenennen.                                                                                                     |
| Struktur funktionaler Standorte kopieren  | Kopiert die funktionale Standorthierarchie.                                                                                                      |
| Anlage installieren                       | Installiert eine Anlage, einschließlich untergeordneter Anlagen, am funktionalen Standort.                                                                        |
| Anlage ersetzen                       | Ersetzt die Anlagenhierarchie durch eine andere Anlagenhierarchie am funktionalen Standort.                                                         |
| Kostensteuerung                        | Öffnen Sie die Seite **Kostensteuerung für funktionalen Standort**, auf der Sie eine Kostenberechnung für den ausgewählten funktionalen Standort ausführen können.                |
| Stundenüberwachung                        | Öffnen Sie die Seite **Stundenüberwachung für funktionalen Standort**, auf der Sie eine Kostenberechnung für den ausgewählten funktionalen Standort ausführen können.                |
| Anlagen                              | Öffnen Sie die Seite **Alle Anlagen**, auf der Sie ein Liste aller Anlagen anzeigen können, die dem ausgewählten funktionalen Standort zugeordnet sind.                      |
| Anforderungen                            | Öffnen Sie die Seite **Aktive Anfragen**, auf der Sie ein Liste aller Anfragen anzeigen können, die dem ausgewählten funktionalen Standort zugeordnet sind.               |
| Arbeitsaufträge                         | Öffnen Sie die Seite **Aktive Arbeitsaufträge**, auf der Sie ein Liste aller Arbeitsaufträge anzeigen können, die dem ausgewählten funktionalen Standort zugeordnet sind.         |
| Fehler                              | Öffnen Sie die Seite **Anlagenfehler**, auf der Sie ein Liste aller Anlagenfehlererfassungen anzeigen können, die dem ausgewählten funktionalen Standort zugeordnet sind. |
| Status für funktionalen Standort aktualisieren    | Aktualisiert die Phase des ausgewählten funktionalen Standorts.                                                                                        |
| Lebenszyklusstatusprotokoll                 | Hier wird ein Protokoll angezeigt, das die Phasen des ausgewählten funktionalen Standorts anzeigt.                                                                        |
