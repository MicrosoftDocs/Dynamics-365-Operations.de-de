---
title: Anlage erstellen
description: In diesem Thema wird erläutert, wie Sie auf der Seite Liste der Anlagen einen neuen Anlagendatensatz erstellen.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab330c604b2485687544a7d8b3eef3a652fa2069
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985136"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="1a0e1-103">Anlage erstellen</span><span class="sxs-lookup"><span data-stu-id="1a0e1-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a0e1-104">In diesem Thema wird erläutert, wie Sie auf der Seite Liste der **Anlagen** einen neuen Anlagedatensatz erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="1a0e1-105">Das System weist die Anlage-Nummer basierend auf der Nummernfolge zu, die der Anlagegruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="1a0e1-106">Wenn Sie die Anlagevorlage verwenden, um Vermögenswerte über das Microsoft Excel Add-In zu importieren oder wenn Sie einen anderen Importjob verwenden, erstellt das System automatisch Anlagenbestandsdatensätze und erhöht die Bestandsnummer.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="1a0e1-107">Führen Sie die folgenden Schritte aus, um einen Anlage-Datensatz manuell zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="1a0e1-108">Wechseln Sie zu **Navigationsbereich \> Module \> Anlagen \> Anlagen \> Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="1a0e1-109">Wählen Sie im **Aktivitätsbereich** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="1a0e1-110">Geben Sie im Feld **Anlagengruppe** einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="1a0e1-111">Das Feld **Nummer** wird als Standardwert angegeben, wenn Sie die Funktion **Anlagen automatisch nummerieren** in den **Anlagenparametern** und der **Anlagengruppe** aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="1a0e1-112">Anderenfalls müssen Sie eine eindeutige Nummer zur Identifizierung der Anlage eingeben.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="1a0e1-113">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="1a0e1-114">Geben Sie die zusätzlichen Informationen ein, die Ihr Unternehmen für diese Anlage benötigt.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="1a0e1-115">Wählen Sie im **Aktivitätsbereich** **Bücher** aus.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="1a0e1-116">Geben Sie im Feld **Anschaffungsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="1a0e1-117">Geben Sie im Feld **Anschaffungspreis** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="1a0e1-118">Geben Sie die zusätzlichen Informationen ein, die Ihr Unternehmen für diese Buchung benötigt.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="1a0e1-119">Geben Sie die zusätzlichen Informationen ein, die Ihr Unternehmen für verbleibenden Bücher benötigt.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="1a0e1-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-120">Close the page.</span></span>

<span data-ttu-id="1a0e1-121">Sie können Anlagen auch mithilfe des Excel-Add-Ins oder durch Ausführen eines Importauftrags aus dem Arbeitsbereich **Datenmanagement** importieren.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="1a0e1-122">Geben Sie vor dem Ausführen des Imports die Werte für die erforderlichen Felder in die Vorlage ein.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="1a0e1-123">Wenn Sie die Anlagennummer nicht in der Vorlage des Excel-Add-Ins oder in der Datenverwaltung definiert haben, erstellt das System für jede importierte Anlage eine Anlagennummer und erhöht automatisch die Nummernfolge für jede Anlage.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="1a0e1-124">Wenn Sie jedoch Anlagens importieren und Anlagen-Nummern in der Vorlage definieren, erhöht das System **nicht** automatisch die Nummernfolge.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="1a0e1-125">In diesem Fall muss ein Administrator möglicherweise die Nummernfolge manuell aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="1a0e1-126">Wenn Sie die Anlagenummer in der Vorlage des Excel-Add-Ins definiert haben, verwendet das System die definierte Anlagenummer und erhöht die Nummernfolge.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="1a0e1-127">Nach Buchung der Abschreibung werden die **Inbetriebnahme** und **Abschreibungslaufdatum**-Felder auf der **Buch** Seite gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="1a0e1-128">Außerdem werden beide Felder von der Datenentität nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="1a0e1-129">Der Anlagebestand wird nicht gelöscht, wenn Transaktionen in das zugehörige Buch gebucht wurden oder wenn die neu erstellte Anlage in einer Erfassungszeile erfasst, aber nicht gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="1a0e1-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 
