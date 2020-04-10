---
title: " Eine Hardwarestation erstellen und zuordnen"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen einer neuen Hardwarestation.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 305308b0e4ba99aae4bf6f8f94041db570a25893
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141036"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="f9e24-103"> Eine Hardwarestation erstellen und zuordnen</span><span class="sxs-lookup"><span data-stu-id="f9e24-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9e24-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen einer neuen Hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="f9e24-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="f9e24-105">Ein neues Hardwareprofil wird erstellt und verwendet, um neue Hardwarestationen eines vordefinierten Shops (Kanal) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9e24-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="f9e24-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9e24-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f9e24-107">Wechseln Sie zu den Handels-Grundlagen > Kanälen >.</span><span class="sxs-lookup"><span data-stu-id="f9e24-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="f9e24-108">> ..</span><span class="sxs-lookup"><span data-stu-id="f9e24-108">> ..</span></span> <span data-ttu-id="f9e24-109">> ..</span><span class="sxs-lookup"><span data-stu-id="f9e24-109">> ..</span></span> <span data-ttu-id="f9e24-110">> Hardwarestation-Profile.</span><span class="sxs-lookup"><span data-stu-id="f9e24-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="f9e24-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f9e24-111">Click New.</span></span>
3. <span data-ttu-id="f9e24-112">Geben Sie im Hardwarestation-Kennungsfeld "TestHWProfile" ein.</span><span class="sxs-lookup"><span data-stu-id="f9e24-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="f9e24-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f9e24-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f9e24-114">Geben Sie im Feld "Portnummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f9e24-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="f9e24-115">Klicken Sie im Feld "Hardwareprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9e24-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f9e24-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f9e24-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f9e24-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9e24-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f9e24-118">Klicken Sie im Feld "Paketname" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9e24-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f9e24-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9e24-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f9e24-120">Dies ist das Standardpaket, das mit einer neuen Umgebung kommt.</span><span class="sxs-lookup"><span data-stu-id="f9e24-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="f9e24-121">Die Versionsnummer kann variieren.</span><span class="sxs-lookup"><span data-stu-id="f9e24-121">The version number may vary.</span></span>  
11. <span data-ttu-id="f9e24-122">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="f9e24-122">Click Save.</span></span>
12. <span data-ttu-id="f9e24-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f9e24-123">Close the page.</span></span>
13. <span data-ttu-id="f9e24-124">Navigieren Sie zu Einzelhandel und Commerce > Kanäle > Alle Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="f9e24-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="f9e24-125">Wählen Sie in der Liste die Zeile "17" aus.</span><span class="sxs-lookup"><span data-stu-id="f9e24-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="f9e24-126">Wenn Sie das USRT-Demodatenunternehmen verwenden, ist dies der Houston-Speicher.</span><span class="sxs-lookup"><span data-stu-id="f9e24-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="f9e24-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9e24-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f9e24-128">Schalten Sie die Erweiterung des Abschnitts "Hardwarestationen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="f9e24-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="f9e24-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9e24-129">Click Add.</span></span>
18. <span data-ttu-id="f9e24-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9e24-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="f9e24-131">Klicken Sie im Feld "Profilkennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f9e24-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="f9e24-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f9e24-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f9e24-133">Dies muss das neue Hardwarestationsprofil sein, das in den vorherigen Schritten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9e24-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="f9e24-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f9e24-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="f9e24-135">Geben Sie im Feld "Hostname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f9e24-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="f9e24-136">Geben Sie einen Wert in das Feld "Terminalkennung für Überweisung (elektronisch)" ein.</span><span class="sxs-lookup"><span data-stu-id="f9e24-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="f9e24-137">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f9e24-137">Click Save.</span></span>

