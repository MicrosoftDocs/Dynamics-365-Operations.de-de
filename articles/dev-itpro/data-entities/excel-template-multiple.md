---
title: Importieren von Daten aus Excel-Datenentitätsvorlagen, die mehrere Arbeitsblätter haben
description: In diesem Thema wird beschrieben, wie Daten mithilfe der Excel-Datenentitätsvorlagen in Microsoft Dynamics 365 for Finance and Operations importiert werden.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "351262"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="b7baa-103">Importieren von Daten aus Excel-Datenentitätsvorlagen, die mehrere Arbeitsblätter haben</span><span class="sxs-lookup"><span data-stu-id="b7baa-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7baa-104">Die Datenverwaltung in Microsoft Dynamics 365 for Finance and Operations unterstützt Microsoft Excel-basierte Vorlagen für Datenentitäten.</span><span class="sxs-lookup"><span data-stu-id="b7baa-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="b7baa-105">Diese Vorlagen können eines oder mehrere Arbeitsblätter enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7baa-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="b7baa-106">Vorlagen mit mehreren Arbeitsblättern werden häufig verwendet, wenn es von Vorteil ist, Daten in einer einzigen Datei zu verwalten und diese in mehrere Datenentitäten zu importieren.</span><span class="sxs-lookup"><span data-stu-id="b7baa-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="b7baa-107">Ein Beispiel wären Standorte und Lagerorte.</span><span class="sxs-lookup"><span data-stu-id="b7baa-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="b7baa-108">Einmaliges Hochladen einer Datei und deren Zuweisung zu allen Entitäten</span><span class="sxs-lookup"><span data-stu-id="b7baa-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="b7baa-109">Nehmen wir als Beispiel eine Excel-Datei mit Arbeitsblättern, die **Standorte** und **Lagerorte** heißen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="b7baa-110">Um das Datenimportprojekt einzurichten, würden Sie die erste Datenentität hinzufügen, nämlich **Standorte**. Dann würden Sie die Datei hochladen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="b7baa-111">Sie können dann **Standorte** als das Arbeitsblatt auswählen, das für diese Entität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7baa-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="b7baa-112">Wenn Sie die zweite Entität **Lagerorte** hinzufügen, ohne das Formular **Datei hinzufügen** zu verlassen, können Sie mithilfe der Arbeitsblattsuche das Arbeitsblatt **Lagerorte** auswählen, ohne die Datei erneut hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="b7baa-113">Der einzige Grund, eine neue Datei hochzuladen, wäre gegeben, wenn die Daten zu **Lagerorte** sich in einer anderen Datei befänden.</span><span class="sxs-lookup"><span data-stu-id="b7baa-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Mehrere Arbeitsblätter](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="b7baa-115">Zuordnung von Arbeitsblatt zu Entität korrigieren</span><span class="sxs-lookup"><span data-stu-id="b7baa-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="b7baa-116">Die Zuordnung des Arbeitsblatts zu einer Datenentität im Importeinzelvorgang kann vom Raster aus korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7baa-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="b7baa-117">Die Spalte **Arbeitsblatt** im Raster zeigt die Arbeitsblätter der Datei an, die zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7baa-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="b7baa-118">Sie können ein anderes Arbeitsblatt über das Dropdownmenü auswählen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="b7baa-119">Wenn das ausgewählte Arbeitsblatt bereits einer Entität im Datenprojekt zugeordnet ist, fordert das System Sie dazu auf, die Änderung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="b7baa-120">Es wird empfohlen, alle Zuordnungen im Raster zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b7baa-120">We recommend that you fix all mappings in the grid.</span></span>

![Arbeitsblattzuordnung aktualisieren](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="b7baa-122">Einer neuen Datei erneut zuordnen</span><span class="sxs-lookup"><span data-stu-id="b7baa-122">Re-map to a new file</span></span>

<span data-ttu-id="b7baa-123">In Fällen, in denen eine neue Version derselben Datei oder eine völlig neue Datei für vorhandene Entitäten in einem Datenprojekt hochgeladen werden müssen, müssen Sie die Benutzeroberfläche für **Datei hinzufügen** verwenden, und die Entitäten erneut hinzufügen, so als ob Sie zum ersten Mal hinzugefügt würden.</span><span class="sxs-lookup"><span data-stu-id="b7baa-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="b7baa-124">Das System bestätigt, dass Sie die vorhandenen Entitäten im Datenprojekt überschreiben möchten, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="b7baa-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="b7baa-125">Entitäten, die nicht erneut hinzugefügt werden (oder überschrieben werden), werden weiterhin die vorherigen Zuordnungen aus der vorherigen Datei aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="b7baa-126">Eine Datei mithilfe von „Projekt ausführen” hochladen</span><span class="sxs-lookup"><span data-stu-id="b7baa-126">Upload a file using Run project</span></span>

<span data-ttu-id="b7baa-127">Sie können eine Excel-Datei hochladen, während Sie die Option **Projekt ausführen** verwenden, um ein Importprojekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b7baa-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="b7baa-128">Sie müssen darauf achten, dass Sie nur Dateien hochladen, die dieselben Arbeitsblätter wie die vorhandenen Zuordnungen zu den Datenentitäten im Datenprojekt haben.</span><span class="sxs-lookup"><span data-stu-id="b7baa-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="b7baa-129">Wenn ein Arbeitsblatt in der neu hochgeladenen Datei nicht gefunden wird, zeigt das System eine Fehlermeldung an und der Importvorgang wird beendet.</span><span class="sxs-lookup"><span data-stu-id="b7baa-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="b7baa-130">Wenn die Zuordnung zum Arbeitsblatt für eine Entität geändert werden muss, dann müssen die Zuordnungen im Datenprojekt zuerst vom Datenprojekt selbst aus aktualisiert werden, bevor die Datei in der Benutzeroberfläche **Projekt ausführen** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7baa-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>
