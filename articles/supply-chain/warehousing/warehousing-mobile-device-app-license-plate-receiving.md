---
title: Kennzeichenempfang über die Warehousing Mobile App
description: In diesem Thema wird erläutert, wie Sie die Warehousing-App so einrichten, dass die Verwendung eines Kennzeichenempfangsprozesses zum Empfangen von Inventar unterstützt wird.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261334"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="35483-103">Kennzeichenempfang über die Warehousing Mobile App</span><span class="sxs-lookup"><span data-stu-id="35483-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="35483-104">In diesem Thema wird erläutert, wie Sie die Warehousing-Mobile-App einrichten, so dass sie die Verwendung eines Kennzeichenempfangsprozesses zum Empfangen von Bestand unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35483-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="35483-105">Mit dieser Funktion können Sie schnell den Eingang des eingehenden Bestands aufzeichnen, der sich auf eine Vorabmitteilung (ASN) bezieht.</span><span class="sxs-lookup"><span data-stu-id="35483-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="35483-106">Das System erstellt automatisch einen Lieferavis, wenn Lagerverwaltungsprozesse zum Versenden eines Transportauftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35483-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="35483-107">Für den Bestellvorgang kann ein ASNs manuell erfasst oder mithilfe eines eingehenden ASN-Datenentitätsprozesses automatisch importiert werden.</span><span class="sxs-lookup"><span data-stu-id="35483-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="35483-108">Die ANS-Daten werden mit Ladungen und Sendungen über die *Verpackungsstrukturen* verknüpft, wo Paletten (übergeordnete Kennzeichen) Fälle enthalten können (verschachtelte Kennzeichen).</span><span class="sxs-lookup"><span data-stu-id="35483-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="35483-109">Um die Anzahl der Bestandtransaktionen zu verringern, wenn Verpackungsstrukturen mit verschachtelten Kennzeichen verwendet werden, zeichnet das System das physische Inventar auf dem übergeordneten Kennzeichen auf.</span><span class="sxs-lookup"><span data-stu-id="35483-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="35483-110">Um die Verschiebung des physischen Bestands vom übergeordneten Kennzeichen zu den verschachtelten Kennzeichen basierend auf den Daten der Verpackungsstruktur auszulösen, muss das mobile Gerät einen Menüpunkt bereitstellen, der auf dem Arbeitserstellungsprozess *auf verschachtelte Kennzeichen packen* basiert.</span><span class="sxs-lookup"><span data-stu-id="35483-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="35483-111">Zeigen Sie die empfangende Zusammenfassungsseite an oder überspringen Sie sie</span><span class="sxs-lookup"><span data-stu-id="35483-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="35483-112">Sie können die Funktion *Steuern Sie, ob auf Mobilgeräten eine Empfangsübersichtsseite angezeigt werden soll* verwenden, um einen zusätzlichen detaillierten Warehouse-App-Ablauf als Teil des Kennzeichenempfangsprozesses zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="35483-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="35483-113">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="35483-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="35483-114">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="35483-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="35483-115">Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="35483-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="35483-116">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="35483-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="35483-117">**Funktionsname:** *Steuern Sie, ob auf Mobilgeräten eine Empfangsübersichtsseite angezeigt werden soll*</span><span class="sxs-lookup"><span data-stu-id="35483-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="35483-118">Wenn diese Funktion aktiviert ist, bieten Menüelemente für mobile Geräte zum Empfangen von Kennzeichen oder zum Empfangen und Einlagerungen eine Einstellung **Empfangsübersichtsseite anzeigen** an.</span><span class="sxs-lookup"><span data-stu-id="35483-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="35483-119">Diese Einstellung bietet folgende Optionen:</span><span class="sxs-lookup"><span data-stu-id="35483-119">This setting has the following options:</span></span>

- <span data-ttu-id="35483-120">**Eine detaillierte Zusammenfassung anzeigen** – Während des Empfangs des Kennzeichens wird den Mitarbeitern eine zusätzliche Seite mit den vollständigen ASN-Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="35483-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="35483-121">**Überspringen Sie die Zusammenfassung** – Die Mitarbeiter sehen nicht die vollständigen ASN-Informationen.</span><span class="sxs-lookup"><span data-stu-id="35483-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="35483-122">Lagerarbeiter können während des Empfangsprozesses auch keinen Dispositionscode festlegen oder Ausnahmen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="35483-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="35483-123">Verhindern Sie, dass Kennzeichen mit Transportauftragsversand in anderen Lagern als dem Ziellager verwendet werden</span><span class="sxs-lookup"><span data-stu-id="35483-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="35483-124">Ein Kennzeichenempfangsprozess kann nicht verwendet werden, wenn ein ASN eine Kennzeichen-ID enthält, die bereits vorhanden ist und physische Daten an einem anderen Lagerort als dem Lagerort enthält, an dem die Kennzeichenregistrierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="35483-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="35483-125">Für Transportauftragsszenarien, in denen das Transitlager keine Kennzeichen erfasst (und daher auch keinen physischen Lagerbestand pro Kennzeichen erfasst), können Sie die Funktion *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* verwenden, um physische Aktualisierungen von unterwegs befindlichen Kennzeichen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="35483-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="35483-126">Bevor Sie diese Funktion nutzen können, muss sie auf Ihrem System aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="35483-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="35483-127">Administratoren können mit den Einstellungen [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und sie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="35483-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="35483-128">Im Arbeitsbereich **Funktionsverwaltung** ist diese Funktion wie folgt aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="35483-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="35483-129">**Module:** *Lagerortverwaltung*</span><span class="sxs-lookup"><span data-stu-id="35483-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="35483-130">**Funktionsname:** *Verhindern Sie, dass Kennzeichen mit Transportauftragsversand in anderen Lagern als dem Ziellager verwendet werden*</span><span class="sxs-lookup"><span data-stu-id="35483-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="35483-131">Führen Sie die folgenden Schritte aus, um die Funktionalität zu verwalten, wenn diese Funktion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="35483-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="35483-132">Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="35483-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="35483-133">Auf der Registerkarte **Allgemeines** im Inforegister **Kennzeichnung** legen Sie das Feld **Kennzeichenrichtlinie für Transitlager** auf einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="35483-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="35483-134">**Wiederverwendung von nicht verfolgtem Kennzeichen zulassen** – Das System funktioniert genauso wie wenn die Funktion *Verhindern Sie, dass Versandkennzeichen für Transportaufträge in anderen Lagern als dem Ziellager verwendet werden* nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="35483-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="35483-135">Dieser Wert ist die Standardeinstellung, wenn Sie die Funktion zum ersten Mal aktivieren.</span><span class="sxs-lookup"><span data-stu-id="35483-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="35483-136">**Verhindern Sie die Wiederverwendung von nicht verfolgten Kennzeichen** – Bis zum Eingang des Überweisungsauftrags sind im Ziellager nur Aktualisierungen zulässig, die sich auf ein versendetes Kennzeichen beziehen.</span><span class="sxs-lookup"><span data-stu-id="35483-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="35483-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35483-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="35483-138">Weitere Informationen zu Menüelementen für Mobilgeräte finden Sie unter [Richten Sie mobile Geräte für die Lagerarbeit ein](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="35483-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
