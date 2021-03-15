---
title: Einführung in Anlagen
description: Dieses Thema bietet einen Überblick über Anlagen in Asset Management.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f629ebdf7423ca75fe215b0a3223478685fe95c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018570"
---
# <a name="introduction-to-assets"></a>Einführung in Anlagen

[!include [banner](../../includes/banner.md)]

 

Dieses Thema bietet einen Überblick über Anlagen in Asset Management. Eine *Anlage* ist jeder Ausrüstungstyp, wie z. B. eine Maschine oder ein Maschinenteil, der Wartung, Service oder Reparatur benötigt.

Eine Anlage wird automatisch mit den dazugehörigen Informationen aktualisiert. Beispielsweise kann es sich bei den zugehörigen Informationen um neue oder aktualisierten Arbeitsaufträge handeln. Sie können eine Anlage mit der Menüoption **Alle Anlagen** oder **Ausstehende Anlagen** erstellen. In diesem Thema wird erläutert, wie Anlagen mit der Menüoption **Alle Anlagen** erstellt werden. Weitere Informationen zum Erstellen von Anlagen mit der Menüoption **Ausstehende Anlagen** finden Sie unter [Anlagen basierend auf Bestellungen erstellen](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Alle Anlagen

Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen**. Die Listenseite **Alle Anlagen** zeigt alle Anlagen und einige der Informationen an, die sich darauf beziehen. Um nur aktive Anlagen anzuzeigen, wählen Sie **Aktive Anlagen** aus. Um nur Anlagen anzuzeigen, die an funktionalen Standorten installiert sind, denen Sie als Wartungsmitarbeiter zugeordnet sind, wählen Sie **Meine aktiven Anlagen** aus. (Diese Beziehung wird auf der Seite **Arbeitskräfte** festgelegt. Weitere Informationen finden Sie unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).)

Wählen Sie in der Rasteransicht **Alle Anlagen** eine Verknüpfung in der Spalte **Anlage** aus, um die Details für den ausgewählten Datensatz anzuzeigen. Um den Datensatz zu bearbeiten, wählen Sie die Schaltfläche **Bearbeiten**. Die Detailansicht zeigt detaillierte Informationen an, die sich auf die Anlage beziehen. Der Bereich **Zugehörige Informationen** auf der rechten Seite enthält zusätzliche auf Anlagen bezogene Informationen. Erweitern Sie den Bereich, um die zugehörigen Informationen für die ausgewählte Anlage anzuzeigen.

Die Schaltflächen im Aktivitätsbereich sind auf Registerkarten zusammengefasst. Die folgende Tabelle beschreibt kurz die Schaltflächen, die sich auf Anlagenmanagement beziehen.

| Name der Schaltfläche          | Beschreibung                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bearbeiten                 | Dient zum Bearbeiten der ausgewählten Anlage.                                                                                                                                         |
| Neue                  | Erstellt eine neuen Anlage.                                                                                                                                                |
| Löschen               | Löscht die ausgewählte Anlage.                                                                                                                                       |
| Anlage verschieben           | Verschiebt Anlagen in eine andere Anlagenstruktur oder an einen anderen Standort in derselben Anlagenstruktur.                                                                                         |
| Anlage ersetzen        | Ersetzt eine untergeordnete Anlage in einer Anlagenhierarchie durch eine andere Anlage.                                                                                                  |
| Anlage installieren        | Installiert eine Anlagen an einem funktionalen Standort.                                                                                                                          |
| Anlage kopieren           | Kopiert eine Anlagenhierarchie zu einer anderen Anlage.                                                                                                                          |
| Anforderungen             | Öffnen Sie die Listenseite **Aktive Anfragen**, auf der Sie ein Wartungsanfragen anzeigen können, die für die ausgewählte Anlage erstellt wurden.                                                                         |
| Ereignishistorie        | Hier wird ein Überblick über die verschiedenen Erfassungen angezeigt, die für die Anlage vorgenommen wurden.                                                                                                         |
| Anlagenstückliste            | Dient zum Anzeigen einer Liste aller Artikel (Ersatzteile und andere Artikel), die für die Anlage verwendet werden.                                                                                  |
| Arbeitsaufträge          | Öffnet die Listenseite **Aktive Arbeitsaufträge**, auf der Sie Arbeitsaufträge für die Anlage anzeigen können.                                                                                        |
| Prüfliste            | Hiermit wird eine Übersicht über die Wartungsprüflisten und Messungen angezeigt, die für die Anlage erfasst wurden.                                                                                                 |
| Wartungsausfallzeit | Dient zum Erstellen oder Anzeigen von Wartungsausfallzeiterfassungen für eine Anlage.                                                                                                       |
| Projektbuchungen | Hier können Sie alle gebuchten Transaktionen anzeigen, die Arbeitsaufträgen zugeordnet wurden, die für die Anlage erstellt wurden.                                                                                       |
| Anlagenmessungen       | Dient zum Erstellen oder Anzeigen von Anlagenmessungen für die Anlage.                                                                                                               |
| Wartungszeitplan | Öffnen Sie die Listenseite **Wartungszeitplan öffnen**, auf der Sie Wartungspläne, Wartungsanfragen und Wartungsdurchgänge anzeigen können, die der Anlage zugeordnet sind und die den Status **Erstellt** haben. |
| Anlagenstatus aktualisieren   | Dient zum Aktualisieren des Lebenszyklusstatus der Anlage. Sie können mehrere Anlagen auf der Listenseite **Alle Anlagen** auswählen und dann den Anlagenlebenszyklusstatus für alle gleichzeitig aktualisieren.              |
| Lebenszyklusstatusprotokoll  | Hiermit wird ein Protokoll geöffnet, das den Lebenszyklusstatus der ausgewählten Anlage enthält.                                                                                                                 |
| Anlagendokumente      | Dient zum Anzeigen einer Liste der Dokumente, die an eine Anlage angefügt sind. Diese Dokumente werden unter **Anlagenverwaltung** \> **Einstellungen** \> **Anlagendokumente** eingerichtet.                 |
| Attribute           | Dient zum Erstellen oder Anzeigen von Anlagenattributen.                                                                                                                             |
| Bild                | Dienst zum Auswählen eines Bilds für die Anlage.                                                                                                                                   |
| Übergeordnete Anlagen        | Hier wird die übergeordnete Anlagenhistorie für die ausgewählte Anlage angezeigt.                                                                                                                |
| Funktionale Standorte | Hier wird die Historie der funktionalen Standorte für die ausgewählte Anlage angezeigt.                                                                                                          |
| Bedingungsbewertung | Dient zum Erfassen von Bedingungsbewertungsmessungen für die Anlage.                                                                                                         |
| Fehler               | Öffnet die Listenseite **Anlagenfehler**, auf der Sie die Fehler anzeigen können, die für die Anlage erfasst wurden.                                                                                             |
| Kostensteuerung         | Vergleicht die Budgetkosten und die Istkosten für die Anlage.                                                                                                              |
| Stundenüberwachung         | Vergleicht die Planungsstunden und die effektiven Arbeitsstunden für die Anlage.                                                                                                              |
| Anlagen-KPIs           | Dient zum Berechnen und Anzeigen von Leistungskennzahlen (KPIs) für die Anlage.                                                                                              |
| Stellentypen            | Zeigt eine Übersicht der aktuellen Standardjobtypen für die Anlage an.                                                                                                            |
| Typen kritischer Werte    | Dient zum Anzeigen oder Aktualisieren von Typen kritischer Werte der Anlage.                                                                                                                              |
| Ersatzteile          | Dient zum Anzeigen einer Liste mit genehmigten und alternativen Ersatzteilen, die für die Anlage verwendet werden können.                                                                               |
| Anlage – Verbrauch    | Dient zum Drucken eines Berichts, der Verbrauchserfassungen für die Anlage anzeigt.                                                                                                |
| Anlagenfehler          | Dient zum Drucken eines Berichts, der Fehlererfassungen für die Anlage anzeigt.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]