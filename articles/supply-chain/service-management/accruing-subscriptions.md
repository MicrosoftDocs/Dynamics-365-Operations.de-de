---
title: Antizipieren von Daueraufträgen
description: Mithilfe von Servicedaueraufträgen werden Umsatzerlöse ab dem Datum, an dem eine Gebührenbuchung fakturiert wurde, manuell abgegrenzt.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ebd65655db56ee1169f24dbc79fbfb5130f06a5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428657"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="cf00b-103">Antizipieren von Daueraufträgen</span><span class="sxs-lookup"><span data-stu-id="cf00b-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cf00b-104">Mithilfe von Servicedaueraufträgen werden Umsatzerlöse ab dem Datum, an dem eine Gebührenbuchung fakturiert wurde, manuell abgegrenzt.</span><span class="sxs-lookup"><span data-stu-id="cf00b-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="cf00b-105">Abgrenzungsperioden werden für die Rechnungsperiode erstellt, die für die Dauerauftragsgebühr eingerichtet wurde, und basieren auf dem Periodencode des Dauerauftrags.</span><span class="sxs-lookup"><span data-stu-id="cf00b-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="cf00b-106">Antizipierter Umsatzerlös kann abgegrenzt oder zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="cf00b-107">Zurücksetzen von Abgrenzungen von Habenbeträgen</span><span class="sxs-lookup"><span data-stu-id="cf00b-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="cf00b-108">Bei einer Gutschrift bereits fakturierter Dauerauftragsbeträge stehen Ihnen drei verschiedene Methoden zur Verfügung, um die Abgrenzungsbeträge zurückzusetzen:</span><span class="sxs-lookup"><span data-stu-id="cf00b-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="cf00b-109">Die antizipierten Umsatzerlösbuchungen können vor dem Erstellen des Gutschriftvorschlags einzeln für die Buchung zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="cf00b-110">Dies ist die manuelle Methode.</span><span class="sxs-lookup"><span data-stu-id="cf00b-110">This is the manual method.</span></span> <span data-ttu-id="cf00b-111">(manuell)</span><span class="sxs-lookup"><span data-stu-id="cf00b-111">(manual)</span></span>

  - <span data-ttu-id="cf00b-112">Sie können die abgegrenzten Beträge an dem Datum, an dem die Gutschrift gebucht wird, oder am ursprünglichen Buchungsdatum der Abgrenzung zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="cf00b-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="cf00b-113">Weitere Informationen finden Sie unter [Formular "Dauerauftragsparameter"](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf00b-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="cf00b-114">Einrichtungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="cf00b-114">Setup requirements</span></span>

<span data-ttu-id="cf00b-115">Vergewissern Sie sich zum Antizipieren von Umsatzerlös, dass die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="cf00b-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="cf00b-116">Kontoeinstellungen</span><span class="sxs-lookup"><span data-stu-id="cf00b-116">Account setup</span></span>

<span data-ttu-id="cf00b-117">Die Konten **WIP - Dauerauftrag** und **Antizipierter Umsatz - Dauerauftrag** müssen im Modul **Projekt** eingerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="cf00b-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="cf00b-118">Beim Buchen von antizipiertem Umsatzerlös wird das Konto **WIP - Dauerauftrag** mit dem Abgrenzungsbetrag belastet, und dem Konto **Antizipierter Umsatz - Dauerauftrag** wird der Abgrenzungsbetrag gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="cf00b-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="cf00b-119">Einrichten von Konten für die Abgrenzung von Dauerauftragsumsatz</span><span class="sxs-lookup"><span data-stu-id="cf00b-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="cf00b-120">Klicken Sie auf **Projektverwaltung und -buchhaltung** \> **Einrichten** \> **Buchung** \> **Sachkontobuchungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="cf00b-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="cf00b-121">Klicken Sie auf die Registerkarte **Umsatzerlöskonten**, und wählen Sie **WIP - Dauerauftrag** oder **Antizipierter Umsatz - Dauerauftrag**, um die Konten einzurichten.</span><span class="sxs-lookup"><span data-stu-id="cf00b-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="cf00b-122">Einrichten der Dauerauftragsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf00b-122">Subscription group setup</span></span>

<span data-ttu-id="cf00b-123">Damit Umsatzerlöse für Daueraufträge abgegrenzt werden können, muss das Kontrollkästchen **Umsatz antizipieren** aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="cf00b-124">Es befindet sich im Formular **Dauerauftragsgruppen** für die Gruppe, die dem Dauerauftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cf00b-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="cf00b-125">Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="cf00b-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="cf00b-126">Aktivieren der Abgrenzung von Umsatzerlösen für eine Dauerauftragsgruppe</span><span class="sxs-lookup"><span data-stu-id="cf00b-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="cf00b-127">Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="cf00b-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="cf00b-128">Perioden</span><span class="sxs-lookup"><span data-stu-id="cf00b-128">Periods</span></span>

<span data-ttu-id="cf00b-129">Ein Code für den Rechnungsstellungszeitraum muss eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="cf00b-130">Sofern der Umsatzerlös nicht innerhalb der gleichen Zeiträume antizipiert werden soll, die auch für die Rechnungsstellung verwendet werden, muss zudem eine Abgrenzungsperiode eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="cf00b-131">Die folgenden Tabellen bieten einen Überblick über die Abgrenzungsperioden, die für die einzelnen Rechnungsstellungszeiträume eingerichtet werden können:</span><span class="sxs-lookup"><span data-stu-id="cf00b-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cf00b-132">Rechnungsstellungszeitraum</span><span class="sxs-lookup"><span data-stu-id="cf00b-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="cf00b-133">Abgrenzungsperiode</span><span class="sxs-lookup"><span data-stu-id="cf00b-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf00b-134"><strong>Jahre</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cf00b-135"><strong>Jahre</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="cf00b-136"><strong>Quartal</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="cf00b-137"><strong>Monat</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="cf00b-138"><strong>Tag</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf00b-139"><strong>Quartal</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cf00b-140"><strong>Quartal</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="cf00b-141"><strong>Monat</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="cf00b-142"><strong>Tag</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf00b-143"><strong>Monat</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cf00b-144"><strong>Monat</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="cf00b-145"><strong>Tag</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf00b-146"><strong>Woche</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cf00b-147"><strong>Tag</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf00b-148"><strong>Tag</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cf00b-149"><strong>Tag</strong></span><span class="sxs-lookup"><span data-stu-id="cf00b-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cf00b-150">Die Einrichtung des Rechnungsstellungszeitraums ist ein obligatorischer Teil der allgemeinen Dauerauftrags-Gruppeneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="cf00b-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="cf00b-151">Sie können entscheiden, ob auch eine Abgrenzungsperiode für die Dauerauftragsgruppe eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf00b-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="cf00b-152">Wenn Sie eine Abgrenzungsperiode für die Dauerauftragsgruppe einrichten, wird diese Periode im Feld **Periodencode** vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="cf00b-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="cf00b-153">Das Feld befindet sich im Formular **Abgrenzen des Dauerauftragsumsatzerlöses**, wenn der Umsatzerlös für den Dauerauftrag abgegrenzt wird.</span><span class="sxs-lookup"><span data-stu-id="cf00b-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="cf00b-154">Allerdings handelt es sich bei der Abgrenzungsperiode um optionale Informationen zur Dauerauftragsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cf00b-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cf00b-155">Verwenden Sie den folgenden Pfad, um das Formular <STRONG>Dauerauftragsumsatz antizipieren</STRONG> zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cf00b-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="cf00b-156">Klicken Sie auf <STRONG>Servicemanagement</STRONG> &gt; <STRONG>Periodisch</STRONG> &gt; <STRONG>Daueraufträge</STRONG> &gt; <STRONG>Dauerauftragsumsatz antizipieren</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="cf00b-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="cf00b-157">Buchungen</span><span class="sxs-lookup"><span data-stu-id="cf00b-157">Transactions</span></span>

<span data-ttu-id="cf00b-158">Sie können die Anzahl der Sachkontobuchungen bestimmen, die beim Buchen des abgegrenzten Umsatzerlöses erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="cf00b-159">Definieren Sie für Daueraufträge, ob die Sachkontobuchungen als Summe oder pro Position erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cf00b-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="cf00b-160">Angeben der anzuzeigenden Menge an Buchungsdetails bei abgegrenzten Buchungen</span><span class="sxs-lookup"><span data-stu-id="cf00b-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="cf00b-161">Klicken Sie auf **Projektverwaltung und Buchhaltung** \> **Setup** \> **Projektverwaltungs- und Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="cf00b-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="cf00b-162">Wählen Sie auf der **Registerkarte** im Feld **Rechnung** entweder **Gesamt** oder **Position** aus.</span><span class="sxs-lookup"><span data-stu-id="cf00b-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="cf00b-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf00b-163">See also</span></span>

[<span data-ttu-id="cf00b-164">Dauerauftragsumsatz antizipieren</span><span class="sxs-lookup"><span data-stu-id="cf00b-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  


