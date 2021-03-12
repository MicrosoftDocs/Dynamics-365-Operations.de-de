---
title: Stornieren von Lagerortarbeit für Ausnahmebehandlung
description: In diesem Thema wird die Funktion zum Stornieren von Arbeit beschrieben, mit der Vorgesetzte am Lagerort gesperrte Arbeit verarbeiten können.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ae4062401cd5be2371c45642b78bf3708b04f664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001197"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="2c8af-103">Stornieren von Lagerortarbeit für Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="2c8af-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c8af-104">Mit der Funktion zum Stornieren von Arbeit in Microsoft Dynamics 365 Supply Chain Management können Administratorbenutzer bestimmte Lagerortarbeit stornieren, die derzeit ausgeführt, aber vom System gesperrt wird oder aufgrund außergewöhnlicher Umstände nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c8af-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="2c8af-105">Diese Funktion ist eine attraktive und sichere Alternative zu korrektiven SQL-Skripts, die inkonsistente Daten beheben.</span><span class="sxs-lookup"><span data-stu-id="2c8af-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="2c8af-106">Während diese Skripts jedoch normalerweise von IT-Profis angefordert werden, kann die Funktion zum Stornieren von Arbeit von Benutzern im Unternehmen verwendet werden, die Administratorrechte haben.</span><span class="sxs-lookup"><span data-stu-id="2c8af-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="2c8af-107">Sie können auf die Funktion zum Stornieren von Arbeit unter **Lagerortverwaltung** \> **Periodische Aufgaben** \> **Bereinigen \> Arbeit stornieren** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2c8af-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="2c8af-108">Geben Sie im Dialogfeld **Arbeit stornieren** die Arbeitskennung der zu stornierenden Arbeit an, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="2c8af-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="2c8af-109">Lagerortarbeit, die storniert werden kann</span><span class="sxs-lookup"><span data-stu-id="2c8af-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="2c8af-110">Während des Lagerortentnahmebetriebs kann es sein, dass eine Arbeitskraft in der Situation ist, dass er Mengen erfasst hat wie von einem Lagerort zu ihrem Benutzerlagerplatz entnommen, aber den Einlagerungsvorgang nicht erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="2c8af-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="2c8af-111">Inkonsistente Lagerortdaten sind häufig, allerdings nicht immer, der Grund, warum Arbeit gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="2c8af-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="2c8af-112">Im Gegensatz zur regulären Stornieren-Funktion, auf die Sie zugreifen können, indem Sie die Schaltfläche **Abbrechen** auf dem Arbeitskopf verwenden, erfordert die Funktion zum Stornieren von Arbeit nicht, dass die letzte abgeschlossene Arbeitsposition eine Arbeitsposition vom Typ **Einlagern** ist.</span><span class="sxs-lookup"><span data-stu-id="2c8af-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="2c8af-113">Das bedeutet, dass die Stornierungslogik für die Funktion zum Stornieren von Arbeit selbst dann ausgeführt werden kann, wenn die Artikelmenge in einer Arbeitsposition in einem Benutzerlagerplatz ist.</span><span class="sxs-lookup"><span data-stu-id="2c8af-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="2c8af-114">Für Arbeit, die aus betrieblichen Ursachen storniert werden muss, müssen Lagerortbenutzer weiterhin die reguläre Stornieren-Funktion auf der Arbeitsseite verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c8af-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="2c8af-115">Nur Arbeit vom Typ **Vertrieb**, **Umlagerungsprobleme**, **Rohmaterialentnahme** oder **Wiederbeschaffung** kann mit Hilfe der Funktion zum Stornieren von Arbeit storniert werden.</span><span class="sxs-lookup"><span data-stu-id="2c8af-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="2c8af-116">Die Stornierungslogik wird nicht für gesperrte Rohmaterialentnahmearbeit oder Arbeit ausgeführt, die mit Hilfe der Funktion zum Stornieren von Arbeit storniert werden kann (siehe den vorhergehenden Hinweis).</span><span class="sxs-lookup"><span data-stu-id="2c8af-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="2c8af-117">Um die Sperrung der Arbeit aufzuheben, storniert das System alle verbleibenden Arbeitspositionen und korrigiert die Lagerortdaten, die der Arbeitskennung zugeordnet sind, die der Benutzer angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="2c8af-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="2c8af-118">Alle regulären Lagerortverarbeitungsvorgänge, die die betroffene Artikelmenge umfassen, können dann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="2c8af-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="2c8af-119">Um den betroffenen Artikel in einen bestimmten Lagerplatz einzulagern, nachdem die Arbeit storniert wurde, muss der Benutzer einen Bestandsumlagerungs- oder Mengenanpassungseinstellvorgang auf einem mobilen Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c8af-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
