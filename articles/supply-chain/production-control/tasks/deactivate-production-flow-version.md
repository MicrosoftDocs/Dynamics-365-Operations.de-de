---
title: Eine Produktionsflussversion deaktivieren
description: Wenn eine aktive Produktionsflussversion nicht mehr erforderlich ist, kann diese deaktiviert werden.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ec2d9f8b275cd4babdf46434aebf0cbf9105eed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212111"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="01f38-103">Eine Produktionsflussversion deaktivieren</span><span class="sxs-lookup"><span data-stu-id="01f38-103">Deactivate a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01f38-104">Wenn eine aktive Produktionsflussversion nicht mehr erforderlich ist, kann diese deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="01f38-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="01f38-105">Sie sollten diese Option nur verwenden, wenn alle Kanban-Regeln und Aktivitäten beendet sind und nicht erneut aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="01f38-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="01f38-106">Beachten Sie, dass das Ablaufdatum aller Kanban-Regeln für diese Produktionsflussversion mit dem aktuellen Datum und der aktuellen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="01f38-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="01f38-107">Um eine aktive Produktionsflussversion zu ändern, sollten Sie ein Ablaufdatum für die aktive Version festgelegt und eine neue Version erstellen.</span><span class="sxs-lookup"><span data-stu-id="01f38-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="01f38-108">Dadurch wird es Ihnen ermöglicht, die Produktionsarbeitsgänge beim Vorbereiten der neuen Version sowie der verwandten Kanban-Regeln fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="01f38-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="01f38-109">Um eine aktive Produktionsflussversion ablaufen zu lassen, müssen Sie ein Ablaufdatum festlegen.</span><span class="sxs-lookup"><span data-stu-id="01f38-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="01f38-110">Die Deaktivierung ist somit mehr eine Ausnahme als eine Regel.</span><span class="sxs-lookup"><span data-stu-id="01f38-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="01f38-111">Für diese Prozedur benötigen Sie einen Produktionsfluss mit einer Version, die deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="01f38-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="01f38-112">Führen Sie dies nicht in einer Produktionsumgebung aus, es sei denn, Sie sind 100% sicher, dass die Version nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="01f38-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="01f38-113">Eine Produktionsflussversion deaktivieren</span><span class="sxs-lookup"><span data-stu-id="01f38-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="01f38-114">Wechseln Sie zu "Produktionssteuerung" > "Einrichten" > "Lean-Produktionsfluss" > "Produktionsflüsse".</span><span class="sxs-lookup"><span data-stu-id="01f38-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="01f38-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="01f38-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="01f38-116">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="01f38-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="01f38-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="01f38-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="01f38-118">Klicken Sie auf "Deaktivieren".</span><span class="sxs-lookup"><span data-stu-id="01f38-118">Click Deactivate.</span></span>
    * <span data-ttu-id="01f38-119">Fahren Sie fort nicht, wenn Sie nicht 100% sicher sind, dass die Produktionsflussversion nicht mehr aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="01f38-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="01f38-120">Beim Klicken auf "Ok" laufen alle aktiven Kaban-Regeln aus und alle Produktions- und Wiederbeschaffungsaktivitäten dieser Produktionsflussversion werden sofort gestoppt.</span><span class="sxs-lookup"><span data-stu-id="01f38-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="01f38-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="01f38-121">Click OK.</span></span>

