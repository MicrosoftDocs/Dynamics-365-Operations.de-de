---
title: Übersicht über Kredit und Inkasso
description: In diesem Thema erhalten Sie einen Überblick über die Funktion für Kredit und Inkasso.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ade76b822904f49135e07dfe0a39d2227dd1dd77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992987"
---
# <a name="credit-and-collections-overview"></a>Übersicht über Kredit und Inkasso

[!include [banner](../includes/banner.md)]

Sie können Kreditlimits für Ihre Kreditoren verwalten und bei Bedarf Inkassotätigkeiten ausführen.

## <a name="credit-management"></a>Kreditverwaltung

Mit dem Kundenkreditmanagement können Sie Kreditlimits verwalten und den Fluss von Aufträgen während des Buchungsprozesses auf der Grundlage der von Ihnen erstellten Kreditregeln steuern.

Der Kreditverwaltungsprozess kann einen der folgenden Schritte umfassen:

- Aktualisieren Sie die Kreditattribute für Kreditoren, um zusätzliche Informationen zu ihrer Kreditwürdigkeit bereitzustellen.
- Erstellen Sie Kreditlimits für Kreditoren mithilfe von Kreditlimitanpassungen.
- Erstellen Sie temporäre Kreditlimits für Kreditoren mithilfe von Kreditlimitanpassungen. Auf diese Weise können Sie das Kundenkreditlimit vorübergehend je nach Geschäftsanforderungen erhöhen oder verringern.
- Fügen Sie Informationen hinzu, die sich auf das Kreditlimit auswirken können, z. B. Informationen zu Versicherungen und Garantien.
- Erstellen Sie Debitorenkreditgruppen, die Kunden so miteinander verknüpfen, dass sie ein einziges Kreditlimit teilen.
- Weisen Sie den Debitoren Risikobewertungen zu und verwenden Sie diese, um automatisch Kreditlimits für diese Debitoren durch Kreditlimitanpassungen zu generieren.
- Erstellen Sie Sperrregeln, die einen Auftrag während eines oder mehrerer Buchungsvorgänge zurückstellen, basierend auf Faktoren wie Risiko, Zahlungsbedingungen, Kreditlimits, überfälligen Beträgen und dem Prozentsatz des verwendeten Kreditlimits.
- Verwalten Sie eine Liste zurückgestellter Kundenaufträge, überprüfen Sie die Gründe für die Zurückstellung und beheben Sie Probleme.
- Geben Sie Aufträge frei, damit sie den Buchungsprozess durchlaufen.
- Richten Sie einen Workflow ein, um die Genehmigung von Kreditlimitänderungen und Kundenauftragsfreigaben zu verwalten.

## <a name="collections-management"></a>Inkassoverwaltung

Informationen zu Debitoreninkassi werden in einer zentralen Ansicht auf der Seite **Inkassi** verwaltet. Bearbeiter von Inkassovorgängen können diese zentrale Ansicht zum Verwalten von Inkassi verwenden. Inkassobeauftragte können den Inkassovorgang entweder über Debitorenlisten beginnen, die unter Verwendung vordefinierter Kriterien generiert werden, oder über die Seite **Debitoren**.

Bevor Sie mit dem Einrichten oder Verwenden von Inkassovorgängen beginnen, sollten Sie über Folgendes informiert sein:

- Fälligkeitsmomentaufnahmen zu Debitoren enthalten Saldorückblickinformationen zu einem bestimmten Zeitpunkt.
- Debitorenpools für Inkassi unterstützen Sie beim Organisieren Ihrer Arbeit.
- Inkassobeauftragte können über eigene Debitorenpools verfügen.
- Auf Listenseiten werden Debitoren, Aktivitäten und Anfragen organisiert.
- Alle Inkassoinformationen für einen Debitor befinden sich auf einer Seite, und Sie können über diese Seite Aktionen ausführen.
- Sie können Zinsen und Gebühren in einem Schritt erheben, wieder erheben oder stornieren.
- Abschreibungsbuchungen können in einem Schritt erstellt werden.
- Zahlungen mit unzureichender Deckung (NSF) können in nur einem Schritt verarbeitet werden.

Beschreibungen dieser Konzepte finden Sie unter [Schlüsselkonzepte für die Sammlungsverwaltung](./cm-collections-concepts.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Einrichtung der Parameter für das Kundenkreditmanagement](./cm-credit-mgmt-setup.md)

[Einrichtung der Informationen für das Kundenkreditmanagement](./cm-setup-information.md)

[Hinzufügen der Informationen für das Kundenkreditmanagement](./cm-add-credit-mgmt-information-customer.md)

[Debitorenkreditgruppen](./cm-customer-credit-groups.md)

[Debitorenkreditlimitregulierungen](./cm-credit-limit-adjustments.md)

[Kreditsperren für Aufträge](./cm-sales-order-credit-holds.md)

[Periodische Aufgaben des Kundenkreditmanagements](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]