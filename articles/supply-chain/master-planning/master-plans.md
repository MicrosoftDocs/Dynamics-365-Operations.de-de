---
title: Übersicht Masterpläne
description: Zur Unterstützung der täglichen Arbeitsabläufe Ihres Unternehmens, zum Simulieren unterschiedlicher Planungsstrategien, die überwacht werden sollen, und zum Implementieren einer Unternehmensrichtlinie, z. B. eine Richtlinie für die interne Leistung oder die Kundenzufriedenheit, können Sie verschiedene Produktprogrammpläne einrichten und verwenden.
author: t-benebo
ms.date: 05/28/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b3d30d9ef2f08c2cb7b2ca022ff1a816567a247
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468748"
---
# <a name="master-plans-overview"></a>Übersicht Masterpläne

[!include [banner](../includes/banner.md)]

Zur Unterstützung der täglichen Arbeitsabläufe Ihres Unternehmens, zum Simulieren unterschiedlicher Planungsstrategien, die überwacht werden sollen, und zum Implementieren einer Unternehmensrichtlinie, z. B. eine Richtlinie für die interne Leistung oder die Kundenzufriedenheit, können Sie verschiedene Produktprogrammpläne einrichten und verwenden.

Sie können Produktprogrammpläne auf der Seite **Produktprogrammpläne** konfigurieren.

Es gibt zwei Arten von Plänen:

- **Statischer Produktprogrammplan** – Bei der Kalkulation im Produktprogrammplanungslauf werden die aktuellen Daten zum Generieren von Bedarfsverlaufsplänen verwendet. Dieser Plan bleibt bis zur nächsten Ausführung eines Produktprogrammplanungslaufs oder einer manuelle Planänderung unverändert. Dies ist ein Betriebsablaufplan, den verschiedene Mitarbeiter wie (Einkäufer oder Produktionsplaner) verwenden können, um informierte Entscheidungen zu treffen und um ihre täglichen Aufgaben und Aktivitäten auszuführen.
- **Dynamischer Produktprogrammplan** – Dieser Plan setzt auf dem gleichen Bedarfsverlaufsplan auf, der im Produktprogrammplanungslauf generiert wurde. Der dynamische Plan kann allerdings jederzeit aktualisiert werden, wenn sich die Stammdaten ändern. Dieser Fall könnte z. B. eintreten, wenn ein neuer Auftrag erstellt wird. Hiermit sind Sie in der Lage, das sich ändernde Auftragsnetzwerk und die Artikelverfügbarkeit zu überwachen, ohne den statischen Plan zu stören, den andere Personen für ihre Arbeitsprozesse benötigen.

Ein Unternehmen kann nur mit einem dynamischen Produktprogrammplan oder mit statischen und dynamischen Plänen arbeiten. Darüber hinaus kann jeder Produktprogrammplan so konfiguriert werden, dass er eine bestimmte Strategie oder ein Problem berücksichtigt. Beispiele:

- Legen Sie höhere Lagerbestände fest, um Fehlbestände zu verhindern.
- Legen Sie höhere Sicherheitszuschläge fest, um sich gegen unzuverlässige Lieferanten abzusichern.

Der anfängliche dynamische Produktprogrammplan kann auch so eingerichtet werden, dass er bei jedem Produktprogrammplanungslauf mit dem neuen Bedarfsverlaufsplan aktualisiert wird. Sie können diese Einstellungen auf der Seite **Produktprogrammplanungsparameter** angeben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Deckungseinstellungen](coverage-settings.md)
- [Taktische und Betriebsplanung für den Produktprogrammplanungslauf trennen](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [Produktprogrammplanung: Verwenden eines statischen und dynamischen Produktprogrammplan oder verwenden Sie einen Plan?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
