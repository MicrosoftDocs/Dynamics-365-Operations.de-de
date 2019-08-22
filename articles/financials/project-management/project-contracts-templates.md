---
title: Synchronisieren von Projektverträgen und Projekten direkt aus Project Service Automation mit Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte und Projektverträge direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: be23b99ddc224328cf067fe0bf36be93fcef4337
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846031"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektverträgen und Projekten direkt aus Project Service Automation mit Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte und Projektverträge direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

> [!NOTE] 
> Wenn Sie Microsoft Dynamics 365 for Finance and Operations,Enterprise Edition 7.3.0 verwenden, müssen Sie KB 4074835 installieren.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

> [!NOTE]
> Bevor Sie die Project Service Automation to Finance and Operations Integrationslösung nutzen können, sollten Sie sich mit der Datenenintegrationsfunktion Microsoft Dynamics 365 vertraut gemacht haben.

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlagen, die in der Daten-Integrationsfunktion verfügbar sind, aktivieren den Fluss von Daten zu Projektverträgen, Projekten, Projektvertragspositionen und Projektvertragszeilen-Meilensteine von Project Service Automation zu Finance and Operations.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integrationmit Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Wenn Sie auf die verfügbaren Vorlagen im Microsoft PowerApps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektverträge und Projekte von Project Service Automation zu Finance and Operations zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projekte und Verträge (PSA zu Fin und Ops)
- **Name der Aufgaben im Projekt:**

    - Projektverträge PSA zu Fin und Ops
    - Projekte PSA zu Fin und Ops
    - Projektvertragszeilen PSA zu Fin und Ops
    - Projektvertragszeilen-Meilensteine PSA zu Fin und Ops

Vor der Synchronisierung von Projektverträgen und Projekten müssen Sie zunächst Konten synchronisieren.

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Aufträge                           | Integrationsentität für Projektvertrag                |
| Projekte                         | Integrationsentität für Projekt                         |
| Auftragspositionen                      | Integrationsentität für Projektvertragsposition           |
| Projektvertragspositionen-Meilenstein | Integrationsentität für Meilensteine von Projektvertragspositionen |

## <a name="entity-flow"></a>Entitätsfluss

Projektverträge werden in der Project Service Automation verwaltet und zu Finance and Operations als Projektverträge synchronisiert. Als Teil der Integrationsvorlage können Sie die Integrationsquelle im Bereich Finance and Operations für den Projektvertrag einrichten.

Zeit- und Materialprojekt sowie Festpreisprojekte werden in Project Service Automation verwaltet, und sie werden mit Finance and Operations als Projekte synchronisiert. Als Teil der Integrationsvorlage können Sie die Integrationsquelle im Bereich Finance and Operations für das Projekt einrichten.

Projektvertragspositionen werden in Project Service Automation verwaltet und zu Finance and Operations als Projektvertrags-Fakturierungsregeln synchronisiert. Wenn sich die Fakturierungsmethode vom Standardprojekttyp unterscheidet, wird durch die Synchronisierung der Projekttyp für das Vertragspositionsprojekt und die Projektgruppe aktualisiert.

Projektvertragspositionen-Meilensteine werden in Project Service Automation verwaltet und zu Finance and Operations als Projektvertrags-Fakturierungsregeln synchronisiert.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Project Service Automation zu Finance and Operations Integrationslösung

Das Feld **Projektvertragskennung** ist auf der Seite **Projektverträge** verfügbar. Das Feld wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration.

Wenn ein neuer Projektvertrag erstellt wird, wenn ein **Projektvertragskennungs**-Wert nicht bereits vorhanden ist, wird er automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **ORD**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Hier ist ein Beispiel: **ORD-01022-Z4M9Q0**.

Das Feld **Projektnummer** steht auf der Seite **Projekte** zur Verfügung. Das Feld wurde zu einem natürlichen und eindeutigen Schlüssel für die Unterstützung der Integration.

Wenn ein neues Projekt angelegt wird und noch kein **Projektnummer**-Wert vorhanden ist, wird es automatisch unter Verwendung einer fortlaufenden Nummerierung erstellt. Der Wert besteht aus **PRJ**, gefolgt von einer aufsteigenden fortlaufenden Nummerierung und einem Suffix aus sechs Zeichen. Hier ist ein Beispiel: **PRJ-01049-CCNID0**.

Wenn die Project Service Automation zu Finance and Operations Integrationslösung angewendet wird in <TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution> wird ein Aktualisierungsskript im **Projektvertrag ID-Feld** für Projektverträge und -**Projektnummeren**-Feld für vorhandene Projekte in der Project Service Automation eingerichtet.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

- Vor der Synchronisierung von Projektverträgen und Projekten müssen Sie zunächst Konten synchronisieren.
- In Ihrem Verbindungssatz fügen Sie eine Integrationsschlüsselfeldzuordnung für **msdyn\_organizationalunits** zu **msdyn\_name \[Name\]** hinzu. Möglicherweise müssen Sie zuerst ein Projekt im Verbindungssatz hinzufügen. Weitere Informationen finden Sie unter [Datenintegration in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- In Ihrem Verbindungssatz fügen Sie eine Integrationsschlüsselfeldzuordnung für **msdyn\_projects** zu **msdynce\_projectnumber \[Project Number\]** hinzu. Möglicherweise müssen Sie zuerst ein Projekt im Verbindungssatz hinzufügen. Weitere Informationen finden Sie unter [Datenintegration in Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** für Projektverträge und Projekte kann mit einem anderen Wert aktualisiert oder von der Zuordnung entfernt werden. Der Standardvorlagewert ist **Project Service Automation**.
- Die Zuordnung **PaymentTerms** muss aktualisiert werden, damit er gültige Zahlungsbedingungen im Bereich Finance and Operations anzeigt. Sie können die Zuordnung aus der Projektaufgabe auch wieder entfernen. Die Standardwerte für Standardwertzuordnung hat Demodaten. Die folgende Tabelle zeigt die Werte in der Project Service Automation.

    | Wert | Beschreibung   |
    |-------|---------------|
    | 1     | Netto 30        |
    | 2     | 2% 10, Netto 30 |
    | 3     | Netto 45        |
    | 4     | Netto 60        |

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn die folgenden Bedingungen erfüllt sind:

- Sie haben Aufträge in Microsoft Dynamics 365 for Sales.
- Es haben mehrere Organisationseinheiten in der Project Service Automation und diese Organisationseinheiten werden mehreren juristischen Personen im Bereich Finance and Operations zugeordnet.

Wenn Sie Power Query verwenden möchten, folgen Sie diesen Richtlinien:

- Die Vorlage für Projekte und Verträge (PSA zu Fin and Ops) besitzt einen Standardfilter, der nur Aufträge vom Typ **Arbeitsaufgabe (msdyn\_ordertype = 192350001)** enthält. Durch diesen Filter wird sichergestellt, dass Projektverträge nicht für Aufträge in Finance and Operations erstellt werden. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.
- Sie müssen einen Power Query-Filter erstellen, der nur Vertragsorganisationen enthält, die mit der juristischen Person des Integrations-Verbindungssatzes synchronisiert werden sollen. Beispielsweise sollten Projektverträge, die Sie mit der Vertragsorganisationseinheit von Contoso USA haben, mit der USSI-juristischen Person synchronisiert werden, aber Projektverträge, die Sie mit der Vertragsorganisationseinheit von Contoso Global haben, sollten mit der USMF juristischen Person synchronisiert werden. Wenn Sie diesen Filter nicht Ihrer Aufgabenzuordnung hinzufügen, werden alle Projektverträge mit der juristischen Person synchronisiert, die für den Verbindungssatz definiert ist, unabhängig von der Vertragsorganisationseinheit.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

> [!NOTE] 
> **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** Und **AddressZipCode** Felder sind nicht in der Standardzuordnung für Projektverträge enthalten. Sie können Zuordnungen hinzugefügen, wenn Sie festlegen, dass die Daten für Projektverträge synchronisiert werden.
>
> **Beschreibung**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** Und **ProjectType** Felder sind nicht in der Standardzuordnung für Projekte einbezogen. Sie können Zuordnungen hinzugefügen, wenn Sie festlegen, dass die Daten für Projeke synchronisiert werden.

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
