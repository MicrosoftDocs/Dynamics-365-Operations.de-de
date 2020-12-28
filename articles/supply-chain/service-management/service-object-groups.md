---
title: Serviceobjektgruppen
description: Objektgruppen sind zum Sortieren und Filtern der Daten von Objekten für Berichte und Statistiken nützlich.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4438487fa234cf093b557bca9455717b2cd3ca0b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428391"
---
# <a name="service-object-groups"></a><span data-ttu-id="f339a-103">Serviceobjektgruppen</span><span class="sxs-lookup"><span data-stu-id="f339a-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f339a-104">Objektgruppen sind zum Sortieren und Filtern der Daten von Objekten für Berichte und Statistiken nützlich.</span><span class="sxs-lookup"><span data-stu-id="f339a-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="f339a-105">Objekte können z. B. nach der geografischen Position oder nach dem Typ gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="f339a-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="f339a-106">Gruppieren nach geografischer Position</span><span class="sxs-lookup"><span data-stu-id="f339a-106">Group by geographical location</span></span>

<span data-ttu-id="f339a-107">Mit dieser Gruppierungsmethode kann angezeigt werden, wo sich die verschiedenen Objekte befinden, für die das Unternehmen Services anbietet.</span><span class="sxs-lookup"><span data-stu-id="f339a-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="f339a-108">Das Gruppieren von Objekten nach geografischer Position kann außerdem hilfreich sein, wenn z. B. die Objekte bestimmt werden müssen, für die in einem bestimmten Land oder einer Region bereits Services erbracht werden.</span><span class="sxs-lookup"><span data-stu-id="f339a-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="f339a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f339a-109">Example</span></span>

<span data-ttu-id="f339a-110">Ein Debitor aus Belgien ruft beim Kundendienst an und möchte eine Servicevereinbarung für das Objekt ABC erstellen.</span><span class="sxs-lookup"><span data-stu-id="f339a-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="f339a-111">Sie haben eine Objektgruppe mit geografischer Position Belgien allen Objekten in Belgien zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f339a-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="f339a-112">Unter Verwendung dieser Gruppe als Filter kann schnell festgestellt werden, ob ABC bereits als Datensatz in der Anwendung vorhanden ist oder ob ein neues Objekt eingerichtet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f339a-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="f339a-113">Gruppieren nach Typ</span><span class="sxs-lookup"><span data-stu-id="f339a-113">Group by type</span></span>

<span data-ttu-id="f339a-114">Mit dieser Gruppierungsmethode kann angezeigt werden, für welche Objekttypen das Unternehmen Services anbietet.</span><span class="sxs-lookup"><span data-stu-id="f339a-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="f339a-115">Das Gruppieren von Objekten nach Typ kann außerdem hilfreich sein, wenn z. B. ein neues Objekt basierend auf ähnlichen in der Anwendung bereits vorhandenen Objekten erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f339a-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="f339a-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f339a-116">Example</span></span>

<span data-ttu-id="f339a-117">Ein Debitor ruft an und möchte eine Servicevereinbarung für eine Klimaanlage HIJ einrichten.</span><span class="sxs-lookup"><span data-stu-id="f339a-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="f339a-118">Für diese Anlage ist noch kein Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f339a-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="f339a-119">Es ist jedoch bereits eine Objektgruppe Klimaanlagen eingerichtet, die allen Klimaanlagenobjekten zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="f339a-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="f339a-120">Sie können deshalb schnell nach allen anderen Klimaanlagen suchen und die Vorlageninformationen aus diesen Objekten als Grundlage für Servicevertragspositionen für HIJ verwenden.</span><span class="sxs-lookup"><span data-stu-id="f339a-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="f339a-121">Wenn Sie Objektgruppen auf diese Weise verwenden, können Sie umgehend neue Objekte einrichten und die Serviceaufgaben bestimmen, die dafür ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f339a-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="f339a-122">Erstellen von Serviceobjektgruppen</span><span class="sxs-lookup"><span data-stu-id="f339a-122">Create service object groups</span></span>

<span data-ttu-id="f339a-123">Erstellen von Gruppen, denen Sie Serviceobjekte zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="f339a-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="f339a-124">Serviceobjekte sind Lagerartikel und andere Produkte, für die Services ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f339a-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="f339a-125">Wenn Sie Serviceobjekte gruppieren, können Sie Berichte für ähnliche und zugehörige Serviceobjekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="f339a-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="f339a-126">Beispielsweise kann eine Serviceobjektgruppe aus zwei Serviceobjekten bestehen: Ein Serviceobjekt ist ein Bausatz, und das zweite Serviceobjekt ist der Service, um den Bausatz zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f339a-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="f339a-127">Um Serviceobjektgruppen zu erstellen, führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f339a-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="f339a-128">Klicken Sie auf **Serviceverwaltung > Einstellungen > Serviceobjekte > Serviceobjektgruppen.**</span><span class="sxs-lookup"><span data-stu-id="f339a-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="f339a-129">Klicken Sie auf **Neu**, um eine neue Serviceobjektgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f339a-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="f339a-130">Geben Sie einen eindeutigen Namen für die Serviceobjektgruppe sowie (optional) eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="f339a-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="f339a-131">Sie können Serviceobjekte der Gruppe zuordnen, indem Sie das Formular **Serviceobjekte** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f339a-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="f339a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f339a-132">See also</span></span>

[<span data-ttu-id="f339a-133">Erstellen von Serviceobjekten</span><span class="sxs-lookup"><span data-stu-id="f339a-133">Create service objects</span></span>](create-service-objects.md)


