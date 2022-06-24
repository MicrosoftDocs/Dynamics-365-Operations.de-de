---
title: Betrag der Rundung für Abschreibungsberechnungen
description: Dieser Artikel erläutert das Feld "Rundungsart Abschreibung", das Sie im Wertmodell und auf den Einstellungsseiten des Abschreibungsbuchs finden.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a93842f7cca483df89188695c945edf77e118cef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870103"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Betrag der Rundung für Abschreibungsberechnungen

[!include [banner](../includes/banner.md)]

Dieser Artikel erläutert das Feld **Rundungsart Abschreibung**, das Sie im Wertmodell und auf den **Einstellungsseiten** des Abschreibungsbuchs finden.

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







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
