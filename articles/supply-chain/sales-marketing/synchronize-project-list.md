---
title: Projektliste von Finance and Operations mit Field Service synchronisieren
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: de-de
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="517b4-103">Projektliste von Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="517b4-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="517b4-104">Dieses Thema erläutert die Vorlagen und die zugrunde liegende Aufgabe, die verwendet wird, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="517b4-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="517b4-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="517b4-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="517b4-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="517b4-106">Templates and tasks</span></span>
<span data-ttu-id="517b4-107">Die folgende Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="517b4-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="517b4-108">**Name der Vorlage in der Datenintegration:**</span><span class="sxs-lookup"><span data-stu-id="517b4-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="517b4-109">Projekte (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="517b4-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="517b4-110">**Namen der Aufgaben im Datenintegrationsprojekt:**</span><span class="sxs-lookup"><span data-stu-id="517b4-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="517b4-111">Projekte</span><span class="sxs-lookup"><span data-stu-id="517b4-111">Projects</span></span>

<span data-ttu-id="517b4-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Projektlisten erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="517b4-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="517b4-113">Konten (Sales zu Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="517b4-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="517b4-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="517b4-114">Entity set</span></span>
<span data-ttu-id="517b4-115">Field Service  Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="517b4-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="517b4-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="517b4-116">Field Service</span></span>           | <span data-ttu-id="517b4-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="517b4-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="517b4-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="517b4-118">msdynce_externalprojects</span></span> | <span data-ttu-id="517b4-119">Projekte</span><span class="sxs-lookup"><span data-stu-id="517b4-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="517b4-120">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="517b4-120">Entity flow</span></span>
<span data-ttu-id="517b4-121">Projekte werden in Finance and Operations erstellt.</span><span class="sxs-lookup"><span data-stu-id="517b4-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="517b4-122">Projekte mit **Projekttyp** Zeit und -material und **Projektphase** Prozess synchronisiert mit **Externer Projekt** Entität in Field Service, einschließlich Projektnummeren-, Projektnamen-, und Projektphasen und Debitorenkontoinformationen.</span><span class="sxs-lookup"><span data-stu-id="517b4-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="517b4-123">Die Liste **Externes Projekt** wird verwendet, um Field Service Arbeitsaufträge mit Finance and Operations Projekte zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="517b4-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="517b4-124">Field Service CRM Lösund The External Project ist eine neue Entität, die alle Projekte aus Operations abruft.</span><span class="sxs-lookup"><span data-stu-id="517b4-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="517b4-125">Das Feld Externes Projekt ist der Arbeitsauftragsentität hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="517b4-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="517b4-126">Dieses Feld ist ein Suchfeld und  verbindet den Arbeitsauftrag mit einem Projekt. Der Auftrag wird dann mit dem Projekt in Operations verbunden.</span><span class="sxs-lookup"><span data-stu-id="517b4-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="517b4-127">Wenn der Systemstatus von Offen auf In Verarbeitung (690.970.000) auf einen höheren Status das Feld für externe Projekttypen wird gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="517b4-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="517b4-128">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="517b4-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="517b4-129">In Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="517b4-129">In Finance and Operations</span></span>
<span data-ttu-id="517b4-130">Änderungsnachverfolgung für Datentitätprojekte nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="517b4-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="517b4-131">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="517b4-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="517b4-132">Projekte (Finance and Operations zu Field Service): Projekte</span><span class="sxs-lookup"><span data-stu-id="517b4-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="517b4-133">[![Vorlagenzuordnung in Datenintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="517b4-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

