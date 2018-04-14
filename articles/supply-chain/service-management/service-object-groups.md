---
title: Serviceobjektgruppen
description: "Objektgruppen sind zum Sortieren und Filtern der Daten von Objekten für Berichte und Statistiken nützlich."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e539d92753bbbc4ac0ca88cec83c4d15135c388b
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="d113e-103">Serviceobjektgruppen</span><span class="sxs-lookup"><span data-stu-id="d113e-103">Service object groups</span></span> 

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d113e-104">Objektgruppen sind zum Sortieren und Filtern der Daten von Objekten für Berichte und Statistiken nützlich.</span><span class="sxs-lookup"><span data-stu-id="d113e-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="d113e-105">Objekte können z. B. nach der geografischen Position oder nach dem Typ gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="d113e-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="d113e-106">Gruppieren nach geografischer Position</span><span class="sxs-lookup"><span data-stu-id="d113e-106">Group by geographical location</span></span>

<span data-ttu-id="d113e-107">Mit dieser Gruppierungsmethode kann angezeigt werden, wo sich die verschiedenen Objekte befinden, für die das Unternehmen Services anbietet.</span><span class="sxs-lookup"><span data-stu-id="d113e-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="d113e-108">Das Gruppieren von Objekten nach geografischer Position kann außerdem hilfreich sein, wenn z. B. die Objekte bestimmt werden müssen, für die in einem bestimmten Land oder einer Region bereits Services erbracht werden.</span><span class="sxs-lookup"><span data-stu-id="d113e-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="d113e-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d113e-109">Example</span></span>

<span data-ttu-id="d113e-110">Ein Debitor aus Belgien ruft beim Kundendienst an und möchte eine Servicevereinbarung für das Objekt ABC erstellen.</span><span class="sxs-lookup"><span data-stu-id="d113e-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="d113e-111">Sie haben eine Objektgruppe mit geografischer Position Belgien allen Objekten in Belgien zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d113e-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="d113e-112">Unter Verwendung dieser Gruppe als Filter kann schnell festgestellt werden, ob ABC bereits als Datensatz in der Anwendung vorhanden ist oder ob ein neues Objekt eingerichtet werden muss.</span><span class="sxs-lookup"><span data-stu-id="d113e-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="d113e-113">Gruppieren nach Typ</span><span class="sxs-lookup"><span data-stu-id="d113e-113">Group by type</span></span>

<span data-ttu-id="d113e-114">Mit dieser Gruppierungsmethode kann angezeigt werden, für welche Objekttypen das Unternehmen Services anbietet.</span><span class="sxs-lookup"><span data-stu-id="d113e-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="d113e-115">Das Gruppieren von Objekten nach Typ kann außerdem hilfreich sein, wenn z. B. ein neues Objekt basierend auf ähnlichen in der Anwendung bereits vorhandenen Objekten erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d113e-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="d113e-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d113e-116">Example</span></span>

<span data-ttu-id="d113e-117">Ein Debitor ruft an und möchte eine Servicevereinbarung für eine Klimaanlage HIJ einrichten.</span><span class="sxs-lookup"><span data-stu-id="d113e-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="d113e-118">Für diese Anlage ist noch kein Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d113e-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="d113e-119">Es ist jedoch bereits eine Objektgruppe Klimaanlagen eingerichtet, die allen Klimaanlagenobjekten zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d113e-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="d113e-120">Sie können deshalb schnell nach allen anderen Klimaanlagen suchen und die Vorlageninformationen aus diesen Objekten als Grundlage für Servicevertragspositionen für HIJ verwenden.</span><span class="sxs-lookup"><span data-stu-id="d113e-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="d113e-121">Wenn Sie Objektgruppen auf diese Weise verwenden, können Sie umgehend neue Objekte einrichten und die Serviceaufgaben bestimmen, die dafür ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d113e-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




