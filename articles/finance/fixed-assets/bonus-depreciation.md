---
title: Vorzeitige Abschreibung
description: Dieser Artikel enthält eine Übersicht der Bonusabschreibungsfunktionalität.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: kfend
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 801747f06d16e70cd04b727787f0bfa6b6baefc0
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711144"
---
# <a name="bonus-depreciation"></a>Vorzeitige Abschreibung

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht der Bonusabschreibungsfunktionalität.

Die vorzeitige Abschreibung ermöglicht es Ihnen, im ersten Jahr der Inbetriebnahme und Abschreibung einer Anlage zusätzliche Abschreibungsbeträge vorzeitig geltend zu machen. Vorzeitige Abschreibung muss vor jeder anderen Abschreibungsberechnung durchgeführt werden. Daher empfiehlt es sich, vorzeitige Abschreibung von Büchern zu verwenden, in denen der Anteil an die Hauptbuchfunktionen deaktiviert wird. Mithilfe der Option **Löschungsbuchungen nicht im Hauptbuch gebucht** können Sie historische Buchungen für Bücher löschen, die nicht im Hauptbuch gebucht werden. Sie können die vorzeitige Abschreibung im Anlagenlebenszyklus später aufnehmen, indem Sie Abschreibungsbuchungen löschen, die bereits gebucht wurden. 

Sie können die vorzeitige Abschreibung mithilfe des Vorschlagsprozesses berechnen, oder Sie können Buchungen für vorzeitige Abschreibungen manuell erstellen. Buchungen für vorzeitige Abschreibungen können nicht erstellt werden, wenn für das jeweilige Anlagenabschreibungsbuch Abschreibungsbuchungen oder Abschreibungsregulierungsbuchungen vorhanden sind.

Wird der Vorschlagsprozess zum Berechnen der vorzeitigen Abschreibung verwendet, werden alle vorhandenen Zulagenbuchungen in die Berechnung der Basis einbezogen. In die Berechnung sind auch alle früheren vorzeitigen Abschreibungen eingeschlossen, die manuell für die Anlage eingegeben wurden. 

Wenn für eine Anlage mehrere vorzeitige Abschreibungen geltend gemacht werden, wird die Priorität berücksichtigt. Jede Zulage reduziert den Anlagenbasiswert für die nächste Zulage. Der Schrottwert wird bei Berechnung der vorzeitigen Abschreibung nicht in der Anlagenbasis berücksichtigt, und die Abschreibungskonvention gilt nicht für die vorzeitige Abschreibung. 

In den Vereinigten Staaten werden gegenwärtig bestimmte Anlagen als Anlagen gemäß Abschnitt 179 eingestuft. Beim Abzug gemäß Abschnitt 179 haben Sie die Möglichkeit, die Kosten für bestimmte Anlagen ganz oder teilweise und bis zu einer bestimmten Grenze zurückzuerhalten. Sie erhalten die Kosten zurück, wenn Sie diese im Jahr der Inbetriebsetzung der Anlage zum Abzug bringen.

## <a name="example"></a>Beispiel
Folgende vorzeitige Abschreibungen sind einem Abschreibungsbuch zugeordnet:

-   **Abschnitt 179:** 1,000.00, Priorität 1
-   **Liberty Zone:** 30 Prozent, Priorität 2

Die Anlagenanschaffungskosten belaufen sich auf 5.000,00. Bei der Berechnung der vorzeitigen Abschreibung beträgt der erste Abschreibungsbetrag 1.000,00 für die Abschreibung gemäß Abschnitt 179. 

Der nächste Betrag für die vorzeitige Abschreibung für die Liberty Zone-Abschreibung wird wie folgt berechnet: 

Anschaffungskosten – 1.000 (Abschreibung gemäß Abschnitt 179) x 30 % = 1.200 

Wenn der Betrag für die vorzeitige Abschreibung höher als die verbleibenden Anschaffungskosten ist, entspricht der Abschreibungsbetrag entweder dem Berechnungsergebnis der vorzeitigen Abschreibung oder den verbleibenden Anschaffungskosten, je nachdem, welcher Betrag geringer ist. 

Wenn die verbleibenden Anschaffungskosten 0 (Null) oder negativ sind, werden keine Buchungen für die vorzeitige Abschreibung generiert. 

Wenn die vorzeitige Abschreibung unter Verwendung des Vorschlagsprozesses berechnet wird, wird eine Abschreibungsbuchung für alle anwendbaren Datensätze der vorzeitigen Abschreibung erstellt, die dem jeweiligen Anlagenabschreibungsbuch zugeordnet sind. 

Sie können eine unbegrenzte Anzahl von Datensätzen für die vorzeitige Abschreibung erstellen. Nach deren Zuordnung zu einem Anlagengruppen-Abschreibungsbuch werden sie auf das Anlagenabschreibungsbuch angewendet. 

Die vorzeitige Abschreibung wird als Prozentsatz oder als fester Wert eingegeben. Beim Buchen von Abschreibungsvorschlägen werden Buchungen für die vorzeitige Abschreibung im Abschreibungsbuch getrennt von Abschreibungsbuchungen erfasst.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
