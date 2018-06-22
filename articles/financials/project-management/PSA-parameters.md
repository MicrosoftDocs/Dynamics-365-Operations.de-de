---
title: Project Service Automation Integrationsparameter
description: "Sie können die Datenstandardwerte definieren, wenn sie in die Project Service Automation mit Dynamics 365 for Finance and Operations integriert werden."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
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
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automation Integrationsparameter

Auf der Seite **Project Service Automationsintegrationsparameter** können Sie die Datenstandardwerte konfigurieren, wenn sie mit der Project Service Automation mit Finance and Operations integriert werden. Folgende Komponenten müssen eingerichtet werden, damit Projekte von der Project Service Automation im Bereich Finance and Operations erfolgreich synchronisiert werden können.

> [!NOTE]
> Projektaufgaben-Integration, Ausgabenbuchungskategorien, StundensDynamics 365 for Finance and Operations version 8.0.chätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Dynamics 365 for Finance and Operations Version 8.0 verfügbar.




| **Registerkarte**                      | **Feld**                          | **Beschreibung**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Allgemeines**                  | **Standardprojekttyp**               | Wählen Sie den Standardwert für **Projekttyp** aus, wenn Projekte von der Project Service Automation synchronisiert werden, wenn Sie einen Standardwert für die Integrationsvorlage angegeben haben. Bei der Synchronisierung haben neue Projekte möglicherweise den **Projekttyp** auf diesen Wert festgelegt und können aktualisiert werden, wenn die Projektvertragspositionen von der Project Service Automation synchronisiert werden.               |
| **Allgemeines**                  | **Zeitkategorie**                      | Wählen Sie den Standardwert für **Zeitkategorie** aus, das Stundenschätzungen ist, wenn von der Project Service Automation synchronisiert werden. Bei der Synchronisierung haben neue Projektstundenplanungen in Finance and Operations die **Kategorie** auf diesen Wert festgelegt wird, wenn die Stundenschätzungen und die tatsächlichen Stunden von der Project Service Automation synchronisiert werden.   |
| **Allgemeines**                  | **Gebührenkategorie**                       | Wählen Sie den Standardwert für **Gebührenkategorie** aus, wenn tatsächliche Gebühren von der Project Service Automation synchronisiert werden. Bei der Synchronisierung haben neue Gebührentransaktionen in Finance and Operations die **Kategorie** auf diesen Wert festgelegt wird, wenn die Stundenschätzungen und die tatsächlichen Stunden von der Project Service Automation synchronisiert werden.          |
| **Projektgruppenstandards**   | **Projekttyp** | Klicken Sie **Neu**, um eine Position hinzuzufügen, in der Sie den Projekttyp auswählen können, für den die Standardprojektgruppe festlegt ist. Ein Projekttyp kann in der Variante nur einmal ausgewählt werden.              
|                              | **Projektgruppe**          | Wählen Sie die Standardprojektgruppe für den angegebenen Projekttyp aus. Wählen Sie den Standardwert für die **Projektgruppe** aus, wenn neue Projekte von der Project Service Automation synchronisiert werden, wenn Sie keinen Standardwert für die Integrationsvorlage angegeben haben.  |
| **Standards Fakturierungstyp**    | **Fakturierungstyp** | Klicken Sie **Neu**, um eine Position hinzuzufügen, in der Sie den Projekttyp auswählen können, für den die Standardprojektgruppe festlegt ist. Ein Rechnungstyp kann in der Variante nur einmal ausgewählt werden.          |
|                              | **Abrechnungscode**| Wählen Sie die Standardzeileneigenschaft für den angegebenen Rechnungstyp aus. Wenn neue Stundenschätzungen, neue Ausgabenenschätzungen oder neue Wirklichkeiten von der Project Service Automation synchronisiert werden, ist der **Abrechnungscode** auf Grundlage der des Fakturierungstyps.          |
| **Funktionssperrung**    |                   | Hier können Sie die Funktionen auswählen, die Sie im Bereich Finance and Operations für Projekte und Verträge deaktivieren möchten, die aus Project Service Automation stammen. Beispielsweise können Sie angeben, ob Sie die Fähigkeit nicht benötigen, Verträge und Projekte zu bearbeiten, Projektstrukturpläne zu erstellen und Arbeitszeitnachweise im Bereich Finance and Operations  einzugeben. Buchhaltungs-zugeordnete Felder bleiben aktiviert, selbst wenn sie durch die Parametereinstellungen nicht verfügbar sind. Standardmäßig sind alle Funktionen aktiviert.           |

