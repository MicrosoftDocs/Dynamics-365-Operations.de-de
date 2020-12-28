---
title: Wartungsanfragetypen
description: In diesem Thema wird erläutert, wie Wartungsanfragetypen in Asset Management eingerichtet werden.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d353f084e0d3e056f1b5ff5af6437ba211def8ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428815"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="8b5b8-103">Wartungsanfragetypen</span><span class="sxs-lookup"><span data-stu-id="8b5b8-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8b5b8-104">Wartungsanfragetypen werden verwendet, um Wartungsanfragen zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="8b5b8-105">Sie können beispielsweise Wartungsanfragetypen haben, die sich auf vorbeugende Wartung und korrektive Wartung beziehen.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="8b5b8-106">Oder Sie haben möglicherweise einen speziellen Wartungsanfragetyp, der verwendet wird, um die Reparatur von Anlagen (Depotreparatur) zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="8b5b8-107">Ein Wartungsanfragetyp definiert die Zuordnung zu einer Wartungsanfrage-Lebenszyklusstatusgruppe (Wartungsanfrage-Lebenszyklusmodell).</span><span class="sxs-lookup"><span data-stu-id="8b5b8-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="8b5b8-108">Wartungsanfrage-Lebenszyklusmodelle definieren die Lebenszyklusstatus, die für eine Wartungsanfrage festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="8b5b8-109">(Beispiele für Wartungsanfrage-Lebenszyklusstatus sind **Erstellt**, **Aktiv** und **Beendet**.)</span><span class="sxs-lookup"><span data-stu-id="8b5b8-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="8b5b8-110">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Wartungsanfragetypen**.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="8b5b8-111">Wählen Sie **Neu** aus, um einen Wartungsanfragetyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="8b5b8-112">Geben Sie im Feld **Wartungsanfragetyp** eine Kennung für den Wartungsanfragetyp ein.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="8b5b8-113">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="8b5b8-114">Wählen Sie auf dem Inforegister **Allgemein** im Feld **Wartungsanfrage-Lebenszyklusmodell** ein Wartungsanfrage-Lebenszyklusmodell aus.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="8b5b8-115">Wählen Sie im Feld **Arbeitsauftragstyp** einen Arbeitsauftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="8b5b8-116">Wenn eine Wartungsanfrage in einen Arbeitsauftrag konvertiert wird, erhält der Arbeitsauftrag automatisch den Arbeitsauftragstyp aus, der dem Wartungsanfragetyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="8b5b8-117">Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfragetypen**.</span><span class="sxs-lookup"><span data-stu-id="8b5b8-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Seite „Wartungsanfragentypen“](media/07-setup-for-requests.png)
