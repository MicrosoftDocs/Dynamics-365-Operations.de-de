---
title: Einrichten eines Lagerorts mithilfe einer Lagerortkonfigurationsvorlage
description: "In diesem Thema wird erklärt, wie ein Lagerort mithilfe einer Lagerortkonfigurationsvorlage eingerichtet wird."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: 9e0c61505a8af864d7ff38655e7e896c4f6ccb65
ms.contentlocale: de-de
ms.lasthandoff: 02/06/2018

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Einrichten eines Lagerorts mithilfe einer Lagerortkonfigurationsvorlage

[!INCLUDE [banner](../includes/banner.md)]

In diesem Thema wird erklärt, wie ein Lagerort mithilfe einer Lagerortkonfigurationsvorlage eingerichtet wird. Es gibt mehrere vordefinierte Konfigurationsvorlagen, die Sie verwenden können. Informationen darüber, wie diese Vorlagen verwendet werden, finden Sie unter [Konfigurationsdatenvorlagen](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Szenarien, bei denen Konfigurationsvorlagen hilfreich sein können

Konfigurationsvorlagen können in vielen Szenarien hilfreich sein. Nachfolgend finden Sie einige Beispiele:

- Sie haben eine Konfigurationseinstellung in einer Testumgebung abgeschlossen und getestet, und Sie möchten jetzt das Setup in eine Produktionsumgebung kopieren.
- Sie möchten das Lagerortsetup für mehrere juristische Personen anwenden oder einen neuen Lagerort in derselben juristischen Person erstellen.
- Sie möchten sich schnell auf eine Vorführung der Lagerortfunktionalität vorbereiten.
- Sie möchten, dass vorhandene Artikel und Lagerorte die Funktionalität in der Lagerortverwaltung anstatt der Funktionalität in der Lagerverwaltung verwenden.

Dieses Thema konzentriert sich auf das erste dieser Szenarien. Es wird gezeigt, wie Sie mithilfe einer Konfigurationsvorlage eine Konfigurationseinstellung von einer Testumgebung in eine Produktionsumgebung kopieren können.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Kopieren einer Konfigurationseinstellung von einer Testumgebung zu einer Produktionsumgebung

Für dieses Szenario sind die Konfigurationseinstellung für einen Lagerort und einige Buchungsprozesse bereits in einer Testumgebung vorhanden. Sie möchten jetzt die Konfigurationseinstellung für den Lagerort aus der Testumgebung in eine Produktionsumgebung kopieren.

> [!NOTE]
> Es ist wichtig, dass Sie die anderen zugehörigen Einstellungsdaten einschließen, wenn Sie eine Konfigurationseinstellung kopieren. Sie möchten beispielsweise Produkte einrichten, indem Sie die Einstellungen aus einer Testumgebung kopieren. Sie können jedoch keinen festen Entnahmeort für das Produkt einrichten, bevor Produkt erstellt ist. Obwohl einzelne Konfigurationsvorlagen nicht diesen Typ der Abhängigkeit unterstützen, gibt es Standarddatenvorlagen, die ihn unterstützen. Sie können diese Standarddatvorlagen leicht in einen Konfigurationsprozess einbeziehen.

### <a name="export-a-default-warehouse-template"></a>Eine Standardlagerortvorlage exportieren 

1. Öffnen Sie den Arbeitsbereich **Datenverwaltung**.

    > [!NOTE]
    > Wenn Sie diesen Arbeitsbereich zum ersten Mal verwenden, müssen Sie alle Datenentitäten laden, bevor Sie fortfahren.

2. Wählen Sie die die Kachel **Vorlagen** aus, und wählen Sie dann **Standardvorlagen laden** aus, um die Standardvorlagen zu laden.

    > [!NOTE]
    > **Standardvorlagen laden** ist nur in der Ansicht **Erweitert** verfügbar. Wählen Sie **Frameworkparameter** aus, und dann im Feld **Ansichtsstandards** wählen Sie **Erweiterte Ansicht** aus.

3. Nachdem die Standardvorlagen geladen sind, können Sie sie ändern, sodass diese Ihren geschäftlichen Anforderungen entsprechen.

    > [!NOTE]
    > Um Standardvorlagen zu laden Vorlagen zu importieren, müssen Sie Systemadministratorzugriff haben. Durch diese Anforderung wird sichergestellt, dass alle Entitäten ordnungsgemäß in die Vorlage geladen werden.

4. Stellen Sie sicher, dass Sie sich in der juristischen Person befinden, aus der Sie die unternehmensspezifischen Daten exportieren möchten.
5. Wählen Sie im Arbeitsbereich **Exportieren** aus.
6. Erstellen Sie ein neues Exportprojekt.
7. Wählen Sie **+ Vorlage hinzufügen** aus, und suchen Sie die Standardlagerortvorlage **400 - WMS** aus. Durch diese Vorlage werden Datenentitäten für die Lagerortkonfiguration hinzugefügt.

    > [!NOTE]
    > Wenn die Daten, die Sie exportieren, gefiltert werden müssen (z. B. wenn Sie nur die Daten exportieren möchten, die einem bestimmten Lagerort zugeordnet sind), müssen Sie jede Datenentität auswerten und Filterung über eine Abfrage hinzufügen. Als Alternative können Sie alle Daten exportieren und dann die Datensätze löschen, die nicht in den Zieldateien erforderlich sind.

8. Wählen Sie **Exportieren**. Daten, die allen Datenentitäten im Projekt zugeordnet sind, werden exportiert.

Sie können eine ZIP-Datei für das Datenpaket herunterladen. Diese Datei beinhaltet alle Daten im ausgewählten Format (beispielsweise Excel-Format). Wie angegeben wurde, müssen möglicherweise einige Datensätze in den Datenpaketdateien aktualisiert werden, bevor Sie sie in die Produktionsumgebung importieren können. Wenn Sie einen Datensatz aktualisieren, stellen Sie sicher, dass Sie den Dateinamen nicht ändern.

### <a name="import-a-warehouse-configuration-setup"></a>Eine Lagerortkonfigurationseinstellung importieren

1. Stellen Sie in der Zielumgebung sicher, dass Sie sich im Unternehmen befinden, zu dem Sie die Lagerortdaten importieren möchten.

    > [!NOTE]
    > Bevor Sie den Import vornehmen, sollten Sie sämtliche Datenenabhängigkeiten identifizieren. Beispielsweise beinhaltet die Vorlage **Lagerortverwaltung** eine Datenentität, die die Bezeichnung **Lagerortdispositionscodes** hat. Diese Entität enthält Daten, die der Seite Einstellungsseite **Dispositionscodes** (**Lagerortverwaltung** > **Einstellungen** > **Mobiles Gerät** > **Dispositionscodes**) zugeordnet sind. Wenn vorhandene Einstellungen bereits den Rückgabeprozess für Aufträge behandeln, enthält das Feld **Rückgabedispositionscode** einen Wert. Der Dispositionscode in diesem Feld ist der Datenentität **Dispositionscode** zugeordnet, die Teil der Vorlage **Vertrieb und Marketing** ist. Wenn die Daten aus der Datenentität **Dispositionscode** nicht vor den Daten aus dem Feld **Lagerortdispositionscodes** importiert werden, schlägt der Import fehl.

2. Im Arbeitsbereich **Datenverwaltung** wählen Sie **Importieren** aus.
3. Erstellen Sie ein neues Importprojekt.
4. Wählen Sie **+ Datei hinzufügen** aus, und laden Sie die ZIP-Datei für das Datenpaket hoch.
5. **Import** auswählen In der Ansicht **Erweitert** können Sie die Option **Filter** verwenden, um schnell eine Übersicht über Probleme abzurufen, die möglicherweise beim Import auftreten.

Das Protokoll **Ansichtsausführung** enthält detaillierte Informationen zu jeder Datenentität, die importiert wird. Sie können die Stagingdatenansicht verwenden, um schnell zu den Zieldaten zu gelangen. Auf diese Weise können Sie sehen, wie die importierten Daten auf den zugeordneten Seiten in der Anwendung aussehen. Wenn Sie die Standarddatenvorlagen verwenden, funktioniert die Importsequenz für jede Datenentität in der vordefinierten Weise, um sicherzustellen, dass alle abhängigen Daten zuerst importiert werden. Wenn benutzerdefinierte Datenentitäten Teil des Projekts sind, müssen Sie sicherstellen, dass die korrekte Reihenfolge definiert wird. Weitere Informationen finden Sie unter [Konfigurieren von Datenvorlagen](../../dev-itpro/data-entities/configuration-data-templates.md).

Weitere Informationen zum Ändern der Lagerortvorlage, um die Konfiguration eines Lagerorts aus einem Unternehmen in ein neues Unternehmen in der gleichen Instanz zu kopieren, sehen Sie sich dieses 3-minütige YouTube Video an.

> [!Video https://www.youtube.com/embed/K2WIfFlqJYs]


## <a name="related-topic"></a>Verwandtes Thema

[Konfigurationsdatenvorlagen](../../dev-itpro/data-entities/configuration-data-templates.md)

