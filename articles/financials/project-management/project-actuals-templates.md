---
title: "Synchronisieren von Projekt-Ist-Werten direkt aus Project Service Automation mit der Projektintegrationserfassung für die Buchung in Finance and Operations"
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projekt-Ist-Werte direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren."
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.contentlocale: de-de
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronisieren von Projekt-Ist-Werten direkt aus Project Service Automation mit der Projektintegrationserfassung für die Buchung in Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Projekt-Ist-Werte direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

Die Vorlage synchronisiert Buchungen aus der Project Service Automation mit einer Stagingtabelle in Finance and Operations. Nachdem die Synchronisierung abgeschlossen wurde, **müssen** Sie die Daten von der Stagingtabelle in die Integrationserfassung importieren.

> [!NOTE]
> - Integration von Projekt-Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher verfügbar.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 verwenden, nachdem Sie KB 4132657 und 4132660 KB installiert haben, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und Ist-Werte zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.
> - Wenn Sie Finance and Operations 7.3.0 verwenden und Gebührenbuchungen aus Project Service Automation übernehmen, müssen Sie KB 4345320 installieren, um diese Gebühren in der Projektrechnung einzuschließen.
> - Wenn Sie Mehrwertsteuerbeträge rechtzeitig oder Ausgabenbuchungen in Project Service Automation eingeben, müssen Sie Project Servie Automation Update 7 installieren. Anderenfalls werden die Steuer-Ist-Werte nicht mit der zugeordneten Zeit oder Ausgaben-Ist-Werten verknüpft, und sie werden nicht mit Finance and Operations synchronisiert. Weitere Informationen erhalten Sie vom Support.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlage, die in der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance and Operations.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integrationmit Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekt-Ist-Werte aus Project Service Automation

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Wenn Sie auf die verfügbaren Vorlagen im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte** aus, und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um die öffentlichen Vorlagen auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektkosten von Project Service Automation zu Finance and Operations zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektkosten (PSA zu Fin und Ops)
- **Name der Aufgaben im Projekt:**

    - Istwerte
    - Transaktionsverbindungen

### <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Istwerte                    | Integrationsentität für Projekt-Istwerte                   |
| Transaktionsverbindungen    | Integrationsentität für Projektbuchungsbeziehungen |

### <a name="entity-flow"></a>Entitätsfluss

Projekt-Ist-Werte werden in Project Service Automation verwaltet und mit Finance and Operations mit der Projektintegrationserfassung synchronisiert. Die Buchhaltung wird basierend auf den Standardfinanzdimensionen und der Buchungseinrichtung angewendet.

### <a name="prerequisites"></a>Erforderliche Komponenten

Bevor die Synchronisieren von Kosten erfolgen kann, müssen Sie die Project Service Automation Integrationsparameter und die Projekte, Projektaufgaben und Projektausgabentransaktionskategorien synchronisieren.

### <a name="power-query"></a>Powerabfrage

In der Projekt-Ist-Werte-Vorlage müssen Sie Microsoft Power Query für Excel verwenden, um diese Aufgaben abzuschließen:

- Transformieren Sie den Transaktionstyp in Project Service Automation zum korrekten Transaktionstyp in Finance and Operations Diese Transformation ist bereits in der Projekt-Ist-Werte-(PSA zu Fin and Ops)-Vorlage definiert.
- Transformieren Sie den Fakturierungstyp in Project Service Automation zum korrekten Fakturierungstyp in Finance and Operations. Diese Transformation ist bereits in der Projekt-Ist-Werte-(PSA zu Fin and Ops)-Vorlage definiert. Der Fakturierungstyp wird dann der Positionseigenschaft zugeordnet, basierend auf der Konfiguration auf der Seite **Project Service Automation-Integrationsparameter**.
- Filtern Sie nach bestimmten Ressourcenorganisationseinheiten, die mit dieser Vorlage synchronisiert werden müssen.
- Wenn Intercompany-Zeit oder Intercompany-Ausgaben-Ist-Werte mit Finance and Operations synchronisiert werden, müssen Sie die Vertragsorganisationseinheit zur richtigen juristischen Person in Finance and Operations zuordnen. In den Projekt-Ist-Werten (PSA zu Fin and Ops) wird eine bedingte Spalte basierend auf Demodaten definiert. Sie müssen die zuletzt eingefügte bedingte Spalte mit den richtigen juristischen Personen aktualisieren. Anderenfalls erfolgt entweder möglicherweise ein Integrationsfehler oder inkorrekte Ist-Wert-Transaktionen werden möglicherweise nach Finance and Operations importiert.
- Wenn Intercompany-Zeit oder Intercompany-Ausgaben-Ist-Werte nicht mit Finance and Operations synchronisiert werden, müssen Sie die zuletzt eingefügte bedingte Spalte aus Ihrer Vorlage löschen. Anderenfalls erfolgt entweder möglicherweise ein Integrationsfehler oder inkorrekte Ist-Wert-Transaktionen werden möglicherweise nach Finance and Operations importiert.

#### <a name="contract-organizational-unit"></a>Vertragsorganisationseinheit
Um die eingefügte bedingte Spalte in der Vorlage zu aktualisieren, klicken Sie auf den Pfeil **Zuordnen**, um die Zuordnung zu öffnen. Wählen Sie den Link **Erweiterte Abfrage und Filterung** aus, um Power Query zu öffnen.

- Wenn Sie die Vorlage der standardmäßigen Projekt-Ist-Werte (PSA zu Fin and Ops) verwenden, wählen Sie in Power Query die letzte **Eingefügte Bedingung** aus dem Abschnitt **Angewendete Schritte** aus. Im Eintrag **Funktion** ersetzen Sie **USSI** durch den Namen der juristischen Person, die bei der Integration verwendet werden soll. Fügen Sie bei Bedarf zusätzliche Bedingungen dem Eintrag **Funktion** hinzu und aktualisieren Sie die Bedingung **sonst** aus **USMF** auf die korrekte juristische Person.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie die Spalte hinzufügen, um Intercompany-Zeit und Ausgaben zu unterstützen. Wählen Sie **Bedingte Spalte hinzufügen**, und geben Sie einen Namen für die Spalte ein, wie beispielsweise **LegalEntity**. Geben Sie eine Bedingung für die Spalte ein, wobei, „if **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organizational unit\>, then \<enter the legal entity\>; else null”.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung in der Datenintegration. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Vorlagenzuordnung](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Aus Stagingtabelle nach der Integration aus Project Service Automation importieren

Der periodische Prozess „Aus Stagingtabelle importieren” muss nach der Synchronisierung von Ist-Werten aus Project Service Automation mit Finance and Operations ausgeführt werden. Dieser Prozess importiert die Projekttransaktionen aus der Stagingtabelle in die Project Service Automation Integrationserfassung, wenn die Buchungen angewendet wird und die importierten Buchungen gebucht werden können. Es wird empfohlen, diesen Prozess im Stapelverarbeitungsmodus auszuführen, und optional kann er so eingerichtet werden, dass er als wiederkehrende Stapelverarbeitung ausgeführt wird.

## <a name="update-actuals-from-finance-and-operations"></a>Ist-Werte aus Finance and Operations aktualisieren

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Belegnummern und Mehrwertsteuer für gebuchte Projekttransaktionen von Finance and Operations zu Project Service Automation zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projekt-Istwerte aktualisiert ( Fin Ops zu PSA)
- **Name der Aufgaben im Projekt:**

    - Istwerte 
    - Transaktionsverbindungen

### <a name="entity-set"></a>Entitätssatz

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integrationsentität für Projekt-Istwerte                   | Istwerte                    |
| Integrationsentität für Projektbuchungsbeziehungen | Transaktionsverbindungen    |

### <a name="entity-flow"></a>Entitätsfluss

Projekt-Ist-Werte werden in Project Service Automation verwaltet und mit Finance and Operations mit der Projektintegrationserfassung synchronisiert. Nachdem Ist-Werte in Finance and Operations gebucht sind, werden sie in Project Service Automation aktualisiert mit der Belegnummer aus Finance and Operations. Wenn Mehrwertsteuern in Finance and Operations hinzugefügt wurden, werden neue Steuer-Ist-Werte in Project Service Automation erstellt.

### <a name="power-query"></a>Powerabfrage

In der Updatevorlage der Projekt-Ist-Werte müssen Sie Power Query verwenden, um diese Aufgaben abzuschließen:

- Transformieren Sie den Transaktionstyp in Finance and Operations zum korrekten Transaktionstyp in Project Service Automation. Diese Transformation ist bereits in der Updatevorlage für Projekt-Ist-Werte (Fin and Ops zu PSA) definiert.
- Transformieren Sie den Fakturierungstyp in Finance and Operations zum korrekten Fakturierungstyp in Project Service Automation. Diese Transformation ist bereits in der Updatevorlage für Projekt-Ist-Werte (Fin and Ops zu PSA) definiert.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Finance and Operations zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Vorlagenzuordnung](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)

