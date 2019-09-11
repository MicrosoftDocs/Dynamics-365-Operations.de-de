---
title: Die automatische Aktualisierung von Anlagenzählern
description: In diesem Thema wird die automatische Aktualisierung von Anlagenzählern in Asset Management beschrieben.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875679"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="1afb1-103">Die automatische Aktualisierung von Anlagenzählern</span><span class="sxs-lookup"><span data-stu-id="1afb1-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1afb1-104">Im vorherigen Abschnitt wurde die manuelle Erfassung von Anlagenzählern beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1afb1-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="1afb1-105">Das Einrichten von Anlagenzählern wird unter [Zähler](../setup-for-objects/counters.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1afb1-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="1afb1-106">Zählerwerte können auch aus Produktionserfassungen automatisch aktualisiert werden, die auf Produktionsstunden oder Produktionsmenge basieren.</span><span class="sxs-lookup"><span data-stu-id="1afb1-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="1afb1-107">Dies erfolgt unter **Anlagenzähler aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="1afb1-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="1afb1-108">Sie können eine oder mehrere Anlagen aktualisieren, indem Sie den Parameter **Von Datum** einfügen.</span><span class="sxs-lookup"><span data-stu-id="1afb1-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="1afb1-109">Dieser Parameter gibt das Startdatum für Produktionserfassungen (Stunden oder produzierte Menge) an, d. h. das Anfangsdatum, ab dem Zählerwerte aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1afb1-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="1afb1-110">Alle Anlagen, die einer Ressource zugeordnet sind *und* Anlagenzähler enthalten, die so eingerichtet wurden, das sie basierend auf der erzeugten Menge oder den Produktionsstunden aktualisiert werden, werden in einer automatischen Aktualisierung berücksichtigt und neue Zählerwerte werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="1afb1-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="1afb1-111">Bezüglich der Zähler, die auf der Produktionsmenge basieren, werden die Gutmenge sowie die erfasste Ausschussmenge in die Zählung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="1afb1-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="1afb1-112">Wenn die Einheit, die für die Erfassung der produzierten Menge verwendet wird, sich von der Einheit unterscheidet, die im Zähler verwendet wird, wird die Menge konvertiert, um der Zählereinheit zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1afb1-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="1afb1-113">Wie bereits angegeben können automatische Zähler aus Produktionserfassungen aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1afb1-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="1afb1-114">Daher muss die Anlage, für die Sie automatisch Zähler aktualisieren möchten, einer Ressource (Maschine) zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1afb1-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="1afb1-115">Die folgenden Beschreibungen bieten einen Überblick über die Einstellungen und die Verarbeitung von Produktionsaufträgen (im Modul **Produktionssteuerung**), das als Grundlage für die automatische Aktualisierung von Zählern für eine Anlage im Modul **Anlagenverwaltung** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1afb1-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="1afb1-116">Bei produzierte Mengen oder Produktionsstunden für die Ressource erfasst wurden, können Sie die zugehörigen Anlagenzähler aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1afb1-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="1afb1-117">Klicken Sie auf **Anlagenverwaltung** > **Periodisch** > **Anlagen** > **Anlagenzähler aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="1afb1-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="1afb1-118">Wählen Sie das Startdatum der automatischen Aktualisierung im Feld **Von Datum** aus.</span><span class="sxs-lookup"><span data-stu-id="1afb1-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="1afb1-119">Das Datum in diesem Feld ist das Datum „In Bearbeitung“ aus **Arbeitsplanbuchungen** (Feld **Produktionssteuerung** > **Abfragen und Berichte** > **Produktion** > **Arbeitsplanbuchungen** > **Physisches Datum**).</span><span class="sxs-lookup"><span data-stu-id="1afb1-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="1afb1-120">Wenn Sie bestimmte Anlagen, Anlagentypen oder Ressourcen auswählen möchten, klicken Sie auf **Filtern** auf dem Inforegister **Einzuschließende Datensätze** und nehmen die zutreffende Auswahl vor.</span><span class="sxs-lookup"><span data-stu-id="1afb1-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="1afb1-121">Bei Bedarf können Sie die automatische Aktualisierung als Batchauftrag auf dem Inforegister **Im Hintergrund ausführen** einrichten.</span><span class="sxs-lookup"><span data-stu-id="1afb1-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Abbildung 1](media/12-work-orders.png)

5. <span data-ttu-id="1afb1-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1afb1-123">Click **OK**.</span></span> <span data-ttu-id="1afb1-124">Wenn die automatische Aktualisierung von Anlagenzählern erfolgt, können Sie die Zählererfassungen, die sich auf die Anlage beziehen, unter **Anlagenzähler** (**Anlagenverwaltung** > **Allgemein** > **Anlagen** > **Alle Anlagen** > Anlage auswählen > Schaltfläche **Zähler** auswählen).</span><span class="sxs-lookup"><span data-stu-id="1afb1-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="1afb1-125">Unter **Anlagenzählersummen** können Sie einen Überblick der letzten Erfassung abrufen, die für alle Zählertypen für alle Anlagen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1afb1-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="1afb1-126">Klicken Sie auf **Anlagenverwaltung** > **Abfragen** > **Anlagen** > **Aggregierter Wert für Anlage**.</span><span class="sxs-lookup"><span data-stu-id="1afb1-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="1afb1-127">Die Ansicht ist **Anlagenzähler** sehr ähnlich, aber Sie können in **Aggregierter Wert für Anlage** keine Erfassungen hinzufügen oder bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1afb1-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="1afb1-128">Es ist nur für den Überblick.</span><span class="sxs-lookup"><span data-stu-id="1afb1-128">It is for overview only.</span></span>

![Abbildung 2](media/13-work-orders.png)


- <span data-ttu-id="1afb1-130">Es ist trotzdem möglich, manuelle Zählerwerterfassungen für Zählertypen zu erstellen, die automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1afb1-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="1afb1-131">Weitere Informationen finden Sie im Abschnitt „Die manuelle Aktualisierung von Anlagenzählern“.</span><span class="sxs-lookup"><span data-stu-id="1afb1-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="1afb1-132">Sie können Zähler einrichten, die sich auf einen anderen beziehen Zähler, was bedeutet, dass, wenn ein Zähler aktualisiert wird, zugehörige Zähler automatisch gleichzeitig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1afb1-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="1afb1-133">Informationen zum Einrichten der zugehörigen Zähler finden Sie unter [Zähler](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="1afb1-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
