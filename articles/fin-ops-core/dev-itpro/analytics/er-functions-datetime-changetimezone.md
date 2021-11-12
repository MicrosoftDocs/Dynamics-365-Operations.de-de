---
title: CHANGETIMEZONE ER-Funktion
description: In diesem Thema werden Informationen zur Verwendung von CHANGETIMEZONE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647935"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CHANGETIMEZONE` gibt den Wert *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) zurück, der aus einem vorgegebenen Datums-Uhrzeitwert in einer Zeitzone in einen Wert für Datum/Uhrzeit in einer anderen Zeitzone konvertiert wird.

## <a name="syntax"></a>Syntax

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumente

`datetime`: *DateTime*

Ein Datums-/Uhrzeitwert in der Zeitzone der koordinierten Weltzeit, der den zu konvertierenden Datums-/Uhrzeitwert darstellt.

`base time zone` *[Zeichenfolge](er-formula-supported-data-types-primitive.md#string)*

Der Name der Zeitzone, in die ein bestimmter Datums-/Uhrzeitwert vor der Konvertierung verschoben wird.

`target time zone`: *String*

Der Name der Zeitzone, in die ein konvertierter Datums-/Uhrzeitwert während der Konvertierung verschoben wird.

## <a name="return-values"></a>Rückgabewerte

*DateTime*

Der resultierende Datums-/Uhrzeitwert in der Zeitzone der koordinierten Weltzeit.

## <a name="usage-notes"></a>Anwendungshinweise

Um Quell- und Zielzeitzonen anzugeben, können Sie Zeitzonennamen verwenden, die bereitgestellt von der [ Internet Assigned Numbers Authority (IANA)](https://www.iana.org/) [bereitgestellt](https://data.iana.org/time-zones/releases/) werden oder die von Microsoft Windows [ unterstützt](/windows-hardware/manufacture/desktop/default-time-zones) werden.

Zur Laufzeit wird die Ausnahme „Zeitzone '\<time zone name\>' existiert nicht“ ausgelöst wenn der angegebene Name nicht in der IANA-Liste oder in der Windows-Registrierung gefunden wird.

Für Zeitzonen, in denen Sommerzeit gilt, berücksichtigt die Konvertierung den Offset der koordinierten Weltzeit-Sommerzeit. Bei der Konvertierung werden die neuesten verfügbaren Informationen zu diesem Offset verwendet.

## <a name="example-1"></a>Beispiel 1

In diesem Beispiel werden die Zeitzonennamen für Windows verwendet.

Sie konfigurieren die **DSX**-Datenquelle des Typs **Berechnetes Feld**. Sie enthält die folgenden Ausdrücke.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Wenn Sie den Ausdruck des der **DSY**-Datenquelle des Typs **Berechnetes Feld** als `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` konfigurieren, gibt die **DSX**-Datenquelle den Text **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00** zurück. Dieser Text zeigt, dass der Zeitunterschied zwischen den beiden angegebenen Zeitzonen am 1. Juni mehr als 24 Stunden beträgt. Daher liegt der konvertierte Datums-/Uhrzeitwert einen Tag früher als der angegebene Datums-/Uhrzeitwert, da die Basiszeitzone der Zielzeitzone voraus ist.

Wenn Sie den Ausdruck des der **DSY**-Datenquelle des Typs **Berechnetes Feld** als `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` konfigurieren, gibt die **DSX**-Datenquelle den Text **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00** zurück. Dieser Text zeigt, dass der Zeitunterschied zwischen den beiden angegebenen Zeitzonen am 1. Dezember weniger als 24 Stunden beträgt. Daher entspricht der konvertierte Datums-/Uhrzeitwert dem angegebenen Datums-/Uhrzeitwert.

> [!NOTE]
> Derselbe Ausdruck gibt eine unterschiedliche Varianz zwischen den bereitgestellten und konvertierten Datums-/Uhrzeitwerten für dasselbe Zeitzonenpaar zurück, da für die angegebenen Zeitzonen an einem bestimmten Datum/Uhrzeit ein unterschiedlicher Offset der koordinierten Weltzeit-Sommerzeit beobachtet wird.

## <a name="example-2"></a>Beispiel 2

In diesem Beispiel werden die IANA-Zeitzonennamen verwendet.

Sie konfigurieren die **DSX**-Datenquelle des Typs **Berechnetes Feld**. Sie enthält die folgenden Ausdrücke.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Wenn Sie den Ausdruck des der **DSY**-Datenquelle des Typs **Berechnetes Feld** als `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` konfigurieren, gibt die **DSX**-Datenquelle den Text **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00** zurück. Dieser Text zeigt, dass der Zeitunterschied zwischen den beiden angegebenen Zeitzonen am 1. Juni mehr als 24 Stunden beträgt. Daher liegt der konvertierte Datums-/Uhrzeitwert einen Tag früher als der angegebene Datums-/Uhrzeitwert, da die Basiszeitzone der Zielzeitzone voraus ist.

Wenn Sie den Ausdruck des der **DSY**-Datenquelle des Typs **Berechnetes Feld** als `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` konfigurieren, gibt die **DSX**-Datenquelle den Text **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00** zurück. Dieser Text zeigt, dass der Zeitunterschied zwischen den beiden angegebenen Zeitzonen am 1. Dezember weniger als 24 Stunden beträgt. Daher entspricht der konvertierte Datums-/Uhrzeitwert dem angegebenen Datums-/Uhrzeitwert.

## <a name="example-3"></a>Beispiel 3

Sie konfigurieren die **DSX**-Datenquelle des Typs **Berechnetes Feld**. Sie enthält die folgenden Ausdrücke.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Wenn Sie den Ausdruck des der **DSY**-Datenquelle des Typs **Berechnetes Feld** als `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` konfigurieren, gibt die **DSX**-Datenquelle den Text **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00** zurück. Dieser Text zeigt, dass der Zeitunterschied zwischen den beiden angegebenen Zeitzonen am 1. Juni mehr als 24 Stunden beträgt. Daher liegt der konvertierte Datums-/Uhrzeitwert einen Tag hinter der angegebene Datums-/Uhrzeitwert, da die Zielzeitzone der Basiszeitzone voraus ist.

## <a name="example-4"></a>Beispiel 4

Möglicherweise erhalten Sie einen Datums-/Zeitstempel von einer externen Quelle als Text, der keine Zeitzoneninformationen enthält. Möglicherweise kennen Sie jedoch die Zeitzone, in der die Quelle betrieben wird. Sie erhalten beispielsweise den Datums-/Zeitstempel **01/12/2021 12:55:00** von einem Dienst, der in Spanien betrieben wird. Um diesen Datums-/Uhrzeitwert korrekt in der Datenbank zu speichern, führen Sie die folgende Konvertierung durch:

- Konfigurieren Sie die **DSY**-Datenquelle des Typs **Berechnetes Feld**, um einen Datums-/Zeitstempel von Text in den Datums-/Zeitwert der koordinierten Weltzeit umzuwandeln.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Konfigurieren Sie die **DSX**-Datenquelle des Typs **Berechnetes Feld**, um den konvertierten Datums-/Uhrzeitwert in die koordinierte Weltzeit als Datums-/Uhrzeitwert der Zeitzone der externen Quelle zu verschieben.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Wenn Sie die `CHANGETIMEZONE`-Funktion für die Datums-/Uhrzeit-Konverntierung verwenden, beachten Sie, dass jeder Datums-/Uhrzeitwert in der Datenbank als Wert in der Zeitzone der koordinierten Weltzeit gespeichert wird. Bevor dieser Wert auf Anwendungsseiten dargestellt werden kann, wird er umgewandelt. Die Transformation berücksichtigt die Zeitzone, die als bevorzugte Zone für den aktuell angemeldeten Anwendungsbenutzer [festgelegt](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
