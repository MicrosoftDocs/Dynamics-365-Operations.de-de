---
title: Bankgarantien
description: "Dieser Artikel enthält Informationen zu Garantiebriefen. Ein Garantiebrief ist eine Einverständniserklärung seitens einer Bank, einen bestimmten Geldbetrag an eine andere Person zu zahlen, falls seitens eines Debitors der Bank eine regelmäßige Zahlungsverpflichtung gegenüber dieser Person besteht."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c2072c571d584185e867f221c24dc44cdbad1dd6
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="letters-of-guarantee"></a><span data-ttu-id="27b16-104">Bankgarantien</span><span class="sxs-lookup"><span data-stu-id="27b16-104">Letters of guarantee</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27b16-105">Dieser Artikel enthält Informationen zu Garantiebriefen.</span><span class="sxs-lookup"><span data-stu-id="27b16-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="27b16-106">Ein Garantiebrief ist eine Einverständniserklärung seitens einer Bank, einen bestimmten Geldbetrag an eine andere Person zu zahlen, falls seitens eines Debitors der Bank eine regelmäßige Zahlungsverpflichtung gegenüber dieser Person besteht.</span><span class="sxs-lookup"><span data-stu-id="27b16-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="27b16-107">Ein Garantiebrief ist eine Einverständniserklärung seitens einer Bank (der Bürge), einen bestimmten Geldbetrag an eine andere Person zu zahlen (den Begünstigten), falls seitens eines Debitors der Bank (der Auftraggeber) eine regelmäßige Zahlungsverpflichtung gegenüber dem Begünstigten besteht.</span><span class="sxs-lookup"><span data-stu-id="27b16-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="27b16-108">Garantiebriefe sind nicht übertragbar.</span><span class="sxs-lookup"><span data-stu-id="27b16-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="27b16-109">Sie richten sich nur an den Begünstigten, der in der Vereinbarung benennt wird.</span><span class="sxs-lookup"><span data-stu-id="27b16-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="27b16-110">Der Auftraggeber kann im Rahmen der Bedingungen der Vereinbarung eine Erhöhung oder Verringerung des Werts eines Garantiebriefs fordern.</span><span class="sxs-lookup"><span data-stu-id="27b16-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="27b16-111">Um einen Garantiebrief zu liquidieren, muss der Begünstigte den ursprünglichen Garantiebrief übermitteln und die Bank vor dem Ablaufdatum von der regelmäßigen Zahlungsverpflichtung seitens des Auftraggebers unterrichten.</span><span class="sxs-lookup"><span data-stu-id="27b16-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="27b16-112">Die Bank zahlt den fälligen Betrag anschließend gemäß der Vereinbarung im Garantiebrief auf das Konto des Begünstigten.</span><span class="sxs-lookup"><span data-stu-id="27b16-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="27b16-113">Die Bank reserviert einen Anteil der Zahlung als Gewinnspanne.</span><span class="sxs-lookup"><span data-stu-id="27b16-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="27b16-114">Der Prozentsatz wird vereinbart und in den Vereinbarungsbedingungen angegeben.</span><span class="sxs-lookup"><span data-stu-id="27b16-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="27b16-115">Sie können einen Code erstellen, um den Zweck eines Garantiebriefs nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="27b16-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="27b16-116">Sie können auch die Gründe angeben, die einem Garantiebrief zugeordnet werden, wenn der Brief storniert wird.</span><span class="sxs-lookup"><span data-stu-id="27b16-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="27b16-117">Sie können die Zweckcodes und die Gründe der Bank auf den Seiten **Zahlungszweckcode** den **Ursachen für Bankbuchungen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="27b16-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="27b16-118">Verwenden Sie die Seite **Garantiebrief**, um die folgenden Aufgaben durchführen:</span><span class="sxs-lookup"><span data-stu-id="27b16-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="27b16-119">Erstellen von korrekten Sachkontoeinträgen und Löschen von manuellen Eingaben.</span><span class="sxs-lookup"><span data-stu-id="27b16-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="27b16-120">Erfassen aller geld- und nicht geldbezogenen Transaktionen und Nachverfolgung der Garantiebriefsalden.</span><span class="sxs-lookup"><span data-stu-id="27b16-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="27b16-121">Erfassen und Nachverfolgen des Status und des Ablaufdatums des Garantiebriefs.</span><span class="sxs-lookup"><span data-stu-id="27b16-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="27b16-122">Generieren eines Berichts, in dem die Banken aufgeführt sind, die Garantiebriefe besitzen.</span><span class="sxs-lookup"><span data-stu-id="27b16-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="27b16-123">In der folgenden Tabelle werden die Aktivitäten beschrieben, die mit einem Garantiebrief ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="27b16-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="27b16-124">Aktion</span><span class="sxs-lookup"><span data-stu-id="27b16-124">Action</span></span>              | <span data-ttu-id="27b16-125">Verwendungszweck</span><span class="sxs-lookup"><span data-stu-id="27b16-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27b16-126">An Bank übermitteln</span><span class="sxs-lookup"><span data-stu-id="27b16-126">Submit to bank</span></span>      | <span data-ttu-id="27b16-127">Übermittlung der Garantiebriefanforderung an die Bank.</span><span class="sxs-lookup"><span data-stu-id="27b16-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="27b16-128">Empfang von der Bank</span><span class="sxs-lookup"><span data-stu-id="27b16-128">Receive from bank</span></span>   | <span data-ttu-id="27b16-129">Nachdem die Bank die übermittelte Anforderung bestätigt hat, wird der Garantiebrief bei der Bank einkassiert.</span><span class="sxs-lookup"><span data-stu-id="27b16-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="27b16-130">Übergabe an den Begünstigten</span><span class="sxs-lookup"><span data-stu-id="27b16-130">Give to beneficiary</span></span> | <span data-ttu-id="27b16-131">Wenn Sie den Garantiebrief von der Bank erhalten haben, übergeben Sie den Garantiebrief an den Begünstigten.</span><span class="sxs-lookup"><span data-stu-id="27b16-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="27b16-132">Erhöhung des Werts</span><span class="sxs-lookup"><span data-stu-id="27b16-132">Increase value</span></span>      | <span data-ttu-id="27b16-133">Wenn der Begünstigte und der Auftraggeber eine entsprechende Vereinbarung treffen, kann der Geldwert erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="27b16-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="27b16-134">Verringerung des Werts</span><span class="sxs-lookup"><span data-stu-id="27b16-134">Decrease value</span></span>      | <span data-ttu-id="27b16-135">Wenn der Begünstigte und der Auftraggeber eine entsprechende Vereinbarung treffen, kann der Geldwert verringert werden.</span><span class="sxs-lookup"><span data-stu-id="27b16-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="27b16-136">Verlängern</span><span class="sxs-lookup"><span data-stu-id="27b16-136">Extend</span></span>              | <span data-ttu-id="27b16-137">Wenn Sie den Garantiebrief an den Begünstigten übergeben haben, verlängern Sie ggf. die Gültigkeitsdauer.</span><span class="sxs-lookup"><span data-stu-id="27b16-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="27b16-138">Stornieren</span><span class="sxs-lookup"><span data-stu-id="27b16-138">Cancel</span></span>              | <span data-ttu-id="27b16-139">Wenn der Zweck, zu dem der Garantiebrief angefordert wurde, nicht mehr zutrifft, stornieren Sie die Vereinbarung.</span><span class="sxs-lookup"><span data-stu-id="27b16-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="27b16-140">Tilgen</span><span class="sxs-lookup"><span data-stu-id="27b16-140">Liquidate</span></span>           | <span data-ttu-id="27b16-141">Wenn der Begünstigte den Garantiebrief bei der Bank vorlegt, kann dieser Garantiebrief liquidiert werden.</span><span class="sxs-lookup"><span data-stu-id="27b16-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="27b16-142">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="27b16-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="27b16-143">Bankgarantiebuchung</span><span class="sxs-lookup"><span data-stu-id="27b16-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="27b16-144">Bankfazilitäten und Buchungsprofile für Bankgarantie einrichten</span><span class="sxs-lookup"><span data-stu-id="27b16-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)



