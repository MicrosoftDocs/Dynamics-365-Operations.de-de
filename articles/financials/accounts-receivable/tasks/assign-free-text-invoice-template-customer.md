---
title: Einem Debitor eine Freitextrechnungsvorlage zuweisen
description: In dieser Aufgabe wird dargestellt, wie Sie eine Freitextrechnungsvorlage zu einem Debitor zuweisen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53bff33083a78c0bb1c7d243fe9965fb264d209e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843048"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="bcf1a-103">Einem Debitor eine Freitextrechnungsvorlage zuweisen</span><span class="sxs-lookup"><span data-stu-id="bcf1a-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bcf1a-104">In dieser Aufgabe wird dargestellt, wie Sie eine Freitextrechnungsvorlage zu einem Debitor zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="bcf1a-105">Für diese Aufgabe wird das USMF-Demounternehmen verwendet und die Erfassung ist für den Benutzer bestimmt, der für die Verwaltung und für die Verarbeitung von Debitorenrechnungen zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="bcf1a-106">Wechseln Sie zu "Debitoren" > "Debitoren" > "Alle Debitoren".</span><span class="sxs-lookup"><span data-stu-id="bcf1a-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="bcf1a-107">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bcf1a-108">Klicken Sie im Aktivitätsbereich auf "Rechnung".</span><span class="sxs-lookup"><span data-stu-id="bcf1a-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="bcf1a-109">Klicken Sie auf "Serienrechnungen".</span><span class="sxs-lookup"><span data-stu-id="bcf1a-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="bcf1a-110">Mithilfe dieser Seite können Sie Debitoren Freitextrechnungsvorlagen zuweisen und angeben, wie häufig Rechnungen an den Debitor gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="bcf1a-111">Klicken Sie auf "Neu", um eine neue Vorlage zum Debitor zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="bcf1a-112">Wählen Sie die Freitextrechnung, die dem Debitor zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="bcf1a-113">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bcf1a-114">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bcf1a-115">Geben Sie das Datum ein, an dem die erste Rechnung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="bcf1a-116">Geben Sie ein wiederkehrendes Enddatum ein.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="bcf1a-117">Wählen Sie eine der folgenden Optionen: Kein Enddatum – Es werden so lange Rechnungen generiert, bis die Vorlage aus dem Debitorenkonto entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="bcf1a-118">Enddatum der Fakturierung – Wählen Sie diese Option aus, und geben Sie das letzte Datum ein, an dem eine Rechnung generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="bcf1a-119">Maximaler kumulierter Betrag, nachdem die Rechnungsgenerierung aufhört.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="bcf1a-120">Geben Sie den maximalen kumulativen Betrag ein, der unter Verwendung der ausgewählten Vorlage erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="bcf1a-121">Beispiel: Wenn Sie in dieses Feld den Wert 1.000,00 eingeben und monatlich eine Rechnung über jeweils 100,00 Einheiten generieren, wird nach der zehnten Rechnung keine weitere Rechnung mehr generiert.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="bcf1a-122">Generieren Sie Serienrechnungen, indem Sie die Standardwerte entweder aus der Freitextrechnungsvorlage oder vom Debitorenkonto verwenden.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="bcf1a-123">Wählen Sie aus, ob die Standardwerte für Sprache, Buchungsprofil, Mehrwertsteuergruppe, Artikel-Mehrwertsteuergruppe, Listencode, Land/Region zur Lieferadresse, Währung, Zahlungsbedingungen, Zahlungsmethode, Zahlungsspezifikation, Zahlungsplan, Skonto, Finanzdimensionen und Giro-Überweisungsbeleg anhand der Freitext-Rechnungsvorlage oder des Debitorenkontos bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="bcf1a-124">Wählen Sie das Wiederholungsmuster aus.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="bcf1a-125">Täglich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="bcf1a-126">Beispiel: Wenn Sie 15 eingeben, wird für diesen Debitor alle 15 Tage eine Rechnung generiert.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="bcf1a-127">Wöchentlich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Wochen ein.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="bcf1a-128">Beispiel: Wenn Sie 2 eingeben, wird für diesen Debitor alle zwei Wochen eine Rechnung generiert.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="bcf1a-129">Monatlich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Monaten ein.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="bcf1a-130">Beispiel: Wenn Sie 6 eingeben, wird für diesen Debitor alle sechs Monate eine Rechnung generiert.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="bcf1a-131">Jährlich – Wählen Sie diese Option aus, und geben Sie im Feld "Pro" die Anzahl von Jahren ein.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="bcf1a-132">Beispiel: Wenn Sie 2 eingeben, wird für diesen Debitor alle zwei Jahre eine Rechnung generiert.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="bcf1a-133">Geben Sie im Feld "Pro" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="bcf1a-133">In the Per field, enter a number.</span></span>

