---
title: Analysieren eingehender Dokumente im JSON-Format
description: In diesem Thema wird erläutert, wie Sie elektronische Berichterstattungsformate (ER) einrichten, um eingehende Dokumente im JavaScript Object Notation (JSON) Format zu analysieren.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703920"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="225bf-103">Analysieren eingehender Dokumente im JSON-Format</span><span class="sxs-lookup"><span data-stu-id="225bf-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="225bf-104">Sie können elektronische Berichterstattungsformate (ER) entwerfen, um eingehende elektronische Dokumente zu analysieren, die Daten in einem Textformat darstellen, das auf JavaScript basiert (das heißt, Dateien in JavaScript Object Notation \[JSON\] Format).</span><span class="sxs-lookup"><span data-stu-id="225bf-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="225bf-105">Um mehr über diese Funktion zu erfahren, laden Sie die Dateien in die folgende Tabelle, und führen Sie den ER Konfigurationsformat erstellen aus, um Daten aus externen JSON-Dateiaufgabenleitfaden zu importieren.</span><span class="sxs-lookup"><span data-stu-id="225bf-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="225bf-106">Dieser Aufgabenleitfaden veranschaulicht, wie ein ER-Format verwendet werden kann, um eine eingehende JSON-Datei zu analysieren, um Bewerbungsdaten zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="225bf-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="225bf-107">Titel</span><span class="sxs-lookup"><span data-stu-id="225bf-107">Title</span></span>                                  | <span data-ttu-id="225bf-108">Dateiname</span><span class="sxs-lookup"><span data-stu-id="225bf-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="225bf-109">ER-Formatkonfiguration</span><span class="sxs-lookup"><span data-stu-id="225bf-109">ER format configuration</span></span>                | [<span data-ttu-id="225bf-110">Format zum Importieren des trans_JSON.xml der Kreditoren</span><span class="sxs-lookup"><span data-stu-id="225bf-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="225bf-111">Beispiel einer eingehenden Datei im .csv-Format</span><span class="sxs-lookup"><span data-stu-id="225bf-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="225bf-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="225bf-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="225bf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="225bf-113">Requirements</span></span>

<span data-ttu-id="225bf-114">Bevor Sie den ER Formatkonfiguration abschließen, um Daten aus einem externen JSON-Dateiaufgabenleitfaden zu importieren, muss die folgende Anforderungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="225bf-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="225bf-115">Übergeordnete Elemente in der JSON-Datei können nur Objektelemente sein.</span><span class="sxs-lookup"><span data-stu-id="225bf-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="225bf-116">Geschachtelte Elemente für ein Objekt sollen Eigenschaftenelemente sein, damit eine gültige JSON-Struktur erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="225bf-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="225bf-117">JSON-Arrays können nur geschachtelte Elemente der Eigenschaftenelemente eines Objekts sein.</span><span class="sxs-lookup"><span data-stu-id="225bf-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="225bf-118">JSON-Arrays können nur JSON-Objekte enthalten.</span><span class="sxs-lookup"><span data-stu-id="225bf-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="225bf-119">Sie können keine direkte Zeichenfolge / numerische Werte und geschachtelte Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="225bf-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="225bf-120">Elemente in diesen Arrays werden in der Reihenfolge analysiert, in der sie im Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="225bf-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="225bf-121">Vielfältige Einstellungen in jedem JSON-Objekt werden berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="225bf-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="225bf-122">Darüber hinaus müssen Sie den Aufgabenleitfaden [ER erforderlichen Konfigurationen erstellen, um Daten aus einer externen Datei für elektronische Berichte zu importieren](tasks/er-required-configurations-import-data.md) abschließen, wenn Sie diesen nicht bereits abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="225bf-122">Additionally, you must complete the [ER Create required configurations to import data from an external file for electronic reporting](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="225bf-123">Laden Sie die folgende Datei herunter, um den Aufgabenleitfaden ausführen.</span><span class="sxs-lookup"><span data-stu-id="225bf-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="225bf-124">Titel</span><span class="sxs-lookup"><span data-stu-id="225bf-124">Title</span></span>                  | <span data-ttu-id="225bf-125">Dateiname</span><span class="sxs-lookup"><span data-stu-id="225bf-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="225bf-126">ER Modellkonfiguration</span><span class="sxs-lookup"><span data-stu-id="225bf-126">ER model configuration</span></span> | [<span data-ttu-id="225bf-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="225bf-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |