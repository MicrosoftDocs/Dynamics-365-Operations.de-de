---
title: "Anzeigen von Belastungen für einen produzierten Artikel"
description: "Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 119f49d9456c49b1e010da1e0b2c52e369164344
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="display-charges-for-a-manufactured-item"></a>Anzeigen von Belastungen für einen produzierten Artikel

[!include[banner](../includes/banner.md)]


Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert.

Der berechnete Betrag der Belastungen eines Artikels kann zusammen mit den Einheitenkosten des Artikels angezeigt werden. Manchmal werden die Belastungen jedoch auch als separate Felder angezeigt und nicht in die Einheitenkosten des Artikels einbezogen. Werden die Belastungen als separate Felder angezeigt, enthält eines der Felder den Gesamtbetrag der Belastungen und ein anderes Feld die Losgröße für die Nachkalkulation, die zur Amortisierung des Betrags verwendet wurde. Die Artikelpreisseite, zum Beispiel zeigt die Belastungen als zwei separate Felder. Die Seite Abgeschlossen zeigt dagegen die Gesamtkosten des Artikels pro Einheit und die amortisierten Kosten sind bereits in den Einheitenkosten enthalten.
Die Belastungen für einen produzierten Artikel werden zum Zwecke der Standardkosten immer in die Einheitenkosten des Artikels einbezogen. Sie können optional auch in geplante Kosten einbezogen werden. Die Einbeziehung der Belastungen in die Kosten eines produzierten Artikels wird durch eine Richtlinie in der Nachkalkulationsversion erzwungen. Durch die Aktivierung des Kostendatensatzes eines Artikels werden die Belastungen in den im Formular  angezeigten Basiskosteninformationen des Artikels aktualisiert. Die Belastungen werden in zwei separaten Feldern angezeigt und nicht in die Einheitenkosten des Artikels einbezogen. Bei jeder Aktivierung werden die Grundkosteninformationen des Artikels aktualisiert. Dies gilt auch, wenn durch die Aktivierung unterschiedliche Standorte berücksichtigt werden. Aus diesem Grund dürfen die Grundkosteninformationen lediglich als Referenzinformationen betrachtet werden.






