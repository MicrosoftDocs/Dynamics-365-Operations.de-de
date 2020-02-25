---
title: Client wurde getrennt
description: In diesem Artikel wird erläutert, was zu tun ist, wenn der Kunde/die Kundin von seiner/ihrer Umgebung getrennt ist und den Grund nicht kennt.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.article: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73f0c31d5153a82651ed77aa37bc10966ce7c9b1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009118"
---
# <a name="client-disconnects"></a><span data-ttu-id="26f47-103">Client wurde getrennt</span><span class="sxs-lookup"><span data-stu-id="26f47-103">Client disconnects</span></span>

<span data-ttu-id="26f47-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="26f47-104">**Environment details**</span></span> 

<span data-ttu-id="26f47-105">Dieses Problem kann in allen Umgebungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="26f47-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="26f47-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="26f47-106">**Symptom**</span></span> 

<span data-ttu-id="26f47-107">Der Kunde/die Kundin ist von seiner/ihrer Umgebung getrennt und kennt den Grund nicht.</span><span class="sxs-lookup"><span data-stu-id="26f47-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="26f47-108">Der Kunde erhält eine der folgenden Fehlermeldungen:</span><span class="sxs-lookup"><span data-stu-id="26f47-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="26f47-109">Die Verbindung wurde getrennt</span><span class="sxs-lookup"><span data-stu-id="26f47-109">We've lost your connection.</span></span> <span data-ttu-id="26f47-110">Klicken Sie auf „Schließen”, um die Arbeit fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="26f47-110">Click Close to continue working.</span></span>
- <span data-ttu-id="26f47-111">Die Netzwerkverbindung wurde anscheinend unterbrochen. Klicken Sie auf 'Wiederholen', um es erneut zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="26f47-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="26f47-112">**Rote Markierung**</span><span class="sxs-lookup"><span data-stu-id="26f47-112">**Red flag**</span></span>

<span data-ttu-id="26f47-113">Dieses Problem tritt häufig auf, wenn Benutzer sich in der Implementierungsphase befinden, nachdem sie Informationen über Produktions- und Testumgebungen hinweg verglichen haben und dabei vergessen, dass sie sich zwischen Sitzungen hin- und herbewegen.</span><span class="sxs-lookup"><span data-stu-id="26f47-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="26f47-114">Wenn Benutzer in dieser Phase sind, erfahren sie höchstwahrscheinlich dieses Problem.</span><span class="sxs-lookup"><span data-stu-id="26f47-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="26f47-115">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="26f47-115">**Issue**</span></span> 

<span data-ttu-id="26f47-116">**Browsertypen:** Google Chrome, Internet Explorer und Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="26f47-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="26f47-117">Microsoft Dynamics 365 Human Resources trennt die Verbindung von Benutzern, wenn verschiedene Sitzungen gleichzeitig für denselben Benutzer und denselben Browsertyp geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="26f47-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="26f47-118">(Benutzer A zeigt beispielsweise sowohl Umgebung 1 als auch Umgebung 2 in Chrome an.) Es spielt keine Rolle, ob die Benutzer verschiedene Browserfenster oder Registerkarten öffnen.</span><span class="sxs-lookup"><span data-stu-id="26f47-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="26f47-119">Wenn dieselben Benutzeranmeldeinformationen verwendet werden, um sich sowohl in Umgebung 1 als auch in Umgebung 2 gleichzeitig und im selben Browsertyp anzumelden, trennt Human Resources die Verbindung für eine der Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="26f47-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="26f47-120">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="26f47-120">**Solution**</span></span>

<span data-ttu-id="26f47-121">Stellen Sie sicher, dass nur eine Umgebung gleichzeitig für einen bestimmten Browsertyp geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="26f47-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="26f47-122">Benutzer können mehrere Sitzungen für die gleiche Umgebung öffnen (das heißt, mehrere Registerkarten im selben Browser).</span><span class="sxs-lookup"><span data-stu-id="26f47-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="26f47-123">Benutzer, die zwischen zwei Umgebung gleichzeitig hin- und herwechseln möchten, sollten jede Umgebung in einem anderen Browsertyp öffnen.</span><span class="sxs-lookup"><span data-stu-id="26f47-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="26f47-124">(Beispielsweise kann Benutzer A Umgebung 1 in Chrome und Umgebung 2 in Microsoft Edge anzeigen.)</span><span class="sxs-lookup"><span data-stu-id="26f47-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
