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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4547731d7e3bc56b1ba5e0a35ff4746c6c0e9863
ms.sourcegitcommit: 901ec3b360303bb8b4d9a9dcfecc6d75d7f844a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2019
ms.locfileid: "1618295"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="7a0ee-103">Erstellen Sie Onlinekanal und definieren Sie Kanalattribute</span><span class="sxs-lookup"><span data-stu-id="7a0ee-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="7a0ee-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="7a0ee-105">Sie müssen die Organisationshierarchie erstellen, bevor Sie einen neuen Online Kanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="7a0ee-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="7a0ee-107">Neuen Onlinechannel erstellen</span><span class="sxs-lookup"><span data-stu-id="7a0ee-107">Create a new online channel</span></span>
1. <span data-ttu-id="7a0ee-108">Navigieren Sie zu Einzelhandel und Handel > Kanäle > Onlineshops.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="7a0ee-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-109">Click New.</span></span>
3. <span data-ttu-id="7a0ee-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7a0ee-111">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="7a0ee-112">Wählen Sie im Feld "Zeitzone des Shops" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="7a0ee-113">Geben Sie im Feld "Standarddebitor" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="7a0ee-114">Geben Sie im Feld "Debitorenadressbuch" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="7a0ee-115">Geben Sie im Feld "Zahlungsbedingungen" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="7a0ee-116">Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="7a0ee-117">Geben Sie im Feld "E-Mail-Benachrichtigungsprofil" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="7a0ee-118">Erweitern Sie den Finanzdimensionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="7a0ee-119">Geben Sie im Feld "BusinessUnit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="7a0ee-120">Legen Sie auf ähnliche Weise den Wert für alle anderen Standarddimensionen fest.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="7a0ee-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="7a0ee-122">Online Kanal zur Organisationshierarchie hinzufügen</span><span class="sxs-lookup"><span data-stu-id="7a0ee-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="7a0ee-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-123">Close the page.</span></span>
2. <span data-ttu-id="7a0ee-124">Wechseln Sie zu "Organisationsverwaltung" > "Organisationen" > "Organisationshierarchien".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="7a0ee-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7a0ee-126">Klicken Sie auf "Ansicht".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-126">Click View.</span></span>
5. <span data-ttu-id="7a0ee-127">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-127">Click Edit.</span></span>
    * <span data-ttu-id="7a0ee-128">Sie können einen beliebigen Hierarchieknoten auswählen, unter dem Sie den neuen Kanal einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="7a0ee-129">Klicken Sie auf Einfügen.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-129">Click Insert.</span></span>
7. <span data-ttu-id="7a0ee-130">Klicken Sie auf "Einzelhandelskanal".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-130">Click Retail channel.</span></span>
8. <span data-ttu-id="7a0ee-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-131">Click OK.</span></span>
9. <span data-ttu-id="7a0ee-132">Klicken Sie auf "Veröffentlichen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="7a0ee-133">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="7a0ee-134">Klicken Sie auf "Veröffentlichen".</span><span class="sxs-lookup"><span data-stu-id="7a0ee-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-realtime-notification"></a><span data-ttu-id="7a0ee-135">Konfigurieren von Aufträgen für die Benachrichtigung beinahe in Echtzeit</span><span class="sxs-lookup"><span data-stu-id="7a0ee-135">Configure orders for near realtime notification</span></span>
1. <span data-ttu-id="7a0ee-136">Gehen Sie zu Einzelhandel > Zentralverwaltungseinrichtung > Parameter > Retail-Parameter.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-136">Go to Retail  > Headquarters setup > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="7a0ee-137">Legen Sie „Echtzeitdienst für eCommerce-Auftragserstellung verwenden“ auf „Ja“ fest.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="7a0ee-138">Führen Sie den Verteilungszeitplan 1070 aus, um Änderungen an der Kanaldatenbank zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="7a0ee-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


