---
title: Synchronisieren von Projektvorkalkulationen direkt aus Project Service Automation mit Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektstundenschätzungen und Projektausgabenvorkalkulationen direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 6bdf139ddd0faa7ba2c9c14b93286eff0ef757fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846002"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektvorkalkulationen direkt aus Project Service Automation mit Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektstundenschätzungen und Projektausgabenvorkalkulationen direkt aus Microsoft Dynamics 365 for Project Service Automation mit Dynamics 365 for Finance and Operations zu synchronisieren.

> [!NOTE]
> - Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Microsoft Dynamics 365 for Finance and Operations, Version 8.0 verfügbar.
> - Integration von Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher verfügbar.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlagen, die in der Datenenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektaufgaben zwischen Finance and Operations and Project Service Automation.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integrationmit Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projektstundenvorkalkulationen

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Wenn Sie auf die verfügbaren Vorlagen im Microsoft PowerApps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenkategorien von Finance and Operations zu Project Service Automation zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektstundenschätzung (PSA zu Fin und Ops)
- **Name der Aufgaben im Projekt:**

    - Transaktionsbeziehungen
    - Ausgabemkalkulation

### <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| Projekt-Aufgaben              | Integrationsentität für Projektstundenschätzungen |

### <a name="entity-flow"></a>Entitätsfluss

Projektstundenschätzungen werden in Project Service Automation verwaltet und nach Finance and Operations als Projektstundenschätzungen synchronisiert.

### <a name="prerequisites"></a>Erforderliche Komponenten

Bevor das Synchronisieren von Projektstundenschätzungen auftreten kann, müssen Sie Projektausgabenbuchungskategorien, Projektaufgaben und Projektausgabentransaktionen synchronisieren.

### <a name="power-query"></a>Powerabfrage

In der Vorlage für Projektstundenvorkalkulationen müssen Sie Microsoft Power Query für Excel verwenden, um diese Aufgaben abzuschließen:

- Legen Sie die Standardprognosemodell-Kennung fest, die verwendet wird, wenn durch die Integration neue Stundenprognosen erstellt werden.
- Filtern Sie sämtliche ressourcenspezifischen Datensätze in der Aufgabe, bei denen die Integration fehlschlagen wird, nach Stundenprognosen.
- Filtern Sie eine leere Buchungskategoriezeilen aus. Wenn diese Aufgabe nicht abgeschlossen wird, kann dies zu falschen Stundenprognosen führen.

#### <a name="set-the-default-forecast-model-id"></a>Legen Sie die Standardplanungsmodell-Kennung fest.

Wählen Sie die ID des standardmäßigen Planzahlenmodells in der Vorlage zu aktualisierenden Vorlage aus, klicken Sie auf den Pfeil **Auf Karte anzeigen** um die Zuordnung zu öffnen. Wählen Sie dann den Link **Erweiterte Abfrage und Filterung** aus.

- Wenn Sie die Vorlage für standardmäßige Projektstundenvorkalkulationen (Project Service Automation zu Finance und Operations) verwenden, wählen Sie die **Eingefügte Bedingung** in der Liste von **Übernommene Schritte** aus. Ersetzen Sie im Eintrag **Funktion** **O\_forecast** mit dem Namen der Prognosemodellkennung, die bei der Integration verwendet werden soll. Die Standardvorlage hat eine Planzahlenmodell-Kennung aus den Demodaten.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen. Wählen Sie in Power Query die Option **Bedingte Spalte hinzufügen** aus, und geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **ModelID**. Geben Sie die Bedingung für die Spalte ein. Wenn dabei die Projektaufgabe nicht null ist, geben Sie dann \<die Prognosemodellkennung ein\>; ansonsten null.

#### <a name="filter-out-resource-specific-records"></a>Ressourcenspezifische Datensätze herausfiltern

Die Vorlage für Projektstundenvorkalkulationen (PSA zu Fin and Ops) hat einen Standardfilter, der alle ressourcenspezifischen Datensätze entfernt. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus, um anhand der Spalte **msdyn\_islinetask** zu filtern, sodass nur **False**-Datensätze enthalten sind.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtern Sie eine leere Buchungskategoriezeilen aus.

Sie müssen einen Filter hinzufügen, um alle Zeilen mit leeren Transaktionskategorien zu entfernen. Diese Aufgabe ist erforderlich, unabhängig davon, ob Sie die Standardvorlage verwenden oder eine eigene Vorlage erstellen. Dieser Filter entfernt sämtliche zusammengefasste Zeilen aus Project Service Automation, die möglicherweise dafür verantwortlich sein könnten, dass die Stundenprognosen in Finance and Operations falsch sind. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus, um Null-Datensätze in der Spalte **msdyn\_transactioncategory\_value** herauszufiltern.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektausgabenvorkalkulationen

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgende Vorlage und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenvorkalkulationen von Project Service Automation mit Finance and Operations zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projektausgabenschätzung (PSA zu Fin und Ops)
- **Name der Aufgaben im Projekt:**

    - Transaktionsbeziehungen 
    - Ausgabemkalkulation

### <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Transaktionsverbindungen    | Integrationsentität für Projektbuchungsbeziehungen |
| Planungspositionen             | Integrationsentität für Projektausgabenvorkalkulationen         |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgabenschätzungen werden in Project Service Automation verwaltet und nach Finance and Operations als Projektstundenschätzungen synchronisiert.

### <a name="prerequisites"></a>Erforderliche Komponenten

Bevor das Synchronisieren von Projektausgabenvorkalkulationen erfolgen kann, müssen Sie Projekte, Projektaufgaben und Projektausgaben-Transaktionskategorien synchronisieren.

### <a name="power-query"></a>Powerabfrage

In der Vorlage für Projektausgabenvorkalkulationen müssen Sie Power Query verwenden, um die folgenden Aufgaben abzuschließen:

- Filtern Sie, damit nur Ausgabenvorkalkulations-Positionsdatensätze einbezogen werden.
- Legen Sie die Standardprognosemodell-Kennung fest, die verwendet wird, wenn durch die Integration neue Stundenprognosen erstellt werden.
- Ändern Sie die Rechnungsstellungstypen.
- Ändern Sie die Transaktionstypen.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtern, damit nur Ausgabenenvorkalkulationspositionen einbezogen werden

Die Vorlage der Projektausgabenvorkalkulationen (PSA zu Fin and Ops) hat einen Standardfilter, der nur Ausgabenpositionen in der Integration einbezieht. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen. Wählen Sie die Aufgabe **Buchungsbeziehungen** aus und klicken Sie dann auf den Pfeil **Zuordnen**, um die Zuordnung zu öffnen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus. Filtern Sie die Spalte **msdyn\_transactiontype1**, um nur **msdyn\_estimateline** einzubeziehen.

#### <a name="set-the-default-forecast-model-id"></a>Legen Sie die Standardplanungsmodell-Kennung fest.

Um die standardmäßige Prognosemodellkennung in der Vorlage zu aktualisieren, wählen Sie die Aufgabe **Ausgabenvorkalkulationen** aus, und klicken Sie dann auf den Pfeil **Zuordnen**, um die Zuordnung zu öffnen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus.

- Wenn Sie die Vorlage der standardmäßigen Projekt-Ist-Werte (PSA zu Fin and Ops) verwenden, wählen Sie in Power Query die erste **Eingefügte Bedingung** aus dem Abschnitt **Angewendete Schritte** aus. Ersetzen Sie im Eintrag **Funktion** **O\_forecast** mit dem Namen der Prognosemodellkennung, die bei der Integration verwendet werden soll. Die Standardvorlage hat eine Planzahlenmodell-Kennung aus den Demodaten.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen. Wählen Sie in Power Query die Option **Bedingte Spalte hinzufügen** aus, und geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **ModelID**. Geben Sie die Bedingung für die Spalte ein, wobei, wenn Vorkalkulationspositionskennung nicht null ist, dann \<geben Sie die Prognosemodellkennung ein\>; anderenfalls null.

#### <a name="transform-the-billing-types"></a>Ändern Sie die Rechnungsstellungstypen

Die Vorlage für Projektausgabenvorkalkulationen (PSA zu Fin und Ops) umfasst eine bedingte Spalte, mit der die Fakturierungstypen umgewandelt werden, die von Project Service Automation bei der Integration empfangen werden. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus, und wählen Sie dann **Bedingungsspalte hinzufügen** aus. Geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **BillingType**. Geben Sie dann die folgende Bedingung ein:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Ändern Sie die Transaktionstypen

Die Vorlage für Projektausgabenvorkalkulationen (PSA zu Fin und Ops) umfasst eine bedingte Spalte, mit der die Transaktionstypen umgewandelt werden, die von Project Service Automation bei der Integration empfangen werden. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus, und wählen Sie dann **Bedingungsspalte hinzufügen** aus. Geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **TransactionType**. Geben Sie dann die folgende Bedingung ein:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Vorlagenzuordnung](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
