---
title: "Aktualisieren der Standardkosten in einer Umgebung ohne Produktionstätigkeit"
description: "Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 472b977dcffb4cadb91621586763e0fd471d5c46
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Aktualisieren der Standardkosten in einer Umgebung ohne Produktionstätigkeit

[!include[banner](../includes/banner.md)]


Dieser Artikel bietet eine Anleitung zum Aktualisieren von Standardkosten in einer Umgebung ohne Produktionstätigkeit.

Für die folgenden Richtlinien wird die Verwendung des Zwei-Versionen-Ansatzes für Standardkostenaktualisierungen vorausgesetzt. Hierbei enthält eine der Nachkalkulationsversionen die ursprünglich definierten Standardkosten für die unveränderliche Periode, während die andere Nachkalkulationsversion die stufenweisen Aktualisierungen beinhaltet. Jede Aktualisierung wird als Kostendatensatz innerhalb der zweiten Nachkalkulationsversion eingegeben und schließlich aktiviert. Eine alternative Lösung stellt der Einzelversionsansatz dar, bei dem die ursprünglich definierte Gruppe von Standardkosten verwendet wird. Für den Zwei-Versionen-Ansatz müssen Sie eine zweite Nachkalkulationsversion definieren. Nachfolgend finden Sie die Richtlinien zur Definition dieser Nachkalkulationsversion:

-   Weisen Sie den Nachkalkulationstyp **Standardkosten** zu.
-   Weisen Sie eine aussagekräftige Kennung zu, die Aufschluss über den Zweck der Nachkalkulationsversion gibt, wie z. B. **2016-AKTUALISIERUNGEN**.
-   Stellen Sie sicher, dass der Inhalt Kostendatensätze einschließt.
-   Ermöglichen Sie die Eingabe von Kostendatensätzen für alle Standorte. Durch Angabe eines Standorts können Kostendatensätze nur für diesen Standort eingegeben werden.
-   Geben Sie als Fallback-Prinzip den Wert **Kein** an. Das Fallback-Prinzip wird ausschließlich auf Kostenberechnungen für produzierte Artikel angewendet.

Gehen Sie zum Korrigieren, Regulieren oder Aktualisieren der Standardkosten für neue Artikel folgendermaßen vor.

1.  Verwenden Sie die Seite **Nachkalkulationsversion** **Einstellungen**, um die Eingabe von Kostendaten in die zweite Nachkalkulationsversion zu aktivieren. Sperren Sie optional die Aktivierung ausstehender Kosten, sodass eine Aktivierung erst möglich ist, nachdem die ausstehenden Kosten vollständig und exakt definiert wurden. Sie können auch optional ein Datum im Feld **Von Datum** eingeben. Allgemeine Richtlinie: Geben Sie das Datum an, an dem die stufenweisen Aktualisierungen voraussichtlich aktiviert werden. Alternative: Lassen Sie das Feld **Von Datum** für die Nachkalkulationsversion leer, und geben Sie anschließend im Feld **Von Datum** für jeden Kostendatensatz ein Datum ein.
2.  Geben Sie mithilfe der Seite **Artikelpreis** Aktualisierungen als Artikelkostendatensätze in der zweiten Nachkalkulationsversion ein.
3.  Prüfen Sie mithilfe des Berichts **Artikelpreis** die Artikelkostendatensätze in der zweiten Nachkalkulationsversion auf Vollständigkeit und Richtigkeit.
4.  Ändern Sie mithilfe der Seite **Verwaltung der Nachkalkulationsversion** die Sperrmarkierung, um in der zweiten Nachkalkulationsversion die Aktivierung von Datensätzen für ausstehende Kosten zu ermöglichen.
5.  Verwenden Sie die Seite **Preise aktivieren** (die Sie über die Seite **Verwaltung der Nachkalkulationsversion** öffnen), um alle ausstehenden Artikelkostendatensätze in der zweiten Nachkalkulationsversion zu aktivieren. Die Datensätze mit ausstehenden Kosten können auch für einzelne Artikel aktiviert werden, indem Sie auf der Seite **Artikelkosten** auf die Schaltfläche **Ausstehende Preise aktivieren** klicken.
6.  Mithilfe der Seite **Einstellungen für Nachkalkulationsversion** können Sie die Sperrmarkierungen in der zweiten Nachkalkulationsversion ändern, um eine weitere Datenverwaltung zu verhindern. Durch die Sperrrichtlinien werden die Eingabe neuer ausstehender Kosten sowie die Aktivierung ausstehender Kosten verhindert.





