---
title: Mietvertragsparameter konfigurieren (Vorschau)
description: In diesem Thema werden die Konfigurationseinstellungen für Anlagenleasing beschrieben, z. B. Sicherheitsinformationen und Buchhaltungseinstellungen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443776"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="fdf96-103">Mietvertragsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="fdf96-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdf96-104">Verschiedene Konfigurationseinstellungen wirken sich auf das Verhalten von Anlagenleasing aus.</span><span class="sxs-lookup"><span data-stu-id="fdf96-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="fdf96-105">Diese Einstellungen umfassen Erfassungsnamen, allgemeine Parameter und Buchungsprofileinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fdf96-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="fdf96-106">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="fdf96-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="fdf96-107">Wählen Sie auf der Registerkarte **Mietverträge** das Inforegister **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="fdf96-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="fdf96-108">Der **Manuelles Überschreiben der Klassifizierung zulassen**-Parameter bestimmt, ob die Mietvertragsklassifizierung überschrieben werden kann, bevor der Zahlungsplan bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="fdf96-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="fdf96-109">Der **Entitätsübergreifender Batch**-Parameter bestimmt, ob Sie von der aktuellen juristischen Person auf andere juristische Personen buchen können.</span><span class="sxs-lookup"><span data-stu-id="fdf96-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="fdf96-110">Wenn dieser Parameter aktiviert ist, können Sie Journaleinträge für die juristischen Personen erstellen, auf die Sie Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="fdf96-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="fdf96-111">Stellen Sie die **Löschen bestätigter Mietverträge zulassen**-Option auf **Ja** fest, damit Mietverträge mit bestätigten Zahlungsplänen gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="fdf96-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="fdf96-112">Mietverträge können, unabhängig von der Einstellung dieser Option, nicht gelöscht werden, wenn gebuchte oder nicht gebuchte Transaktionen mit ihnen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fdf96-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="fdf96-113">Sie können einen Mietvertragsdatensatz nach dem Löschen nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="fdf96-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="fdf96-114">Wenn Sie Datensätze für einen gelöschten Mietvertrag entweder manuell oder über Dateneinheiten hochladen, werden die hochgeladenen Informationen als neu behandelt und nicht als Aktualisierung eines vorhandenen Mietvertrags.</span><span class="sxs-lookup"><span data-stu-id="fdf96-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="fdf96-115">Wenn Sie diese Option auf **Ja** setzen, und die Übergangsart des Buches **Kumulative Aufholoption A oder B** ist, setzt das System das **Zinssatz für Neukredit**-Feld auf der Seite **Bucheinrichtung** auf den Wert des **Zinssatz für Neukredit bei Übergang**-Felds.</span><span class="sxs-lookup"><span data-stu-id="fdf96-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="fdf96-116">Wenn diese Option auf **Nein** gesetzt ist, wird der Zinssatz für den Hauptmietvertrag auf den Wert vom Feld **Zinssatz für Neukredit** auf der **Buchdetails**-Seite festgelegt, unabhängig von der Übergangsart des Buches.</span><span class="sxs-lookup"><span data-stu-id="fdf96-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="fdf96-117">Stellen Sie die **Abschreibungen für geschlossene Bücher zulassen**-Option auf **Ja**, damit Abschreibungsaufwendungen rückgängig gemacht werden können.</span><span class="sxs-lookup"><span data-stu-id="fdf96-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="fdf96-118">Aufwandstransaktionen können auch bei geschlossener Buchversion rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="fdf96-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fdf96-119">Wir empfehlen, diese Option auf **Nein** zu setzen.</span><span class="sxs-lookup"><span data-stu-id="fdf96-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="fdf96-120">Die Einstellung dieser Option wird als Validierung und Kontrolle verwendet, um zu verhindern, dass eine geschlossene Buchversion versehentlich abgeschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="fdf96-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="fdf96-121">Indem Sie die Option auf **Nein** setzen, tragen Sie dazu bei, den Nettobuchwert und zukünftige Abschreibungsberechnungen korrekt zu halten.</span><span class="sxs-lookup"><span data-stu-id="fdf96-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
