---
title: "Synchronisieren Sie Projektkosten von Project Service Automation direkt in die Projekt-Integrationserfassung für die Buchung in Finance and Operations"
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Project Service Automation in Dynamics 365 for Finance and Operations zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronisieren Sie Projektkosten von Project Service Automation direkt in die Projekt-Integrationserfassung für die Buchung in Finance and Operations

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Project Service Automation in Dynamics 365 for Finance and Operations zu synchronisieren.

Die Vorlage synchronisiert Buchungen aus der Project Service Automation in eine Stagingtabelle in Finance and Operations. Nachdem die Synchronisierung abgeschlossen wurde, müssen Sie von der Stagingtabelle in die Integrationserfassung importieren.

> [!NOTE]
> Projektkostenintegration ist in Dynamics 365 for Finance and Operations, Version 8.01 verfügbar.

> [!NOTE]
> Wenn Sie Mehrwertsteuerbeträge für Ausgabenbuchungen in der Project Service Automation eingeben, müssen Sie die Project Servie Automation Update 7 installieren. Wenn diese Aktualisierung nicht eingerichtet ist, werden die Steuerkosten nicht mit den zugeordneten Zeit- oder Ausgabenkosten verknüpft und werden nicht in Finance and Operations synchronisiert. Weitere Informationen erhalten Sie vom Support.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die  Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlage, die in der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance and Operations.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integrationmit Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektkosten von Project Service Automation zu Finance and Operations zu synchronisieren:

-  **Name der Vorlage in der Datenintegration:** Projektkosten (PSA zu Fin und Ops)

-  **Name der Aufgaben im Projekt:** 
    - Istwerte 
    - Transaktionsverbindungen

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Istwerte                         | Integrationsentität für Projekt-Istwerte                      |
| Transaktionsverbindungen         | Integrationsentität für Projektbuchungsbeziehungen    |

## <a name="entity-flow"></a>Entitätsfluss

Projektkosten werden in der Project Service Automation verwaltet und mit Finance and Operations in der Projektintegrationserfassung verwaltet. Die Buchhaltung wird basierend auf der Standardfinanzdimensionen und Buchungseinrichtung angewendet.

## <a name="preconditions"></a>Vorbedingungen

Bevor die Synchronisieren von Kosten erfolgen kann, müssen Sie die Project Service Automation Integrationsparameter und die Projekte, Projektaufgaben und Projektausgabentransaktionskategorien  synchronisieren.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query in der Projektkosten-Vorlage verwenden:
- Verschieben Sie den Project Service Automation **Transaktions-Typ** zum richtigen **Transaktionstyp** in Finance and Operations Die Vorlage der Projektkosten (PSA zu Fin und Ops) hat diese Transformtion bereits definiert.
- Verschieben Sie den Project Service Automation **Rechnungs-Typ** zum richtigen **Rechnungstyp** in Finance and Operations. Die Vorlage der Projektkosten (PSA zu Fin und Ops) hat diese Transformtion bereits definiert. Der des Fakturierungstyps ist dann auf **Abrechnungscode** gemäß den Einstellungen im Dynamics 365 for Project Service Automation Integrationsparamter-Formular.
- Filtern Sie bestimmte **Ressourcenorganisationseinheiten**, die mit dieser Vorlage synchronisiert werden sollen.
- Wenn **Intercompany-Zeit oder Intercompany-Ausgaben** mit Finance and Operations synchronis"iert werden, müssen Sie die **Vertragsorganisationseinheit** zur richtigen **juristischen Person** in "Finance and Operations zuordnen. Die Projektkostenvorlage (PSA zu Fin and Ops) hat eine bedingte Spalte basierend auf dem Demodaten definiert. Sie müssen die letzte aktualisierte Bedingungsspalte mit den richtigen juristischen Personen aktualisieren. Erfolgt dies nicht, wird möglicherweise ein Integrationsfehler oder eine falsche Transaktion in Finance and Operations importiert.
- Wenn **Intercompanyzeit oder Intercompanyausgaben** nicht mit Finance and Operations synchronisiert werden, müssen Sie die letzte eingefügte Bedingung von Ihrer Vorlage gelöscht werden. Erfolgt dies nicht, wird möglicherweise ein Integrationsfehler oder eine falsche Transaktion in Finance and Operations importiert.

### <a name="contract-organizational-unit"></a>Vertrags-Oganisations-Einheit
Um die eingefügte Bedingungsspalte in der Vorlage zu aktualisieren, klicken Sie auf **Zuordnen**, um die Zuordnung zu öffnen. Wählen Sie Erweiterter Filter- und Abfragesyntax öffnen.
- Wenn Sie Vorlage der standardmäßigen Microsoft Project-Kosten (PSA zu Fin und Ops) verwenden, wählen Sie **Eingefügte Bedingung** im Abschnitt **Übernommene Schritte** aus. Unter **Funktion** ersetzen Sie Eingabe von **USSI** mit dem Namen der **Juristischen Entität** die bei der Integration verwendet werden soll. Fügen Sie bei Bedarf zusätzliche Bedingungen den Eintrag **Funktion** hinzu und aktualisieren Sie **einfügen** auch die richtigen von **USMF** unter **Juristische Person**.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen, um Intercompany-Zeit und Ausgaben zu unterstützen. Wählen Sie **Hinzufügen von bedingten Spalten** aus und geben Sie der Spalte einen Namen, wie LegalEntity. Geben Sie die Bedingung für die Spalte ein, wenn msdyn_contractorganizationalunitid.msdyn_name ist <organizational unit>, dann <enter the Legal entity>. sonst Null.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Vorlagenzuordnung](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Aus Stagingtabelle importieren

Der Import von periodischen Stagingtabellenprozessen muss nach der Synchronisierung der tatsächlichen Werte von Project Service Automation zu Finance and Operations ausgeführt werden. Dieser Prozess importiert die Projekttransaktionen aus der Stagingtabelle in die Project Service Automation Integrationserfassung, wenn die Buchungen angewendet wird und die importierten Buchungen gebucht werden können. Es wird empfohlen, diesen Prozess im Stapelverarbeitungsmodus optional auszuführen und können optional als wiederkehrende Stapelverarbeitung ausgeführt werden.

## <a name="update-actuals"></a>Aktualisierung von Istwerten

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Belegnummern und Mehrwertsteuer für gebuchte Projekttransaktionen von Finance and Operations zu Project Service Automation zu synchronisieren:

-  **Name der Vorlage in der Datenintegration:** Projekt-Istwerte aktualisiert ( Fin Ops zu PSA)
-  **Name der Aufgaben im Projekt:** 
     - Istwerte 
     - Transaktionsverbindungen

## <a name="entity-set"></a>Entitätssatz

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Integrationsentität für Projekt-Istwerte                         | Istwerte                           |
| Integrationsentität für Projektbuchungsbeziehungen       | Transaktionsverbindungen           |

## <a name="entity-flow"></a>Entitätsfluss

Projektkosten werden in der Project Service Automation verwaltet und mit Finance and Operations in der Projektintegrationserfassung synchronisiert. Einmal in Finance and Operations gebucht, werden die Ist-Werte in Project Service Automation aktualisiert mit der Belegnummer von Finance and Operations. Wenn Mehrwertsteuer im Bereich Finance and Operations hinzugefügt wurden, werden neue Steuer-Istwerte in Project Service Automation erstellt.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query in der aktualisierten Projekt-Istwert-Vorlage verwenden:
- Verschieben Sie den Finance and Operations **Transaktions-Typ** zum richtigen **Transaktionstyp** in Project Service Automation. Die aktualisierte Vorlage der Projekt-Istkosten  (Fin Ops zu PSA) hat diese Transformtion bereits definiert.
- Verschieben Sie den Finance and Operations **Rechnungs-Typ** zum richtigen **Rechnungstyp** in Project Service Automation. Die aktualisierte Vorlage der Projekt-Istkosten  (Fin Ops zu PSA) hat diese Transformtion bereits definiert.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Finance and Operations zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Vorlagenzuordnung](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




