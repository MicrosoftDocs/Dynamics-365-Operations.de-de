---
title: Generieren von Dokumenten, die Anwendungsdaten haben
description: 'Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 4: Ändern Sie das Format)".'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90c6ebc456d3e137e43022fad7d59ce3ca2cdcab
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544494"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="66ccd-103">Generieren von Dokumenten, die Anwendungsdaten haben</span><span class="sxs-lookup"><span data-stu-id="66ccd-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66ccd-104">Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 4: Ändern Sie das Format)".</span><span class="sxs-lookup"><span data-stu-id="66ccd-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="66ccd-105">Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="66ccd-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="66ccd-106">In diesem Verfahren führen Sie die ER-Formatkonfiguration aus, um die Intrastat-Berichts- und Aktualisierungsbewerbungsdaten für das Archivieren von Details des Generieren eines Berichts zu generieren.</span><span class="sxs-lookup"><span data-stu-id="66ccd-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="66ccd-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="66ccd-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="66ccd-108">Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="66ccd-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="66ccd-109">Bevor Sie beginnen, stellen Sie sicher, dass der Landkontext für das DEMF-Unternehmen BEL (Belgien) ist.</span><span class="sxs-lookup"><span data-stu-id="66ccd-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="66ccd-110">Außenhandelsparameter einrichten</span><span class="sxs-lookup"><span data-stu-id="66ccd-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="66ccd-111">Wechseln Sie zu "Steuer" > "Einstellungen" > "Außenhandel" > "Außenhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="66ccd-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="66ccd-112">Klicken Sie auf die Registerkarte "Nummernkreis".</span><span class="sxs-lookup"><span data-stu-id="66ccd-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="66ccd-113">Zum Archivieren der Details des Intrastat-Berichterstattungsprozess müssen wir Datensätze jedes Archivs, das wir erstellt haben identifizieren.</span><span class="sxs-lookup"><span data-stu-id="66ccd-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="66ccd-114">Ein spezieller Nummernkreis muss konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="66ccd-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="66ccd-115">Wählen Sie die Intrastat-Archiv "ID-" Referenz aus.</span><span class="sxs-lookup"><span data-stu-id="66ccd-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="66ccd-116">Geben Sie im Feld "Nummernkreiscode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="66ccd-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="66ccd-117">Geben Sie im Feld "Nummernsequenzcode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="66ccd-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="66ccd-118">ResolveChanges den Nummersequenzcode.</span><span class="sxs-lookup"><span data-stu-id="66ccd-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="66ccd-119">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="66ccd-119">Click Save.</span></span>
7. <span data-ttu-id="66ccd-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="66ccd-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="66ccd-121">Führen Sie geändertes ER-Format aus</span><span class="sxs-lookup"><span data-stu-id="66ccd-121">Run modified ER format</span></span>
1. <span data-ttu-id="66ccd-122">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="66ccd-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="66ccd-123">Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="66ccd-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="66ccd-124">Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Format)" aus.</span><span class="sxs-lookup"><span data-stu-id="66ccd-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="66ccd-125">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="66ccd-125">Click Run.</span></span>
5. <span data-ttu-id="66ccd-126">Geben Sie im Feld Tabelle den Typ intrastat2.xml ein.</span><span class="sxs-lookup"><span data-stu-id="66ccd-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="66ccd-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="66ccd-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="66ccd-128">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="66ccd-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="66ccd-129">Überprüfen Sie die Ergebnisse der ER-Formatausführung</span><span class="sxs-lookup"><span data-stu-id="66ccd-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="66ccd-130">Erstellte XML Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="66ccd-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="66ccd-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="66ccd-131">Close the page.</span></span>
2. <span data-ttu-id="66ccd-132">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="66ccd-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="66ccd-133">Öffnen Sie dieses Formular, das die Intrastat-Buchungen enthält, die im generierten elektronischen Dokument enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="66ccd-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="66ccd-134">Intrastat-Archivkennung anklicken.</span><span class="sxs-lookup"><span data-stu-id="66ccd-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="66ccd-135">Da das ausgeführte ER-Format nur Einstellungen für Anwendungsdatenenaktualisierungen enthält, wurden die Details des abgeschlossenen Intrastat-Bericht archiviert.</span><span class="sxs-lookup"><span data-stu-id="66ccd-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="66ccd-136">In diesem Formular können Sie den Headerdatensatz des erstellten Dokumentarchivs finden.</span><span class="sxs-lookup"><span data-stu-id="66ccd-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="66ccd-137">Klicken Sie auf Details.</span><span class="sxs-lookup"><span data-stu-id="66ccd-137">Click Details.</span></span>
    * <span data-ttu-id="66ccd-138">In diesem Formular können Sie die Details für das erstellte Dokumentarchiv finden.</span><span class="sxs-lookup"><span data-stu-id="66ccd-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="66ccd-139">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="66ccd-139">Close the page.</span></span>
6. <span data-ttu-id="66ccd-140">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="66ccd-140">Close the page.</span></span>
7. <span data-ttu-id="66ccd-141">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="66ccd-141">Close the page.</span></span>

