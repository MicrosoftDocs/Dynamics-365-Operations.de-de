---
title: Verbesserte Handhabung von Artikeln mit Chargenverfolgung
description: Dieses Thema behandelt die vorgenommenen Verbesserungen bei der Handhabung von Artikeln mit Chargenverfolgung beim Aufstellungsbuchungsprozess.
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799708"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="95450-103">Verbesserte Handhabung von Artikeln mit Chargenverfolgung</span><span class="sxs-lookup"><span data-stu-id="95450-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="95450-104">In der Verkaufsstelle (POS) können für Artikel mit Chargenverfolgung zum Zeitpunkt des Verkaufs keine POS-Chargennummern erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="95450-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="95450-105">Bei bestimmten Konfigurationen aber, wenn Umsätze am Hauptsitz mittels Kundenaufträgen oder Auszugsbuchungen gebucht werden, wird im Microsoft Dynamics-System davon ausgegangen, dass für Artikel mit Chargenverfolgung gültige Chargennummern vorliegen und bei der Rechnungsabwicklung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95450-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="95450-106">Wenn gültige Chargennummern für Produkte vorhanden sind, werden sie vom Prozess zur Berechnung von Debitorenaufträgen und Aufträgen der Auszugsbuchung verwendet.</span><span class="sxs-lookup"><span data-stu-id="95450-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="95450-107">Andernfalls kann die Debitorenrechnung nicht gebucht werden und der POS-Benutzer erhält eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="95450-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="95450-108">Die Auszugsbuchung wechselt dann in den Fehlerstatus.</span><span class="sxs-lookup"><span data-stu-id="95450-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="95450-109">Dieser Fehlerstatus tritt auf, wenn für die Produkte ein negativer Bestand aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="95450-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="95450-110">Dank der Verbesserungen, die in Retail ab Version 10.0.4 vorgenommen wurden, wird bei Artikeln, deren Bestand 0 (null) ist oder wenn keine Chargennummer vorhanden ist, die Berechnung von Debitorenaufträgen und Aufträgen durch die Auszugsbuchung nicht blockiert, wenn für Artikel mit Chargenverfolgung ein negativer Bestand aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="95450-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="95450-111">Sind keine Chargennummern vorhanden, verwendet die neue Funktion für die Verkaufspositionen eine Standardkennung.</span><span class="sxs-lookup"><span data-stu-id="95450-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="95450-112">Um die Standardchargenkennung für Debitorenaufträge festzulegen, legen Sie auf der Seite **Handelsparameter** auf der Registerkarte **Debitorenaufträge** auf dem Inforegister **Auftrag** das Feld **Standardchargenkennung** fest.</span><span class="sxs-lookup"><span data-stu-id="95450-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="95450-113">Um die Standardchargenkennung für die Berechnung von Aufträgen im Zuge der Auszugsbuchung festzulegen, legen Sie auf der Seite **Handelsparameter** auf der Registerkarte **Buchung** auf dem Inforegister **Lageraktualisierung** das Feld **Standardchargenkennung** fest.</span><span class="sxs-lookup"><span data-stu-id="95450-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="95450-114">Diese Funktion ist nur dann verfügbar, wenn für den entsprechenden Filiallagerort und die Artikel die erweiterte Lagerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="95450-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="95450-115">In einer späteren Version wird die Funktion auch in Fällen unterstützt, in denen keine erweiterte Lagerung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95450-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="95450-116">Die Unterstützung für eine verbesserte Handhabung von per Stapel nachverfolgten Artikeln bei der Aufstellungsbuchung einfacher Lagerverwaltungsszenarien wurde in Retail-Version 10.0.5 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="95450-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]