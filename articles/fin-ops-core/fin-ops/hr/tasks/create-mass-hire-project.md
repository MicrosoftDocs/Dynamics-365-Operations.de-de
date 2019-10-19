---
title: Erstellen eines Masseneinstellungsprojekts
description: Diese Prozedur führt Sie durch den Prozess der Einrichtung eines Masseneinstellungsprojekts.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea0f4638a968d2aecf4e3bb27acbd19e6455a8b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190625"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="ee832-103">Erstellen eines Masseneinstellungsprojekts</span><span class="sxs-lookup"><span data-stu-id="ee832-103">Create a mass hire project</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee832-104">Diese Prozedur führt Sie durch den Prozess der Einrichtung eines Masseneinstellungsprojekts.</span><span class="sxs-lookup"><span data-stu-id="ee832-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="ee832-105">Ein Personalbeschaffungsmitarbeiter kann Masseneinstellungsprojekte verwenden, um auf einfache Weise mehrere Positionen zu erstellen und mehrere Arbeitskräfte in diesen Positionen einzustellen.</span><span class="sxs-lookup"><span data-stu-id="ee832-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="ee832-106">Um diese Prozedur zu starten, gehen Sie zu "Personalverwaltung" > "Personalbeschaffung" > "Masseneinstellungsprojekte".</span><span class="sxs-lookup"><span data-stu-id="ee832-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="ee832-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="ee832-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ee832-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ee832-108">Click New.</span></span>
2. <span data-ttu-id="ee832-109">Geben Sie im Feld "Masseneinstellungsprojekt" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ee832-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="ee832-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ee832-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="ee832-111">Geben Sie im Feld "Projektstart"ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ee832-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="ee832-112">Geben Sie im Feld "Projektende"ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="ee832-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="ee832-113">Klicken Sie auf "Projekt öffnen".</span><span class="sxs-lookup"><span data-stu-id="ee832-113">Click Open project.</span></span>
7. <span data-ttu-id="ee832-114">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="ee832-114">Click Yes.</span></span>
8. <span data-ttu-id="ee832-115">Klicken Sie auf "Positionen erstellen".</span><span class="sxs-lookup"><span data-stu-id="ee832-115">Click Create positions.</span></span>
9. <span data-ttu-id="ee832-116">Geben Sie im Feld "Menge" die Anzahl der zu erstellenden Positionen ein.</span><span class="sxs-lookup"><span data-stu-id="ee832-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="ee832-117">Das Startdatum wird zum Einstellungsdatum für die neuen Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="ee832-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="ee832-118">Das Enddatum wird zum Kündigungsdatum für die neuen Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="ee832-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="ee832-119">Geben Sie an, ob die neuen Arbeitskräfte Mitarbeiter oder Auftragnehmer sind.</span><span class="sxs-lookup"><span data-stu-id="ee832-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="ee832-120">Klicken Sie im Feld "Einzelvorgang auf die Dropdownschaltfläche, um den Einzelvorgang auszuwählen, für den die Positionen erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ee832-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="ee832-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="ee832-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ee832-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="ee832-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ee832-123">Der standardmäßige Wert für Vollzeitmitarbeiter stammt aus dem ausgewählten Einzelvorgang.</span><span class="sxs-lookup"><span data-stu-id="ee832-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="ee832-124">Diesen Wert können Sie bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="ee832-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="ee832-125">Wählen Sie optional die Abteilung für die neuen Positionen aus.</span><span class="sxs-lookup"><span data-stu-id="ee832-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="ee832-126">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="ee832-126">Click OK.</span></span>

