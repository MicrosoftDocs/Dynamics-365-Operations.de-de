---
title: "Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird"
description: "Dieses Thema enthält Informationen darüber, wie Sie das elektronische Meldung (ER)- Format ändern können, das verwendet wird, um Geschäftsdokumente zu generieren, indem eine geänderte Tabelle erneut angewendet wird."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: fca7fb75b965886c2ebc06b12940434f2ffc2543
ms.contentlocale: de-de
ms.lasthandoff: 02/27/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a><span data-ttu-id="b8012-103">Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird</span><span class="sxs-lookup"><span data-stu-id="b8012-103">Modify an Electronic reporting format by reapplying a Microsoft Excel template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b8012-104">Das elektronische Meldung (ER)- Tool wird verwendet, um Geschäftsdokumente in einem elektronischen Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b8012-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="b8012-105">Um ein Geschäftsdokument zu generieren, müssen Sie ein ER-Format erstellen und verwenden dann den ER-Designe, um das Layout des Geschäftsdokuments zu definieren und die Daten anzugeben, die im Modul implementierten einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8012-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="b8012-106">Sie können das ER-Format anschließend ausführen, um das Geschäftsdokument zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b8012-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="b8012-107">Das ER-Tool kann verwendet werden, um Geschäftsdokumente als Microsoft Excel-Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b8012-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="b8012-108">Sie können ein Excel-Dokument als Vorlage für diese Dokumente verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8012-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="b8012-109">Um das Dokumentlayout im ER-Designer zu definieren, können Sie den Inhalt des Excel-Dokuments importieren das als Vorlage für das festgelegte ER-Format verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b8012-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="b8012-110">Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Design einer Konfiguration zur Generierung von Berichten im OPENXML-WORD-Format** (Teil des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses) wieder.</span><span class="sxs-lookup"><span data-stu-id="b8012-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="b8012-111">Wenn Sie das Excel-Dokument bearbeiten, das als Vorlage für ein Geschäftsdokument verwendet wird, wenn neue ER-Funktionen Sie die aktualisierte Vorlage für den ER-Format erneut verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8012-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="b8012-112">Das ER-Format wird dann aktualisiert, damit sie die aktualisierte Vorlage verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8012-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="b8012-113">Weitere Informationen zu diesen Funktionen, siehe Aufgabenleitfaden **Ein elektronisches Berichterstellungsformat ändern, indem eine Microsoft Excel-Vorlage erneut angewendet wird** (Gehört zum 7.5.5.3 Acquire/Develop IT service/solution components (10683) Geschäftsprozess).</span><span class="sxs-lookup"><span data-stu-id="b8012-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="b8012-114">Als Teil des Schritts für das Importieren einer aktualisierten Vorlage im Aufgabenleitfaden, verwenden Sie die geänderte Vorlage des Zahlungsberichts SampleVendPaymWsReport2-Excel-Datei als Vorlage.</span><span class="sxs-lookup"><span data-stu-id="b8012-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

