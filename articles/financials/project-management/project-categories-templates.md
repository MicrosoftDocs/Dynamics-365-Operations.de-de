---
title: Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projektausgabenkategorien zwischen Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation zu synchronisieren.

> [!NOTE]
> - Projektaufgabenintegration, Ausgabentransaktionskategorien, Stundenvorkalkulationen, Ausgabenvorkalkulationen und Funktionalitätssperren sind in Microsoft Dynamics 365 for Finance and Operations, Version 8.0, verfügbar.
> - Integration von Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher, verfügbar.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 verwenden, nachdem Sie KB 4132657 und 4132660 KB installiert haben, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und Ist-Werte zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Datenfluss für Project Service Automation und Finance and Operations

Die Project Service Automation und Finance and Operations Integrationslösung nutzen die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlagen, die in der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektausgaben-Transaktionskategorien zwischen Finance and Operations und Project Service Automation.

Wenn die Projektausgabenkategorien in Finance and Operations erfolgreich gehandhabt werden, erfolgt der Integrationsfluss zuerst von Finance and Operations nach Project Service Automation. Die Integrationskennungen aus den Projektausgabenkategorien werden dann über Synchronisierung von Project Service Automation nach Finance and Operations synchronisiert.

Wenn die Projektausgabenkategorien in der Project Service Automation erfolgt, ist der Integrationsfluss zuerst von Project Service Automation zu Finance and Operations. Die Projektkategorien müssen in Finance and Operations bereits vor der Synchronisierung von Project Service Automation konfiguriert werden. Dann synchronisieren Sie von Finance and Operations zurück zu Project Service Automation und dann von Project Service Automation zu Finance and Operations. Auf diese Weise können Sie sicherstellen, dass die Kategorien verknüpft sind und dass keine Duplikate erstellt werden.

> [!NOTE]
> Normalerweise werden die Projektausgabenkategorien in Finance and Operations abgewickelt. Wenn sie jedoch nicht in Finance and Operations erfolgreich gehandhabt werden, oder wenn Ausgabenkategorien bereits in Project Service Automation erstellt wurden, müssen Sie zuerst mithilfe der Vorlage für Projektausgaben-Transaktionskategorien (PSA zu Fin and Ops) synchronisieren. Synchronisieren Sie dann mithilfe der Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA). Sie sollten dann die Synchronisierung von Project Service Automation nach Finance and Operations noch einmal ausführen.
>
> Wenn Sie zuerst von Project Service Automation synchronisieren, müssen die folgenden Anforderungen in Finance and Operations erfüllt sein, bevor die Synchronisierung ausgeführt wird:
>
> - Die freigegebene Kategorie, die mit der Projektkategorie übereinstimmt, die in Project Service Automation eingerichtet ist, muss vorhanden sein, und sie muss sowohl für **Projekt** als auch **Ausgaben** aktiviert sein.
> - Für jede juristische Finance and Operations-Person, mit der eine Integration hergestellt werden muss, müssen die folgenden Projektkategorien vorhanden sein:
>
>     - **Projektkategorie** ist vorhanden. 
>     - **In Ausgaben verwenden** ist aktiviert.
>     - **Aktiv in der Erfassung** ist aktiviert.
>     - **Transaktionstyp** ist auf **Ausgaben** festgelegt.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Projektausgabenkategorie-Synchronisierung von Finance and Operations nach Project Service Automation

### <a name="template-and-task"></a>Vorlage und Aufgabe

Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte** aus, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektausgabenkategorien von Finance and Operations mit Project Service Automation zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projekctausgabentransaktionskategorien (Fin and Ops zu PSA)
- **Name der Aufgabe im Projekt:** Synchronisierungskategorien zu PSA

### <a name="entity-set"></a>Entitätssatz

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrationsentität für Kategorien | Transaktionskategorien     |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.

### <a name="power-query"></a>Powerabfrage

Wenn Sie mit Project Service Automation synchronisieren, müssen Sie Microsoft Power Query für Excel nutzen, um den Fakturierungstyps für die Transaktionskategorie festzulegen. Die Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA) bietet eine Standardspalte und -zuordnung. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen. Führen Sie diese Schritte aus.

1. Klicken Sie auf den Pfeil, um die Zuordnung der Projektausgaben-Kategorieaufgabe in der Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA) zu öffnen.
2. Klicken Sie auf den Link **Erweiterte Abfrage und Filterung**, um Power Query zu öffnen.
2. Wählen Sie **Hinzufügen von bedingten Spalten** aus.
3. Geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **BillingType**.
4. Geben Sie die folgende Bedingung ein: **wenn CATEGORYID ungleich null dann 19235001, ansonsten null**.
5. Klicken Sie **OK** in der Spalte.
6. Stellen Sie sicher, dass Sie diese neue Spalte auf der Zuordnungsseite zuzuordnen.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Finance and Operations zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Projektausgabenkategorie-Synchronisierung von Project Service Automation nach Finance and Operations

### <a name="template-and-task"></a>Vorlage und Aufgabe

Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektausgabenkategorien von Project Service Automation mit Finance and Operations zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA)
- **Name der Aufgabe im Projekt:** Synchronisierungskategorien nach Finance and Operations

### <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Transaktionskategorien     | Integrationsentität für Kategorien |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgaben werden in Finance and Operations verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert. Die Rücksynchronisierung mit Finance and Operations aktualisiert die Projektkategorie in Finance and Operations mit der Integrationskennung aus Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

