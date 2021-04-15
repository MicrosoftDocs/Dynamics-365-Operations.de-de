---
title: Erstellen und Aktualisieren einer Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal
description: In diesem Thema wird erläutert, wie Sie eine Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal einrichten.
author: ShalabhjainMSFT
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: e23291130d55fdfb5c2e2077b78c221866d72c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792074"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="cf530-103">Retouren- und Rückerstattungsrichtlinie für einen Kanal erstellen und aktualisieren</span><span class="sxs-lookup"><span data-stu-id="cf530-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf530-104">Die Kanal-Rücklieferungsrichtlinie in Dynamics 365 Commerce ermöglicht Einzelhändlern, Durchsetzungsbestimmungen für Zahlungsmittel festzulegen, die für die Verarbeitung einer Rücklieferung an einem POS-Gerät (Point of Sale) zugelassen werden können.</span><span class="sxs-lookup"><span data-stu-id="cf530-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="cf530-105">In diesem Thema werden die Schritte beschrieben, wie Sie eine Rücklieferungs- und Rückerstattungsrichtlinie für einen Kanal einrichten.</span><span class="sxs-lookup"><span data-stu-id="cf530-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="cf530-106">Der Geltungsbereich der Richtlinie beschränkt sich derzeit auf die Festlegung der Zahlungsmittel, die für einen Kanal zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cf530-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="cf530-107">Die Liste „Zulässig“ basiert auf den Zahlungsmethoden, die für den Kauf verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="cf530-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="cf530-108">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cf530-108">For example:</span></span>

- <span data-ttu-id="cf530-109">Wenn ein Kauf mit einer Geschenkkarte getätigt wurde, besteht die Shoprichtlinie darin, Rückerstattungen nur für eine neue Geschenkkarte zu verarbeiten oder eine Gutschrift für den Shop zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="cf530-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="cf530-110">Wenn ein Verkauf mit Bargeld erfolgte, sind die zulässigen Optionen für die Rückerstattung Bargeld, Geschenkkarte und Kundenkonto, jedoch keine Kreditkarte.</span><span class="sxs-lookup"><span data-stu-id="cf530-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="cf530-111">Aktivieren der Rücklieferungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="cf530-111">Enable return policy</span></span>

<span data-ttu-id="cf530-112">Gehen Sie wie folgt vor, um die Funktion der Kanal-Rücklieferungsrichtlinie zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="cf530-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="cf530-113">Gehen Sie in Dynamics 365 Commerce zum Arbeitsbereich **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="cf530-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="cf530-114">Suchen Sie in der Liste der Funktionsnamen nach der Funktion **Aktivieren der Kanal-Rücklieferungsrichtlinien**.</span><span class="sxs-lookup"><span data-stu-id="cf530-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="cf530-115">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="cf530-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="cf530-116">Konfigurieren der Rücklieferungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="cf530-116">Configure return policy</span></span>

<span data-ttu-id="cf530-117">Folgen Sie diesen Schritten, um eine Rücklieferungsrichtlinie für einen Einzelhandelsshop oder einen Online-Einzelhandelskanal zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf530-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="cf530-118">Gehen Sie zu **Einzelhandel und Handel** \> **Kanaleinrichtung** \> **Rücklieferungen** \> **Kanal-Rücklieferungsrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="cf530-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="cf530-119">Wählen Sie **Neu** aus, um eine neue Rücklieferungsrichtlinienvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cf530-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="cf530-120">Um eine vorhandene Vorlage zu verwenden, wählen Sie die Vorlage im linken Bereich aus.</span><span class="sxs-lookup"><span data-stu-id="cf530-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="cf530-121">Fügen Sie für neue Vorlagen einen Namen und eine Beschreibung hinzu, anhand derer Sie die Richtlinie identifizieren können, wenn sie auf den Kanal angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf530-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="cf530-122">![Hinzufügen einer neuen Rücklieferungsrichtlinie](media/Return-policy-page1.png "Hinzufügen einer neuen Rücklieferungsrichtlinie")</span><span class="sxs-lookup"><span data-stu-id="cf530-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="cf530-123">Definieren Sie im Abschnitt **Zulässige Rückerstattungszahlungsmethoden** die **zulässigen** Rücklieferungszahlungsmittel, die für jede Zahlungsmethode spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="cf530-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="cf530-124">![Hinzufügen von Zahlungsmethoden](media/Return-policy-page2.PNG "Festlegen zulässiger Zahlungsmethoden pro Zahlungstyp")</span><span class="sxs-lookup"><span data-stu-id="cf530-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="cf530-125">Die Zahlungsmethoden leiten sich aus den für die Organisation festgelegten Zahlungsmethoden ab.</span><span class="sxs-lookup"><span data-stu-id="cf530-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="cf530-126">Durch Hinzufügen eines zulässigen Rücklieferungszahlungsmitteltyps für jede aufgelistete Zahlungsmethode wird sichergestellt, dass Rücklieferungen an den zulässigen Rücklieferungszahlungsmitteltyp erfolgen können.</span><span class="sxs-lookup"><span data-stu-id="cf530-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="cf530-127">Ordnen Sie die Rücklieferungsrichtlinienvorlage den Filialen zu, in denen sie verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf530-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="cf530-128">Wählen Sie in der Registerkarte **Retail Channels** die Option **Hinzufügen** aus und ordnen Sie die verfügbaren Kanäle zu.</span><span class="sxs-lookup"><span data-stu-id="cf530-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="cf530-129">Wählen Sie im Dialogfenster **Organisationsknoten auswählen** die Filialen, Regionen und Organisationen aus, denen die Vorlage zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf530-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="cf530-130">Jeder Filiale kann nur eine Rücklieferungsrichtlinienvorlage zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="cf530-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="cf530-131">Verwenden Sie die Pfeiltasten, um Filialen, Regionen oder Organisationen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="cf530-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="cf530-132">Das Gültigkeitsdatum der Richtlinie ist das Datum, an dem die Richtlinien auf die Kanäle angewendet und die Kanalvorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cf530-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="cf530-133">![Auswählen des Organisationsknoten-Dialogfensters](media/Return-policy-page3.PNG "Auswählen des Organisationsknoten-Dialogfensters")</span><span class="sxs-lookup"><span data-stu-id="cf530-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="cf530-134">Führen Sie auf der Seite **Verteilungszeitplan** den Vorgang **1070** durch, um die Kanal-Rücklieferungsrichtlinie für den POS verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="cf530-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="cf530-135">Vorschau der Kanal-Rücklieferungsrichtlinie im POS</span><span class="sxs-lookup"><span data-stu-id="cf530-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="cf530-136">Folgen Sie den Schritten in einem der folgenden Beispiele, um die zulässigen Rücklieferungszahlungsmitteltypen im POS anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf530-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="cf530-137">Melden Sie sich als Kassierer oder Manager am POS an.</span><span class="sxs-lookup"><span data-stu-id="cf530-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="cf530-138">Wählen Sie unter **Schicht und Kasse** die Option **Erfassung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="cf530-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="cf530-139">Wählen Sie die Transaktion aus, die Teil der Rücklieferung ist.</span><span class="sxs-lookup"><span data-stu-id="cf530-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="cf530-140">Wählen Sie die Artikel, die erstattet werden sollen, und die Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="cf530-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="cf530-141">Befindet sich das ausgewählte Zahlungsmittel in der Liste der zulässigen Rücklieferungszahlungsmitteltypen, kann der Kassierer die Transaktion abschließen.</span><span class="sxs-lookup"><span data-stu-id="cf530-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="cf530-142">Wenn das ausgewählte Zahlungsmittel nicht zulässig ist, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf530-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="cf530-143">Wählen Sie **Fälliger Betrag** aus, um eine Liste aller zulässigen Rücklieferungszahlungsmitteltypen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf530-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="cf530-144">– oder –</span><span class="sxs-lookup"><span data-stu-id="cf530-144">-or-</span></span>

1. <span data-ttu-id="cf530-145">Melden Sie sich als Kassierer oder Manager am POS an.</span><span class="sxs-lookup"><span data-stu-id="cf530-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="cf530-146">Wählen Sie **Rücklieferungstransaktion** aus und geben Sie die Quittungs-ID mit einem Barcode-Scan oder durch manuelle Eingabe ein.</span><span class="sxs-lookup"><span data-stu-id="cf530-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="cf530-147">Wählen Sie die Transaktion aus, die Teil der Rücklieferung ist.</span><span class="sxs-lookup"><span data-stu-id="cf530-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="cf530-148">Wählen Sie die Artikel, die erstattet werden sollen, und die Zahlungsmethode aus.</span><span class="sxs-lookup"><span data-stu-id="cf530-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="cf530-149">Befindet sich das ausgewählte Zahlungsmittel in der Liste der zulässigen Rücklieferungszahlungsmitteltypen, kann der Kassierer die Transaktion abschließen.</span><span class="sxs-lookup"><span data-stu-id="cf530-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="cf530-150">Wenn das ausgewählte Zahlungsmittel nicht zulässig ist, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf530-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="cf530-151">Wählen Sie **Fälliger Betrag** aus, um eine Liste aller zulässigen Rücklieferungszahlungsmitteltypen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cf530-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="cf530-152">![Nicht zulässige Rückerstattung](media/Return-policy-page6.png "Nicht zulässiger Rückerstattungstyp")</span><span class="sxs-lookup"><span data-stu-id="cf530-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="cf530-153">![Liste der Zahlungsmethoden](media/Return-policy-page5.PNG "Zulässige Rückerstattungstypen")</span><span class="sxs-lookup"><span data-stu-id="cf530-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
