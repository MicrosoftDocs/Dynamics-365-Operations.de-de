---
title: Debitorentreuekarten und Belohnungspunkte
description: In diesem Thema wird die Integration von Daten zu Kundenbindungskarten und Prämienpunkten mit dualem Schreiben beschrieben.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568027"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="3bee7-103">Debitorentreuekarten und Belohnungspunkte</span><span class="sxs-lookup"><span data-stu-id="3bee7-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3bee7-104">Unternehmen klassifizieren Kunden und bieten anspruchsvolle Dienstleistungen basierend auf Kundeneinkaufs- und Ausgabenmustern.</span><span class="sxs-lookup"><span data-stu-id="3bee7-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="3bee7-105">Beispielsweise verfügt Dynamics 365 Commerce über die Infrastruktur und Funktionen zur Erleichterung und Verwaltung von Kundenbindungskarten, Prämienpunkten, loyalitätsbasierten Preisen und belohnungsbasierten Einkaufserlebnissen.</span><span class="sxs-lookup"><span data-stu-id="3bee7-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="3bee7-106">Wenn Daten zu Kundenbindungskarten und Prämienpunkten in Commerce mit Dataverse synchronisiert werden, können Customer Engagement-Apps diese Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="3bee7-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="3bee7-107">Beispielsweise können Benutzer des Dynamics 365 Customer Service die Daten verwenden, um über den Helpdesk dieselben anspruchsvollen Dienste bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3bee7-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="3bee7-108">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="3bee7-108">Templates</span></span>

| <span data-ttu-id="3bee7-109">Finance and Operations Apps</span><span class="sxs-lookup"><span data-stu-id="3bee7-109">Finance and Operations apps</span></span> | <span data-ttu-id="3bee7-110">Modellgesteuerte Anwendungen in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3bee7-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3bee7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3bee7-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="3bee7-112">Treuekarte</span><span class="sxs-lookup"><span data-stu-id="3bee7-112">Loyalty card</span></span>                | <span data-ttu-id="3bee7-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="3bee7-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="3bee7-114">Diese Vorlage synchronisiert Informationen über Treukarten von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="3bee7-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="3bee7-115">Treuebelohnungspunkte</span><span class="sxs-lookup"><span data-stu-id="3bee7-115">Loyalty reward points</span></span>       | <span data-ttu-id="3bee7-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="3bee7-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="3bee7-117">Diese Vorlage synchronisiert Informationen über Belohnungspunkte von Debitoren.</span><span class="sxs-lookup"><span data-stu-id="3bee7-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]