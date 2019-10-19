---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (16. Oktober 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 13e89faa3f8470125010ccdb40a6f01c0a9c4fe7
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008776"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-19-2018"></a><span data-ttu-id="d7aca-103">Neuerungen oder Änderungen in Dynamics 365 Talent: Core HR (19. Oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="d7aca-103">What's new or changed in Dynamics 365 Talent: Core HR (October 19, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="d7aca-104">**Build 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="d7aca-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="d7aca-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="d7aca-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="d7aca-106">Managern erlauben, Freizeitanforderungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d7aca-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="d7aca-107">Freizeitanforderungen von Mitarbeitern müssen möglicherweise aktualisiert werden, nachdem sie über den Workflow genehmigt sind.</span><span class="sxs-lookup"><span data-stu-id="d7aca-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="d7aca-108">In vielen Fällen kann der Manager diese Aktualisierungen im Auftrag des Mitarbeiters machen.</span><span class="sxs-lookup"><span data-stu-id="d7aca-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="d7aca-109">Diese neue Funktion bietet Managern die Möglichkeit, Freizeitanforderungen im Auftrag der Mitarbeiter zu aktualisieren oder zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="d7aca-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="d7aca-110">Diese Funktion wird vom Parameter **Arbeit im Auftrag** gesteuert, der auf der Seite **Personalverwaltungs-Parameter** aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d7aca-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="d7aca-111">HR erlauben, Freizeitanforderungen zu aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d7aca-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="d7aca-112">Ähnlich der Funktion zuvor, müssen möglicherweise Mitarbeiterfreizeitanforderungen von HR aktualisiert werden, nachdem sie bereits über den Workflow genehmigt wurden.</span><span class="sxs-lookup"><span data-stu-id="d7aca-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="d7aca-113">Diese Funktion bietet die Möglichkeit für HR-Nutzer, Freizeitanforderungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d7aca-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="d7aca-114">Die Funktion ist im Arbeitsbereich **Personen** auf der Seite **Arbeitskraft** aktiviert, und zwar mithilfe eine neue Option **Ansichtsfreizeit**.</span><span class="sxs-lookup"><span data-stu-id="d7aca-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="d7aca-115">Auf diesen Seiten können Personalverwaltungsbenutzer Freizeitanforderungstransaktionen anzeigen und aktualisieren, ähnlich wie Manager diese Aktivitäten ausführen können.</span><span class="sxs-lookup"><span data-stu-id="d7aca-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="d7aca-116">Die Sicherheitsberechtigung, die Zugriff auf diese Funktionen steuert, ist:</span><span class="sxs-lookup"><span data-stu-id="d7aca-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="d7aca-117">Auftrag: Arbeitskraftspezifische Urlaubs- und Abwesenheitsprozesse verwalten.</span><span class="sxs-lookup"><span data-stu-id="d7aca-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="d7aca-118">Recht: Urlaubs- und Abwesenheitsanforderungen für alle Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="d7aca-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="d7aca-119">Andere Änderungen</span><span class="sxs-lookup"><span data-stu-id="d7aca-119">Other changes</span></span>
<span data-ttu-id="d7aca-120">Folgende Aktualisierungen sind in dieser Version erfolgt:</span><span class="sxs-lookup"><span data-stu-id="d7aca-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="d7aca-121">Änderungen an Arbeitseinstellungsaktivitäten, sodass sie nicht mehr im Status **Workflow abgeschlossen** sind.</span><span class="sxs-lookup"><span data-stu-id="d7aca-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="d7aca-122">Beschäftigungszahl kann nun ohne Beschäftigung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d7aca-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="d7aca-123">Das Registrierungsdatum für Dynamics 365 Talent für einen Kurs, der im Mitarbeiter-Self-Service angezeigt wird, wendet nun den Zeitzonenunterschied im Datum an.</span><span class="sxs-lookup"><span data-stu-id="d7aca-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="d7aca-124">Excel-Dateien können mehrmals ohne gefundene Fehler mithilfe von  **Mitarbeiter-Entität** importiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7aca-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="d7aca-125">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="d7aca-125">Known issue</span></span>

- <span data-ttu-id="d7aca-126">**Abgang**: Wenn sie einer Arbeitskraft einen neuen Anhang hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** ausgegraut.</span><span class="sxs-lookup"><span data-stu-id="d7aca-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="d7aca-127">**Problemumgehung:**, Bevor die Anhangseite geöffnet wird, stellen Sie sicher, dass die Infoboxen auf der Seite **Arbeitskraft** geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="d7aca-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="d7aca-128">Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d7aca-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="d7aca-129">(Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)</span><span class="sxs-lookup"><span data-stu-id="d7aca-129">(This issue will be fixed in the next platform update.)</span></span>
