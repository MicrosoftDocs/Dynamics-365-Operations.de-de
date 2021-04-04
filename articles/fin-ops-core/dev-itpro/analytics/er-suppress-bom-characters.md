---
title: Entwerfen von EB-Konfigurationen, um Zeichen von Bytereihenfolge-Marken in generierten Dateien zu unterdrücken
description: In diesem Thema wird erläutert, wie Sie ein EB-Format (elektronische Berichterstellung) konfigurieren, um Berichte zu generieren, die Zeichen von Bytereihenfolge-Marken unterdrücken.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9260db2edab75c9876ddf5af99bee4ff174c64e1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568972"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="c175b-103">Entwerfen von EB-Konfigurationen, um Zeichen von Bytereihenfolge-Marken in generierten Dateien zu unterdrücken</span><span class="sxs-lookup"><span data-stu-id="c175b-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c175b-104">Sie können eine [EB-](general-electronic-reporting.md)[Lösung](er-quick-start1-new-solution.md) entwerfen, um ausgehende Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c175b-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="c175b-105">Um die Dokumente als Text- oder XML-Dateien zu generieren, muss die Lösung eine EB-[Konfiguration](general-electronic-reporting.md#Configuration) enthalten, die eine EB-[Format-](general-electronic-reporting.md#FormatComponentOutbound)-Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="c175b-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="c175b-106">Um die [Zeichencodierung](https://docs.microsoft.com/windows/win32/intl/character-sets) anzugeben, die den Zeichensatz in generierten Dateien darstellt, muss das EB-Format das Formatelement **Allgemein\\Datei** enthalten.</span><span class="sxs-lookup"><span data-stu-id="c175b-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="c175b-107">Um die EB-Formatkomponente zu konfigurieren, öffnen Sie die [Entwurfs](general-electronic-reporting.md#component-versioning)version der erstellten EB-Konfiguration im EB-Format-Designer, und fügen Sie das Element **Allgemein\\Datei** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c175b-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="c175b-108">Geben Sie im Feld **Codierung** die Codierung ausgehender Dateien an, die zur Laufzeit mithilfe dieser Komponente generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c175b-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="c175b-109">Wenn das Format einen falschen Codierungsnamen enthält, wird ein Fehler ausgegeben, wenn Sie Ihre Änderungen an den Einstellungen des Formats speichern.</span><span class="sxs-lookup"><span data-stu-id="c175b-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Hinzufügen eines Stammelements auf der Seite „Formatdesigner“](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="c175b-111">Wenn Sie **UTF-8**, **UTF-16** oder **UTF-32** als Codierung angeben, wird die Option **Zeichen von Bytereihenfolge-Marken unterdrücken** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c175b-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="c175b-112">Setzen Sie diese Option auf **Ja**, um [Zeichen von Bytereihenfolge-Marken](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in ausgehenden Dateien zu unterdrücken, die zur Laufzeit generiert werden, wenn das bearbeitbare ER-Format ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c175b-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="c175b-113">Wenn Sie das Feld **Codierung** leer lassen, wird die Standardcodierung **UTF-8** verwendet.</span><span class="sxs-lookup"><span data-stu-id="c175b-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Festlegen der Option „Zeichen von Bytereihenfolge-Marken unterdrücken“ auf der Seite „Format-Designer“](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="c175b-115">Führen Sie die entsprechenden Schritte aus, um die Funktionalität zur Laufzeit zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c175b-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="c175b-116">Führen Sie beispielsweise die Schritte im Thema [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md) aus.</span><span class="sxs-lookup"><span data-stu-id="c175b-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="c175b-117">Nachdem Sie die Schritte im Abschnitt [Ändern des Formats, sodass die Berechnung auf der generierten Ausgabe basiert](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) dieses Themas abgeschlossen haben, befolgen Sie diese zusätzlichen Schritte.</span><span class="sxs-lookup"><span data-stu-id="c175b-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="c175b-118">Geben Sie die UTF-Codierung an:</span><span class="sxs-lookup"><span data-stu-id="c175b-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="c175b-119">Wählen Sie das Element **Bericht** des Typs **Allgemein\\Datei** aus.</span><span class="sxs-lookup"><span data-stu-id="c175b-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="c175b-120">Geben Sie im Feld **Codierung** die **UTF-8**-Codierung an.</span><span class="sxs-lookup"><span data-stu-id="c175b-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="c175b-121">Generieren Sie eine XML-Datei mit einem Zeichen von Bytereihenfolge-Marken:</span><span class="sxs-lookup"><span data-stu-id="c175b-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="c175b-122">Stellen Sie die Option **Zeichen von Bytereihenfolge-Marken unterdrücken** auf **Nein**, Zeichen von Bytereihenfolge-Marken in generierte XML-Dateien aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="c175b-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c175b-123">Führen Sie die Schritte im Abschnitt [Verzögern der Ausführung des XML-Elements „Zusammenfassung“, sodass die berechnete Gesamtsumme verwendet wird](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) des Themas [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md), und speichern Sie die generierte Datei als **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="c175b-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="c175b-124">Generieren Sie eine XML-Datei, die kein Zeichen von Bytereihenfolge-Marken enthält:</span><span class="sxs-lookup"><span data-stu-id="c175b-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="c175b-125">Stellen Sie die Option **Zeichen von Bytereihenfolge-Marken unterdrücken** auf **Ja**, um Zeichen von Bytereihenfolge-Marken in generierten XML-Dateien zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="c175b-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="c175b-126">Führen Sie die Schritte im Abschnitt [Verzögern der Ausführung des XML-Elements „Zusammenfassung“, sodass die berechnete Gesamtsumme verwendet wird](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) des Themas [Ausführung von XML-Elementen in ER-Formaten verzögern](er-defer-xml-element.md) aus, und speichern Sie die generierte Datei als **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="c175b-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="c175b-127">Vergleichen Sie in einem Dienstprogramm zum Dateivergleich die generierten Dateien.</span><span class="sxs-lookup"><span data-stu-id="c175b-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="c175b-128">Der erste Unterschied, den Sie bemerken werden, liegt in der Dateikopfzeile.</span><span class="sxs-lookup"><span data-stu-id="c175b-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="c175b-129">Die Datei „SampleXmlReport.xml“ enthält ein Zeichen von Bytereihenfolge-Marke, die Datei „SampleXmlReport(1).xml“ nicht.</span><span class="sxs-lookup"><span data-stu-id="c175b-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Vergleichen der generierten Dateien in einem Dienstprogramm zum Dateivergleich](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="c175b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c175b-131">See also</span></span>

- [<span data-ttu-id="c175b-132">Ausführung von XML-Elementen in ER-Formaten verzögern</span><span class="sxs-lookup"><span data-stu-id="c175b-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]