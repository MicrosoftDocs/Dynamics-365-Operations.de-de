---
title: Methodik der Abschreibungskonvention für ein halbes Jahr
description: In diesem Artikel wird die Methode beschrieben, mit der bei Anlagevermögen die Abschreibung nach der Halbjahreskonvention berechnet wird, die die sechsmonatige Abschreibung während des ersten und letzten Betriebsjahres eines Vermögenswerts berechnet.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879594"
---
# <a name="half-year-depreciation-convention-methodology"></a>Methodik der Abschreibungskonvention für ein halbes Jahr

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel wird die Methode beschrieben, mit der im Anlagevermögen die Abschreibung nach der Halbjahreskonvention berechnet wird. Mit der Halbjahreskonvention wird die sechsmonatige Abschreibung während des ersten und letzten Dienstjahres eines Vermögenswerts berechnet. Weitere Informationen zu Abschreibungskonventionen finden Sie untere [Abschreibungsmethoden und - konventionen](Fixed-asset-depreciation-conventions.md). 

Wenn Sie die sechsmonatige Abschreibungskonvention verwenden, nutzt das System das Erwerbsjahr oder das Jahr, in dem der Vermögenswert in Betrieb genommen wurde, berechnet dann fünf Jahre Abschreibung aus diesem Jahr und addiert dann sechs Monate. Betrachten Sie zur Veranschaulichung dieses Prozesses einen Vermögenswert, der zum Preis von 50.000 erworben und im April 2020 in Betrieb genommen wurde. Nehmen Sie außerdem an, dass der Vermögenswert eine Lebensdauer von fünf Jahren hat.

Das erste Dienstjahr endet im Dezember 2020, d.h. die fünfjährige Nutzungsdauer des Vermögenswerts endet im Dezember 2024. Die Halbjahresabschreibungskonvention verlängert die Lebensdauer des Vermögenswerts um sechs Monate, was bedeutet, dass seine Nutzungsdauer im Juni 2025 endet. 

> Jährliche Abschreibung 50.000/5 = 10.000 monatliche Abschreibung 10.000/12 = 833,33 <br>
> Abschreibung im ersten Jahr 10.000/2 = 5.000 und die anschließende monatliche Abschreibung 5.000/9 = 555,56

   [![Abschreibungsplan für die Halbjahresabschreibungskonvention.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Die verlängerten Abschreibungszeiträume die durch die Halbjahreskonvention hinzugefügt werden, ermöglichen eine genauere Zuordnung der Abschreibungen. Die Sechsmonatsvereinbarung stellt die Abschreibungskosten gleichmäßiger dar, was für die Berichterstattung in der Gewinn- und Verlustrechnung nützlich ist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
