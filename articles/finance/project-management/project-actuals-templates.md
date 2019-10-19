---
title: Synchronisieren von Projekt-Ist-Werten direkt aus Project Service Automation mit der Projektintegrationserfassung für die Buchung in Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte und Istwerte direkt aus Microsoft Dynamics 365 Project Service Automation zu Finance and Operations zu synchronisieren.
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
ms.openlocfilehash: 0aeaa1ee4c35ca42a5382b3c7ff3519cba52996c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250529"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronisieren von Projekt-Ist-Werten direkt aus Project Service Automation mit der Projektintegrationserfassung für die Buchung in Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekt-Istwerte direkt aus Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.

Die Vorlage synchronisiert Buchungen aus der Project Service Automation mit einer Stagingtabelle in Finance. Nachdem die Synchronisierung abgeschlossen wurde, **müssen** Sie die Daten von der Stagingtabelle in die Integrationserfassung importieren.

> [!NOTE]
> - Integration von Projekt-Istwerten ist ab Version 8.0.1 oder höher verfügbar.
> - Wenn Sie Enterprise Edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.
> - Wenn Sie Version 7.3.0 verwenden und Gebührenbuchungen aus Project Service Automation übernehmen, müssen Sie KB 4345320 installieren, um diese Gebühren in der Projektrechnung einzuschließen.
> - Wenn Sie Mehrwertsteuerbeträge rechtzeitig oder Ausgabenbuchungen in Project Service Automation eingeben, müssen Sie Project Servie Automation Update 7 installieren. Anderenfalls werden die Steuer-Ist-Werte nicht mit der zugeordneten Zeit oder Ausgaben-Ist-Werten verknüpft, und sie werden nicht mit Finance synchronisiert. Weitere Informationen erhalten Sie vom Support.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

Die Project Service Automation nach Finance-Integrationslösung nutzen die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance zu synchronisieren. Die Integrationsvorlage, die in der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integrationmit Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekt-Ist-Werte aus Project Service Automation

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Wenn Sie auf die verfügbaren Vorlagen im Microsoft PowerApps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgende Vorlage und zugrunde liegenden Aufgaben werden verwendet, um Projektistwerte von Project Service Automation mit Finance zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektkosten (PSA zu Fin und Ops)
- **Name der Aufgaben im Projekt:**

    - Istwerte
    - Transaktionsverbindungen

### <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finanzen                                   |
|----------------------------|----------------------------------------------------------|
| Istwerte                    | Integrationsentität für Projekt-Istwerte                   |
| Transaktionsverbindungen    | Integrationsentität für Projektbuchungsbeziehungen |

### <a name="entity-flow"></a>Entitätsfluss

Projekt-Ist-Werte werden in Project Service Automation verwaltet und mit Finance mit der Projektintegrationserfassung synchronisiert. Die Buchhaltung wird basierend auf den Standardfinanzdimensionen und der Buchungseinrichtung angewendet.

### <a name="prerequisites"></a>Erforderliche Komponenten

Bevor die Synchronisieren von Kosten erfolgen kann, müssen Sie die Project Service Automation Integrationsparameter und die Projekte, Projektaufgaben und Projektausgabentransaktionskategorien synchronisieren.

### <a name="power-query"></a>Powerabfrage

In der Projekt-Ist-Werte-Vorlage müssen Sie Microsoft Power Query für Excel verwenden, um diese Aufgaben abzuschließen:

- Transformieren Sie den Transaktionstyp in Project Service Automation zum korrekten Transaktionstyp in Finance Diese Transformation ist bereits in der Projekt-Ist-Werte-(PSA zu Fin and Ops)-Vorlage definiert.
- Transformieren Sie den Fakturierungstyp in Project Service Automation zum korrekten Fakturierungstyp in Finance. Diese Transformation ist bereits in der Projekt-Ist-Werte-(PSA zu Fin and Ops)-Vorlage definiert. Der Fakturierungstyp wird dann der Positionseigenschaft zugeordnet, basierend auf der Konfiguration auf der Seite **Project Service Automation-Integrationsparameter**.
- Filtern Sie nach bestimmten Ressourcenorganisationseinheiten, die mit dieser Vorlage synchronisiert werden müssen.
- Wenn Intercompany-Zeit oder Intercompany-Ausgaben-Ist-Werte mit Finance synchronisiert werden, müssen Sie die Vertragsorganisationseinheit zur richtigen juristischen Person in Finance zuordnen. In den Projekt-Ist-Werten (PSA zu Fin and Ops) wird eine bedingte Spalte basierend auf Demodaten definiert. Sie müssen die zuletzt eingefügte bedingte Spalte mit den richtigen juristischen Personen aktualisieren. Anderenfalls erfolgt entweder möglicherweise ein Integrationsfehler oder inkorrekte Ist-Wert-Transaktionen werden möglicherweise nach Finance importiert.
- Wenn Intercompany-Zeit oder Intercompany-Ausgaben-Ist-Werte nicht mit Finance synchronisiert werden, müssen Sie die zuletzt eingefügte bedingte Spalte aus Ihrer Vorlage löschen. Anderenfalls erfolgt entweder möglicherweise ein Integrationsfehler oder inkorrekte Ist-Wert-Transaktionen werden möglicherweise nach Finance importiert.

#### <a name="contract-organizational-unit"></a>Vertragsorganisationseinheit
Um die eingefügte bedingte Spalte in der Vorlage zu aktualisieren, klicken Sie auf den Pfeil **Zuordnen**, um die Zuordnung zu öffnen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus, um Power Query zu öffnen.

- Wenn Sie die Vorlage der standardmäßigen Projekt-Ist-Werte (PSA zu Fin and Ops) verwenden, wählen Sie in Power Query die letzte **Eingefügte Bedingung** aus dem Abschnitt **Angewendete Schritte** aus. Im Eintrag **Funktion** ersetzen Sie **USSI** durch den Namen der juristischen Person, die bei der Integration verwendet werden soll. Fügen Sie bei Bedarf zusätzliche Bedingungen dem Eintrag **Funktion** hinzu und aktualisieren Sie die Bedingung **sonst** aus **USMF** auf die korrekte juristische Person.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie die Spalte hinzufügen, um Intercompany-Zeit und Ausgaben zu unterstützen. Wählen Sie **Bedingte Spalte hinzufügen**, und geben Sie einen Namen für die Spalte ein, wie beispielsweise **LegalEntity**. Geben Sie eine Bedingung für die Spalte ein, wobei, „if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null”.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung in der Datenintegration. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Vorlagenzuordnung](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Aus Stagingtabelle nach der Integration aus Project Service Automation importieren

Der periodische Prozess „Aus Stagingtabelle importieren” muss nach der Synchronisierung von Ist-Werten aus Project Service Automation mit Finance ausgeführt werden. Dieser Prozess importiert die Projekttransaktionen aus der Stagingtabelle in die Project Service Automation Integrationserfassung, wenn die Buchungen angewendet wird und die importierten Buchungen gebucht werden können. Es wird empfohlen, diesen Prozess im Stapelverarbeitungsmodus auszuführen. Er kann optional so eingerichtet werden, dass er als wiederkehrende Stapelverarbeitung ausgeführt wird.

## <a name="update-actuals-from-finance"></a>Aktualisierung von Istwerten aus Finance

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Belegnummern und Mehrwertsteuer für gebuchte Projekttransaktionen von Finance zu Project Service Automation zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projekt-Istwerte aktualisiert ( Fin Ops zu PSA)
- **Name der Aufgaben im Projekt:**

    - Istwerte 
    - Transaktionsverbindungen

### <a name="entity-set"></a>Entitätssatz

| Finanzen                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integrationsentität für Projekt-Istwerte                   | Istwerte                    |
| Integrationsentität für Projektbuchungsbeziehungen | Transaktionsverbindungen    |

### <a name="entity-flow"></a>Entitätsfluss

Projekt-Ist-Werte werden in Project Service Automation verwaltet und mit Finance mit der Projektintegrationserfassung synchronisiert. Nachdem Ist-Werte in Finance gebucht sind, werden sie in Project Service Automation aktualisiert mit der Belegnummer aus Finance. Wenn Mehrwertsteuern in Finance hinzugefügt wurden, werden neue Steuer-Ist-Werte in Project Service Automation erstellt.

### <a name="power-query"></a>Powerabfrage

In der Updatevorlage der Projekt-Ist-Werte müssen Sie Power Query verwenden, um diese Aufgaben abzuschließen:

- Transformieren Sie den Transaktionstyp in Finance zum korrekten Transaktionstyp in Project Service Automation. Diese Transformation ist bereits in der Updatevorlage für Projekt-Ist-Werte (Fin and Ops zu PSA) definiert.
- Transformieren Sie den Fakturierungstyp in Finance zum korrekten Fakturierungstyp in Project Service Automation. Diese Transformation ist bereits in der Updatevorlage für Projekt-Ist-Werte (Fin and Ops zu PSA) definiert.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Finance zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Vorlagenzuordnung](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
