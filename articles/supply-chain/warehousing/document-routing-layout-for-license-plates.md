---
title: Dokumenten-Routing-Layout für Kennzeichenetiketten
description: In diesem Thema wird beschrieben, wie Formatierungsmethoden zum Drucken von Werten auf Etiketten verwendet werden.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 7c20d3d0540f8f1a05928df9aff5253745982da9
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558261"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="3de52-103">Dokumenten-Routing-Layout für Kennzeichenetiketten</span><span class="sxs-lookup"><span data-stu-id="3de52-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3de52-104">Das Layout des Dokumentroutings definiert das Layout der Kennzeichenetiketten und die darauf gedruckten Daten.</span><span class="sxs-lookup"><span data-stu-id="3de52-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="3de52-105">Sie konfigurieren die Druckauslöserpunkte, wenn Sie Menüelemente und Arbeitsvorlagen für mobile Geräte einrichten.</span><span class="sxs-lookup"><span data-stu-id="3de52-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="3de52-106">In einem typischen Szenario drucken Lagerempfänger unmittelbar nach der Aufzeichnung des Inhalts von Paletten, die im Empfangsbereich eintreffen, Kennzeichenetiketten.</span><span class="sxs-lookup"><span data-stu-id="3de52-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="3de52-107">Die physischen Etiketten werden auf die Paletten aufgebracht.</span><span class="sxs-lookup"><span data-stu-id="3de52-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="3de52-108">Sie können dann zur Validierung als Teil des folgenden Einlagerungsprozesses und zukünftiger ausgehender Kommissioniervorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3de52-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="3de52-109">Sie können hochkomplexe Etiketten drucken, vorausgesetzt, das Druckgerät kann den an das Gerät gesendeten Text interpretieren.</span><span class="sxs-lookup"><span data-stu-id="3de52-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="3de52-110">Beispielsweise kann ein ZPL-Layout (Zebra Programming Language), das einen Barcode enthält, dem folgenden Beispiel ähneln.</span><span class="sxs-lookup"><span data-stu-id="3de52-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="3de52-111">Im Rahmen des Etikettendruckprozesses wird der Text `$LicensePlateId$` in diesem Beispiel durch einen Datenwert ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3de52-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="3de52-112">Um die Werte anzuzeigen, die gedruckt werden sollen, gehen Sie zu **Lagerverwaltung \> Anfragen und Berichte \> Kennzeichenetiketten**.</span><span class="sxs-lookup"><span data-stu-id="3de52-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="3de52-113">Mithilfe verschiedener weit verbreiteter Tools zur Etikettengenerierung können Sie den Text für das Etikettenlayout formatieren.</span><span class="sxs-lookup"><span data-stu-id="3de52-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="3de52-114">Viele dieser Tools unterstützen das `$FieldName$` Format.</span><span class="sxs-lookup"><span data-stu-id="3de52-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="3de52-115">Darüber hinaus verwendet Microsoft Dynamics 365 Supply Chain Management eine spezielle Formatierungslogik als Teil der Feldzuordnung für das Dokumentrouting-Layout.</span><span class="sxs-lookup"><span data-stu-id="3de52-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="3de52-116">Schalten Sie diese Funktion für Ihr System ein</span><span class="sxs-lookup"><span data-stu-id="3de52-116">Turn on this feature for your system</span></span>

<span data-ttu-id="3de52-117">Wenn Ihr System nicht bereits die in diesem Thema beschriebenen Funktionen enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Erweiterte Layouts für Ladungsträger* ein.</span><span class="sxs-lookup"><span data-stu-id="3de52-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="3de52-118">Benutzerdefinierte Zahlenformate</span><span class="sxs-lookup"><span data-stu-id="3de52-118">Custom number formats</span></span>

<span data-ttu-id="3de52-119">Sie können die Formatierung der gedruckten numerischen Feldwerte mithilfe von Codes im folgenden Format anpassen.</span><span class="sxs-lookup"><span data-stu-id="3de52-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="3de52-120">Hier ist eine Erklärung für dieses Format:</span><span class="sxs-lookup"><span data-stu-id="3de52-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="3de52-121">`FieldName` ist der Name des Datenfeldes (z. B. **Menge**).</span><span class="sxs-lookup"><span data-stu-id="3de52-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="3de52-122">`FormatString` definiert, wie die Daten gedruckt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3de52-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="3de52-123">Die folgenden Beispiele zeigen, wie Sie die Arbeitsmenge anpassen können (**Menge**) Feld:</span><span class="sxs-lookup"><span data-stu-id="3de52-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="3de52-124">Um immer vier Ziffern anzuzeigen (indem Sie Nullen als Platzhalter verwenden), verwenden Sie `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="3de52-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="3de52-125">Wenn die Menge beispielsweise 10 ist, wird auf dem Etikett 0010 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3de52-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="3de52-126">Um immer zwei Dezimalstellen anzuzeigen, verwenden Sie `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="3de52-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="3de52-127">Wenn die Menge beispielsweise 10 ist, wird auf dem Etikett 10.00 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3de52-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="3de52-128">Eine vollständige Liste der verfügbaren Zeichenfolgen im Zahlenformat finden Sie unter [Benutzerdefinierte Zeichenfolgen im numerischen Format](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="3de52-128">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="3de52-129">Benutzerdefinierte Zeichenfolgenformate</span><span class="sxs-lookup"><span data-stu-id="3de52-129">Custom string formats</span></span>

<span data-ttu-id="3de52-130">Sie können die ersten Zeichen einer Zeichenfolge mithilfe des folgenden Feld- und Formatcodes entfernen.</span><span class="sxs-lookup"><span data-stu-id="3de52-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="3de52-131">Hier, `#` gibt die Anzahl der zu überspringenden Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="3de52-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="3de52-132">Verwenden Sie beispielsweise `$LicensePlateId:2..$`, um Serien-Versandcontainercode (SSCC) Kennzeichennummer zu drucken, das die ersten beiden Zeichen nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="3de52-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="3de52-133">In diesem Fall wird das Kennzeichen 0011111111111222221 als 11111111111222221 gedruckt.</span><span class="sxs-lookup"><span data-stu-id="3de52-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="3de52-134">Benutzerdefinierte Datums-/Uhrzeitformate</span><span class="sxs-lookup"><span data-stu-id="3de52-134">Custom date/time formats</span></span>

<span data-ttu-id="3de52-135">Das folgende Beispiel zeigt, wie Sie das Format steuern können, das zum Drucken von Datumsangaben verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3de52-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="3de52-136">In diesem Beispiel wird das Datum 30. April 2020 als 30-04-2020 gedruckt.</span><span class="sxs-lookup"><span data-stu-id="3de52-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="3de52-137">Eine vollständige Liste der verfügbaren Datums-/Zeitformate finden Sie unter [Benutzerdefinierte Datum-/Zeitformatzeichenfolgen](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="3de52-137">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="3de52-138">Drucken Sie einzelne Zeilen aus mehrzeiligen Daten</span><span class="sxs-lookup"><span data-stu-id="3de52-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="3de52-139">Wenn ein Datenfeld mehrere Zeilen enthält (d.h Zeilen, die durch Zeilenumbrüche getrennt sind), können Sie eine einzelne Zeile im folgenden Format drucken.</span><span class="sxs-lookup"><span data-stu-id="3de52-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="3de52-140">Hier ist `#` die Zeilennummer, die Sie drucken möchten.</span><span class="sxs-lookup"><span data-stu-id="3de52-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="3de52-141">(Verwenden Sie 1 für die erste Zeile.)</span><span class="sxs-lookup"><span data-stu-id="3de52-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="3de52-142">Zum Beispiel hat Ihr System ein Feld `AdditionalAddress`, in dem die folgende mehrzeilige Adresse gespeichert ist:</span><span class="sxs-lookup"><span data-stu-id="3de52-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="3de52-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="3de52-143">Contoso Inc.</span></span>  
<span data-ttu-id="3de52-144">123 Straßenname</span><span class="sxs-lookup"><span data-stu-id="3de52-144">123 Street Name</span></span>  
<span data-ttu-id="3de52-145">Eine Stadt, ein Staat</span><span class="sxs-lookup"><span data-stu-id="3de52-145">Some City, Some State</span></span>

<span data-ttu-id="3de52-146">Sie können diese Adresse zeilenweise mit den folgenden Codes drucken.</span><span class="sxs-lookup"><span data-stu-id="3de52-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="3de52-147">Code</span><span class="sxs-lookup"><span data-stu-id="3de52-147">Code</span></span> | <span data-ttu-id="3de52-148">Text, der gedruckt wird</span><span class="sxs-lookup"><span data-stu-id="3de52-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="3de52-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="3de52-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="3de52-150">123 Straßenname</span><span class="sxs-lookup"><span data-stu-id="3de52-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="3de52-151">Eine Stadt, ein Staat</span><span class="sxs-lookup"><span data-stu-id="3de52-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="3de52-152">Drucken und Formatieren über eine Anzeigemethode</span><span class="sxs-lookup"><span data-stu-id="3de52-152">Print and format from a display method</span></span>

<span data-ttu-id="3de52-153">Sie können von einer Anzeigemethode aus im folgenden Format drucken.</span><span class="sxs-lookup"><span data-stu-id="3de52-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="3de52-154">Sie können dieses Format mit anderen Typen kombinieren, die weiter oben in diesem Thema beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="3de52-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="3de52-155">Sie haben beispielsweise eine Anzeigemethode mit dem Namen `DisplayListOfItemsNumbers()`, und Sie möchten die erste Artikelnummer dieser Methode drucken.</span><span class="sxs-lookup"><span data-stu-id="3de52-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="3de52-156">In diesem Fall können Sie folgenden Code verwenden.</span><span class="sxs-lookup"><span data-stu-id="3de52-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="3de52-157">Weitere Informationen zum Drucken von Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="3de52-157">More information about how to print labels</span></span>

<span data-ttu-id="3de52-158">Weitere Informationen zum Einrichten und Drucken von Etiketten finden Sie unter [Aktivieren Sie das Drucken von Kennzeichnungsetiketten](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="3de52-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]