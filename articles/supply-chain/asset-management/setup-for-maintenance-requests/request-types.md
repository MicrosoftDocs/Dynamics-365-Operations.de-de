---
title: Wartungsanfragetypen
description: In diesem Thema wird erläutert, wie Wartungsanfragetypen in Asset Management eingerichtet werden.
author: johanhoffmann
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ff80b2f3e23f46467b8a2fe7a2abd805e5e3a20
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808495"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="72707-103">Wartungsanfragetypen</span><span class="sxs-lookup"><span data-stu-id="72707-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="72707-104">Wartungsanfragetypen werden verwendet, um Wartungsanfragen zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="72707-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="72707-105">Sie können beispielsweise Wartungsanfragetypen haben, die sich auf vorbeugende Wartung und korrektive Wartung beziehen.</span><span class="sxs-lookup"><span data-stu-id="72707-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="72707-106">Oder Sie haben möglicherweise einen speziellen Wartungsanfragetyp, der verwendet wird, um die Reparatur von Anlagen (Depotreparatur) zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="72707-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="72707-107">Ein Wartungsanfragetyp definiert die Zuordnung zu einer Wartungsanfrage-Lebenszyklusstatusgruppe (Wartungsanfrage-Lebenszyklusmodell).</span><span class="sxs-lookup"><span data-stu-id="72707-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="72707-108">Wartungsanfrage-Lebenszyklusmodelle definieren die Lebenszyklusstatus, die für eine Wartungsanfrage festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="72707-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="72707-109">(Beispiele für Wartungsanfrage-Lebenszyklusstatus sind **Erstellt**, **Aktiv** und **Beendet**.)</span><span class="sxs-lookup"><span data-stu-id="72707-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="72707-110">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Wartungsanfragen** \> **Wartungsanfragetypen**.</span><span class="sxs-lookup"><span data-stu-id="72707-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="72707-111">Wählen Sie **Neu** aus, um einen Wartungsanfragetyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="72707-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="72707-112">Geben Sie im Feld **Wartungsanfragetyp** eine Kennung für den Wartungsanfragetyp ein.</span><span class="sxs-lookup"><span data-stu-id="72707-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="72707-113">Geben Sie im Feld **Name** einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="72707-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="72707-114">Wählen Sie auf dem Inforegister **Allgemein** im Feld **Wartungsanfrage-Lebenszyklusmodell** ein Wartungsanfrage-Lebenszyklusmodell aus.</span><span class="sxs-lookup"><span data-stu-id="72707-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="72707-115">Wählen Sie im Feld **Arbeitsauftragstyp** einen Arbeitsauftragstyp aus.</span><span class="sxs-lookup"><span data-stu-id="72707-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="72707-116">Wenn eine Wartungsanfrage in einen Arbeitsauftrag konvertiert wird, erhält der Arbeitsauftrag automatisch den Arbeitsauftragstyp aus, der dem Wartungsanfragetyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="72707-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="72707-117">Die folgende Abbildung zeigt ein Beispiel der Seite **Wartungsanfragetypen**.</span><span class="sxs-lookup"><span data-stu-id="72707-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Seite „Wartungsanfragentypen“](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]