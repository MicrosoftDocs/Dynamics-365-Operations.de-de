--- 
title: "Bücher einrichten"
description: Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen.
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: b18f52254b9073cd95bf50539a4414598a8c19cc
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-books"></a><span data-ttu-id="741cd-103">Bücher einrichten</span><span class="sxs-lookup"><span data-stu-id="741cd-103">Set up books</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="741cd-104">Die folgende Prozedur zeigt, wie Sie ein neues Abschreibungsbuch erstellen und es einer Anlagengruppe zuordnen.</span><span class="sxs-lookup"><span data-stu-id="741cd-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="741cd-105">Dabei werden die Buchhalterrolle und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="741cd-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="741cd-106">Buch erstellen</span><span class="sxs-lookup"><span data-stu-id="741cd-106">Create a book</span></span>
1. <span data-ttu-id="741cd-107">Wechseln Sie zu "Anlagen" > "Einstellungen" > "Bücher".</span><span class="sxs-lookup"><span data-stu-id="741cd-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="741cd-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="741cd-108">Click New.</span></span>
3. <span data-ttu-id="741cd-109">Geben Sie im Feld 'Buch' einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="741cd-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="741cd-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="741cd-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="741cd-111">Wenn "Abschreibung berechnen" ausgewählt ist, werden die zugeordneten Anlagenbuch in die Abschreibungsvorschläge einbezogen.</span><span class="sxs-lookup"><span data-stu-id="741cd-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="741cd-112">Wenn dies nicht ausgewählt ist, wird die Anlagebuch nicht automatisch abgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="741cd-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="741cd-113">Wählen Sie "Ja" im Feld "Ermittelte Abschreibung" aus.</span><span class="sxs-lookup"><span data-stu-id="741cd-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="741cd-114">Geben Sie im Feld 'Abschreibungsprofil' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="741cd-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="741cd-115">Ein alternatives Abschreibungsprofil ist auch als eine Switchover-Methode der Abschreibung bekannt.</span><span class="sxs-lookup"><span data-stu-id="741cd-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="741cd-116">Der Abschreibungsvorschlag schaltet auf dieses Profil um, wenn das alternative Profil einen Abschreibungsbetrag berechnet, der gleich oder größer ist, als das standardmäßiges "Abschreibungsprofil".</span><span class="sxs-lookup"><span data-stu-id="741cd-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="741cd-117">Das "Außerordentliche Abschreibungsprofil" wird für die zusätzliche Abschreibung einer Anlage unter besonderen Umständen verwendet.</span><span class="sxs-lookup"><span data-stu-id="741cd-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="741cd-118">Sie können dieses Profil z. B. verwenden, um eine Abschreibung in Folge einer Naturkatastrophe zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="741cd-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="741cd-119">Wenn die Option "Abschreibungsregulierungen mit Basisregulierungen erstellen" ausgewählt ist, werden Abschreibungsregulierungen automatisch erstellt, wenn der Wert einer Anlage aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="741cd-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="741cd-120">Wenn sie nicht ausgewählt ist, wird der aktualisierte Anlagewert sich nur auf die Abschreibungsberechnungen ausgehend vom heutigen Datum auswirken.</span><span class="sxs-lookup"><span data-stu-id="741cd-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="741cd-121">Wählen Sie "Ja" im Feld "Abschreibungsregulierungen mit Basisregulierungen erstellen".</span><span class="sxs-lookup"><span data-stu-id="741cd-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="741cd-122">Standardmäßig werden Anlagenbuchtransaktionen im Hauptbuch gebucht.</span><span class="sxs-lookup"><span data-stu-id="741cd-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="741cd-123">Sie können Buchungen im Hauptbuch für das Buch deaktivieren, indem Sie das Feld "Ins Hauptbuch buchen" auf Nein festlegen.</span><span class="sxs-lookup"><span data-stu-id="741cd-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="741cd-124">Bücher, die nicht im Hauptbuch buchen, werden in der Regel für die Steuererklärung verwendet.</span><span class="sxs-lookup"><span data-stu-id="741cd-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="741cd-125">Dies bietet zusätzliche Flexibilität zur Löschung von historischen Buchungen für das Anlagenbuch, da sie nicht im Hauptbuch eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="741cd-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="741cd-126">Die Buchungsebene wird standardmäßig auf die aktuellen Ebene festgelegt, wenn das Buch im Hauptbuch bucht, und auf "Keine", wenn es nicht im Hauptbuch bucht.</span><span class="sxs-lookup"><span data-stu-id="741cd-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="741cd-127">Aktualisieren Sie die "Buchungsebene", wenn Sie benötigen, dass Transaktionen für dieses Buch zu einer anderen Ebene gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="741cd-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="741cd-128">Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="741cd-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="741cd-129">Abgeleitete Bücher buchen Translationen für verschiedene Bücher gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="741cd-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="741cd-130">Sie erstellen die Buchungen mit dem primären Buch und während der Buchung wird eine genaue Kopie der Buchung im abgeleiteten Abschreibungsbuch gebucht.</span><span class="sxs-lookup"><span data-stu-id="741cd-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="741cd-131">Es gibt keine Neuberechnung bei den Transaktionen im abgeleiteten Buch. Sie sollten diese nicht für Abschreibungsbuchungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="741cd-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="741cd-132">Buch einer Anlagengruppe zuordnen</span><span class="sxs-lookup"><span data-stu-id="741cd-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="741cd-133">Klicken Sie auf "Anlagengruppen".</span><span class="sxs-lookup"><span data-stu-id="741cd-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="741cd-134">Geben Sie im Feld "Anlagengruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="741cd-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="741cd-135">Geben Sie im Feld "Nutzungsdauer" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="741cd-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="741cd-136">Beachten Sie, dass Abschreibungszeiträume nach der Festlegung der Nutzungsdauer berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="741cd-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="741cd-137">Sie können die Abschreibungskonvention für Steuerzwecke bei Bedarf festlegen.</span><span class="sxs-lookup"><span data-stu-id="741cd-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


