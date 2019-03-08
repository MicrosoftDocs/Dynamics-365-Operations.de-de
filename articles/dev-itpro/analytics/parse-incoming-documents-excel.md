---
title: Eingehende Dokumente im Excel-Format analysieren
description: In diesem Thema finden Sie Informationen über den Entwurf von Elektronischen Berichtsformaten (ER) zum Analysieren von Inhalten in eingehenden Microsoft Excel-Dateien.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367477"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="0ec87-103">Analysieren eingehender Dokumente im Excel-Format</span><span class="sxs-lookup"><span data-stu-id="0ec87-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0ec87-104">Sie können Elektronische Berichtsformate (ER) erstellen, um eingehende Microsoft Excel-Dateien zu analysieren, die Daten in Microsoft Excel-Arbeitsmappen darstellen (Dateien im XLSX-Format).</span><span class="sxs-lookup"><span data-stu-id="0ec87-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="0ec87-105">Sie können den Inhalt aus diesen Dateien dann verwenden, um Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0ec87-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="0ec87-106">Dies ist hilfreich, wenn Sie:</span><span class="sxs-lookup"><span data-stu-id="0ec87-106">This is useful if you:</span></span>

- <span data-ttu-id="0ec87-107">Ein neues Modell und Format entwerfen und diese zur Laufzeit testen wollen.</span><span class="sxs-lookup"><span data-stu-id="0ec87-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="0ec87-108">In diesem Fall simuliert Excel die eigentlichen Anwendungsdaten.</span><span class="sxs-lookup"><span data-stu-id="0ec87-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="0ec87-109">Verwalten Sie Daten außerhalb Ihrer Anwendung in Excel und importieren Sie diese Daten, um einen bestimmten Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ec87-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="0ec87-110">Um mehr über diese Funktion zu erfahren, führen Sie die Aufgabenleitfäden **ER Daten aus einer Microsoft Excel-Datei importieren (Teil 1: Entwerfen des Formats)** und **ER Daten aus einer Microsoft Excel-Datei importieren (Teil 2: Daten importieren)** aus (Teile des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses).</span><span class="sxs-lookup"><span data-stu-id="0ec87-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="0ec87-111">Diese Aufgabenleitfäden zeigen, wie die eingehende Excel-Datei analysiert werden kann, indem das ER-Format verwendet wird, um Informationen aus eingehenden Dokumenten zu importieren und Anwendungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0ec87-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="0ec87-112">Sie können die Dateien des Aufgabenleitfaden im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="0ec87-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="0ec87-113">Laden Sie die folgenden Dateien herunter, um die oben genannten Aufgabenleitfäden auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0ec87-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="0ec87-114">Inhaltsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0ec87-114">Content description</span></span>                         | <span data-ttu-id="0ec87-115">Datei</span><span class="sxs-lookup"><span data-stu-id="0ec87-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="0ec87-116">Eingehende Datei im .XLSX-Format - Vorlage</span><span class="sxs-lookup"><span data-stu-id="0ec87-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="0ec87-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="0ec87-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="0ec87-118">Eingehende Datei im .XLSX-Format - Beispieldaten</span><span class="sxs-lookup"><span data-stu-id="0ec87-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="0ec87-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="0ec87-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="0ec87-120">Wenn Sie den Aufgabenleitfaden [ER Erstellen der erforderlichen Konfigurationen, um Daten aus einer externen Datei zu importieren](./tasks/er-required-configurations-import-data.md) in der aktuellen Dynamics 365 for Finance and Operation-Anwendung noch nicht abgespielt haben, laden Sie die folgende Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="0ec87-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="0ec87-121">Inhaltsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0ec87-121">Content description</span></span>    | <span data-ttu-id="0ec87-122">Datei</span><span class="sxs-lookup"><span data-stu-id="0ec87-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="0ec87-123">ER Modellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0ec87-123">ER model configuration</span></span> | [<span data-ttu-id="0ec87-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="0ec87-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
