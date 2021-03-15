---
title: Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung
description: Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f189d1ed5b0917c9975587accc2275556ceb8143
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968753"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Ausgeglichene Erfassungen für einheitenübergreifende Buchhaltung

[!include [banner](../includes/banner.md)]

Dieser Artikel zeigt, wie eine Erfassung automatisch ausgeglichen wird, wenn eine ausgleichende Finanzdimension auf der Sachkontoseite ausgewählt ist. 

Wenn Buchhaltungseinträge nicht auf der Ebene der Finanzdimensionswerte ausgeglichen sind, werden zusätzliche Kontoeinträge automatisch erstellt, um die Erfassung auszugleichen. Diese Kontoeinträge verwenden **Einheitenbezogen - Soll**- und **Einheitenbezogen - Haben**-Buchungstypen auf der Seite **Konten für automatische Buchungen**, um das Hauptkonto zu bestimmen. Beispielsweise wird Geschäftseinheit, die das zweite Segment des Sachkontos darstellt, als Ausgleichsfinanzdimension ausgewählt, und die folgenden Buchhaltungseinträge werden anschließend erstellt.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

In diesem Fall werden die folgenden Salden bestimmt:

-   Für Geschäftseinheit MSP = 100,00 CR
-   Für Geschäftseinheit NY = 100,00 DR

Die folgenden Buchhaltungseinträge werden daher automatisch erstellt, damit die Erfassung auf der Ebene der Finanzdimensionswerte ausgeglichen ist.

|                                   |           |
|-----------------------------------|-----------|
| (Einheitenbezogen Soll) – MSP  – OU\_256 | 100,00 DR |
| (Einheitenbezogen Haben) – NY – OU\_249 | 100,00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]