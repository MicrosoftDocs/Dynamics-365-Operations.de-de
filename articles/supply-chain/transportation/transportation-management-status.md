---
title: Status der Transportverwaltung
description: In diesem Thema wird erklärt, wie Sie einen Transportstatus erstellen und diesen Status einem Spediteur-Status zuordnen.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4429166"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="6c2e5-103">Status der Transportverwaltung</span><span class="sxs-lookup"><span data-stu-id="6c2e5-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c2e5-104">Legen Sie Mastercodes für Transportstatus fest, um Codes zu interpretieren, die von Ihren Spediteuren bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="6c2e5-105">So können Sie mit Spediteuren zusammenarbeiten, um einen Status bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="6c2e5-106">Der Transportstatus, den Sie für einen Transport-Stammstatuscode bereitstellen, kann Ihnen helfen, den Status einer Ladung, einer Sendung oder eines Containers zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="6c2e5-107">Der spezifische Transportstatus für eine Ladung, eine Sendung oder einen Container kann nur durch Datenintegration und nicht manuell über die Benutzeroberfläche aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="6c2e5-108">Erzeugen eines Transportstatus</span><span class="sxs-lookup"><span data-stu-id="6c2e5-108">Create a transportation status</span></span>

<span data-ttu-id="6c2e5-109">Um einen Transportstatus zu erstellen, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="6c2e5-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="6c2e5-110">Gehen Sie zu **Transportverwaltung \> Einrichten \> Transportstatus-Stämme**.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="6c2e5-111">Wählen Sie **Neu**, um einen Transportstatus-Stamm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="6c2e5-112">Geben Sie in das Feld **Transportstatus-Stamm** einen eindeutigen Code für den Transportstatus ein.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="6c2e5-113">Wählen Sie im Feld **Transportart** entweder *Spediteur* oder *Hub* als Transportart.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="6c2e5-114">Geben Sie einen Namen und einen Transportstatus ein.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="6c2e5-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="6c2e5-116">Zuordnen eines Transportstatus zu einem Spediteur-Status</span><span class="sxs-lookup"><span data-stu-id="6c2e5-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="6c2e5-117">Um einen Transportstatus einem Spediteur-Status zuzuordnen, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="6c2e5-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="6c2e5-118">Gehen Sie zu **Transportverwaltung \> Einrichten \> Spediteure \> Spediteur-Transportstatus**.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="6c2e5-119">Wählen Sie **Neu**, um einen Code eines Spediteurs einem Transportstatus-Stammcode zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="6c2e5-120">Wählen Sie die eindeutige ID für den Spediteur und den Speditionsdienst.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="6c2e5-121">Wählen Sie den Transportstatus-Code, den Sie dem Code des gewählten Spediteurs zuordnen wollen.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="6c2e5-122">Geben Sie den externen Code ein, der von dem Spediteur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="6c2e5-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6c2e5-123">Close the page.</span></span>
