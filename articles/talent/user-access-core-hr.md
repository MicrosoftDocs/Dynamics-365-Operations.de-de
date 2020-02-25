---
title: Benutzer kann auf Personalverwaltung aber nicht auf Onboard oder Attract zugreifen
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 Talent – Personalverwaltung aber nicht auf Attract oder Onboard zugreifen kann.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006309"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="d72c3-103">Benutzer kann auf Personalverwaltung aber nicht auf Onboard oder Attract zugreifen</span><span class="sxs-lookup"><span data-stu-id="d72c3-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d72c3-104">**Umgebungsdetails**</span><span class="sxs-lookup"><span data-stu-id="d72c3-104">**Environment details**</span></span>

- <span data-ttu-id="d72c3-105">Die Microsoft Dynamics Lifecycle Services (LCS)-Bereitstellung wurde von Benutzer A ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d72c3-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="d72c3-106">Benutzer A hat Benutzer B als Benutzer zu Microsoft Dynamics 365 Human Resources hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d72c3-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d72c3-107">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="d72c3-107">**Issue**</span></span>

<span data-ttu-id="d72c3-108">Benutzer B kann auf Personalverwaltung aber nicht auf Talent zugreifen: Attract- oder Talent: Onboard-App.</span><span class="sxs-lookup"><span data-stu-id="d72c3-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="d72c3-109">Wenn der Benutzer versucht, zu **Erfahrungs-Apps** zu wechseln, wird er oder sie zu einer stattdessen zu einer Testumgebung geführt.</span><span class="sxs-lookup"><span data-stu-id="d72c3-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="d72c3-110">**Lösung**</span><span class="sxs-lookup"><span data-stu-id="d72c3-110">**Solution**</span></span>

<span data-ttu-id="d72c3-111">Benutzer B müssen die Rechte zugewiesen werden, um die Microsoft Power Apps-Umgebung anzuzeigen, die Benutzer A während des Bereitstellungsprozesses erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="d72c3-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="d72c3-112">Informationen dazu finden Sie im Abschnitt „Zugriff auf die Umgebung gewähren” in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="d72c3-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="d72c3-113">**Langfristige Lösung**</span><span class="sxs-lookup"><span data-stu-id="d72c3-113">**Long-term solution**</span></span>

<span data-ttu-id="d72c3-114">Microsoft erwägt, die entsprechenden Rechte automatisch an Onboard oder Attact zuzuweisen, wenn ein Benutzer zu Personalverwaltung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="d72c3-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
