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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adbd5ef1cafe778cf897aafb05c77fca89be3e20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964919"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="d6b80-103"> Eine Hardwarestation erstellen und zuordnen</span><span class="sxs-lookup"><span data-stu-id="d6b80-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6b80-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen einer neuen Hardwarestation.</span><span class="sxs-lookup"><span data-stu-id="d6b80-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="d6b80-105">Ein neues Hardwareprofil wird erstellt und verwendet, um neue Hardwarestationen eines vordefinierten Shops (Kanal) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6b80-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="d6b80-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6b80-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d6b80-107">Wechseln Sie zu den Handels-Grundlagen > Kanälen >.</span><span class="sxs-lookup"><span data-stu-id="d6b80-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="d6b80-108">> ..</span><span class="sxs-lookup"><span data-stu-id="d6b80-108">> ..</span></span> <span data-ttu-id="d6b80-109">> ..</span><span class="sxs-lookup"><span data-stu-id="d6b80-109">> ..</span></span> <span data-ttu-id="d6b80-110">> Hardwarestation-Profile.</span><span class="sxs-lookup"><span data-stu-id="d6b80-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="d6b80-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d6b80-111">Click New.</span></span>
3. <span data-ttu-id="d6b80-112">Geben Sie im Hardwarestation-Kennungsfeld "TestHWProfile" ein.</span><span class="sxs-lookup"><span data-stu-id="d6b80-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="d6b80-113">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d6b80-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d6b80-114">Geben Sie im Feld "Portnummer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="d6b80-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="d6b80-115">Klicken Sie im Feld "Hardwareprofil" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d6b80-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d6b80-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d6b80-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d6b80-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6b80-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d6b80-118">Klicken Sie im Feld "Paketname" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d6b80-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d6b80-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6b80-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d6b80-120">Dies ist das Standardpaket, das mit einer neuen Umgebung kommt.</span><span class="sxs-lookup"><span data-stu-id="d6b80-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="d6b80-121">Die Versionsnummer kann variieren.</span><span class="sxs-lookup"><span data-stu-id="d6b80-121">The version number may vary.</span></span>  
11. <span data-ttu-id="d6b80-122">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="d6b80-122">Click Save.</span></span>
12. <span data-ttu-id="d6b80-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="d6b80-123">Close the page.</span></span>
13. <span data-ttu-id="d6b80-124">Navigieren Sie zu Einzelhandel und Commerce > Kanäle > Alle Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="d6b80-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="d6b80-125">Wählen Sie in der Liste die Zeile "17" aus.</span><span class="sxs-lookup"><span data-stu-id="d6b80-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="d6b80-126">Wenn Sie das USRT-Demodatenunternehmen verwenden, ist dies der Houston-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d6b80-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="d6b80-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6b80-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="d6b80-128">Schalten Sie die Erweiterung des Abschnitts "Hardwarestationen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="d6b80-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="d6b80-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6b80-129">Click Add.</span></span>
18. <span data-ttu-id="d6b80-130">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6b80-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="d6b80-131">Klicken Sie im Feld "Profilkennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d6b80-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="d6b80-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="d6b80-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6b80-133">Dies muss das neue Hardwarestationsprofil sein, das in den vorherigen Schritten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6b80-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="d6b80-134">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="d6b80-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d6b80-135">Geben Sie im Feld "Hostname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d6b80-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="d6b80-136">Geben Sie einen Wert in das Feld "Terminalkennung für Überweisung (elektronisch)" ein.</span><span class="sxs-lookup"><span data-stu-id="d6b80-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="d6b80-137">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="d6b80-137">Click Save.</span></span>

