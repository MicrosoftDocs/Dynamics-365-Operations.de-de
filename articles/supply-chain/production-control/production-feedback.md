---
title: Produktionsrückmeldung
description: Dieser Artikel enthält Informationen über Produktionsrückmeldungen, die den Arbeitskräften ein Feedback zu Produktionseinzelvorgängen geben. Der Artikel umfasst Informationen zu den verschiedenen Methoden, wie Produktionsrückmeldungen aktualisiert werden können.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b0a49cf05a7eee838dcf9fb699d273d0f7518a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "340912"
---
# <a name="production-feedback"></a><span data-ttu-id="52cce-104">Produktionsrückmeldung</span><span class="sxs-lookup"><span data-stu-id="52cce-104">Production feedback</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52cce-105">Dieser Artikel enthält Informationen über Produktionsrückmeldungen, die den Arbeitskräften ein Feedback zu Produktionseinzelvorgängen geben.</span><span class="sxs-lookup"><span data-stu-id="52cce-105">This article provides information about production feedback, which gives workers feedback about production jobs.</span></span> <span data-ttu-id="52cce-106">Der Artikel umfasst Informationen zu den verschiedenen Methoden, wie Produktionsrückmeldungen aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="52cce-106">The article includes information about the various ways that production feedback can be updated.</span></span>

<span data-ttu-id="52cce-107">Produktionsrückmeldung gibt Arbeitskräften Feedback zu Produktionseinzelvorgängen.</span><span class="sxs-lookup"><span data-stu-id="52cce-107">Production feedback gives workers feedback about production jobs.</span></span> <span data-ttu-id="52cce-108">Sie zeichnet Zeit und Materialentnahme für Produktionsaufträge, Arbeitsgangmengen und Statusangaben sowie Fehler auf, die einen Einzelvorgang oder einen Arbeitsgang fehlschlagen lassen.</span><span class="sxs-lookup"><span data-stu-id="52cce-108">It records time and material consumption on production orders, operation quantities and status, and errors that cause a job or operation to fail.</span></span> <span data-ttu-id="52cce-109">Produktionsrückmeldung kann in Erfassungen aktualisiert werden, die sich auf Produktionsaufträge beziehen.</span><span class="sxs-lookup"><span data-stu-id="52cce-109">Production feedback can be updated in journals that are related to production orders.</span></span> <span data-ttu-id="52cce-110">Die Erfassungen **Produktion - Einzelvorgangsliste** und **Produktion - Arbeitsplanliste** werden verwendet, um Zeit und Mengen pro Einzelvorgang oder Arbeitsgang zu melden.</span><span class="sxs-lookup"><span data-stu-id="52cce-110">The **Production job card** and **Production route card** journals are used to report time and quantities per job or operation.</span></span> <span data-ttu-id="52cce-111">Bei Berichten zum letzten Einzelvorgang oder Arbeitsgang können Mengen im Produkt als fertig gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="52cce-111">For reporting about the last job or operation, quantities on the finished product can be reported as finished.</span></span> <span data-ttu-id="52cce-112">Produktionsrückmeldung kann auch auf den Seiten **Terminal Einzelvorgangsliste** und **Einzelvorgangslistengerät** aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="52cce-112">Production feedback can also be updated on the **Job card terminal** and **Job card device** pages.</span></span> <span data-ttu-id="52cce-113">Diese Seiten aktivieren, dass Produktionsrückmeldung für den Fertigungsbereich aktualisiert wird, und sind Teil der Fertigungssteuerungsfunktionen im Modul  **Produktionssteuerung**.</span><span class="sxs-lookup"><span data-stu-id="52cce-113">These pages enable production feedback to be updated on the shop floor and are part of the manufacturing execution functionality in the **Production control** module.</span></span> <span data-ttu-id="52cce-114">Die Seite **Terminal Einzelvorgangsliste** enthält eine konfigurierbare Benutzeroberfläche, die eine Liste der freigegebenen Einzelvorgänge in einem priorisierten Auftrag für einen ausgewählten Arbeitsbereich anzeigt.</span><span class="sxs-lookup"><span data-stu-id="52cce-114">The **Job card terminal** page has a configurable user interface that shows a list of the released jobs in a prioritized order for a selected work area.</span></span> <span data-ttu-id="52cce-115">Sie bietet auch erweiterte Optionen wie Bündelung von Einzelvorgängen und Teamarbeit.</span><span class="sxs-lookup"><span data-stu-id="52cce-115">It also offers advanced options such as job bundling and team work.</span></span> <span data-ttu-id="52cce-116">Die Seite **Einzelvorgangslistengerät** hat eine für Fingereingaben optimierte Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="52cce-116">The **Job card device** page has a touch-optimized user interface.</span></span> <span data-ttu-id="52cce-117">Produktionsrückmeldung wird auf beiden Seiten aus den Produktionserfassungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="52cce-117">Production feedback on both pages is updated from the production journals.</span></span>



