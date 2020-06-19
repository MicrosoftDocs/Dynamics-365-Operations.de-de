---
title: Erstellen und Anwenden von Bedingungen für einbehaltene Kreditorenbeträge
description: 'Dieses Thema enthält Informationen zum Einrichten und Verwalten von Bedingungen für einbehaltene Kreditorenbeträge:'
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410225"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="b5b65-103">Erstellen und Anwenden von Bedingungen für einbehaltene Kreditorenbeträge</span><span class="sxs-lookup"><span data-stu-id="b5b65-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="b5b65-104">Das Einrichten von Aufbewahrungsbedingungen für Lieferantenzahlungen für ein Projekt ist hilfreich, wenn Ihre Organisation einen Teil der an einen Lieferanten geleisteten Zahlungen behalten möchte.</span><span class="sxs-lookup"><span data-stu-id="b5b65-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="b5b65-105">Zum Beispiel, wenn Sie die Zahlung an einen Lieferanten halten möchten, bis die gelieferten Produkte Ihren Erwartungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b5b65-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="b5b65-106">Wenn Sie mit einem Kreditor verhandeln, können Sie Bedingungen für das Einbehalten der Kreditorenzahlungsbeträgen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b5b65-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="b5b65-107">Bedingungen für einbehaltene Kreditorenzahlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="b5b65-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="b5b65-108">Sie können den einzubehaltenden Prozentsatz einer Kreditorenzahlung eingeben wie auch den freizugebenden Prozentsatz der zuvor einbehaltenen Beträge.</span><span class="sxs-lookup"><span data-stu-id="b5b65-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="b5b65-109">Beträge werden bei Kreditorenrechnungen automatisch einbehalten, bis der festgelegte Vollendungsgrad erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="b5b65-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="b5b65-110">Nachdem Sie die Bedingungen für den Einbehalt für einen Kreditor eingerichtet haben, können Sie diese auf jedes beliebige Projekt anwenden, an dem der Kreditor beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="b5b65-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="b5b65-111">Folgen Sie diesen Schritten, um die Bedingungen für den Einbehalt von Kreditorenzahlungen einzurichten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="b5b65-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="b5b65-112">Gehen Sie zu **Projektmanagement und Buchhaltung** > **Aufbewahrung** > **Aufbewahrungsbedingungen für Lieferantenzahlungen**.</span><span class="sxs-lookup"><span data-stu-id="b5b65-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="b5b65-113">Wählen Sie **Neu**, um eine neue Bedingung für einbehaltene Kreditorenbeträge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b5b65-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="b5b65-114">Der Wert **Regelkennung** für die neue Bedingung wird automatisch eingegeben.</span><span class="sxs-lookup"><span data-stu-id="b5b65-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="b5b65-115">Geben Sie eine kurze Beschreibung in das Feld **Beschreibung** ein und wählen Sie auf dem Inforegister **Bedingungen** **Zeile hinzufügen** aus, um die Bedingungswerte für Folgendes einzugeben:</span><span class="sxs-lookup"><span data-stu-id="b5b65-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="b5b65-116">Geben Sie im Feld **Prozentsatz gelieferter Einheiten** einen Vollendungsgrad für die Bestimmung ein.</span><span class="sxs-lookup"><span data-stu-id="b5b65-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="b5b65-117">Beträge werden bei Kreditorenrechnungen automatisch einbehalten, bis die Projektvollendungsstufe gleich dem Prozentsatz ist, den Sie eingeben haben.</span><span class="sxs-lookup"><span data-stu-id="b5b65-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="b5b65-118">Beispiel: Bei der Eingabe von 50.00 werden Beträge einbehalten, bis das Projekt zu 50 Prozent abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b5b65-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="b5b65-119">Geben Sie im Feld **: Einzubehaltender Prozentsatz** den einzubehaltenden Prozentsatz eines Kreditorenrechnungsbetrags ein.</span><span class="sxs-lookup"><span data-stu-id="b5b65-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="b5b65-120">Wenn Sie beispielsweise 10,00 in dieses Feld eingeben, werden 10 Prozent des Betrags für Kreditorenrechnungen einbehalten, bis das Projekt den Vollendungsgrad erreicht, den Sie im Feld **Prozentsatz der gelieferten Einheiten** festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="b5b65-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="b5b65-121">**Feizugebender Prozentsatz**: Geben Sie im Feld **Zeile hinzufügen** den Prozentsatz zuvor einbehaltener Kreditorenrechnungsbeträge ein, die beim ausgewählten Vollendungsgrad des Projekts freizugeben sind.</span><span class="sxs-lookup"><span data-stu-id="b5b65-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="b5b65-122">Wenn Sie mehrere Meilensteine für verschiedene Vollendungsgrade des Projekts bestimmt haben, geben Sie für jede Einbehaltungsregel eine separate Position für Bedingungen für die einbehaltenen Kreditorenbeträge ein.</span><span class="sxs-lookup"><span data-stu-id="b5b65-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="b5b65-123">Jede Position kann jeweils unterschiedliche Prozentsätze zur Einbehaltung oder zur Prozentsätze für die Freigabe für jeden Vollendungsgrad des Projekts bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b5b65-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="b5b65-124">Nachdem Sie die Bedingungen für den Einbehalt für einen Kreditor eingerichtet haben, können Sie diese auf ein Projekt anwenden, an dem der Kreditor beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="b5b65-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="b5b65-125">Wenden Sie Lieferantenbindungsbedingungen auf ein Projekt an</span><span class="sxs-lookup"><span data-stu-id="b5b65-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="b5b65-126">Gehen Sie zu **Projektmanagement und Buchhaltung** > **Projekte** > **Alle Projekte** und öffnen Sie ein Projekt auf der Projektlistenseite.</span><span class="sxs-lookup"><span data-stu-id="b5b65-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="b5b65-127">Wählen Sie im Inforegister **Kreditorenvereinbarungen** die Option **Position hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b5b65-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="b5b65-128">Wählen Sie im **Kontocodefeld** eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="b5b65-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="b5b65-129">**Tabelle**: Die Bedingungen für einbehaltene Kreditorenbeträge gelten für einen einzelnen Kreditor.</span><span class="sxs-lookup"><span data-stu-id="b5b65-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="b5b65-130">**Gruppe**: Die Bedingungen für einbehaltene Kreditorenbeträge gelten für alle Kreditoren in einer Kreditorengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5b65-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="b5b65-131">**Alle**: Die Bedingungen für einbehaltene Kreditorenbeträge gelten für alle Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="b5b65-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="b5b65-132">Wählen Sie im **Kreditor/Kreditorengruppenfeld** den Kreditor oder die Kreditorengruppe aus, für die die Bedingungen für einbehaltene Kreditorenbeträge gelten.</span><span class="sxs-lookup"><span data-stu-id="b5b65-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="b5b65-133">(Dieses Feld ist nur verfügbar, wenn im vorangegangenen Schritt nicht die Option **Alle** ausgewählt wurde.)</span><span class="sxs-lookup"><span data-stu-id="b5b65-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="b5b65-134">Wählen Sie im Feld **Bedingungen für einbehaltene Kreditorenbeträge** die Bedingungen für einbehaltene Kreditorenbeträge aus, die Sie im vorherigen Verfahren erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b5b65-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="b5b65-135">Wenn das Projekt auch Pay-When-Paid (PWP)-Begriffe für den Kreditor enthält, geben Sie in das Feld **Pay When Paid - Schwellenwertprozentsatz** den Schwellenwertprozentsatz für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="b5b65-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="b5b65-136">Die Bedingungen für einbehaltene Kreditorenbeträge werden auch in Bestellungen angezeigt, die Sie für den Kreditor erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b5b65-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
