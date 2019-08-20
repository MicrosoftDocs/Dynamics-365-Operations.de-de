---
title: Unternehmensübergreifende Finanzdatenfreigabe konfigurieren
description: Diese Prozedur zeigt Ihnen, wie Sie konfigurieren, aktivieren, überprüfen und Konflikte auflösen, wenn Sie Daten zwischen Unternehmen gemeinsam nutzen.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 049ffeee7db95cc2e5a31526d5d99026303456be
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848254"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="602ac-103">Unternehmensübergreifende Finanzdatenfreigabe konfigurieren</span><span class="sxs-lookup"><span data-stu-id="602ac-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="602ac-104">Diese Prozedur zeigt Ihnen, wie Sie konfigurieren, aktivieren, überprüfen und Konflikte auflösen, wenn Sie Daten zwischen Unternehmen gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="602ac-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="602ac-105">Dabei wird das USMF-Unternehmen und die Finanzdatenfreigabe-Vorlage verwendet.</span><span class="sxs-lookup"><span data-stu-id="602ac-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="602ac-106">Dieser Aufgabenleitfaden erfordert eine Dynamics AX-Plattform 7.1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="602ac-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="602ac-107">Wechseln Sie zu Systemverwaltung > Arbeitsbereiche > Datenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="602ac-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="602ac-108">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="602ac-108">Click Import.</span></span>
3. <span data-ttu-id="602ac-109">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="602ac-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="602ac-110">Wählen Sie im Feld "Quelldatenformat" den Pakettyp aus.</span><span class="sxs-lookup"><span data-stu-id="602ac-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="602ac-111">Klicken Sie auf Hochladen.</span><span class="sxs-lookup"><span data-stu-id="602ac-111">Click Upload.</span></span> <span data-ttu-id="602ac-112">Navigieren Sie zum Speicherort der Finanzdatenfreigaben-Vorlagenpaketdatei und wählen Sie diese Datei aus.</span><span class="sxs-lookup"><span data-stu-id="602ac-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="602ac-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="602ac-113">Click Save.</span></span>
6. <span data-ttu-id="602ac-114">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="602ac-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="602ac-115">Wählen Sie die Datenfreigaberichtlinie aus, die soeben erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="602ac-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="602ac-116">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="602ac-116">Click Import.</span></span>
8. <span data-ttu-id="602ac-117">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="602ac-117">Click Close.</span></span>
9. <span data-ttu-id="602ac-118">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="602ac-118">Refresh the page.</span></span>
10. <span data-ttu-id="602ac-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="602ac-119">Close the page.</span></span>
11. <span data-ttu-id="602ac-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="602ac-120">Close the page.</span></span>
12. <span data-ttu-id="602ac-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="602ac-121">Close the page.</span></span>
13. <span data-ttu-id="602ac-122">Wechseln Sie zu "Systemverwaltung" > "Einstellungen" > "Unternehmensübergreifende Datenfreigabe konfigurieren".</span><span class="sxs-lookup"><span data-stu-id="602ac-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="602ac-123">Suchen Sie in der Liste die Option "Zahlungstage" und wählen Sie diese aus</span><span class="sxs-lookup"><span data-stu-id="602ac-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="602ac-124">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="602ac-124">Click Add.</span></span>
16. <span data-ttu-id="602ac-125">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="602ac-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="602ac-126">Geben Sie im Feld "Unternehmen" die Zeichenfolge "USSI" ein.</span><span class="sxs-lookup"><span data-stu-id="602ac-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="602ac-127">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="602ac-127">Click Add.</span></span>
19. <span data-ttu-id="602ac-128">Geben Sie im Feld "Unternehmen" die Zeichenfolge "USMF" ein.</span><span class="sxs-lookup"><span data-stu-id="602ac-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="602ac-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="602ac-129">Click Save.</span></span>
21. <span data-ttu-id="602ac-130">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="602ac-130">Click Enable.</span></span>
22. <span data-ttu-id="602ac-131">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="602ac-131">Click Yes.</span></span>
23. <span data-ttu-id="602ac-132">Klicken Sie auf "Freigabeprobleme suchen".</span><span class="sxs-lookup"><span data-stu-id="602ac-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="602ac-133">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="602ac-133">Click Yes.</span></span>
25. <span data-ttu-id="602ac-134">Klicken Sie auf "Feldwert aktualisieren".</span><span class="sxs-lookup"><span data-stu-id="602ac-134">Click Update field value.</span></span>
26. <span data-ttu-id="602ac-135">Klicken Sie auf "Wert von Unternehmen 1 verwenden".</span><span class="sxs-lookup"><span data-stu-id="602ac-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="602ac-136">Aktualisieren Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="602ac-136">Refresh the page.</span></span>
28. <span data-ttu-id="602ac-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="602ac-137">Close the page.</span></span>

