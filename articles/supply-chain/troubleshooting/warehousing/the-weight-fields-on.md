---
title: Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern auf der Ladung überein
description: Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern auf der Ladung überein
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924350"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="52390-103">Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern auf der Ladung überein</span><span class="sxs-lookup"><span data-stu-id="52390-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="52390-104">Fehlercodes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="52390-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="52390-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="52390-105">Symptoms</span></span>

<span data-ttu-id="52390-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="52390-106">The system shows the following error message:</span></span>

> <span data-ttu-id="52390-107">Die Gewichtsfelder auf den Zeilen der Ladung stimmen nicht mit den Gewichtsfeldern der Ladung %1 überein.</span><span class="sxs-lookup"><span data-stu-id="52390-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="52390-108">Führen Sie die Konsistenzprüfung für die Ladung des Lagers aus, um die Gewichtsfelder neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="52390-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="52390-109">Ursache</span><span class="sxs-lookup"><span data-stu-id="52390-109">Cause</span></span>

<span data-ttu-id="52390-110">Die Felder **Nettogewicht** und **Tara-Gewicht** werden in der Zeile der Ladung auf *0* (Null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52390-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="52390-111">Die Gewichtsfelder sind jedoch nicht auf *0* für die Messungen des Gewichts auf dem Produkt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52390-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="52390-112">Wenn die Gewichtsfelder in der Zeile der Ladung nicht festgelegt sind, können Korrekturen der Menge in der Zeile der Ladung zu einer falschen Gewichtsberechnung der Ladung führen.</span><span class="sxs-lookup"><span data-stu-id="52390-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="52390-113">Dieses Problem kann auftreten, wenn die Gewichte auf dem Produkt geändert wurden, seit die Zeile für die Ladung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="52390-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="52390-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="52390-114">Resolution</span></span>

<span data-ttu-id="52390-115">Standardmäßig werden beim Erstellen einer Ladungs-Zeile die Gewichtsfelder aus dem Produkt darauf eingetragen.</span><span class="sxs-lookup"><span data-stu-id="52390-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="52390-116">Wenn das Gewicht Null ist, können Sie es mit Hilfe der Funktionalität *Konsistenzprüfung des Gewichts der Lagerorte* neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="52390-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="52390-117">Gehen Sie zu **Systemverwaltung \> Periodische Aufgaben \> Datenbank \> Konsistenzprüfung**.</span><span class="sxs-lookup"><span data-stu-id="52390-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="52390-118">Legen Sie im Dialogfeld **Konsistenzprüfung** das Feld **Modul** auf *Lagerortverwaltung* fest.</span><span class="sxs-lookup"><span data-stu-id="52390-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="52390-119">Legen Sie das Feld **Prüfen/Beheben** auf *Fehler beheben* fest.</span><span class="sxs-lookup"><span data-stu-id="52390-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="52390-120">Wählen Sie in der Liste der Kontrollkästchen das Kontrollkästchen **Konsistenz der Ladung** und stellen Sie sicher, dass nur die Zeile für dieses Kontrollkästchen markiert ist.</span><span class="sxs-lookup"><span data-stu-id="52390-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="52390-121">Wählen Sie oben in der Liste der Kontrollkästchen die Schaltfläche mit den Auslassungspunkten (**...**), und wählen Sie dann im Menü **Dialog**.</span><span class="sxs-lookup"><span data-stu-id="52390-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="52390-122">Legen Sie im Dialogfeld **Konsistenzprüfung des Gewichts der Ladung im Lagerort** die folgenden Felder fest, um die Kriterien anzugeben, nach denen die Konsistenzprüfung ausgeführt werden soll:</span><span class="sxs-lookup"><span data-stu-id="52390-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="52390-123">**Ladungs-ID:** Geben Sie eine Ladungs-ID an.</span><span class="sxs-lookup"><span data-stu-id="52390-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="52390-124">Lassen Sie dies leer, um alle Ladung-IDs zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="52390-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="52390-125">**Elementnummer:** Geben Sie eine Elementnummer an.</span><span class="sxs-lookup"><span data-stu-id="52390-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="52390-126">Lassen Sie dies leer, um alle Elemente zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="52390-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="52390-127">**Gewicht auf Ladungen immer neu berechnen:** Legen Sie diese Option auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="52390-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="52390-128">**Überschreiben von Gewicht auf Ladungs-Zeilen zulassen:** Legen Sie diese Option auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="52390-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="52390-129">Wählen Sie **OK**, um die Dialogbox **Prüfung der Konsistenz des Gewichts der Ladung im Lagerort** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="52390-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="52390-130">Wählen Sie die Schaltfläche mit den Auslassungspunkten und dann **Ausführen** im Menü aus.</span><span class="sxs-lookup"><span data-stu-id="52390-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="52390-131">Das Gewicht wird auf der Grundlage der von Ihnen angegebenen Kriterien neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="52390-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="52390-132">Wählen Sie den Link **Meldungsdetails**, um das Ergebnis der Konsistenzprüfung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="52390-132">Select the **Message details** link to view the result of the consistency check.</span></span>
