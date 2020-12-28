---
title: Debitoren abschließen
description: Im folgenden Thema werden die Seiten aufgeführt, in denen die Geschäftsprozesskomponente für den Debitorenabschluss unterstützt wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3563f0f4d7d281a02231c1d3edcfe3ceb4277f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443545"
---
# <a name="close-accounts-receivable"></a><span data-ttu-id="381f7-103">Debitoren abschließen</span><span class="sxs-lookup"><span data-stu-id="381f7-103">Close Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="381f7-104">In der folgenden Tabelle werden die Seiten aufgeführt, in denen die Geschäftsprozesskomponente für den Debitorenabschluss unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="381f7-104">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="381f7-105">Hinweis: Für das Öffnen einiger der in der folgenden Tabelle enthaltenen Seiten müssen Informationen oder Parameter eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="381f7-105">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="381f7-106">**Geschäftsprozesskomponente**</span><span class="sxs-lookup"><span data-stu-id="381f7-106">**Business process component task**</span></span>                   

<span data-ttu-id="381f7-107">Periodenabschluss im Hauptbuch</span><span class="sxs-lookup"><span data-stu-id="381f7-107">Close periods in the general ledger</span></span>

| <span data-ttu-id="381f7-108">Seitenname</span><span class="sxs-lookup"><span data-stu-id="381f7-108">Page name</span></span>                            | <span data-ttu-id="381f7-109">Nutzung</span><span class="sxs-lookup"><span data-stu-id="381f7-109">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="381f7-110">Stapelverarbeitungsauftrag</span><span class="sxs-lookup"><span data-stu-id="381f7-110">Batch job</span></span>                             | <span data-ttu-id="381f7-111">Dient zum Anzeigen oder Erstellen von Stapelverarbeitungsaufträgen.</span><span class="sxs-lookup"><span data-stu-id="381f7-111">View or create batch jobs.</span></span> <span data-ttu-id="381f7-112">Stapelverarbeitungsaufträge werden möglicherweise nicht abgeschlossen und Sie möchten sicherstellen, dass alle Buchung abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="381f7-112">Batch jobs might not be completed, and you want to make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="381f7-113">Auftrag bestätigen</span><span class="sxs-lookup"><span data-stu-id="381f7-113">Confirm sales order</span></span>                   | <span data-ttu-id="381f7-114">Dient zum Aktualisieren von Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="381f7-114">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="381f7-115">Neubewertung der Fremdwährung</span><span class="sxs-lookup"><span data-stu-id="381f7-115">Foreign currency revaluation</span></span>          | <span data-ttu-id="381f7-116">Dient zum Generieren von Buchungen, durch die der Wert offener Debitorenbuchungen in Fremdwährungen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="381f7-116">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="381f7-117">Erfassung</span><span class="sxs-lookup"><span data-stu-id="381f7-117">Journal</span></span>                              | <span data-ttu-id="381f7-118">Dient zum Buchen von Rechnungen, Zahlungen und Solawechseln.</span><span class="sxs-lookup"><span data-stu-id="381f7-118">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="381f7-119">Alle Journale</span><span class="sxs-lookup"><span data-stu-id="381f7-119">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="381f7-120">**Zahlungserfassung** – Dient zum Generieren, Verarbeiten und Buchen von Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="381f7-120">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="381f7-121">**Wechselerfassung ziehen** – Dient zum Buchen von Wechseln.</span><span class="sxs-lookup"><span data-stu-id="381f7-121">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="381f7-122">**Wechselerfassung protestieren** – Dient zum Buchen protestierter Wechsel.</span><span class="sxs-lookup"><span data-stu-id="381f7-122">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="381f7-123">**Wechselerfassung neu ziehen** – Dient zum Buchen erneut gezogener Wechsel.</span><span class="sxs-lookup"><span data-stu-id="381f7-123">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="381f7-124">**Rimesseerfassung** – Dient zum Buchen von Rimessen.</span><span class="sxs-lookup"><span data-stu-id="381f7-124">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="381f7-125">**Wechselerfassung ausgleichen** – Dient zum Buchen ausgeglichener Wechsel</span><span class="sxs-lookup"><span data-stu-id="381f7-125">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="381f7-126">Lieferschein buchen</span><span class="sxs-lookup"><span data-stu-id="381f7-126">Packing slip posting</span></span>                 | <span data-ttu-id="381f7-127">Dient zum Aktualisieren von Lieferscheinen für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="381f7-127">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="381f7-128">Freitextrechnung buchen</span><span class="sxs-lookup"><span data-stu-id="381f7-128">Post free text invoice</span></span>               | <span data-ttu-id="381f7-129">Dient zum Buchen von Freitextrechnungen.</span><span class="sxs-lookup"><span data-stu-id="381f7-129">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="381f7-130">Rechnung buchen</span><span class="sxs-lookup"><span data-stu-id="381f7-130">Posting invoice</span></span>                      | <span data-ttu-id="381f7-131">Dient zum Buchen von Rechnungen für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="381f7-131">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="381f7-132">Kommissionierliste buchen</span><span class="sxs-lookup"><span data-stu-id="381f7-132">Posting picking list</span></span>                 |<span data-ttu-id="381f7-133">Dient zum Aktualisieren von Kommissionierlisten für Aufträge.</span><span class="sxs-lookup"><span data-stu-id="381f7-133">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="381f7-134">**Aufgabe der jeweiligen Geschäftsprozesskomponente**</span><span class="sxs-lookup"><span data-stu-id="381f7-134">**Business process component task**</span></span>   

<span data-ttu-id="381f7-135">Erstellen und Übermitteln der zusammenfassenden Meldung</span><span class="sxs-lookup"><span data-stu-id="381f7-135">Create and submit the EU sales list</span></span>

| <span data-ttu-id="381f7-136">Seitenname</span><span class="sxs-lookup"><span data-stu-id="381f7-136">Page name</span></span>                            | <span data-ttu-id="381f7-137">Nutzung</span><span class="sxs-lookup"><span data-stu-id="381f7-137">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="381f7-138">Zusammenfassende Meldung</span><span class="sxs-lookup"><span data-stu-id="381f7-138">EU sales list</span></span>                         | <span data-ttu-id="381f7-139">Melden von EU-Verkäufen an die Steuerbehörde zum Zweck der Mehrwertsteuererklärung.</span><span class="sxs-lookup"><span data-stu-id="381f7-139">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |






