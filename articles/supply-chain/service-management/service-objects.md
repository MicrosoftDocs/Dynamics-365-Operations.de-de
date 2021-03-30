---
title: Übersicht der Serviceobjekte
description: Serviceobjekte sind die Anlagen und Produkte eines Debitors, für die Sie eine Dienstleistung durchführen können.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dae74ebb59d73e1197426757ec9c050b1905852e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211789"
---
# <a name="service-objects-overview"></a><span data-ttu-id="943e7-103">Übersicht der Serviceobjekte</span><span class="sxs-lookup"><span data-stu-id="943e7-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="943e7-104">Serviceobjekte sind die Anlagen und Produkte eines Debitors, für die Sie eine Dienstleistung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="943e7-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="943e7-105">Abhängig von der Art der angebotenen Dienstleistung handelt es sich entweder um ein materielles oder um ein immaterielles Objekt:</span><span class="sxs-lookup"><span data-stu-id="943e7-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="943e7-106">Materielle Objekte sind Dinge wie Maschinen oder Gebäude, für die eine physische Serviceaufgabe ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="943e7-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="943e7-107">Bei einem materiellen Serviceobjekt kann es sich auch um einen Lagerartikel handeln, den Sie in den freigegebenen Produktdetails erstellen.</span><span class="sxs-lookup"><span data-stu-id="943e7-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="943e7-108">Abhängig von der zugeordneten Lagerungsdimensionsgruppe, die Sie dem Artikel zuweisen, können Sie ein Serviceobjekt bis hinunter zu einer Ebene erstellen, die die Artikelseriennummer enthält.</span><span class="sxs-lookup"><span data-stu-id="943e7-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="943e7-109">Dies ist hilfreich, wenn der exakte Artikel verfolgt werden muss, für den das Serviceobjekt steht.</span><span class="sxs-lookup"><span data-stu-id="943e7-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="943e7-110">Ein materielles Serviceobjekt kann auch ein Artikel sein, der nicht direkt mit der direkten Produktion oder Lieferkette des Unternehmens verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="943e7-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="943e7-111">So kann ein Tool-Kit, das für Reparaturen in einem Serviceauftrag verwendet wird, ein Serviceobjekt sein, das nicht in den Bestand einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="943e7-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="943e7-112">In diesem Fall erfassen Sie es nicht als Lagerartikel.</span><span class="sxs-lookup"><span data-stu-id="943e7-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="943e7-113">Immaterielle Objekte sind nicht physische Dinge, wie ein Konto oder ein Vertrag, für die Sie eine Serviceaufgabe ausgeführen können.</span><span class="sxs-lookup"><span data-stu-id="943e7-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="943e7-114">Beispiel für ein immaterielles Serviceobjekt</span><span class="sxs-lookup"><span data-stu-id="943e7-114">Example of an intangible service object</span></span>

<span data-ttu-id="943e7-115">Unternehmen A verwaltet die Finanzdatensätze für eine Reihe von kleinen Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="943e7-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="943e7-116">Einer der Kunden von Unternehmen A ist das lokale Fußballteam, für das Unternehmen A die wöchentliche Buchführung sowie die Jahresabschlussprüfung der Konten des Vereins durchführt.</span><span class="sxs-lookup"><span data-stu-id="943e7-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="943e7-117">Die Konten des Vereins werden im Formular Dienstleistungsobjekte eingerichtet und als das Objekt im Servicevertrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="943e7-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="943e7-118">Es gibt zwei Servicevertragspositionen für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="943e7-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="943e7-119">Position 1 ist die wöchentliche Buchführung mit einem wöchentlichen Intervall, das der Position zugeordnet ist, und Position 2 ist die Jahresabschlussprüfung mit einem jährlichen Intervall, das ihr zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="943e7-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="943e7-120">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="943e7-120">Related topics</span></span>

[<span data-ttu-id="943e7-121">Erstellen von Serviceobjekten</span><span class="sxs-lookup"><span data-stu-id="943e7-121">Create service objects</span></span>](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]