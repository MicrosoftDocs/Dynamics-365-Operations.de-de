---
title: 'ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 1: Format erstellen)'
description: In diesem Thema wird beschrieben, wie Sie ein elektronisches Berichtsformat für das Zählen und Summieren basierend auf Daten der bereits generierten Textausgabe konfigurieren. (Teil 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749044"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="97784-104">ER – Konfigurieren des Formats für Inventuren und Summierungen (Teil 1: Format erstellen)</span><span class="sxs-lookup"><span data-stu-id="97784-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97784-105">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="97784-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="97784-106">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="97784-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="97784-107">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="97784-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="97784-108">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="97784-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="97784-109">Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="97784-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="97784-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="97784-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="97784-111">Überprüfen Sie, ob „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="97784-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="97784-112">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="97784-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="97784-113">Wählen Sie den „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="97784-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="97784-114">Anbieter.</span><span class="sxs-lookup"><span data-stu-id="97784-114">provider.</span></span>
3. <span data-ttu-id="97784-115">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="97784-115">Click Repositories.</span></span>
    * <span data-ttu-id="97784-116">Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.</span><span class="sxs-lookup"><span data-stu-id="97784-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="97784-117">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="97784-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="97784-118">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="97784-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="97784-119">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="97784-119">Click Create repository.</span></span>
7. <span data-ttu-id="97784-120">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="97784-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="97784-121">Intrastat-Konfigurationen von Microsoft erhalten</span><span class="sxs-lookup"><span data-stu-id="97784-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="97784-122">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="97784-122">Click Open.</span></span>
2. <span data-ttu-id="97784-123">Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="97784-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="97784-124">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="97784-124">Click Import.</span></span>
    * <span data-ttu-id="97784-125">Klicken Sie auf "Importieren" für Version 1.1 der ausgewählten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="97784-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="97784-126">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="97784-126">Click Yes.</span></span>
5. <span data-ttu-id="97784-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="97784-127">Close the page.</span></span>
6. <span data-ttu-id="97784-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="97784-128">Close the page.</span></span>
7. <span data-ttu-id="97784-129">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="97784-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="97784-130">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="97784-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="97784-131">Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="97784-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]