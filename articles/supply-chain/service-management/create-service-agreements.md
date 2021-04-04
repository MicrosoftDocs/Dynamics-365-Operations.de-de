---
title: Erstellen von Servicevereinbarungen
description: In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f883d5b312c042a995e30998fc24da5b1c02f22a
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470856"
---
# <a name="create-service-agreements"></a><span data-ttu-id="bed02-103">Erstellen von Servicevereinbarungen</span><span class="sxs-lookup"><span data-stu-id="bed02-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bed02-104">In diesem Thema wird beschrieben, wie mithilfe der Funktionen in den Modulen Servicemanagement und Projektmanagement und Buchhaltung Serviceverträge erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bed02-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="bed02-105">Erstellen eines Servicevertrags aus der Serviceverwaltung</span><span class="sxs-lookup"><span data-stu-id="bed02-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="bed02-106">Navigieren Sie zu **Serviceverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="bed02-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="bed02-107">Wählen Sie **Servicevereinbarungen**, um eine neue Zeile für Servicevereinbarungen in der Kopfzeile der Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bed02-107">Select **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="bed02-108">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="bed02-108">Select **New**.</span></span> <span data-ttu-id="bed02-109">Geben Sie eine Beschreibung ein, wählen Sie einen Verweis auf ein **Projekt-ID** im Feld  aus, und füllen Sie die restlichen Felder und Positionen für den Servicevertrag aus.</span><span class="sxs-lookup"><span data-stu-id="bed02-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="bed02-110">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="bed02-110">Select **Save**.</span></span>
4. <span data-ttu-id="bed02-111">Klicken Sie auf die Registerkarte ,**Beziehung** und wählen Sie Erstellen von **Serviceobjektbeziehungen** oder **Serviceaufgabenbeziehungen** für den Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="bed02-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="bed02-112">Die Serviceobjekte und -aufgaben, für die eine Beziehung erstellt wurden, können den Positionen der Servicevereinbarung zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="bed02-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="bed02-113">Erstellen Sie Servicevereinbarungspositionen in der unteren Hälfte des Formulars , indem Sie Positionen aus einer Servicevorlage oder aus einer anderen Servicevereinbarung kopieren, oder erstellen Sie die Servicevereinbarungspositionen manuell.</span><span class="sxs-lookup"><span data-stu-id="bed02-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="bed02-114">Beim Kopieren von Positionen aus einer anderen Servicevereinbarung kann angegeben werden, ob auch die Serviceobjekt- und die Serviceaufgabenbeziehungen kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bed02-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="bed02-115">Werden diese Beziehungen kopiert, werden sie den für die Servicevereinbarung möglicherweise bereits vorhandenen Beziehungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bed02-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="bed02-116">Beim Kopieren von Servicevereinbarungspositionen aus einer Servicevorlage werden die Serviceobjekt- sowie die Serviceaufgabenbeziehungen automatisch entsprechend in die neuen Servicevereinbarungspositionen kopiert.</span><span class="sxs-lookup"><span data-stu-id="bed02-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="bed02-117">Manuelles Erstellen von Servicevertragspositionen</span><span class="sxs-lookup"><span data-stu-id="bed02-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="bed02-118">Fügen Sie im Formular **Servicevereinbarungen** eine Servicevertragsposition im Raster  hinzu.</span><span class="sxs-lookup"><span data-stu-id="bed02-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="bed02-119">Geben Sie die für die Servicevereinbarungsposition erforderlichen Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="bed02-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="bed02-120">Wählen Sie **Speichern**, um die Zeile zu speichern, und schließen Sie dann die Seite.</span><span class="sxs-lookup"><span data-stu-id="bed02-120">Select **Save** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="bed02-121">Erstellen einer Servicevereinbarung mithilfe des Moduls "Projekt"</span><span class="sxs-lookup"><span data-stu-id="bed02-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="bed02-122">Wählen Sie **Projektverwaltung und Buchhaltung**.</span><span class="sxs-lookup"><span data-stu-id="bed02-122">Select **Project management and accounting**.</span></span>
2. <span data-ttu-id="bed02-123">Wählen Sie **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="bed02-123">Select **All projects**.</span></span>
3. <span data-ttu-id="bed02-124">Wählen Sie in der Liste ein Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="bed02-124">Select the project from the list.</span></span>
4. <span data-ttu-id="bed02-125">Wählen Sie im **Aktivitätsbereich** die Option **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="bed02-125">On the **Action Pane**, select **Manage**.</span></span> <span data-ttu-id="bed02-126">Wählen Sie in der Gruppe **Neue** Aktion **Service** und wählen Sie **Servicesvereinbarung**.</span><span class="sxs-lookup"><span data-stu-id="bed02-126">In the **New** Action group, select **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="bed02-127">Führen Sie die Schritte im Abschnitt **Erstellen eines Servicevertrags** aus der Serviceverwaltung" (siehe vorheriger Kommentar in diesem Thema) aus.</span><span class="sxs-lookup"><span data-stu-id="bed02-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="bed02-128">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bed02-128">Related topics</span></span>

[<span data-ttu-id="bed02-129">Ausarbeiten und Festsetzen von Serviceverträge – Übersicht</span><span class="sxs-lookup"><span data-stu-id="bed02-129">Develop and establish service agreements overview</span></span>](service-agreements.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]