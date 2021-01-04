---
title: Debitorentreuekarten und Belohnungspunkte
description: In diesem Thema wird die Integration von Daten zu Kundenbindungskarten und Prämienpunkten mit dualem Schreiben beschrieben.
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
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683497"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="dbccc-103">Debitorentreuekarten und Belohnungspunkte</span><span class="sxs-lookup"><span data-stu-id="dbccc-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dbccc-104">Unternehmen klassifizieren Kunden und bieten anspruchsvolle Dienstleistungen basierend auf Kundeneinkaufs- und Ausgabenmustern.</span><span class="sxs-lookup"><span data-stu-id="dbccc-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="dbccc-105">Beispielsweise verfügt Dynamics 365 Commerce über die Infrastruktur und Funktionen zur Erleichterung und Verwaltung von Kundenbindungskarten, Prämienpunkten, loyalitätsbasierten Preisen und belohnungsbasierten Einkaufserlebnissen.</span><span class="sxs-lookup"><span data-stu-id="dbccc-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="dbccc-106">Wenn Daten zu Kundenbindungskarten und Prämienpunkten in Commerce mit Dataverse synchronisiert werden, können Customer Engagement-Apps diese Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="dbccc-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="dbccc-107">Beispielsweise können Benutzer des Dynamics 365 Customer Service die Daten verwenden, um über den Helpdesk dieselben anspruchsvollen Dienste bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dbccc-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="dbccc-108">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="dbccc-108">Templates</span></span>

| <span data-ttu-id="dbccc-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="dbccc-109">Finance and Operations apps</span></span> | <span data-ttu-id="dbccc-110">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="dbccc-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="dbccc-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbccc-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="dbccc-112">Treuekarte</span><span class="sxs-lookup"><span data-stu-id="dbccc-112">Loyalty card</span></span>                | <span data-ttu-id="dbccc-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="dbccc-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="dbccc-114">Diese Vorlage synchronisiert Informationen über Treukarten von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="dbccc-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="dbccc-115">Treuebelohnungspunkte</span><span class="sxs-lookup"><span data-stu-id="dbccc-115">Loyalty reward points</span></span>       | <span data-ttu-id="dbccc-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="dbccc-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="dbccc-117">Diese Vorlage synchronisiert Informationen über Belohnungspunkte von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="dbccc-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
