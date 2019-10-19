---
title: Talent-Client trennt Verbindung
description: In diesem Thema wird erläutert, was zu tun ist, wenn der Kunde/die Kundin von seiner/ihrer Umgebung getrennt ist und den Grund nicht kennt.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d174a8acac3863fb6d9f9431c6bc777cb717470
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008174"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="5c714-103">Talent-Client trennt Verbindung</span><span class="sxs-lookup"><span data-stu-id="5c714-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c714-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="5c714-104">**Environment details**</span></span> 

<span data-ttu-id="5c714-105">Dieses Problem kann in allen Umgebungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="5c714-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="5c714-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="5c714-106">**Symptom**</span></span> 

<span data-ttu-id="5c714-107">Der Kunde/die Kundin ist von seiner/ihrer Umgebung getrennt und kennt den Grund nicht.</span><span class="sxs-lookup"><span data-stu-id="5c714-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="5c714-108">Der Kunde erhält eine der folgenden Fehlermeldungen:</span><span class="sxs-lookup"><span data-stu-id="5c714-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="5c714-109">Die Verbindung wurde getrennt</span><span class="sxs-lookup"><span data-stu-id="5c714-109">We've lost your connection.</span></span> <span data-ttu-id="5c714-110">Klicken Sie auf „Schließen”, um die Arbeit fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="5c714-110">Click Close to continue working.</span></span>
- <span data-ttu-id="5c714-111">Die Netzwerkverbindung wurde anscheinend unterbrochen. Klicken Sie auf 'Wiederholen', um es erneut zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="5c714-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="5c714-112">**Rote Markierung**</span><span class="sxs-lookup"><span data-stu-id="5c714-112">**Red flag**</span></span>

<span data-ttu-id="5c714-113">Dieses Problem tritt häufig auf, wenn Benutzer sich in der Implementierungsphase befinden, nachdem sie Informationen über Produktions- und Testumgebungen hinweg verglichen haben und dabei vergessen, dass sie sich zwischen Sitzungen hin- und herbewegen.</span><span class="sxs-lookup"><span data-stu-id="5c714-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="5c714-114">Wenn Benutzer in dieser Phase sind, erfahren sie höchstwahrscheinlich dieses Problem.</span><span class="sxs-lookup"><span data-stu-id="5c714-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="5c714-115">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="5c714-115">**Issue**</span></span> 

<span data-ttu-id="5c714-116">**Browsertypen:** Google Chrome, Internet Explorer und Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5c714-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="5c714-117">Microsoft Dynamics 365 Talent trennt die Verbindung von Benutzern, wenn verschiedene Sitzungen gleichzeitig für denselben Benutzer und denselben Browsertyp geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="5c714-117">Microsoft Dynamics 365 Talent disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="5c714-118">(Benutzer A zeigt beispielsweise sowohl Umgebung 1 als auch Umgebung 2 in Chrome an.) Es spielt keine Rolle, ob die Benutzer verschiedene Browserfenster oder Registerkarten öffnen.</span><span class="sxs-lookup"><span data-stu-id="5c714-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="5c714-119">Wenn dieselben Benutzeranmeldeinformationen verwendet werden, um sich sowohl in Umgebung 1 als auch in Umgebung 2 gleichzeitig und im selben Browsertyp anzumelden, trennt Talent die Verbindung für eine der Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="5c714-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="5c714-120">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="5c714-120">**Solution**</span></span>

<span data-ttu-id="5c714-121">Stellen Sie sicher, dass nur eine Umgebung gleichzeitig für einen bestimmten Browsertyp geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5c714-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="5c714-122">Benutzer können mehrere Sitzungen für die gleiche Umgebung öffnen (das heißt, mehrere Registerkarten im selben Browser).</span><span class="sxs-lookup"><span data-stu-id="5c714-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="5c714-123">Benutzer, die zwischen zwei Umgebung gleichzeitig hin- und herwechseln möchten, sollten jede Umgebung in einem anderen Browsertyp öffnen.</span><span class="sxs-lookup"><span data-stu-id="5c714-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="5c714-124">(Beispielsweise kann Benutzer A Umgebung 1 in Chrome und Umgebung 2 in Microsoft Edge anzeigen.)</span><span class="sxs-lookup"><span data-stu-id="5c714-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
