--- 
title: " Zahlungskonfigurationen für Einzelhandelsauszüge"
description: "Diese Prozedur zeigt Konfigurationen für Einzelhandelsgeschäft-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f12d8ac9be11b92eaef4acce094ae183906278d4
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="1ff06-103"> Zahlungskonfigurationen für Einzelhandelsauszüge</span><span class="sxs-lookup"><span data-stu-id="1ff06-103">Payment configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1ff06-104">Diese Prozedur zeigt Konfigurationen für Einzelhandelsgeschäft-Zahlungsmethoden, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="1ff06-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="1ff06-105">Für diese Erfassung wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ff06-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="1ff06-106">Navigieren Sie zu Einzelhandel und Handel > Kanäle > Einzelhandelsgeschäfte > Alle Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="1ff06-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="1ff06-107">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="1ff06-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1ff06-108">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="1ff06-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1ff06-109">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="1ff06-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="1ff06-110">Klicken Sie auf "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="1ff06-110">Click Payment methods.</span></span>
6. <span data-ttu-id="1ff06-111">Erweitern oder reduzieren Sie den Abschnitt ''Buchung".</span><span class="sxs-lookup"><span data-stu-id="1ff06-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="1ff06-112">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="1ff06-112">Click Edit.</span></span>
    * <span data-ttu-id="1ff06-113">Wählen Sie aus, ob die Beträge, die für diese Zahlungsmethode eingehen, auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="1ff06-114">Wählen Sie das Konto aus, auf dem die Beträge, die für diese Zahlungsmethode eingehen, gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="1ff06-115">Wählen Sie ein Konto aus, um mögliche Differenzen zwischen dem Gesamtbuchungsbetrag, der eingeht, und dem Betrag, der für diese Zahlungsmethode berechnet wird, zu buchen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="1ff06-116">In diesem Feld können Sie einen Betrag eingeben, um zu steuern, wann der Differenzbetrag auf einem anderen Differenzkonto gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ff06-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="1ff06-117">Sie können dieses verwenden, um große Differenzen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="1ff06-118">Wählen Sie ein Konto aus, um mögliche Differenzen zwischen dem Gesamtbuchungsbetrag, der eingeht, und dem gezählten Betrag zu buchen, wenn er den Wert überschreitet, der im Feld "Maximaler Differenzbetrag" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ff06-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="1ff06-119">Wählen Sie "Ja" aus, um Bankeinzahlungsbeträge auf einem separaten Konto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-119">Select "Yes" to post bank drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="1ff06-120">In diesem Feld können Sie auswählen, ob Bankeinzahlungsbeträge auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="1ff06-121">Wählen Sie das Konto zum Buchen von Bankeinzahlungsbeträgen aus.</span><span class="sxs-lookup"><span data-stu-id="1ff06-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="1ff06-122">Wählen Sie die Bankbuchungsart aus, die zum Buchen von Bankeinzahlungsbeträgen auf das Bankkonto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ff06-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="1ff06-123">Wählen Sie "Ja" aus, um Ablage im Tresor-Beträge auf einem separaten Konto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-123">Select "Yes" to post safe drop amounts to a seperate account.</span></span>  
    * <span data-ttu-id="1ff06-124">Wählen Sie aus, ob Ablage im Tresor-Beträge auf ein Sachkonto oder ein Bankkonto gebucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ff06-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="1ff06-125">Wählen Sie das Konto zum Buchen von Ablage im Tresor-Beträgen aus.</span><span class="sxs-lookup"><span data-stu-id="1ff06-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="1ff06-126">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1ff06-126">Click Save.</span></span>


