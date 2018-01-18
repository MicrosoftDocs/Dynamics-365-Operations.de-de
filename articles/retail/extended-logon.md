---
title: "Einrichten der erweiterten Anmeldungfunktionalität für Cloud POS und MPOS"
description: "Dieses Thema behandelt die Optionen für die Einrichtung der erweiterten Anmeldung für Cloud-POS und Retail Modern POS (MPOS)."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 7547ff6dcea546100a11f20e8e8f7f7fcab82cee
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="cfe63-103">Einrichten der erweiterten Anmeldungfunktionalität für Cloud POS und MPOS</span><span class="sxs-lookup"><span data-stu-id="cfe63-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="cfe63-104">Dieses Thema behandelt die Optionen für die Einrichtung der erweiterten Anmeldung für Cloud-POS und Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="cfe63-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

<a name="setting-up-extended-logon"></a><span data-ttu-id="cfe63-105">Einrichten der erweiterten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-105">Setting up extended logon</span></span>
=========================

<span data-ttu-id="cfe63-106">Sie können die Einstellungen für Strichcodemasken unter **Einzelhandel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile** &gt; **Funktionsprofile** finden.</span><span class="sxs-lookup"><span data-stu-id="cfe63-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="cfe63-107">Das Inforegister **Funktionen** umfasst folgende Optionen, die der erweiterten Anmeldung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cfe63-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="cfe63-108">Personal-Strichcodeanmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-108">Staff bar code logon</span></span>

<span data-ttu-id="cfe63-109">Wenn die Option **Personal-Strichcodeanmeldung** aktiviert ist, können Arbeitskräfte, deren POS-Anmeldeinformationen die erweiterte Anmeldung zugewiesen ist, sich mit einem Strichcode anmelden.</span><span class="sxs-lookup"><span data-stu-id="cfe63-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="cfe63-110">Personalanmeldung mit Strichcode erfordert Kennwort.</span><span class="sxs-lookup"><span data-stu-id="cfe63-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="cfe63-111">Wenn die Option **Personalanmeldung mit Strichcode erfordert Kennwort** aktiviert ist, wird bei der Personalanmeldung mit Strichode nur die Arbeitskraft ausgewählt, die der angegebenen erweiterten Anmeldung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cfe63-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="cfe63-112">Arbeitskräfte müssen noch eigene Kennwörter eingeben, wenn diese Option aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cfe63-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="cfe63-113">Personalkartenanmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-113">Staff card logon</span></span>

<span data-ttu-id="cfe63-114">Wenn die Option **Personalkartenanmeldung** aktiviert ist, können Arbeitskräfte, deren POS-Anmeldeinformationen die erweiterte Anmeldung zugewiesen ist, sich mit einem Magnetstreifen anmelden.</span><span class="sxs-lookup"><span data-stu-id="cfe63-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="cfe63-115">Personalanmeldung mit Karte erfordert Kennwort.</span><span class="sxs-lookup"><span data-stu-id="cfe63-115">Staff card logon requires password</span></span>

<span data-ttu-id="cfe63-116">Wenn die Option **Personalanmeldung mit Karte erfordert Kennwort** aktiviert ist, wird bei der Personalanmeldung mit Karte nur die Arbeitskraft ausgewählt, die der angegebenen erweiterten Anmeldung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cfe63-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="cfe63-117">Arbeitskräfte müssen noch eigene Kennwörter eingeben, wenn diese Option aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cfe63-117">Workers must still enter their password when this option is enabled.</span></span>

<a name="assigning-an-extended-logon"></a><span data-ttu-id="cfe63-118">Zuweisen einer erweiterten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-118">Assigning an extended logon</span></span>
===========================

<span data-ttu-id="cfe63-119">Standardmäßig können nur Manager die erweiterte Anmeldung den Arbeitskräften zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cfe63-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="cfe63-120">Um erweiterte Anmeldung zuzuweisen, fahren Sie mit **Erweiterte Anmeldung** in POS fort.</span><span class="sxs-lookup"><span data-stu-id="cfe63-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="cfe63-121">Suchen Sie dann nach einer Arbeitskraft nach Eingabe der Kennung in der Auswahlliste.</span><span class="sxs-lookup"><span data-stu-id="cfe63-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="cfe63-122">Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="cfe63-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="cfe63-123">Auf der nächsten Seite ziehen Sie die Karte durch das Lesegerät oder scannen Sie die Karte, um der Arbeitskraft die erweiterte Anmeldung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="cfe63-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="cfe63-124">Wenn der Vorgang erfolgreich war, wird die Schaltfläche **OK** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfe63-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="cfe63-125">Klicken Sie auf **OK**, um die erweiterten Anmeldung für diese Arbeitskraft zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cfe63-125">Click **OK** to save the extended logon for that worker.</span></span>

<a name="deleting-an-extended-logon"></a><span data-ttu-id="cfe63-126">Löschen einer erweiterten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-126">Deleting an extended logon</span></span>
==========================

<span data-ttu-id="cfe63-127">Um die erweiterte Anmeldung zu löschen, die einer Arbeitskraft zugewiesen wurde, suchen Sie die Arbeitskraft, indem Sie den Vorgang **Erweiterte Anmeldung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="cfe63-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="cfe63-128">Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisung aufheben**.</span><span class="sxs-lookup"><span data-stu-id="cfe63-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="cfe63-129">Alle erweiterten Anmeldeinformationen, die dieser Arbeitskraft zugeordnet sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="cfe63-129">All extended logon credentials that are associated with that worker are removed.</span></span>

<a name="extending-extended-logon"></a><span data-ttu-id="cfe63-130">Erweitern der erweiterten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-130">Extending extended logon</span></span>
========================

<span data-ttu-id="cfe63-131">Der Anmeldedienst kann erweitert werden, um zusätzliche Geräte für die erweiterte Anmeldung zu unterstützen, z.B. Handflächenscanner.</span><span class="sxs-lookup"><span data-stu-id="cfe63-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="cfe63-132">Weitere Informationen finden Sie in der Dokumentation zur Erweiterbarkeit des POS.</span><span class="sxs-lookup"><span data-stu-id="cfe63-132">For more information, see the POS extensibility documentation.</span></span>

<a name="using-extended-logon"></a><span data-ttu-id="cfe63-133">Verwenden der erweiterten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="cfe63-133">Using extended logon</span></span>
====================

<span data-ttu-id="cfe63-134">Wenn die erweiterte Anmeldung konfiguriert ist und einer Arbeitskraft ein Strichcode oder ein Magnetstreifen zugewiesen wurde, muss die Arbeitskraft seine Karte nur Karte durch ein Lesegerät ziehen, wenn die POS-Anmeldeseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cfe63-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="cfe63-135">Wenn auch ein Kennwort erforderlich ist, damit die Anmeldung durchgeführt werden kann, wird die Arbeitskraft aufgefordert, das Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="cfe63-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>




