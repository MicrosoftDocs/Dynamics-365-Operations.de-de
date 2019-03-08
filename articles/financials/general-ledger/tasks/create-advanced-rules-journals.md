---
title: Erweiterte Regeln für Erfassungen erstellen
description: Dieses Verfahrens zeigt das Erstellen von erweiterten Regeln für Erfassungen.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326169"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="8527f-103">Erweiterte Regeln für Erfassungen erstellen</span><span class="sxs-lookup"><span data-stu-id="8527f-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8527f-104">Dieses Verfahrens zeigt das Erstellen von erweiterten Regeln für Erfassungen.</span><span class="sxs-lookup"><span data-stu-id="8527f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="8527f-105">Hierzu zählen die Einrichtung Erfassungssteuerungs- und Benutzerbuchungseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="8527f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="8527f-106">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="8527f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="8527f-107">Einrichten der Erfassungskontrolle</span><span class="sxs-lookup"><span data-stu-id="8527f-107">Set up journal control</span></span>
1. <span data-ttu-id="8527f-108">Wechseln Sie zu "Hauptbuch" > "Erfassung einrichten" >"Erfassungsnamen".</span><span class="sxs-lookup"><span data-stu-id="8527f-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="8527f-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8527f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8527f-110">Klicken Sie auf "Erfassungssteuerung".</span><span class="sxs-lookup"><span data-stu-id="8527f-110">Click Journal control.</span></span>
4. <span data-ttu-id="8527f-111">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8527f-111">Click Add.</span></span>
5. <span data-ttu-id="8527f-112">Klicken Sie im Feld "Unternehmenskonten" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8527f-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8527f-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8527f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8527f-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8527f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8527f-115">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8527f-115">Click Add.</span></span>
9. <span data-ttu-id="8527f-116">Klicken Sie im Feld "Kontenstruktur" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8527f-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8527f-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8527f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="8527f-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8527f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8527f-119">Klicken Sie im Feld "Segment" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8527f-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="8527f-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8527f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8527f-121">Klicken Sie im Feld "Von" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8527f-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8527f-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8527f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="8527f-123">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8527f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="8527f-124">Klicken Sie im Feld "Bis" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8527f-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="8527f-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="8527f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="8527f-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="8527f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="8527f-127">Einrichten von Buchungseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="8527f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="8527f-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8527f-128">Close the page.</span></span>
2. <span data-ttu-id="8527f-129">Klicken Sie auf "Buchungseinschränkungen".</span><span class="sxs-lookup"><span data-stu-id="8527f-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="8527f-130">Wählen Sie im Feld "Wie möchten Sie Buchungseinschränkungen einrichten?" die Option "Nach Benutzer" aus.</span><span class="sxs-lookup"><span data-stu-id="8527f-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="8527f-131">In der Struktur überprüfen Sie die Gruppe, der Sie die Buchung für diesen Erfassungsnamen gestatten möchten.</span><span class="sxs-lookup"><span data-stu-id="8527f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="8527f-132">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="8527f-132">Click OK.</span></span>

