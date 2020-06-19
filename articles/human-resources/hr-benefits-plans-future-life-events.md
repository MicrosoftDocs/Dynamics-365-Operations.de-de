---
title: Zukünftige Lebensereignisse konfigurieren
description: Sie können in Dynamics 365 Human Resources zukünftige Lebensereignisse planen.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78c65faa4ae0f428184700a912998e9dded026c5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429404"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="e540c-103">Zukünftige Lebensereignisse konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e540c-103">Configure future life events</span></span>

<span data-ttu-id="e540c-104">Sie können in Dynamics 365 Human Resources zukünftige Lebensereignisse planen.</span><span class="sxs-lookup"><span data-stu-id="e540c-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="e540c-105">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Zukünftige Lebensereignisse**.</span><span class="sxs-lookup"><span data-stu-id="e540c-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="e540c-106">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e540c-106">Select **New**.</span></span>

3. <span data-ttu-id="e540c-107">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="e540c-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e540c-108">Feld</span><span class="sxs-lookup"><span data-stu-id="e540c-108">Field</span></span> | <span data-ttu-id="e540c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e540c-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e540c-110">Datum des Lebensereignisses</span><span class="sxs-lookup"><span data-stu-id="e540c-110">Life event date</span></span> | <span data-ttu-id="e540c-111">Das System verarbeitet alle Ereignisse während der Registrierungsperiode, die bis zu diesem Datum auftreten.</span><span class="sxs-lookup"><span data-stu-id="e540c-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="e540c-112">Lebensereignis protokolliert</span><span class="sxs-lookup"><span data-stu-id="e540c-112">Life event logged</span></span> | <span data-ttu-id="e540c-113">Datum und Uhrzeit, zu denen das Lebensereignis protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="e540c-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="e540c-114">Protokolltyp</span><span class="sxs-lookup"><span data-stu-id="e540c-114">Log type</span></span> | <span data-ttu-id="e540c-115">Zeigt an, ob die Aktivität einem der folgenden Werte entspricht:</span><span class="sxs-lookup"><span data-stu-id="e540c-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="e540c-116">- **Aktualisieren** – Änderung an einem vorhandenen Datensatz, in dem Lebensereignisse aufgezeichnet werden</span><span class="sxs-lookup"><span data-stu-id="e540c-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="e540c-117">- **Einfügen** – Erstellung eines neuen Lebensereignisdatensatzes</span><span class="sxs-lookup"><span data-stu-id="e540c-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="e540c-118">Kennung des Lebensereignistyps</span><span class="sxs-lookup"><span data-stu-id="e540c-118">Life event type ID</span></span> | <span data-ttu-id="e540c-119">Der eindeutige Bezeichner für den Lebensereignistyp.</span><span class="sxs-lookup"><span data-stu-id="e540c-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="e540c-120">Lebensereignistyp</span><span class="sxs-lookup"><span data-stu-id="e540c-120">Life event type</span></span> | <span data-ttu-id="e540c-121">Ein Katalysator für die Aktualisierung der Vorteilsregistrierung eines Mitarbeiters.</span><span class="sxs-lookup"><span data-stu-id="e540c-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="e540c-122">Weitere Informationen finden Sie im Abschnitt „Auslöser für Lebensereignisse“.</span><span class="sxs-lookup"><span data-stu-id="e540c-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="e540c-123">Status</span><span class="sxs-lookup"><span data-stu-id="e540c-123">Status</span></span> | <span data-ttu-id="e540c-124">Gibt an, ob das Lebensereignis verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e540c-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="e540c-125">Position</span><span class="sxs-lookup"><span data-stu-id="e540c-125">Line</span></span> | <span data-ttu-id="e540c-126">Die Positionsnummer des zukünftigen Lebensereignisses.</span><span class="sxs-lookup"><span data-stu-id="e540c-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="e540c-127">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="e540c-127">Select **Save**.</span></span> 
