---
title: Erstellen Sie eine Organisationshierarchie
description: Verwenden Sie die folgende Prozedur, um eine Organisationshierarchie zu erstellen.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48c8564694b22a5110341d853a79096fbe805c91
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916460"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="be2e5-103">Erstellen Sie eine Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="be2e5-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be2e5-104">Verwenden Sie die folgende Prozedur, um eine Organisationshierarchie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be2e5-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="be2e5-105">Organisationshierarchien können verwendet werden, um unterschiedliche Perspektiven des Unternehmens anzuzeigen und entsprechende Berichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="be2e5-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="be2e5-106">So können Sie z. B. eine Hierarchie für Steuererklärungen sowie für rechtlich relevante oder für gesetzlich vorgeschriebene Berichte einrichten.</span><span class="sxs-lookup"><span data-stu-id="be2e5-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="be2e5-107">Anschließend können Sie eine weitere Hierarchie einrichten, um anhand von Finanzdaten Berichte zu erstellen, die zwar gesetzlich nicht erforderlich sind, aber zur internen Berichterstattung dienen.</span><span class="sxs-lookup"><span data-stu-id="be2e5-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="be2e5-108">Bevor Sie eine Organisationshierarchie erstellen, müssen Sie Organisationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="be2e5-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="be2e5-109">Weitere Informationen finden Sie unter den Aufgaben "Eine juristische Person erstellen" oder "Eine Organisationseinheit erstellen".</span><span class="sxs-lookup"><span data-stu-id="be2e5-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="be2e5-110">Sie können auch Abteilungen und Teams erstellen.</span><span class="sxs-lookup"><span data-stu-id="be2e5-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="be2e5-111">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="be2e5-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="be2e5-112">Hierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="be2e5-112">Create a hierarchy</span></span>
1. <span data-ttu-id="be2e5-113">Wechseln Sie zu **Navigationsbereich > Module > Organisationsverwaltung > Organisationen > Organisationshierarchien**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="be2e5-114">Klicken Sie im **Aktivitätsbereich** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="be2e5-115">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="be2e5-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="be2e5-116">Klicken Sie im Abschnitt **Zweck** auf **Zweck zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="be2e5-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="be2e5-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="be2e5-118">Wählen Sie einen Zweck aus, der Ihrer Organisationshierarchie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="be2e5-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="be2e5-119">Klicken Sie im Abschnitt **Zugewiesene Hierarchien** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="be2e5-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="be2e5-120">In the list, mark the selected row.</span></span> <span data-ttu-id="be2e5-121">Suchen Sie die Hierarchie, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="be2e5-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="be2e5-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="be2e5-123">Hinzufügen von Organisationen zur Hierarchie</span><span class="sxs-lookup"><span data-stu-id="be2e5-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="be2e5-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="be2e5-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="be2e5-125">Wählen Sie Ihre Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="be2e5-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="be2e5-126">Klicken Sie im Abschnitt **Zugewiesene Hierarchien** auf **Hierarchie anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="be2e5-127">Fügen Sie Organisationen nach Bedarf hinzu.</span><span class="sxs-lookup"><span data-stu-id="be2e5-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="be2e5-128">Um eine Organisation hinzuzufügen, klicken Sie auf **Bearbeiten** und dann **Einfügen**, um die Organisation hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="be2e5-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="be2e5-129">Wenn Sie mit den Änderungen fertig sind, können Sie einen Entwurf **Speichern** und/oder die Änderungen **veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="be2e5-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

