---
title: Kostenkategorien in Produktionsarbeitsplänen
description: Dieser Artikel bietet Informationen über Kostenkategorien, die für Produktionsumgebungen gelten, die Arbeitspläne verwenden.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca4c0c9cecb79366cdd41069cb6c96f01b44a2094f4caf57077c391beb6ac106
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779685"
---
# <a name="cost-categories-used-in-production-routing"></a>Kostenkategorien in Produktionsarbeitsplänen

[!include [banner](../includes/banner.md)]

Dieser Artikel bietet Informationen über Kostenkategorien, die für Produktionsumgebungen gelten, die Arbeitspläne verwenden.

Kostenkategorien gelten für Produktionsumgebungen mit Arbeitsplänen. Sie werden betrieblichen Ressourcen und Arbeitsgängen des Arbeitsplans zugewiesen, um Stundenkosten zu definieren und Kostenbeiträge in den berechneten Kosten eines produzierten Artikels zu segmentieren. Die Produktionskostenbeiträge durch die Kostengruppen, die Kostenkategorien zugewiesen sind, werden nach betrieblicher Ressource und Aktivitätstyp (beispielsweise Rüst- und Bearbeitungszeit) klassifiziert. Die Genauigkeit der Kostengruppenzuweisung erlaubt die Berechnung von Produktionsgemeinkosten auf Basis von Arbeitsplaninformationen. 

**Hinweis:** Kostenkategorien besitzen innerhalb von Produktionsumgebungen eine Vielzahl unterschiedlicher Bezeichnungen wie "Arbeitssatzcodes" oder "Maschinensatzcodes". 

Jede Kostenkategorie besitzt zugeordnete Kostendatensätze sowie eine zugewiesene Kostengruppe. Für unterschiedliche Produktionszwecke werden unterschiedliche Kostenkategorien benötigt.

-   Weisen Sie abhängig von der betrieblichen Ressource unterschiedliche Stundenkosten zu. Beispielsweise können sich die Kosten für verschiedene Arten von Arbeitsqualifikationen, Maschinen oder Produktionszellen unterscheiden.
-   Weisen Sie für die Rüst- oder Bearbeitungszeit, die einem Arbeitsgang des Arbeitsplans zugeordnet ist, andere Stundenkosten zu.
-   Weisen Sie anstelle der Stundenkosten Kosten für betriebliche Ressourcen auf Basis der Ausgabemenge, beispielsweise Stücksätze für Lohnzahlungen, zu.
-   Geben Sie die Kostensegmentierung in den berechneten Kosten des übergeordneten produzierten Artikels an. So können Sie beispielsweise aus den Arbeits- und Maschinenkosten Kosten segmentieren.
-   Geben Sie die Grundlage für die Kostengruppe für Gemeinkostenberechnungsformeln an – beispielsweise Formeln für arbeitsbezogene und maschinenbezogene Gemeinkosten oder Gemeinkosten, die sich auf Rüst- und Ausführungszeiten beziehen.

Eine Kostenkategorie kann der Rüstzeit, der Verarbeitungszeit sowie der Menge für einen Arbeitsplanvorgang zugewiesen werden. Ergibt sich beispielsweise für die Kosten oder die Kostengruppensegmentierung eine Abweichung zwischen Rüst- und Bearbeitungszeit, müssen unterschiedliche Kostenkategorien in der Rüst- und Bearbeitungszeit definiert und zugewiesen werden. Die selektive Verwendung von Kostenkategorien für Rüstzeit, Bearbeitungszeit und Menge wird durch die Arbeitsplangruppe bestimmt, die einem Arbeitsgang zugewiesen ist. Die Zuweisung von Kostenkategorien zu Zeit und Menge kann auf Basis unternehmensweiter Richtlinien, die im Formular **Produktionssteuerungsparameter** definiert sind, vorgegeben werden. 

Jede Kostenkategorie verfügt über zugeordnete Kosten, die auf der Definition von Kostendatensätzen innerhalb einer Nachkalkulationsversion basieren. Definieren Sie im Formular **Kostenkategoriepreis** die Kostendatensätze für eine angegebene Nachkalkulationsversion und einen Standort. Wenn der Kostendatensatz für eine Kostenkategorie erstmalig eingegen wird, ist der Status **Ausstehend** sowie mit einem vorgesehenen Gültigkeitsdatum eingegeben. Bei Aktivierung des Kostendatensatzes wird der Status zu **Zurzeit aktiv** und das Gültigkeitsdatum in das Aktivierungsdatum aktualisiert. Unterschiedliche Kostendatensätze können für unterschiedliche Standorte, Gültigkeitsdaten oder Status stehen. Für Stücklistkostenkalkulationen zu einem späteren oder früheren Datum verwenden Sie die Kostendatensätze mit dem entsprechenden Gültigkeitsdatum. Der zurzeit aktive Kostendatensatz wird für die Vorkalkulation von Kosten für Produktionsaufträge sowie zur Bewertung der gemeldeten Zeit für einen Produktionsauftrag verwendet. 

Der Kostendatensatz für eine Kostenkategorie kann sich auf einen bestimmten Standort oder das gesamte Unternehmen beziehen. Um standortspezifische Kostendatensätze zu erstellen, weisen Sie ihm einen Standort zu. Ist kein Wert angegeben, gilt der Kostendatensatz innerhalb des Unternehmens für alle Standorte. Da Kosten sich beispielsweise je nach Standort unterscheiden können, müssen die Kostendatensätze als standortspezifisch definiert werden. 

Von einem Arbeitsgang des Arbeitsplan werden in der Regel die Kostenkategorien, die dem Arbeitsgang für betriebliche Ressourcen oder dem Masterarbeitsgang zugewiesen sind, übernommen. Bei der Erstellung eines Produktionsauftrags wird die ausgewählte Arbeitsplanversion durch die Arbeitsgänge des Arbeitsplans innerhalb des Produktionsarbeitsplans widergespiegelt. Die Kostenkategorien, die den Arbeitsgängen im Produktionsarbeitsplan zugewiesen sind, können außer Kraft gesetzt werden. 

Bestimmte Arten von Produktionsarbeiten beziehen sich auch auf Vorkalkulationen und Berichte in Bezug auf den Projektzeitaufwand. In diesem Fall ist eine Kostenkategorie für die Produktion und die Projektzwecke erforderlich. Sie müssen zusätzlich projektbezogene Informationen definieren, wenn eine Kostenkategorie für die Verwendung in Projekten gekennzeichnet ist.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]