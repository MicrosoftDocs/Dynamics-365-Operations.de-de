---
title: Servicevorlagen
description: Sie können eine Servicevereinbarung als Vorlage definieren und später die Positionen dieser Vorlage in eine andere Servicevorlage oder in einen Serviceauftrag kopieren.
author: ShylaThompson
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 409c15ae9c8f5f3c9c72adf3313f4594ba3c1764
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819015"
---
# <a name="service-templates"></a><span data-ttu-id="bb160-103">Servicevorlagen</span><span class="sxs-lookup"><span data-stu-id="bb160-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb160-104">Sie können eine Servicevereinbarung als Vorlage definieren und später die Positionen dieser Vorlage in eine andere Servicevorlage oder in einen Serviceauftrag kopieren.</span><span class="sxs-lookup"><span data-stu-id="bb160-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="bb160-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bb160-105">Example</span></span>

<span data-ttu-id="bb160-106">Ein Debitor, für den Sie eine Serviceleistung erbringen, besitzt fünf identische Lastenaufzüge an fünf unterschiedlichen Standorten.</span><span class="sxs-lookup"><span data-stu-id="bb160-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="bb160-107">Für den Debitor sollen fünf einzelne Servicevereinbarungen eingerichtet werden – pro Standort jeweils eine.</span><span class="sxs-lookup"><span data-stu-id="bb160-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="bb160-108">Hierzu erstellen Sie eine Servicevereinbarung und geben diese als Vorlage für die Servicearbeiten an den Aufzügen an. Dadurch ersparen Sie sich nicht nur das wiederholte Ausführen der gleichen Schritte, sondern stellen überdies sicher, dass die Servicevereinbarungen identische Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bb160-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="bb160-109">Nun können die Vorlagenpositionen in die fünf neuen Servicevereinbarungen kopiert werden, sodass jede Servicevereinbarung mit den Positionen aus der Vorlage ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="bb160-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="bb160-110">Eine Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="bb160-110">Create a template</span></span>

<span data-ttu-id="bb160-111">Gehen Sie zum Erstellen einer Servicevorlage folgendermaßen vor: Erstellen Sie eine Servicevereinbarung, erstellen Sie die erforderlichen Positionen, und ordnen Sie die Servicevereinbarung anschließend einer Servicevorlagengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="bb160-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="bb160-112">Eine Servicevereinbarung kann nur dann als Vorlage fungieren, wenn ihr keine Serviceaufträge zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bb160-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="bb160-113">Umgekehrt lassen sich keine Serviceaufträge auf Basis einer Servicevereinbarung erstellen, die als Vorlage definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bb160-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="bb160-114">Vorlagenpositionen kopieren</span><span class="sxs-lookup"><span data-stu-id="bb160-114">Copy template lines</span></span>

<span data-ttu-id="bb160-115">Die Positionen einer Vorlage können aus einer Servicevorlage in eine andere Servicevorlage oder in ein einen Serviceauftrag kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="bb160-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="bb160-116">Beim Kopieren von Vorlagenpositionen in einen Serviceauftrag oder in eine Servicevereinbarung wird eine Strukturdarstellung der Vorlagengruppen angezeigt, in der die einzelnen Gruppen erweitert werden können.</span><span class="sxs-lookup"><span data-stu-id="bb160-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="bb160-117">Diese Darstellung ermöglicht das Anzeigen sämtlicher Vorlagen und Vorlagenpositionen.</span><span class="sxs-lookup"><span data-stu-id="bb160-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="bb160-118">Zur Vereinfachung der Suche nach den zu kopierenden Positionen empfiehlt es sich, die Vorlagen unter aussagekräftigen Namen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="bb160-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb160-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="bb160-119">Related topics</span></span>

[<span data-ttu-id="bb160-120">Kopieren von Servicevorlagenpositionen</span><span class="sxs-lookup"><span data-stu-id="bb160-120">Copy service templates lines</span></span>](copy-service-template-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]