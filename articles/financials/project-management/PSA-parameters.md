---
title: Project Service Automation Integrationsparameter
description: In diesem Thema wird erläutert, wie Sie die Eingabe von Standarddaten konfigurieren, wenn Sie Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations integrieren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "347053"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation-Integrationsparameter

[!include[banner](../includes/banner.md)]

Auf der Seite **Project Service Automation Integrationsparameter** können Sie konfigurieren, wie Standarddaten eingegeben werden, wenn Sie Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations integrieren. Damit Projekte von Project Service Automation erfolgreich mit Finance and Operations synchronisiert werden, müssen Sie die folgenden Felder einrichten.

> [!NOTE]
> - Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Microsoft Dynamics 365 for Finance and Operations, Version 8.0 verfügbar.
> - Integration von Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher verfügbar.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch KB 4131710 installieren.

| Registerkarte                    | Feld                | Beschreibung |
|------------------------|----------------------|-------------|
| Allgemein                | Standardprojekttyp | Wählen Sie den Standardprojekttyp aus. Wenn Projekte von Project Service Automation synchronisiert werden, wird dieser Wert verwendet, wenn Sie keinen Standardwert in der Integrationsvorlage angegeben haben. Während der Synchronisierung wird das Feld **Projekttyp** von neuen Projekten auf diesen Wert festgelegt. Allerdings wird der Wert möglicherweise aktualisiert, wenn die Projektvertragspositionen von Project Service Automation synchronisiert werden. |
|                        | Zeitkategorie        | Wählen Sie die Standardzeitkategorie aus. Dieser Wert wird verwendet, wenn Stundenvorkalkulationen von Project Service Automation synchronisiert werden. Wenn die Stundenvorkalkulationen und Stunden-Ist-Werte von Project Service Automation synchronisiert werden, wird das Feld **Kategorie** neuer Projektstundenprognosen in Finance and Operations auf diesen Wert festgelegt. |
|                        | Gebührenkategorie         | Wählen Sie die Standardgebührenkategorie aus. Dieser Wert wird verwendet, wenn Gebühren-Ist-Werte von Project Service Automation synchronisiert werden. Wenn die Gebühren-Ist-Werte von Project Service Automation synchronisiert werden, wird das Feld **Kategorie** neuer Gebührenbuchungen in Finance and Operations auf diesen Wert festgelegt. |
| Projektgruppenstandards | Projekttyp         | Klicken Sie **Neu**, um eine Zeile hinzuzufügen, in der Sie den Projekttyp auswählen können, für den die Standardprojektgruppe festgelegt werden soll. Ein spezifischer Projekttyp kann in der Konfiguration nur einmal ausgewählt werden. |
|                        | Projektgruppe        | Wählen Sie die Standardprojektgruppe für den ausgewählten Projekttyp aus. Wenn neue Projekte von Project Service Automation synchronisiert werden, wird das Feld **Projektgruppe** auf den Standardwert für den Projekttyp festgelegt, wenn Sie keinen Standardwert in der Integrationsvorlage angegeben haben. |
| Standards Fakturierungstyp  | Fakturierungstyp         | Klicken Sie auf **Neu**, um eine Reihe hinzuzufügen, in der Sie den Fakturierungstyp auswählen können, für den die Standardpositionseigenschaft festlegt werden soll. Ein spezifischer Fakturierungstyp kann in der Konfiguration nur einmal ausgewählt werden. |
|                        | Abrechnungscode        | Wählen Sie die Standardpositionseigenschaft für den ausgewählten Fakturierungstyp aus. Wenn neue Stundenvorkalkulationen, neue Ausgabenvorkalkulationen oder neue Ist-Werte von Project Service Automation synchronisiert werden, wird das Feld **Positionseigenschaft** auf den Standardwert für den Fakturierungstyp festgelegt. |
| Funktionssperrung  | Nicht zutreffend       | Hier können Sie die Funktionen auswählen, die Sie im Bereich Finance and Operations für Projekte und Verträge deaktivieren möchten, die aus Project Service Automation stammen. Beispielsweise können Sie die Fähigkeit deaktivieren, Verträge und Projekte zu bearbeiten, Projektstrukturpläne zu erstellen und Arbeitszeitnachweise in Finance and Operations einzugeben. Buchhaltungs-zugeordnete Felder bleiben aktiviert, selbst wenn sie durch die Parametereinstellungen nicht verfügbar sind. Standardmäßig sind alle Funktionen aktiviert. |
