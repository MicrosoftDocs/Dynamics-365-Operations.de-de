---
title: Zugriffsrechte für einen Kostenobjekt-Controller konfigurieren
description: Verwenden Sie diese Prozedur, um Zugriffsberechtigungen für einen Kostenträgercontroller zu konfigurieren.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b62e5765964a13357e0e7b663be1c7fd2cc19037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208798"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="6fd18-103">Zugriffsrechte für einen Kostenobjekt-Controller konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6fd18-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fd18-104">Verwenden Sie diese Prozedur, um Zugriffsberechtigungen für einen Kostenträgercontroller zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6fd18-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="6fd18-105">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="6fd18-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="6fd18-106">Weisen Sie die Kostenträgercontroller-Rolle zu</span><span class="sxs-lookup"><span data-stu-id="6fd18-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="6fd18-107">Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".</span><span class="sxs-lookup"><span data-stu-id="6fd18-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="6fd18-108">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6fd18-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6fd18-109">Filtern Sie beispielsweise im Feld Benutzernamen mit einem Wert "Alicia".</span><span class="sxs-lookup"><span data-stu-id="6fd18-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="6fd18-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="6fd18-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6fd18-111">Rollen zuweisen</span><span class="sxs-lookup"><span data-stu-id="6fd18-111">Click Assign roles.</span></span>
5. <span data-ttu-id="6fd18-112">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="6fd18-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="6fd18-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="6fd18-114">Aktivieren Sie dke Zugriffslistensicherheit</span><span class="sxs-lookup"><span data-stu-id="6fd18-114">Enable access list security</span></span>
1. <span data-ttu-id="6fd18-115">Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.</span><span class="sxs-lookup"><span data-stu-id="6fd18-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="6fd18-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6fd18-117">Organisation auswählen</span><span class="sxs-lookup"><span data-stu-id="6fd18-117">Select Organization.</span></span>  
3. <span data-ttu-id="6fd18-118">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="6fd18-118">Click Edit.</span></span>
4. <span data-ttu-id="6fd18-119">Wählen Sie die Option Ja im Feld Zugriffslisten-Hierarchiegebiet aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="6fd18-120">Klicken Sie auf "Hierarchie anzeigen".</span><span class="sxs-lookup"><span data-stu-id="6fd18-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="6fd18-121">Weisen Sie dem Benutzer Zugriffsberechtigungen zu</span><span class="sxs-lookup"><span data-stu-id="6fd18-121">Assign access rights to user</span></span>
1. <span data-ttu-id="6fd18-122">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6fd18-122">Click New.</span></span>
2. <span data-ttu-id="6fd18-123">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6fd18-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6fd18-124">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="6fd18-125">Wählen Sie Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-125">Select Admin.</span></span>  
4. <span data-ttu-id="6fd18-126">Wählen Sie in der Struktur Organisation\CEO\CFO\FIM'.</span><span class="sxs-lookup"><span data-stu-id="6fd18-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="6fd18-127">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="6fd18-127">Click New.</span></span>
6. <span data-ttu-id="6fd18-128">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="6fd18-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="6fd18-129">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="6fd18-130">Wählen Sie Alicia aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-130">Select Alicia.</span></span>  
8. <span data-ttu-id="6fd18-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6fd18-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="6fd18-132">Aktivieren Sie Zugriffsberechtigungen in der Kostenrechnung</span><span class="sxs-lookup"><span data-stu-id="6fd18-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="6fd18-133">Gehen Sie zu Kostenbuchhaltung > Einrichtung > Parameter.</span><span class="sxs-lookup"><span data-stu-id="6fd18-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="6fd18-134">Klicken Sie auf die Registerkarte "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="6fd18-134">Click the General tab.</span></span>
3. <span data-ttu-id="6fd18-135">Wählen Sie im Anzeigezugriff für Kostenobjektdimensionsmitglieder Ja aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="6fd18-136">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6fd18-136">Click Save.</span></span>
5. <span data-ttu-id="6fd18-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6fd18-137">Close the page.</span></span>
6. <span data-ttu-id="6fd18-138">Wechseln Sie zur Kostenbuchhaltung > Einstellungs > Kostenkontrollearbeitsbereichskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6fd18-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="6fd18-139">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="6fd18-139">Click Edit.</span></span>
8. <span data-ttu-id="6fd18-140">Wählen Sie "Ja" im Feld "Veröffentlichte Felder" aus.</span><span class="sxs-lookup"><span data-stu-id="6fd18-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="6fd18-141">Wenn Sie diese Option auf Ja setzen, können Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller.</span><span class="sxs-lookup"><span data-stu-id="6fd18-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="6fd18-142">Wenn Sie diese Option auf Nein setzen, können Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller.</span><span class="sxs-lookup"><span data-stu-id="6fd18-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="6fd18-143">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="6fd18-143">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]