---
title: Manuelle Abschreibung
description: Dieser Artikel enthält eine Übersicht der manuellen Abschreibungsmethode.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3545b863f14ac9553563caa9b6e57443ea378536
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723194"
---
# <a name="manual-depreciation"></a>Manuelle Abschreibung

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht der manuellen Abschreibungsmethode.

Wenn Sie ein Anlagenabschreibungsprofil einrichten und auf der Seite **Abschreibungsprofile** im Feld **Methode** die Option **Manuell** auswählen, entspricht die Abschreibung von Anlagen, die diesem Abschreibungsprofil zugeordnet sind, dem Prozentsatz, den Sie für jedes Intervall im Kalenderjahr eingeben. Die Intervalle, für die Sie Prozentsätze einrichten, werden gemäß Ihrer Auswahl auf der Seite **Abschreibungsprofile** auf dem Inforegister **Allgemeines** im Feld **Periodenhäufigkeit** gebucht. Folgende Werte stehen zur Auswahl:

- Jährlich
- Monatlich
- Vierteljährlich
- Halbjährlich
- Täglich

Klicken Sie nach Auswahl der Periodenhäufigkeit auf **Manuelle Zeitpläne**, und richten Sie Prozentsätze für jedes Buchungsintervall ein. Die manuellen Zeitpläne und die Buchungsintervalle definieren zusammen den Abschreibungsbetrag (siehe Beispiele weiter unten in diesem Artikel). Die manuelle Abschreibung wird immer als Prozentsatz des Anschaffungspreises berechnet. Für manuellen Abschreibung müssen die von Ihnen für die Abschreibungsintervalle eingegebenen Prozentsätze nicht unbedingt 100 Prozent ergeben. Bei manueller Abschreibung handelt es sich um eine flexible Abschreibungsmethode, die häufig verwendet wird, um auf der Seite **Bücher** ein außerordentliches Abschreibungsprofil zu definieren – beispielsweise eine nicht periodische Abschreibung für besondere (ggf. steuerliche) Zwecke.

## <a name="examples"></a>Beispiele
Anschaffungspreis: 11.000,00 Euro; Erwarteter Schrottwert: 1.000,00 Euro. Folgende Tabelle zeigt die Intervalle und Prozentsätze, die Sie auf der Seite **Zeitplan für Anlagenabschreibungsprofil** einrichten.

| Intervallnummer | Prozentsatz |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Die folgende Tabelle zeigt, wie die Abschreibung für jedes Intervall berechnet wird.

|  Intervallnummer | Berechnung des jährlichen Abschreibungsbetrags | Nettobuchwert am Ende des Intervalls |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11.000 – 1.000) × 10 % = 1.000                | 10.000 (11.000 – 1.000)                   |
| 2                | (11.000 – 1.000) × 50 % = 5.000                | 5.000 (10.000 – 5.000)                    |
| 3                | (11.000 – 1.000) × 8 % = 800                   | 4.200 (5.000 – 800)                       |

Wenn Sie im Feld **Periodenhäufigkeit** die Option **Monatlich** auswählen, haben Sie im manuellen Zeitplan 12 Intervalle eingerichtet. Die folgende Tabelle zeigt die Abschreibungsbeträge für die ersten beiden Intervalle.

| Intervall | Abschreibungsbetrag            |
|----------|--------------------------------|
| Januar  | (11.000 – 1.000) × 10 % = 1.000 |
| Februar | (11.000 – 1.000) × 50 % = 5.000 |

Wenn Sie <strong>Halbjährlich</strong> im Feld *<strong><em>Periodenhäufigkeit</em>*</strong> auswählen, richten Sie zwei manuelle Zeitplanintervalle ein. Die folgende Tabelle zeigt die Abschreibungsbeträge für diese beiden Intervalle.

| Intervall    | Abschreibungsbetrag            |
|-------------|--------------------------------|
| 30. Juni     | (11.000 – 1.000) × 10 % = 1.000 |
| 31. Dezember | (11.000 – 1.000) × 50 % = 5.000 |

Die Summe der Prozentsätze für alle Intervalle muss nicht unbedingt 100 ergeben. Allerdings wird eine Meldung angezeigt, wenn der Wert im Feld **Kumulierter Prozentsatz** Feld auf der Seite **Zeitplan für Anlagenabschreibungsprofil** ist nicht **100**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
