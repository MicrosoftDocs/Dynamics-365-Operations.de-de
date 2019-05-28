---
title: Abschreibungseffekte bei Rückbuchungen
description: Dieser Artikel behandelt mögliche Auswirkung beim Stornieren einer Anlagentransaktion.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d624fa998329680d9fa471fa325f6fcfd3920c6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556294"
---
# <a name="depreciation-effects-with-reversals"></a>Abschreibungseffekte bei Rückbuchungen

[!include [banner](../includes/banner.md)]

Dieser Artikel behandelt mögliche Auswirkung beim Stornieren einer Anlagentransaktion. 

Anlagenbuchungen können storniert werden. Gleiches gilt für die Buchungen, die einer Anlage zugeordnet sind. Darüber hinaus besteht die Möglichkeit zum Widerrufen stornierter Buchungen. 

Sie können eine Buchung stornieren oder widerrufen, bei der es sich nicht um den Posten handelt, der zuletzt in das Wertmodell oder in das Abschreibungsbuch der Anlage gebucht wurde. Prüfen Sie in diesem Fall zunächst, ob nach der zu stornierenden Buchungen bereits Abschreibungsbuchungen erfolgt sind. Dieser Schritt ist erforderlich, da Abschreibungen beim Stornieren einer Buchung nicht neu berechnet werden. Aus diesem Grund ist die Abschreibung nach einer Stornierung häufig zu hoch oder zu niedrig bewertet, was in den entsprechenden Beispielen veranschaulicht wird. 

Wenn eine Meldung mit dem Hinweis angezeigt wird, dass keine Neuberechnung der Abschreibung stattfindet, setzen Sie den Stornovorgang nicht fort, um eine korrekte Abschreibung zu gewährleisten. Stornieren Sie stattdessen zunächst die Abschreibungsbuchung, die nach der zu stornierenden Buchung erfolgt ist, und setzen Sie dann den eigentlichen Stornovorgang fort. Sie erhalten keinen Hinweis zur Neuberechnung der Abschreibung, und die Stornierung kann fortgesetzt werden. 

In den folgenden Beispielen werden die Berechnungen veranschaulicht, die ausgeführt werden, wenn der Vorgang ungeachtet der Warnmeldung und ohne vorherige Stornierung der Abschreibungsbuchungen fortgesetzt wird:

## <a name="example-1-depreciation-is-overstated"></a>Beispiel 1: Zu hohe Bewertung der Abschreibung
Eine Anlage ist mit einer Nutzungsdauer von fünf Jahren und mit einer linearen Abschreibung (60 Abschreibungsperioden) konfiguriert. In diesem Beispiel ergibt sich eine zu hohe Bewertung der Abschreibung.
#### <a name="asset-transaction-history"></a>Anlagenbuchungshistorie

| Datum       | Buchungstyp                                                          | Betrag                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. Januar  | Anschaffung                                                               | 59.000,00                                 |
| 1. Januar  | Anschaffungsänderung                                                    | 1.000,00                                  |
| 31. Januar | Abschreibung (unter Verwendung eines Vorschlags für eine Abschreibungsperiode) | 1.000,00; Berechnung: Buchwert (59.000 + 1.000) / Anzahl der verbleibenden Abschreibungsperioden (60) |

#### <a name="reversal-action"></a>Storno

| Datum      | Transaktionstyp                | Betrag    |
|-----------|---------------------------------|-----------|
| 1. Januar | Storno der Anschaffungsänderung | -1.000,00 |

#### <a name="depreciation-effect"></a>Abschreibungseffekt

| Datum        | Transaktionstyp        | Betrag                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. Februar | Abschreibung (Vorschlag) | 983,05; Berechnung: Buchwert (59.000 - 1.000 Abschreibung) / Anzahl der verbleibenden Abschreibungsperioden (59) |

Die Abschreibung ist um 16,95 (1.000 - 983,05) zu hoch bewertet.

## <a name="example-2-depreciation-is-understated"></a>Beispiel 2: Zu niedrige Bewertung der Abschreibung
Eine Anlage ist mit einer Nutzungsdauer von fünf Jahren und mit einer linearen Abschreibung (60 Abschreibungsperioden) konfiguriert. In diesem Beispiel ergibt sich eine zu niedrige Bewertung der Abschreibung.
#### <a name="asset-transaction-history"></a>Anlagenbuchungshistorie

| Datum       | Buchungsart                                                          | Betrag                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. Januar  | Anschaffung                                                               | 59.000,00                                   |
| 1. Januar  | Regulierung vom Typ "Niedrigerbewertung"                                                     | 1.000,00                                    |
| 31. Januar | Abschreibung (unter Verwendung eines Vorschlags für eine Abschreibungsperiode) | 966,67; Berechnung: Buchwert (59.000 – 1.000) / Anzahl der verbleibenden Abschreibungsperioden (60) |

#### <a name="reversal-action"></a>Storno

| Datum      | Transaktionstyp               | Betrag    |
|-----------|--------------------------------|-----------|
| 1. Januar | Storno der Regulierung vom Typ "Niedrigerbewertung" | -1.000,00 |

#### <a name="depreciation-effect"></a>Abschreibungseffekt

| Datum        | Transaktionstyp        | Betrag                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. Februar | Abschreibung (Vorschlag) | 983,62; Berechnung: Buchwert (59.000 - 966,67 Abschreibung) / Anzahl der verbleibenden Abschreibungsperioden (59) |

Die Abschreibung ist um 16,95 (983,62 - 966,67) zu niedrig bewertet.



<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Anlagenabschreibung](fixed-asset-depreciation.md)



