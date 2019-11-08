---
title: Einführung in Arbeitsaufträge
description: Dieses Thema bietet einen Überblick über Arbeitsaufträge in Asset Management.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b8340d3f4fd98e02e372fd5ac68f1ae107819304
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626407"
---
# <a name="introduction-to-work-orders"></a>Einführung in Arbeitsaufträge

[!include [banner](../../includes/banner.md)]



Arbeitsaufträge werden verwendet, um Wartungsaufträge zu verwalten, erforderliche Informationen bereitzustellen und den Verbrauch zu erfassen. Jeder Arbeitsauftrag kann einen oder mehrere Arbeitsaufträge enthalten, und ein oder mehrere Anlagen können mit einem Arbeitsauftrag verbunden sein. Jeder Arbeitsauftragseinzelvorgang definiert einen Wartungsauftrag, der für die Anlage geplant ist.

Arbeitsaufträge können folgendermaßen erstellt werden:

- Für kalenderbasierte Wartungspläne, bei denen die Einstellung „Automatisch einrichten“ aktiviert ist, automatisch mit Hilfe von [Wartungspläne planen](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md).

- Für Wartungsdurchgänge, bei denen die Einstellung „Automatisch einrichten“ aktiviert ist, automatisch mit Hilfe von [Wartungsdurchgänge planen](../preventive-and-reactive-maintenance/maintenance-rounds.md).

- Für vorbeugende Wartungsaufträge oder Wartungsanfragen, über [Wartungszeitplan](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Manuell

- Über die Seite **Alle Wartungsanfragen**, **Aktive Wartungsanfragen** oder **Meine Wartungsanfragen für funktionale Standorte**.

>[!NOTE]
>Arbeitsauftragseinzelvorgänge, die sich auf dieselbe Anlage beziehen, beziehen sich auf dieselbe Projektkennung.

## <a name="all-work-orders"></a>Alle Arbeitsaufträge

Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** aus, um die Listenseite **Alle Arbeitsaufträge** zu öffnen. Auf dieser Seite werden alle Arbeitsaufträge und einige der Informationen angezeigt, die sich auf die einzelnen Arbeitsaufträge beziehen.

In der folgenden Abbildung wird ein Beispiel der Listenseite **Alle Arbeitsaufträge** angezeigt.

![Abbildung 1](media/01-work-orders.png)

Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Aktive Arbeitsaufträge** aus, um eine Liste von nur aktiven Arbeitsaufträgen anzuzeigen. 

Um eine Liste von Arbeitsauftragseinzelvorgängen anzuzeigen, die Anlagen enthalten, die auf funktionalen Standorten installiert sind, mit denen Sie als Arbeitskraft verbunden sind, wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Meine Funktionaler Standort-Wartungsaufträge für Arbeitsaufträge** aus. (Die Beziehung zwischen Arbeitskräften und funktionalen Standorten wird auf der Seite **Arbeitskräfte** eingerichtet. Weitere Informationen finden Sie unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).)

Nachfolgend einige Möglichkeiten, wie Sie die Seite **Alle Arbeitsaufträge** verwenden können:

- Wählen Sie in der Rasteransicht eine Verknüpfung in der Spalte **Arbeitsauftrag** aus, um die Detailansicht für den ausgewählten Datensatz anzuzeigen. Sie können dann **Bearbeiten** auswählen, um den Datensatz zum Bearbeiten zu öffnen.

- In der Detailansicht werden detaillierte Informationen angezeigt, die sich auf den Arbeitsauftrag beziehen.  

- Wählen Sie in der Detailansicht die Registerkarte **Positionen** aus, um Details zum Arbeitsauftragseinzelvorgang anzuzeigen, oder die Registerkarte **Kopfzeile**, um Details zum Arbeitsauftrag anzuzeigen.  

- Erweitern Sie den Bereich **Zugehörige Informationen** auf der rechten Seite der Seite, um zusätzliche Informationen anzuzeigen, die dem ausgewählten Arbeitsauftrag zugeordnet sind.

In der folgenden Abbildung wird ein Beispiel der Detailansicht **Alle Arbeitsaufträge** angezeigt.

![Abbildung 2](media/02-work-orders.png)


Die Schaltflächen im Aktivitätsbereich sind auf Registerkarten zusammengefasst. Die folgende Tabelle beschreibt kurz die Schaltflächen, die sich auf Anlagenmanagement beziehen:



| Name der Schaltfläche                     | Beschreibung                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bearbeiten                            | Bearbeiten Sie den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                                           |
| Neue                             | Erstellen Sie einen neuen Arbeitsauftrag.                                                                                                                                                                                                                                                  |
| Löschen                          | Löschen SIe den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                                         |
| Arbeitsauftragspool                 | Fügen Sie den ausgewählten Arbeitsauftrag zu einem Arbeitsauftragspool hinzu oder entfernen Sie ihn aus dem Arbeitsauftragspool.                                                                                                                                                                                           |
| Anpassen                          | Passen Sie Informationen über den erwarteten Beginn und das erwartete Ende, den Servicelevel, den verantwortlichen Wartungsarbeiter oder die verantwortliche Wartungsarbeitergruppe für ausgewählte Arbeitsaufträge an.                                                                                                                                     |
| Zugehöriger Arbeitsauftrag              | Erstellen Sie einen neuen Arbeitsauftrag, der sich auf den ausgewählten Arbeitsauftragseinzelvorgang bezieht. Dies ist hilfreich, wenn Sie primäre und sekundäre Arbeitsaufträge erfassen möchten.                                                                                                                              |
| Arbeitsauftrag kopieren                 | Erstellen Sie einen neuen Arbeitsauftrag auf Basis eines vorhandenen Arbeitsauftrags.                                                                                                                                                                                                               |
| Ereignishistorie                   | Zeigen Sie die Erfassungshistorie für den Arbeitsauftrag an.                                                                                                                                                                                                                |
| Hinweise zu Wartungsarbeitsaufträgen                           | Erstellen Sie eine Beschreibung für einen Arbeitsauftrag oder fügen Sie Hinweise oder Bemerkungen dazu hinzu. Wählen Sie zunächst **Zeitstempel hinzufügen** aus, um den Benutzernamen und einen Zeitstempel zum Hinweis hinzufügen. Hinweise werden auf der Registerkarte **Beschreibung** auf dem Inforegister **Positionsdetails** auf der Seite **Arbeitsauftrag** angezeigt.         |
| Extras                           | Erstellen Sie eine Liste der erforderlichen Tools in einem Arbeitsauftrag. Werkzeuge werden als Ressourcen in **Organisationsverwaltung** > **Ressourcen** > **Ressourcen** eingerichtet.                                                                                                      |
| Wartungsprüfliste           | Zeigen Sie die Prüfliste für die mit dem Arbeitsauftrag verbundene Anlage an.                                                                                                                                                                                                              |
| Anlagenfehler                     | Zeigen Sie Fehlerinformationen zu einer Anlage an oder erfassen Sie sie. Diese Informationen werden für das Fehlermanagement verwendet.                                                                                                                                                                                      |
| Wartungsausfallzeit            | Geben Sie die Wartungsausfallzeit für einen Arbeitsauftrag an.                                                                                                                                                                                                                               |
| Bedingungsbewertung            | Registrieren Sie Bedingungsbewertungsmessungen auf einem Arbeitsauftrag.                                                                                                                                                                                                             |
| Anlagenzähler                 | Dient zum Erstellen oder Anzeigen von Zählererfassungen für eine Anlage.                                                                                                                                                                                                                     |
| Planung                        | Dient zum Anzeigen oder Erstellen von Planungen auf einem Arbeitsauftrag.                                                                                                                                                                                                                               |
| Journale                        | Dient zum Anzeigen oder Erstellen von Arbeitsauftragserfassungen. Erfassungspositionen können aus den Planungen kopiert werden.                                                                                                                                                                                         |
| Projektbuchungen            | Zeigen Sie alle gebuchten Transaktionen an, die sich auf Arbeitsaufträge beziehen, die für die Anlage angelegt wurden.                                                                                                                                                                                             |
| Arbeitsauftragsstatus aktualisieren           | Aktualisieren Sie den Lebenszyklusstatus von Arbeitsaufträgen.                                                                                                                                                                                                                                                |
| Lebenszyklusstatusprotokoll                      | Hiermit wird ein Protokoll angezeigt, das den Lebenszyklusstatus des ausgewählten Arbeitsauftrags enthält.                                                                                                                                                                                                                   |
| Anlagendokumente                | Dient dem Anzeigen einer Liste der Dokumente, die Anlagen zugeordnet sind, die sich auf einen Arbeitsauftrag beziehen. Diese Dokumente werden unter **Anlagenverwaltung** > **Einstellungen** > **Anlagendokumente**eingerichtet.                                                                                                 |
| Planung                        | Planen Sie den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                                      |
| Disponieren            | Planen Sie den ausgewählten Arbeitsauftrag für eine Arbeitskraft.                                                                                                                                                                                                                        |
| Zeitplan löschen                 | Löschen Sie die Planung für den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                          |
| Geplante Wartungsarbeitsaufträge             | Öffnen Sie die Listenseite **Geplante Wartungsaufträge für Arbeitsaufträge**.                                                                                                                                                                                                                             |
| Arbeitsauftrag – Bestellanforderung | Öffnen Sie die Listenseite **Arbeitsauftragsbestellanforderung**.                                                                                                                                                                                                                 |
| Arbeitsauftrag – Einkauf             | Öffnen Sie die Listenseite **Arbeitsauftragsbestellung**.                                                                                                                                                                                                                             |
| Kostensteuerung                    | Vergleiche Sie die Budgetkosten und die Istkosten für den Arbeitsauftrag.                                                                                                                                                                                                                |
| Stundenüberwachung                    | Vergleichen Sie die geplanten Stunden und die effektiven Stunden für den Arbeitsauftrag.                                                                                                                                                                                                                |
| Arbeitsauftragsbericht               | Drucken Sie einen Arbeitsauftragsbericht.                                                                                                                                                                                                                                                |
| Arbeitsauftrag – Verbrauch          | Drucken Sie einen Verbrauchsbericht.                                                                                                                                                                                                                                               |


Die Schaltflächen in der Gruppe **Projekt** auf der Registerkarte **Arbeitsauftrag** vom Aktivitätsbereich beziehen sich auf die Funktionalität für Prognosen, Erfassungen und Fakturierung im Modul **Projektverwaltung und Buchhaltung**.

>[!NOTE]
>Prognosen, die auf einem Arbeitsauftrag erstellt wurden, können bei der Ausführung des Produktprogrammplanungslaufs mit Hilfe des auf der Seite **Anlagenverwaltungsparameter** ausgewählten Prognosemodells berücksichtigt werden.

