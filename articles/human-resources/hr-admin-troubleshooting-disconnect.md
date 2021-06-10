---
title: Client wurde getrennt
description: In diesem Artikel wird erläutert, was zu tun ist, wenn Kunden von der Umgebung getrennt sind und den Grund nicht kennen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fcb7e5e3230aee9f6c04e4854c8eea836ae14c7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053418"
---
# <a name="client-disconnects"></a><span data-ttu-id="41f85-103">Client wurde getrennt</span><span class="sxs-lookup"><span data-stu-id="41f85-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="41f85-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="41f85-104">**Environment details**</span></span> 

<span data-ttu-id="41f85-105">Dieses Problem kann in allen Umgebungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="41f85-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="41f85-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="41f85-106">**Symptom**</span></span> 

<span data-ttu-id="41f85-107">Kunden sind von der Umgebung getrennt und kennen den Grund nicht.</span><span class="sxs-lookup"><span data-stu-id="41f85-107">The customer is disconnected from the environment and doesn't know why.</span></span> <span data-ttu-id="41f85-108">Der Kunde erhält eine der folgenden Fehlermeldungen:</span><span class="sxs-lookup"><span data-stu-id="41f85-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="41f85-109">Die Verbindung wurde getrennt</span><span class="sxs-lookup"><span data-stu-id="41f85-109">We've lost your connection.</span></span> <span data-ttu-id="41f85-110">Klicken Sie auf „Schließen”, um die Arbeit fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="41f85-110">Click Close to continue working.</span></span>
- <span data-ttu-id="41f85-111">Die Netzwerkverbindung wurde anscheinend unterbrochen. Klicken Sie auf 'Wiederholen', um es erneut zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="41f85-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="41f85-112">**Rote Markierung**</span><span class="sxs-lookup"><span data-stu-id="41f85-112">**Red flag**</span></span>

<span data-ttu-id="41f85-113">Dieses Problem tritt häufig auf, wenn Benutzer sich in der Implementierungsphase befinden, nachdem sie Informationen über Produktions- und Testumgebungen hinweg verglichen haben und dabei vergessen, dass sie sich zwischen Sitzungen hin- und herbewegen.</span><span class="sxs-lookup"><span data-stu-id="41f85-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="41f85-114">Wenn Benutzer in dieser Phase sind, erfahren sie höchstwahrscheinlich dieses Problem.</span><span class="sxs-lookup"><span data-stu-id="41f85-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="41f85-115">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="41f85-115">**Issue**</span></span> 

<span data-ttu-id="41f85-116">**Browsertypen:** Google Chrome, Internet Explorer und Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41f85-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="41f85-117">Microsoft Dynamics 365 Human Resources trennt die Verbindung von Benutzern, wenn verschiedene Sitzungen gleichzeitig für denselben Benutzer und denselben Browsertyp geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="41f85-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="41f85-118">(Benutzer A zeigt beispielsweise sowohl Umgebung 1 als auch Umgebung 2 in Chrome an.) Es spielt keine Rolle, ob die Benutzer verschiedene Browserfenster oder Registerkarten öffnen.</span><span class="sxs-lookup"><span data-stu-id="41f85-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="41f85-119">Wenn dieselben Benutzeranmeldeinformationen verwendet werden, um sich sowohl in Umgebung 1 als auch in Umgebung 2 gleichzeitig und im selben Browsertyp anzumelden, trennt Human Resources die Verbindung für eine der Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="41f85-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="41f85-120">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="41f85-120">**Solution**</span></span>

<span data-ttu-id="41f85-121">Stellen Sie sicher, dass nur eine Umgebung gleichzeitig für einen bestimmten Browsertyp geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="41f85-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="41f85-122">Benutzer können mehrere Sitzungen für die gleiche Umgebung öffnen (das heißt, mehrere Registerkarten im selben Browser).</span><span class="sxs-lookup"><span data-stu-id="41f85-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="41f85-123">Benutzer, die zwischen zwei Umgebung gleichzeitig hin- und herwechseln möchten, sollten jede Umgebung in einem anderen Browsertyp öffnen.</span><span class="sxs-lookup"><span data-stu-id="41f85-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="41f85-124">(Beispielsweise kann Benutzer A Umgebung 1 in Chrome und Umgebung 2 in Microsoft Edge anzeigen.)</span><span class="sxs-lookup"><span data-stu-id="41f85-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]