---
title: Massen-Finanzperiodenabschluss
description: Dieses Verfahren zeigt, wie eine Periode als "Gesperrt" oder "Permanent geschlossen" oder für mehrere juristische Person auf einmal festgelegt wird.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "311380"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="ff929-103">Massen-Finanzperiodenabschluss</span><span class="sxs-lookup"><span data-stu-id="ff929-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff929-104">Dieses Verfahren zeigt, wie eine Periode als "Gesperrt" oder "Permanent geschlossen" oder für mehrere juristische Person auf einmal festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ff929-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="ff929-105">Darüber hinaus zeigt die Aufgabe, wie die Benutzergruppenbuchun auf bestimmte Module beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="ff929-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="ff929-106">Wechseln Sie zu Hauptbuch > Zeitraum geschlossen > Hauptbuch.</span><span class="sxs-lookup"><span data-stu-id="ff929-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="ff929-107">Beachten Sie, dass die Liste der angezeigten juristischen Personen vom auf der Seite ausgewählten Steuerkalender abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="ff929-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="ff929-108">Nur juristischen Personen, die den ausgewählten Steuerkalender verwenden, werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ff929-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="ff929-109">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="ff929-109">Click Edit.</span></span>
3. <span data-ttu-id="ff929-110">Wählen Sie den Zeitraum aus, für den Sie den Status ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="ff929-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="ff929-111">Wählen Sie die juristischen Personen aus, für den Sie den Status aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ff929-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="ff929-112">Sie können schnell alle juristischen Personen auswählen, indem Sie das Kontrollkästchen in der oberen linken Seite des Formulars auswählen.</span><span class="sxs-lookup"><span data-stu-id="ff929-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="ff929-113">Wählen Sie "Modulzugriff aktualisieren" aus, um den Buchungszugriff mit einem bestimmten Modul zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ff929-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="ff929-114">Der Modulstatus kann auch einzeln aktualisiert werden, indem die Datensätze des Rasters bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ff929-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="ff929-115">Die Schaltfläche ist hilfreich, wenn Sie mehrere Datensätze der juristischen Person schnell aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ff929-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="ff929-116">Wählen Sie im Feld Anwendungsmodul das Modul aus, für das Sie den Status aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ff929-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="ff929-117">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="ff929-117">Click Select.</span></span>
7. <span data-ttu-id="ff929-118">Wählen Sie in Zugriffsebene aus Alle, Keine oder eine bestimmte Benutzergruppe aus.</span><span class="sxs-lookup"><span data-stu-id="ff929-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="ff929-119">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="ff929-119">Click Select.</span></span>
    * <span data-ttu-id="ff929-120">"Alle" legt fest, dass alle Benutzer mit Bearbeitungszugriff auf das Modul buchen können wenn die Periode offen ist.</span><span class="sxs-lookup"><span data-stu-id="ff929-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="ff929-121">"Keine" legt fest, dass Benutzer nicht im Modul buchen können, wenn die Periode offen ist.</span><span class="sxs-lookup"><span data-stu-id="ff929-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="ff929-122">Eine bestimmte Benutzergruppe gibt an, das nur Benutzer der Gruppe im Modul buchen dürfen, wenn die Periode geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="ff929-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="ff929-123">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ff929-123">Click Update.</span></span>
9. <span data-ttu-id="ff929-124">Wählen Sie eine andere Periode aus, um den Status zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ff929-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="ff929-125">Wählen Sie die juristischen Personen aus, für den Sie die Periode aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ff929-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="ff929-126">Wählen Sie "Periodenstatus Aktualisierung" aus und legen Sie den Status auf "Gesperrt", "Offen" oder "Permanent geschlossen" fest.</span><span class="sxs-lookup"><span data-stu-id="ff929-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="ff929-127">"Offen" legt fest, das für die Periode gebucht werden kann, vorausgesetzt der Benutzer hat Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ff929-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="ff929-128">"Gesperrt" bedeutet, dass nicht in den Zeitraum gebucht werden kann, aber der Zeitraum erneut geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff929-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="ff929-129">"Permanent geschlossen" bedeutet, das der Zeitraum abgeschlossen ist und nicht geöffnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff929-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="ff929-130">Regulierungen können nicht gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ff929-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="ff929-131">Wir empfehlen nicht, einen Zeitraum auf "Permanent geschlossen" festzulegen, bis alle Anpassungen und Audits abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="ff929-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="ff929-132">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ff929-132">Click Update.</span></span>

