---
title: "Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel"
description: "In diesem Thema werden die Schritte zur Vorbereitung der Kostenverwaltung für produzierte Artikel beschrieben."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: c1942d1f2c8eeb05a6cbaddd2d7911a93b7e05a1
ms.contentlocale: de-de
ms.lasthandoff: 03/07/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel

[!include[banner](../includes/banner.md)]

In diesem Thema werden die Schritte zur Vorbereitung der Kostenverwaltung für produzierte Artikel beschrieben. Die Schritte für produzierte Artikel unterscheiden sich etwas von den Schritten für eingekaufte Artikel.

Richtlinien, die produzierten Artikeln zugewiesen sind, können sich auf die Kostenberechnungen für die übergeordneten produzierten Artikel auswirken. Gehen Sie zur Vorbereitung der Kostenverwaltung für produzierte Artikel folgendermaßen vor.

1. Weisen Sie dem produzierten Artikel eine Artikelmodellgruppe zu. 

   Die Artikelmodellgruppe bestimmt, dass Standardkosten verwendet werden.

2. Weisen Sie dem produzierten Artikel eine Artikelgruppe zu. 

   Die Artikelgruppe enthält Sachkonten für den produzierten Artikel. Die Sachkonten für einen produzierten Artikel mit einem Lagermodell vom Typ „Standardkosten” umfassen mehrere Produktionsabweichungen sowie die Abweichung bei Kostenänderung und die Neubewertung der Lagerkosten.

3. Weisen Sie dem Artikel die Lagermaßeinheit zu. 

   Die Kosten des Artikels werden stets in der Lagermaßeinheit des Artikels ausgedrückt.

4. Weisen Sie dem produzierten Artikel nur dann eine Kostengruppe zu, wenn der Artikel als eingekaufter Artikel behandelt wird.

5. Weisen Sie dem produzierten Artikel eine Stücklisten-Berechnungsgruppe zu. 

   Durch die Stücklisten-Berechnungsgruppe des Artikels werden Warnbedingungen definiert, die gelten. Dadurch können, wenn eine Stücklistenberechnung erfolgt, Warnmeldungen über mögliche Quellen von Berechnungsfehlern generiert werden. So kann beispielsweise durch eine Warnmeldung darauf hingewiesen werden, dass keine aktive Stückliste oder kein aktiver Arbeitsplan vorhanden ist. Die Stücklisten-Kalkulationsgruppe enthält eine Richtlinie vom Typ „Stücklistenauflösung beenden”, durch die angegeben wird, wann ein produzierter Artikel als eingekaufter Artikel behandelt werden soll.

6. Wenn der produzierte Artikel konstante Kosten aufweist, weisen Sie ihm eine Standardauftragsmenge zu. 

   Die Standardauftragsmenge fungiert als Abrechnungspostengröße für die Amortisierung konstanter Kosten. Beispiele der konstanten Kosten umfassen Rüstzeiten bei Routingarbeitsgängen und eine konstante Komponentenmenge in der Stückliste.

7. Definieren Sie die Stückliste für den produzierten Artikel. 

   Für den produzierten Artikel können mehrere Stücklistenversionen definiert werden. Vergewissern Sie sich, dass die gewünschten Versionen als „Genehmigt” und „Aktiv” markiert sind und das gewünschte Gültigkeitsdatum besitzen. Die Stücklistenversion kann als unternehmensweite oder als standortspezifische Version verwendet werden.

8. Definieren Sie den Arbeitsplan für den produzierten Artikel. 

   Für den produzierten Artikel können mehrere Arbeitsplanversionen definiert werden. Vergewissern Sie sich, dass die gewünschten Versionen als „Genehmigt” und „Aktiv” markiert sind und das gewünschte Gültigkeitsdatum besitzen. Die Arbeitsplanversion muss standortspezifisch sein.

Wenn Sie Routinginformationen für die Nachkalkulation verwenden möchten, sind weitere Vorbereitungen erforderlich. So muss beispielsweise sichergestellt werden, dass die dem Arbeitsgang des Arbeitsplans zugewiesenen Kostenkategorien korrekt und vollständig sind.

<a name="related-topics"></a>Verwandte Themen
--------

[Amortisierung konstanter Kosten für einen produzierten Artikel](amortize-constant-costs-manufactured-item.md)

[Einrichten von Produkten, die produziert werden oder beschafft werden](manufactured-items-treated-as-purchased-items.md)


