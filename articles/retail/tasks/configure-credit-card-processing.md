---
title: " Verarbeitung der Kreditkartendaten konfigurieren"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Anzeigen der Liste der Zahlungsanbieter und Konfigurieren eines Zahlungskontos für Debitoren.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d75ff895c252bfd4f70f8bcc4c4adece585d9a22
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320396"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="17b58-103"> Verarbeitung der Kreditkartendaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="17b58-103">Configure credit card processing</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="17b58-104">Diese Prozedur führt Sie Schritt für Schritt durch das Anzeigen der Liste der Zahlungsanbieter und Konfigurieren eines Zahlungskontos für Debitoren.</span><span class="sxs-lookup"><span data-stu-id="17b58-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="17b58-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet. Sie ist für Administratoren und IT-Experten vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="17b58-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="17b58-106">Eine Liste der Zahlungsanbieter anzeigen</span><span class="sxs-lookup"><span data-stu-id="17b58-106">View a list of payment providers</span></span>
1. <span data-ttu-id="17b58-107">Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsdienste".</span><span class="sxs-lookup"><span data-stu-id="17b58-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="17b58-108">Klicken Sie auf "Verfügbare Anbieter".</span><span class="sxs-lookup"><span data-stu-id="17b58-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="17b58-109">Konfigurieren Sie ein Zahlungskonto</span><span class="sxs-lookup"><span data-stu-id="17b58-109">Configure payment account</span></span>
1. <span data-ttu-id="17b58-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="17b58-110">Click New.</span></span>
2. <span data-ttu-id="17b58-111">Geben Sie im Feld "Zahlungsdienst" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="17b58-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="17b58-112">Wählen Sie im Feld "Connector für Zahlungen" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="17b58-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="17b58-113">Schalten Sie die Erweiterung des Abschnitts "Zahlungsservicekonto" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="17b58-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="17b58-114">Geben Sie "PROD" im Feld "Umgebung:" ein.</span><span class="sxs-lookup"><span data-stu-id="17b58-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="17b58-115">Klicken Sie auf "Kreditkartentypen".</span><span class="sxs-lookup"><span data-stu-id="17b58-115">Click Credit card types.</span></span>
7. <span data-ttu-id="17b58-116">Klicken Sie im Feld "Zahlungserfassung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17b58-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="17b58-117">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="17b58-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="17b58-118">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17b58-118">Click Add.</span></span>
10. <span data-ttu-id="17b58-119">Geben Sie im Feld "Währung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="17b58-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="17b58-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="17b58-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="17b58-121">Klicken Sie im Feld "Zahlungserfassung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17b58-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="17b58-122">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="17b58-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="17b58-123">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17b58-123">Click Add.</span></span>
15. <span data-ttu-id="17b58-124">Geben Sie im Feld "Währung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="17b58-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="17b58-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="17b58-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="17b58-126">Sie können diese Schritte für beliebig viele Kartentypen wiederholen.</span><span class="sxs-lookup"><span data-stu-id="17b58-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="17b58-127">Klicken Sie im Feld "Zahlungserfassung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="17b58-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="17b58-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="17b58-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="17b58-129">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="17b58-129">Click Add.</span></span>
20. <span data-ttu-id="17b58-130">Geben Sie im Feld "Währung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="17b58-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="17b58-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="17b58-131">Click Save.</span></span>
22. <span data-ttu-id="17b58-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="17b58-132">Close the page.</span></span>
23. <span data-ttu-id="17b58-133">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="17b58-133">Click Validate.</span></span>
24. <span data-ttu-id="17b58-134">Klicken Sie auf das Kontrollkästchen "Standardmäßige Verarbeitungsstelle für neue Kreditkarten".</span><span class="sxs-lookup"><span data-stu-id="17b58-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="17b58-135">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="17b58-135">Click Save.</span></span>

