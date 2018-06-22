---
title: Synchronisieren Sie Ausgabenkategorien von Project Service Automation
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Dynamics 365 for Project Service Automation zu synchronisieren."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Dynamics 365 for Project Service Automation zu synchronisieren.

> [!NOTE]
> Projektaufgaben-Integration, Ausgabenbuchungskategorien, StundensDynamics 365 for Finance and Operations version 8.0.chätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Dynamics 365 for Finance and Operations Version 8.0 verfügbar.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Datenfluss für Project Service Automation und Finance and Operations

Die Project Service Automation und Finance and Operations Integrationslösung nutzen die  Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlagen, die in der Datenenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektaufgaben zwischen Finance and Operations and Project Service Automation.

Wenn die Projektausgabenkategorien im Bereich Finance and Operations verwaltet werden, erfolgt der Integrationsfluss zuerst von Finance and Operations zu Project Service Automation und aktualisiert dann Projektausgabenkategorien-Integrations-IDs durch Synchronisierung von Project Service Automation zu Finance and Operations.

Wenn die Projektausgabenkategorien in der Project Service Automation erfolgt, ist der Integrationsfluss zuerst von Project Service Automation zu Finance and Operations. Die Projektkategorien müssen im Bereich Finance and Operations vor der Synchronisierung mit Project Service Automation konfiguriert werden. Dann synchronisieren Sie von Finance and Operations zurück zur Project Service Automation und dann von Project Service Automation zu Finance and Operations. Dadurch wird sichergestellt, dass die Kategorien verknüpft werden und keine Duplikate erstellt werden.

> [!NOTE]
> Normalerweise werden die Projektausgabenkategorien in Finance and Operations abgewickelt. Wenn das nicht Ihrer Situation entspricht oder Sie bereits Ausgabenkategorien in Project Service Automation erstellt haben, müssen Sie zuerst die Projektausgabenbuchungskategorien (PSA zu Fin und Ops) synchronisieren und dann Projektausgabentransaktions-Kategorien (Fin und Ops zu PSA) synchronisieren. Sie sollten dann die Synchronisierung von PSA zu Fin und Ops noch einmal ausführen.

> Wenn Sie zuerst von Project Service Automation synchronisieren, müssen die Projektkategorien zuerst in Finance and Operations eingerichtet werden und sämtliche Projektkategorien, die mit Project Service Automation Transaktionskategorien synchronisiert werden müssen, müssen eingerichtet werden, um **Aktiv in Erfassungen** zu sein.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenkategorien von Finance and Operations zu Project Service Automation zu synchronisieren:

-  **Name der Vorlage in der Datenintegration:** Projekctausgabentransaktionskategorien (Fin and Ops zu PSA)
-  **Name der Aufgabe im Projekt:** Synchronisierungskategorien zu PSA

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Integrationsentität für Kategorien    | Transaktionskategorien        |

## <a name="entity-flow"></a>Entitätsfluss

Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.

## <a name="power-query"></a>Powerabfrage

Sie müssen icrosoft Power Query nutzen, um den Fakturierungstyps auf der Transaktionskategorie festzulegen, wenn Sie mit Project Service Automation synchronisieren. Die Project Ausgabentransaktionskategorie (Fin und Ops zu PSA) Vorlage hat eine Standardspalte und die Zuordnung ist bereits festgelegt. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen.
- Öffnen Sie die Vorabfragen- und Filterungsformulare in der Zuordnung der Projektausgabenkategorieaufgabe.
- Wählen Sie **Hinzufügen von bedingten Spalten** aus.
- Geben Sie der neuen Spalte einen Namen, wie BillingType.
- Geben Sie die folgende Bedingung ein: wenn **CATEGORYID Ungleich null dann 19235001, ansonsten NULL**.
- Klicken Sie **OK** in der Spalte.
- Stellen Sie sicher, dass Sie diese neue Spalte der Zuordnungsseite zuzuordnen.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Finance and Operations zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektausgabenkategorien von Project Service Automation zu Finance and Operations zu synchronisieren.

-**Bezeichnung der Vorlage in der Datenintegration:** Projektausgabentransaktion (PSA zu Fin and Ops) - **Name der Aufgabe im Projekt** Synchronisation der Kategorien zu Fin Ops

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Transaktionskategorien          | Integrationsentität für Kategorien  | 

## <a name="entity-flow"></a>Entitätsfluss

Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert. Die Rücksynchronisierung zu Finance and Operations aktualisiert die Integrations-ID von Project Service Automation auf der Finance and Operations Projektkategorie.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

