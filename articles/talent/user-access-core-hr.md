---
title: Benutzer kann auf Core HR, aber nicht auf Onboard oder Attract zugreifen
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 Talent – Core HR, aber nicht auf die Attract- und Onboard-App zugreifen kann.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009305"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="b7cf7-103">Benutzer kann auf Core HR, aber nicht auf Onboard oder Attract zugreifen</span><span class="sxs-lookup"><span data-stu-id="b7cf7-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7cf7-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="b7cf7-104">**Environment details**</span></span>

- <span data-ttu-id="b7cf7-105">Die Microsoft Dynamics Lifecycle Services (LCS)-Bereitstellung wurde von Benutzer A ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="b7cf7-106">Benutzer A hat Benutzer B als Benutzer zu Microsoft Dynamics 365 Talent: Core HR hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="b7cf7-107">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="b7cf7-107">**Issue**</span></span>

<span data-ttu-id="b7cf7-108">Benutzer B kann auf Core HR, aber nicht auf Talent zugreifen: Attract oder Talent: Onboard-App.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="b7cf7-109">Wenn der Benutzer versucht, zu **Erfahrungs-Apps** zu wechseln, wird er oder sie zu einer stattdessen zu einer Testumgebung geführt.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="b7cf7-110">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="b7cf7-110">**Solution**</span></span>

<span data-ttu-id="b7cf7-111">Benutzer B müssen die Rechte zugewiesen werden, um die Microsoft PowerApps-Umgebung anzuzeigen, die Benutzer A während des Bereitstellungsprozesses erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="b7cf7-112">Informationen dazu finden Sie im Abschnitt „Zugriff auf die Umgebung gewähren” in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="b7cf7-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="b7cf7-113">**Langfristige Lösung**</span><span class="sxs-lookup"><span data-stu-id="b7cf7-113">**Long-term solution**</span></span>

<span data-ttu-id="b7cf7-114">Microsoft erwägt, die entsprechenden Rechte automatisch an Onboard oder Attact zuzuweisen, wenn ein Benutzer zu Core HR hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7cf7-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
