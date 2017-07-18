---
title: Frachtverkehrsrouten mit mehreren Zwischenstopps planen
description: Dieser Artikel beschreibt die verschiedenen Elemente zur Planung von Transportrouten in Microsoft Dynamics 365 for Finance and Operations.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: e7965c094f91bcbcad21ecfa599f133a6e84f4f7
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Frachtverkehrsrouten mit mehreren Zwischenstopps planen

[!include[banner](../includes/banner.md)]


Dieser Artikel beschreibt die verschiedenen Elemente zur Planung von Transportrouten in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Sie können Routenpläne und Routenführungen für komplexe Transportrouten mit mehrere Haltepunkten verwenden. Wenn dieselbe Route regelmäßig verwendet wird, können Sie eine geplante Route einrichten.

## <a name="route-plans"></a>Planungen von Arbeitsplänen
Ein Routenplan enthält Routenabschnitte, die Informationen über die in der Route besuchten Haltepunkte und die für jedes Segment genutzten Spediteure bereitstellen. Sie müssen die Haltepunkte der Route als Hubs definieren. Ein Hub kann einen Kreditor, einen Lagerort, ein Debitor oder einfach nur Umladeort für einen anderen Spediteur sein. Sie können für jedes Segment "Kassakurse" für verschiedene Zuschläge definieren. Nachfolgend finden Sie einige Beispiele:

-   Zuschläge für den Weg zu den jeweiligen Segmenten
-   Zuschläge für die Abholung der Waren
-   Zuschläge für das Abliefern der Waren

Jede Routenplan muss einer Routenführung zugeordnet sein.

## <a name="route-guides"></a>Arbeitsplananleitungen
Eine Routenführung definiert die Kriterien für eine Zuordnung einer Ladung zu einem bestimmten Routenplan. Beispielsweise können Sie einen Ursprungs-Hub und einen Ziel-Hub, Beschränkungen für das Containervolumen oder Gewicht und einen Spediteur, eine Dienstleistung oder eine Gruppe festlegen. Routenführungen finden Sie auf der **Routen-Workbench-Satz**-Seite. Dort können Ladungen manuell oder automatisch zu Routen zugeordnet werden. Wenn die Routenführung für eine geplante Route gedacht ist, steht sie auch auf die **Ladungserstellungsworkbench**-Seite zur Verfügung.

## <a name="scheduled-routes"></a>Arbeitspläne
Eine geplante Route ist ein vordefinierter Routenplan, der über einen Zeitplan für die Versanddaten verfügt. Geplante Routen und nicht geplanten Routen unterscheiden sich durch die ihnen zugewiesenen Ladungen. Wenn Sie eine nicht geplante Route über den Routen-Workbench-Satz zuweisen, werden nur die Ladung und die Routenführung überprüft. Wenn Sie eine geplante Route zuweisen, werden auch die Daten und Adressen aus den Aufträgen und die Hubs, die Daten auf dem Routenplan berücksichtigt. Sie müssen die Seite "Routen-Workbench-Satz" nicht zur manuellen Zuweisung von Ladungen an eine geplante Route nutzen. Stattdessen können Sie die Seite "Ladungserstellungsworkbench" nutzen, um Ladungen auf Basis der Kundenadressen und Lieferdaten aus den Aufträgen für eine bestimmte geplante Router vorschlagen zu lassen. Für geplante Routen hat der Routenplan einen feste Start- und Ziel-Hubs. Normalerweise sind Spediteur und Dienstleistung für alle Segmente gleich. Sie können sich jedoch auch unterscheiden. Die Ziel-Hubs werden über die Postleitzahlen der im Rahmen der Route besuchten Kunden erstellt. Sie können für einen Routenplan mehrere Routen Zeitpläne definieren. Der Routenplan muss einer Routenführung zugeordnet sein. Für geplante Routen kann der Plan jedoch nur einer Routenführung zugeordnet werden. Der Routenplan wird nur zur Erstellung der tatsächlichen Routen auf der Seite **Routenzeitplan** genutzt. Sie können die Standard-Ladungsvorlage für Vorschläge zu Ladungen auf der Seite Ladungserstellungsworkbench verwenden.

## <a name="load-building-workbench"></a>Ladungserstellungsworkbench
Die Seite Ladungserstellungsworkbench verwendet die Adressen und Lieferdaten aus Aufträgen und die verfügbaren geplanten Routen, um eine Ladung vorzuschlagen. Standardmäßig werden die Werte der Route über die Arbeitsfläche eingegeben. Allerdings können Sie ein "Von"-Datum auswählen, das vor dem "Von"-Datum der Route liegt. Wenn eine Ladung vorgeschlagen wird, werden die Lieferadresse und das Lieferdatum für alle offenen Auftrage überprüft. Wenn die Postleitzahl der Lieferadresse der Postleitzahl eines Hubs im Routenplan entspricht, und wenn das Lieferdatum innerhalb des in den Kriterien gewählten Bereichs liegt, wird der Auftrag für die Ladung vorgeschlagen. Die Kapazität der Ladungsvorlage wird ebenfalls berücksichtigt. Es wird immer nur eine Ladung vorgeschlagen. Wenn Sie einen Auftrag haben, der nicht einbezogen ist, möchten Sie möglicherweise eine andere Ladungsvorlage verwenden (z. B. eine Ladungsvorlage für einen größeren LKW oder Container) oder eine zusätzliche Lieferung planen.




