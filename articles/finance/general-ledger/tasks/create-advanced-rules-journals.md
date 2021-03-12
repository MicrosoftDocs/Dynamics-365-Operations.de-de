---
title: Erweiterte Regeln für Erfassungen erstellen
description: Dieses Verfahrens zeigt das Erstellen von erweiterten Regeln für Erfassungen.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c06855c7a7648c5829b90bc548a7d2e400967698
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988601"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="dcf2a-103">Erweiterte Regeln für Erfassungen erstellen</span><span class="sxs-lookup"><span data-stu-id="dcf2a-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcf2a-104">Dieses Verfahrens zeigt das Erstellen von erweiterten Regeln für Erfassungen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="dcf2a-105">Hierzu zählen die Einrichtung Erfassungssteuerungs- und Benutzerbuchungseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="dcf2a-106">Für diese Prozedur wird das Demo-Datenunternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="dcf2a-107">Einrichten der Erfassungskontrolle</span><span class="sxs-lookup"><span data-stu-id="dcf2a-107">Set up journal control</span></span>
1. <span data-ttu-id="dcf2a-108">Wechseln Sie im **Navigationsbereich** zu **Module > Hauptbuch > Erfassungseinstellungen > Journale**.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="dcf2a-109">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dcf2a-110">Klicken Sie im **Aktivitätsbereich** auf **Erfassungssteuerung**.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="dcf2a-111">Klicken Sie im Inforegister **Welche Kontenarten können gebucht werden** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="dcf2a-112">Klicken Sie im Feld **Unternehmenskonten** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dcf2a-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="dcf2a-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="dcf2a-115">Klicken Sie im Inforegister **Welche Segmentwerte sind für diese Erfassung gültig** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="dcf2a-116">Klicken Sie im Feld **Kontostruktur** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dcf2a-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="dcf2a-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dcf2a-119">Klicken Sie im Feld **Segment** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="dcf2a-120">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="dcf2a-121">Klicken Sie im Feld **Von Wert** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="dcf2a-122">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="dcf2a-123">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="dcf2a-124">Klicken Sie im Feld **Bis Wert** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="dcf2a-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="dcf2a-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="dcf2a-127">Einrichten von Buchungseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="dcf2a-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="dcf2a-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-128">Close the page.</span></span>
2. <span data-ttu-id="dcf2a-129">Klicken Sie auf **Buchungseinschränkungen**.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="dcf2a-130">Wählen Sie im Feld **Wie möchten Sie Buchungseinschränkungen einrichten?** die Option 'Nach Benutzergruppe' aus.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="dcf2a-131">In der Struktur überprüfen Sie die Gruppe, der Sie die Buchung für diesen Erfassungsnamen gestatten möchten.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="dcf2a-132">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dcf2a-132">Click **OK**.</span></span>

