---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (14. Februar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "859389"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="d61d8-103">Neuerungen oder Änderungen in Dynamics 365 for Talent (14. Februar 2019)</span><span class="sxs-lookup"><span data-stu-id="d61d8-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d61d8-104">In diesem Thema werden die Funktionen beschrieben, die in Talent entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="d61d8-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="d61d8-105">Änderungen in Attract</span><span class="sxs-lookup"><span data-stu-id="d61d8-105">Changes in Attract</span></span>
<span data-ttu-id="d61d8-106">Es gibt kleinere Fehlerkorrekturen in dieser Version.</span><span class="sxs-lookup"><span data-stu-id="d61d8-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="d61d8-107">Änderungen in Onboarding</span><span class="sxs-lookup"><span data-stu-id="d61d8-107">Changes in Onboarding</span></span>
<span data-ttu-id="d61d8-108">Es gibt kleinere Fehlerkorrekturen in dieser Version.</span><span class="sxs-lookup"><span data-stu-id="d61d8-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="d61d8-109">Core HR-Änderungen</span><span class="sxs-lookup"><span data-stu-id="d61d8-109">Changes in Core HR</span></span> 
<span data-ttu-id="d61d8-110">**Build 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="d61d8-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="d61d8-111">Die Entität für feste Mitarbeitervergütung exportiert nicht alle Datensätze</span><span class="sxs-lookup"><span data-stu-id="d61d8-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="d61d8-112">Mit dieser Änderung exportiert die Entität **Feste Mitarbeitervergütung** nun alle Datensätze.</span><span class="sxs-lookup"><span data-stu-id="d61d8-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="d61d8-113">Die Entität kann verwendet werden, um vorhandene Datensätze mit fester Vergütung für Mitarbeiter zu erstellen und zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d61d8-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="d61d8-114">Das Enddatum der Beschäftigung berücksichtigt keine bevorzugten Zeitzoneneinstellungen für Mitarbeiter</span><span class="sxs-lookup"><span data-stu-id="d61d8-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="d61d8-115">Das Enddatum der Beschäftigung berücksichtigt nun bevorzugte Zeitzonen von Mitarbeitern beim Erstellen oder Beenden einer Beschäftigung.</span><span class="sxs-lookup"><span data-stu-id="d61d8-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="d61d8-116">Adressenanzeige für das Vereinigte Königreich in Analytics als Adressen der Ost-Schweiz angezeigt</span><span class="sxs-lookup"><span data-stu-id="d61d8-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="d61d8-117">In dieser Version wurde eine Änderung vorgenommen, um falsche Adressen in der **Personalführung** im Bericht „Mitarbeiterzahl nach Abteilung“ zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="d61d8-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="d61d8-118">Kündigungscode wird im Arbeitskraftpositions-Zuweisungsdatensatz nicht ausgefüllt, wenn die Position beendet wird</span><span class="sxs-lookup"><span data-stu-id="d61d8-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="d61d8-119">Eine Änderung am Standardcode für den Kündigungsgrund wurde vorgenommen, wenn die Mitarbeiterpositionszuweisung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d61d8-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="d61d8-120">Neue Entität für Stellenvergütungsstufen erstellt</span><span class="sxs-lookup"><span data-stu-id="d61d8-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="d61d8-121">Eine neue Datenverwaltungsframework (DMF)-Entität wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="d61d8-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="d61d8-122">Die Entität stellt Erstellung und Aktualisierungen der Vergütungsstufen, Marktwerte und Umfrageinformationen zu den im System definierten Stellen bereit.</span><span class="sxs-lookup"><span data-stu-id="d61d8-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
