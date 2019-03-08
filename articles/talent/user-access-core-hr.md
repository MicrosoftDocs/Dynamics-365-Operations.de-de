---
title: Benutzer kann auf Core HR, aber nicht auf die Onboard- oder Attract-App zugreifen
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 for Talent Core HR, aber nicht auf die Attract- und Onboard-App zugreifen kann.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304562"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="a7e14-103">Benutzer kann auf Core HR, aber nicht auf die Onboard- oder Attract-Anwendung zugreifen</span><span class="sxs-lookup"><span data-stu-id="a7e14-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7e14-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="a7e14-104">**Environment details**</span></span>

- <span data-ttu-id="a7e14-105">Die Microsoft Dynamics Lifecycle Services (LCS)-Bereitstellung wurde von Benutzer A ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e14-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="a7e14-106">Benutzer A hat Benutzer B als Benutzer zu Microsoft Dynamics 365 for Talent Core HR hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a7e14-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="a7e14-107">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="a7e14-107">**Issue**</span></span>

<span data-ttu-id="a7e14-108">Benutzer B kann auf Core HR, aber nicht auf Talent zugreifen: Attract oder Talent: Onboard-App.</span><span class="sxs-lookup"><span data-stu-id="a7e14-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="a7e14-109">Wenn der Benutzer versucht, zu **Erfahrungs-Apps** zu wechseln, wird er oder sie zu einer stattdessen zu einer Testumgebung geführt.</span><span class="sxs-lookup"><span data-stu-id="a7e14-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="a7e14-110">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="a7e14-110">**Solution**</span></span>

<span data-ttu-id="a7e14-111">Benutzer B müssen die Rechte zugewiesen werden, um die Microsoft PowerApps-Umgebung anzuzeigen, die Benutzer A während des Bereitstellungsprozesses erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="a7e14-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="a7e14-112">Informationen dazu finden Sie im Abschnitt „Zugriff auf die Umgebung gewähren” in [Talent bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="a7e14-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="a7e14-113">**Langfristige Lösung**</span><span class="sxs-lookup"><span data-stu-id="a7e14-113">**Long-term solution**</span></span>

<span data-ttu-id="a7e14-114">Microsoft erwägt, die entsprechenden Rechte automatisch an Onboard oder Attact zuzuweisen, wenn ein Benutzer zu Core HR hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a7e14-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
