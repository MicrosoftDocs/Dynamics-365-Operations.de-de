---
title: Analysieren der Shopleistung
description: In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblick zu Speicherleistung basierend auf Ihrer Dynamics 365 Commerce-Daten zu erhalten.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4688d3268986a9ae6fb2c9601396b56aacf87a93
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009617"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="7547a-103">Analysieren der Leistung des Geschäfts</span><span class="sxs-lookup"><span data-stu-id="7547a-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7547a-104">In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblick zu Speicherleistung basierend auf Ihrer Dynamics 365 Commerce-Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7547a-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="7547a-105">In Retail können Benutzer die Shopleistung in Echtzeit auf unterschiedlichen Ebenen der Organisationshierarchie für eine ausgewählte Periode überprüfen, indem sie den vordefinierten Bericht **Kanalzusammenfassung** an einer der folgenden Stellen öffnen:</span><span class="sxs-lookup"><span data-stu-id="7547a-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="7547a-106">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht Kanalzusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="7547a-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="7547a-107">**Finanzdaten für den Einzelhandelsshop**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Finanzdaten für den Einzelhandelsshop** &gt; **Berichte** &gt; **Bericht Kanalzusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="7547a-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="7547a-108">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht Kanalzusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="7547a-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="7547a-109">Der Bericht enthält eine Momentaufnahme der folgenden Zusammenfassungen im Rahmen der Shopleistung:</span><span class="sxs-lookup"><span data-stu-id="7547a-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="7547a-110">Übersicht Bruttoverkäufe</span><span class="sxs-lookup"><span data-stu-id="7547a-110">Gross sales summary</span></span>
- <span data-ttu-id="7547a-111">Übersicht Zahlungsmitteltyp</span><span class="sxs-lookup"><span data-stu-id="7547a-111">Tender type summary</span></span>
- <span data-ttu-id="7547a-112">Steuerzusammenfassung</span><span class="sxs-lookup"><span data-stu-id="7547a-112">Tax summary</span></span>
- <span data-ttu-id="7547a-113">Preisüberschreibungsübersicht</span><span class="sxs-lookup"><span data-stu-id="7547a-113">Price overrides summary</span></span>
- <span data-ttu-id="7547a-114">Rabattübersicht</span><span class="sxs-lookup"><span data-stu-id="7547a-114">Discounts summary</span></span>
