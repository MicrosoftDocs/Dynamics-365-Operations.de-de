---
title: Allgemeine Ursachen für Produktionsabweichungen
description: In diesem Artikel werden verschiedene typische Quellen jedes Typs einer Produktionsabweichung beschrieben.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce352db56fe41264562fd11260f9fa91931babeeb62d352327a588fb622492d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766193"
---
# <a name="common-sources-of-production-variances"></a>Allgemeine Ursachen für Produktionsabweichungen

[!include [banner](../includes/banner.md)]

In diesem Artikel werden verschiedene typische Quellen jedes Typs einer Produktionsabweichung beschrieben. 

Nachfolgend sind einige typische Quellen einer **Losgrößen** abweichung:

-   Die Gutmenge eines Produktionsauftrags unterscheidet sich von der Berechnungsmenge, die für die Standardkostenberechnung verwendet wird. Die Menge bildet die Grundlage für die Amortisierung konstanter Kosten.
-   Der Wert der konstanten Kosten im Produktionsauftrag unterscheidet sich von den konstanten Kosten in der Standardkostenberechnung. Die Abweichung der konstanten Kosten im Produktionsauftrag kann unterschiedliche Ursachen haben. Beispielsweise beinhalteten die konstanten Kosten möglicherweise die folgenden Faktoren:
    -   Manuelle Änderungen an der Stückliste oder am Arbeitsplan für die Produktion
    -   Auswahl einer anderen Stücklisten- oder Arbeitplanversion beim Erstellen des Produktionsauftrags
    -   Geplante Änderungen an der dem Artikel zugewiesenen Stücklisten- oder Arbeitsplanversion

Nachfolgend sind einige typische Quellen einer **Produktionpreis** abweichung:

-   Die Kostenkategorie (und der entsprechende Kostenkategoriepreis) für den gemeldeten Verbrauch eines Arbeitsplan-Arbeitsgangs unterscheidet sich von der Kostenkategorie, die in der Standardkostenberechnung verwendet wird.
-   Die aktiven Kosten für den Kostenkategoriepreis unterscheiden sich vom Kostenkategoriepreis, der in der Standardkostenberechnung verwendet wird.

Nachfolgend sind einige typische Quellen einer **Produktionsmengen** abweichung:

-   Zu hoher oder zu geringer Abgang einer Materialkomponente.
-   Über- oder unterbewerteter Bericht der Zeit für einen Routing-Arbeitsgang.
-   Über- oder Unterempfang der Warenmenge des übergeordneten Artikels, relativ zur Auftragsmenge. Sie melden aber Komponenten und Meldungen zu Arbeitsgängen als abgeschlossen, basierend auf der Menge für den Produktionsauftrag.

Nachfolgend sind einige typische Quellen einer **Produktionsersatz** abweichung:

-   Abgang einer Materialkomponente, die sich nicht in der Produktionsstückliste befindet.
-   Manuelles Hinzufügen einer Komponente zur Produktionsstückliste und Melden der Komponente als verbraucht.
-   Melden eines Artikels als verbraucht, ohne ihn manuell der Produktionsstückliste hinzuzufügen.
-   Manuelles Hinzufügen eines Arbeitsgangs zum Produktionsarbeitsplan und Melden des Arbeitsgangs als verbraucht.
-   Auswählen einer anderen Stücklistenversion beim Erstellen des Produktionsauftrags, die sich von der in der Standardkostenberechnung verwendeten Stücklistenversion unterscheidet.
-   Auswählen einer anderen Arbeitsplanversion beim Erstellen des Produktionsauftrags, die sich von der in der Standardkostenberechnung verwendeten Arbeitsplanversion unterscheidet.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]