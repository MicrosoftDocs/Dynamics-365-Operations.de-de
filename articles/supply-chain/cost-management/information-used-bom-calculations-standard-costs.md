---
title: "In Stücklistenberechnungen mit Standardkosten verwendete Informationen"
description: "In einer Stücklistenberechnung werden anhand von Daten aus mehreren Quellen die Standardkosten eines produzierten Artikels berechnet. Zu diesen Quellen zählen Informationen zu Artikeln, Listenrouten, Berechnungsformeln für indirekte Kosten sowie die Nachkalkulationsversion."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 187482f29e6982220b844777ef31997f0d5ef0d3
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="information-used-in-bom-calculations-with-standard-costs"></a>In Stücklistenberechnungen mit Standardkosten verwendete Informationen

[!include [banner](../includes/banner.md)]

In einer Stücklistenberechnung werden anhand von Daten aus mehreren Quellen die Standardkosten eines produzierten Artikels berechnet. Zu diesen Quellen zählen Informationen zu Artikeln, Listenrouten, Berechnungsformeln für indirekte Kosten sowie die Nachkalkulationsversion.

Die Informationen zu eingekauften Artikeln, die in einer Herstellkostenkalkulation für Standardkosten verwendet werden, umfassen Folgendes:
-   Kosten – Die Kosten eines eingekauften Artikels werden als standortspezifische Kostendatensätze innerhalb einer Nachkalkulationsversion für Standardkosten verwaltet. Jeder Kostendatensatz besitzt ein Gültigkeitsdatum, und anhand des Datums der Herstellkostenkalkulation wird der zu verwendende Kostendatensatz bestimmt. So kann beispielsweise von einer Herstellkostenkalkulation mit einem noch nicht erreichten Berechnungsdatum ein Kostendatensatz mit dem Status "Ausstehend" und einem Gültigkeitsdatum verwendet werden, das in der Zukunft liegt.
-   Kostengruppen – Die einem eingekauften Artikel zugewiesene Kostengruppe bildet die Grundlage für die Kostensegmentierung in den berechneten Kosten eines produzierten Artikels.
-   Warnbedingungen, die in der Stücklistenberechnungsgruppe des Artikels eingebettet sind, aktivieren die Stücklistenberechnung, um potenzielle Probleme zu identifizieren. Dies kann der Fall sein, wenn der eingekaufte Artikel in der Stückliste die Kosten Null hat oder einen veralteten Kostendatensatz besitzt. Die anzuwendenden Warnbedingungen können bei der Initiierung der Herstellkostenkalkulation außer Kraft gesetzt werden.

Die Informationen zu produzierten Artikeln, die in einer Herstellkostenkalkulation für Standardkosten verwendet werden, umfassen Folgendes:
-   Standardauftragsmenge für den Bestand – Die Standardauftragsmenge des Artikels für den Bestand fungiert als standardmäßige Abrechnungslosgröße für die Amortisierung konstanter Kosten in einer Stücklistenberechnung. Sofern angegeben, spiegelt die Abrechnungslosgröße zudem auch das Vielfache der Auftragsmenge wider.
-   Warnbedingungen, die in der Stücklistenberechnungsgruppe des Artikels eingebettet sind, aktivieren die Stücklistenberechnung, um potenzielle Probleme zu identifizieren. Ein Beispiel kann etwa sein, dass der produzierte Artikel nicht über eine Stückliste oder einen Arbeitsplan verfügt. Die anzuwendenden Warnbedingungen können bei der Initiierung der Herstellkostenkalkulation außer Kraft gesetzt werden.

Die Stücklisteninformationen, die in einer Herstellkostenkalkulation für Standardkosten verwendet werden, umfassen Folgendes:
-   Stücklistenversion – Die dem produzierten Artikel zugewiesene Stücklistenversion besitzt ein Gültigkeitsanfangs- und ein Gültigkeitsenddatum sowie einen Genehmigungs- und einen Aktivierungsstatus. Die Stücklistenversion kann unternehmensweit gelten oder standortspezifisch sein und optional Mengen-Breakpoints beinhalten.
-   Stücklistenpositionsartikelmenge − Eine Komponente verfügt in der Regel über eine variable erforderliche Menge, allerdings kann dies auch eine Konstante sein. Die Komponentenmenge wird in der Regel für die Produktion eines übergeordneten Artikels ausgedrückt, zur Vermeidung von Rundungsfehlern kann sie jedoch auch pro 100 oder pro 1000 Stück angegeben werden. Die Komponentenmenge kann auch basierend auf Messungen berechnet werden.
-   Stücklistenpositionsartikel: Ausschuss – Eine Komponente kann entweder eine variable oder eine konstante Menge für geplanten Ausschuss besitzen.
-   Stücklistenpositionsartikel: Gültigkeitsdaten – Eine Komponente kann über ein Gültigkeitsanfangs- und Gültigkeitsenddatum verfügen.
-   Stücklistenpositionsartikel: Produktionstyp – Die Abrechnungslosgröße für die Amortisierung konstanter Kosten enthält die Stücklistenberechnungsmenge sowie den Auflösungsmodus "Auf Auftrag fertigen", da für die Stücklistenberechnung angenommen wird, dass die produzierte Komponente nicht in der Standardauftragsmenge, sondern in der exakten Menge produziert wird.
-   Stücklistenversion für eine produzierte Komponente – Eine produzierte Komponente kann optional mit einer angegebenen Stücklistenversion versehen werden, die dann in einer Herstellkostenkalkulation anstelle der aktuellen aktiven Stücklistenversion des Artikels verwendet wird.
-   Arbeitsplanversion für eine produzierte Komponente – Eine produzierte Komponente kann optional mit einer angegebenen Arbeitsplanversion versehen werden, die dann in einer Herstellkostenkalkulation anstelle der aktuellen aktiven Arbeitsplanversion des Artikels verwendet wird.
-   Arbeitsgangnummer und die Auswirkung von Ausschussprozentsätzen auf den Arbeitsgang – Anhand der Arbeitsgangnummer wird eine Komponente mit einem bestimmten Arbeitsgang verknüpft; Arbeitsgänge können mit einem Ausschussprozentsatz versehen werden. Die Verknüpfung ermöglicht in Herstellkostenkalkulationen die Berücksichtigung von Ausschussprozentsätzen und kumulierten Ausschussprozentsätzen (plattformübergreifend) für die erforderliche Menge der Komponente.
-   Ignorieren des Stücklistenpositionsartikels in Kostenberechnungen – Eine Komponente kann bei der Herstellkostenkalkulation ignoriert werden.

Die betrieblichen Ressourceninformationen, die in einer Stücklistenberechnung für Standardkosten verwendet werden, umfassen Folgendes:
-   Stundenkosten – Die einer betrieblichen Ressource zugeordneten Stundenkosten werden als Kostenkategorien ausgedrückt, die Rüst- und Ausführungszeiten zugewiesen sind. Diese Kostenkategorien müssen für Ressourcengruppen und betriebliche Ressourcen gekennzeichnet sein. Die einer Kostenkategorie zugeordneten Stundenkosten können standortspezifisch sein oder unternehmensweit gelten.
-   Kosten pro Einheit - In manchen Produktionsumgebungen werden Kosten für betriebliche Ressourcen pro Ausgabeeinheit zugewiesen, was als andere Kostenkategorie für die Menge ausgedrückt werden würde. So können die mengenbezogenen Kosten beispielsweise Stücksätze für Arbeit reflektieren, oder ein Farbenhersteller kann betriebliche Ressourcenkosten  pro Gallone Ausgabe zuweisen.
-   Außerkraftsetzen von betrieblichen Ressourceninformationen für Arbeitsgänge des Arbeitsplans – Die Ressourceninformationen zu Kostenkategorien werden aus den Arbeitsgängen übernommen, wo sie außer Kraft gesetzt werden können. Für die Herstellkostenkalkulation werden die Kostenkategorieinformationen verwendet, die für die Arbeitsgänge des Arbeitsplans angegeben sind.
-   Kostengruppe für eine Kostenkategorie – Die einer Kostenkategorie zugewiesene Kostengruppe ermöglicht in den berechneten Kosten eines produzierten Artikels die Segmentierung von Kosten. So können beispielsweise unterschiedliche Kostengruppen verwendet werden, um die berechneten Kosten, die Maschinen und Arbeiten oder Rüst- und Ausführungszeiten zugeordnet sind, zu segmentieren.

Die Arbeitsplaninformationen, die in einer Herstellkostenkalkulation für Standardkosten verwendet werden, umfassen Folgendes:
-   Arbeitsplanversion – Die dem produzierten Artikel zugewiesene Arbeitsplanversion besitzt ein Gültigkeitsanfangs- und ein Gültigkeitsenddatum sowie einen Genehmigungs- und einen Aktivierungsstatus. Die Arbeitsplanversion kann unternehmensweit gelten oder standortspezifisch sein und optional Mengen-Breakpoints beinhalten.
-   Zeit für Arbeitsgang des Arbeitsplans – Die Zeit kann für Ausführungs- und für Rüstzeit angegeben werden. Die Stundenzeit wird in der Regel für die Produktion eines übergeordneten Artikels ausgedrückt, zur Vermeidung von Rundungsfehlern kann sie jedoch auch pro 100 oder pro 1000 Stück angegeben werden.
-   Zeit für Arbeitsgang des Arbeitsplans (Sekundärressourcen) – Eine Sekundärressource besitzt die gleiche Arbeitsgangnummer wie die Primärressource sowie die gleiche Zeit für den Arbeitsgang des Arbeitsplans. Ein Beispiel hierfür wäre ein Arbeitsgang, der als Primärressource eine Maschine und als Sekundärressourcen Arbeiten und Werkzeuge umfasst.
-   Arbeitsgang Ausschussprozentsatz − Stücklistenberechnungen für Ausschussprozentsätze und kumulierte Ausschussprozentsätze für mehrere Operationen. Dies gilt für die die erforderliche Zeit für Arbeitsplan-Arbeitsgänge und die erforderliche Menge für Komponenten, die mit Arbeitsgangnummern verknüpft werden.
-   Kostenkategorien für den Arbeitsgang des Arbeitsplans – Die betrieblichen Ressourceninformationen zu Kostenkategorien werden aus den Arbeitsgängen übernommen, wo sie außer Kraft gesetzt werden können. Für die Herstellkostenkalkulation werden die Kostenkategorieinformationen verwendet, die für die Arbeitsgänge des Arbeitsplans angegeben sind.

Die Informationen zu Produktionsgemeinkosten, die in einer Herstellkostenkalkulation für Standardkosten verwendet werden, umfassen Folgendes:
-   Zuschlag – Eine Zuschlagsberechnungsformel steht für den prozentualen Anteil eines Werts (beispielsweise 100 Prozent), der mit einer bestimmten Kostengruppe (beispielsweise "Arbeit") verknüpft ist.
-   Satz – Eine Satzberechnungsformel steht für den Betrag pro Einheit (beispielsweise EUR 10,00 pro Stunde), der mit einer bestimmten Kostengruppe (beispielsweise "Arbeit") verknüpft ist.
-   Zeitbasierte contra materialbasierte Gemeinkosten – Die Produktionsgemeinkosten können mit Arbeitsgängen des Arbeitsplans oder mit Materialkomponenten verknüpft werden.

Die Informationen zur Nachkalkulationsversion, die in einer Herstellkostenkalkulation für Standardkosten verwendet werden, umfassen Folgendes:
-   Nachkalkulationstyp – Die Nachkalkulationsversion muss Standardkosten beinhalten. Für Herstellkostenkalkulationen mit Standardkosten gelten eine Reihe von Einschränkungen. So wird durch diese Einschränkungen beispielsweise die Einbeziehung sonstiger Zuschläge in die Einheitenkosten sowie die Verwendung eines Auflösungsmodus für die Herstellkostenkalkulation vorgeschrieben, der lediglich eine einzelne Ebene aufweist.
-   Vorgegebenes Fallback-Prinzip – Durch die Nachkalkulationsversion kann die Verwendung eines Fallback-Prinzips vorgegeben werden (beispielsweise die Verwendung einer angegebenen Nachkalkulationsversion oder der aktiven Kostendatensätze). Das vorgegebene Fallback-Prinzip gilt üblicherweise für eine Nachkalkulationsversion, die in einem Zwei-Versionen-Ansatz für Kostenaktualisierungen die stufenweisen Aktualisierungen beinhaltet.
-   Sperrmarkierung für ausstehende Kosten – Durch eine Sperrmarkierung kann eine Herstellkostenkalkulation der ausstehenden Kosten für produzierte Artikel verhindert werden.
-   Angegebenes Anfangsdatum – Das angegebene Anfangsdatum fungiert für alle Herstellkostenkalkulationen mit der Nachkalkulationsversion als Standardberechnungsdatum.
-   Angegebener Standort – Durch Angabe eines Standorts wird die Herstellkostenkalkulation auf diesen Standort beschränkt.
-   Inhalt der Nachkalkulationsversion muss Kosten enthalten – Der Inhalt muss Kosten enthalten. Zur Berechnung der vorgeschlagenen Verkaufspreise für produzierte Artikel können optional auch Verkaufspreise enthalten sein.

Beim Initiieren der Herstellkostenkalkulation können eine Reihe von Informationsquellen angegeben werden. Hierzu zählen der Standort, das Berechnungsdatum sowie die Nachkalkulationsversion.






