--- 
title: " POS-Berechtigungsgruppen erstellen"
description: Diese Prozedur zeigt, wie eine POS-Berechtigungsgruppe erstellt wird.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e924dc59c3e4cb9b6979014852512453dd3d70db
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="fc538-103"> POS-Berechtigungsgruppen erstellen</span><span class="sxs-lookup"><span data-stu-id="fc538-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fc538-104">Diese Prozedur zeigt, wie eine POS-Berechtigungsgruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fc538-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="fc538-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USRT.</span><span class="sxs-lookup"><span data-stu-id="fc538-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="fc538-106">Diese Aufgabe ist für die Rolle "Bereichsleiter (Einzelhandel)" vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="fc538-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="fc538-107">Gehen Sie zu "Berechtigungsgruppen".</span><span class="sxs-lookup"><span data-stu-id="fc538-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="fc538-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="fc538-108">Click New.</span></span>
3. <span data-ttu-id="fc538-109">Geben Sie im Feld "POS-Berechtigungsgruppenkennung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc538-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="fc538-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fc538-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fc538-111">Wählen Sie "Ja" im Feld "Zeiterfassungseinträge anzeigen" aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="fc538-112">Sie können verschiedene Berechtigungen für Ihre POS-Berechtigungsgruppe jetzt aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fc538-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="fc538-113">Bei einigen Berechtigungen können Sie einen Wert festlegen, der verwendet wird, wenn überprüft werden soll, ob der POS-Benutzer die Aktivität ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="fc538-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="fc538-114">Dieses Aufgabenhandbuch ermöglicht einige Berechtigungen, die einem Kassierer zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fc538-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="fc538-115">Wählen Sie "Ja" im Feld "Auftragserstellung zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="fc538-116">Wählen Sie "Ja" im Feld "Auftragsbearbeitung zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="fc538-117">Wählen Sie "Ja" im Feld "Auftragsabruf zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="fc538-118">Wählen Sie "Ja" im Feld "Kennwortänderung zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="fc538-119">Wählen Sie "Ja" im Feld "Blindschließen zulassen" aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="fc538-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc538-120">Click Save.</span></span>
    * <span data-ttu-id="fc538-121">Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Einzelhandelskanäle zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="fc538-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="fc538-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="fc538-122">Close the page.</span></span>
13. <span data-ttu-id="fc538-123">Gehen Sie zu "Einzelvorgänge".</span><span class="sxs-lookup"><span data-stu-id="fc538-123">Go to Jobs.</span></span>
    * <span data-ttu-id="fc538-124">Danach weisen wir die POS-Berechtigungsgruppe einem Einzelvorgang zu.</span><span class="sxs-lookup"><span data-stu-id="fc538-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="fc538-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="fc538-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="fc538-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="fc538-127">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fc538-127">Click Edit.</span></span>
17. <span data-ttu-id="fc538-128">Erweitern Sie den Einzelvorgangsklassifizierungs-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="fc538-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="fc538-129">Geben Sie im Feld "POS-Berechtigungsgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="fc538-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="fc538-130">Alle Arbeitskräfte in Positionen für diesen Einzelvorgang werden die Einstellungen dieser POS-Berechtigungsgruppe verwenden, es sei denn, die POS-Berechtigungen dieser Arbeitskräfte wurden in ihrer Positionsebene überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc538-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="fc538-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="fc538-131">Click Save.</span></span>
    * <span data-ttu-id="fc538-132">Nachdem die Änderungen gespeichert sind, müssen Sie den Mitarbeiterverteilungszeitplan ausführen, um die Änderungen an Einzelhandelskanäle zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="fc538-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


