---
title: Solver-Strategie für Produktkonfiguration
description: In diesem Thema wird beschrieben, wie Sie die Solver-Strategie verwenden können, um die Leistung der Produktkonfiguration zu verbessern.
author: cvocph
manager: tfehr
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb0fc054e0feec4c54c0bd916e01ce3a2a4cd903
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986550"
---
# <a name="solver-strategy-for-product-configuration"></a>Solver-Strategie für Produktkonfiguration

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Solver-Strategie verwenden können, um die Leistung der Produktkonfiguration zu verbessern.

Das Konzept der Solver-Strategien wurde erstmalig im Kumulativen Update 7 (CU7) für Microsoft Dynamics AX 2012 R2 eingeführt. Es wurde in kumulierter Update 8 (CU8) für Microsoft Dynamics AX 2012 R3 und Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.

Das Solver-Strategiekonzept besteht aus den folgenden Strategien:

- Standard
- Minimaldomänen zuerst
- Von oben nach unten
- Z3

## <a name="solver-strategy"></a>Solver-Strategie 

Ein Produktkonfigurationsmodell kann als [Constraint-Satisfaction-Problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf) formuliert werden. Microsoft Solver Foundation (MSF) bietet zwei Typen von Lösungs-Strategien, um die CSPs zu beheben, die von Produktkonfigurationsmodellen verwendet werden können. Diese Solver-Strategien hängen von [Heuristiken](https://techterms.com/definition/heuristic) ab, mit denen die Reihenfolge bestimmt wird, in der die Variablen der CSPs berücksichtigt werden, wenn das Problem behoben wird. Heuristiken können sich deutlich auf die Leistung auswirken, wenn ein Problem oder eine Klasse von Problemen gelöst wird.

Die Solver-Strategie für Produktkonfigurationsmodelle bestimmt, welcher Solver mit Heuristiken verwendet wird. Die Strategien **Standard**, **Minimaldomänen zuerst** und **Oben-nach-unten** verwenden die beiden Solver von MSF, wohingegen die Strategie **Z3** den Z3-Solver verwendet. 

Tatsächliche Kundenimplementierungsstudien haben gezeigt, dass eine Änderung der Solver-Strategie für ein Produktkonfigurationsmodell die Antwortzeit von Minuten in Millisekunden reduzieren kann. Daher lohnt sich der Aufwand, verschiedene Solver-Strategien auszuprobieren, um die effizienteste Strategie für Ihr Produktkonfigurationsmodell zu finden.

## <a name="change-the-settings-for-the-solver-strategy"></a>Ändern der Einstellungen für die Solver-Strategie

Um die Solver-Strategie auf der Seite **Produktkonfigurationsmodelle** im Aktivitätsbereich zu ändern, wählen Sie **Modelleigenschaften** aus. Wählen Sie dann im Dialogfeld **Modelldetails bearbeiten** eine Solver-Strategie aus.

[![Ändern der Solver-Strategie](./media/solver-strategy.png)](./media/solver-strategy.png)

Aktuell gibt es keine Logik, die automatisch feststellt, welche Solver-Strategie die effizienteste Strategie für eine einschränkungsbasierte Produktkonfiguration sein wird. Daher müssen Sie die Solver-Strategien einzeln nacheinander ausprobieren.

Die folgende Tabelle enthält Empfehlungen zur Verwendung der Solver-Strategie in unterschiedlichen Szenarien.

| Solver-Strategie      | Verwenden der Strategie in diesem Szenario |
|----------------------|-----------------------------------|
| Standard              | Die **Standard**-Strategie wurde optimiert, um eine Lösung für Modelle zu bieten, die von Tabelleneinschränkungen abhängen. Kundenimplementierungsstudien haben gezeigt, dass diese Strategie die effizienteste Strategie in Szenarien ist, in denen Tabelleneinschränkungen in großem Umfang verwendet werden. |
| Minimaldomänen zuerst | Die Strategien **Minimaldomänen zuerst** und **Von oben nach unten** sind eng verwandt. Kundenimplementierungsstudien haben gezeigt, dass die Strategie **Von oben nach unten** leistungsfähiger ist, als die Strategie **Minimaldomänen zuerst**. Allerdings wird die Strategie **Minimaldomänen zuerst** zwecks Abwärtskompatibilität im Produkt beibehalten. Beide diese Solver-Strategien haben sich bei der Lösung von Modellen, die mehrere arithemtische Ausdrücke enthalten, bei denen keine Tabelleneinschränkungen verwendet werden, als effizienter erwiesen. Jedoch ist in einigen Fällen die Strategie **Standard** leistungsfähiger als diese beiden Strategien. Daher denken Sie daran, jede Strategie auszuprobieren. |
| Von oben nach unten             | Die Strategien **Minimaldomänen zuerst** und **Von oben nach unten** sind eng verwandt. Kundenimplementierungsstudien haben gezeigt, dass die Strategie **Von oben nach unten** leistungsfähiger ist, als die Strategie **Minimaldomänen zuerst**. Allerdings wird die Strategie **Minimaldomänen zuerst** zwecks Abwärtskompatibilität im Produkt beibehalten. Beide diese Solver-Strategien haben sich bei der Lösung von Modellen, die mehrere arithemtische Ausdrücke enthalten, bei denen keine Tabelleneinschränkungen verwendet werden, als effizienter erwiesen. Jedoch ist in einigen Fällen die Strategie **Standard** leistungsfähiger als diese beiden Strategien. Daher denken Sie daran, jede Strategie auszuprobieren. |
| Z3                   | Es wird empfohlen, die Strategie **Z3** als standardmäßige Solver-Strategie zu verwenden. Wenn Sie Bedenken hinsichtlich Leistung oder Skalierbarkeit haben, können Sie die anderen Strategien prüfen. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Produktkonfiguration – Übersicht](build-product-configuration-model.md)

[Heuristik](https://techterms.com/definition/heuristic)

[Constraint-Satisfaction-Problem](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)
