---
title: Projektliste von Finance and Operations mit Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525876"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="76643-103">Projektliste von Finance and Operations mit Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="76643-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="76643-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Microsoft Dynamics 365 for Finance and Operations mit Microsoft Dynamics 365 for Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="76643-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="76643-105">[![Synchronisierung von Geschäftsprozessen zwischen Finance and Operations und Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="76643-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="76643-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="76643-106">Templates and tasks</span></span>
<span data-ttu-id="76643-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Synchronisation von Projekten von Microsoft Dynamics 365 for Finance and Operations nach Microsoft Dynamics 365 for Field Service durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="76643-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="76643-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="76643-108">**Template in Data integration**</span></span>
- <span data-ttu-id="76643-109">Projects (Finance and Operations zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="76643-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="76643-110">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="76643-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="76643-111">Projekte</span><span class="sxs-lookup"><span data-stu-id="76643-111">Projects</span></span>

<span data-ttu-id="76643-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Projektlisten erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="76643-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="76643-113">Konten (Sales nach Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="76643-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="76643-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="76643-114">Entity set</span></span>
| <span data-ttu-id="76643-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="76643-115">Field Service</span></span>           | <span data-ttu-id="76643-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="76643-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="76643-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="76643-117">msdynce_externalprojects</span></span> | <span data-ttu-id="76643-118">Projekte</span><span class="sxs-lookup"><span data-stu-id="76643-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="76643-119">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="76643-119">Entity flow</span></span>
<span data-ttu-id="76643-120">Projekte werden in Finance and Operations erstellt.</span><span class="sxs-lookup"><span data-stu-id="76643-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="76643-121">Projekte mit **Projekttyp** **Zeit und -material** und **Projektphase** **Prozess** synchronisiert mit **Externer Projekt** Entität in Field Service, einschließlich Projektnummeren-, Projektnamen-, und Projektphasen und Debitorenkontoinformationen.</span><span class="sxs-lookup"><span data-stu-id="76643-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="76643-122">Die Liste **Externes Projekt** wird verwendet, um Field Service Arbeitsaufträge mit Finance and Operations Projekte zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="76643-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="76643-123">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="76643-123">Field Service CRM solution</span></span>
<span data-ttu-id="76643-124">Die Entität ruft **Externes Projekt** alle Projekte von der erhaltenen Finanzierung und Arbeitsgängen ab.</span><span class="sxs-lookup"><span data-stu-id="76643-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="76643-125">Das Feld **Externes Projekt** ist der **Arbeitsauftragsentität** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="76643-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="76643-126">Dieses Feld ist ein Suchfeld. Durch das Markieren des Arbeitsauftrags mit einem Projekt wird der Auftrag dem Projekt in Finance and Operations verbunden.</span><span class="sxs-lookup"><span data-stu-id="76643-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="76643-127">Wenn der **Systemstatus** von **Offen auf In Verarbeitung (690.970.000)** auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="76643-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="76643-128">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="76643-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="76643-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="76643-129">Finance and Operations</span></span>
<span data-ttu-id="76643-130">Änderungsnachverfolgung für Datentitätprojekte nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="76643-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="76643-131">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="76643-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="76643-132">Projects (Finance and Operations zu Field Service): Projects</span><span class="sxs-lookup"><span data-stu-id="76643-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="76643-133">[![Vorlagenzuordnung in Datenintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="76643-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
