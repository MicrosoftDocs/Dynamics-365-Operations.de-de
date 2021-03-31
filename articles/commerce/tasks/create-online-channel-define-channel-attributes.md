---
title: Erstellen Sie Onlinekanal und definieren Sie Kanalattribute
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f85a74e44be28452f5d892f1875d74261f9dbe3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215435"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="e8c8d-103">Erstellen Sie Onlinekanal und definieren Sie Kanalattribute</span><span class="sxs-lookup"><span data-stu-id="e8c8d-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8c8d-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="e8c8d-105">Sie müssen die Organisationshierarchie erstellen, bevor Sie einen neuen Online Kanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="e8c8d-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="e8c8d-107">Neuen Onlinechannel erstellen</span><span class="sxs-lookup"><span data-stu-id="e8c8d-107">Create a new online channel</span></span>
1. <span data-ttu-id="e8c8d-108">Navigieren Sie zu Einzelhandel und Handel > Kanäle > Onlineshops.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="e8c8d-109">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-109">Click New.</span></span>
3. <span data-ttu-id="e8c8d-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e8c8d-111">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="e8c8d-112">Wählen Sie im Feld "Zeitzone des Shops" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="e8c8d-113">Geben Sie im Feld "Standarddebitor" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="e8c8d-114">Geben Sie im Feld "Debitorenadressbuch" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="e8c8d-115">Geben Sie im Feld "Zahlungsbedingungen" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="e8c8d-116">Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="e8c8d-117">Geben Sie im Feld "E-Mail-Benachrichtigungsprofil" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="e8c8d-118">Erweitern Sie den Finanzdimensionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="e8c8d-119">Geben Sie im Feld "BusinessUnit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="e8c8d-120">Legen Sie auf ähnliche Weise den Wert für alle anderen Standarddimensionen fest.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="e8c8d-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e8c8d-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="e8c8d-122">Online Kanal zur Organisationshierarchie hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e8c8d-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="e8c8d-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-123">Close the page.</span></span>
2. <span data-ttu-id="e8c8d-124">Wechseln Sie zu "Organisationsverwaltung" > "Organisationen" > "Organisationshierarchien".</span><span class="sxs-lookup"><span data-stu-id="e8c8d-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="e8c8d-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e8c8d-126">Klicken Sie auf "Ansicht".</span><span class="sxs-lookup"><span data-stu-id="e8c8d-126">Click View.</span></span>
5. <span data-ttu-id="e8c8d-127">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="e8c8d-127">Click Edit.</span></span>
    * <span data-ttu-id="e8c8d-128">Sie können einen beliebigen Hierarchieknoten auswählen, unter dem Sie den neuen Kanal einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="e8c8d-129">Klicken Sie auf Einfügen.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-129">Click Insert.</span></span>
7. <span data-ttu-id="e8c8d-130">Klicken Sie auf den Commerce-Kanal.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="e8c8d-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="e8c8d-131">Click OK.</span></span>
9. <span data-ttu-id="e8c8d-132">Klicken Sie auf "Veröffentlichen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="e8c8d-133">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="e8c8d-134">Klicken Sie auf "Veröffentlichen".</span><span class="sxs-lookup"><span data-stu-id="e8c8d-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="e8c8d-135">Konfigurieren von Aufträgen für die Benachrichtigung beinahe in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="e8c8d-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="e8c8d-136">Gehen Sie zu Einzelhandel und Handel > Zentralverwaltungseinrichtung > Parameter > Commerce-Parameter.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="e8c8d-137">Legen Sie „Echtzeitdienst für eCommerce-Auftragserstellung verwenden“ auf „Ja“ fest.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="e8c8d-138">Führen Sie den Verteilungszeitplan 1070 aus, um Änderungen an der Kanaldatenbank zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e8c8d-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]