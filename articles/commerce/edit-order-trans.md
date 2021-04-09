---
title: Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen
description: In diesem Thema wird beschrieben, wie Onlineauftrags- und asynchrone Debitorenauftragstransaktionen in Microsoft Dynamics 365 Commerce bearbeitet und überwacht werden.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5113f7ac0d308076ebaa9daeca0929eb537e94ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792680"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="6c043-103">Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="6c043-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c043-104">In diesem Thema wird beschrieben, wie Onlineauftrags- und asynchrone Debitorenauftragstransaktionen in Microsoft Dynamics 365 Commerce bearbeitet und überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="6c043-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6c043-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="6c043-105">Overview</span></span>

<span data-ttu-id="6c043-106">Zwischen den Commerce-Versionen 10.0.5 und 10.0.6 wurde die Unterstützung für die Bearbeitung von Abholungstransaktion (z. B. Verkäufe und Rückgaben) und Zahlungsmanagementtransaktionen (z. B. Bareinlage und Entfernung von Zahlungsmitteln) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6c043-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="6c043-107">In Commerce Version 10.0.7 wurde Unterstützung für das Bearbeiten von Onlineauftragstransaktionen und asynchronen Debitorenauftragstransaktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6c043-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="6c043-108">Auftragstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="6c043-108">Edit and audit order transactions</span></span>

<span data-ttu-id="6c043-109">Führen Sie die folgenden Schritte aus, um Auftragstransaktionen in der Commerce-Zentralverwaltung zu bearbeiten und zu prüfen.</span><span class="sxs-lookup"><span data-stu-id="6c043-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6c043-110">Installieren Sie das [Microsoft Dynamics Office-Add-In](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="6c043-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="6c043-111">Legen Sie auf der Seite **Einzelhandelsparameter**, der Registerkarte **Debitorenaufträge**, im Inforegister **Auftrag** einen Sperrcode für **Code bei Auftragssynchronisierungsfehler sperren** fest.</span><span class="sxs-lookup"><span data-stu-id="6c043-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="6c043-112">Öffnen Sie den Arbeitsbereich **Finanzdaten für Shop**.</span><span class="sxs-lookup"><span data-stu-id="6c043-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="6c043-113">Die Kacheln **Onlineauftragssynchronisierungsfehler** und **Debitorenauftragssynchronisierungsfehler** bieten eine vorgefilterte Ansicht der Einzelhandelstransaktionsseite.</span><span class="sxs-lookup"><span data-stu-id="6c043-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="6c043-114">Es werden die Transaktionsdatensätze angezeigt, bei denen die Synchronisierung des entsprechenden Auftragstyps fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6c043-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="6c043-115">Öffnen Sie entweder die Seite **Onlineauftragssynchronisierungsfehler** oder die Seite **Debitorenauftragssynchronisierungsfehler**.</span><span class="sxs-lookup"><span data-stu-id="6c043-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="6c043-116">Wählen Sie einen Datensatz aus, um die Details des Synchronisationsfehlers anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6c043-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="6c043-117">Das Inforegister **Synchronisierungsstatus** bietet folgende Fehlerdetails:</span><span class="sxs-lookup"><span data-stu-id="6c043-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="6c043-118">Status des ausstehenden Auftrags</span><span class="sxs-lookup"><span data-stu-id="6c043-118">Pending order status</span></span>
    - <span data-ttu-id="6c043-119">Auftragsfehlerdetails</span><span class="sxs-lookup"><span data-stu-id="6c043-119">Order error details</span></span>
    - <span data-ttu-id="6c043-120">Änderungsdatum und -uhrzeit</span><span class="sxs-lookup"><span data-stu-id="6c043-120">Modified date and time</span></span>
    - <span data-ttu-id="6c043-121">Anzahl von Wiederholungen</span><span class="sxs-lookup"><span data-stu-id="6c043-121">Retry count</span></span>

1. <span data-ttu-id="6c043-122">Wenn der Datensatz laut Fehlerdetails repariert werden muss, wählen Sie **Office-Add-In** und anschließend **Ausgewählte Transaktion bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6c043-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="6c043-123">Es öffnet sich eine Excel-Datei mit den Details der ausgewählten Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="6c043-124">Wenn es sich bei der zu bearbeitenden Transaktion um eine Onlineauftragstransaktion handelt, enthält die Excel-Datei folgende Arbeitsblätter:</span><span class="sxs-lookup"><span data-stu-id="6c043-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="6c043-125">**Transaktion** – Dieses Arbeitsblatt enthält die Kopfzeilendetails der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="6c043-126">**Verkaufstransaktion** – Dieses Arbeitsblatt enthält die Positionsdetails der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="6c043-127">**Zahlungstransaktionen** – Dieses Arbeitsblatt enthält die Details der Zahlungspositionen der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="6c043-128">**Rabatttransaktionen** – Dieses Arbeitsblatt enthält die rabattbezogenen Details der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="6c043-129">**Steuertransaktionen** – Dieses Arbeitsblatt enthält die steuerlichen Details der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="6c043-130">**Belastungsbuchungen** – Dieses Arbeitsblatt enthält die belastungsbezogenen Daten der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="6c043-131">Wenn es sich bei der zu bearbeitenden Transaktion um eine asynchrone Debitorenauftragstransaktion handelt, enthält die Excel-Datei folgende Arbeitsblätter:</span><span class="sxs-lookup"><span data-stu-id="6c043-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="6c043-132">**Positionen** – Dieses Arbeitsblatt enthält die Kopfzeilen- und Positionsdetails der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="6c043-133">**Zahlungen** – Dieses Arbeitsblatt enthält die Details der Zahlungspositionen der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="6c043-134">**Rabatte** – Dieses Arbeitsblatt enthält die rabattbezogenen Details der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="6c043-135">**Steuern** – Dieses Arbeitsblatt enthält die steuerlichen Details für die Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="6c043-136">**Gebühren** – Dieses Arbeitsblatt enthält die belastungsbezogenen Daten der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="6c043-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="6c043-137">Geben Sie **Bearbeitung** in der Excel-Datei im Feld **Status des ausstehenden Auftrags** ein, und veröffentlichen Sie dann die Änderung.</span><span class="sxs-lookup"><span data-stu-id="6c043-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="6c043-138">Auf diese Weise verhindern Sie, dass der Einzelvorgang **Auftrag synchronisieren**, der im Batchmodus ausgeführt wird, diesen Datensatz bei der Bearbeitung überspringt.</span><span class="sxs-lookup"><span data-stu-id="6c043-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="6c043-139">Ändern Sie die entsprechenden Felder in der Excel-Datei, und laden Sie die Daten dann mit Hilfe der Veröffentlichungsfunktion des Dynamics Excel-Add-Ins wieder in die Commerce-Zentralverwaltung hoch.</span><span class="sxs-lookup"><span data-stu-id="6c043-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="6c043-140">Sobald die Daten veröffentlich sind, werden die Änderungen im System berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6c043-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="6c043-141">Während der Veröffentlichung wird keine Überprüfung der von den Benutzern vorgenommenen Änderungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c043-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="6c043-142">Sie können sich ein vollständiges Protokoll der Änderungen anzeigen lassen, indem Sie **Audit-Trail anzeigen** in der **Einzelhandelstransaktion**-Kopfzeile (Änderungen auf Kopfzeilenebene) oder in den entsprechenden Abschnitt und Datensatz auswählen.</span><span class="sxs-lookup"><span data-stu-id="6c043-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="6c043-143">Beispielsweise werden alle Änderungen, die sich auf Verkaufspositionen beziehen, auf der Seite **Verkaufstransaktionen** angezeigt, und alle Änderungen, die sich auf Zahlungen beziehen, werden auf der Seite **Zahlungstransaktionen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c043-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="6c043-144">Die folgenden Prüfungsdetails werden für die Änderungen beibehalten:</span><span class="sxs-lookup"><span data-stu-id="6c043-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="6c043-145">Änderungsdatum und -uhrzeit</span><span class="sxs-lookup"><span data-stu-id="6c043-145">Modified date and time</span></span>
    - <span data-ttu-id="6c043-146">Feld</span><span class="sxs-lookup"><span data-stu-id="6c043-146">Field</span></span>
    - <span data-ttu-id="6c043-147">Alter Wert</span><span class="sxs-lookup"><span data-stu-id="6c043-147">Old value</span></span>
    - <span data-ttu-id="6c043-148">Neuer Wert</span><span class="sxs-lookup"><span data-stu-id="6c043-148">New value</span></span>
    - <span data-ttu-id="6c043-149">Geändert von</span><span class="sxs-lookup"><span data-stu-id="6c043-149">Modified by</span></span>

1. <span data-ttu-id="6c043-150">Sobald Sie Ihre Änderungen vorgenommen und veröffentlicht haben, wählen Sie **Auftrag synchronisieren** aus, um den Synchronisierungsprozess sofort zu starten.</span><span class="sxs-lookup"><span data-stu-id="6c043-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="6c043-151">Alternativ können Sie auf den Synchronisierungsprozess warten, der im Batchmodus ausgeführt wird, um die Transaktion zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c043-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="6c043-152">Sobald die Aufträge erfolgreich synchronisiert wurden, werden sie standardmäßig in einen Wartestatus versetzt, basierend auf dem in den Commerce-Parametern definierten Sperrcode.</span><span class="sxs-lookup"><span data-stu-id="6c043-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="6c043-153">Das Zurückhalten der Aufträge muss aufgehoben werden, bevor die Aufträge zur Erfüllung oder für andere Vorgänge weiter verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="6c043-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c043-154">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6c043-154">Additional resources</span></span>

[<span data-ttu-id="6c043-155">Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="6c043-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="6c043-156">Finanzdimensionen für Einzelhandelstransaktionen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="6c043-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="6c043-157">Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen</span><span class="sxs-lookup"><span data-stu-id="6c043-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="6c043-158">Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen</span><span class="sxs-lookup"><span data-stu-id="6c043-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]