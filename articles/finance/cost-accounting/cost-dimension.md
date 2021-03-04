---
title: Dimensionen erstellen und Dimensionsmitglieder importieren
description: Die Kostenrechnung ist ein unabhängiges Modul, das Masterdaten aus anderen Modulen erfordert.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d61358be79adc943572bb4a5d624cb7c80b52e6e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443602"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Dimensionen erstellen und Dimensionsmitglieder importieren

[!include [banner](../includes/banner.md)]

Die Kostenrechnung ist ein unabhängiges Modul, das Masterdaten aus anderen Modulen erfordert. Diese Daten werden in wie folgt kategorisiert:

-  Kostenelemente
-  Kostenobjekte
-  Statistische Dimensionen

Ein **Kostenelement** entspricht einem kostenrelevanten Artikel in dem Kontenplan. Ein **Kostenträger** entspricht einem Typ der Finanzdimension wie Produkte, Kostenstellen und Projekte, für die Sie Kosten schätzen, zuweisen oder direkt messen möchten. Eine **Statistischen Dimension** und seine Mitgliedern werden verwendet, um nicht monetäre Einträge in der Kostenrechnung zu erfassen und zu steuern. Statistische Dimensionswerte können als Verrechnungsgrundlage in den Richtlinien wie Kostenaufteilung und Prozentsatz verwendet werden. 

Das folgende Diagramm veranschaulicht die Dimensionen, die in der Kostenrechnung verwendet werden.

[![Kostenrechnungsdimensionen](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Nachdem die Daten in die Kostenrechnung importiert wurden, können Variablengruppen verwendet werden, um unterschiedliche Perspektiven zu erstellen, die Manager auf allen Ebenen der Organisation Einblicke geben. Unter den folgenden Themen finden Sie Informationen zum Erstellen von Dimensionen und importieren von Dimensionsmitgliedern. 

-  [Kostenelementdimensionen](cost-elements.md)
-  [Kostenelemente erstellen](./tasks/create-cost-elements.md)
-  [Kostenträgerdimensionen](cost-objects.md)
-  [Kostenelement-Dimensionselemente einem allgemeinen Satz von Dimensionselementen zuordnen](map-cost-elements-dimension-members.md)
-  [Eine Kostenelementdimension zuordnen](./tasks/map-cost-element-dimension.md)
-  [Statistische Dimensionselement und statistischen Maßnahmenanbieter-Vorlagen](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]