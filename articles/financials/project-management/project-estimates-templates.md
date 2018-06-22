---
title: "Synchronisieren Sie Projektschätzungen von der Project Service Automation direkt in Finance and Operations"
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektstundenschätzungen und Projektausgaben direkt von Microsoft Dynamics 365 for Project Service Automation zu Dynamics 365 for Finance and Operations zu schätzen."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Synchronisieren Sie Projektschätzungen von der Project Service Automation direkt in Finance and Operations

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektstundenschätzungen und Projektausgaben direkt von Microsoft Dynamics 365 for Project Service Automation zu Dynamics 365 for Finance and Operations zu schätzen.

> [!NOTE]
> Projektaufgaben-Integration, Ausgabenbuchungskategorien, StundensDynamics 365 for Finance and Operations version 8.0.chätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Dynamics 365 for Finance and Operations Version 8.0 verfügbar.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die  Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlagen, die in der Datenenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektaufgaben zwischen Finance and Operations and Project Service Automation.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integrationmit Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenkategorien von Finance and Operations zu Project Service Automation zu synchronisieren:

-  **Name der Vorlage in der Datenintegration:** Projektstundenschätzung (PSA zu Fin und Ops)

-  **Name der Aufgaben im Projekt:** 
    - Transaktionsbeziehungen 
    - Ausgabemkalkulation

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Projekt-Aufgaben                   | Integrationsentität für Projektstundenschätzungen   |

## <a name="entity-flow"></a>Entitätsfluss

Projektstundenschätzungen werden in Project Service Automation verwaltet und nach Finance and Operations als Projektstundenschätzungen synchronisiert.

## <a name="preconditions"></a>Vorbedingungen

Bevor das Synchronisieren von Projektstundenschätzungen auftreten kann, müssen Sie Projektausgabenbuchungskategorien, Projektaufgaben und Projektausgabentransaktionen synchronisieren.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query in der Projektstunden-Schätzungsvorlage verwenden:
- Definieren Sie die **Planzahlenmodell-Kennung** die verwendet wird, wenn die neue Integration Stundenplanungen erstellt.
- Filtern Sie spezifische Ressourcen innerhalb der Aufgabe, die die Integration in Stundenplanungen scheitern lässt.
- Filtern Sie eine leere Buchungskategoriezeilen aus. Eine Unterlassung führt möglicherweise zu falschen Stundenplanungen.

### <a name="forecast-model-id"></a>Planzahlenmodellkennung
Wählen Sie die ID des standardmäßigen Planzahlenmodells in der Vorlage zu aktualisierenden Vorlage aus, klicken Sie auf den Pfeil **Auf Karte anzeigen** um die Zuordnung zu öffnen. Wählen Sie Erweiterter Filter- und Abfragesyntax öffnen.
- Wenn Sie Vorlage der standardmäßigen Microsoft Project-Stundenschätzungen (PSA zu Fin und Ops) verwenden, wählen Sie **Eingefügte Bedingung** im Abschnitt **Übernommene Schritte** aus. Unter **Funktion** ersetzen Sie Eingabe von **O_forecast** mit dem Namen der **Planzahlenmodell Kennung** die bei der Integration verwendet werden soll. Die Standardvorlage hat eine Planzahlenmodell-Kennung aus den Demodaten.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen. Wählen Sie **Hinzufügen von bedingten Spalten** aus und geben Sie einen Namen der Spalte, wie ModelID. Geben Sie die Bedingung für die Spalte ein, wenn Projektaufgabe, nicht Null ist, dann <enter the forecast model ID> Null einfügen.

### <a name="filter-out-resource-specific-records"></a>Filtern Sie Ressourcen spezifische Datensätze aus
Die Projekt-Stunden-Schätzungen (PSA zu Fin and Ops) Vorlage hat einen Standardfilter, der alle Ressourcen spezifischen Datensätze entfernt. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen. In der erweiterten Abfragen- und Filterungsform wählen Sie den Filter aus der Spalte**msdyn_islinetask**, um nur Datensätze **Falsch** einzubeziehen.

### <a name="filter-out-empty-transaction-category-rows"></a>Filtern Sie eine leere Buchungskategoriezeilen aus.
Sie müssen einen Filter hinzufügen, um alle Zeilen mit leeren Buchungskategorien zu entfernen. Dies ist erforderlich, unabhängig davon, ob Sie die Standardvorlage verwenden oder eine eigene Vorlage erstellen. Dieser Filter entfernt zusammengefasste Zeilen, die von der Project Service Automation kommen, die dafür verantwortlich sein könnten, dass die geplanten Stunden in Finance and Operations falsch sind. Wählen Sie in der erweiterten Abfragen und Filterungsform die Option aus, um ungültige Datensätze in der Spalte **msdyn_transactioncategory_value** zu finden.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenplanungen von Project Service Automation zu Finance and Operations zu synchronisieren.

-  **Name der Vorlage in der Datenintegration:** Projektausgabenschätzung (PSA zu Fin und Ops)
-  **Name der Aufgaben im Projekt:** 
     - Transaktionsbeziehungen 
     - Ausgabemkalkulation

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Transaktionsverbindungen         | Integrationsentität für Projektbuchungsbeziehungen.   |
| Planungspositionen                  | Integrationsentität für Projektausgabenvorkalkulationen.           |

## <a name="entity-flow"></a>Entitätsfluss

Projektausgabenschätzungen werden in Project Service Automation verwaltet und nach Finance and Operations als Projektstundenschätzungen synchronisiert.

## <a name="prerequisites"></a>Erforderliche Komponenten

Bevor das Synchronisieren von Projektstundenschätzungen auftreten kann, müssen Sie Projektausgabenbuchungskategorien, Projektaufgaben und Projektausgabentransaktionen synchronisieren.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query in der Projektstunden-Schätzungsvorlage verwenden:
- Filtern, damit nur Ausgabenenvorkalkulationspositionsdatensätze einbezogen werden
- Definieren Sie die **Planzahlenmodell-Kennung** die verwendet wird, wenn die neue Integration Stundenplanungen erstellt.
- Ändern Sie die Rechnungsstellungstypen.
- Ändern Sie die Transaktionstypen.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtern, damit nur Ausgabenenvorkalkulationspositionen einbezogen werden
Die Vorlage der Projektausgabenschätzungen-Vorlage (PSA zu Fin und Ops) hat einen Standardfilter, um nur Ausgabenpositionen in der Integration einzubeziehen. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen. Wählen Sie die Buchungsbeziehungsaufgabe aus und klicken Sie auf den Pfeil **Auf Karte anzeigen** Wählen Sie **Erweiterter Filter- und Abfragesyntax** Filtert die Spalte **msdyn_transactiontype1**, um nur **msdyn_estimateline** einzubeziehen.

### <a name="forecast-model-id"></a>Planzahlenmodellkennung
Wählen Sie die standardmäßige Planzahlenmodells-ID in der Vorlage für die Ausgabenschätzungsaufgabe und klicken Sie auf **Auf Karte anzeigen** um die Zuordnung zu öffnen. Wählen Sie Erweiterter Filter- und Abfragesyntax öffnen.
- Wenn Sie die Vorlage für standardmäßige Microsoft Project-Ausgabenschätzungen (PSA zu Fin und Ops) verwenden, wählen Sie **Eingefügte Bedingung** im Abschnitt **Übernommene Schritte** aus. Unter **Funktion** ersetzen Sie Eingabe von **O_forecast** mit dem Namen der **Planzahlenmodell Kennung** die bei der Integration verwendet werden soll. Die Standardvorlage hat eine Planzahlenmodell-Kennung aus den Demodaten.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen. Wählen Sie **Hinzufügen von bedingten Spalten** aus und geben Sie einen Namen der Spalte, wie ModelID. Geben Sie die Bedingung für die Spalte ein, wenn Vorkalkulationsposition Kennung nicht ungültig ist, dann < geben Sie die Kennung > Planzahlenmodell ein; NULL einfügen.

### <a name="transform-the-billing-types"></a>Ändern Sie die Rechnungsstellungstypen
Die Projektausgabenschätzung (PSA zu Fin und Ops) hat eine bedingte Spalte hinzugefügt, um die Rechnungsstellungstypen umzuwandeln, die von der Project Service Automation bei der Integration empfangen werden.
- Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen. Wählen Sie in der erweiterten Abfragen und Filterungsform **Hinzufügen von bedingten Spalten**. Geben Sie der neuen Spalte einen Namen, wie "Rechnungstyp". Der einzugebenden Bedingungen sind wie folgt:

    Wenn **msdyn_billingtype** = 192350000, dann **Nicht fakturierbar** sonst wenn **msdyn_billingtype** = 192350001, dann **Fakturierbar** sonst wenn **msdyn_billingtype** = 192350002, dann **Höflich** **NotAvailable** einfügen

### <a name="transform-the-transaction-types"></a>Ändern Sie die Transaktionstypen
Die Projektausgabenschätzung (PSA zu Fin und Ops) hat eine bedingte Spalte hinzugefügt, um die Rechnungsstellungstypen umzuwandeln, die von der Project Service Automation bei der Integration empfangen werden.
- Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen. Wählen Sie in der erweiterten Abfragen und Filterungsform **Hinzufügen von bedingten Spalten**. Geben Sie der neuen Spalte einen Namen, wie "Transaktionstyp" ein. Die Bedingung Einzugebende ist, wie folgt: Wenn **msdyn_transactiontypecode** = 192350000, dann **Kosten** sonst wenn **msdyn_transactiontypecode** = 192350005, dann **Verkäufe** **NULL** einfügen

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Vorlagenzuordnung](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




