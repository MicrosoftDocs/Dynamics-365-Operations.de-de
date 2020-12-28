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
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8d95bb0927de5a1906efe180cb9e725c380a724f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412635"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="d56c7-103">Analysieren der Leistung des Geschäfts</span><span class="sxs-lookup"><span data-stu-id="d56c7-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d56c7-104">In diesem Artikel wird beschrieben, wie Sie die Echtzeitanalyse und Analyse im Arbeitsspeicher verwenden können, um Einblick zu Speicherleistung basierend auf Ihrer Dynamics 365 Commerce-Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d56c7-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="d56c7-105">In Retail können Benutzer die Shopleistung in Echtzeit auf unterschiedlichen Ebenen der Organisationshierarchie für eine ausgewählte Periode überprüfen, indem sie den vordefinierten Bericht **Kanalzusammenfassung** an einer der folgenden Stellen öffnen:</span><span class="sxs-lookup"><span data-stu-id="d56c7-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="d56c7-106">**Einzelhandelsshopleitung**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Einzelhandelsshopleitung** &gt; **Berichte** &gt; **Bericht Kanalzusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="d56c7-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="d56c7-107">**Finanzdaten für den Einzelhandelsshop**-Arbeitsbereich &gt; **Einzelhandel** &gt; **Kanäle** &gt; **Finanzdaten für den Einzelhandelsshop** &gt; **Berichte** &gt; **Bericht Kanalzusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="d56c7-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="d56c7-108">**Abfragen und Berichte**-Abschnitt &gt; **Einzelhandel** &gt; **Abfragen und Berichte** &gt; **Umsatzberichte** &gt; **Bericht Kanalzusammenfassung**</span><span class="sxs-lookup"><span data-stu-id="d56c7-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="d56c7-109">Der Bericht enthält eine Momentaufnahme der folgenden Zusammenfassungen im Rahmen der Shopleistung:</span><span class="sxs-lookup"><span data-stu-id="d56c7-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="d56c7-110">Übersicht Bruttoverkäufe</span><span class="sxs-lookup"><span data-stu-id="d56c7-110">Gross sales summary</span></span>
- <span data-ttu-id="d56c7-111">Übersicht Zahlungsmitteltyp</span><span class="sxs-lookup"><span data-stu-id="d56c7-111">Tender type summary</span></span>
- <span data-ttu-id="d56c7-112">Steuerzusammenfassung</span><span class="sxs-lookup"><span data-stu-id="d56c7-112">Tax summary</span></span>
- <span data-ttu-id="d56c7-113">Preisüberschreibungsübersicht</span><span class="sxs-lookup"><span data-stu-id="d56c7-113">Price overrides summary</span></span>
- <span data-ttu-id="d56c7-114">Rabattübersicht</span><span class="sxs-lookup"><span data-stu-id="d56c7-114">Discounts summary</span></span>
