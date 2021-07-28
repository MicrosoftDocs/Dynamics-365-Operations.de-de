---
title: Berechnungen für Produktkonfigurationsmodelle
description: In diesem Thema wird beschrieben, wie Sie Berechnungen für Attribute in einem Produktkonfigurationsmodell erstellen
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f0806a5b36b04e77a5a6d10f3c2eb3d7ba680e75
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356415"
---
# <a name="product-configuration-model-calculations"></a>Berechnungen für Produktkonfigurationsmodelle

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Berechnungen für Attribute in einem Produktkonfigurationsmodell erstellen.

## <a name="prerequisites"></a>Voraussetzungen

Berechnungen werden in einem Produktkonfigurationsmodell verwendet, um die Konfigurationswerte für ein Produkt zu berechnen. Bevor Sie mit dem Einrichten von Berechnungen beginnen können, muss das zugehörige Produktkonfigurationsmodell vorhanden sein. Eine Übersicht über den Einrichtungsprozess für Konfigurationsmodelle und die damit verbundenen Aufgaben finden Sie unter [Produktkonfigurationsmodell einrichten](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Eine Berechnung erstellen

Eine Berechnung besteht aus einem Ausdruck und einem Zielattribut. Weitere Informationen finden Sie unter [Berechnungen für Produktkonfigurationsmodelle, FAQ](calculate-product-configuration-models.md).

Gehen Sie wie folgt vor, um eine Berechnung für ein vorhandenes Produktmodell zu erstellen.

1. Gehen Sie zu **Produktinformationsverwaltung \> Allgemein \> Produktkonfigurationsmodelle**.
1. Öffnen Sie ein Konfigurationsmodell und wählen Sie anschließend **Bearbeiten**.
1. Wählen Sie auf dem Inforegister **Berechnungen** **Hinzufügen**, um eine Berechnung hinzuzufügen, und legen Sie dann die folgenden Felder fest:

    - **Name** – Geben Sie einen Namen für die Berechnung ein.
    - **Beschreibung** – Geben Sie eine Beschreibung für die Berechnung ein.
    - **Zielattribut** – Wählen Sie das Attribut aus, für das Sie die Berechnung erstellen.

1. Wählen Sie **Ausdruck bearbeiten** aus.
1. Fügen Sie im Dialogfeld **Eine Berechnung eingeben** dem Ausdruck die erforderlichen Attribute, Operatoren und Werte hinzu. Weitere Informationen zum Arbeiten mit diesen Elementen finden Sie unter [Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen](expression-constraints-table-constraints-product-configuration-models.md).
1. Wenn Ihr Ausdruck fertig ist, wählen Sie **OK**.

## <a name="calculation-examples"></a>Berechnungsbeispiele

Dieser Abschnitt enthält einige Beispiele, die zeigen, wie Berechnungen funktionieren.

### <a name="example-1"></a>Beispiel 1

Das Zielattribut ist vom booleschen Typ und die Berechnung verwendet den folgenden Bedingungsausdruck:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Dieser Ausdruck gibt dem Zielattribut den Wert *Wahr* zurück, wenn `decimalAttribute2` größer oder gleich `decimalAttribute1` ist. Andernfalls gibt sie den Wert *falsch* zurück.

### <a name="example-2"></a>Beispiel 2

In diesem Beispiel wird das Textattribut `textFixedList` als Zielattribut verwendet. Dieses Attribut enthält die folgende feste Liste.

| Wert | Solver-Wert |
|---|---|
| K | 1a |
| Mrd | 2b |
| C | 2c |

Der folgende Screenshot zeigt, wie die Einstellungen für dieses Attribut in Ihrem System aussehen könnten.

![Attributtypeinstellungen für Beispiel 2.](media/model-calculations-example2.png "Attributtypeinstellungen für Beispiel 2")

Das Attribut wird in der folgenden Bedingungsanweisung verwendet:

`If[integerAttribute < 150, 0, 2]`

Wenn `integerAttribute` kleiner ist als 150, gibt diese Anweisung den Textwert des ersten Datensatzes in der festen Liste zurück – *A*. Andernfalls wird der Textwert des dritten Datensatzes in der festen Liste zurückgegeben – *C*.

> [!NOTE]
> Die feste Liste entspricht einer auf Null basierenden Aufzählung (enum). Auf ihre Werte wird über den entsprechenden Ganzzahlwert zugegriffen. Daher wird der erste Wert der festen Liste (*A*) *0* zugeordnet, der zweite Wert (*B*) *1* und der dritte Wert (*C*) *2*.

### <a name="example-3"></a>Beispiel 3

In diesem Beispiel wird das Zielattribut `textFixedList` aus dem letzten Beispiel verwendet. Es wird auch ein anderes Textattribut verwendet, `textAttribute`, das die folgende feste Liste enthält.

| Wert | Solver-Wert |
|---|---|
| AA | 1aa |
| BB | 2bb |

Der folgende Screenshot zeigt, wie die Einstellungen für dieses Attribut in Ihrem System aussehen könnten.

![Attributtypeinstellungen für Beispiel 3.](media/model-calculations-example3.png "Attributtypeinstellungen für Beispiel 3")

Der Wert für das Attribut `textFixedList` wird unter Verwendung der folgenden Bedingungsanweisung berechnet:

`If[textAttribute == "1aa", 0, 2]`

Wenn der Wert `textAttribute` einen Solver-Wert hat, der *1aa* entspricht, gibt dieser Ausdruck den Textwert des ersten Datensatzes in der festen Liste `textFixedList` zurück – *A*. Andernfalls wird der Textwert des dritten Datensatzes in der festen Liste `textFixedList` zurückgegeben – *C*.

> [!NOTE]
> - Die Bedingungsanweisung muss den Solver-Wert des Attributs verwenden.
> - Bei Berechnungen können nur Textattribute mit fester Liste verwendet werden.

## <a name="see-also"></a>Siehe auch

- [Berechnungen für Produktkonfigurationsmodelle, FAQ](calculate-product-configuration-models.md)
- [Einem Produktkonfigurationsmodell eine Ausdruckseinschränkung hinzufügen](tasks/add-expression-constraint-product-configuration-model.md)
- [Produktkonfigurationsmodelle – Überblick](product-configuration-models.md)
