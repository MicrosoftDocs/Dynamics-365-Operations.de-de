---
title: Servicevorlagen
description: "Sie können eine Servicevereinbarung als Vorlage definieren und später die Positionen dieser Vorlage in eine andere Servicevorlage oder in einen Serviceauftrag kopieren."
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c4bde1869b2be6e4cbbf979dae1b84c2a4974a9
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="service-templates"></a><span data-ttu-id="59a49-103">Servicevorlagen</span><span class="sxs-lookup"><span data-stu-id="59a49-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59a49-104">Sie können eine Servicevereinbarung als Vorlage definieren und später die Positionen dieser Vorlage in eine andere Servicevorlage oder in einen Serviceauftrag kopieren.</span><span class="sxs-lookup"><span data-stu-id="59a49-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="59a49-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="59a49-105">Example</span></span>

<span data-ttu-id="59a49-106">Ein Debitor, für den Sie eine Serviceleistung erbringen, besitzt fünf identische Lastenaufzüge an fünf unterschiedlichen Standorten.</span><span class="sxs-lookup"><span data-stu-id="59a49-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="59a49-107">Für den Debitor sollen fünf einzelne Servicevereinbarungen eingerichtet werden – pro Standort jeweils eine.</span><span class="sxs-lookup"><span data-stu-id="59a49-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="59a49-108">Hierzu erstellen Sie eine Servicevereinbarung und geben diese als Vorlage für die Servicearbeiten an den Aufzügen an. Dadurch ersparen Sie sich nicht nur das wiederholte Ausführen der gleichen Schritte, sondern stellen überdies sicher, dass die Servicevereinbarungen identische Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59a49-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="59a49-109">Nun können die Vorlagenpositionen in die fünf neuen Servicevereinbarungen kopiert werden, sodass jede Servicevereinbarung mit den Positionen aus der Vorlage ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="59a49-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="59a49-110">Eine Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="59a49-110">Create a template</span></span>

<span data-ttu-id="59a49-111">Gehen Sie zum Erstellen einer Servicevorlage folgendermaßen vor: Erstellen Sie eine Servicevereinbarung, erstellen Sie die erforderlichen Positionen, und ordnen Sie die Servicevereinbarung anschließend einer Servicevorlagengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="59a49-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="59a49-112">Eine Servicevereinbarung kann nur dann als Vorlage fungieren, wenn ihr keine Serviceaufträge zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="59a49-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="59a49-113">Umgekehrt lassen sich keine Serviceaufträge auf Basis einer Servicevereinbarung erstellen, die als Vorlage definiert ist.</span><span class="sxs-lookup"><span data-stu-id="59a49-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="59a49-114">Vorlagenpositionen kopieren</span><span class="sxs-lookup"><span data-stu-id="59a49-114">Copy template lines</span></span>

<span data-ttu-id="59a49-115">Die Positionen einer Vorlage können aus einer Servicevorlage in eine andere Servicevorlage oder in ein einen Serviceauftrag kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="59a49-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="59a49-116">Beim Kopieren von Vorlagenpositionen in einen Serviceauftrag oder in eine Servicevereinbarung wird eine Strukturdarstellung der Vorlagengruppen angezeigt, in der die einzelnen Gruppen erweitert werden können.</span><span class="sxs-lookup"><span data-stu-id="59a49-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="59a49-117">Diese Darstellung ermöglicht das Anzeigen sämtlicher Vorlagen und Vorlagenpositionen.</span><span class="sxs-lookup"><span data-stu-id="59a49-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="59a49-118">Zur Vereinfachung der Suche nach den zu kopierenden Positionen empfiehlt es sich, die Vorlagen unter aussagekräftigen Namen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="59a49-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a49-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="59a49-119">Related topics</span></span>

[<span data-ttu-id="59a49-120">Kopieren von Servicevorlagenpositionen</span><span class="sxs-lookup"><span data-stu-id="59a49-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

