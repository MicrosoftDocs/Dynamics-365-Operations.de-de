---
title: Zugriff auf private Informationen nach Sicherheitsrolle
description: In diesem Artikel wird erläutert, wie das Problem gelöst wird, wobei ein Kunde nicht auf Privatadressen zugreifen kann.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009170"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="c38a3-103">Zugriff auf private Adressen nach Sicherheitsrolle</span><span class="sxs-lookup"><span data-stu-id="c38a3-103">Access to private addresses by security role</span></span>

<span data-ttu-id="c38a3-104">**Abgang**</span><span class="sxs-lookup"><span data-stu-id="c38a3-104">**Issue**</span></span>

<span data-ttu-id="c38a3-105">Nachdem ein Kunde eine Sicherheitsrolle dupliziert und sich als diese neue Rolle anmeldet, kann der Kunde die Adressen, die als privat markiert wurden, nicht sehen.</span><span class="sxs-lookup"><span data-stu-id="c38a3-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="c38a3-106">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="c38a3-106">**Resolution**</span></span>

<span data-ttu-id="c38a3-107">Um das Problem zu beheben, muss der Kunde diese Schritte für die duplizierte Sicherheitsrolle befolgen.</span><span class="sxs-lookup"><span data-stu-id="c38a3-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="c38a3-108">Wechseln Sie zu **Organisationsverwaltung \> Globales Adressbuch \> Parameter für das globale Adressbuch**.</span><span class="sxs-lookup"><span data-stu-id="c38a3-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="c38a3-109">Auf der Registerkarte **Sicherheit für private Standorte** verschieben Sie die neue Sicherheitsrolle von der Liste **Verfügbare Rollen** in die Liste **Ausgewählte Rollen**.</span><span class="sxs-lookup"><span data-stu-id="c38a3-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="c38a3-110">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c38a3-110">Select **Save**.</span></span>

![Seite „Parameter des globalen Adressbuchs”](media/GAD-parameters.png)
