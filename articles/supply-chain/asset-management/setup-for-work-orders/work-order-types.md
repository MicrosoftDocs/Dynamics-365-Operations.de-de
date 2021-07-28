---
title: Arbeitsauftragstypen
description: In diesem Thema werden die Arbeitsauftragsarten im Anlagenmanagement erläutert.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d89d7c652837e881f7fcb6014fe017eedc2f876c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351464"
---
# <a name="work-order-types"></a>Arbeitsauftragstypen

[!include [banner](../../includes/banner.md)]

 

Arbeitsauftragsarten werden zur Kategorisierung von Arbeitsaufträgen verwendet. Beispielsweise können Sie Arbeitsaufträge haben, die sich auf vorbeugende Instandhaltung oder korrektive Instandhaltung beziehen.

Ein Arbeitsauftragstyp definiert eine Zugehörigkeit zu einem Arbeitsauftrags-Lebenszyklusmodell. Ein Arbeitsauftrags-Lebenszyklusmodell definiert die Arbeitsauftrags-Lebenszykluszustände, die auf einem Arbeitsauftrag festgelegt werden können. (Beispiele für Lebenszykluszustände von Arbeitsaufträgen sind **Erstellt**, **In Bearbeitung** und **Fertig**.)

Weitere Informationen über den Lebenszyklus von Arbeitsaufträgen und Projektphasen finden Sie unter [Lebenszykluszustand von Arbeitsaufträgen](work-order-lifecycle-states.md).

1. Wählen Sie **Anlagenmanagement** \> **Einrichtung** \> **Arbeitsaufträge** \> **Arbeitsauftragsarten**.
2. Wählen Sie **Neu**, um einen Arbeitsauftragstyp anzulegen.
3. Geben Sie im Feld **Arbeitsauftragsart** eine ID für die Arbeitsauftragsart ein.
4. Geben Sie im Feld **Name** einen Namen ein.
5. Wählen Sie im Feld **Lebenszyklusmodell Arbeitsauftrag** ein Lebenszyklusmodell aus.
5. Setzen Sie die Option **Ein Wartungsarbeiter** auf **Ja**, wenn alle Arbeitsaufträge, die sich auf einen Arbeitsauftrag dieses Typs beziehen, auf denselben Wartungsarbeiter terminiert werden sollen.
6. Wählen Sie im Feld **Kostenart** **Korrektur**, **Präventiv** oder **Investition**. Alle Arbeitsaufträge auf einem Arbeitsauftrag müssen die gleiche Kostenart haben.
7. Setzen Sie im Abschnitt **Pflicht** die entsprechenden Optionen auf **Ja**, um festzulegen, welche fehler- oder wartungsbezogenen Informationen zu einem solchen Arbeitsauftrag hinzugefügt werden.

    > [!NOTE]
    > Die Optionen im Abschnitt **Pflicht** beziehen sich auf die Optionen auf der **Validieren** FastTab der **Lebenszykluszustände von Arbeitsaufträgen** Seite (**Anlagenmanagement** \> **Einrichtung** \> **Aufträge** \> **Lebenszykluszustände**).

8. Wählen Sie **Speichern** aus.

![Arbeitsauftragstypen.](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]