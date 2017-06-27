---
title: "Standardkosten für einen neuen produzierten Artikel aktualisieren"
description: "Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten für einen neuen produzierten Artikel."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d8f1b5614811faad3fda15809e4e606c93e6b786
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Standardkosten für einen neuen produzierten Artikel aktualisieren

[!include[banner](../includes/banner.md)]


Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten für einen neuen produzierten Artikel. 

Für die folgenden Richtlinien wird die Verwendung des Zwei-Versionen-Ansatzes für Standardkostenaktualisierungen vorausgesetzt. Bei diesem Ansatz enthält eine der Nachkalkulationsversionen die ursprünglich definierten Standardkosten für die unveränderliche Periode, während die andere Nachkalkulationsversion die stufenweisen Aktualisierungen für die neu produzierten Artikel enthält. Die stufenweisen Aktualisierungen werden als Kostendatensätze in der zweiten Nachkalkulationsversion eingeben und schließlich aktiviert. Für den Zwei-Versionen-Ansatz müssen Sie eine zweite Nachkalkulationsversion definieren. Nachfolgend finden Sie die Richtlinien zur Definition dieser Nachkalkulationsversion:

-   Weisen Sie den Nachkalkulationstyp **Standardkosten** zu.
-   Weisen Sie eine aussagekräftige Kennung zu, die Aufschluss über den Zweck der Nachkalkulationsversion gibt, wie z. B. **2016-AKTUALISIERUNGEN**.
-   Überprüfen Sie, ob in der Feldgruppe **Preistyp zulassen** der **Einstandspreis** auf **Ja** festgelegt ist.
-   Kostendatensätze müssen für jeden Standort eingegeben werden können (lassen Sie daher das Feld **Standort**leer). Durch Angabe eines Standorts können Kostendatensätze nur für diesen Standort eingegeben werden.
-   Verwenden Sie das Fallback-Prinzip **Aktiv**.

Führen Sie die folgenden Schritte aus, um innerhalb der unveränderlichen Periode neue produzierte Artikel hinzuzufügen.

1.  Verwenden Sie die Seite **Einstellungen für Nachkalkulationsversion**, um die Eingabe von Kostendatensätzen in die zweite Nachkalkulationsversion zu aktivieren, die stufenweise Aktualisierungen enthält. Sperren Sie die Aktivierung ausstehender Kosten. Die Aktivierung ist wieder zulässig, nachdem die ausstehenden Kosten vollständig und exakt definiert wurden. Geben Sie als Richtlinie in der Nachkalkulationsversion kein Anfangsdatum an, sondern geben Sie das Anfangsdatum bei der Eingabe der einzelnen Kostendatensätze ein. Das Anfangsdatum muss vor dem Zeitpunkt liegen, zu dem die neuen Artikel eingekauft oder produziert werden.
2.  Geben Sie auf der Seite **Artikelpreis** Kostendatensätze für neue eingekaufte Artikel ein. Geben Sie für jeden Kostendatensatz die Nachkalkulationsversion mit den stufenweisen Aktualisierungen ein, und verwenden Sie ein Anfangsdatum, das vor dem voraussichtlichen Herstellungsdatum für neue produzierte Artikel liegt.
3.  Berechnen Sie mithilfe der Seite **Berechnung** die Kosten für neue produzierte Artikel. Öffnen Sie die Seite **Berechnung** über die Seite **Verwaltung der Nachkalkulationsversion** und wählen Sie hier die Nachkalkulationsversion mit den stufenweisen Aktualisierungen aus. Geben Sie mithilfe der Auswahlkriterien den neuen produzierten Artikel sowie dessen produzierte Komponenten an. In einer Produktstruktur mit mehreren Ebenen müssen möglicherweise auch übergeordnete Artikel angegeben werden, die die neuen produzierten Artikel als Komponente enthalten. Geben Sie als Anfangsdatum für die Herstellkostenkalkulation den Produktionsbeginn für die neuen produzierten Artikel ein. Das Anfangsdatum muss innerhalb der Gültigkeitsdaten für die Stücklisten- und für die Arbeitsplanversion des Artikels liegen. **Hinweis:** Ein fehlender Kostendatensatz kann auf einen neuen produzierten Artikel hindeuten. Herstellkostenkalkulationen lassen sich auf Artikel mit fehlenden Kosten beschränken.
4.  Überprüfen Sie die Vollständigkeit und die Richtigkeit der für den neuen produzierten Artikel berechneten Kosten. Mithilfe der Seite **Abgeschlossen** können Sie die berechneten Kosten der einzelnen Artikelkostendatensätze sowie alle möglicherweise vorhandenen Infologs mit Warnmeldungen überprüfen. Alternativ können die berechneten Kosten auf der Seite **Berechnung** überprüft werden.
5.  Ändern Sie mithilfe der Seite **Einstellungen für Nachkalkulationsversion** die Sperrmarkierung, um in der zweiten Nachkalkulationsversion die Aktivierung von Datensätzen für ausstehende Kosten zu ermöglichen.
6.  Verwenden Sie die Seite **Preise aktivieren** (die Sie über die Seite **Verwaltung der Nachkalkulationsversion** öffnen), um alle ausstehenden Artikelkostendatensätze in der zweiten Nachkalkulationsversion zu aktivieren. Die Datensätze mit ausstehenden Kosten können auch für einzelne Artikel aktiviert werden, indem Sie auf der Seite **Artikelkosten** auf die Schaltfläche **Aktivieren** klicken.
7.  Mithilfe der Seite **Einstellungen für Nachkalkulationsversion** können Sie die Sperrmarkierungen in der zweiten Nachkalkulationsversion ändern, um eine weitere Datenverwaltung zu verhindern. Durch die Sperrrichtlinien werden die Eingabe neuer ausstehender Kosten sowie die Aktivierung ausstehender Kosten verhindert.





