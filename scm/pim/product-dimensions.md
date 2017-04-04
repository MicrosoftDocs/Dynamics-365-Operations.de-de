---
title: Produktdimensionen
description: "Es gibt vier - Produktdimensionen Farbe, Variante, Größe und Stil. Sie kombinieren Produktdimensionen in den Dimensionsgruppen und weisen diesen Dimensionsgruppen Produktmaster zu. Diese Kombinationen der Produktdimensionen bestimmen, wie Produktvarianten definiert sind."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8854ab94a71cc363bcd073d2df47bc01a243b6cd
ms.lasthandoff: 03/31/2017


---

# <a name="product-dimensions"></a>Produktdimensionen

Es gibt vier - Produktdimensionen Farbe, Variante, Größe und Stil. Sie kombinieren Produktdimensionen in den Dimensionsgruppen und weisen diesen Dimensionsgruppen Produktmaster zu. Diese Kombinationen der Produktdimensionen bestimmen, wie Produktvarianten definiert sind.

Produktdimensionen sind Merkmale, die dazu dienen, eine Produktvariante zu identifizieren. Sie können Kombinationen der Produktdimensionen verwenden, um Produktvarianten zu definieren. Um eine Produktvariante zu erstellen, müssen Sie mindestens eine Produktdimension für einen Produktmaster definieren.
Produktvarianten
----------------

Produktvarianten werden auch als Artikel bezeichnet. Ein Artikel ist ein materielles Produkt, was ist nicht dasselbe wie eine Dienstleistung ist. Es ist auch möglich, einem Produktmaster mit den Dienstleistungstyp zu definieren. Wenn Sie den Typ "Dienstleistung" verwenden, können Sie Produktvarianten angeben, die Dienstleistungen umfassen. So können Sie beispielsweise einen Produktmaster für Beratungsarbeit und Produktvarianten für Arbeit angeben, die von leitenden Beratern und von Juniorberatern ausgeführt wird.

## <a name="product-dimensions"></a>Produktdimensionen
Die folgenden Produktdimensionen sind verfügbar: Konfiguration, Größe, Farbe und Stil. Produktvariante Eine kann auf der Produktdimensionswerte generiert werden.

Produktdimensionswerte beispielsweise Größe, Farbe und Stil können auf ** ** ** Größe, Farbe und Stil ** ** ** Seiten erstellt werden, die von den folgenden Positionen aus zugegriffen werden kann: ** Produktinformationsverwaltung ** ** &gt; Einstellungen ** ** &gt; Dimensions-und Variante Gruppen ** ** &gt; Größen und Farben oder Stile **. Produktdimensionswerte für die Variantendimension werden üblicherweise entweder mithilfe des Variantenkonfigurators oder des dimensionsbasierten Konfigurators erstellt. Produktdimensionen können auch auf der Seite **Produktdimensionen** erstellt und verwaltet werden, auf die Sie von folgenden Orten aus zugreifen können:
-   Produktinformationsverwaltung auf ** ** ** &gt; Produkte ** ** &gt; Produktmaster **. Im Aktivitätsbereich ** **, auf ** Produktdimensionen **.
-   Produktinformationsverwaltung auf ** ** ** &gt; Produkte ** ** &gt; alle Produkte und Produktmaster **. Wählen Sie einen Produktmaster aus. Im Aktivitätsbereich ** **, auf ** Produktdimensionen **.
-   Produktinformationsverwaltung auf ** ** ** &gt; freigegebene Produkte **. Wählen Sie einen Produktmaster aus. Im Aktivitätsbereich ** **, auf ** Produkt **. Klicken Sie in der Gruppe **Produktmaster** auf **Produktdimensionen**.

Die Anzahl von Varianten, die Sie für einen Artikel erstellen können, hängt von der Anzahl der möglichen Produktdimensionskombinationen ab.
| **Tipp **                                                                                                                                              |
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




