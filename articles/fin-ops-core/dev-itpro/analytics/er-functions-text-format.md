---
title: FORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FORMAT-Funktion bei der elektronischen Berichterstellung bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df158e80bd1c11832376678a631a9e0e162534ad
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915716"
---
# <a name="FORMAT">FORMAT EB-Funktion</a>

[!include [banner](../includes/banner.md)]

Die Funktion `FORMAT` gibt den angegebenen Zeichenfolgenwert mit dem Wert *String* zurück, nachdem sie durch Ersetzen sämtlicher Vorkommnisse von **%N** durch das *N*. Argument formatiert wurde.

## <a name="syntax"></a>Syntax

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumente

`string`: *String*

Ein Verweis auf die Datenquelle des Typs *String*, die formatiert werden muss. Dieses Argument ist erforderlich.

`argument 1`: *String*

Das erste Argument, das verwendet wird, um Vorkommnisse von **%1** zu ersetzen. Dieses Argument ist erforderlich.

`argument N`: *String*

Das *N*. Argument, das verwendet wird, um Vorkommnisse von **%2**, **%3** usw. zu ersetzen. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn eine Anfrage nicht für einen Parameter angegeben wird, wird der Parameter als **"%N"** in der Zeichenfolge zurückgegeben. Für Werte für den Typ *Real*, wird die Standard-Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.

## <a name="example"></a>Beispiel

In der folgenden Abbildung gibt die Datenquelle **PaymentModel** eine Liste der Kundendatensätze zurück, indem die Komponente **Debitor** verwendet wird. Sie gibt den Wert des Verarbeitungsdatums über das Feld **ProcessingDate** zurück.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Im Format für die elektronische Berichterstellung (EB), das entworfen wurde, um eine Datei für ausgewählte Debitoren zu generieren, wird **PaymentModel** als Datenquelle ausgewählt, um den Prozessablauf zu steuern. Wenn ein ausgewählter Debitor zu dem Datum angehalten wird, an dem der Bericht verarbeitet wird, wird zur Benachrichtigung des Benutzers eine Ausnahme ausgelöst. Die Formel, die für diese Art von Prozesssteuerung entworfen wurde, kann die folgenden Ressourcen verwenden:

- Beschriftung SYS70894, die den folgenden Text hat:

    - **Für die EN-US-Sprache:** "Nichts zu drucken"
    - **Für deutsche Sprache:** "Nichts zu drucken"

- Beschriftung SYS18389, die den folgenden Text hat:

    - **Für die Sprache EN-US:** "Debitor %1 wird für %2 beendet."
    - **Für die Sprache DE:** "Debitor '%1' wird für %2 gesperrt."

Hier ist der Ausdruck, der gestaltet werden kann.

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Wenn ein Bericht für den Kunden **Litware Retail** am 17. Dezember 2015 in der **EN-US**-Kultur und in der **EN-US**-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der dann als Ausnahmenachricht für den Benutzer präsentiert werden kann:

*Nichts zu drucken. Debitor Litware Retail wird am 12/17/2015 beendet.*

Wenn derselbe Bericht für den Kunden **Litware Retail** am 17. Dezember 2015 in der **DE**-Kultur und in der **DE**-Sprache verarbeitet wird, gibt diese Formel den folgenden Text zurück, der ein anderes Datumsformat verwendet:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Die folgende Syntax wird in EB-Formeln für Beschriftungen angewendet:
>
> - **Für Bezeichnungen aus Ressourcen in der Microsoft Dynamics 365 Finance-App:** **@X**, wobei **X** die Bezeichnungs-ID in der Entwicklungsumgebung ist.
> - **Für Bezeichnungen in EB-Konfigurationen:** **@"GER_LABEL:X"**, wobei **X** die Bezeichnungs-ID in der EB-Konfiguration ist

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
