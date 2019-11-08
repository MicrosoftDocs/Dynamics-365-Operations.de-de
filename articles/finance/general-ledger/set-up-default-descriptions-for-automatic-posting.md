---
title: Standardbeschreibungen für automatische Buchungen einrichten
description: In diesem Thema wird beschrieben, wie Sie Standardtext einrichten, der verwendet wird, um Buchhaltungseinträge auszufüllen, die automatisch im Hauptbuch gebucht werden. Sie können Standardbeschreibungstext einrichten, indem Sie Freihandtext verwenden oder indem Sie feste Variablen auswählen.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622688"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="ff425-104">Standardbeschreibungen für automatische Buchungen einrichten</span><span class="sxs-lookup"><span data-stu-id="ff425-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="ff425-105">In diesem Thema wird beschrieben, wie Sie Standardtext einrichten, der verwendet wird, um Buchhaltungseinträge auszufüllen, die automatisch im Hauptbuch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="ff425-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="ff425-106">Sie können Standardbeschreibungstext einrichten, indem Sie Freihandtext verwenden oder indem Sie feste Variablen auswählen.</span><span class="sxs-lookup"><span data-stu-id="ff425-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="ff425-107">Bei bestimmten Buchungstypen in einigen Regionen oder Ländern können Sie auch Text aus den Feldern der Microsoft Dynamics AX-Datenbank, die den Buchungsarten zugeordnet sind, einschließen.</span><span class="sxs-lookup"><span data-stu-id="ff425-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="ff425-108">Eine Liste der Buchungsarten und der Länder und Regionen finden Sie im Abschnitt [Optional: Hinzufügen von weiterem Text zu Standardbeschreibungen](#optional-add-other-text-to-default-descriptions) weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ff425-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="ff425-109">Einrichten von Standardbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="ff425-109">Set up default descriptions</span></span>

1. <span data-ttu-id="ff425-110">Wechseln Sie zu **Organisationsverwaltung** \> **Einstellungen** \> **Standardbeschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="ff425-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="ff425-111">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="ff425-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="ff425-112">Wählen Sie im Feld **Beschreibung** den Buchungstyp aus, für den eine standardmäßige Beschreibung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff425-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="ff425-113">Wählen Sie im Feld **Sprache** die Sprache aus, für die diese Beschreibung gilt.</span><span class="sxs-lookup"><span data-stu-id="ff425-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="ff425-114">Geben Sie im Feld **Text** die Standardbeschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="ff425-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="ff425-115">Sie können Text im Feld eingeben, oder Sie können eine oder mehrere der folgenden Freitextvariablen verwenden:</span><span class="sxs-lookup"><span data-stu-id="ff425-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="ff425-116">**%1** – Das Buchungdatum hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff425-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="ff425-117">**%2** – Hinzufügen einer Kennung, die dem Dokumenttyp entspricht, der im Hauptbuch gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="ff425-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="ff425-118">Zum Beispiel fügt für Buchungsarten, die Rechnungen zugeordnet sind, die Variable **%2** die Rechnungsnummer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ff425-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="ff425-119">**%3** – Hinzufügen einer Kennung, die dem Dokumenttyp entspricht, der im Hauptbuch gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="ff425-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="ff425-120">Zum Beispiel fügt für Buchungsarten, die Rechnungen zugeordnet sind, die Variable **%3** die Kundenkontonummer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ff425-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="ff425-121">Optional: Hinzufügen von weiterem Text zu Standardbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="ff425-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="ff425-122">Bei bestimmten Buchungstypen in einigen Regionen oder Ländern können Standardbeschreibungen Text enthalten, der aus den Feldern Ihrer Daten kommt, die den Buchungsarten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ff425-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="ff425-123">Die folgenden Listen zeigen die Buchungsarten und die Länder und Regionen an, für die diese Option verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ff425-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="ff425-124">**Buchungsarten**</span><span class="sxs-lookup"><span data-stu-id="ff425-124">**Transaction types**</span></span>

<span data-ttu-id="ff425-125">Sie können sonstige Texte den Standardbeschreibungen für Buchungsarten hinzufügen, dieden folgenden Dokumenttypen zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="ff425-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="ff425-126">Debitorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="ff425-126">Customer invoices</span></span>
- <span data-ttu-id="ff425-127">Debitorengutschriften</span><span class="sxs-lookup"><span data-stu-id="ff425-127">Customer credit notes</span></span>
- <span data-ttu-id="ff425-128">Debitorenbarzahlungen</span><span class="sxs-lookup"><span data-stu-id="ff425-128">Customer cash payments</span></span>
- <span data-ttu-id="ff425-129">Kreditorenzahlungen</span><span class="sxs-lookup"><span data-stu-id="ff425-129">Vendor payments</span></span>
- <span data-ttu-id="ff425-130">Aufträge</span><span class="sxs-lookup"><span data-stu-id="ff425-130">Sales orders</span></span>
- <span data-ttu-id="ff425-131">Bestellungen</span><span class="sxs-lookup"><span data-stu-id="ff425-131">Purchase orders</span></span>
- <span data-ttu-id="ff425-132">Lagererfassungen</span><span class="sxs-lookup"><span data-stu-id="ff425-132">Inventory journals</span></span>
- <span data-ttu-id="ff425-133">Produktprogrammplanung (MRP)</span><span class="sxs-lookup"><span data-stu-id="ff425-133">Master planning (MRP)</span></span>
- <span data-ttu-id="ff425-134">Anlagen</span><span class="sxs-lookup"><span data-stu-id="ff425-134">Fixed assets</span></span>

<span data-ttu-id="ff425-135">**Länder und Regionen**</span><span class="sxs-lookup"><span data-stu-id="ff425-135">**Countries and regions**</span></span>

<span data-ttu-id="ff425-136">Diese Option ist für die folgenden Länder und Regionen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ff425-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="ff425-137">Brasilien</span><span class="sxs-lookup"><span data-stu-id="ff425-137">Brazil</span></span>
- <span data-ttu-id="ff425-138">China</span><span class="sxs-lookup"><span data-stu-id="ff425-138">China</span></span>
- <span data-ttu-id="ff425-139">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="ff425-139">Czech Republic</span></span>
- <span data-ttu-id="ff425-140">Osteuropa</span><span class="sxs-lookup"><span data-stu-id="ff425-140">Eastern Europe</span></span>
- <span data-ttu-id="ff425-141">Ungarn</span><span class="sxs-lookup"><span data-stu-id="ff425-141">Hungary</span></span>
- <span data-ttu-id="ff425-142">Indien</span><span class="sxs-lookup"><span data-stu-id="ff425-142">India</span></span>
- <span data-ttu-id="ff425-143">Japan</span><span class="sxs-lookup"><span data-stu-id="ff425-143">Japan</span></span>
- <span data-ttu-id="ff425-144">Litauen</span><span class="sxs-lookup"><span data-stu-id="ff425-144">Lithuania</span></span>
- <span data-ttu-id="ff425-145">Lettland</span><span class="sxs-lookup"><span data-stu-id="ff425-145">Latvia</span></span>
- <span data-ttu-id="ff425-146">Polen</span><span class="sxs-lookup"><span data-stu-id="ff425-146">Poland</span></span>
- <span data-ttu-id="ff425-147">Russland</span><span class="sxs-lookup"><span data-stu-id="ff425-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="ff425-148">Hinzufügen von Text zu Standardbeschreibungen</span><span class="sxs-lookup"><span data-stu-id="ff425-148">Add text to default descriptions</span></span>

<span data-ttu-id="ff425-149">Nachdem Sie die Schritte in [Einrichten von Standardbeschreibungen](#set-up-default-descriptions) weiter oben in diesem Thema, abgeschlossen haben, gehen Sie folgendermaßen vor, um weiteren Text den Standardbeschreibungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ff425-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="ff425-150">Auf dem Inforegister **Parameter** wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ff425-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="ff425-151">Wählen Sie im Feld **Bezugstabelle** die Datenbanktabelle aus, aus der der Beschreibung Parameterdaten hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff425-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="ff425-152">Wählen Sie im Feld **Referenzfeld** das Feld aus, aus dem der Beschreibung Parameterdaten hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff425-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="ff425-153">Wiederholen Sie zum Hinzufügen weiterer Parameter die Schritte 1 bis 3.</span><span class="sxs-lookup"><span data-stu-id="ff425-153">Repeat steps 1 through 3 to add more parameters.</span></span>
