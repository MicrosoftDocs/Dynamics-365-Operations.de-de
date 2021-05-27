---
title: Systemadministratoren können Auftragssperren nicht löschen, da sie nicht dazu autorisiert sind
description: Systemadministratoren können Auftragssperren nicht löschen, da sie nicht dazu autorisiert sind.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026558"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="43f8e-103">Systemadministratoren können Auftragssperren nicht löschen, da sie nicht dazu autorisiert sind</span><span class="sxs-lookup"><span data-stu-id="43f8e-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="43f8e-104">KB-Nummer: 4614642</span><span class="sxs-lookup"><span data-stu-id="43f8e-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="43f8e-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="43f8e-105">Symptoms</span></span>

<span data-ttu-id="43f8e-106">Systemadministratoren können Auftragssperren nur löschen, wenn sie die spezifische Rolle haben, die im Auftragssperrcode zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="43f8e-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="43f8e-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="43f8e-107">Resolution</span></span>

<span data-ttu-id="43f8e-108">Der Zugriff auf manche Vorgänge, z. B. das Löschen von Auftragssperren, wird durch die Einrichtung einer Geschäftsrichtlinie gesteuert.</span><span class="sxs-lookup"><span data-stu-id="43f8e-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="43f8e-109">Systemadministratoren dürfen normalerweise keine Vorgänge dieses Typs ausführen.</span><span class="sxs-lookup"><span data-stu-id="43f8e-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="43f8e-110">Häufiger wird der Zugriff zur Ausführung einer bestimmten Aufgabe durch Geschäftsrichtlinien geregelt, und nur bestimmte Personen in einer Organisation sind zur Ausführung dieser Aufgabe berechtigt.</span><span class="sxs-lookup"><span data-stu-id="43f8e-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="43f8e-111">Beispiele hierfür sind Genehmigungen, die aus Workflow-Genehmigungen stammen, und bestimmte Aufgaben, die aus einer Workflow-Konfiguration stammen.</span><span class="sxs-lookup"><span data-stu-id="43f8e-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="43f8e-112">Obwohl mit Auftragssperren kein Workflow verbunden ist, ist das Prinzip ähnlich.</span><span class="sxs-lookup"><span data-stu-id="43f8e-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="43f8e-113">Eine relevante Rolle bezeichnet die spezifische Gruppe von Personen in einer Organisation, die das Recht haben, Auftragssperren zu löschen.</span><span class="sxs-lookup"><span data-stu-id="43f8e-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="43f8e-114">Dieses Recht sollte nicht unbedingt allen Administratoren gewährt werden, da dieser Ansatz gegen die festgelegte Geschäftsrichtlinie verstößt.</span><span class="sxs-lookup"><span data-stu-id="43f8e-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
