---
title: Faktorabschreibung
description: Dieser Artikel gibt einen Überblick über die Faktorabschreibungsmethode.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840528"
---
# <a name="factor-depreciation"></a>Faktorabschreibung

[!include [banner](../includes/banner.md)]

Dieser Artikel gibt einen Überblick über die Faktorabschreibungsmethode.

Faktoren sind die zum Abschreiben von Anlagen verwendeten Prozentsätze. Wenn Sie ein Anlagenabschreibungsprofil einrichten und **Faktor** im Feld **Methode** auf der Seite **Abschreibungsprofile**auswählen, können Sie progressive, degressive oder lineare Abschreibung einrichten:

-   Bei der progressiven Abschreibung nimmt der Abschreibungsbetrag mit jedem Abschreibungszeitraum zu.
-   Bei degressiver Abschreibung nimmt der Abschreibungsbetrag pro Zeitraum im zeitlichen Verlauf ab.
-   Bei der linearen Abschreibung ist die Abschreibung in jedem Zeitraum identisch.

In den nachstehenden Regeln und Beispielen wird gezeigt, wie Sie Faktoren für die einzelnen Abschreibungstypen einrichten können. 

> [!NOTE] 
> Hinweis: Wenn Sie  **Faktor** im Feld  **Methode** auswählen, werden die Felder **Faktor** und **Intervall**  angezeigt.

## <a name="progressive-depreciation"></a>Progressive Abschreibung
Der Wert im Feld **Faktor** ist größer als **50**.

### <a name="example"></a>Beispiel

Der Anschaffungspreis beträgt 100.000, der Faktor ist 70, die Nutzungsdauer liegt bei 10 Jahren, und die Abschreibung beginnt am 1. Januar. Die Abschreibungsbeträge und die Nettobuchwerte werden nur für die ersten sechs Jahre der Nutzungsdauer angezeigt.

| Jahr | Periode      | Abschreibungsbetrag | Nettobuchwert |
|------|-------------|---------------------|-----------------------|
| 1    | 31. Dezember | 307,69              | 99.692,31             |
| 2    | 31. Dezember | 1.447,21            | 98.245,10             |
| 3    | 31. Dezember | 3.104,50            | 95.140,60             |
| 4    | 31. Dezember | 5.150,21            | 89.990,39             |
| 5    | 31. Dezember | 7.522,95            | 82.467,44             |
| 6    | 31. Dezember | 10.184,06           | 72.283,38             |

## <a name="digressive-depreciation"></a>Degressive Abschreibung
Der Wert im Feld **Faktor** ist kleiner als **50**.

### <a name="example"></a>Beispiel

Der Anschaffungspreis beträgt 100.000, der Faktor ist 20, die Nutzungsdauer liegt bei 10 Jahren, und die Abschreibung beginnt am 1. Januar. Die Abschreibungsbeträge und die Nettobuchwerte werden nur für die ersten sechs Jahre der Nutzungsdauer angezeigt.

| Jahr | Periode      | Abschreibungsbetrag | Nettobuchwert |
|------|-------------|---------------------|-----------------------|
| 1    | 31. Dezember | 56.080,43           | 43.919,57             |
| 2    | 31. Dezember | 10.665,70           | 33.253,87             |
| 3    | 31. Dezember | 7.156,22            | 26.097,65             |
| 4    | 31. Dezember | 5.538,06            | 20.559,59             |
| 5    | 31. Dezember | 4.579,89            | 15.979,70             |
| 6    | 31. Dezember | 3.937,36            | 12.042,34             |

## <a name="straight-line-depreciation"></a>Lineare Abschreibung
Der Wert im Feld **Faktor** ist gleich **50**. In diesem Fall ist die Abschreibung in jedem Zeitraum identisch. Sie sollten die Konsequenzen Ihrer Wertangaben in anderen Feldern entsprechend der Beschreibung in [Abschreibungsmethode "Lineare Nutzungsdauer"](straight-line-service-life-depreciation.md) berücksichtigen.



