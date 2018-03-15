---
title: Erstellen von Servicevereinbarungen
description: "In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: de-de
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="f05f3-103">Erstellen von Servicevereinbarungen</span><span class="sxs-lookup"><span data-stu-id="f05f3-103">Create service agreements</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f05f3-104">In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f05f3-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="f05f3-105">Erstellen eines Servicevertrags aus der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="f05f3-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="f05f3-106">Navigieren Sie zu **Serviceverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="f05f3-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="f05f3-107">Klicken Sie auf die Schaltfläche **Dienstleistungsvereinbarung** , um im Formularkopf eine neue Servicevertragsposition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f05f3-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="f05f3-108">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f05f3-108">Click **New**.</span></span> <span data-ttu-id="f05f3-109">Geben Sie eine Beschreibung ein, wählen Sie einen Verweis auf ein **Projekt-ID** im Feld  aus, und füllen Sie die restlichen Felder und Positionen für den Servicevertrag aus.</span><span class="sxs-lookup"><span data-stu-id="f05f3-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="f05f3-110">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f05f3-110">Click **Save**.</span></span>
4. <span data-ttu-id="f05f3-111">Klicken Sie auf die Registerkarte ,**Beziehung** und wählen Sie Erstellen von **Serviceobjektbeziehungen** oder **Serviceaufgabenbeziehungen** für den Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="f05f3-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="f05f3-112">Die Serviceobjekte und -aufgaben, für die eine Beziehung erstellt wurden, können den Positionen der Servicevereinbarung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f05f3-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="f05f3-113">Erstellen Sie Servicevereinbarungspositionen in der unteren Hälfte des Formulars , indem Sie Positionen aus einer Servicevorlage oder aus einer anderen Servicevereinbarung kopieren, oder erstellen Sie die Servicevereinbarungspositionen manuell.</span><span class="sxs-lookup"><span data-stu-id="f05f3-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="f05f3-114">Beim Kopieren von Positionen aus einer anderen Servicevereinbarung kann angegeben werden, ob auch die Serviceobjekt- und die Serviceaufgabenbeziehungen kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f05f3-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="f05f3-115">Werden diese Beziehungen kopiert, werden sie den für die Servicevereinbarung möglicherweise bereits vorhandenen Beziehungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f05f3-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="f05f3-116">Beim Kopieren von Servicevereinbarungspositionen aus einer Servicevorlage werden die Serviceobjekt- sowie die Serviceaufgabenbeziehungen automatisch entsprechend in die neuen Servicevereinbarungspositionen kopiert.</span><span class="sxs-lookup"><span data-stu-id="f05f3-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="f05f3-117">Manuelles Erstellen von Servicevertragspositionen</span><span class="sxs-lookup"><span data-stu-id="f05f3-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="f05f3-118">Fügen Sie im Formular **Servicevereinbarungen**eine Servicevertragsposition im Raster  hinzu.</span><span class="sxs-lookup"><span data-stu-id="f05f3-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="f05f3-119">Geben Sie die für die Servicevereinbarungsposition erforderlichen Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="f05f3-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="f05f3-120">Drücken Sie **STRG+S**, um die Position zu speichern, und schließen Sie anschließend das Formular.</span><span class="sxs-lookup"><span data-stu-id="f05f3-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="f05f3-121">Erstellen einer Servicevereinbarung mithilfe des Moduls "Projekt"</span><span class="sxs-lookup"><span data-stu-id="f05f3-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="f05f3-122">Auf **Projektverwaltung und -buchhaltung** klicken.</span><span class="sxs-lookup"><span data-stu-id="f05f3-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="f05f3-123">**Alle Projekte** anklicken.</span><span class="sxs-lookup"><span data-stu-id="f05f3-123">Click **All projects**.</span></span>
3. <span data-ttu-id="f05f3-124">Wählen Sie in der Liste ein Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="f05f3-124">Select the project from the list.</span></span>
4. <span data-ttu-id="f05f3-125">Klicken Sie im **Aktivitätsbereich** auf **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="f05f3-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="f05f3-126">In der Aktivitätsgruppe **Neu** klicken Sie **Dienst** und wählen Sie **Servicevertrag** aus.</span><span class="sxs-lookup"><span data-stu-id="f05f3-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="f05f3-127">Führen Sie die Schritte im Abschnitt **Erstellen eines Servicevertrags** aus der Serviceverwaltung" (siehe vorheriger Kommentar in diesem Thema) aus.</span><span class="sxs-lookup"><span data-stu-id="f05f3-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="f05f3-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f05f3-128">Related topics</span></span>

[<span data-ttu-id="f05f3-129">Servicevereinbarungen</span><span class="sxs-lookup"><span data-stu-id="f05f3-129">Service agreements</span></span>](service-agreements.md)



