---
title: Beschaffungsworkflows
description: "Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat. Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 27c211e6ded17e085559add916c28a48c40e5b8e
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Beschaffungsworkflows

Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat. Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss. Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:
-   **Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.
-   **Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.
-   ** ** Zentralisierte Arbeitsliste — Benutzer können eine zentralisierte Arbeitsliste öffnen, um die Workflowaufgaben und - genehmigungen anzuzeigen, die Ihnen über den Workflow zugewiesen wurden alle, wie er in teilnehmen. Dies ist in der Arbeitsaufgabenseite verfügbar.

## <a name="the-types-of-workflows-that-you-can-create"></a> Erstellbare Workflowtypen
Die folgenden Workflowtypen stehen für die Beschaffung zur Verfügung.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Typ**                         | **Mit diesem Typ können Sie folgende Aufgaben ausführen:**                                          |
| Prüfung der Bestellanforderungen      | Erstellen Sie Prüfungsworkflows für Bestellanforderungen.            |
| Prüfung der Bestellanforderungsposition | Erstellen Sie Prüfungsworkflows für Bestellanforderungspositionen.       |
| Bestellworkflow          | Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellungen.     |
| Bestellpositionsworkflow     | Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellpositionen. |

## <a name="creating-a-workflow"></a>Erstellen eines Workflows
So erstellen Sie einen Workflow, den Einstellungsbeschaffungs- &gt; Beschaffungs- Beschaffung und &gt; -Bevorratungsworkflow und fahren einen neuen Workflow durch die Auswählen des Typs des Workflows erstellen, den Sie erstellen möchten.  

Auf der Workflowarbeitsfläche können Sie Workflowelemente in den Designer ziehen und die Elemente in einen Fluss verknüpfen. Die Workflowelemente sollten konfiguriert werden. Für Genehmigungs- und Aufgabenworkflowelemente können Sie konfigurieren, welcher Teilnehmer Aktivitäten ausführen soll.
Teilnehmertypen
----------------------

Sie können folgenden Teilnehmergruppen einen Genehmigungsschritt zuweisen.

| Benutzergruppe    | Beschreibung                                                               |
|---------------|---------------------------------------------------------------------------|
| Teilnehmer   | Weisen Sie den Genehmigungsschritt den Mitgliedern einer Gruppe oder Rolle zu.                   |
| Hierarchie     | Weisen Sie den Genehmigungsschritt den Benutzern in einer bestimmten Organisationshierarchie zu. |
| Workflowbenutzer | Weisen Sie den Genehmigungsschritt den Benutzern dieses Workflows zu.                       |
| Warteschlange         | Weisen Sie den Genehmigungsschritt einer Warteschlange für Arbeitsaufgaben zu.                            |
| Benutzer          | Weisen Sie den Genehmigungsschritt bestimmten Benutzern zu.                               |



<a name="see-also"></a>Siehe auch
--------

[Definieren von geschäftlichen Prozessworkflows für Bestellanforderungen.](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Purchase requisition workflow](purchase-requisitions-workflow.md)


