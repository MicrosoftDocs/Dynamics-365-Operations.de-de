---
title: Einen Frachtbrief erstellen
description: In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd014f5804681936920b47e999709f153def11bc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429122"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="094e8-103">Einen Frachtbrief erstellen</span><span class="sxs-lookup"><span data-stu-id="094e8-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="094e8-104">In diesem Thema wird beschrieben, wie Sie einen Frachtbrief erstellen, wenn der Lagerortverwaltungsprozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="094e8-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="094e8-105">Ein Frachtbrief ist ein Vertrag zwischen dem Unternehmen, das den Artikel versendet und dem Spediteur.</span><span class="sxs-lookup"><span data-stu-id="094e8-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="094e8-106">Das Dokument liegt den Versandartikeln bei und dient als Lieferbeleg, wenn die Artikel am Zielort ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="094e8-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="094e8-107">Wenn Sie die Lagerortverwaltung verwenden, gibt es zwei Möglichkeiten, einen Frachtbrief zu generieren:</span><span class="sxs-lookup"><span data-stu-id="094e8-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="094e8-108">Erstellen Sie den Bericht manuell über die Seite **Frachtbrief**.</span><span class="sxs-lookup"><span data-stu-id="094e8-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="094e8-109">Generieren Sie den Bericht aus **Ladungsplanungsworkbench**.</span><span class="sxs-lookup"><span data-stu-id="094e8-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="094e8-110">Wenn Sie den Frachtbrief aus dem **Ladungsplanungsworkbench** generieren, muss der Ladungsstatus **. Versendet** sein.</span><span class="sxs-lookup"><span data-stu-id="094e8-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="094e8-111">Wenn mehr als eine Lieferung für die Auslastung vorhanden sind, wird ein Frachtbrief für jede Lieferung erstellt.</span><span class="sxs-lookup"><span data-stu-id="094e8-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="094e8-112">Nachdem ein Frachtbrief erstellt wurde, können Sie die auf der Seite **Frachtbrief** Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="094e8-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="094e8-113">Hauptfrachtbrief</span><span class="sxs-lookup"><span data-stu-id="094e8-113">Master bill of lading</span></span>
<span data-ttu-id="094e8-114">Wenn mehr als eine Lieferung in einer Ladung enthalten ist, können Sie einen Hauptfrachtbrief generieren.</span><span class="sxs-lookup"><span data-stu-id="094e8-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="094e8-115">Dieser hat das gleiche Layout und die Informationen wie ein Frachtbrief, aber enthält den zusammengefassten Inhalt aller Lieferungen.</span><span class="sxs-lookup"><span data-stu-id="094e8-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="094e8-116">Wenn die Option **Erstellen Sie einen Hauptfrachtbrief, wenn mehr als eine Lieferung in einer Ladung enthalten ist.** auf **Ja** auf der Seite **Transportverwaltungsparameter** festgelegt ist, wird automatisch ein Hauptfrachtbrief generiert, wenn Sie einen Frachtbrief aus dem **Ladungsplanungsworkbench** erstellen und es mehrere Lieferung gibt.</span><span class="sxs-lookup"><span data-stu-id="094e8-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="094e8-117">Sie können eine Liste der Frachtbriefe auch abrufen, indem Sie auf **Zugehörige Informationen** &gt; **Frachtbrief** klicken.</span><span class="sxs-lookup"><span data-stu-id="094e8-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="094e8-118">Wenn Sie Frachtbriefe manuell erstellen, können Sie einen Hauptfrachtbrief auf der Seite **Frachtbrief** erstellen.</span><span class="sxs-lookup"><span data-stu-id="094e8-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



