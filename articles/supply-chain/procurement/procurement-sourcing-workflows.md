---
title: Beschaffungsworkflows
description: Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat. Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.
author: GalynaFedorova
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfd96690eea762d0797db1b485544d957d17ce0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671925"
---
# <a name="procurement-and-sourcing-workflows"></a>Beschaffungsworkflows

[!include [banner](../includes/banner.md)]

Einige Organisationen verlangen, dass Bestellanforderungen und Bestellungen von einem Benutzer bestätigt werden, der die Transaktion nicht eingegeben hat. Zum Einrichten eines Genehmigungsprozesses können Sie einen Workflow erstellen.

Ein Workflow stellt einen Geschäftsprozess dar. Ein Workflow definiert, wie ein Dokument das System durchläuft und zeigt an, wer eine Aufgabe abschließen oder ein Dokument genehmigen muss. Die Verwendung des Workflowsystems in der Organisation verspricht mehrere Vorteile:

- **Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Dokumente definieren, z. B. Bestellanforderungen und Spesenabrechnungen. Das Workflowsystem trägt dazu bei, dass Dokumente konsistent und effizient verarbeitet und genehmigt werden.
- **Prozesssichtbarkeit** – Sie können den Status, die Historie und die Leistungskennzahlen einer bestimmten Workflowinstanz nachverfolgen. So können Sie besser feststellen, ob zur Effizienzsteigerung Änderungen am Workflow vorgenommen werden sollten.
- **Zentralisierte Arbeitsliste**- Benutzer können eine zentralisierte Arbeitsliste öffnen, um die Workflowaufgaben und ‑genehmigungen anzuzeigen, die ihnen zu allen Workflows zugewiesen werden, an denen sie teilnehmen. Dies ist in der Arbeitsaufgabenseite verfügbar.

## <a name="the-types-of-workflows-that-you-can-create"></a>Erstellbare Workflowtypen

Die folgenden Workflowtypen stehen für die Beschaffung zur Verfügung.

| Typ | Mit diesem Typ können Sie folgende Aufgaben ausführen: |
|---|---|
| Prüfung der Bestellanforderungen | Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellanforderungen. |
| Prüfung der Bestellanforderungsposition | Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellanforderungspositionen. |
| Bestellworkflow | Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellungen. |
| Bestellpositionsworkflow | Erstellen Sie Prüfungs- und Genehmigungsworkflows für Bestellpositionen. |
| Workflow für Antrag zum Hinzufügen eines Kreditors | Erstellen Sie Prüfungs- und Genehmigungsworkflows zum Hinzufügen neuer Kreditoren über Kreditorenanforderungen. |

> [!IMPORTANT]
> Wenn Sie einen neuen Workflow hinzufügen, werden möglicherweise auch die folgenden veralteten Workflows im Dialogfeld **Workflow erstellen** aufgeführt. Diese beziehen sich auf die *Empfangsbestätigung*-Funktionalität, die in [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows) verfügbar war, die aber jetzt außer Betrieb genommen wurde. Diese Workflows werden derzeit nicht unterstützt.
> 
> - Workflow für Benachrichtigung über Lieferfälligkeit
> - Workflow für Benachrichtigung über Rechnungseingang
> - Workflow für Benachrichtigung über Produktzugangsfehler
> - Workflow für Benachrichtigung über einen abgelehnten, nicht bestätigten Produktzugang

## <a name="creating-a-workflow"></a>Erstellen eines Workflows

Um einen Workflow zu erstellen, wechseln Sie zu Beschaffung &gt; Einrichtung &gt; Beschaffungsworkflows und erstellen Sie einen neuen Workflow, indem sie den Workflowtyp auswählen, den Sie erstellen möchten. 

Auf der Workflowarbeitsfläche können Sie Workflowelemente in den Designer ziehen und die Elemente in einen Fluss verknüpfen. Die Workflowelemente sollten konfiguriert werden. Für Genehmigungs- und Aufgabenworkflowelemente können Sie konfigurieren, welcher Teilnehmer Aktivitäten ausführen soll.

## <a name="types-of-participants"></a>Teilnehmertypen

Sie können folgenden Teilnehmergruppen einen Genehmigungsschritt zuweisen.

| Benutzergruppe | Beschreibung |
|---|---|
| Teilnehmer | Weisen Sie den Genehmigungsschritt den Mitgliedern einer Gruppe oder Rolle zu. |
| Hierarchie | Weisen Sie den Genehmigungsschritt den Benutzern in einer bestimmten Organisationshierarchie zu. |
| Workflowbenutzer | Weisen Sie den Genehmigungsschritt den Benutzern dieses Workflows zu. |
| Warteschlange | Weisen Sie den Genehmigungsschritt einer Warteschlange für Arbeitsaufgaben zu. |
| Benutzer | Weisen Sie den Genehmigungsschritt bestimmten Benutzern zu. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Definieren von geschäftlichen Prozessworkflows für Bestellanforderungen.](https://www.microsoft.com/download/details.aspx?id=101821)
- [Bestellanforderungs-Workflow](purchase-requisitions-workflow.md)
- [Kreditoren aufnehmen](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]