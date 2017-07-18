---
title: Produktdimensionen
description: "Es gibt vier Produktdimensionen: Farbe, Konfiguration, Größe und Farbe. Sie kombinieren Produktdimensionen in den Dimensionsgruppen und weisen diesen Dimensionsgruppen Produktmaster zu. Diese Kombinationen der Produktdimensionen bestimmen, wie Produktvarianten definiert sind."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7e6409db92b929eebca70d6d0176dd9b54a5f9b9
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017

---

# <a name="product-dimensions"></a>Produktdimensionen

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


Es gibt vier Produktdimensionen: Farbe, Konfiguration, Größe und Farbe. Sie kombinieren Produktdimensionen in den Dimensionsgruppen und weisen diesen Dimensionsgruppen Produktmaster zu. Diese Kombinationen der Produktdimensionen bestimmen, wie Produktvarianten definiert sind.

Produktdimensionen sind Merkmale, die dazu dienen, eine Produktvariante zu identifizieren. Sie können Kombinationen der Produktdimensionen verwenden, um Produktvarianten zu definieren. Um eine Produktvariante zu erstellen, müssen Sie mindestens eine Produktdimension für einen Produktmaster definieren.
Produktvarianten
----------------

Produktvarianten werden auch als Artikel bezeichnet. Ein Artikel ist ein materielles Produkt, was ist nicht dasselbe wie eine Dienstleistung ist. Es ist es jedoch auch möglich, einen Produktmaster mit dem Servicetyp zu definieren. Wenn Sie den Typ "Dienstleistung" verwenden, können Sie Produktvarianten angeben, die Dienstleistungen umfassen. So können Sie beispielsweise einen Produktmaster für Beratungsarbeit und Produktvarianten für Arbeit angeben, die von leitenden Beratern und von Juniorberatern ausgeführt wird.

## <a name="product-dimensions"></a>Produktdimensionen
Es gibt die folgenden vier Produktdimensionen: Farbe, Konfiguration, Größe und Farbe. Eine Produktvarianten kann basieren auf Produktdimensionenwerten generiert werden.

Produktdimensionswerte wie Größe, Farbe und Stil können auf den Seiten **Größe**, **Farbe** und **Stil**erstellt werden, auf die an folgenden Orten zugegriffen werden kann: **Produktinformationsverwaltung** &gt; **Einstellungen** &gt; **Dimensions- und Variantengruppen** &gt; **Größen/Farben/Stile**. Produktdimensionswerte für die Variantendimension werden üblicherweise entweder mithilfe des Variantenkonfigurators oder des dimensionsbasierten Konfigurators erstellt. Produktdimensionen können auch auf der Seite **Produktdimensionen** erstellt und verwaltet werden, auf die Sie von folgenden Orten aus zugreifen können:
-   Klicken Sie auf **Produktinformationsverwaltung** &gt; **Produkte** &gt; **Produktmaster.** Klicken Sie im **Aktivitätsbereich** auf **Produktdimensionen.**
-   Klicken Sie auf **Produktinformationsverwaltung** &gt; **Produkte** &gt; **Alle Produkte und Produktmaster.** Wählen Sie einen Produktmaster aus. Klicken Sie im **Aktivitätsbereich** auf **Produktdimensionen.**
-   Klicken Sie auf **Produktinformationsverwaltung** &gt; **Freigegebene Produkte.** Wählen Sie einen Produktmaster aus. Klicken Sie im **Aktivitätsbereich** auf **Produkt**. Klicken Sie in der Gruppe **Produktmaster** auf **Produktdimensionen**.

Die Anzahl von Varianten, die Sie für einen Artikel erstellen können, hängt von der Anzahl der möglichen Produktdimensionskombinationen ab.
| **Tipp**                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wenn Sie ein Produkt beispielsweise auf einer Auftragsposition verwenden, wählen Sie die Produktdimensionen aus, um die Produktvariante zu ermitteln, mit der Sie arbeiten möchten. |

## <a name="example"></a>Beispiel
Ein Unternehmen verkauft Denim-Jeans. Für den Artikel, Jeans, werden die Produktdimensionen "Farbe" und "Größe" verwendet. Die Jeans wird in drei verschiedenen Farben und sechs verschiedenen Größen angeboten. Farben: Blau, Schwarz, Braun. Größen: XS, S, M, L, XL, XXL. Es sind nicht alle Größen in allen drei Farben verfügbar. Wenn alle Kombinationen verfügbar wären, ergäbe dies 18 unterschiedliche Jeanstypen. In diesem Beispiel werden nur die folgenden neun Produktvariantenkombinationen produziert.

| Farbe | Größe |
|-------|------|
| Blau  | XS   |
| Blau  | So    |
| Blau  | Mo    |
| Schwarz | Mo    |
| Schwarz | L    |
| Schwarz | XL   |
| Braun | L    |
| Braun | XL   |
| Braun | XXL  |






