---
title: Kreditlimit-Szenarien
description: Dieser Artikel beschreibt, wie das Kreditlimit des Debitors überprüft wird, wenn der Debitor zu einer Kundenkreditlimitgruppe gehört.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130256"
---
# <a name="credit-limit-scenarios"></a>Kreditlimit-Szenarien

In der Kreditverwaltung kann Kunden auf der Ebene des Debitors ein Kreditlimit zugewiesen werden. Jeder Debitor kann einer *Kundenkreditlimitgruppe* zugewiesen werden, und jede Gruppe verfügt über ein Kreditlimit. Daher kann den Debitor auch auf Gruppenebene ein Kreditlimit zugewiesen werden. Alle Kunden, die der gleichen Debitor-Kreditgruppe zugeordnet sind, haben das gleiche Kreditlimit.

Allgemein werden Gruppen-Kreditlimits vor individuellen Kreditlimits geprüft. Das individuelle Kreditlimit hat nicht immer Vorrang vor dem Gruppen-Kreditlimit.

Dieser Artikel beschreibt fünf Szenarien, die sich auf Debitor-Kreditgruppen und individuelle Kreditlimits beziehen.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Das Kreditlimit der Kundengruppe ist höher als das individuelle Kreditlimit

Der Debitor hat z.B. ein individuelles Kreditlimit von 10.000 $. Der Debitor ist einer Kundenkreditgruppe zugeordnet, und das Kreditlimit der Gruppe beträgt $15.000. In diesem Fall beträgt das „effektive Kreditlimit“ des Debitors $10.000, da dieser Betrag unter dem Gruppenlimit liegt. Die Sperrregeln prüfen zunächst das Gruppenlimit. Sie prüfen dann das individuelle Limit. Alle Verkaufsaufträge über $10.000 werden blockiert.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Das individuelle Kreditlimit ist höher als das Kreditlimit der Debitor-Gruppe

Der Debitor hat zum Beispiel ein individuelles Kreditlimit von 20.000 $. Der Debitor ist einer Kundenkreditgruppe zugeordnet, und das Kreditlimit der Gruppe beträgt $15.000. In diesem Fall beträgt das effektive Kreditlimit des Debitors $15.000, da die Sperrregeln immer zuerst das Gruppenlimit prüfen. Alle Verkaufsaufträge über $15.000 werden blockiert.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Das individuelle Kreditlimit ist auf 0,00 festgelegt und das obligatorische Kreditlimit ist auf Ja festgelegt.

Wenn der Debitor ein individuelles Kreditlimit hat, das auf **0,00** festgelegt ist, und die Option **Pflichtkreditlimit** auf **Ja** festgelegt ist, beträgt das effektive Kreditlimit des Debitors $0,00, auch wenn der Debitor einer Kundenkreditgruppe zugeordnet ist. Auf diese Weise kann der Debitor Teil einer Gruppe sein, aber alle Bestellungen gehen an die Kreditverwaltung.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Das individuelle Kreditlimit ist auf 0,00 festgelegt und das unbegrenzte Kreditlimit ist auf Ja festgelegt

Wenn der Debitor ein individuelles Kreditlimit hat, das auf **0,00** festgelegt ist, aber die Option **Unbegrenztes Kreditlimit** auf **Ja** festgelegt ist, hat der Debitor ein unbegrenztes Kreditlimit, auch wenn er einer Kundenkreditgruppe zugewiesen ist.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Das individuelle Kreditlimit ist auf 0,00 festgelegt und der Debitor ist Teil einer Kundenkreditgruppe

Zum Beispiel hat der Debitor ein individuelles Kreditlimit, das auf **0,00** festgelegt ist, die Option **Unbegrenzter Kredit** ist auf **Nein** festgelegt und die Option **Pflichtkreditlimit** ist auf **Nein** festgelegt. Der Debitor ist einer Kundenkreditgruppe zugeordnet, und das Kreditlimit der Gruppe beträgt $15.000. In diesem Fall ist das effektive Kreditlimit des Debitors das Gruppenlimit, also $15.000. Daher werden alle Verkaufsaufträge, die diesen Betrag überschreiten, gesperrt. Mit diesem Verhalten kann das Kreditlimit auf der Ebene der Kundenkreditgruppe statt auf der Ebene des einzelnen Debitors verwaltet werden. Alle Debitor, die der gleichen Gruppe zugeordnet sind, haben das gleiche Kreditlimit.
