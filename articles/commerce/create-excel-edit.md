---
title: Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Excel-Arbeitsmappe erstellen, damit Sie Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten können.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2b6e98db54e7747912aad26f4b8ae24b9ad5a6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459123"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="7183b-103">Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen</span><span class="sxs-lookup"><span data-stu-id="7183b-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7183b-104">In diesem Thema wird beschrieben, wie Sie eine Excel-Arbeitsmappe erstellen, damit Sie Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="7183b-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7183b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7183b-105">Overview</span></span>

<span data-ttu-id="7183b-106">Es gibt eine vordefinierte Excel-Vorlage, auf die Debitoren von verschiedenen Bereichen des Systems aus zugreifen und zum Bearbeiten und Prüfen von Einzelhandelstransaktionen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7183b-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="7183b-107">Zu diesem Zweck können Debitoren aber auch eine benutzerdefinierte Excel-Arbeitsmappe erstellen.</span><span class="sxs-lookup"><span data-stu-id="7183b-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="7183b-108">Excel-Arbeitsmappe erstellen und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="7183b-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="7183b-109">Führen Sie die folgenden Schritte aus, um eine Excel-Arbeitsmappe zu erstellen und zu konfigurieren, damit Sie Einzelhandelstransaktionen bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="7183b-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="7183b-110">Öffnen Sie Excel, und erstellen Sie eine leere Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="7183b-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="7183b-111">Wählen Sie auf der Registerkarte **Einfügen** **Meine Add-Ins** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="7183b-112">Wählen Sie im rechten Bereich den Link **Serverinformationen hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="7183b-113">Geben Sie die Server-URL ein, und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="7183b-114">Wenn die Fehlermeldung „Keine Applet-Registrierungen gefunden“ erscheint, führen Sie die folgenden Schritte aus, um das Problem zu beheben:</span><span class="sxs-lookup"><span data-stu-id="7183b-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="7183b-115">Rufen Sie in Commerce **Systemadministration \> Setup \> Office-App-Parameter** auf.</span><span class="sxs-lookup"><span data-stu-id="7183b-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="7183b-116">Wählen Sie im Inforegister **App-Parameter** **App-Parameter initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="7183b-117">Wählen Sie im Benachrichtigungsfeld **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="7183b-118">Wählen Sie im Inforegister **Registrierte Applets** **Applet-Registrierung initialisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="7183b-119">Wiederholen Sie bei Bedarf diese drei Schritte.</span><span class="sxs-lookup"><span data-stu-id="7183b-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="7183b-120">Wählen Sie **Entwerfen** und anschließend **Tabelle hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="7183b-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="7183b-121">Wählen Sie basierend auf den Daten, die geändert werden müssen, die Entitäten aus, die der Excel-Arbeitsmappe zur Bearbeitung hinzugefügt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7183b-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="7183b-122">Verwenden Sie die folgende Tabelle als Referenz.</span><span class="sxs-lookup"><span data-stu-id="7183b-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="7183b-123">Transaktionstyp</span><span class="sxs-lookup"><span data-stu-id="7183b-123">Transaction type</span></span> | <span data-ttu-id="7183b-124">Zu verwendende Datenentitäten</span><span class="sxs-lookup"><span data-stu-id="7183b-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="7183b-125">Abholungstransaktionen, Onlineaufträge, asynchrone Debitorenaufträge, asynchrone Debitorenangebote</span><span class="sxs-lookup"><span data-stu-id="7183b-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="7183b-126">Transaktion (prüfbar), Verkaufstransaktion (prüfbar), Zahlungstransaktionen (prüfbar), Steuertransaktionen (prüfbar), Rabatttransaktionen (prüfbar), Belastungstransaktionen (prüfbar)</span><span class="sxs-lookup"><span data-stu-id="7183b-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="7183b-127">Bankeinzahlung</span><span class="sxs-lookup"><span data-stu-id="7183b-127">Bank drop</span></span> | <span data-ttu-id="7183b-128">Transaktion (prüfbar), Zahlungsmittelbuchungen (Bank, prüfbar)</span><span class="sxs-lookup"><span data-stu-id="7183b-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="7183b-129">Sichere Einzahlung</span><span class="sxs-lookup"><span data-stu-id="7183b-129">Safe drop</span></span> | <span data-ttu-id="7183b-130">Transaktion (prüfbar), sichere Zahlungsmittelbuchungen (prüfbar)</span><span class="sxs-lookup"><span data-stu-id="7183b-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="7183b-131">Zahlungsmitteldeklaration</span><span class="sxs-lookup"><span data-stu-id="7183b-131">Tender declaration</span></span> | <span data-ttu-id="7183b-132">Transaktion (prüfbar), Zahlungsmitteldeklarationsbuchungen (prüfbar)</span><span class="sxs-lookup"><span data-stu-id="7183b-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="7183b-133">Einnahmen, Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7183b-133">Income, Expense</span></span> | <span data-ttu-id="7183b-134">Transaktion (prüfbar), Einnahmen/Ausgaben-Transaktionen (prüfbar), Zahlungstransaktionen (prüfbar)</span><span class="sxs-lookup"><span data-stu-id="7183b-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="7183b-135">Startbetrag angeben, Zahlungsmittel entfernen, Mittelzugang, Zahlungsmittel ändern, Rechnungszahlung, Debitoreneinzahlung</span><span class="sxs-lookup"><span data-stu-id="7183b-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="7183b-136">Transaktion (prüfbar), Zahlungstransaktionen (prüfbar)</span><span class="sxs-lookup"><span data-stu-id="7183b-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="7183b-137">Es ist wichtig, dass Sie jeder Excel-Arbeitsmappe nur eine Datenentität hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7183b-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="7183b-138">Zusätzlich müssen alle Felder, die durch ein Schlüsselsymbol gekennzeichnet sind, der entsprechenden Arbeitsmappe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7183b-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="7183b-139">Wenden Sie nach der Konfiguration der Arbeitsmappe die erforderlichen Filter an.</span><span class="sxs-lookup"><span data-stu-id="7183b-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="7183b-140">Vergewissern Sie sich, dass Sie auf alle Arbeitsblätter in der Datei dieselben Filter anwenden.</span><span class="sxs-lookup"><span data-stu-id="7183b-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="7183b-141">Vermeiden Sie das Laden sehr großer Datenmengen in die Excel-Datei.</span><span class="sxs-lookup"><span data-stu-id="7183b-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="7183b-142">Andernfalls kann die Leistung beeinträchtigt sein, sodass Excel und Ihr System möglicherweise langsamer werden.</span><span class="sxs-lookup"><span data-stu-id="7183b-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="7183b-143">Wir empfehlen, immer „Unternehmen“ und entweder „Kontoauszugsnummer“ oder „Buchungsnummer“ als Filter für Ihre Datei zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7183b-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="7183b-144">Sobald Sie die Filter konfiguriert haben, wählen Sie **Aktualisieren** aus, um die Daten zu laden.</span><span class="sxs-lookup"><span data-stu-id="7183b-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="7183b-145">Bearbeiten Sie die erforderlichen Daten, und veröffentlichen Sie sie anschließend.</span><span class="sxs-lookup"><span data-stu-id="7183b-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="7183b-146">Wenn die Schaltfläche **Veröffentlichen** nicht verfügbar ist, wurden der Excel-Arbeitsmappe wahrscheinlich einige Schlüsselfelder nicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7183b-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7183b-147">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7183b-147">Additional resources</span></span>

[<span data-ttu-id="7183b-148">Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="7183b-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="7183b-149">Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen</span><span class="sxs-lookup"><span data-stu-id="7183b-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="7183b-150">Finanzdimensionen für Einzelhandelstransaktionen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="7183b-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="7183b-151">Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen</span><span class="sxs-lookup"><span data-stu-id="7183b-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)