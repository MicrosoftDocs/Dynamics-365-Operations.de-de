---
title: Angaben zur TDS-Gruppe, PAN und TAN für Debitoren und Kreditoren einrichten
description: In diesem Thema wird Erklärt, wie Sie Angaben zur Gruppe im Rahmen der Quellenbesteuerung (TDS-Gruppe), zur permanenten Kontonummer (PAN) und zur Steuerkontonummer (TAN) für Kreditoren und Debitoren einrichten.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023269"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="825a8-103">Angaben zur TDS-Gruppe, PAN und TAN für Debitoren und Kreditoren einrichten</span><span class="sxs-lookup"><span data-stu-id="825a8-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="825a8-104">In diesem Thema wird Erklärt, wie Sie Angaben zur Gruppe im Rahmen der Quellenbesteuerung (TDS-Gruppe), zur permanenten Kontonummer (PAN) und zur Steuerkontonummer (TAN) für Kreditoren und Debitoren einrichten.</span><span class="sxs-lookup"><span data-stu-id="825a8-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="825a8-105">Gehen Sie zu **Kreditorenkonten \> Kreditoren \> Alle Kreditoren** oder **Debitorenkonten \> Debitoren \> Alle Debitoren**.</span><span class="sxs-lookup"><span data-stu-id="825a8-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="825a8-106">[![Seite „Alle Kreditoren“](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="825a8-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="825a8-107">Wählen Sie im Aktionsbereich die Option **Neu** aus, um einen Kreditor oder Debitor zu erstellen und die erforderlichen Details einzugeben.</span><span class="sxs-lookup"><span data-stu-id="825a8-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="825a8-108">Alternativ können Sie einen vorhandenen Kreditor oder Debitor auswählen.</span><span class="sxs-lookup"><span data-stu-id="825a8-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="825a8-109">Setzen Sie im Inforegister **Rechnung und Lieferung** im Abschnitt **Quellensteuer** die Option **Quellensteuer berechnen** auf **Ja**, um für den Kreditor oder Debitor Quellensteuern, TDS oder TCS zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="825a8-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="825a8-110">Die TDS für eine Einkaufsrechnung wird auf Grundlage der Standard-TDS-Gruppe berechnet, die für den Kreditor oder Debitor festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="825a8-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="825a8-111">Wählen Sie im Feld **TDS-Gruppe** die Standard-TDS-Gruppe aus.</span><span class="sxs-lookup"><span data-stu-id="825a8-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="825a8-112">Wenn Sie eine TDS-Gruppe im Feld **TDS-Gruppe** auswählen, sind die Felder **Quellensteuergruppe** und **TCS-Gruppe** nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="825a8-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="825a8-113">Wählen Sie im Inforegister **Steuerliche Angaben** im Abschnitt **PAN-Informationen** den Status der permanenten Kontonummer für den Kreditor oder Debitor im Feld **Status** aus:</span><span class="sxs-lookup"><span data-stu-id="825a8-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="825a8-114">**Nicht verfügbar**: Der Kreditor oder Debitor hat keine PAN.</span><span class="sxs-lookup"><span data-stu-id="825a8-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="825a8-115">**Erhalten**: Der Kreditor oder Debitor hat eine PAN.</span><span class="sxs-lookup"><span data-stu-id="825a8-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="825a8-116">**Beantragt**: Der Kreditor oder Debitor hat eine PAN beantragt.</span><span class="sxs-lookup"><span data-stu-id="825a8-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="825a8-117">**Ungültig**: Der Kreditor oder Debitor hat eine PAN, diese ist jedoch nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="825a8-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="825a8-118">Wenn Sie **Erhalten** als **Status** ausgewählt haben, weil der Kreditor oder Debitor eine PAN hat, geben Sie die PAN im Feld **Nummer** ein.</span><span class="sxs-lookup"><span data-stu-id="825a8-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="825a8-119">Die PAN muss aus fünf alphabetischen Zeichen, dann vier numerischen Zeichen und dann einem alphabetischen Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="825a8-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="825a8-120">Hier ist ein Beispiel: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="825a8-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="825a8-121">Wenn Sie **Beantragt** als **Status** ausgewählt haben, weil der Kreditor oder Debitor eine PAN beantragt hat, geben Sie die Referenznummer im Feld **Referenznummer** ein.</span><span class="sxs-lookup"><span data-stu-id="825a8-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="825a8-122">Wählen Sie im Feld **Art des Steuerschuldners** die Steuerschuldnerkategorie aus, in die der Kreditor oder Debitor fällt.</span><span class="sxs-lookup"><span data-stu-id="825a8-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="825a8-123">Firma</span><span class="sxs-lookup"><span data-stu-id="825a8-123">Company</span></span>
    - <span data-ttu-id="825a8-124">HUF</span><span class="sxs-lookup"><span data-stu-id="825a8-124">HUF</span></span>
    - <span data-ttu-id="825a8-125">Vorschlagsumwandlung</span><span class="sxs-lookup"><span data-stu-id="825a8-125">Firm</span></span>
    - <span data-ttu-id="825a8-126">Einzeln</span><span class="sxs-lookup"><span data-stu-id="825a8-126">Individual</span></span>
    - <span data-ttu-id="825a8-127">AOP</span><span class="sxs-lookup"><span data-stu-id="825a8-127">AOP</span></span>
    - <span data-ttu-id="825a8-128">BOI</span><span class="sxs-lookup"><span data-stu-id="825a8-128">BOI</span></span>
    - <span data-ttu-id="825a8-129">Gemeinde</span><span class="sxs-lookup"><span data-stu-id="825a8-129">Local authority</span></span>
    - <span data-ttu-id="825a8-130">Andere</span><span class="sxs-lookup"><span data-stu-id="825a8-130">Others</span></span>

    <span data-ttu-id="825a8-131">[![Inforegister „Steuerliche Angaben“](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="825a8-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="825a8-132">Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Kreditor** in der Gruppe **Registrierung** **Registrierungskennungen** aus, um die Seite **Adressen verwalten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="825a8-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="825a8-133">Wählen Sie auf der Seite **Adressen verwalten** im Inforegister **Steuerliche Angaben** **Hinzufügen** oder **Bearbeiten** aus, um die Seite **Steuerliche Angaben verwalten** zu öffnen, auf der Sie den Steuerregistrierungseintrag pflegen können.</span><span class="sxs-lookup"><span data-stu-id="825a8-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="825a8-134">Geben Sie auf der Seite **Steuerliche Angaben verwalten** im Inforegister **Quellensteuer** im Feld **Steuerkontonummer (TAN)** die TAN ein.</span><span class="sxs-lookup"><span data-stu-id="825a8-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="825a8-135">Die TAN muss aus vier alphabetischen Zeichen, dann fünf numerischen Zeichen und dann einem alphabetischen Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="825a8-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="825a8-136">Hier ist ein Beispiel: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="825a8-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="825a8-137">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="825a8-137">Close the page.</span></span>
