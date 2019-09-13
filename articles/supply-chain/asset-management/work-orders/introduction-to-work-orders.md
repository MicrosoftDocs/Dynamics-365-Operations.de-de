---
title: Einführung in Arbeitsaufträge
description: Dieses Thema bietet einen Überblick über Arbeitsaufträge in Asset Management.
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
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875680"
---
# <a name="introduction-to-work-orders"></a>Einführung in Arbeitsaufträge

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Arbeitsaufträge werden verwendet, um Wartungsaufträge zu verwalten, erforderliche Informationen bereitzustellen und den Verbrauch zu erfassen. Ein Arbeitsauftrag kann einen oder mehrere Arbeitsaufträge enthalten, und ein oder mehrere Anlagen können mit einem Arbeitsauftrag verbunden sein. Jede Arbeitsauftragsposition definiert einen Wartungsauftrag, der für die Anlage geplant ist.

Arbeitsaufträge können entweder manuell oder auch automatisch erstellt werden.

- Automatisch mithilfe des Formulars **Wartungspläne planen**, für Kalender-basierte Wartungspläne festgelegt auf „Automatisch einrichten“.  

- Automatisch mithilfe des Formulars **Wartungsdurchgänge planen**, für Kalender-basierte Wartungsdurchgänge festgelegt auf „Automatisch einrichten“.  

- Erstellen Sie aus dem Wartungszeitplan heraus, d.h. aus vorbeugenden Wartungsaufträgen oder Wartungsanfragen.  

- Erstellen Sie Arbeitsaufträge manuell.  

- Erstellen Sie einen Arbeitsauftrag aus **Alle Wartungsanfragen** oder **Aktive Wartungsanfragen** oder **Meine Funktionaler Standort-Wartungsanfragen**.

>[!NOTE]
>Arbeitsauftragseinzelvorgänge, die sich auf dieselbe Anlage beziehen, beziehen sich auf dieselbe Projektkennung.

## <a name="all-work-orders"></a>Alle Arbeitsaufträge

Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge**, um die Liste zu öffnen. **Alle Arbeitsaufträge** enthalten eine Liste aller Arbeitsaufträge und zeigen einige der Informationen zu einem Arbeitsauftrag an.

![Abbildung 1](media/01-work-orders.png)

- Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge**, um eine Liste der aktiven Arbeitsaufträge anzuzeigen.

- Klicken Sie auf **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Meine Funktionaler Standort-Arbeitsauftragwartungsanfragen**, um eine Liste von Arbeitsaufträgen anzuzeigen, die Anlagen enthalten, die auf funktionalen Standorten installiert sind, mit denen Sie als Arbeitskraft verbunden sind (Einrichtung in [Wartungsarbeiter und Arbeitskraftgruppen](../setup-for-objects/workers-and-worker-groups.md)).

- Klicken Sie in der Liste (Rasteransicht) **Alle Arbeitsaufträge** auf einen Link in der Spalte **Arbeitsauftrag**, um die Detailansicht des ausgewählten Datensatzes anzuzeigen. Klicken Sie auf die Schaltfläche **Bearbeiten**, um ihn zur Bearbeitung zu öffnen.  

- In der Detailansicht werden detailierte Informationen angezeigt, die sich auf den Arbeitsauftrag beziehen.  

- Wählen Sie in der Detailansicht den Link **Positionen** aus, um Details zum Arbeitsauftrag anzuzeigen, oder den Link **Kopfzeile**, um Details zum Arbeitsauftrag anzuzeigen.  

- Der vertikale Bereich **Verwandte Informationen** auf der rechten Seite des Bildschirms enthält zusätzliche arbeitsauftragsbezogene Informationen. Erweitern Sie den Bereich, um die zugehörigen Informationen für den ausgewählten Arbeitsauftrag anzuzeigen.  


![Abbildung 2](media/02-work-orders.png)


Die Aktionsbereichschaltflächen sind in Registerkarten im Aktivitätsbereich organisiert. Hier finden Sie eine kurze Beschreibung der Schaltflächen zum Thema Enterprise Asset Management:



| Name der Schaltfläche                     | Beschreibung                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bearbeiten                            | Bearbeiten Sie den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                                           |
| Neue                             | Erstellen Sie einen neuen Arbeitsauftrag.                                                                                                                                                                                                                                                  |
| Löschen                          | Löschen SIe den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                                         |
| Arbeitsauftragspool                 | Fügen Sie ausgewählte Arbeitsaufträge zu einem Arbeitsauftragspool hinzu oder entfernen Sie sie aus dem Arbeitsauftragspool.                                                                                                                                                                                           |
| Anpassen                          | Passen Sie Informationen über den erwarteten Beginn und das erwartete Ende, den Servicelevel, den verantwortlichen Wartungsarbeiter oder die verantwortliche Wartungsarbeitergruppe für ausgewählte Arbeitsaufträge an.                                                                                                                                     |
| Zugehöriger Arbeitsauftrag              | Erstellen Sie einen neuen Arbeitsauftrag, der sich auf den ausgewählten Arbeitsauftragseinzelvorgang bezieht. Dies ist hilfreich, wenn Sie primäre und sekundäre Arbeitsaufträge erfassen möchten.                                                                                                                              |
| Arbeitsauftrag kopieren                 | Erstellen Sie einen neuen Arbeitsauftrag auf Basis eines vorhandenen Arbeitsauftrags.                                                                                                                                                                                                                |
| Ereignishistorie                   | Siehe Registrierungshistorie auf dem Arbeitsauftrag.                                                                                                                                                                                                                |
| Hinweise zu Wartungsarbeitsaufträgen                           | Erstellen Sie eine Beschreibung oder fügen Sie Hinweise oder Bemerkungen in einen Arbeitsauftrag ein. Klicken SIe zunächst auf die Schaltfläche **Zeitstempel hinzufügen**, um den Benutzernamen und einen Zeitstempel zum Hinweis hinzufügen. Hinweise werden im Formular **Arbeitsauftrag** > Inforegister **Positionsdetails** > Registerkarte **Beschreibung** angezeigt. |
| Extras                           | Erstellen Sie eine Liste der erforderlichen Tools in einem Arbeitsauftrag. Werkzeuge werden als Ressourcen in **Organisationsverwaltung** > **Allgemein** > **Ressourcen** > **Ressourcen** eingerichtet.                                                                                                      |
| Wartungsprüfliste           | Dient zum Anzeigen der Prüfliste für die mit dem Arbeitsauftrag verbundene Anlage.                                                                                                                                                                                                              |
| Anlagenfehler                     | Dient zum Anzeigen oder Erfassen von Fehlerinformationen zu einer Anlage, die für das Fehlermanagement verwendet werden soll.                                                                                                                                                                                        |
| Wartungsausfallzeit            | Geben Sie die Wartungsausfallzeit für einen Arbeitsauftrag an.                                                                                                                                                                                                                               |
| Bedingungsbewertung            | Registrieren Sie Bedingungsbewertungsmessungen auf einem Arbeitsauftrag.                                                                                                                                                                                                             |
| Anlagenzähler                 | Dient zum Erstellen oder Anzeigen von Zählererfassungen für eine Anlage.                                                                                                                                                                                                                     |
| Planung                        | Dient zum Anzeigen oder Erstellen von Planungen auf einem Arbeitsauftrag.                                                                                                                                                                                                                               |
| Journale                        | Dient zum Anzeigen oder Erstellen von Arbeitsauftragserfassungen. Erfassungspositionen können aus den Planungen kopiert werden.                                                                                                                                                                                         |
| Projektbuchungen            | Dient dem Anzeigen aller gebuchten Transaktionen, die sich auf Arbeitsaufträge beziehen, die für die Anlage angelegt wurden.                                                                                                                                                                                             |
| Arbeitsauftragsstatus aktualisieren                | Lebenszyklusstatus von Arbeitsaufträgen aktualisieren                                                                                                                                                                                                                                                |
| Lebenszyklusstatusprotokoll                       | Protokoll, das die Lebenszyklusstatus des ausgewählten Arbeitsauftrags anzeigt.                                                                                                                                                                                                                   |
| Anlagendokumente                | Dient dem Anzeigen einer Liste der Dokumente, die Anlagen zugeordnet sind, die sich auf einen Arbeitsauftrag beziehen. Diese Dokumente werden unter **Anlagenverwaltung** > **Einstellungen** > **Anlagendokumente**eingerichtet.                                                                                                 |
| Planung                        | Planen Sie den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                                      |
| Disponieren            | Planen Sie den ausgewählten Arbeitsauftrag für eine Arbeitskraft.                                                                                                                                                                                                                        |
| Zeitplan löschen                 | Löschen Sie die Planung für den ausgewählten Arbeitsauftrag.                                                                                                                                                                                                                          |
| Geplante Wartungsarbeitsaufträge             | Öffnen Sie die Listenseite **Geplante Wartungsaufträge für Arbeitsaufträge**.                                                                                                                                                                                                                             |
| Arbeitsauftrag – Bestellanforderung | Öffnen Sie die Listenseite **Arbeitsauftragsbestellanforderung**.                                                                                                                                                                                                                 |
| Arbeitsauftrag – Einkauf             | Öffnen Sie die Listenseite **Arbeitsauftragsbestellung**.                                                                                                                                                                                                                             |
| Kostensteuerung                    | Vergleiche Sie die Budgetkosten und die Istkosten für den Arbeitsauftrag.                                                                                                                                                                                                                |
| Stundenüberwachung                    | Vergleichen Sie die geplanten Stunden und die effektiven Stunden für den Arbeitsauftrag.                                                                                                                                                                                                                |
| Arbeitsauftragsbericht               | Drucken Sie den Arbeitsauftragsbericht.                                                                                                                                                                                                                                                |
| Arbeitsauftrag – Verbrauch          | Drucken Sie den Verbrauchsbericht.                                                                                                                                                                                                                                               |


Die Schaltflächen auf der Registerkarte **Arbeitsauftrag** > Gruppe **Projekt** beziehen sich auf die Funktionalität des Moduls **Projektmanagement und Buchhaltung** für Prognosen, Erfassungen und Fakturierung.

>[!NOTE]
>Prognosen, die auf einem Arbeitsauftrag erstellt wurden, können bei der Durchführung des Produktprogrammplanungslauf mit Hilfe des im Formular **Anlagenverwaltungsparameter** ausgewählten Prognosemodells berücksichtigt werden.

