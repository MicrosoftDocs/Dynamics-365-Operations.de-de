---
title: Erweiterte Bankabstimmung MT940 Import – Zusammengesetzter Datenentitäts-Upgrade
description: Eine Sequenznummer muss der Bankauszugs-Importentität hinzugefügt werden, um das Format MT940 zu unterstützen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554850"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="16740-103">Erweiterte Bankabstimmung MT940 Import – Zusammengesetzter Datenentitäts-Upgrade</span><span class="sxs-lookup"><span data-stu-id="16740-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16740-104">Eine Sequenznummer muss der Bankauszugs-Importentität hinzugefügt werden, um das Format MT940 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="16740-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="16740-105">Gehen Sie folgendermaßen vor, um die Bankauszugs-Importentität hinzuzufügen, um das Format MT940 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="16740-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="16740-106">Kompilieren und synchronisieren Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16740-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="16740-107">Zusammengesetzte Entität\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="16740-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="16740-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="16740-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="16740-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="16740-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="16740-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="16740-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="16740-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="16740-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="16740-112">Tables\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="16740-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="16740-113">Datenverwaltung\\Datenprojekte.</span><span class="sxs-lookup"><span data-stu-id="16740-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="16740-114">Laden Sie MT940-Importprojekt(e)</span><span class="sxs-lookup"><span data-stu-id="16740-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="16740-115">Ändern Sie XSLT.</span><span class="sxs-lookup"><span data-stu-id="16740-115">Change XSLT.</span></span>
            -   <span data-ttu-id="16740-116">Klicken Sie auf **Zuordnung anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="16740-116">Click **View map**.</span></span>
            -   <span data-ttu-id="16740-117">Klicken Sie auf **Zuordnung anzeigen** auf dem Bankauszugsdokument.</span><span class="sxs-lookup"><span data-stu-id="16740-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="16740-118">Klicken Sie auf **Umwandlungen**</span><span class="sxs-lookup"><span data-stu-id="16740-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="16740-119">Löschen Sie die Datei „BankReconiliation-to-Composite.xslt”.</span><span class="sxs-lookup"><span data-stu-id="16740-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="16740-120">Fügen Sie die neue Version von „BankReconiliation-to-Composite.xsl” hinzu.</span><span class="sxs-lookup"><span data-stu-id="16740-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="16740-121">Machen Sie die **Sequenznummer** im Layout **Quelldaten** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16740-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="16740-122">Quelldatenformat = XML-Element.</span><span class="sxs-lookup"><span data-stu-id="16740-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="16740-123">Entitätsname = Bankauszüge.</span><span class="sxs-lookup"><span data-stu-id="16740-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="16740-124">Laden Sie die Datendatei hoch = neue Version „SampleBankCompositeEntity.xml”.</span><span class="sxs-lookup"><span data-stu-id="16740-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="16740-125">Klicken Sie auf **Ja**, um die vorhandene Datei zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="16740-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="16740-126">Klicken Sie auf **Ja**, um eine neue Zuordnung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="16740-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="16740-127">Überprüfen Sie, ob S**equenceNumber** zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="16740-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="16740-128">Klicken Sie auf **Zuordnung anzeigen** auf der Auszugsentität.</span><span class="sxs-lookup"><span data-stu-id="16740-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="16740-129">Überprüfen Sie, dass **SequenceNumber** von der Quelle zum Bereitstellen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="16740-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="16740-130">Importieren Sie den neuen Auszug.</span><span class="sxs-lookup"><span data-stu-id="16740-130">Import the new statement.</span></span>




