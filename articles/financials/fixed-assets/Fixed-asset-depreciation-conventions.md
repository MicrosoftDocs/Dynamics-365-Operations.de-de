---
title: Anlagenabschreibungskonventionen
description: Dieses Thema bietet eine Übersicht der Abschreibungskonventionen für Anlagen.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad44282de9d999aa211548601eb416f4bdba2047
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840768"
---
# <a name="fixed-asset-depreciation-conventions"></a>Anlagenabschreibungskonventionen

[!include [banner](../includes/banner.md)]

Abschreibungskonventionen werden verwendet, um zu bestimmen, wann und wie eine Abschreibung berechnet wird, sowohl für das Jahr, in dem die Anlage erworben wird als auch für das Jahr, in dem die Anlage abgeht.

Abschreibungskonventionen können den Einstellungen für ein Anlagengruppenbuch zugewiesen werden. Um die Abschreibungskonvention im Aufsetzbereich von Anlagen anzuzeigen oder zuzuweisen, wählen Sie die Gruppen **Anlage** aus. Wählen Sie die Schaltfläche **Bücher**. In diesem Fall werden die Abschreibungskonventionen, die zugewiesen werden, als Standardwerte verwendet, wenn Anlagenbücher erstellt werden. Abschreibungskonventionen können auch für ein einzelnes Anlagenbuch festgelegt werden. Um dies zu bewerkstelligen, wählen Sie **Bücher** im Aufsetzbereich von Anlagen aus und wählen Sie dann die Schaltfläche **Anlagengruppen** aus.


|  Abschreibungskonvention  |   Beschreibung  |
|---------------------------|-----------------|
|           Keiner            |  Anlagen beginnen ab dem Datum der <strong>Inbetriebnahme</strong>, an Wert zu verlieren.|
|         Halbjahr         |  Sie ziehen eine Halbjahresabschreibung sowohl für das erste Jahr als auch das letzte Jahr für das abzuschreibende Objekt ab. Sie ziehen eine ganzjährige Abschreibung für jedes andere Jahr während des Abscheibungszeitraums ab. |
|        Ganzer Monat         | Bei Anlagen, die ein Datum <strong>Inbetriebnahme</strong> haben, dass sich an jedem beliebigen Zeitpunkt während des Monats ereignen kann, beginnt die Abschreibung ab dem ersten Tag jenes Monats. Anlagen, die zu einem beliebigen Zeitpunkt während des Monats außer Betrieb gesetzt werden, gelten zu Abschreibungszwecken am letzten Tag des vorangegangenen Monats als außer Betrieb gesetzt.  |
|        Quartalsmitte        | Um Ihren Abschreibungsabzug für das Jahr zu berechnen, in dem Sie das Objekt in Betrieb setzen, multiplizieren Sie die Abschreibung für ein ganzes Jahr mit dem Prozentsatz für das Quartal, in dem das Objekt in Betrieb genommen wird, wie in der folgenden Tabelle dargestellt.<table><thead><tr><th>Quartal</th><th>Prozentsatz</th></tr></thead><tbody><tr><td>Vorname</td><td>87,5</td></tr><tr><td>Zweites</td><td>62,5</td></tr><tr><td>Drittes</td><td>37,5</td></tr><tr><td>Viertes</td><td>12,5</td></tr></tbody></table>Ein Halbquartal Abschreibung wird im Quartal des Abgangs berechnet (oder das vollständig abgeschriebene Quartal). |
| Monatsmitte (1. des Monats)  | Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der ersten Hälfte des Monats haben (Tage 1 bis 15) beginnt die Abschreibung am ersten Tag des Monats des Datums der <strong>Inbetriebnahme</strong>. Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der zweiten Hälfte des Monats haben (Tage 16 bis Monatsende) beginnt die Abschreibung am ersten Tag des Monats nach dem Datum der <strong>Inbetriebnahme</strong>. Anlagen, die in der ersten Hälfte des Monats außer Betrieb gesetzt werden (Tage 1 bis 15), gelten zu Abschreibungszwecken am letzten Tag des vorangegangenen Monats als außer Betrieb gesetzt. Anlagen, die in der zweiten Hälfte des Monats außer Betrieb gesetzt werden (Tage 16 bis Monatsende), gelten zu Abschreibungszwecken am letzten Tag des vorangegangenen Monats der Außerbetriebsetzung als außer Betrieb gesetzt. |
| Monatsmitte (15. des Monats) |  Um Ihren Abschreibungsabzug für das Jahr zu berechnen, in dem Sie das Objekt in Betrieb setzen, multiplizieren Sie die Abschreibung für ein ganzes Jahr mit einer Bruchzahl. Der Zähler (obere Zahl) dieses Bruchs ist die Zahl ganzer Monate im Jahr, während die das Objekt in Betrieb ist, plus 1/2 oder (0,5). Der Nenner (untere Zahl) ist 12. Wenn Sie den Abgang des Objekts vor dem Ende Ihres Abschreibungszeitraums vollziehen, verwenden Sie dieselbe Methode, um Ihren Abschreibungsabzug für das Jahr des Abgangs zu berechnen.   |
| Halbes Jahr (Jahresanfang) | Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der ersten Hälfte des Jahres haben, beginnt die Abschreibung am ersten Tag des Jahres (ganzes Jahr). Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der zweiten Hälfte des Jahres haben, beginnt die Abschreibung in der Mitte des Jahres.|
|   Halbes Jahr (nächstes Jahr)   |   Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der ersten Hälfte des Jahres haben, beginnt die Abschreibung am ersten Tag des Jahres (ganzes Jahr). Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der zweiten Hälfte des Jahres haben, beginnt die Abschreibung am ersten Tag des nächsten Jahres. Anlagen, die in der ersten Hälfte des Jahres außer Betrieb gesetzt werden, gelten zu Abschreibungszwecken am letzten Tag des vorangegangenen Jahres als außer Betrieb gesetzt. Jede Abschreibung, die im aktuellen Jahr gebucht wird, muss zurückgesetzt oder bereinigt werden. Anlagen, die in der zweiten Hälfte des Jahres außer Betrieb gesetzt werden, gelten für Abschreibungszwecke am letzten Tag des Jahres der Außerbetriebsetzung als außer Betrieb gesetzt.|

