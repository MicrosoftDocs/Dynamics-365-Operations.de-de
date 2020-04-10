---
title: " Zahlungskonfigurationen für Einzelhandelsauszüge"
description: Diese Prozedur zeigt Konfigurationen für Commerce-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 390ccdfde3f9bb93770d456af7532a42e81955a1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140806"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="61c99-103"> Zahlungskonfigurationen für Einzelhandelsauszüge</span><span class="sxs-lookup"><span data-stu-id="61c99-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61c99-104">Diese Prozedur zeigt Konfigurationen für Commerce-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="61c99-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="61c99-105">Für diese Erfassung wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="61c99-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="61c99-106">Navigieren Sie zu Einzelhandel und Commerce > Kanäle > Geschäfte > Alle Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="61c99-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="61c99-107">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="61c99-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="61c99-108">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="61c99-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="61c99-109">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="61c99-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="61c99-110">Klicken Sie auf "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="61c99-110">Click Payment methods.</span></span>
6. <span data-ttu-id="61c99-111">Erweitern oder reduzieren Sie den Abschnitt ''Buchung".</span><span class="sxs-lookup"><span data-stu-id="61c99-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="61c99-112">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="61c99-112">Click Edit.</span></span>
    * <span data-ttu-id="61c99-113">Wählen Sie aus, ob die Beträge, die für diese Zahlungsmethode eingehen, auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61c99-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="61c99-114">Wählen Sie das Konto aus, auf dem die Beträge, die für diese Zahlungsmethode eingehen, gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61c99-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="61c99-115">Wählen Sie ein Konto aus, um mögliche Differenzen zwischen dem Gesamtbuchungsbetrag, der eingeht, und dem Betrag, der für diese Zahlungsmethode berechnet wird, zu buchen.</span><span class="sxs-lookup"><span data-stu-id="61c99-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="61c99-116">In diesem Feld können Sie einen Betrag eingeben, um zu steuern, wann der Differenzbetrag auf einem anderen Differenzkonto gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c99-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="61c99-117">Sie können dieses verwenden, um große Differenzen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="61c99-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="61c99-118">Wählen Sie ein Konto aus, um mögliche Differenzen zwischen dem Gesamtbuchungsbetrag, der eingeht, und dem gezählten Betrag zu buchen, wenn er den Wert überschreitet, der im Feld "Maximaler Differenzbetrag" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="61c99-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="61c99-119">Wählen Sie "Ja" aus, um Bankeinzahlungsbeträge auf einem separaten Konto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="61c99-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="61c99-120">In diesem Feld können Sie auswählen, ob Bankeinzahlungsbeträge auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61c99-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="61c99-121">Wählen Sie das Konto zum Buchen von Bankeinzahlungsbeträgen aus.</span><span class="sxs-lookup"><span data-stu-id="61c99-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="61c99-122">Wählen Sie die Bankbuchungsart aus, die zum Buchen von Bankeinzahlungsbeträgen auf das Bankkonto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c99-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="61c99-123">Wählen Sie "Ja" aus, um Ablage im Tresor-Beträge auf einem separaten Konto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="61c99-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="61c99-124">Wählen Sie aus, ob Ablage im Tresor-Beträge auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61c99-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="61c99-125">Wählen Sie das Konto zum Buchen von Ablage im Tresor-Beträgen aus.</span><span class="sxs-lookup"><span data-stu-id="61c99-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="61c99-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="61c99-126">Click Save.</span></span>

