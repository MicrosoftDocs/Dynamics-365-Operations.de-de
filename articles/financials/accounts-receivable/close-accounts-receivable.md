---
title: "Debitoren abschließen"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b2e827df0c679855af9624f8a2fb36cb23f359a
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="close-accounts-receivable"></a><span data-ttu-id="16d97-102">Debitoren abschließen</span><span class="sxs-lookup"><span data-stu-id="16d97-102">Close Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="16d97-103">In der folgenden Tabelle werden die Seiten aufgeführt, in denen die Geschäftsprozesskomponente für den Debitorenabschluss unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="16d97-103">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="16d97-104">Hinweis: Für das Öffnen einiger der in der folgenden Tabelle enthaltenen Seiten müssen Informationen oder Parameter eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="16d97-104">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="16d97-105">**Geschäftsprozesskomponente**</span><span class="sxs-lookup"><span data-stu-id="16d97-105">**Business process component task**</span></span>                   

<span data-ttu-id="16d97-106">Periodenabschluss im Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="16d97-106">Close periods in the general ledger</span></span>

| <span data-ttu-id="16d97-107">Seitenname</span><span class="sxs-lookup"><span data-stu-id="16d97-107">Page name</span></span>                            | <span data-ttu-id="16d97-108">Nutzung</span><span class="sxs-lookup"><span data-stu-id="16d97-108">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="16d97-109">Stapelverarbeitungsauftrag</span><span class="sxs-lookup"><span data-stu-id="16d97-109">Batch job</span></span>                             | <span data-ttu-id="16d97-110">Dient zum Anzeigen oder Erstellen von Stapelverarbeitungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="16d97-110">View or create batch jobs.</span></span> <span data-ttu-id="16d97-111">Stapelverarbeitungsaufträge werden möglicherweise nicht abgeschlossen und Sie möchten sicherstellen, dass alle Buchung abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="16d97-111">Batch jobs might not be completed, and you want make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="16d97-112">Auftrag bestätigen</span><span class="sxs-lookup"><span data-stu-id="16d97-112">Confirm sales order</span></span>                   | <span data-ttu-id="16d97-113">Dient zum Aktualisieren von Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="16d97-113">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="16d97-114">Neubewertung der Fremdwährung</span><span class="sxs-lookup"><span data-stu-id="16d97-114">Foreign currency revaluation</span></span>          | <span data-ttu-id="16d97-115">Dient zum Generieren von Buchungen, durch die der Wert offener Debitorenbuchungen in Fremdwährungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="16d97-115">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="16d97-116">Erfassung</span><span class="sxs-lookup"><span data-stu-id="16d97-116">Journal</span></span>                              | <span data-ttu-id="16d97-117">Dient zum Buchen von Rechnungen, Zahlungen und Solawechseln.</span><span class="sxs-lookup"><span data-stu-id="16d97-117">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="16d97-118">Alle Journale</span><span class="sxs-lookup"><span data-stu-id="16d97-118">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="16d97-119">**Zahlungserfassung** – Dient zum Generieren, Verarbeiten und Buchen von Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="16d97-119">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="16d97-120">**Wechselerfassung ziehen** – Dient zum Buchen von Wechseln.</span><span class="sxs-lookup"><span data-stu-id="16d97-120">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="16d97-121">**Wechselerfassung protestieren** – Dient zum Buchen protestierter Wechsel.</span><span class="sxs-lookup"><span data-stu-id="16d97-121">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="16d97-122">**Wechselerfassung neu ziehen** – Dient zum Buchen erneut gezogener Wechsel.</span><span class="sxs-lookup"><span data-stu-id="16d97-122">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="16d97-123">**Rimesseerfassung** – Dient zum Buchen von Rimessen.</span><span class="sxs-lookup"><span data-stu-id="16d97-123">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="16d97-124">**Wechselerfassung ausgleichen** – Dient zum Buchen ausgeglichener Wechsel</span><span class="sxs-lookup"><span data-stu-id="16d97-124">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="16d97-125">Lieferschein buchen</span><span class="sxs-lookup"><span data-stu-id="16d97-125">Packing slip posting</span></span>                 | <span data-ttu-id="16d97-126">Dient zum Aktualisieren von Lieferscheinen für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="16d97-126">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="16d97-127">Freitextrechnung buchen</span><span class="sxs-lookup"><span data-stu-id="16d97-127">Post free text invoice</span></span>               | <span data-ttu-id="16d97-128">Dient zum Buchen von Freitextrechnungen.</span><span class="sxs-lookup"><span data-stu-id="16d97-128">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="16d97-129">Rechnung buchen</span><span class="sxs-lookup"><span data-stu-id="16d97-129">Posting invoice</span></span>                      | <span data-ttu-id="16d97-130">Dient zum Buchen von Rechnungen für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="16d97-130">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="16d97-131">Kommissionierliste buchen</span><span class="sxs-lookup"><span data-stu-id="16d97-131">Posting picking list</span></span>                 |<span data-ttu-id="16d97-132">Dient zum Aktualisieren von Kommissionierlisten für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="16d97-132">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="16d97-133">**Aufgabe der jeweiligen Geschäftsprozesskomponente**</span><span class="sxs-lookup"><span data-stu-id="16d97-133">**Business process component task**</span></span>   

<span data-ttu-id="16d97-134">Erstellen und Übermitteln der zusammenfassenden Meldung</span><span class="sxs-lookup"><span data-stu-id="16d97-134">Create and submit the EU sales list</span></span>

| <span data-ttu-id="16d97-135">Seitenname</span><span class="sxs-lookup"><span data-stu-id="16d97-135">Page name</span></span>                            | <span data-ttu-id="16d97-136">Nutzung</span><span class="sxs-lookup"><span data-stu-id="16d97-136">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="16d97-137">Zusammenfassende Meldung</span><span class="sxs-lookup"><span data-stu-id="16d97-137">EU sales list</span></span>                         | <span data-ttu-id="16d97-138">Melden von EU-Verkäufen an die Steuerbehörde zum Zweck der Mehrwertsteuererklärung.</span><span class="sxs-lookup"><span data-stu-id="16d97-138">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |







