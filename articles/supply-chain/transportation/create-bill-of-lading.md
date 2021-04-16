---
title: Einen Frachtbrief erstellen
description: In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a14d971475c71e6a02957acfa0c6e6494c4638fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807631"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="703c5-103">Einen Frachtbrief erstellen</span><span class="sxs-lookup"><span data-stu-id="703c5-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="703c5-104">In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="703c5-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="703c5-105">Ein Frachtbrief ist ein Vertrag zwischen dem Unternehmen, das den Artikel versendet und dem Spediteur.</span><span class="sxs-lookup"><span data-stu-id="703c5-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="703c5-106">Das Dokument liegt den Versandartikeln bei und dient als Lieferbeleg, wenn die Artikel am Zielort ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="703c5-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="703c5-107">Wenn Sie die Lagerortverwaltung verwenden, gibt es zwei Möglichkeiten, einen Frachtbrief zu generieren:</span><span class="sxs-lookup"><span data-stu-id="703c5-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="703c5-108">Erstellen Sie den Bericht manuell über die Seite **Frachtbrief**.</span><span class="sxs-lookup"><span data-stu-id="703c5-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="703c5-109">Generieren Sie den Bericht aus **Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="703c5-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="703c5-110">Wenn Sie den Frachtbrief aus dem **Ladungsplanungsworkbench** generieren, muss der Ladungsstatus **. Versendet** sein.</span><span class="sxs-lookup"><span data-stu-id="703c5-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="703c5-111">Wenn mehr als eine Lieferung für die Auslastung vorhanden sind, wird ein Frachtbrief für jede Lieferung erstellt.</span><span class="sxs-lookup"><span data-stu-id="703c5-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="703c5-112">Nachdem ein Frachtbrief erstellt wurde, können Sie die auf der Seite **Frachtbrief** Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="703c5-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="703c5-113">Hauptfrachtbrief</span><span class="sxs-lookup"><span data-stu-id="703c5-113">Master bill of lading</span></span>
<span data-ttu-id="703c5-114">Wenn mehr als eine Lieferung in einer Ladung enthalten ist, können Sie einen Hauptfrachtbrief generieren.</span><span class="sxs-lookup"><span data-stu-id="703c5-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="703c5-115">Dieser hat das gleiche Layout und die Informationen wie ein Frachtbrief, aber enthält den zusammengefassten Inhalt aller Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="703c5-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="703c5-116">Wenn die Option **Erstellen Sie einen Hauptfrachtbrief, wenn mehr als eine Lieferung in einer Ladung enthalten ist.** auf **Ja** auf der Seite **Transportverwaltungsparameter** festgelegt ist, wird automatisch ein Hauptfrachtbrief generiert, wenn Sie einen Frachtbrief aus dem **Ladungsplanungsworkbench** erstellen und es mehrere Lieferung gibt.</span><span class="sxs-lookup"><span data-stu-id="703c5-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="703c5-117">Sie können eine Liste der Frachtbriefe auch abrufen, indem Sie auf **Zugehörige Informationen** &gt; **Frachtbrief** klicken.</span><span class="sxs-lookup"><span data-stu-id="703c5-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="703c5-118">Wenn Sie Frachtbriefe manuell erstellen, können Sie einen Hauptfrachtbrief auf der Seite **Frachtbrief** erstellen.</span><span class="sxs-lookup"><span data-stu-id="703c5-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]