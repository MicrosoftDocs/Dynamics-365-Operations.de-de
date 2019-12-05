---
title: Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projektausgabenkategorien zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation zu synchronisieren.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770311"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronisieren Sie Projektausgabenkategorien zwischen Finance and Operations and Project Service Automation

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projektausgabenkategorien zwischen Dynamics 365 Finance und Dynamics 365 Project Service Automation zu synchronisieren.

> [!NOTE]
> - Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Version 8.0 verfügbar.
> - Integration von Ist-Werten ist in Version 8.0.1 oder höher verfügbar.
> - Wenn Sie Enterprise Edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Datenfluss für Project Service Automation und Finance

Die Project Service Automation und Finance-Integrationslösung nutzen die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance zu synchronisieren. Die Integrationsvorlagen, die in der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss zu Projektausgaben-Transaktionskategorien zwischen Finance und Project Service Automation.

Wenn die Projektausgabenkategorien in Finance erfolgreich gehandhabt werden, erfolgt der Integrationsfluss zuerst von Finance nach Project Service Automation. Die Integrationskennungen aus den Projektausgabenkategorien werden dann über Synchronisierung von Project Service Automation nach Finance synchronisiert.

Wenn die Projektausgabenkategorien in der Project Service Automation erfolgt, ist der Integrationsfluss zuerst von Project Service Automation zu Finance. Die Projektkategorien müssen in Finance bereits vor der Synchronisierung von Project Service Automation konfiguriert werden. Dann synchronisieren Sie von Finance zurück zu Project Service Automation und dann von Project Service Automation zu Finance. Auf diese Weise können Sie sicherstellen, dass die Kategorien verknüpft sind und dass keine Duplikate erstellt werden.

> [!NOTE]
> Normalerweise werden die Projektausgabenkategorien in Finance abgewickelt. Wenn dies nicht der Fall ist oder wenn Ausgabenkategorien bereits in Project Service Automation erstellt wurden, müssen Sie zuerst mithilfe der Vorlage für Projektausgaben-Transaktionskategorien (PSA zu Fin and Ops) synchronisieren. Synchronisieren Sie dann mithilfe der Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA). Sie sollten dann die Synchronisierung von Project Service Automation nach Finance noch einmal ausführen.
>
> Wenn Sie zuerst von Project Service Automation synchronisieren, müssen die folgenden Anforderungen in Finance erfüllt sein, bevor die Synchronisierung ausgeführt wird:
>
> - Die freigegebene Kategorie, die mit der Projektkategorie übereinstimmt, die in Project Service Automation eingerichtet ist, muss vorhanden sein, und sie muss sowohl für **Projekt** als auch **Ausgaben** aktiviert sein.
> - Für jede juristische Finance-Person, mit der eine Integration hergestellt werden muss, müssen die folgenden Projektkategorien vorhanden sein:
>
>     - **Projektkategorie** ist vorhanden. 
>     - **In Ausgaben verwenden** ist aktiviert.
>     - **Aktiv in der Erfassung** ist aktiviert.
>     - **Transaktionstyp** ist auf **Ausgaben** festgelegt.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projektausgabenkategorie-Synchronisierung von Finance nach Project Service Automation

### <a name="template-and-task"></a>Vorlage und Aufgabe

Wenn Sie auf die Vorlage im Microsoft Power Apps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegende Aufgabe werden verwendet, um Projektausgabenkategorien von Finance zu Project Service Automation zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projekctausgabentransaktionskategorien (Fin and Ops zu PSA)
- **Name der Aufgabe im Projekt:** Synchronisierungskategorien zu PSA

### <a name="entity-set"></a>Entitätssatz

| Finanzen                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrationsentität für Kategorien | Transaktionskategorien     |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgaben werden in Finance verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert.

### <a name="power-query"></a>Powerabfrage

Wenn Sie mit Project Service Automation synchronisieren, müssen Sie Microsoft Power Query für Excel nutzen, um den Fakturierungstyps für die Transaktionskategorie festzulegen. Die Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA) bietet eine Standardspalte und -zuordnung. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie eine bedingte Spalte in der Power-Abfrage hinzufügen. Führen Sie diese Schritte aus.

1. Klicken Sie auf den Pfeil, um die Zuordnung der Projektausgaben-Kategorieaufgabe in der Vorlage für Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA) zu öffnen.
2. Klicken Sie auf den Link **Erweiterte Abfrage und Filterung**, um Power Query zu öffnen.
2. Wählen Sie **Hinzufügen von bedingten Spalten** aus.
3. Geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **BillingType**.
4. Geben Sie die folgende Bedingung ein: **wenn CATEGORYID ungleich null dann 19235001, ansonsten null**.
5. Klicken Sie **OK** in der Spalte.
6. Stellen Sie sicher, dass Sie diese neue Spalte auf der Zuordnungsseite zuzuordnen.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Finance zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projektausgabenkategorie-Synchronisierung von Project Service Automation zu Finance

### <a name="template-and-task"></a>Vorlage und Aufgabe

Die folgenden Vorlagen und zugrunde liegende Aufgabe werden verwendet, um Projektausgabenkategorien von Project Service Automation zu Finance zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektausgaben-Transaktionskategorien (Fin and Ops zu PSA)
- **Name der Aufgabe im Projekt:** Synchronisierungskategorien nach Finance and Operations

### <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finanzen                           |
|----------------------------|-----------------------------------|
| Transaktionskategorien     | Integrationsentität für Kategorien |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgaben werden in Finance verwaltet und dann zu Project Service Automation als Transaktionskategorien synchronisiert. Die Rücksynchronisierung mit Finance aktualisiert die Projektkategorie in Finance mit der Integrationskennung aus Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator.

> [!NOTE]
> Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
