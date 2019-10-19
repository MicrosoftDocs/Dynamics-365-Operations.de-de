---
title: Anlagenabschreibung
description: Dieser Artikel enthält eine Übersicht der Abschreibung von Anlagen.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1056dadab4294072cc064670f5cfcda239e22e19
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177895"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="1dea2-103">Anlagenabschreibung</span><span class="sxs-lookup"><span data-stu-id="1dea2-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dea2-104">Dieser Artikel enthält eine Übersicht der Abschreibung von Anlagen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="1dea2-105">Eine Abschreibung ist eine periodische Buchung, die normalerweise den Wert des Anlagevermögens in der Bilanz verringert und in einem Gewinn- und Verlustkonto als Ausgabe gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="1dea2-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="1dea2-106">Folglich wird ein Hauptkonto normalerweise für die periodische Abschreibung in der Bilanz verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dea2-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="1dea2-107">Ein Gegenkonto ist ein Konto im Gewinn- und Verlustteil des Kontenplans.</span><span class="sxs-lookup"><span data-stu-id="1dea2-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="1dea2-108">Abschreibungsregulierung</span><span class="sxs-lookup"><span data-stu-id="1dea2-108">Depreciation adjustment</span></span>
<span data-ttu-id="1dea2-109">Normalerweise wird nur eine Korrektur an einer bereits gebuchten Abschreibungsbuchung als Abschreibungsanpassung gebucht.</span><span class="sxs-lookup"><span data-stu-id="1dea2-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="1dea2-110">Daher werden das Hauptkonto und das Gegenkonto ebenso wie die Konten für die Abschreibung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="1dea2-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="1dea2-111">Bei einer Abschreibungsanpassung kann es sich um einen positiven oder einen negativen Betrag handeln, jedoch bleiben das Hauptkonto (als Bilanzkonto) und das Gegenkonto (normalerweise als Gewinn- und Verlustkonto) funktionell gleich.</span><span class="sxs-lookup"><span data-stu-id="1dea2-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="1dea2-112">Außerordentliche Abschreibung</span><span class="sxs-lookup"><span data-stu-id="1dea2-112">Extraordinary depreciation</span></span>
<span data-ttu-id="1dea2-113">Außerordentliche Abschreibungen funktionieren wie normale Abschreibungen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="1dea2-114">Folglich wird ein Hauptkonto verwendet, um den Abschreibungsbetrag in der Bilanz zu buchen und den Wert der Anlage zu verringern.</span><span class="sxs-lookup"><span data-stu-id="1dea2-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="1dea2-115">Ein Gegenkonto ist ein GuV-Konto, in dem die Abschreibung, die für das Geschäftsjahr berechnet wird, als Ausgabe berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="1dea2-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="1dea2-116">Eine außerordentliche Abschreibung ist von der grundlegenden Abschreibung unabhängig.</span><span class="sxs-lookup"><span data-stu-id="1dea2-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="1dea2-117">Wurde die außerordentliche Abschreibung als separate Buchungsart eingerichtet, kann die außerordentliche Abschreibung getrennt von der normalen grundlegenden Abschreibung gebucht und gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="1dea2-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="1dea2-118">Sonderabschreibung</span><span class="sxs-lookup"><span data-stu-id="1dea2-118">Special depreciation allowance</span></span>
<span data-ttu-id="1dea2-119">Die Sonderabschreibung ermöglicht Ihnen, im ersten Jahr der Inbetriebnahme und Abschreibung einer Anlage zusätzliche Abschreibungsbeträge geltend zu machen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="1dea2-120">Die Sonderabschreibung muss vor jeder anderen Abschreibungsberechnung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1dea2-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="1dea2-121">Da Sonderabschreibungen bis vor kurzem für die Nutzungsdauer der Anlage unbekannt waren, empfiehlt es sich, diese Art Abschreibungsbetrag mit einem Buch zu verwenden, mit dem nicht im Hauptbuch gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="1dea2-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="1dea2-122">Mithilfe der Funktion "Buchungen löschen, die nicht im Hauptbuch gebucht werden" können Sie historische Transaktionen für diese Bücher löschen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="1dea2-123">Sie können die Abschreibungshistorie zum Anlagenbuch dann löschen, buchen die Sonderabschreibung, wenn dieses bekannt hat, und die restlichen Abschreibungsbuchungen für das Jahr dann buchen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="1dea2-124">Sie können eine unbegrenzte Anzahl von Datensätzen für die Sonderabschreibung erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="1dea2-125">Nach deren Zuordnung zu einem Anlagengruppenbuch werden sie auf das Anlagenbuch angewendet.</span><span class="sxs-lookup"><span data-stu-id="1dea2-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="1dea2-126">Die Sonderabschreibung wird entweder als Prozentsatz oder als fester Wert eingegeben.</span><span class="sxs-lookup"><span data-stu-id="1dea2-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="1dea2-127">Beim Buchen von Abschreibungsvorschlägen werden Buchungen für Sonderabschreibungen im Abschreibungsbuch getrennt von Abschreibungsbuchungen erfasst.</span><span class="sxs-lookup"><span data-stu-id="1dea2-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="1dea2-128">Abschreibungskalender</span><span class="sxs-lookup"><span data-stu-id="1dea2-128">Depreciation calendars</span></span>
<span data-ttu-id="1dea2-129">Jedes Abschreibungsbuch hat einen Kalender, der verwendet wird, wenn Sie Anlagen abschreiben.</span><span class="sxs-lookup"><span data-stu-id="1dea2-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="1dea2-130">Das Buch verwendet standardmäßig den Sachkontosteuerkalender, wenn Sie keinen Kalender angeben.</span><span class="sxs-lookup"><span data-stu-id="1dea2-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="1dea2-131">Sie müssen einen Steuerkalender für ein Buch auswählen, wenn das entsprechende Abschreibungsprofil des Buchs ein steuerlich relevantes Abschreibungsjahr verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dea2-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="1dea2-132">Sie können freigegebene Kalender mithilfe der Seite **Steuerkalender**im Hauptbuch erstellen.</span><span class="sxs-lookup"><span data-stu-id="1dea2-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="1dea2-133">Weitere Informationen finden Sie untere [Abschreibungsmethoden und - konventionen](depreciation-methods-conventions.md). </span><span class="sxs-lookup"><span data-stu-id="1dea2-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



