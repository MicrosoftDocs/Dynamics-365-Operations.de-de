---
title: Debitorentreuekarten und Belohnungspunkte
description: Dieses Thema beschreibt die Integration von Daten zu Kundenbindungskarten und Prämienpunkten zwischen Finance and Operations-Apps und Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998013"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="60949-103">Debitorentreuekarten und Belohnungspunkte</span><span class="sxs-lookup"><span data-stu-id="60949-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="60949-104">Unternehmen klassifizieren Kunden und bieten anspruchsvolle Dienstleistungen basierend auf Kundeneinkaufs- und Ausgabenmustern.</span><span class="sxs-lookup"><span data-stu-id="60949-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="60949-105">In der Microsoft Dynamics 365-Anwendungssuite verfügt Dynamics 365 Commerce über die Infrastruktur und Funktionen zur Erleichterung und Verwaltung von Kundenbindungskarten, Prämienpunkten, loyalitätsbasierten Preisen und belohnungsbasierten Einkaufserlebnissen.</span><span class="sxs-lookup"><span data-stu-id="60949-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="60949-106">Wenn Daten zu Kundenbindungskarten und Prämienpunkten in Commerce mit dem Common Data Service synchronisiert werden, können modellgesteuerte Apps in Dynamics 365 diese Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="60949-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="60949-107">Beispielsweise können Benutzer des Dynamics 365 Customer Service die Daten verwenden, um über den Helpdesk dieselben anspruchsvollen Dienste bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="60949-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="60949-108">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="60949-108">Templates</span></span>

| <span data-ttu-id="60949-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="60949-109">Finance and Operations apps</span></span> | <span data-ttu-id="60949-110">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="60949-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="60949-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60949-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="60949-112">Treuekarte</span><span class="sxs-lookup"><span data-stu-id="60949-112">Loyalty card</span></span>                | <span data-ttu-id="60949-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="60949-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="60949-114">Diese Vorlage synchronisiert Informationen über Treukarten von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="60949-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="60949-115">Treuebelohnungspunkte</span><span class="sxs-lookup"><span data-stu-id="60949-115">Loyalty reward points</span></span>       | <span data-ttu-id="60949-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="60949-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="60949-117">Diese Vorlage synchronisiert Informationen über Belohnungspunkte von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="60949-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
