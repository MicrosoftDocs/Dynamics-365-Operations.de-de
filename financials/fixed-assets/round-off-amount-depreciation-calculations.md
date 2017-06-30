---
title: "Betrag der Rundung für Abschreibungsberechnungen"
description: "Dieser Artikel erläutert das Feld \"Rundungsart Abschreibung\", das Sie im Wertmodell und auf den Einstellungsseiten des Abschreibungsbuchs finden."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8d5a9d9267c14ee045388c3b3b42b26f2fff45ea
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="round-off-amount-for-depreciation-calculations"></a>Betrag der Rundung für Abschreibungsberechnungen

[!include[banner](../includes/banner.md)]


Dieser Artikel erläutert das Feld "Rundungsart Abschreibung", das Sie im Wertmodell und auf den Einstellungsseiten des Abschreibungsbuchs finden.

Rundungsart Abschreibungbeträge werden für jedes Buch festgelegt. Gerundete Abschreibungsbeträge werden im Anlagenabschreibungsprofil, das die zukünftige Abschreibung und den Wert der Anlage anzeigt, sowie in den Abschreibungsvorschlägen verwendet. Den niedrigsten Abschreibungsbetrag eingeben, der für dieses Buch zulässig ist. 

Unabhängig von der eingerichteten Rundung wird der Abschreibungsbetrag im letzten Abschreibungszeitraum nicht gerundet. Am Ende des letzten Abschreibungszeitraums muss der Wert der Anlage 0 (Null) oder der Schrottwert sein, wenn Schrottwert verwendet wird.

### <a name="example"></a>Beispiel

Die Abschreibung ohne Rundung beträgt 2.444,44. Wie die folgende Tabelle zeigt, sind die vorgeschlagenen Beträge unterschiedlich, abhängig davon, wie die Rundung eingerichtet wurde.

| Rundungsmethode | Abschreibungsbetrag |
|-----------------|---------------------|
| Rundung 0,1    | 2.444,40            |
| Rundung 1,00   | 2.444,00            |
| Rundung 10,00  | 2.440,00            |
| Rundung 100,00 | 2.400,00            |






