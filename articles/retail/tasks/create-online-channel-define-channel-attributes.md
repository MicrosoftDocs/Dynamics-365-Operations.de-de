---
title: Erstellen Sie Onlinekanal und definieren Sie Kanalattribute
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569520"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="44a7f-103">Erstellen Sie Onlinekanal und definieren Sie Kanalattribute</span><span class="sxs-lookup"><span data-stu-id="44a7f-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="44a7f-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Online Kanals und dessen Hinzufügen zur Organisationshierarchie.</span><span class="sxs-lookup"><span data-stu-id="44a7f-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="44a7f-105">Sie müssen die Organisationshierarchie erstellen, bevor Sie einen neuen Online Kanal erstellen können.</span><span class="sxs-lookup"><span data-stu-id="44a7f-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="44a7f-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="44a7f-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="44a7f-107">Neuen Onlinechannel erstellen</span><span class="sxs-lookup"><span data-stu-id="44a7f-107">Create a new online channel</span></span>
1. <span data-ttu-id="44a7f-108">Navigieren Sie zu Einzelhandel und Handel > Kanäle > Onlineshops.</span><span class="sxs-lookup"><span data-stu-id="44a7f-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="44a7f-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="44a7f-109">Click New.</span></span>
3. <span data-ttu-id="44a7f-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="44a7f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="44a7f-111">Geben Sie im Feld 'Lagerort' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="44a7f-112">Wählen Sie im Feld "Zeitzone des Shops" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="44a7f-113">Geben Sie im Feld "Standarddebitor" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="44a7f-114">Geben Sie im Feld "Debitorenadressbuch" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="44a7f-115">Geben Sie im Feld "Zahlungsbedingungen" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="44a7f-116">Geben Sie im Feld "Zahlungsmethode" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="44a7f-117">Geben Sie im Feld "E-Mail-Benachrichtigungsprofil" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="44a7f-118">Erweitern Sie den Finanzdimensionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="44a7f-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="44a7f-119">Geben Sie im Feld "BusinessUnit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="44a7f-120">Legen Sie auf ähnliche Weise den Wert für alle anderen Standarddimensionen fest.</span><span class="sxs-lookup"><span data-stu-id="44a7f-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="44a7f-121">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="44a7f-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="44a7f-122">Online Kanal zur Organisationshierarchie hinzufügen</span><span class="sxs-lookup"><span data-stu-id="44a7f-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="44a7f-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="44a7f-123">Close the page.</span></span>
2. <span data-ttu-id="44a7f-124">Wechseln Sie zu "Organisationsverwaltung" > "Organisationen" > "Organisationshierarchien".</span><span class="sxs-lookup"><span data-stu-id="44a7f-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="44a7f-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="44a7f-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="44a7f-126">Klicken Sie auf "Ansicht".</span><span class="sxs-lookup"><span data-stu-id="44a7f-126">Click View.</span></span>
5. <span data-ttu-id="44a7f-127">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="44a7f-127">Click Edit.</span></span>
    * <span data-ttu-id="44a7f-128">Sie können einen beliebigen Hierarchieknoten auswählen, unter dem Sie den neuen Kanal einfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="44a7f-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="44a7f-129">Klicken Sie auf Einfügen.</span><span class="sxs-lookup"><span data-stu-id="44a7f-129">Click Insert.</span></span>
7. <span data-ttu-id="44a7f-130">Klicken Sie auf "Einzelhandelskanal".</span><span class="sxs-lookup"><span data-stu-id="44a7f-130">Click Retail channel.</span></span>
8. <span data-ttu-id="44a7f-131">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="44a7f-131">Click OK.</span></span>
9. <span data-ttu-id="44a7f-132">Klicken Sie auf "Veröffentlichen", um das Ablagedialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="44a7f-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="44a7f-133">Geben Sie im Feld "Gültigkeitsdatum" ein Datum und eine Uhrzeit ein.</span><span class="sxs-lookup"><span data-stu-id="44a7f-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="44a7f-134">Klicken Sie auf "Veröffentlichen".</span><span class="sxs-lookup"><span data-stu-id="44a7f-134">Click Publish.</span></span>

