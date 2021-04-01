---
title: Behebung von Problemen mit dem Produktkonfigurator
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit dem Produktkonfigurator auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d17d9f16f01a68da724751273b7d137a0f0f14de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248762"
---
# <a name="troubleshoot-the-product-configurator"></a>Behebung von Problemen mit dem Produktkonfigurator

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit dem Produktkonfigurator auftreten können.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Element-Text wird überschrieben, wenn ich ein Produkt in einer Zeile eines Verkaufsauftrags konfiguriere.

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem tritt auf, wenn Sie eine Verkaufsauftragszeile für einen konfigurierbaren Artikel erstellen und dann den Artikeltext ändern. Wenn Sie den Artikel konfigurieren und dann **OK** wählen, wird der Text mit dem Standardtext überschrieben.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten wird erwartet. Das Textfeld enthält den Variantennamen, der erst ausgefüllt wird, nachdem Sie die Zeile konfiguriert haben. Daher müssen Sie den Text ändern, nachdem Sie die Zeile konfiguriert haben, nicht vorher.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Ganzzahlige Attribute werden bei der Berechnung von Produktkonfigurationsmodellen falsch gerundet.

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem kann auftreten, wenn Sie die folgende Reihe von Aktionen durchführen:

1. Legen Sie die folgenden Attribute in einem Produktkonfigurationsmodell fest:

    - Eingabe (ganzzahlig)
    - Prozentsatz (dezimal)
    - Ergebnis (ganzzahlig)

2. Erstellen Sie eine Formel, die den folgenden Ausdruck hat:

    *Ergebnis* = *Eingabe* × *Prozent* ÷ 100

In diesem Fall wird das ganzzahlige Ergebnis nicht immer korrekt gerundet. Zum Beispiel ist die Eingabe 1.000, und der Prozentsatz ist 2,40. Daher erwarten Sie, dass das ganzzahlige Ergebnis 24 ist, denn 2,40 Prozent von 1.000 ist 24 (oder 24,00 in dezimaler Form). Stattdessen wird das Ergebnis als 23 angezeigt. Wenn der Prozentsatz jedoch 2,39 beträgt, wird die Berechnung auf 24 anstelle von 23 gerundet. Wenn der Prozentsatz 2,50 beträgt, wird die Berechnung wie erwartet auf 25 gerundet.

### <a name="issue-resolution"></a>Problemlösung

Dieses Problem tritt aufgrund der Art und Weise auf, wie Microsoft Solver Foundation intern Zahlen unter Verwendung von Brüchen darstellt. Im vorangegangenen Beispiel wird das Ergebnis der Berechnung, bei der der Prozentsatz 2,40 beträgt, als 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375 dargestellt. Wenn .NET diesen Wert in eine Ganzzahl umwandelt, wird 23 zurückgegeben.

Dieses Verhalten wird nicht geändert, da andere Szenarien davon abhängen. Für das vorangegangene Beispiel können Sie das Problem beheben, indem Sie ein zusätzliches Dezimalattribut und eine Berechnung einführen.

Sie können zum Beispiel die folgenden Attribute in einem Produktionskonfigurationsmodell festlegen:

- Eingabe (ganzzahlig)
- Prozentsatz (dezimal)
- ResultDecimal (dezimal)
- ResultInteger (ganzzahlig)

Sie können dann die folgenden Berechnungen hinzufügen:

- *ResultDecimal* = *Eingabe* × *Prozent* ÷ 100
- *ResultInteger* = *ResultDecimal*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]