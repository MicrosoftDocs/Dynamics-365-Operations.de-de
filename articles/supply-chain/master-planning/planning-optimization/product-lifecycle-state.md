---
title: Ausschließen von Produkten, die bestimmte Status im Produktlebenszyklus haben
description: In diesem Thema wird erklärt, wie Sie Produkte basierend auf ihrem Status im Lebenszyklus ausschließen können, wenn die Funktionalität der Planungsoptimierung verwendet wird.
author: ChristianRytt
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 030bdea7c03dd5eb3347c1d43acd1aeabdf566602872dd8ef5aab6d16b06f503
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739034"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Ausschließen von Produkten, die bestimmte Status im Produktlebenszyklus haben

[!include [banner](../../includes/banner.md)]

Freigegebene Produkte und freigegebene Produktversionen enthalten ein **Produktlebenszyklus-Status**-Feld. Mit diesem Feld können Sie u. a. steuern, welche Produkte bei der Produktprogrammplanung berücksichtigt werden. Sie können Lebenszyklusstatus nach Bedarf hinzufügen, entfernen und bearbeiten, indem Sie zu **Produktinformationsmanagement \> Einrichten \> Produktlebenszyklusstatus** gehen. Legen Sie für jeden Produktlebenszyklus-Status die Option **Ist aktiv für die Planung** auf *Ja* fest, wenn Produkte, die diesen Status haben, bei der Produktprogrammplanung berücksichtigt werden sollen. Wenn die Option auf *Nein* festgelegt ist, werden die zugehörigen Produkte und Varianten von der gesamten Produktprogrammplanung und allen Berechnungen auf Stücklisten-Ebene ausgeschlossen.

Freigegebene Produkte und Varianten, bei denen das Feld **Produktlebenszyklus-Status** leer gelassen wird, werden so behandelt, als hätten sie einen Produktlebenszyklus-Status, bei dem die Option **Ist für die Planung aktiv** auf *Ja* festgelegt ist. Mit anderen Worten: Sie werden bei der Produktprogrammplanung berücksichtigt.

> [!NOTE]
> Um unnötige Liefervorschläge zu vermeiden, empfehlen wir Ihnen dringend, alle veralteten freigegebenen Produkte und Varianten mit einem Produktlebenszyklus-Status zu verknüpfen, bei dem die Option **Ist aktiv für die Planung** auf *Nein* festgelegt ist. Diese Vorgehensweise ist besonders wichtig, wenn Sie mit Produktkonfigurationsvarianten arbeiten, die nicht wiederverwendbar sind, weil dadurch Verschwendung vermieden werden kann.

## <a name="related-resources"></a>Zugehörige Ressourcen

Weitere Informationen zu den Status im Produktlebenszyklus finden Sie unter [Übersicht über den Status im Produktlebenszyklus](../../pim/product-lifecycle.md).

Detaillierte Informationen mit Schritten zur Verwendung von Produktlebenszyklusstatus zum Ausschluss von Produkten aus der Produktprogrammplanung und Berechnungen auf Stücklistenebene finden Sie unter [Erstellen eines Produktlebenszyklusstatus zum Ausschluss von Produkten aus der Produktprogrammplanung](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]