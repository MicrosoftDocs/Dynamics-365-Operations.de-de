---
title: "Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (15. November 2018)"
description: "In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a><span data-ttu-id="83326-103">Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (15. November 2018)</span><span class="sxs-lookup"><span data-stu-id="83326-103">What's new or changed in Dynamics 365 for Talent Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83326-104">**Build 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="83326-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="83326-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="83326-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="83326-106">Andere Änderungen/Korrekturen</span><span class="sxs-lookup"><span data-stu-id="83326-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="83326-107">Aktuelle Position des Mitarbeiters kann nicht zu einer zukünftigen offenen Position geändert werden</span><span class="sxs-lookup"><span data-stu-id="83326-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="83326-108">Eine Änderung ist vorgenommen worden, um Positionsübertragungen zu ermöglichen, wenn die Position erst in der Zukunft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="83326-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="83326-109">Position wird nicht angezeigt, wenn ein neuer Mitarbeiter erstellt wird</span><span class="sxs-lookup"><span data-stu-id="83326-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="83326-110">Eine Änderung ist vorgenommen worden, um alle offenen Positionen anzuzeigen, die für die Zuweisung zur Verfügung stehen, wenn neue Mitarbeiter in Talent eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="83326-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="83326-111">Hierzu zählen historische Positionen oder wenn die Positionen in die Zukunft vordatiert wurden.</span><span class="sxs-lookup"><span data-stu-id="83326-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="83326-112">Positionen werden jetzt korrekt basierend auf dem Beschäftigungsstartdatum angezeigt.</span><span class="sxs-lookup"><span data-stu-id="83326-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="83326-113">Kündigungsdatum wird basierend auf den Benutzereinstellungen angezeigt</span><span class="sxs-lookup"><span data-stu-id="83326-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="83326-114">Eine Änderung ist an der Liste früherer Mitarbeiter vorgenommen worden, um sämtliche Zeitzonenabweichungen für die bevorzugte Zeitzone der Mitarbeiter zu berücksichtigen, wenn das Kündigungsdatum angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83326-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="83326-115">Links für mir zugewiesene Arbeitsaufgaben zeigen nicht die richtigen Informationen an</span><span class="sxs-lookup"><span data-stu-id="83326-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="83326-116">Mit dieser Änderung wird die Navigation zu den Details der einzelnen Arbeitsaufgaben in der Liste die richtigen Informationen für die ausgewählte Aufgabe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="83326-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="83326-117">Dieses Problem ist nur bei erweiterten Sicherheitsoptionen aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="83326-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="83326-118">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="83326-118">Known issue</span></span>

- <span data-ttu-id="83326-119">**Abgang**: Wenn sie einer Arbeitskraft einen neuen Anhang hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** ausgegraut.</span><span class="sxs-lookup"><span data-stu-id="83326-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="83326-120">**Problemumgehung:**, Bevor die Anhangseite geöffnet wird, stellen Sie sicher, dass die Infoboxen auf der Seite **Arbeitskraft** geschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="83326-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="83326-121">Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="83326-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="83326-122">(Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)</span><span class="sxs-lookup"><span data-stu-id="83326-122">(This issue will be fixed in the next platform update.)</span></span>
