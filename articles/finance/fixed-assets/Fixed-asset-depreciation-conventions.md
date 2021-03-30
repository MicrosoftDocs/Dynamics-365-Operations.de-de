---
title: Anlagenabschreibungskonventionen
description: Dieses Thema beschreibt die Abschreibungskonventionen für Anlagen.
author: saraschi2
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b238a4a57ee2eb58fea11661ae79a649d399f5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230297"
---
# <a name="fixed-asset-depreciation-conventions"></a>Anlagenabschreibungskonventionen

[!include [banner](../includes/banner.md)]

Dieses Thema beschreibt die Abschreibungskonventionen für Anlagen. Abschreibungskonventionen werden verwendet, um zu bestimmen, wann und wie eine Abschreibung berechnet wird, sowohl für das Jahr, in dem die Anlage erworben wird als auch für das Jahr, in dem die Anlage abgeht.

Abschreibungskonventionen können den Einstellungen für ein Anlagengruppenbuch zugewiesen werden. Um die Abschreibungskonvention im Aufsetzbereich von Anlagen anzuzeigen oder zuzuweisen, wählen Sie die Gruppen **Anlage** aus. Wählen Sie die Schaltfläche **Bücher**. In diesem Fall werden die Abschreibungskonventionen, die zugewiesen werden, als Standardwerte verwendet, wenn Anlagenbücher erstellt werden. Abschreibungskonventionen können auch für ein einzelnes Anlagenbuch festgelegt werden. Um dies zu bewerkstelligen, wählen Sie **Bücher** im Aufsetzbereich von Anlagen aus und wählen Sie dann die Schaltfläche **Anlagengruppen** aus.

| Abschreibungskonvention   | Beschreibung |
|---------------------------|-------------|
| Keiner                      | Anlagen beginnen ab dem Datum der <strong>Inbetriebnahme</strong>, an Wert zu verlieren. |
| Halbjahr                 | Eine Halbjahresabschreibung sowohl wird sowohl für das erste Jahr als auch das letzte Jahr abgezogen, in dem Sie das Objekt abschreiben. Eine ganzjährige Abschreibung wird für jedes andere Jahr während des Abschreibungszeitraums abgeschrieben. |
| Ganzer Monat                | Bei Anlagen, die ein Datum <strong>Inbetriebnahme</strong> haben, dass sich an jedem beliebigen Zeitpunkt während des Monats ereignen kann, beginnt die Abschreibung ab dem ersten Tag jenes Monats. Für Abschreibungszwecke gelten Vermögenswerte am letzten Tag des Vormonats als stillgelegt. Der bestimmte Tag des Monats, an dem sie in den Ruhestand gingen, wird nicht berücksichtigt. |
| Quartalsmitte               | Um Ihren Abschreibungsabzug für das Jahr zu berechnen, in dem Sie das Objekt in Betrieb setzen, multiplizieren Sie die Abschreibung für ein ganzes Jahr mit dem Prozentsatz für das Quartal, in dem das Objekt in Betrieb genommen wird, wie in der folgenden Tabelle dargestellt wird.<table><thead><tr><th>Quartal</th><th>Prozentsatz</th></tr></thead><tbody><tr><td>Vorname</td><td>87,5</td></tr><tr><td>Zweites</td><td>62,5</td></tr><tr><td>Drittes</td><td>37,5</td></tr><tr><td>Viertes</td><td>12.5</td></tr></tbody></table>Ein Halbquartal Abschreibung wird im Quartal des Abgangs der Anlage berechnet (oder das vollständig abgeschriebene Quartal). |
| Monatsmitte (1. des Monats)  | Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der ersten Hälfte des Monats haben (Tage 1 bis 15) beginnt die Abschreibung am ersten Tag des Monats des Datums der <strong>Inbetriebnahme</strong>. Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der zweiten Hälfte des Monats haben (Tage 16 bis Monatsende) beginnt die Abschreibung am ersten Tag des Monats nach dem Datum der <strong>Inbetriebnahme</strong>. Anlagen, die in der ersten Hälfte des Monats außer Betrieb gesetzt werden (Tage 1 bis 15), gelten für Abschreibungszwecken am letzten Tag des vorangegangenen Monats als außer Betrieb gesetzt. Anlagen, die in der zweiten Hälfte des Monats außer Betrieb gesetzt werden (Tage 16 bis Monatsende), gelten für Abschreibungszwecke am letzten Tag des vorangegangenen Monats der Außerbetriebsetzung als außer Betrieb gesetzt. |
| Monatsmitte (15. des Monats) | Um Ihren Abschreibungsabzug für das Jahr zu berechnen, in dem Sie das Objekt in Betrieb setzen, multiplizieren Sie die Abschreibung für ein ganzes Jahr mit einer Bruchzahl. Der Zähler (obere Zahl) dieses Bruchs ist die Zahl ganzer Monate im Jahr, während die das Objekt in Betrieb ist, plus 1/2 oder (0,5). Der Nenner (untere Zahl) ist 12. Wenn Sie den Abgang des Objekts vor dem Ende Ihres Abschreibungszeitraums vollziehen, verwenden Sie dieselbe Methode, um Ihren Abschreibungsabzug für das Jahr des Abgangs zu berechnen. |
| Halbes Jahr (Jahresanfang) | Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der ersten Hälfte des Jahres haben, beginnt die Abschreibung am ersten Tag des Jahres (ganzes Jahr). Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der zweiten Hälfte des Jahres haben, beginnt die Abschreibung in der Mitte des Jahres. |
| Halbes Jahr (nächstes Jahr)     | Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der ersten Hälfte des Jahres haben, beginnt die Abschreibung am ersten Tag des Jahres (ganzes Jahr). Bei Anlagen, die ein Datum der <strong>Inbetriebnahme</strong> in der zweiten Hälfte des Jahres haben, beginnt die Abschreibung am ersten Tag des nächsten Jahres. Anlagen, die in der ersten Hälfte des Jahres außer Betrieb gesetzt werden, gelten für Abschreibungszwecke am letzten Tag des vorangegangenen Jahres als außer Betrieb gesetzt. Jede Abschreibung, die im aktuellen Jahr gebucht wird, muss zurückgesetzt oder bereinigt werden. Anlagen, die in der zweiten Hälfte des Jahres außer Betrieb gesetzt werden, gelten zu Abschreibungszwecken am letzten Tag des Jahres der Außerbetriebsetzung als außer Betrieb gesetzt. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]