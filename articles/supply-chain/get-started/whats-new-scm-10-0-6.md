---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.6. (November 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Supply Chain Management 10.0.6 neu oder geändert wurden.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 83798af9c39ae8845125026903741882356d8845
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909328"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="94c2a-103">Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.6. (November 2019)</span><span class="sxs-lookup"><span data-stu-id="94c2a-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94c2a-104">In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Supply Chain Management 10.0.6 entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="94c2a-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="94c2a-105">Diese Version hat eine Build-Nummer von 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="94c2a-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="94c2a-106">Während das allgemeine Verfügbarkeitsdatum im November liegt, sind die neuen Funktionen für die vorzeitige Veröffentlichung im Oktober verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94c2a-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="94c2a-107">Weitere Informationen zur Version 10.0.6 finden Sie unter [zusätzliche Ressourcen](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="94c2a-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="94c2a-108">Produktkonfigurationsmodelle V2 Datenentität</span><span class="sxs-lookup"><span data-stu-id="94c2a-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="94c2a-109">Eine zweite Version für die Dateneinheit Produktkonfigurationsmodelle wird veröffentlicht (als Produktkonfigurationsmodelle V2 bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="94c2a-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="94c2a-110">Die Standardvorlage 418-Produktkonfigurationsmodelle muss ebenfalls so sein, dass sie die neue Datenentität Produktkonfigurationsmodelle V2 in den Import/Export-Framework-Vorlagen verwendet.</span><span class="sxs-lookup"><span data-stu-id="94c2a-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="94c2a-111">Die Vorlage wird nicht automatisch aktualisiert, sodass Sie die Vorlage manuell von der Standardeinstellung laden müssen.</span><span class="sxs-lookup"><span data-stu-id="94c2a-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="94c2a-112">Die V2-Entität exportiert eine Zeile als separate Datei in einen Anhang anstatt inline, wodurch die Größenbeschränkungen der V1-Entität gelöst werden.</span><span class="sxs-lookup"><span data-stu-id="94c2a-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="94c2a-113">Was müssen Sie tun, um diese Änderung vorzunehmen?</span><span class="sxs-lookup"><span data-stu-id="94c2a-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="94c2a-114">Da die V1-Entität veraltet ist, sollten Sie mit der Migration von V1 auf V2 beginnen.</span><span class="sxs-lookup"><span data-stu-id="94c2a-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="94c2a-115">Wenn Sie die Vorlage 418-Produktkonfigurationsmodelle verwenden, können Sie auf die Schaltfläche Standardvorlagen laden klicken und die Vorlage 418 – Produktkonfigurationsmodelle neu laden.</span><span class="sxs-lookup"><span data-stu-id="94c2a-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="94c2a-116">Wenn Sie die Kompatibilität mit vorhandenen Systemen beibehalten möchten, können Sie die vorhandene Vorlage und die (veraltete) V1-Entität vorerst weiter verwenden, bis Sie Ihre Integrationen in die neue Vorlage verschieben.</span><span class="sxs-lookup"><span data-stu-id="94c2a-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="94c2a-117">Funktionsverwaltungsverbesserungen</span><span class="sxs-lookup"><span data-stu-id="94c2a-117">Feature management enhancements</span></span>
<span data-ttu-id="94c2a-118">Mit der Funktionsverwaltung können Sie jetzt standardmäßig alle neuen Funktionen aktivieren, eine Bestätigung zum Aktivieren einer Funktion anfordern und alle Funktionen aktivieren, die noch nicht aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="94c2a-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="94c2a-119">Zuständige Partei für Kaufvertrag</span><span class="sxs-lookup"><span data-stu-id="94c2a-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="94c2a-120">Sie haben jetzt die Möglichkeit, primäre und sekundäre Verantwortliche auf dem Klassifizierungsformular für Kaufverträge und den daraus resultierenden Kaufverträgen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="94c2a-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="94c2a-121">Dadurch erhält der Benutzer Zugriff darauf, wer die Vereinbarungen überwacht.</span><span class="sxs-lookup"><span data-stu-id="94c2a-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="94c2a-122">Angebotsanforderung auf der Bestellungszeile</span><span class="sxs-lookup"><span data-stu-id="94c2a-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="94c2a-123">Sie können einen Referenzlink aus den Bestellpositionen zu den entsprechenden Angebotsanforderungs-Zeilen hinzufügen, aus denen sie stammen, sodass der Benutzer problemlos die unterstützende Angebotsanfrage erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="94c2a-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94c2a-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94c2a-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="94c2a-125">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="94c2a-125">Bug fixes</span></span>
<span data-ttu-id="94c2a-126">Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.6 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) an.</span><span class="sxs-lookup"><span data-stu-id="94c2a-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="94c2a-127">Plattformupdate 30</span><span class="sxs-lookup"><span data-stu-id="94c2a-127">Platform update 30</span></span>
<span data-ttu-id="94c2a-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 enthält das Plattform-Update 30.</span><span class="sxs-lookup"><span data-stu-id="94c2a-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="94c2a-129">Weitere Informationen zum Plattform-Update 30 finden Sie unter [Was ist neu oder geändert in Platform Update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="94c2a-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="94c2a-130">Dynamics 365: 2019 Veröffentlichungsplan Welle 2</span><span class="sxs-lookup"><span data-stu-id="94c2a-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="94c2a-131">Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?</span><span class="sxs-lookup"><span data-stu-id="94c2a-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="94c2a-132">Testen Sie [Dynamics 365: 2019 Release Welle 2 Plan](/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="94c2a-132">Check out the [Dynamics 365: 2019 release wave 2 plan](/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="94c2a-133">Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.</span><span class="sxs-lookup"><span data-stu-id="94c2a-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="94c2a-134">Entfernte und veraltete Supply Chain Management-Funktionen</span><span class="sxs-lookup"><span data-stu-id="94c2a-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="94c2a-135">Das Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94c2a-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="94c2a-136">Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94c2a-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="94c2a-137">Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="94c2a-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="94c2a-138">Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="94c2a-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="94c2a-139">Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate.</span><span class="sxs-lookup"><span data-stu-id="94c2a-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="94c2a-140">In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="94c2a-140">Typically, these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]