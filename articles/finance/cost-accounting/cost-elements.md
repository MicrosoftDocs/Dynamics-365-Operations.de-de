---
title: Kostenelementdimensionen
description: Als eine der Kernpfeiler bei der Kostenrechnung werden Kostenelementdimensionen verwendet, um zu kategorisieren und nachzuverfolgen, wo Kosten hinfließen.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 86d2e431e630afd37ebd1fa3b8f7f553c77bb822
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735169"
---
# <a name="cost-element-dimensions"></a>Kostenelementdimensionen

[!include [banner](../includes/banner.md)]

Als eine der Kernpfeiler bei der Kostenrechnung werden Kostenelementdimensionen verwendet, um zu kategorisieren und nachzuverfolgen, wo Kosten hinfließen. 

Ein Kostenelement entspricht einem kostenrelevanten Artikel in dem Kontenplan. Grundsätzlich kann es jeder Elementtyp auf der untersten Ebene in einem Unternehmen sein, wohin die Kosten fließen können. Kostenelemente als Konzeptbereich von Sachkonten zu allen kostenrelevanten Ressourcen. Aktuell unterstützt die Kostenrechnung Sachkonten.

## <a name="two-types-of-cost-elements"></a>Zwei Typen von Kostenelementen
Es gibt zwei Typen von Kostenelementen: primäre Kostenelemente und sekundäre Kostenelemente. In der folgenden Tabelle wird der Unterschied zwischen beiden Typen beschrieben.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Primäre Kostenelemente</strong></td>
<td><strong>Sekundäre Kostenelemente</strong></td>
</tr>
<tr class="even">
<td>Die primären Kostenelemente stellen den Kostenfluss von der Finanzbuchhaltung zur Kostenrechnung dar. Die Kostenelementstruktur entspricht der Gewinn- und Verlustkontostruktur im Hauptbuch, wo ein Kostenelement einem Hauptkonto entsprechen kann. Nicht alle Hauptkonten werden notwendigerweise als Kostenelemente dargestellt, je nach den Geschäftsanforderungen. Beispiele von primären Kostenelementen sind unter Anderem:
<ul>
<li>Wareneinsätze (COGs)</li>
<li>Indirekte Materialkosten</li>
<li>Personalkosten</li>
<li>Energiekosten</li>
</ul></td>
<td>Die sekundären Kostenelemente stellen den Fluss der Kosten intern dar, da diese Kosten nur in der Kostenrechnung erstellt und verwendet werden. Sie werden verwendet, um sicherzustellen, dass die Kostenquelle nachverfolgt werden kann. Diese Kostenelemente werden in Kostenzuteilungen und bei Gemeinkostenberechnungen verwendet. Beispiele von sekunären Kostenelementen sind unter Anderem:
<ul>
<li>Produktionskosten</li>
<li>Gemeinkosten für Produktion, Material und Marketing</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Kostenelementdimensionen und Kostenelement-Dimensionsmitglieder
Kostenelemente werden als *Kostenelementdimensionen* bezeichnet. Die einzelnen Dimensionswerte werden *Kostenelement-Dimensionsmitglieder* genannt. Beispielsweise haben Sie eine US-Kontenplanstruktur (COA), die die Basis für ihre Offenlegungspflicht ist. Diese COA wird als Kostenelementdimension verwendet. Die Konten, die primäre Kostenelemente sind, werden als Kostenelement-Dimensionsmitglieder in der Kostenrechnung dargestellt. Das folgende Screenshot zeigt ein Beispiel der Hauptkonten als die Kostenelementdimension mit ihren tatsächlichen Hauptkonten als die Kostenelement-Dimensionsmitglieder an. 

[![Screenshot von Hauptkonten als Kostenelementdimension.](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Kostenelement-Dimensionsmitglieder über Datenkonnektoren importieren
Um die Einstellungen der Kostenelement-Dimensionsmitglieder in der Kostenrechnung zu vereinfachen, können Sie Datenkonnektoren verwenden, die entweder vorkonfiguriert sind oder Ihr benutzerdefinierter Build sind, um die primären Kostenelemente aus einem oder mehreren Quellsystemen abzurufen.

## <a name="implementation-considerations"></a>Implementierungsüberlegungen
Da Kostenelemente die unterste Ebene der Kostendetails darstellen, sollten Sie sicherstellen, dass alle Kostenelemente, die zur Berichterstellung auf Führungsebene erforderlich sind, einbezogen werden, wenn Sie die Kostenelementstruktur implementieren. Es kann eine Herausforderung sein, eine entsprechenden Anzahl von Kostenelementen für die Kostensteuerung zu finden. Wenn Sie Tausende von Kostenelementen haben, kann es schwierig sein, jedes Kostenelement zu steuern. Alternativ können Sie Kostenelemente gruppieren und die Kostensteuerung auf einer aggregierten Ebene verwalten.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
