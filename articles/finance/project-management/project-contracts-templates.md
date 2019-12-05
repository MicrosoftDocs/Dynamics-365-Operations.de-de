---
title: Synchronisieren von Projektverträgen und Projekten direkt aus Project Service Automation mit Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte und Projektverträge direkt aus Microsoft Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b44fc116f1dcaa1275b2262487ef9114bce639c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773853"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektverträgen und Projekten direkt aus Project Service Automation mit Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte und Projektverträge direkt aus Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.

> [!NOTE] 
> Wenn Sie Enterprise Edition 7.3.0 verwenden, müssen Sie KB 4074835 installieren.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

> [!NOTE]
> Bevor Sie die Project Service Automation to Finance Integrationslösung nutzen können, sollten Sie sich mit der Datenenintegrationsfunktion von Dynamics 365 vertraut gemacht haben.

Die Project Service Automation nach Finance-Integrationslösung nutzen die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance zu synchronisieren. Die Integrationsvorlagen, die in der Daten-Integrationsfunktion verfügbar sind, aktivieren den Fluss von Daten zu Projektverträgen, Projekten, Projektvertragspositionen und Projektvertragszeilen-Meilensteine von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Wenn Sie auf die verfügbaren Vorlagen im Microsoft Power Apps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektverträge und Projekte von Project Service Automation zu Finance zu synchronisieren:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integration in Dynamics 365 Project Service Automation v2.x
- **Name der Vorlage in der Datenintegration:** Projekte und Verträge (PSA zu Fin und Ops)
- **Name der Aufgaben im Projekt:**

    - Projektverträge PSA zu Fin und Ops
    - Projekte PSA zu Fin und Ops
    - Projektvertragszeilen PSA zu Fin und Ops
    - Projektvertragszeilen-Meilensteine PSA zu Fin und Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integration in Dynamics 365 Project Service Automation v3.x
Es gibt eine Schemaänderung in Project Service Automation, die sich auf die Vorlage für Projektvertragspositionsmeilensteine auswirkt und die Nutzung der Vorlage für Version v2 der erforderlich, um Project Service Automation v3.x in Dynamics 365 zu integrieren.

- **Name der Vorlage in der Datenintegration:** Projekte und Verträge (PSA 3.x zu Fin und Ops) - v2
- **Name der Aufgaben im Projekt:**

    - Projektverträge PSA zu Fin und Ops
    - Projekte PSA zu Fin und Ops
    - Projektvertragszeilen PSA zu Fin und Ops
    - Projektvertragszeilen-Meilensteine PSA zu Fin und Ops

Vor der Synchronisierung von Projektverträgen und Projekten müssen Sie zunächst Konten synchronisieren.

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation       | Finanzen                                                |
|----------------------------------|--------------------------------------------------------|
| Aufträge                           | Integrationsentität für Projektvertrag                |
| Projekte                         | Integrationsentität für Projekt                         |
| Auftragspositionen                      | Integrationsentität für Projektvertragsposition           |
| Projektvertragspositionen-Meilenstein | Integrationsentität für Meilensteine von Projektvertragspositionen |

## <a name="entity-flow"></a>Entitätsfluss

Projektverträge werden in der Project Service Automation verwaltet und zu Finance als Projektverträge synchronisiert. Als Teil der Integrationsvorlage können Sie die Integrationsquelle in Finance für den Projektvertrag einrichten.

Zeit- und Materialprojekt sowie Festpreisprojekte werden in Project Service Automation verwaltet, und sie werden mit Finance als Projekte synchronisiert. Als Teil der Integrationsvorlage können Sie die Integrationsquelle in Finance für das Projekt einrichten.

Projektvertragspositionen werden in Project Service Automation verwaltet und zu Finance als Projektvertrags-Fakturierungsregeln synchronisiert. Wenn sich die Fakturierungsmethode vom Standardprojekttyp unterscheidet, wird durch die Synchronisierung der Projekttyp für das Vertragspositionsprojekt und die Projektgruppe aktualisiert.

Projektvertragspositionen-Meilensteine werden in Project Service Automation verwaltet und zu Finance als Projektvertrags-Fakturierungsregeln synchronisiert.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation zu Finance-Integrationslösung

Das Feld **Projektvertragskennung** ist auf der Seite **Projektverträge** verfügbar. Das Feld wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration.

Wenn ein neuer Projektvertrag erstellt wird, wenn ein **Projektvertragskennungs**-Wert nicht bereits vorhanden ist, wird er automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **ORD**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Hier ist ein Beispiel: **ORD-01022-Z4M9Q0**.

Das Feld **Projektnummer** steht auf der Seite **Projekte** zur Verfügung. Das Feld wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration.

Wenn ein neues Projekt angelegt wird und noch kein **Projektnummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **PRJ**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Hier ist ein Beispiel: **PRJ-01049-CCNID0**.

Wenn die Project Service Automation zu Finance Integrationslösung angewendet wird, legt ein Aktualisierungsskript das Feld **Projektvertrag ID** für vorhandene Projektverträge und das Feld **Projektnummern** für vorhandene Projekte in Project Service Automation fest.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

- Vor der Synchronisierung von Projektverträgen und Projekten müssen Sie zunächst Konten synchronisieren.
- In Ihrem Verbindungssatz fügen Sie eine Integrationsschlüsselfeldzuordnung für **msdyn\_organizationalunits** zu **msdyn\_name \[Name\]** hinzu. Möglicherweise müssen Sie zuerst ein Projekt im Verbindungssatz hinzufügen. Weitere Informationen finden Sie unter [Datenintegration in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- In Ihrem Verbindungssatz fügen Sie eine Integrationsschlüsselfeldzuordnung für **msdyn\_projects** zu **msdynce\_projectnumber \[Project Number\]** hinzu. Möglicherweise müssen Sie zuerst ein Projekt im Verbindungssatz hinzufügen. Weitere Informationen finden Sie unter [Datenintegration in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** für Projektverträge und Projekte kann mit einem anderen Wert aktualisiert oder von der Zuordnung entfernt werden. Der Standardvorlagewert ist **Project Service Automation**.
- Die Zuordnung **PaymentTerms** muss aktualisiert werden, damit er gültige Zahlungsbedingungen in Finance anzeigt. Sie können die Zuordnung aus der Projektaufgabe auch wieder entfernen. Die Standardwerte für Standardwertzuordnung hat Demodaten. Die folgende Tabelle zeigt die Werte in der Project Service Automation.

    | Wert | Beschreibung   |
    |-------|---------------|
    | 1     | Netto 30        |
    | 2     | 2% 10, Netto 30 |
    | 3     | Netto 45        |
    | 4     | Netto 60        |

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn die folgenden Bedingungen erfüllt sind:

- Sie haben Aufträge in Dynamics 365 Sales.
- Es haben mehrere Organisationseinheiten in der Project Service Automation und diese Organisationseinheiten werden mehreren juristischen Personen in Finance zugeordnet.

Wenn Sie Power Query verwenden möchten, folgen Sie diesen Richtlinien:

- Die Vorlage für Projekte und Verträge (PSA zu Fin and Ops) besitzt einen Standardfilter, der nur Aufträge vom Typ **Arbeitsaufgabe (msdyn\_ordertype = 192350001)** enthält. Durch diesen Filter wird sichergestellt, dass Projektverträge nicht für Aufträge in Finance erstellt werden. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.
- Sie müssen einen Power Query-Filter erstellen, der nur Vertragsorganisationen enthält, die mit der juristischen Person des Integrations-Verbindungssatzes synchronisiert werden sollen. Beispielsweise sollten Projektverträge, die Sie mit der Vertragsorganisationseinheit von Contoso USA haben, mit der USSI-juristischen Person synchronisiert werden, aber Projektverträge, die Sie mit der Vertragsorganisationseinheit von Contoso Global haben, sollten mit der USMF juristischen Person synchronisiert werden. Wenn Sie diesen Filter nicht Ihrer Aufgabenzuordnung hinzufügen, werden alle Projektverträge mit der juristischen Person synchronisiert, die für den Verbindungssatz definiert ist, unabhängig von der Vertragsorganisationseinheit.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE] 
> **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** Und **AddressZipCode** Felder sind nicht in der Standardzuordnung für Projektverträge enthalten. Sie können Zuordnungen hinzugefügen, wenn Sie festlegen, dass die Daten für Projektverträge synchronisiert werden.
>
> **Beschreibung**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** Und **ProjectType** Felder sind nicht in der Standardzuordnung für Projekte einbezogen. Sie können Zuordnungen hinzugefügen, wenn Sie festlegen, dass die Daten für Projeke synchronisiert werden.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Meilensteinzuordnung von Projektvertragspositionen in Projekten und PSA-Verträgen (3.x zu Dynamics) - Vorlage v2:

[![Vorlagenzuordnung](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
