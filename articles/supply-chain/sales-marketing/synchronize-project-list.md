---
title: Projektliste von Supply Chain Management zu Field Service synchronisieren
description: Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3d17b226cabd0668bcdb52e9a7fdfc5973fe49b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243056"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="27882-103">Projektliste von Supply Chain Management zu Field Service synchronisieren</span><span class="sxs-lookup"><span data-stu-id="27882-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27882-104">Dieses Thema beschreibt die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um die Projekte aus Dynamics 365 Supply Chain Management mit Dynamics 365 Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="27882-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="27882-105">[![Synchronisierung von Geschäftsprozessen zwischen Supply Chain Management und Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="27882-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="27882-106">Vorlagen und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="27882-106">Templates and tasks</span></span>
<span data-ttu-id="27882-107">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekte von Supply Chain Management auf Field Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="27882-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="27882-108">**Vorlagen in der Datenintegration**</span><span class="sxs-lookup"><span data-stu-id="27882-108">**Template in Data integration**</span></span>
- <span data-ttu-id="27882-109">Projekte (Supply Chain Management zu Field Service)</span><span class="sxs-lookup"><span data-stu-id="27882-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="27882-110">**Aufgaben im Datenintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="27882-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="27882-111">Projekte</span><span class="sxs-lookup"><span data-stu-id="27882-111">Projects</span></span>

<span data-ttu-id="27882-112">Die folgende Synchronisierung ist erforderlich, bevor die Synchronisierung von  Projektlisten erfolgen kann:</span><span class="sxs-lookup"><span data-stu-id="27882-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="27882-113">Konten (Sales zu Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="27882-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="27882-114">Entitätssatz</span><span class="sxs-lookup"><span data-stu-id="27882-114">Entity set</span></span>
| <span data-ttu-id="27882-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="27882-115">Field Service</span></span>           | <span data-ttu-id="27882-116">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="27882-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="27882-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="27882-117">msdynce_externalprojects</span></span> | <span data-ttu-id="27882-118">Projekte</span><span class="sxs-lookup"><span data-stu-id="27882-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="27882-119">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="27882-119">Entity flow</span></span>
<span data-ttu-id="27882-120">Projekte werden in Supply Chain Management erstellt.</span><span class="sxs-lookup"><span data-stu-id="27882-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="27882-121">Projekte mit **Projekttyp** **Zeit und -material** und **Projektphase** **Prozess** synchronisiert mit **Externer Projekt** Entität in Field Service, einschließlich Projektnummeren-, Projektnamen-, und Projektphasen und Debitorenkontoinformationen.</span><span class="sxs-lookup"><span data-stu-id="27882-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="27882-122">Die Liste **Externes Projekt** wird verwendet, um Field Service Arbeitsaufträge mit Supply Chain Management-Projekten zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="27882-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="27882-123">Field Service CRM-Lösung</span><span class="sxs-lookup"><span data-stu-id="27882-123">Field Service CRM solution</span></span>
<span data-ttu-id="27882-124">Die Entität **Externes Projekt** ruft alle Projekte aus Supply Chain Management ab.</span><span class="sxs-lookup"><span data-stu-id="27882-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="27882-125">Das Feld **Externes Projekt** ist der **Arbeitsauftragsentität** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="27882-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="27882-126">Dieses Feld ist ein Suchfeld. Durch das Markieren des Arbeitsauftrags mit einem Projekt wird der Auftrag dem Projekt in Supply Chain Management verbunden.</span><span class="sxs-lookup"><span data-stu-id="27882-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="27882-127">Wenn der **Systemstatus** von **Offen auf In Verarbeitung (690.970.000)** auf einen höheren Status ändert, wird das Feld **Externe Projekttypen** gesperrt und Sie können den Wert nicht hinzufügen, entfernen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="27882-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="27882-128">Voraussetzungen und Zuordnungseinrichtung</span><span class="sxs-lookup"><span data-stu-id="27882-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="27882-129">Lieferkettenverwaltung</span><span class="sxs-lookup"><span data-stu-id="27882-129">Supply Chain Management</span></span>
<span data-ttu-id="27882-130">Änderungsnachverfolgung für Datentitätprojekte nachverfolgen</span><span class="sxs-lookup"><span data-stu-id="27882-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="27882-131">Vorlagenzuordnung in Datenintegration</span><span class="sxs-lookup"><span data-stu-id="27882-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="27882-132">Projekte (Supply Chain Management zu Field Service): Projekt</span><span class="sxs-lookup"><span data-stu-id="27882-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="27882-133">[![Vorlagenzuordnung in Datenintegration](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="27882-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]