---
title: Konfigurationen entwerfen, um Dokumente zu generieren, die Anwendungsdaten haben
description: Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 1 - Importkonfigurationen).
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
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544517"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="67bb4-103">Konfigurationen entwerfen, um Dokumente zu generieren, die Anwendungsdaten haben</span><span class="sxs-lookup"><span data-stu-id="67bb4-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67bb4-104">Um die Schritte in dieser Prozedur auszuführen, müssen Sie zuerst das Verfahren abschließen, "ER generiert Dokumente mit Anwendungsdatenenaktualisierung (Teil 1: Importkonfigurationen).</span><span class="sxs-lookup"><span data-stu-id="67bb4-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="67bb4-105">Die Schritte in dieser Prozedur erläutern, wie elektronische Berichtskonfigurationen (ER) erstellt werden, um elektronische Dokumente zu generieren.</span><span class="sxs-lookup"><span data-stu-id="67bb4-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="67bb4-106">In diesem Beispiel erstellen Sie die erforderlichen ER-Konfigurationen für das Beispielunternehmen Litware, Inc., um elektronische Dokumentd zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="67bb4-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="67bb4-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="67bb4-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="67bb4-108">Die Schritte können abgeschlossen werden, indem Sie den DEMF-Datensatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="67bb4-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="67bb4-109">Bevor Sie beginnen, ändern Sie den Landkontext für das DEMF-Unternehmen DEU (Deutschland) zu BEL (Belgien).</span><span class="sxs-lookup"><span data-stu-id="67bb4-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="67bb4-110">Klicken Sie auf Organisationsverwaltung >Organisation >Juristische Personen, um den Ländercode in der primären Adresse der juristischen Person DEMF zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="67bb4-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="67bb4-111">Starten Sie Ihre Anwendung neu.</span><span class="sxs-lookup"><span data-stu-id="67bb4-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="67bb4-112">Führen Sie das importierte ER-Format aus</span><span class="sxs-lookup"><span data-stu-id="67bb4-112">Run imported ER format</span></span>
1. <span data-ttu-id="67bb4-113">Wechseln Sie zu Organisationsverwaltung > Elektronische Berichterstellung > Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="67bb4-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="67bb4-114">Erweitern Sie 'Intrastatmodell' (Modell) in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="67bb4-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="67bb4-115">Wählen Sie in der Strukturdarstellung "Intrastat(Modell)\Intrastat (Format)" aus.</span><span class="sxs-lookup"><span data-stu-id="67bb4-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="67bb4-116">Klicken Sie auf "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="67bb4-116">Click Run.</span></span>
    * <span data-ttu-id="67bb4-117">Führt die Entwurfsversion der ER-Formatkonfiguration aus, um den Intrastat-Bericht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="67bb4-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="67bb4-118">Geben Sie im Feld Tabelle den Typ Intrastat.xml ein.</span><span class="sxs-lookup"><span data-stu-id="67bb4-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="67bb4-119">Namen der Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="67bb4-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="67bb4-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="67bb4-120">Click OK.</span></span>
    * <span data-ttu-id="67bb4-121">Erstellte XML Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="67bb4-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="67bb4-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="67bb4-122">Close the page.</span></span>
8. <span data-ttu-id="67bb4-123">Wechseln Sie zu "Steuer" > "Meldungen" > "Außenhandel" > "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="67bb4-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="67bb4-124">Öffnen Sie dieses Formular, das die Intrastat-Buchungen enthält, die im generierten elektronischen Dokument enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="67bb4-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="67bb4-125">Intrastat-Archivkennung anklicken.</span><span class="sxs-lookup"><span data-stu-id="67bb4-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="67bb4-126">Da das ausgeführte ER-Format nur Einstellungen für Anwendungsdatenenaktualisierungen enthält, wurden die Details des abgeschlossenen Intrastat-Bericht archiviert.</span><span class="sxs-lookup"><span data-stu-id="67bb4-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="67bb4-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="67bb4-127">Close the page.</span></span>
11. <span data-ttu-id="67bb4-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="67bb4-128">Close the page.</span></span>

