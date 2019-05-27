---
title: Erstellen Sie eine Organisationshierarchie
description: Verwenden Sie die folgende Prozedur, um eine Organisationshierarchie zu erstellen.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 203a586b06a13a7c67f246384152d17627e22041
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545544"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="59b0a-103">Erstellen Sie eine Organisationshierarchie</span><span class="sxs-lookup"><span data-stu-id="59b0a-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59b0a-104">Verwenden Sie die folgende Prozedur, um eine Organisationshierarchie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="59b0a-105">Organisationshierarchien können verwendet werden, um unterschiedliche Perspektiven des Unternehmens anzuzeigen und entsprechende Berichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="59b0a-106">So können Sie z. B. eine Hierarchie für Steuererklärungen sowie für rechtlich relevante oder für gesetzlich vorgeschriebene Berichte einrichten.</span><span class="sxs-lookup"><span data-stu-id="59b0a-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="59b0a-107">Anschließend können Sie eine weitere Hierarchie einrichten, um anhand von Finanzdaten Berichte zu erstellen, die zwar gesetzlich nicht erforderlich sind, aber zur internen Berichterstattung dienen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="59b0a-108">Bevor Sie eine Organisationshierarchie erstellen, müssen Sie Organisationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="59b0a-109">Weitere Informationen finden Sie unter den Aufgaben "Eine juristische Person erstellen" oder "Eine Organisationseinheit erstellen".</span><span class="sxs-lookup"><span data-stu-id="59b0a-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="59b0a-110">Sie können auch Abteilungen und Teams erstellen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="59b0a-111">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="59b0a-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="59b0a-112">Hierarchie erstellen</span><span class="sxs-lookup"><span data-stu-id="59b0a-112">Create a hierarchy</span></span>
1. <span data-ttu-id="59b0a-113">Wechseln Sie zu "Organisationsverwaltung" > "Organisationen" > "Organisationshierarchien".</span><span class="sxs-lookup"><span data-stu-id="59b0a-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="59b0a-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="59b0a-114">Click New.</span></span>
3. <span data-ttu-id="59b0a-115">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="59b0a-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="59b0a-116">Klicken Sie auf "Zweck zuweisen".</span><span class="sxs-lookup"><span data-stu-id="59b0a-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="59b0a-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="59b0a-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="59b0a-118">Wählen Sie einen Zweck aus, der Ihrer Organisationshierarchie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="59b0a-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="59b0a-119">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-119">Click Add.</span></span>
7. <span data-ttu-id="59b0a-120">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="59b0a-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="59b0a-121">Suchen Sie die Hierarchie, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="59b0a-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="59b0a-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="59b0a-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="59b0a-123">Hinzufügen von Organisationen zur Hierarchie</span><span class="sxs-lookup"><span data-stu-id="59b0a-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="59b0a-124">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="59b0a-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="59b0a-125">Wählen Sie Ihre Hierarchie aus.</span><span class="sxs-lookup"><span data-stu-id="59b0a-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="59b0a-126">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="59b0a-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="59b0a-127">Fügen Sie Organisationen nach Bedarf hinzu.</span><span class="sxs-lookup"><span data-stu-id="59b0a-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="59b0a-128">Um eine Organisation hinzuzufügen, klicken Sie auf "Bearbeiten" und dann "Einfügen", um die Organisation hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="59b0a-129">Wenn Sie mit den Änderungen fertig sind, können Sie einen Entwurf speichern und/oder die Änderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="59b0a-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  

