---
title: Sie können eine Sendung nicht bestätigen, weil es ein Problem mit dem Kalender gibt
description: Sie können eine Sendung nicht bestätigen, weil es ein Problem mit dem Kalender gibt
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938478"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="a972e-103">Sie können eine Sendung nicht bestätigen, weil es ein Problem mit dem Kalender gibt</span><span class="sxs-lookup"><span data-stu-id="a972e-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="a972e-104">Fehlercode: TRX2716</span><span class="sxs-lookup"><span data-stu-id="a972e-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="a972e-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="a972e-105">Symptoms</span></span>

<span data-ttu-id="a972e-106">Wenn Sie versuchen, eine Sendung zu bestätigen, zeigt das System die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="a972e-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="a972e-107">Der Kalendertyp %1 erfordert, dass der Termin %2 ein- und ausgecheckt wird.</span><span class="sxs-lookup"><span data-stu-id="a972e-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="a972e-108">Daher können Sie die Sendung für die Ladung nicht bestätigen.</span><span class="sxs-lookup"><span data-stu-id="a972e-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="a972e-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="a972e-109">Cause</span></span>

<span data-ttu-id="a972e-110">Aktive Termine für die Ladung sind vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a972e-110">Active appointments for the load exist.</span></span> <span data-ttu-id="a972e-111">Zum Beispiel gibt es eine Regel, die das Einchecken von Fahrern erfordert.</span><span class="sxs-lookup"><span data-stu-id="a972e-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="a972e-112">Daher befindet sich die Ladung derzeit in einem Status, in dem die Versandbestätigung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a972e-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="a972e-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="a972e-113">Resolution</span></span>

<span data-ttu-id="a972e-114">Sie müssen alle Probleme mit den aktiven Terminen, die mit der Ladung verbunden sind, untersuchen und beheben.</span><span class="sxs-lookup"><span data-stu-id="a972e-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="a972e-115">Gehen Sie zu **Lagerortverwaltung \> Ladungen \> Alle Ladungen**.</span><span class="sxs-lookup"><span data-stu-id="a972e-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="a972e-116">Wählen Sie die Ladung, für die die Sendung nicht bestätigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a972e-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="a972e-117">Wählen Sie im Aktivitätsbereich auf der Registerkarte **Transporte** in der Gruppe **Termine** den Eintrag **Terminplanung**.</span><span class="sxs-lookup"><span data-stu-id="a972e-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="a972e-118">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="a972e-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="a972e-119">Stellen Sie sicher, dass das Ein- und Auschecken des Fahrers für den Termin abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a972e-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="a972e-120">Vervollständigen oder stornieren Sie den Termin.</span><span class="sxs-lookup"><span data-stu-id="a972e-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="a972e-121">Deaktivieren Sie die Option **Fahrer Check-In erforderlich** für die zugehörige Terminregel.</span><span class="sxs-lookup"><span data-stu-id="a972e-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
