---
title: Zugriff auf private Adressen nach Sicherheitsrolle
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wobei ein Kunde nicht auf Privatadressen zugreifen kann.
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
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897096"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="cb060-103">Zugriff auf private Adressen nach Sicherheitsrolle</span><span class="sxs-lookup"><span data-stu-id="cb060-103">Access to private addresses by security role</span></span>

<span data-ttu-id="cb060-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="cb060-104">**Issue**</span></span>

<span data-ttu-id="cb060-105">Nachdem ein Kunde eine Sicherheitsrolle dupliziert und sich als diese neue Rolle anmeldet, kann der Kunde die Adressen, die als privat markiert wurden, nicht sehen.</span><span class="sxs-lookup"><span data-stu-id="cb060-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="cb060-106">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="cb060-106">**Resolution**</span></span>

<span data-ttu-id="cb060-107">Um das Problem zu beheben, muss der Kunde diese Schritte für die duplizierte Sicherheitsrolle befolgen.</span><span class="sxs-lookup"><span data-stu-id="cb060-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="cb060-108">Wechseln Sie zu **Organisationsverwaltung \> Globales Adressbuch \> Parameter für das globale Adressbuch**.</span><span class="sxs-lookup"><span data-stu-id="cb060-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="cb060-109">Auf der Registerkarte **Sicherheit für private Standorte** verschieben Sie die neue Sicherheitsrolle von der Liste **Verfügbare Rollen** in die Liste **Ausgewählte Rollen**.</span><span class="sxs-lookup"><span data-stu-id="cb060-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="cb060-110">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="cb060-110">Select **Save**.</span></span>

![Seite „Parameter des globalen Adressbuchs”](media/GAD-parameters.png)
