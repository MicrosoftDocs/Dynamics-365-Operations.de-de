---
title: Automatische Belastungen nach Kanal aktivieren und konfigurieren
description: In diesem Thema wird erläutert, wie Sie automatische Gebühren nach Kanal in Microsoft Dynamics 365 Commerce aktivieren und konfigurieren.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d37b2b785dd29850dcd02d0905e5872445384990
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993727"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="a623b-103">Automatische Belastungen nach Kanal aktivieren und konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a623b-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="a623b-104">In diesem Thema wird erläutert, wie Sie automatische Gebühren nach Kanal in Microsoft Dynamics 365 Commerce aktivieren und auch konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a623b-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a623b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a623b-105">Overview</span></span>

<span data-ttu-id="a623b-106">Möglicherweise gibt es Szenarien, in denen Recyclinggebühren oder andere Gebühren auf eine Gruppe von Produkten erhoben werden müssen, die in allen oder einigen Geschäften in einem bestimmten Bundesstaat (z. B. Kalifornien) verkauft werden.</span><span class="sxs-lookup"><span data-stu-id="a623b-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="a623b-107">Die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** in Commerce lässt Sie automatische Gebühren nach Kanal festlegen (z. B. einen bestimmten stationären Kanal).</span><span class="sxs-lookup"><span data-stu-id="a623b-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="a623b-108">Diese Funktion wird in Dynamics 365 Commerce Version 10.0.10 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a623b-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="a623b-109">Um automatische Gebühren nach Kanal zu aktivieren und zu konfigurieren, müssen Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="a623b-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="a623b-110">Aktivieren Sie **Aktivieren Sie die automatische Filterladung nach Kanal**.</span><span class="sxs-lookup"><span data-stu-id="a623b-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="a623b-111">Konfigurieren Sie die Organisationshierarchiezwecke.</span><span class="sxs-lookup"><span data-stu-id="a623b-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="a623b-112">Definieren Sie automatische Gebühren nach Kanal.</span><span class="sxs-lookup"><span data-stu-id="a623b-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="a623b-113">Die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** funktioniert nur, wenn die erweiterte Funktion zum automatischen Laden ebenfalls aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a623b-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="a623b-114">Informationen zum Aktivieren der erweiterten Funktion für automatische Gebühren finden Sie unter [Erweiterte automatische Omni-Channel-Gebühren](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="a623b-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="a623b-115">Starten Sie Aktivieren Sie die automatische Filterladung nach Kanal</span><span class="sxs-lookup"><span data-stu-id="a623b-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="a623b-116">Führen Sie die folgenden Schritte aus, um automatische Gebühren nach Kanal in Commerce zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a623b-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a623b-117">Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="a623b-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="a623b-118">Auf der Registerkarte **Nicht aktiviert** in der Liste **Funktionsname** finden und wählen Sei **Aktivieren Sie die automatische Filterladung nach Kanal**.</span><span class="sxs-lookup"><span data-stu-id="a623b-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="a623b-119">Wählen Sie in der unteren rechten Ecke **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="a623b-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="a623b-120">Nachdem die Funktion aktiviert wurde, wird sie in der Liste auf der Registerkarte **Alle** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a623b-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="a623b-121">Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="a623b-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a623b-122">Suchen und wählen Sie im linken Bereich den Auftrag **1110** ( **Globale Konfiguration**).</span><span class="sxs-lookup"><span data-stu-id="a623b-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="a623b-123">Wählen Sie im Aktionsbereich **jetzt ausführen**, um die Konfigurationsänderungen zu verbreiten.</span><span class="sxs-lookup"><span data-stu-id="a623b-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="a623b-124">Wenn Sie die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** ausschalten, nachdem Sie sie bereits verwendet haben, wird das Feld unter **Einzelhandelskanalbeziehung** unter **Automatische Aufladung** nicht mehr angezeigt und Sie verlieren alle vorhandenen Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="a623b-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="a623b-125">Wenn die Entfernung der Konfiguration **Einzelhandelskanalbeziehung** die Regeln für automatische Gebühren dupliziert, schlägt der Versuch zur Deaktivierung fehl.</span><span class="sxs-lookup"><span data-stu-id="a623b-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="a623b-126">Überprüfen Sie vor dem Deaktivieren der Funktion unbedingt alle Regeln für automatische Gebühren und nehmen Sie die erforderlichen Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="a623b-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="a623b-127">Konfigurieren Sie die Organisationshierarchiezwecke</span><span class="sxs-lookup"><span data-stu-id="a623b-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="a623b-128">Ein neuer Zweck der Organisationshierarchie, der **Automatische Gebühr für den Einzelhandel** benannt wird, wurde erstellt, um die Hierarchie für automatische Gebühren nach Kanal zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a623b-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="a623b-129">Führen Sie die folgenden Schritte aus, um einem Organisationshierarchiezweck in Commerce eine Standardhierarchie zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a623b-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="a623b-130">Wechseln Sie zu **Organisationsverwaltung \> Organisationen \> Organisationshierarchiezwecke**.</span><span class="sxs-lookup"><span data-stu-id="a623b-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="a623b-131">Wählen Sie im linken Bereich **Automatische Gebühr für den Einzelhandel** aus.</span><span class="sxs-lookup"><span data-stu-id="a623b-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="a623b-132">Unter **Zugeordnete Hierarchien** wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a623b-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="a623b-133">In dem Dialogfeld **Organisationshierarchien** wählen Sie im Dialogfeld eine Organisationshierarchie aus (z. B. **Einzelhandelsgeschäfte nach Regionen**) und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="a623b-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="a623b-134">Unter **Zugeordnete Hierarchien** wählen Sie **Als Standard festlegen**.</span><span class="sxs-lookup"><span data-stu-id="a623b-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="a623b-135">Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="a623b-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a623b-136">Suchen und wählen Sie im linken Bereich den Auftrag **1040** (**Produkte**).</span><span class="sxs-lookup"><span data-stu-id="a623b-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="a623b-137">Wählen Sie im Aktivitätsbereich **Jetzt ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="a623b-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="a623b-138">Wiederholen Sie die beiden vorherigen Schritte, um Aufträge **1070** (**Kanalkonfiguration**) und **1110** (**Globale Konfiguration**) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a623b-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Konfiguration des Hierarchiezwecks der automatischen Organisation für den Einzelhandel](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="a623b-140">Definieren Sie automatische Gebühren nach Kanal</span><span class="sxs-lookup"><span data-stu-id="a623b-140">Define auto charges by channel</span></span>

<span data-ttu-id="a623b-141">Nachdem Sie die Funktion **Aktivieren Sie die automatische Filterladung nach Kanal** aktiviert und den Organisationshierarchiezweck **Automatische Belastung für den Einzelhandel** konfiguriert haben, können automatische Gebühren nach Kanal entweder auf der Ebene der Auftragskopfzeilen oder auf der Ebene der Auftragspositionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a623b-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="a623b-142">Führen Sie die folgenden Schritte aus, um automatische Gebühren nach Kanal in Commerce zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a623b-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a623b-143">Wechseln Sie zu **Debitoren \> Belastungen einrichten \> Auto-Belastungen**.</span><span class="sxs-lookup"><span data-stu-id="a623b-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="a623b-144">Im linken Bereich im Feld **Ebene** wählen Sie entweder **Kopf** oder **Linie** aus, abhängig von Ihren Geschäftsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="a623b-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="a623b-145">In dem Feld **Retail Channel-Code** wählen Sie im Feld den entsprechenden Kanalcode aus (z. B. **Tabelle** oder **Gruppe**).</span><span class="sxs-lookup"><span data-stu-id="a623b-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="a623b-146">Wenn die Standardeinstellung, **Alle** verwendet wird, werden Gebührenregeln auf alle Kanäle angewendet.</span><span class="sxs-lookup"><span data-stu-id="a623b-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="a623b-147">Wenn Sie **Gruppe** auswählen, stellen Sie sicher, dass eine Gebührengruppe für Einzelhandelskanäle unter **Einzelhandel und Handel \> Kanaleinrichtung \> Gebühren \> Gebührengruppen für Einzelhandelskanäle** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a623b-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="a623b-148">Wenn Sie **Tabelle** auswählen, können Sie einen bestimmten Kanal auswählen (z. B. **San Francisco**) in dem Feld **Einzelhandelskanalbeziehung**.</span><span class="sxs-lookup"><span data-stu-id="a623b-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="a623b-149">Gehen Sie zu **Retail and Commerce \> Retail and Commerce IT \> Vertriebsplan**.</span><span class="sxs-lookup"><span data-stu-id="a623b-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a623b-150">Suchen und wählen Sie im linken Bereich den Auftrag **1040** (**Produkte**).</span><span class="sxs-lookup"><span data-stu-id="a623b-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="a623b-151">Wählen Sie im Aktivitätsbereich **Jetzt ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="a623b-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="a623b-152">Wiederholen Sie die beiden vorherigen Schritte, um Aufträge **1070** (**Kanalkonfiguration**) und **1110** (**Globale Konfiguration**) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a623b-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Automatische Gebühren nach Kanal definiert](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="a623b-154">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="a623b-154">Example scenario</span></span>

<span data-ttu-id="a623b-155">Im folgenden Beispiel werden die Schritte beschrieben, die zum Konfigurieren eines Produkts erforderlich sind, damit beim Verkauf des Produkts über einen stationären Kanal in San Francisco Recyclinggebühren erhoben werden.</span><span class="sxs-lookup"><span data-stu-id="a623b-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="a623b-156">Das Beispiel zeigt auch, wie die automatischen Gebühren in der POS-Anwendung (Commerce Point of Sale) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a623b-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="a623b-157">Die Organisation definiert einen Gebührencode, der **RECYCELN** benannt wird, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a623b-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![RECYCLE berechnet den Code](media/Auto-charges-charge-code.png)

<span data-ttu-id="a623b-159">Eine automatische Belastung wird auf Positionsebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="a623b-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="a623b-160">Es weist die folgenden Konfigurationen auf:</span><span class="sxs-lookup"><span data-stu-id="a623b-160">It has the following configuration:</span></span>

- <span data-ttu-id="a623b-161">Das Feld **Kontocode** ist festgelegt auf **Alle** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="a623b-162">Das Feld **Artikelcode** ist auf **Tabelle** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="a623b-163">Das Feld **Artikelbeziehung** ist auf Produkt-ID **91001** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="a623b-164">Das Feld **Lieferungscode-Modus** ist auf **Alle** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="a623b-165">Das Feld **Retail Channel Code** ist auf **Tabelle** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="a623b-166">Das Feld **Retail Channel Beziehung** ist auf Geschäft **San Francisco** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="a623b-167">Eine automatische Gebührenzeile wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="a623b-167">An auto charges line is created.</span></span> <span data-ttu-id="a623b-168">Es weist die folgenden Konfigurationen auf:</span><span class="sxs-lookup"><span data-stu-id="a623b-168">It has the following configuration:</span></span>

- <span data-ttu-id="a623b-169">Das Feld **Währung** wird mit auf **USD** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="a623b-170">Das Feld **Belstungscode** ist auf **RECYCLE** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="a623b-171">Das Feld **Kategorie** ist auf **Fest** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="a623b-172">Das Feld **Belastung** wird mit auf **$6.25** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a623b-172">The **Charges** field is set to **$6.25**.</span></span>

![Konfiguration der Zeile automatischen Belastungsebene und automatische Belastung](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="a623b-174">In der POS-Anwendung wird ein Auftrag im Shopkanal **San Francisco** erstellt.</span><span class="sxs-lookup"><span data-stu-id="a623b-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="a623b-175">Die Position **Belastungen** zeigen die Recyclinggebühr von **6,25 $**.</span><span class="sxs-lookup"><span data-stu-id="a623b-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="a623b-176">Durch die Auswahl von **Transaktionsoptionen \> Gebühren \> Gebühren verwalten** in der POS-Anwendung können Sie den Gebührencode und die Beschreibung der Recyclinggebühr anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a623b-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Recyclinggebühr in der POS-Anwendung](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="a623b-178">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a623b-178">Additional resources</span></span>

[<span data-ttu-id="a623b-179">Erweiterte automatische Omni-Channel-Belastungen</span><span class="sxs-lookup"><span data-stu-id="a623b-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="a623b-180">Kopfbelastungen auf übereinstimmende Verkaufspositionen aufteilen</span><span class="sxs-lookup"><span data-stu-id="a623b-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)
