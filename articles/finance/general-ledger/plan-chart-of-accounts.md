---
title: Kontenplan planen
description: Dieser Artikel enthält Informationen, die Ihnen helfen, Kontenpläne für Ihre Organisation zu planen.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e797117199ff57cb4d3beae187ae7649579d33b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853347"
---
# <a name="plan-your-chart-of-accounts"></a>Kontenplan planen

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen, die Ihnen helfen, Kontenpläne für Ihre Organisation zu planen.

Um Finanzdaten in einer Organisation zu verfolgen und zu verwalten, können Sie einen Kontenplan einrichten. Ein Kontenplan ist eine Reihe von Konten, die ein finanziellen Rahmen definieren. Um Buchungen in diesen Konten noch weiter nachzuverfolgen, können Sie Segmente hinzufügen. Diese Segmente sind als Finanzdimensionen bekannt. Beispielsweise kann ein Ausgabenkonto Finanzdimensionen mit der Bezeichnung "Abteilung", "Kostenstelle" und "Kostenträger" enthalten. Benutzerdefinierte Regeln bestimmen, wie Finanzdimensionen an die Hauptkonten und andere Finanzdimensionen angefügt werden und auch wie Buchungen eingegeben werden. Diese benutzerdefinierten Regeln sind als Kontostrukturen und erweiterte Regeln bekannt.

Der Kontenplan ist eine strukturierte Liste der Hauptbuchkonten einer juristischen Person. Diese Liste wird verwendet, um Finanzberichte für Behörden und Eigentümer vorzubereiten. Die Konten werden zuerst nach Kontenarten gruppiert und dann in übergeordneten Kategorien zusammengefasst. Auf der allgemeinsten Ebene sind die Konten in Umsatzerlöse und Kosten (Betriebskonten) sowie Aktiva und Passiva (Bilanzkonten) unterteilt.

Ein Kontenplan kann freigegeben und von jeder juristischen Person in einer Organisation verwendet werden. Der Kontenplan für die juristischen Person wird auf der Seite **Sachkonto** definiert.

Hier einige der Faktoren, die Sie bei der Strukturierung des Kontenplans für Ihre Organisation berücksichtigen müssen:

- Die Meldeanforderungen für das Land oder die Region, in der Ihre Organisation ihren Sitz hat.
- Die Meldeanforderungen für Ihre juristische Person
- Der erforderliche Spezifikationsgrad, sowohl für externe Organisationen als auch für Ihre Organisation

Sie erstellen den Kontenplan auf der Seite **Kontenplan**. Sie können Hauptkonten über die Seite **Kontenplan** oder die Seite **Hauptkonten** erstellen. Ihre Hauptkonten dürfen keine Sonderzeichen verwenden, die als Trennzeichen für Kontenplan verwendet werden. Andernfalls erfahren Sie möglicherweise Instabilität, oder Sie müssen möglicherweise immer Suchen oder das Dialogfeld verwenden, wenn Sie Kombinationen von Konten und Dimensionen eingeben. Weitere Informationen finden Sie unter [Erstellen eines Hauptkontos](tasks/create-main-account.md).

> [!NOTE]
> In Dynamics 365 for Finance and Operations, Version 8.0 (April 2018 ), können Sie das Kontenplantrennzeichen aus der Seite **Hauptbuchparameter** ändern.

Es wird empfohlen, die Hauptkonten mit Hauptkontokategorien verknüpfen, sodass Sie die standardmäßige Finanzberichte nutzen können, ohne Änderungen vornehmen zu müssen. Daher können Sie Berichte schneller und einfacher entwerfen und verwalten.

Sie können Kontostrukturen auf der Seite **Kontostrukturen konfigurieren** erstellen. Kontostrukturen definieren zulässige Kombinationen. Diese Kombinationen bilden zusammen mit den Hauptkonten einen Kontenplan. Weitere Informationen zu Kontostrukturen finden Sie unter [Kontostrukturen erstellen](tasks/create-account-structures.md).

**Juristische Person überschreibt**

Nicht alle Hauptkonten sind für alle juristischen Personen gültig und manche sind möglicherweise nur für eine bestimmte Zeitperiode relevant. In diesem Szenario können Sie den Abschnitt **Überschreibungen der juristischen Person** verwenden, um die Unternehmen zu identifizieren, für die das Hauptkonto ausgesetzt werden soll, den Besitzer und den Zeitraum, zu dem die Dimension aktiv ist. Die Überschreibungen auf der freigegebenen Ebene können nicht einschränkender als die Überschreibungen auf der Ebene der juristischen Person sein.

Weitere Informationen finden Sie in folgenden Themen:

- [Finanzdimensionen](financial-dimensions.md)
- [Strukturen für erweiterte Regeln erstellen und zuweisen](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
